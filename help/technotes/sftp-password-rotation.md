---
title: FTP 및 SFTP 서버에 대한 보안 요구 사항
description: FTP 및 SFTP 서버의 보안 요구 사항에 대해 알아봅니다.
feature: Data Configuration and Collection
role: Admin
source-git-commit: 94059a3b7d667fafe1900a4a9c82ed931d769df1
workflow-type: tm+mt
source-wordcount: '1933'
ht-degree: 3%

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
>* **가능한 경우 Adobe에서는 SFTP로 업그레이드하지 않고 최신 클라우드 대상으로 전환할 것을 권장합니다.**
>FTP 및 SFTP는 기존 대상 유형입니다. 이 문서에 설명된 대로 FTP 계정을 SFTP로 업그레이드하고 SFTP 암호를 순환하지 않고, Adobe에서 최신 클라우드 대상 유형(예: Amazon S3, Google Cloud Platform 또는 Azure)으로 이동하는 것이 좋습니다. 이러한 클라우드 대상은 더 높은 수준의 보안을 제공합니다. 자세한 내용은 [클라우드 가져오기 및 내보내기 계정 구성](https://experienceleague.adobe.com/ko/docs/analytics/components/locations/configure-import-accounts)을 참조하십시오.
>
>* **FTP 및 SFTP 계정이 분류에만 사용되는 경우 분류 세트로 마이그레이션하십시오.**
>FTP 또는 SFTP 계정이 분류에만 사용되는 경우 이 문서에 설명된 대로 FTP 계정을 SFTP로 업그레이드하고 SFTP 암호를 순환하지 않고 **분류 가져오기**&#x200B;에서 **분류 세트**(으)로 마이그레이션해야 합니다. 분류 가져오기는 더 이상 사용되지 않으며 **2026년 8월 31일** 이후에 더 이상 액세스할 수 없습니다. 자세한 내용은 [분류 집합 개요](https://experienceleague.adobe.com/en/docs/analytics/components/classifications/sets/overview)를 참조하십시오.

## 사전 요구 사항

### FTP 계정 인벤토리 작성

데이터 피드 또는 Data Warehouse과 함께 사용되는 모든 FTP 사이트에 대해 이 페이지에서 SFTP 업그레이드 단계를 완료해야 합니다.

따라서 데이터 피드 또는 Data Warehouse에 대한 데이터를 받는 모든 FTP 계정을 식별해야 합니다. 이 정보는 문서 [클라우드 가져오기 및 내보내기 계정 구성](/help/components/locations/configure-import-accounts.md)의 [기존 계정 유형](/help/components/locations/configure-import-accounts.md#configure-a-location-account) 섹션에 설명된 대로 FTP 구성 설정에 표시됩니다.

각 계정에 대해 다음 정보를 수집합니다.

* **호스트**: 계정이 연결되는 FTP 서버의 호스트 이름입니다(예: `ftp.omniture.com`, `ftp2.omniture.com` 등).

* **포트**: Adobe에서 호스팅하는 SFTP 서버를 사용하는 경우 SFTP 클라이언트가 포트 22에 연결됩니다. 비보안 FTP 연결은 포트 21을 사용합니다.

* **사용자 이름**: FTP 서버에 로그인할 때 사용하는 사용자 이름입니다.

* **위치 계정 암호**: 계정의 현재 계정 암호입니다. FTP 위치로 전달된 데이터를 다운로드할 때 현재 사용하는 계정 암호(암호)입니다. 이 정보는 Adobe Analytics 인터페이스에서 사용할 수 없습니다.

### 도구에서 자격 증명을 업데이트할 수 있는지 확인합니다

SFTP 사이트에 연결하는 데 사용하는 도구 또는 스크립트(예: SFTP 클라이언트, 자동화된 스크립트 또는 타사 플랫폼)에서 SFTP 암호를 업데이트할 수 있는지 확인하십시오.

모든 클라이언트는 SFTP를 통해 암호로 폴백하여 연결해야 합니다.

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

   Adobe에서 호스팅하는 SFTP 서버를 사용하는 경우 Adobe은 RSA 및 ED25519 키를 지원합니다.

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

1. Adobe Analytics에서 [!UICONTROL **구성 요소**] > [!UICONTROL **위치**] (으)로 이동합니다.

1. [!UICONTROL **위치 계정**] 탭을 선택합니다.

1. [!UICONTROL **계정 추가**]&#x200B;를 선택합니다.

1. [!UICONTROL **계정 유형**] 드롭다운 메뉴에서 [!UICONTROL **SFTP(기존)**]&#x200B;을(를) 선택합니다.

1. 다음 필드를 완료합니다.

   | 필드 이름 | 함수 |
   |---------|----------|
   | [!UICONTROL **호스트 이름**] | SFTP 호스트 이름(예: `ftp.omniture.com`)입니다. |
   | [!UICONTROL **포트**] | 데이터를 전송할 방화벽 포트입니다. Adobe 호스팅 SFTP 연결용 포트 22입니다. |
   | [!UICONTROL **사용자 이름**] | SFTP 사용자 이름. FTP 계정에 사용한 사용자 이름과 동일한 사용자 이름을 사용합니다. |

1. [!UICONTROL **저장**]&#x200B;을 선택합니다.

1. [!UICONTROL **계정 만들기**] 대화 상자에서 RSA 또는 ed25519 공개 키를 다운로드한 다음 [!UICONTROL **확인**]&#x200B;을 선택합니다. Adobe에서 SFTP 서버에 데이터를 업로드하는 데 사용하는 SSH 공개 키입니다. (다음 섹션에서 이 키를 사용합니다. [Adobe의 SSH 공개 키를 SFTP 서버에 추가](#add-adobes-ssh-public-key-to-the-sftp-server).)

1. 생성하려는 각 SFTP 계정에 대해 이 프로세스를 반복합니다.

1. [SFTP 서버에 공개 키 업로드](#upload-the-public-key-to-the-sftp-server) 섹션을 계속합니다.

#### Adobe의 SSH 공개 키를 [!DNL `authorized_keys`] 파일에 추가하고 FTP 서버에 업로드합니다.

이전 섹션의 7단계에서 방금 다운로드한 공개 키는 Adobe에서 SFTP 서버로 **데이터를 업로드**&#x200B;하는 데 사용하는 공개/개인 키 쌍의 일부입니다.

이전에 조직의 다운로드 키([1단계: 데이터 다운로드를 위해 조직의 SSH 키 생성](#step-1-generate-your-organizations-ssh-keys-for-downloading-data)에서 생성한 키)를 추가한 것과 동일한 [!DNL `authorized_keys`] 파일에 이 공개 키를 추가해야 합니다.

Adobe의 SSH 공개 키를 [!DNL `authorized_keys`] 파일에 추가하고 FTP 서버에 업로드하려면 다음을 수행하십시오.

1. FTP 서버에서 데이터를 다운로드하는 워크스테이션에 로그인합니다.

1. [!DNL `authorized_keys`] 파일을 열고 Adobe의 업로드 키를 추가합니다. 이 파일에는 [1단계: 데이터 다운로드를 위한 조직의 SSH 키 생성](#step-1-generate-your-organizations-ssh-keys-for-downloading-data)에서 조직의 다운로드 키가 이미 포함되어 있어야 합니다.

1. [!DNL `authorized_keys`] 파일을 FTP 서버에 업로드합니다.

   1. FTP 서버에 연결하고 사용자 이름과 암호로 로그인합니다.
Adobe에서 호스팅하는 FTP 서버이거나 자체 FTP 서버일 수 있습니다.
   1. [!DNL .ssh] 디렉토리가 없는 경우 디렉토리를 만듭니다.
   1. [!DNL `authorized_keys`] 파일을 [!DNL .ssh] 디렉토리에 업로드합니다.

1. SFTP 서버에서 인바운드 연결을 허용하도록 방화벽 설정을 업데이트합니다. Adobe에서 호스팅하는 SFTP 서버를 사용하는 경우 포트 22에서 Adobe의 IP 범위에서 인바운드 연결을 허용합니다.

1. SFTP 클라이언트를 사용하여 서버에 로그인하여 연결을 테스트합니다.

1. 이전 섹션 [SFTP 계정 만들기](#create-the-sftp-account)에서 만든 각 SFTP 계정에 대해 이 프로세스를 반복합니다.

1. [계정 내에 위치 추가](#add-a-location-within-the-account) 섹션을 계속합니다.

#### 계정 내에 위치 추가

1. [!UICONTROL **위치**] 탭에서 [!UICONTROL **위치 추가**]&#x200B;를 선택합니다.

1. 이름, 설명 및 이 위치를 데이터 피드와 함께 사용할지 Data Warehouse과 함께 사용할지 여부를 지정합니다.

1. [!UICONTROL **위치 계정**] 필드에서 방금 만든 계정을 선택합니다.

1. [!UICONTROL **디렉터리 경로**] 필드에서 SFTP 서버의 디렉터리 경로를 지정합니다. 경로에 폴더가 이미 있어야 합니다. 그렇지 않으면 오류가 발생합니다. (예: `/folder_name/folder_name`)

1. [!UICONTROL **저장**]&#x200B;을 선택합니다.

1. 생성한 각 SFTP 계정에 대해 이 프로세스를 반복합니다.

자세한 지침은 [클라우드 가져오기 및 내보내기 위치 구성](https://experienceleague.adobe.com/en/docs/analytics/components/locations/configure-import-locations)을 참조하십시오.

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

자세한 내용은 [데이터 피드 관리](/help/export/analytics-data-feed/df-manage-feeds.md)에서 [데이터 피드 편집](/help/export/analytics-data-feed/df-manage-feeds.md#edit-a-data-feed)을 참조하세요.

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

자세한 내용은 [Data Warehouse 요청 관리](/help/export/data-warehouse/data-warehouse-requests-manage.md)에서 [요청 편집](/help/export/data-warehouse/data-warehouse-requests-manage.md#edit-requests)을 참조하세요.

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


