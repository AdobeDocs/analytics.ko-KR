---
title: FTP 및 SFTP 서버에 대한 보안 요구 사항
description: FTP 및 SFTP 서버의 보안 요구 사항에 대해 알아봅니다.
feature: Data Configuration and Collection
role: Admin
source-git-commit: 26ae4edacbc3591d4d3358afe009bf7831d45efb
workflow-type: tm+mt
source-wordcount: '1899'
ht-degree: 2%

---

# FTP 및 SFTP 서버에 대한 보안 요구 사항

이 페이지에서는 Adobe Analytics 데이터 피드 또는 Data Warehouse에서 제공하는 데이터를 수신하는 기존 FTP 및 SFTP 서버에 대한 보안 요구 사항을 다룹니다.

* **기존 FTP 서버**: 아래 섹션에 설명된 대로 SFTP를 사용하도록 업그레이드해야 합니다. [SFTP를 사용하도록 FTP 서버 업그레이드](#upgrade-ftp-servers-to-use-sftp).

  SFTP를 통해 보안을 강화할 수 있으므로 FTP에서 SFTP로 업그레이드하는 것이 필수입니다.

  또는 더 높은 수준의 보안을 위해 최신 클라우드 대상으로 전환할 수 있습니다. 자세한 내용은 [클라우드 가져오기 및 내보내기 계정 구성](https://experienceleague.adobe.com/ko/docs/analytics/components/locations/configure-import-accounts)을 참조하십시오.

* **기존 SFTP 서버(및 새로 업그레이드된 SFTP 서버)**: 아래 섹션에 설명된 대로 이전 암호를 회전해야 합니다. [SFTP 암호 회전](#rotate-your-sftp-password).

  SFTP 암호의 정기적 순환은 데이터를 보호하는 데 도움이 되는 보안 모범 사례입니다.

>[!IMPORTANT]
>
>이 문서의 단계를 완료하기 전에 다음 상황을 고려하십시오.
>
>* **가능한 경우 Adobe은 SFTP로 업그레이드하지 않고 최신 클라우드 대상으로 전환할 것을 권장합니다.**
>FTP 및 SFTP는 기존 대상 유형입니다. 이 문서에 설명된 대로 FTP 계정을 SFTP로 업그레이드하고 SFTP 암호를 순환하지 않고, Adobe에서 최신 클라우드 대상 유형(예: Amazon S3, Google Cloud Platform 또는 Azure)으로 이동하는 것이 좋습니다. 이러한 클라우드 대상은 더 높은 수준의 보안을 제공합니다. 자세한 내용은 [클라우드 가져오기 및 내보내기 계정 구성](https://experienceleague.adobe.com/ko/docs/analytics/components/locations/configure-import-accounts)을 참조하십시오.
>
>* **FTP 및 SFTP 계정이 분류에만 사용되는 경우 분류 세트로 마이그레이션하십시오.**
>FTP 또는 SFTP 계정이 분류에만 사용되는 경우 이 문서에 설명된 대로 FTP 계정을 SFTP로 업그레이드하고 SFTP 암호를 순환하지 않고 **분류 가져오기**&#x200B;에서 **분류 세트**(으)로 마이그레이션해야 합니다. 분류 가져오기는 더 이상 사용되지 않으며 **2026년 8월 31일** 이후에 더 이상 액세스할 수 없습니다. 자세한 내용은 [분류 집합 개요](https://experienceleague.adobe.com/en/docs/analytics/components/classifications/sets/overview)를 참조하십시오.

## 사전 요구 사항

### FTP 계정 인벤토리 작성

SFTP를 사용하도록 FTP 서버를 업그레이드할 때 이 페이지에 설명된 프로세스는 데이터 피드 및 Data Warehouse에 사용 중인 모든 FTP 사이트에 대해 완료해야 합니다.

따라서 데이터 피드 또는 Data Warehouse에 대한 데이터를 받는 모든 FTP 계정을 식별해야 합니다. 이 정보는 문서 [클라우드 가져오기 및 내보내기 계정 구성](/help/components/locations/configure-import-accounts.md#configure-a-location-account)의 [기존 계정 유형](/help/components/locations/configure-import-accounts.md) 섹션에 설명된 대로 FTP 구성 설정에 표시됩니다.

각 계정에 대해 다음 정보를 수집합니다.

* **호스트**: 계정이 연결되는 FTP 서버의 호스트 이름입니다(예: `ftp.omniture.com`, `ftp2.omniture.com` 등).

* **포트**: Adobe에서 호스팅하는 SFTP 서버를 사용하는 경우 SFTP 클라이언트가 포트 22에 연결됩니다. 비보안 FTP 연결은 포트 21을 사용합니다.

* **사용자 이름**: FTP 서버에 로그인할 때 사용하는 사용자 이름입니다.

* **위치 계정 암호**: 계정의 현재 계정 암호입니다. FTP 위치로 전달된 데이터를 다운로드할 때 현재 사용하는 계정 암호(암호)입니다. 이 정보는 Adobe Analytics 인터페이스에서 사용할 수 없습니다.

### 도구에서 자격 증명을 업데이트할 수 있는지 확인합니다

SFTP 사이트에 연결하는 데 사용하는 도구 또는 스크립트(예: SFTP 클라이언트, 자동화된 스크립트 또는 타사 플랫폼)에서 SFTP 암호를 업데이트할 수 있는지 확인하십시오.

모든 클라이언트는 암호로 SFTP를 통해 폴백으로 연결해야 합니다.

## SFTP를 사용하도록 FTP 서버 업그레이드

>[!IMPORTANT]
>
>FTP 데이터가 타사 파트너(예: 컨설팅 회사 또는 분석 공급업체)에 전달되는 경우 이 문서의 단계를 따르기 전에 해당 파트너와 조율하십시오.

### 1단계: 데이터 다운로드를 위한 조직의 SSH 키 생성

이 섹션에서는 SFTP 서버에서 **데이터를 다운로드**&#x200B;하는 데 사용되는 조직의 SSH 키(공개/개인 키 쌍)를 생성하는 방법에 대해 설명합니다.

>[!NOTE]
>
>향후 단계에서는 Adobe에서 제공하는 다른 공개 키를 다운로드합니다. 두 번째 공개/개인 키 쌍의 일부입니다. 이 쌍은 Adobe에서 SFTP 서버로 **데이터를 업로드**&#x200B;하는 데 사용됩니다.

FTP 서버에서 데이터를 다운로드하기 위한 보안 전송을 설정하려면:

1. FTP 서버에서 데이터를 다운로드하는 워크스테이션에 로그인합니다.

1. 보안 전송에 사용할 공개/개인 키 쌍을 생성합니다.

   Adobe에서 호스팅하는 FTP 서버를 사용하는 경우 Adobe은 RSA 및 ED25519 키를 지원합니다.

   * **Linux 환경에서**: 다음 명령을 실행하여 ed25519 키 쌍을 생성합니다.

     ```
     ssh-keygen -t ed25519 -C "your-comment-or-email"
     ```

     정책에서 ed25519 키 사용을 허용하지 않는 경우 다음 명령을 실행하여 RSA 키 쌍을 생성합니다.

     ```
     ssh-keygen -t rsa -b 4096 -C "your-comment-or-email"
     ```

   * **Windows 환경에서**: PuTTYgen을 사용합니다.

1. [!DNL `authorized_keys`]라는 파일 (확장명 없음)을 만듭니다.

1. 공개 키의 내용을 [!DNL `authorized_keys`] 파일에 복사합니다.

1. 이후 단계에서는 이 [!DNL `authorized_keys`] 파일로 돌아와 Adobe의 공개 키를 추가합니다. 이 공개 키는 Adobe에서 데이터를 SFTP 서버에 업로드하는 데 사용됩니다. [!DNL `authorized_keys`] 파일을 SFTP 서버에 추가합니다.

### 2단계: Adobe Analytics에서 새 SFTP 위치 계정 만들기

새로운 SFTP 위치 계정을 만들어 각각의 기존 FTP 계정을 바꿉니다.

새 SFTP 위치 계정을 만들 때 바꿀 기존 FTP 계정에서 사용하는 동일한 호스트 이름과 사용자 이름을 사용해야 합니다.

>[!NOTE]
>
>이후 단계에서는 데이터 피드 및 Data Warehouse 게재의 대상으로 사용하도록 이 새 위치 계정을 구성합니다.

#### SFTP 계정 만들기

1. Adobe Analytics에서 [!UICONTROL **구성 요소**] > [!UICONTROL **위치**](으)로 이동합니다.

1. [!UICONTROL **위치 계정**] 탭을 선택합니다.

1. [!UICONTROL **계정 추가**]&#x200B;를 선택합니다.

1. [!UICONTROL **계정 유형**] 드롭다운 필드에서 [!UICONTROL **SFTP(기존)**]&#x200B;을(를) 선택합니다.

1. 다음 필드를 완료합니다. 

   | 필드 이름 | 함수 |
   |---------|----------|
   | [!UICONTROL **호스트 이름**] | SFTP 호스트 이름(예: `ftp.omniture.com`)입니다. |
   | [!UICONTROL **포트**] | 데이터를 전송할 방화벽 포트입니다. Adobe 호스팅 SFTP 연결용 포트 22입니다. |
   | [!UICONTROL **사용자 이름**] | SFTP 사용자 이름. FTP 계정에 사용한 사용자 이름과 동일한 사용자 이름을 사용합니다. |

1. [!UICONTROL **저장**]&#x200B;을 선택합니다.

1. [!UICONTROL **계정 만들기**] 대화 상자에서 RSA 또는 ed25519 공개 키를 다운로드한 다음 **[!UICONTROL 확인]**&#x200B;을 선택합니다. Adobe에서 SFTP 서버에 데이터를 업로드하는 데 사용하는 SSH 공개 키입니다. (다음 섹션에서 이 키를 사용합니다. [Adobe의 SSH 공개 키를 SFTP 서버에 추가](#add-adobes-ssh-public-key-to-the-sftp-server).)

1. 생성하려는 각 SFTP 계정에 대해 이 프로세스를 반복합니다.

1. [SFTP 서버에 공개 키 업로드](#upload-the-public-key-to-the-sftp-server) 섹션을 계속합니다.

#### Adobe의 SSH 공개 키를 `authorized_keys` 파일에 추가하고 FTP 서버에 업로드합니다.

이전 섹션의 7단계에서 방금 다운로드한 공개 키는 Adobe에서 SFTP 서버로 **데이터를 업로드**&#x200B;하는 데 사용하는 공개/개인 키 쌍의 일부입니다.

이 공개 키를 이전에 조직의 다운로드 키(`authorized_keys`1단계: 조직의 다운로드 키를 생성하여 FTP 서버에 추가[에서 생성한 키)를 추가한 것과 동일한 ](#step-1-generate-your-organizations-download-key-and-add-it-to-your-ftp-server) 파일에 추가해야 합니다.

Adobe의 SSH 공개 키를 `authorized_keys` 파일에 추가하고 FTP 서버에 업로드하려면 다음을 수행하십시오.

1. FTP 서버에서 데이터를 다운로드하는 워크스테이션에 로그인합니다.

1. [!DNL `authorized_keys`] 파일을 열고 Adobe의 업로드 키를 추가합니다. 이 파일에는 [1단계: 조직의 다운로드 키를 생성하여 FTP 서버에 추가](#step-1-generate-your-organizations-download-key-and-add-it-to-your-ftp-server)에서 조직의 다운로드 키가 이미 포함되어 있어야 합니다.

1. [!DNL `authorized_keys`] 파일을 FTP 서버에 업로드합니다.

   1. FTP 서버에 연결하고 사용자 이름과 암호로 로그인합니다.\
      Adobe에서 호스팅하는 FTP 서버이거나 자체 FTP 서버일 수 있습니다.
   1. [!DNL .ssh] 디렉토리가 없는 경우 디렉토리를 만듭니다.
   1. [!DNL `authorized_keys`] 파일을 [!DNL .ssh] 디렉토리에 업로드합니다.

1. SFTP 서버에서 인바운드 연결을 허용하도록 방화벽 설정을 업데이트합니다. Adobe에서 호스팅하는 SFTP 서버를 사용하는 경우 포트 22에서 Adobe의 IP 범위에서 인바운드 연결을 허용합니다.

1. SFTP 클라이언트를 사용하여 서버에 로그인하여 연결을 테스트합니다.

1. 이전 섹션 [SFTP 계정 만들기](#create-the-sftp-account)에서 만든 각 SFTP 계정에 대해 이 프로세스를 반복합니다.

1. [계정 내에 위치 추가](#add-a-location-within-the-account) 섹션을 계속합니다.

#### 계정 내에 위치 추가

1. **위치** 탭에서 **위치 추가**&#x200B;를 선택합니다.

1. 이름, 설명 및 이 위치를 데이터 피드와 함께 사용할지 Data Warehouse과 함께 사용할지 여부를 지정합니다.

1. [!UICONTROL **위치 계정**] 필드에서 방금 만든 계정을 선택합니다.

1. [!UICONTROL **디렉터리 경로**] 필드에서 SFTP 서버의 디렉터리 경로를 지정합니다. 경로에 폴더가 이미 있어야 합니다. 그렇지 않으면 오류가 발생합니다. (예: `/folder_name/folder_name`)

1. **저장**&#x200B;을 선택합니다.

1. 생성한 각 SFTP 계정에 대해 이 프로세스를 반복합니다.

자세한 지침은 [클라우드 가져오기 및 내보내기 위치 구성](https://experienceleague.adobe.com/ko/docs/analytics/components/locations/configure-import-locations)을 참조하십시오.

### 3단계: 새 SFTP 대상을 사용하도록 데이터 피드 및 Data Warehouse 요청 편집

사용자가 만든 새 SFTP 대상을 사용하도록 현재 FTP 대상에 데이터를 보내는 기존의 예약된 데이터 피드 및 Data Warehouse 요청을 업데이트합니다.

#### 데이터 피드 편집

새 SFTP 대상을 사용하도록 이전 FTP 대상으로 구성된 각 예약된 데이터 피드를 편집합니다.

1. Adobe Analytics에서 [!UICONTROL **관리자**] > [!UICONTROL **데이터 피드**]&#x200B;를 선택합니다.

1. 편집할 데이터 피드를 찾습니다. 데이터 피드를 찾으려면 [데이터 피드 목록을 필터링하고 검색](#filter-and-search-the-list-of-data-feeds)할 수 있습니다.

1. [!UICONTROL **피드 이름**] 열에서 데이터 피드를 선택하십시오.

   [!UICONTROL **_feed_name_**] 편집 페이지가 표시됩니다.

1. [!UICONTROL **대상**] 섹션의 [!UICONTROL **계정**] 필드에서 드롭다운 메뉴를 사용하여 만든 새 SFTP 대상을 선택합니다.

1. [!UICONTROL **위치**] 필드에서 드롭다운 메뉴를 사용하여 SFTP 계정의 위치를 선택합니다.

1. [!UICONTROL **저장**]&#x200B;을 선택합니다.

자세한 내용은 [데이터 피드 관리](/help/export/analytics-data-feed/df-manage-feeds.md#edit-a-data-feed)에서 [데이터 피드 편집](/help/export/analytics-data-feed/df-manage-feeds.md)을 참조하세요.

#### Data Warehouse 요청 편집

새 SFTP 대상을 사용하도록 이전 FTP 대상으로 구성된 각 예약된 Data Warehouse 요청을 편집합니다.

1. Adobe Analytics에서 [!UICONTROL **도구**] > [!UICONTROL **Data Warehouse**]&#x200B;을(를) 선택합니다.

1. Data Warehouse 페이지에서 편집할 요청을 선택합니다.

   ![요청 관리](assets/dw-manage-request.png)

1. [!UICONTROL **편집**]&#x200B;을 선택합니다.

1. [!UICONTROL **보고서 대상**] 탭을 선택합니다.

1. [!UICONTROL **계정**] 필드에서 드롭다운 메뉴를 사용하여 만든 새 SFTP 대상을 선택합니다.

1. [!UICONTROL **위치**] 필드에서 드롭다운 메뉴를 사용하여 SFTP 계정의 위치를 선택합니다.

1. [!UICONTROL **변경 내용 저장**]&#x200B;을 선택합니다.

자세한 내용은 [Data Warehouse 요청 관리](/help/export/data-warehouse/data-warehouse-requests-manage.md#edit-requests)에서 [요청 편집](/help/export/data-warehouse/data-warehouse-requests-manage.md)을 참조하세요.

### 4단계: 방화벽 설정 업데이트

아직 업데이트하지 않았다면 다음과 같이 방화벽 설정을 업데이트해야 합니다.

* **Adobe의 FTP 서버를 사용하는 경우**: 포트 22에서 **아웃바운드** 연결을 허용하도록 방화벽 설정을 업데이트해야 합니다.

* **자체 FTP 서버를 사용하는 경우**: 서비스를 호스팅하는 모든 포트(일반적으로 포트 22)에서 **인바운드** 연결을 허용하도록 방화벽 설정을 업데이트해야 합니다.

또한 포트 21에서 인바운드 연결 허용과 같은 이전 FTP 관련 규칙을 제거해야 합니다. (FTP는 포트 21과 데이터 전송을 위한 다양한 추가 포트를 사용합니다. 보안 모범 사례로서 방화벽을 통해 이러한 불필요한 액세스를 제거해야 합니다.)

### 5단계: 예약된 데이터 피드 및 Data Warehouse 요청이 올바르게 전달되고 있는지 확인

새 SFTP 계정 및 위치를 사용하도록 각 기존 데이터 피드 및 Data Warehouse 요청을 업데이트한 후, 다음 예약된 배달을 기다립니다. 데이터가 예상대로 새 대상에 도착하는지 확인합니다.

### 6단계: 업그레이드된 SFTP 서버에서 암호 회전

FTP 서버를 SFTP로 업그레이드한 후 다음 섹션 [SFTP 암호 회전](#rotate-your-sftp-password)에 설명된 대로 SFTP 암호도 회전해야 합니다.

## SFTP 암호 회전

SFTP 암호는 키 기반 인증이 실패할 경우 대체 인증 방법으로 사용됩니다.

FTP에서 SFTP로 업그레이드한 후 바로 SFTP 암호를 회전합니다. 설정된 정책에 따라 정기적으로 계속 회전해야 합니다.

1. Adobe 고객 지원 센터에 문의하여 새 암호를 요청합니다.

1. 각 SFTP 계정에 대해 **호스트 이름** 및 **사용자 이름**&#x200B;을 제공하십시오.

   고객 지원 센터에서 각 FTP 계정에 대해 새 암호를 생성합니다.

1. SFTP 서버에 연결하는 데 사용하는 클라이언트에서 암호를 업데이트합니다.


<!--
< **_Ignore everything after this_** >

-------

## Set up a new SFTP server or upgrade your existing FTP server

## Upgrade your FTP server to use SFTP where files are delivered or FTP account to use SFTP

Set up an SFTP server where Data Feed and Data Warehouse files can be delivered. This could beYou first need to upgrade your FTP server to use SFTP To upgrade an FTP account to use SFTP, follow the steps in [Connect to an FTP account with SFTP](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-connect.md).

## Create an SFTP account

## Rotate the passphrase on SFTP accounts


 
Adobe recommends that you periodically rotate the account secrets (passwords) on your FTP accounts that are associated with Data Feeds and Data Warehouse. 
 
Regular rotation of account secrets is a security best practice that helps protect your data. 
 
To ensure uninterrupted reception of data, follow the steps in [Prepare to rotate account secrets](#prepare-to-rotate-account-secrets) prior to changing any account secrets.  
 
>[!IMPORTANT] 
> 
>If your FTP data is delivered to a third-party partner (for example, a consulting firm or Adobe Analytics vendor), coordinate with them before rotating account secrets. The third-party partner will need to update their own tools and scripts with the new account secrets immediately after the new account secrets are provided by your FTP host provider (either Adobe or another provider).

## When rotating account secrets is not necessary 
 
### Transition from FTP to a cloud destination 
 
FTP and SFTP are legacy destination types. Rather than rotating FTP account secrets, Adobe recommends moving to a modern cloud destination type (such as Amazon S3, Google Cloud Platform, or Azure), which provide a higher level of security. For more information, see [Configure cloud import and export accounts](https://experienceleague.adobe.com/en/docs/analytics/components/locations/configure-import-accounts). 
 
### Transition from the Classifications importer to Classification sets 
 
If your FTP account is used exclusively for Classifications, you should migrate from the **Classifications importer** to **Classification sets**, rather than rotating your FTP account secrets. The Classification importer will be deprecated and no longer accessible after **August 31, 2026**. For more information, see [Classification sets overview](https://experienceleague.adobe.com/en/docs/analytics/components/classifications/sets/overview). 

## Prepare to rotate account secrets 
 
Complete the following steps before attempting to rotate FTP account secrets: 
 
### Step 1: Inventory your FTP accounts 
 
Identify all FTP accounts that are receiving data for Data Feeds or Data Warehouse. This information is shown in your FTP configuration settings, as described in the [Legacy account types](/help/components/locations/configure-import-accounts.md#configure-a-location-account) section of the article [Configure cloud import and export accounts](/help/components/locations/configure-import-accounts.md). 
 
For each account, gather the following information: 
 
* **Host**: The FTP destination of the host your account connects to (for example, `ftp.omniture.com`, `ftp2.omniture.com`, and so forth). 
 
* **Port**: SFTP clients connect on port 22. FTP connections that are non-secure use port 21. 
 
* **Username**: The username used to log in to the FTP site. 
 
* **location account secret**: The current account secret for the account. This is the account secret (password) that you use currently when downloading data delivered to your FTP location. This information is not available from the Adobe Analytics interface. 
 
 
### Step 2: Confirm that you can update credentials in your tools 
 
Make sure you can update the FTP account secret in whatever tool or script you use to connect to the FTP site (for example, an FTP client, automated script, or third-party platform). 
 
### Step 3: Create FTP cloud location accounts with your current credentials 
 
Create new FTP cloud location accounts to replace your existing FTP location accounts. These new accounts will be used as the destination for your Data Feeds and Data Warehouse deliveries.  
 
When creating the new FTP accounts, you must use the same hostname, username, and account secret that are used in your existing FTP accounts. 
 
#### Create each FTP account 
 
1. In Adobe Analytics, go to **Components** > **Locations**. 
 
1. Select the **Location accounts** tab. 
 
1. Select **Add account**. 
 
1. In the **Account type** drop-down field, select **FTP (legacy)**. 
 
1. Complete the following fields: 

   | Field name | Function |
   |---------|----------|
   | **Hostname** |  Your Adobe FTP hostname (for example, `ftp.omniture.com`). | 
   | **Port** | SFTP clients connect on port 22. FTP connections that are non-secure use port 21. | 
   | **Username** | Your current FTP username. |
   | **Location account secret** | Your current FTP account secrets (password).  |
 
1. Select **Save**. 
 
Repeat this process for each FTP account. 
 
For detailed instructions, see [Configure cloud import and export accounts](https://experienceleague.adobe.com/en/docs/analytics/components/locations/configure-import-accounts). 
 
#### Add a location within the account 
 
1. On the **Locations** tab, select **Add location**. 
 
1. Specify a name, description, and whether this location will be used with Data Feeds or Data Warehouse. 
 
1. In the [!UICONTROL **Location account**] field, select the account you just created. 
 
1. In the [!UICONTROL **Directory path**] field, specify the path to the directory on the FTP server. Folders must already exist; feeds throw an error if the specified path does not exist. For example, `/folder_name/folder_name`. 
 
1. Select **Save**. 
 
Repeat this process for each location. 
 
For detailed instructions, see [Configure cloud import and export locations](https://experienceleague.adobe.com/en/docs/analytics/components/locations/configure-import-locations). 
 
### Step 4: Reference the new FTP cloud accounts from any scheduled Data Feeds and Data Warehouse requests 
 
Update any existing scheduled Data Feeds and Data Warehouse requests to use the FTP cloud accounts you created.  
 
* **Data Feeds**: Go to **Admin** > **Data Feeds**, edit each scheduled  Data Feed that uses an FTP account, then change the destination to the newly created FTP cloud account. 
 
  For detailed instructions, see [Edit a data feed](/help/export/analytics-data-feed/df-manage-feeds.md#edit-a-data-feed) in [Manage data feeds](/help/export/analytics-data-feed/df-manage-feeds.md). 
 
* **Data Warehouse**: Go to **Tools** > **Data Warehouse**, edit each scheduled Data Warehouse request that uses an FTP account, then change the report destination to the newly created FTP cloud account. 
 
  For detailed instructions, see [Edit requests](/help/export/data-warehouse/data-warehouse-requests-manage.md#edit-requests) in [Manage Data Warehouse requests](/help/export/data-warehouse/data-warehouse-requests-manage.md). 
 
### Step 5: Ensure that scheduled Data Feeds and Data Warehouse requests are being delivered correctly. 
 
After updating each existing Data Feed and Data Warehouse request to use the new FTP account and location, wait for the next scheduled delivery. Verify that data arrives at the new destination as expected. 

## Request a new account secret 
 
>[!IMPORTANT] 
>
>Before requesting a new account secret, consider the following:
>
>* The steps in this section apply only if you are using an Adobe-provided FTP account. For example, the FTP hostname is `ftp.omniture.com`, `ftp2.omniture.com` or similar.   If your FTP hostname is not provided by Adobe, please contact your FTP host provider for details on changing the account secret.
> 
>* Request a new account secret only after you complete all the preparation steps described in [Prepare to rotate account secrets](#prepare-to-rotate-account-secrets). 
>
>* After Adobe Customer Care or your third-party FTP host provider provides a new account secret, the old account secret is immediately invalidated. There is no way to revert to the previous account secret. 
>
 
To request a new account secret from Adobe: 
 
1. Contact Adobe Customer Care. 
 
1. For each FTP account, provide the **Hostname** and **Username** for each account that needs a new account secret. 
 
   Customer Care will generate a new account secret for each FTP account. 

1. Continue immediately with the following section, [After you receive the new account secret](#after-you-receive-the-new-account-secret).
 
## After you receive the new account secret 
 
Act immediately after receiving the new credentials. Any delay results in failed deliveries for active Data Feeds and Data Warehouse requests. 
 
### Step 1: Update your tools and scripts 
 
Update the FTP account secret in any tool, script, or automated process that connects to the FTP account. Make sure all team members and third-party partners who access the account are notified. 
 
### Step 2: Update your cloud location accounts 
 
1. In Adobe Analytics, go to **Components** > **Locations**. 

1. Select the **Location accounts** tab. 

1. Find the FTP account that you created in Step 3 of section, [Prepare to rotate account secrets](#prepare-to-rotate-account-secrets).

1. Select **Edit details**. 

1. Enter the new account secret and confirm it. 

1. Select **Save**. 
 
Repeat this process for each account that was reset. 

For more detailed information about this process, see [Configure cloud import and export accounts](https://experienceleague.adobe.com/en/docs/analytics/components/locations/configure-import-accounts).
 
### Step 3: Test your connections 
 
Verify that your Data Feeds or Data Warehouse requests that use the FTP account are working correctly with the new account secret. 
 
>[!TIP] 
> 
>If your current tools use SFTP with SSH keys that haven't been recently rotated, consider rotating those keys as well.

 
## Troubleshooting 
 
If something goes wrong after the account secret is rotated and you cannot restore connectivity, you can create a new FTP account. After the new account is set up, point your Data Feed or Data Warehouse request to the new account and update your cloud location accordingly. 

For information about how to create an FTP account, see [Configure cloud import and export accounts](https://experienceleague.adobe.com/en/docs/analytics/components/locations/configure-import-accounts).

To set up secure transfer with your FTP server: 

1. Generate a public/private key pair to use for secure transfer.

   This process differs depending on whether your FTP server is Adobe-hosted or self-hosted:

   +++ For an Adobe-hosted FTP server:

   Generate a public/private key pair: 
   
      * **In a Linux environment**: Run the following command to generate the ed25519 key pair: 

        ```
        ssh-keygen -t ed25519 -C "your-comment-or-email"
        ```

        If your policy does not allow you to use ed25519 keys, run the following command to generate the RSA key pair (**Note:** The RSA key typically applies to customers who operate under FIPS 186-4, as ed25519 is first supported in the newer FIPS 186-5):

        ```
        ssh-keygen -t rsa -b 4096 -C "your-comment-or-email"
        ```

      * **In a Windows environment**: Use PuTTYgen.

   +++

   +++ For a self-hosted FTP server: 
   
   If you want to set up secure transfer with your own FTP server, you must have an SFTP hostname, username, and SFTP account within Adobe Analytics that contains a valid RSA or ed25519 public key from Adobe. This key must be installed on your SFTP server. You download this public key as part of the process of [creating the SFTP account](#create-the-sftp-account).

   +++

1. Create a file named [!DNL `authorized_keys`] (no extension).



3 basic steps: Set up SFTP on customer side, then on Adobe side, then change passphrase. 

1. FTP site: ftp.omniture.com - Using username/password to connect. Adobe uses the same username/password to connect to the site.

2. user can then upload their public key to that server, then start connecting to that server with their private key using SFTP. (They also need to open Port 22 in the firewall and they would close the other ports they don't need.)

3. In Locations, create a new location, use the same username. 

4. After they create that location, we give them our public key, and they have to install it on their SFTP server.

5. Then they switch all their data feeds to use the new Location. And then we'll use SFTP to send the data. 

6. Then they call Customer Care to get new passphrase (rotate passphrase), and then they change the passphrase on their side. Passphrase is only used if SSH fails (they have the wrong keys--a bad actor could use bad keys and then use the password. But they don't have to coordinate the switching of the passphrase with installation of SFTP. )


If they're using a third-party to do this, the third-party would need to set up SFTP - This is the same as we have documented right now. It doesn't have to be immediate, though, like we were assuming before. 


If it's they're own FTP site, it would be the same. They would need to start using SFTP with their FTP server, then get our public key and install it on their server. Shouldn't matter if the FTP site is hosted by Adobe or not. 

-->

