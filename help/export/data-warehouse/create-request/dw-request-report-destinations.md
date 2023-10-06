---
description: Data Warehouse 요청을 만드는 방법을 설명하는 단계입니다.
title: Data Warehouse 요청에 대한 보고서 대상 구성
feature: Data Warehouse
exl-id: 3c7faea3-4d90-4274-88f3-e9337c94155f
source-git-commit: f1264344a380944946ffa7b427db7bbc3ea96b1f
workflow-type: tm+mt
source-wordcount: '2255'
ht-degree: 15%

---

# Data Warehouse 요청에 대한 보고서 대상 구성

>[!AVAILABILITY]
>
>이 문서에 설명된 일부 Data Warehouse 기능(및 이 섹션의 다른 Data Warehouse 문서)은 릴리스의 제한된 테스트 단계에서만 사용할 수 있으며 사용자 환경에서 아직 사용하지 못할 수 있습니다.
>
>모든 고객이 아직 사용할 수 없는 기능에 대한 정보와 이러한 기능의 릴리스 타임라인에 대한 정보는 다음을 참조하십시오. [릴리스 정보](/help/release-notes/latest.md).
>
>기능이 일반적으로 제공되면 이 메모는 제거됩니다. Analytics 릴리스 프로세스에 대한 자세한 내용은 [Adobe Analytics 기능 릴리스](/help/release-notes/releases.md)를 참조하십시오.

Data Warehouse 요청을 만들 때 사용할 수 있는 구성 옵션은 다양합니다. 다음 정보는 요청에 대한 보고서 대상을 구성하는 방법을 설명합니다.

요청 만들기를 시작하는 방법과 기타 중요한 구성 옵션에 대한 링크에 대한 자세한 내용은 을 참조하십시오. [Data Warehouse 요청 만들기](/help/export/data-warehouse/create-request/t-dw-create-request.md).

>[!NOTE]
>
>보고서 대상을 구성할 때는 다음 사항을 고려하십시오.
>
>* 보고서 대상에 클라우드 계정 또는 이메일을 사용하는 것이 좋습니다. 기존 FTP 및 SFTP 계정은 사용할 수 있지만 권장되지 않습니다.
>
>* 클라우드 계정은 Adobe Analytics 사용자 계정과 연결되어 있습니다. 다른 사용자는 사용자가 구성한 클라우드 계정을 사용하거나 볼 수 없습니다.
>
>* 이전에 소유한 모든 클라우드 계정 [데이터 피드에 대해 구성됨](/help/export/analytics-data-feed/create-feed.md) Data Warehouse에 사용할 수 있습니다.
>
>* 다음에 대해 구성된 클라우드 계정 [Adobe Analytics 분류 데이터 가져오기](/help/components/locations/locations-manager.md) 클라우드 대상의 은(는) 보고서 대상을 구성할 때 사용할 수 있습니다. 하지만 분류 데이터를 가져오도록 구성된 위치는 사용할 수 없습니다.

Data Warehouse 보고서를 전송할 대상을 구성하려면 다음 작업을 수행하십시오.

1. 다음을 선택하여 Adobe Analytics에서 요청 만들기 시작 **[!UICONTROL 도구]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **추가**].

   자세한 내용은 [Data Warehouse 요청 만들기](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. 새 Data Warehouse 요청 페이지에서 [!UICONTROL **보고서 대상**] 탭.

   ![보고서 대상 탭](assets/dw-report-destination.png)

1. (조건부) 보고서 대상으로 사용할 계정(및 해당 계정의 대상)을 이전에 구성한 경우:

   1. 에서 계정 선택 [!UICONTROL **계정 선택**] 드롭다운 메뉴.

      구성한 모든 클라우드 계정 [Adobe Analytics 분류 데이터 가져오기](/help/components/locations/locations-manager.md) 클라우드 대상의 은 여기에 표시되며 사용할 수 있습니다. 하지만 분류 데이터를 가져오도록 구성된 위치는 사용할 수 없습니다. 대신 아래 설명된 대로 새 대상을 추가합니다.

   1. 다음에서 계정과 연결된 대상을 선택합니다. [!UICONTROL **대상 선택**] 드롭다운 메뉴. <!-- Is this correct? -->

1. (조건부) 이전에 계정을 구성하지 않은 경우:

   1. 선택 [!UICONTROL **계정 추가**]&#x200B;을(를) 클릭한 후 다음 정보를 지정합니다.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **계정 유형**] | 클라우드 계정 유형을 선택합니다. 각 계정 유형에 대해 해당 계정 내에서 필요에 따라 여러 위치가 있는 단일 계정을 사용하는 것이 좋습니다. <p>계정 유형을 선택하면 해당 계정 유형과 관련된 필드가 표시됩니다. </p> |
      | [!UICONTROL **계정 이름**] | 계정 이름을 지정합니다. 이 이름은 위치를 만들 때 나타납니다. <!-- true? --> |
      | [!UICONTROL **계정 설명**] | 동일한 계정 유형의 다른 계정과 구분하는 데 도움이 되도록 계정에 대한 간단한 설명을 입력합니다. |

      구성 지침을 보려면 아래에 있는 해당 섹션을 확장합니다. [!UICONTROL **계정 유형**] 을(를) 선택합니다.

      보고서 대상을 구성할 때 다음 계정 유형을 사용하십시오. 구성 지침을 보려면 계정 유형을 확장합니다. (추가 [이전 대상](#legacy-destinations) 사용할 수도 있지만 권장되지는 않습니다.)

      +++Amazon S3

      Amazon S3 역할 ARN 계정을 구성하려면 다음 정보를 지정합니다.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **역할 ARN**] | Adobe이 Amazon S3 계정에 대한 액세스 권한을 받는 데 사용할 수 있는 역할 ARN(Amazon 리소스 이름)을 제공해야 합니다. 이렇게 하려면 소스 계정에 대한 IAM 권한 정책을 만들고, 이 정책을 사용자에게 연결한 다음 대상 계정에 대한 역할을 만듭니다. 자세한 내용은 다음을 참조하십시오. [이 AWS 설명서](https://aws.amazon.com/premiumsupport/knowledge-center/cross-account-access-iam/). |
      | [!UICONTROL **사용자 ARN**] | Adobe ARN(Amazon 리소스 이름)은 사용자가 제공합니다. 이 사용자를 생성한 정책에 첨부해야 합니다. |

      {style="table-layout:auto"}

+++

      +++Google Cloud 플랫폼

      Google Cloud Platform 계정을 구성하려면 다음 정보를 지정합니다.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **프로젝트 ID**] | Google Cloud 프로젝트 ID입니다. 다음을 참조하십시오. [프로젝트 ID 가져오기에 대한 Google Cloud 설명서](https://cloud.google.com/resource-manager/docs/creating-managing-projects#identifying_projects). |

      {style="table-layout:auto"}

+++

      +++Azure SAS

      Azure SAS 계정을 구성하려면 다음 정보를 지정하십시오.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **애플리케이션 ID**] | 생성한 Azure 애플리케이션에서 이 ID를 복사합니다. Microsoft Azure에서 이 정보는 **개요** 응용 프로그램 내의 탭입니다. 자세한 내용은 [Microsoft ID 플랫폼을 사용하여 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
      | [!UICONTROL **테넌트 ID**] | 생성한 Azure 애플리케이션에서 이 ID를 복사합니다. Microsoft Azure에서 이 정보는 **개요** 응용 프로그램 내의 탭입니다. 자세한 내용은 [Microsoft ID 플랫폼을 사용하여 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
      | [!UICONTROL **키 자격 증명 모음 URI**] | <p>Azure Key Vault의 SAS 토큰 경로.  Azure SAS를 구성하려면 Azure 키 자격 증명 모음을 사용하여 SAS 토큰을 비밀로 저장해야 합니다. 자세한 내용은 [Azure Key Vault에서 암호를 설정하고 검색하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations).</p><p>Key Vault URI가 만들어진 후 Key Vault에 액세스 정책을 추가하여 만든 Azure 애플리케이션에 권한을 부여합니다. 자세한 내용은 [주요 자격 증명 모음 액세스 정책을 할당하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/key-vault/general/assign-access-policy?tabs=azure-portal).</p> |
      | [!UICONTROL **키 자격 증명 모음 암호 이름**] | Azure Key Vault에 암호를 추가할 때 만든 암호 이름입니다. Microsoft Azure에서 이 정보는 만든 Key Vault의 **주요 자격 증명 모음** 설정 페이지를 참조하십시오. 자세한 내용은 [Azure Key Vault에서 암호를 설정하고 검색하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations). |
      | [!UICONTROL **Secret**] | 생성한 Azure 애플리케이션에서 암호를 복사합니다. Microsoft Azure에서 이 정보는 **인증서 및 암호** 응용 프로그램 내의 탭입니다. 자세한 내용은 [Microsoft ID 플랫폼을 사용하여 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |

      {style="table-layout:auto"}

+++

      +++Azure RBAC

      Azure RBAC 계정을 구성하려면 다음 정보를 지정하십시오.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **애플리케이션 ID**] | 생성한 Azure 애플리케이션에서 이 ID를 복사합니다. Microsoft Azure에서 이 정보는 **개요** 응용 프로그램 내의 탭입니다. 자세한 내용은 [Microsoft ID 플랫폼을 사용하여 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
      | [!UICONTROL **테넌트 ID**] | 생성한 Azure 애플리케이션에서 이 ID를 복사합니다. Microsoft Azure에서 이 정보는 **개요** 응용 프로그램 내의 탭입니다. 자세한 내용은 [Microsoft ID 플랫폼을 사용하여 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
      | [!UICONTROL **Secret**] | 생성한 Azure 애플리케이션에서 암호를 복사합니다. Microsoft Azure에서 이 정보는 **인증서 및 암호** 응용 프로그램 내의 탭입니다. 자세한 내용은 [Microsoft ID 플랫폼을 사용하여 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |

      {style="table-layout:auto"}

+++

      +++이메일

      전자 메일 계정을 구성하려면 다음 정보를 지정하십시오.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **수신자**] | 보고서 전송 시 특정 사용자에게 이메일 알림을 보낼 수 있습니다. 단일 이메일 주소 또는 쉼표로 구분된 이메일 주소 목록을 지정하십시오. <!-- How does this differ from the Notification email tab? --> |

   1. 선택 [!UICONTROL **위치 추가**]&#x200B;을(를) 클릭한 후 다음 정보를 지정합니다. |필드 | 함수 | ------------------- | [!UICONTROL **이름**] | 위치의 이름입니다.  | | [!UICONTROL **설명**] | 같은 계정 유형의 다른 계정과 구분할 수 있도록 계정에 대한 간단한 설명을 제공합니다. | | [!UICONTROL **위치 계정**] | 만든 위치 계정 선택 [계정 추가](#add-an-account). |

   1. 다음에서 [!UICONTROL **위치 속성**] 섹션에서 위치 계정의 계정 유형과 관련된 정보를 지정합니다.

      구성 지침을 보려면 아래에 있는 해당 섹션을 확장합니다. [!UICONTROL **계정 유형**] 을(를) 이전에 선택했습니다.

      +++Amazon S3

      Amazon S3 위치를 구성하려면 다음 정보를 지정하십시오.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **버킷 이름**] | Adobe Analytics 데이터를 전송할 Amazon S3 계정 내의 버킷입니다. Adobe이 제공한 사용자 ARN이 이 버킷에 파일을 업로드할 수 있는 액세스 권한이 있는지 확인하십시오. |
      | [!UICONTROL **키 접두사**] | 데이터를 저장할 버킷 내의 폴더입니다. 폴더 이름을 지정한 다음 이름 뒤에 백슬래시를 추가하여 폴더를 만듭니다. 예: folder_name/ |

      {style="table-layout:auto"}

+++

      +++Google Cloud 플랫폼

      다음 정보를 지정하여 Google Cloud Platform 위치를 구성하십시오.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **버킷 이름**] | Adobe Analytics 데이터를 전송할 GCP 계정 내의 버킷입니다. 이 버킷에 파일을 업로드할 수 있도록 Adobe이 제공한 사용자에 대한 권한을 부여했는지 확인하십시오. 권한 부여에 대한 자세한 내용은 [버킷 수준 정책에 사용자 추가](https://cloud.google.com/storage/docs/access-control/using-iam-permissions#bucket-add) Google Cloud 설명서에서 확인할 수 있습니다. |
      | [!UICONTROL **키 접두사**] | 데이터를 저장할 버킷 내의 폴더입니다. 폴더 이름을 지정한 다음 이름 뒤에 백슬래시를 추가하여 폴더를 만듭니다. 예: folder_name/ |

      {style="table-layout:auto"}

+++

      +++Azure SAS

      Azure SAS 위치를 구성하려면 다음 정보를 지정하십시오.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **컨테이너 이름**] | Adobe Analytics 데이터를 전송할 지정한 계정 내의 컨테이너입니다. |
      | [!UICONTROL **키 접두사**] | 데이터를 저장할 컨테이너 내의 폴더입니다. 폴더 이름을 지정한 다음 이름 뒤에 백슬래시를 추가하여 폴더를 만듭니다. 예, `folder_name/` |

      {style="table-layout:auto"}

+++

      +++Azure RBAC

      Azure RBAC 위치를 구성하려면 다음 정보를 지정하십시오.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **컨테이너 이름**] | Adobe Analytics 데이터를 전송할 지정한 계정 내의 컨테이너입니다. 이전에 만든 Azure 애플리케이션에 파일을 업로드할 수 있는 권한을 부여했는지 확인하십시오. |
      | [!UICONTROL **키 접두사**] | 데이터를 저장할 컨테이너 내의 폴더입니다. 폴더 이름을 지정한 다음 이름 뒤에 백슬래시를 추가하여 폴더를 만듭니다. 예, `folder_name/` |
      | [!UICONTROL **계정 이름**] | Azure 스토리지 계정입니다. |

      {style="table-layout:auto"}

+++

   1. [!UICONTROL **저장**]&#x200B;을 선택합니다.

      이제 구성한 계정 및 위치로 데이터를 가져올 수 있습니다.

1. 에서 Data Warehouse 요청 구성 계속 [!UICONTROL **보고서 옵션**] 탭. 자세한 내용은 [Data Warehouse 요청에 대한 보고서 옵션 구성](/help/export/data-warehouse/create-request/dw-request-report-options.md).

## 이전 대상

>[!IMPORTANT]
>
>이 섹션에 설명된 대상은 기존 대상이며, 권장되지 않습니다. 대신 데이터 웨어하우스 대상을 만들 때 Amazon S3, Google Cloud Platform, Azure RBAC, Azure SAS 또는 이메일 대상 중 하나를 사용합니다. 이러한 각 권장 대상에 대한 자세한 내용은 위의 정보를 참조하십시오.

다음 정보는 각 기존 대상에 대한 구성 정보를 제공합니다.

### FTP

Data Warehouse 데이터는 Adobe 또는 고객 호스팅 FTP 위치로 배달될 수 있습니다. FTP 호스트, 사용자 이름 및 암호가 필요합니다. 폴더에 피드 파일을 배치하려면 경로 필드를 사용하십시오. 폴더는 이미 있어야 합니다. 지정된 경로가 존재하지 않을 경우 피드에서 오류가 발생합니다.

사용 가능한 필드를 완성할 때 다음 정보를 사용하십시오.

#### 계정 필드

* [!UICONTROL **계정 이름**]: FTP 계정의 이름입니다.

* [!UICONTROL **계정 설명**]: FTP 계정에 대한 설명입니다.

* [!UICONTROL **호스트 이름**]: 원하는 FTP 대상 URL을 입력합니다. (예: `ftp.company.com`)

  >[!NOTE]
  >
  >  포함하지 않음 `ftp://` 를 입력합니다.

* [!UICONTROL **사용자 이름**]: FTP 사이트에 로그인할 사용자 이름을 입력합니다.

* [!UICONTROL **암호 및 암호 확인**]: FTP 사이트에 로그인할 암호를 입력합니다.

#### 위치 필드

* [!UICONTROL **위치 이름**]: 파일을 전송할 FTP 계정의 위치 이름입니다.

* [!UICONTROL **위치 설명**]: FTP 계정의 위치에 대한 설명입니다.

* [!UICONTROL **디렉터리 경로**]: FTP 계정의 위치에 대한 경로입니다.

### SFTP

Data Warehouse에 대한 SFTP 지원을 사용할 수 있습니다. 유효한 RSA 또는 DSA 공개 키를 포함하기 위해 SFTP 호스트, 사용자 이름 및 대상 사이트가 필요합니다. Data Warehouse 대상을 만들 때 적절한 공개 키를 다운로드할 수 있습니다.

사용 가능한 필드를 완성할 때 다음 정보를 사용하십시오.

#### 계정 필드

* [!UICONTROL **계정 이름**]: FTP 계정의 이름입니다.

* [!UICONTROL **계정 설명**]: FTP 계정에 대한 설명입니다.

* [!UICONTROL **호스트 이름**]: 원하는 SFTP 대상 URL을 입력합니다. (예: `sftp.company.com`)

  >[!NOTE]
  >
  >  포함하지 않음 `sftp://` 를 입력합니다.

* [!UICONTROL **사용자 이름**]: SFTP 사이트에 로그인할 사용자 이름을 입력합니다.

* [!UICONTROL **공개 키**]: Data Warehouse 대상을 만들 때 적절한 공개 키를 다운로드합니다.

#### 위치 필드

* [!UICONTROL **위치 이름**]: 파일을 전송하려는 SFTP 계정의 위치 이름입니다.

* [!UICONTROL **위치 설명**]: SFTP 계정의 위치에 대한 설명입니다.

* [!UICONTROL **디렉터리 경로**]: SFTP 계정의 위치에 대한 경로입니다.

### S3

웨어하우스 데이터를 Amazon S3 버킷으로 직접 보낼 수 있습니다. 이 대상 유형에는 버킷 이름, 액세스 키 ID 및 보안 키가 필요합니다. 자세한 내용은 Amazon S3 문서 내의 [Amazon S3 버킷 이름 지정 요구 사항](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-s3-bucket-naming-requirements.html)을 참조하십시오.

Data Warehouse 데이터 업로드를 위해 제공한 사용자에는 다음 항목이 있어야 합니다 [권한](https://docs.aws.amazon.com/AmazonS3/latest/API/API_Operations_Amazon_Simple_Storage_Service.html):

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
