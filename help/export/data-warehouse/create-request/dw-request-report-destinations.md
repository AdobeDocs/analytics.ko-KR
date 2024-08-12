---
description: Data Warehouse 요청을 만드는 방법을 설명하는 단계입니다.
title: Data Warehouse 요청에 대한 보고서 대상 구성
feature: Data Warehouse
exl-id: 3c7faea3-4d90-4274-88f3-e9337c94155f
source-git-commit: 16a9c9a2b6692b9b1944cfdb9b5b0411d48db666
workflow-type: tm+mt
source-wordcount: '1925'
ht-degree: 84%

---

# Data Warehouse 요청에 대한 보고서 대상 구성

Data Warehouse 요청을 만들 때 사용할 수 있는 다양한 구성 옵션이 있습니다. 다음 정보는 요청에 대한 보고자 대상을 구성하는 방법을 설명합니다.

요청 만들기를 시작하는 방법과 다른 중요 구성 옵션 링크에 대한 자세한 내용은 [Data Warehouse 요청 만들기](/help/export/data-warehouse/create-request/t-dw-create-request.md)을 참조하십시오.

>[!NOTE]
>
>보고서 대상 구성 시 다음과 같은 사항을 고려하십시오.
>
>* 보고서 대상에 클라우드 계정이나 이메일을 사용하는 것이 좋습니다. [이전 FTP 및 SFTP 계정](#legacy-destinations)은 사용할 수 있지만 권장되지 않습니다.
>
>* 이전에 구성한 모든 클라우드 계정을 Data Warehouse에 사용할 수 있습니다. 다음 방법 중 하나로 클라우드 계정을 구성할 수 있습니다.
>
>   * [데이터 피드](/help/export/analytics-data-feed/create-feed.md) 구성할 때
>   
>   * [Adobe Analytics 분류 데이터를 가져올 때](/help/components/locations/locations-manager.md)(계정을 사용할 수 있지만 해당 계정에 구성된 위치는 사용할 수 없음)
>   
>   * [구성 요소 > 위치](/help/components/locations/configure-import-accounts.md)의 위치 관리자에서
>
>* 클라우드 계정은 Adobe Analytics 사용자 계정과 연계되어 있습니다. 다른 사용자는 구성된 클라우드 계정을 사용하거나 볼 수 없습니다.
>
>* [구성 요소 > 위치](/help/components/locations/configure-import-accounts.md)의 위치 관리자에서 생성한 모든 위치를 편집할 수 있습니다.

Data Warehouse 보고서가 전송되는 대상을 구성하려면

1. **[!UICONTROL 도구]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **추가**]&#x200B;를 선택하여 Adobe Analytics에서 요청 만들기를 시작하십시오.

   자세한 내용은 [Data Warehouse 요청 만들기](/help/export/data-warehouse/create-request/t-dw-create-request.md)를 참조하십시오.

1. 새 Data Warehouse 요청 페이지에서 [!UICONTROL **보고서 대상**] 탭을 선택합니다.

   ![보고서 대상 탭](assets/dw-report-destination.png)

1. (조건부) Adobe Analytics에 클라우드 계정(및 해당 계정의 대상)이 이미 구성된 경우, 보고서 대상으로 사용할 수 있습니다.

   >[!NOTE]
   >
   >계정은 귀하가 구성했거나 귀하가 속한 조직과 공유된 경우에만 사용할 수 있습니다.
   >
   >시스템 관리자인 경우, [!UICONTROL **모든 대상 표시**] 옵션을 사용할 수 있습니다. 조직의 사용자가 생성한 모든 계정과 위치에 액세스하려면 이 옵션을 활성화합니다.

   1. [!UICONTROL **계정**] 드롭다운 메뉴에서 계정을 선택합니다.

      Adobe Analytics의 다음 영역 중 하나에서 구성한 모든 클라우드 계정을 사용할 수 있습니다.

      * [스키마](/help/components/classifications/sets/manage/schema.md)에 설명된 대로 Adobe Analytics 분류 데이터를 가져올 때

        하지만 분류 데이터 가져오기에 대해 구성된 위치는 사용할 수 없습니다. 대신 아래 설명된 대로 새 대상을 추가합니다.

      * [클라우드 가져오기 및 내보내기 계정 구성](/help/components/locations/configure-import-accounts.md) 및 [클라우드 가져오기 및 내보내기 위치 구성](/help/components/locations/configure-import-locations.md)에 설명된 대로 위치 영역에서 계정 및 위치를 구성할 때

   1. [!UICONTROL **대상 선택**] 드롭다운 메뉴에서 계정과 연계된 대상을 선택합니다. <!-- Is this correct? -->

1. (조건부) Adobe Analytics에 이미 구성되어 있는 클라우드 계정에 대한 액세스 권한이 없는 경우에 다음 중 하나를 구성할 수 있습니다.

   1. [!UICONTROL **계정**] 드롭다운 메뉴를 선택한 다음 [!UICONTROL **계정 추가**]&#x200B;를 선택합니다.

   1. 계정 추가 대화 상자에서 다음 정보를 지정합니다.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **위치 계정 이름**] | 위치 계정의 이름입니다. 이 이름은 위치를 만들 때 나타납니다 |
      | [!UICONTROL **위치 계정 설명**] | 동일한 계정 유형의 다른 계정과 구분할 수 있도록 계정에 대한 간단한 설명을 제공합니다. |
      | [!UICONTROL **조직의 모든 사용자가 사용할 수 있는 계정을 만듭니다**] | 조직의 다른 사용자가 계정을 사용할 수 있도록 하려면 이 옵션을 활성화합니다.<p>계정을 공유할 때는 다음 사항을 고려하십시오.</p><ul><li>공유하는 계정은 공유 해제할 수 없습니다.</li><li>공유 계정은 계정 소유자만 편집할 수 있습니다.</li><li>누구나 공유 계정의 위치를 만들 수 있습니다.</li></ul> |
      | [!UICONTROL **계정 유형**] | 클라우드 계정 유형을 선택합니다. 각 계정 유형에 대해 단일 계정을 사용하고 해당 계정 내에서 필요에 따라 여러 위치를 사용하는 것이 좋습니다.<p>시스템 관리자는 [사용자가 계정을 만들 수 있는지 여부 구성](/help/components/locations/locations-manager.md#configure-whether-users-can-create-accounts)에 설명된 대로 사용자가 만들 수 있는 계정 유형을 제한할 수 있습니다. 이 섹션에 설명된 대로 계정을 만들 수 없는 경우 시스템 관리자에게 문의하십시오.</p> |

   1. [!UICONTROL **계정 속성**] 섹션에서 선택한 계정 유형과 관련된 정보를 지정합니다.

      구성 지침을 보려면 선택한 [!UICONTROL **계정 유형**]&#x200B;에 해당하는 아래 섹션을 확장하세요. (추가적인 레거시 계정 유형도 사용할 수 있지만 권장되지는 않습니다.)

      **계정 유형**

      +++Amazon S3 역할 ARN

      Amazon S3 Role ARN 계정을 구성하려면 다음 정보를 지정합니다.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **Role ARN**] | Adobe가 Amazon S3 계정에 액세스하는 데 사용할 수 있는 Role ARN(Amazon 리소스 이름)을 제공해야 합니다. 이렇게 하려면 소스 계정에 대한 권한 정책을 만들고 해당 정책을 사용자에게 첨부한 다음 대상 계정에 대한 역할을 생성합니다. 자세한 내용은 [이 AWS 설명서](https://aws.amazon.com/premiumsupport/knowledge-center/cross-account-access-iam/)를 참조하십시오. |

      {style="table-layout:auto"}

+++

      +++Google Cloud Platform

      Google Cloud Platform 계정을 구성하려면 다음 정보를 지정합니다.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **프로젝트 ID**] | Google Cloud 프로젝트 ID입니다. [프로젝트 ID 가져오기에 대한 Google Cloud 설명서](https://cloud.google.com/resource-manager/docs/creating-managing-projects#identifying_projects)를 참조하십시오. |

      {style="table-layout:auto"}

+++

      +++Azure SAS

      Azure SAS 계정을 구성하려면 다음 정보를 지정합니다.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **애플리케이션 ID**] | 만든 Azure 애플리케이션에서 이 ID를 복사합니다. 이 정보는 Microsoft Azure의 애플리케이션 내부 **개요** 탭에 있습니다. 자세한 내용은 [Microsoft ID 플랫폼으로 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app)를 참조하십시오. |
      | [!UICONTROL **테넌트 ID**] | 만든 Azure 애플리케이션에서 이 ID를 복사합니다. 이 정보는 Microsoft Azure의 애플리케이션 내부 **개요** 탭에 있습니다. 자세한 내용은 [Microsoft ID 플랫폼으로 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app)를 참조하십시오. |
      | [!UICONTROL **키 자격 증명 모음 URI**] | <p>Azure Key Vault의 SAS 토큰에 대한 경로입니다.  Azure SAS를 구성하려면 Azure 키 자격 증명 모음을 사용하여 SAS 토큰을 비밀로 저장해야 합니다. 자세한 내용은 [Azure Key Vault에서 암호를 설정 및 검색하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations)를 참조하십시오.</p><p>Key Vault URI가 만들어지면 Key Vault에 액세스 정책을 추가하여 만든 Azure 애플리케이션에 권한을 부여합니다. 자세한 내용은 [Azure 키 액세스 정책을 할당하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/key-vault/general/assign-access-policy?tabs=azure-portal)를 참조하십시오.</p> |
      | [!UICONTROL **키 자격 증명 모음 암호 이름**] | Azure Key Vault에 암호를 추가할 때 만든 암호 이름입니다. Microsoft Azure에서 이 정보는 **주요 자격 증명 모음** 설정 페이지에서 만든 주요 자격 증명 모음에 있습니다. 자세한 내용은 [Azure Key Vault에서 암호를 설정 및 검색하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations)를 참조하십시오. |
      | [!UICONTROL **위치 계정 암호**] | 만든 Azure 애플리케이션에서 암호를 복사합니다. 이 정보는 Microsoft Azure의 애플리케이션 내부 **인증서 및 암호** 애플리케이션 탭에 있습니다. 자세한 내용은 [Microsoft ID 플랫폼으로 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app)를 참조하십시오. |

      {style="table-layout:auto"}

+++

      +++Azure RBAC

      Azure RBAC 계정을 구성하려면 다음 정보를 지정합니다.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **애플리케이션 ID**] | 만든 Azure 애플리케이션에서 이 ID를 복사합니다. 이 정보는 Microsoft Azure의 애플리케이션 내부 **개요** 탭에 있습니다. 자세한 내용은 [Microsoft ID 플랫폼으로 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app)를 참조하십시오. |
      | [!UICONTROL **테넌트 ID**] | 만든 Azure 애플리케이션에서 이 ID를 복사합니다. 이 정보는 Microsoft Azure의 애플리케이션 내부 **개요** 탭에 있습니다. 자세한 내용은 [Microsoft ID 플랫폼으로 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app)를 참조하십시오. |
      | [!UICONTROL **위치 계정 암호**] | 만든 Azure 애플리케이션에서 암호를 복사합니다. 이 정보는 Microsoft Azure의 애플리케이션 내부 **인증서 및 암호** 애플리케이션 탭에 있습니다. 자세한 내용은 [Microsoft ID 플랫폼으로 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app)를 참조하십시오. |

      {style="table-layout:auto"}

+++

      +++이메일

      >[!NOTE]
      >
      >전자 메일 계정은 [데이터 피드](/help/export/analytics-data-feed/create-feed.md)에서만 사용할 수 있습니다. (전자 메일 계정은 [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md) 또는 [분류 집합](/help/components/classifications/sets/overview.md)에서 지원되지 않습니다.)

      Azure RBAC 계정을 구성하려면 다음 정보를 지정합니다.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **수신자**] | 보고서 전송 시 특정 사용자에게 이메일 알림을 보낼 수 있습니다. 단일 이메일 주소 또는 쉼표로 구분된 이메일 주소 목록을 지정하십시오. |

      {style="table-layout:auto"}

+++

1. [!UICONTROL **보고서 옵션**] 탭에서 Data Warehouse 요청을 계속 구성합니다. 자세한 내용은 [Data Warehouse 요청에 대한 보고서 옵션](/help/export/data-warehouse/create-request/dw-request-report-options.md)을 참조하십시오.

## 이전 계정 유형

>[!IMPORTANT]
>
>이 섹션에 설명된 대상은 기존 대상으로 권장되지 않습니다. 대신 Data Warehouse 대상을 만드는 경우 Amazon S3, Google Cloud Platform, Azure RBAC, Azure SAS 또는 이메일 대상 중 하나를 사용합니다. 각 추천 대상에 대한 자세한 내용은 상기 정보를 참조하십시오.

다음 정보는 각 기존 대상에 대한 구성 정보를 제공합니다.

### FTP

Data Warehouse 데이터는 Adobe 또는 호스팅된 FTP 위치에 전달될 수 있습니다. FTP 호스트, 사용자 이름 및 암호가 필요합니다. 폴더에 피드 파일을 배치하려면 경로 필드를 사용하십시오. 폴더는 이미 있어야 합니다. 지정된 경로가 존재하지 않을 경우 피드에서 오류가 발생합니다.

사용 가능한 필드가 완료되면 다음 정보를 사용합니다.

#### 계정 필드

* [!UICONTROL **계정 이름**]: FTP 계정의 이름입니다.

* [!UICONTROL **계정 설명**]: FTP 계정에 대한 설명입니다.

* [!UICONTROL **호스트 이름**]: 원하는 FTP 대상 URL을 입력합니다. (예: `ftp.company.com`)

  >[!NOTE]
  >
  >  URL의 앞부분에는 `ftp://`를 포함하지 마십시오.

* [!UICONTROL **사용자 이름**]: FTP 사이트에 로그인할 사용자 이름을 입력합니다.

* [!UICONTROL **암호 및 암호 확인**]: FTP 사이트에 로그인할 암호를 입력합니다.

#### 위치 필드

* [!UICONTROL **위치 이름**]: 파일을 전송할 FTP 계정의 위치 이름입니다.

* [!UICONTROL **위치 설명**]: FTP 계정의 위치에 대한 설명입니다.

* [!UICONTROL **디렉터리 경로**]: FTP 계정의 위치에 대한 경로입니다.

### SFTP

Data Warehouse에 대한 SFTP 지원을 사용할 수 있습니다. 유효한 RSA 또는 DSA 공개 키를 포함하기 위해 SFTP 호스트, 사용자 이름 및 대상 사이트가 필요합니다. Data Warehouse 대상을 만들 때 적절한 공개 키를 다운로드할 수 있습니다.

사용 가능한 필드가 완료되면 다음 정보를 사용합니다.

#### 계정 필드

* [!UICONTROL **계정 이름**]: FTP 계정의 이름입니다.

* [!UICONTROL **계정 설명**]: FTP 계정에 대한 설명입니다.

* [!UICONTROL **호스트 이름**]: 원하는 SFTP 대상 URL을 입력합니다. (예: `sftp.company.com`)

  >[!NOTE]
  >
  >  URL의 앞부분에는 `sftp://`를 포함하지 마십시오.

* [!UICONTROL **사용자 이름**]: SFTP 사이트에 로그인할 사용자 이름을 입력합니다.

* [!UICONTROL **업로드 중 임시 파일 확장자 사용**]: 활성화하면 업로드 프로세스 중에 `.part` 파일 확장자가 사용됩니다. 업로드가 완료된 후 SFTP 서버가 파일 이름 변경을 제한하지 않는 한 이 옵션을 활성화된 상태로 유지하십시오.

* [!UICONTROL **공개 키**]: Data warehouse 대상을 만들 때 적절한 공개 키를 다운로드합니다.

#### 위치 필드

* [!UICONTROL **위치 이름**]: 파일을 전송할 SFTP 계정의 위치 이름입니다.

* [!UICONTROL **위치 설명**]: SFTP 계정의 위치에 대한 설명입니다.

* [!UICONTROL **디렉터리 경로**]: SFTP 계정의 위치에 대한 경로입니다.

SFTP 구성에 대한 자세한 내용은 [SFTP 서버로 Data Warehouse 요청 보내기](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-dw.md)를 참조하십시오.

### S3

웨어하우스 데이터를 Amazon S3 버킷으로 직접 보낼 수 있습니다. 이 대상 유형에는 버킷 이름, 액세스 키 ID 및 보안 키가 필요합니다. 자세한 내용은 Amazon S3 문서 내의 [Amazon S3 버킷 이름 지정 요구 사항](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-s3-bucket-naming-requirements.html)을 참조하십시오.

데이터 Data Warehouse 업로드를 위해 제공한 사용자는 다음 [권한](https://docs.aws.amazon.com/AmazonS3/latest/API/API_Operations_Amazon_Simple_Storage_Service.html)이 있어야 합니다.

* s3:GetObject
* s3:PutObject
* s3:PutObjectAcl

다음 16개의 표준 AWS 지역이 지원됩니다(필요한 경우 적절한 서명 알고리즘 사용).

* us-east-2
* us-east-1
* us-west-1
* us-west-2
* ap-south-1
* ap-northeast-2
* ap-southeast-1
* ap-southeast-2
* ap-northeast-1
* ca-central-1
* eu-central-1
* eu-west-1
* eu-west-2
* eu-west-3
* eu-north-1
* sa-east-1

>[!NOTE]
>
>cn-north-1 지역은 지원되지 않습니다.

### Azure Blob

Data Warehouse는 Azure Blob 대상을 지원합니다. 컨테이너, 계정 및 키가 필요합니다. Amazon은 데이터를 사용하지 않을 때 자동으로 암호화합니다. 데이터를 다운로드할 때 데이터 암호화는 자동으로 해제됩니다. 자세한 내용은 Microsoft Azure 문서 내에서 [저장소 계정 만들기](https://docs.microsoft.com/ko-kr/azure/storage/common/storage-quickstart-create-account?tabs=azure-portal#view-and-copy-storage-access-keys)를 참조하십시오.

>[!NOTE]
>
>Data Warehouse 대상의 디스크 공간을 관리하려면 자체 프로세스를 구현해야 합니다. Adobe는 서버에서 데이터를 삭제하지 않습니다.
