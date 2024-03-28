---
description: Data Warehouse 요청을 만드는 방법을 설명하는 단계입니다.
title: Data Warehouse 요청에 대한 보고서 대상 구성
feature: Data Warehouse
exl-id: 3c7faea3-4d90-4274-88f3-e9337c94155f
source-git-commit: 4e4b5e1c362778223be01f78b173a698c53f9b32
workflow-type: ht
source-wordcount: '2430'
ht-degree: 100%

---

# Data Warehouse 요청에 대한 보고서 대상 구성

Data Warehouse 요청을 만들 때 사용할 수 있는 다양한 구성 옵션이 있습니다. 다음 정보는 요청에 대한 보고자 대상을 구성하는 방법을 설명합니다.

요청 만들기를 시작하는 방법과 다른 중요 구성 옵션 링크에 대한 자세한 내용은 [Data Warehouse 요청 만들기](/help/export/data-warehouse/create-request/t-dw-create-request.md)을 참조하십시오.

>[!NOTE]
>
>보고서 대상 구성 시 다음과 같은 사항을 고려하십시오.
>
>* 보고서 대상에 클라우드 계정이나 이메일을 사용하는 것이 좋습니다. 이전 FTP 및 SFTP 계정은 사용할 수 있지만 권장되지 않습니다.
>
>* [데이터 피드](/help/export/analytics-data-feed/create-feed.md) 또는 [Adobe Analytics 분류 데이터 가져오기](/help/components/locations/locations-manager.md)에 대해 이전에 구성된 모든 클라우드 계정은 Data Warehouse에 사용할 수 있습니다. 하지만 분류 데이터 가져오기에 대해 구성된 위치는 사용할 수 없습니다.
>
>* 클라우드 계정은 Adobe Analytics 사용자 계정과 연계되어 있습니다. 다른 사용자는 구성된 클라우드 계정을 사용하거나 볼 수 없습니다.
>

Data Warehouse 보고서가 전송되는 대상을 구성하려면

1. **[!UICONTROL 도구]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **추가**]&#x200B;를 선택하여 Adobe Analytics에서 요청 만들기를 시작하십시오.

   자세한 내용은 [Data Warehouse 요청 만들기](/help/export/data-warehouse/create-request/t-dw-create-request.md)를 참조하십시오.

1. 새 Data Warehouse 요청 페이지에서 [!UICONTROL **보고서 대상**] 탭을 선택합니다.

   ![보고서 대상 탭](assets/dw-report-destination.png)

1. (조건부) 보고서 대상으로 사용할 계정(및 해당 계정의 대상)이 이미 구성되어 있는 경우

   1. (선택 사항) 시스템 관리자인 경우 [!UICONTROL **모든 대상 표시**] 옵션을 사용할 수 있습니다. 조직의 사용자가 생성한 모든 계정과 위치에 액세스하려면 이 옵션을 활성화합니다.

   1. [!UICONTROL **계정 선택**] 드롭다운 메뉴에서 계정을 선택합니다.

      클라우드 대상에서 [Adobe Analytics 분류 데이터 가져오기](/help/components/locations/locations-manager.md)에 대해 구성된 모든 클라우드 계정을 여기에 표시하여 사용할 수 있습니다. 하지만 분류 데이터 가져오기에 대해 구성된 위치는 사용할 수 없습니다. 대신 아래 설명된 대로 새 대상을 추가합니다.

   1. [!UICONTROL **대상 선택**] 드롭다운 메뉴에서 계정과 연계된 대상을 선택합니다. <!-- Is this correct? -->

1. (조건부) 이전에 계정을 구성하지 않은 경우

   1. [!UICONTROL **계정 추가**]&#x200B;를 선택하고 다음 정보를 지정합니다.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **계정 유형**] | 클라우드 계정 유형을 선택합니다. 각 계정 유형에 대해 단일 계정을 사용하고 해당 계정 내에서 필요에 따라 여러 위치를 사용하는 것이 좋습니다. <p>계정 유형을 선택하면 해당 계정에 해당되는 필드가 표시됩니다. </p> |
      | [!UICONTROL **계정 이름**] | 계정 이름을 지정합니다. 위치가 생성되면 이 이름이 표시됩니다. <!-- true? --> |
      | [!UICONTROL **계정 설명**] | 동일한 계정 유형의 다른 계정과 구분할 수 있도록 계정에 대한 간단한 설명을 제공합니다. |

      구성 지침을 보려면 선택한 [!UICONTROL **계정 유형**]&#x200B;에 해당하는 아래 섹션을 확장합니다.

      보고서 대상을 구성할 때 다음 계정 유형 중 하나를 사용합니다. 구성 지침을 보려면 계정 유형을 확장합니다. (추가 [기존 대상](#legacy-destinations)은 사용할 수도 있지만 권장되지 않습니다.)

      +++Amazon S3

      다음 정보를 지정하여 Amazon S3 Role ARN 계정을 구성합니다.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **Role ARN**] | Adobe가 Amazon S3 계정에 액세스하는 데 사용할 수 있는 Role ARN(Amazon 리소스 이름)을 제공해야 합니다. 이렇게 하려면 소스 계정에 대한 권한 정책을 만들고 해당 정책을 사용자에게 첨부한 다음 대상 계정에 대한 역할을 생성합니다. 자세한 내용은 [이 AWS 설명서](https://aws.amazon.com/premiumsupport/knowledge-center/cross-account-access-iam/)를 참조하십시오.<p>버킷 권한을 설정하는 방법에 대한 자세한 내용은 [Amazon S3 버킷 내 오브젝트에 대한 교차 계정 액세스를 제공할 수 있는 방법을 참조하십시오.](https://repost.aws/knowledge-center/cross-account-access-s3) Amazon 지식 센터 내부. |
      | [!UICONTROL **사용자 ARN**] | 사용자 ARN(Amazon 리소스 이름)은 Adobe에서 제공합니다. 사용자가 만든 정책에 이 사용자를 첨부해야 합니다. |

      {style="table-layout:auto"}

      +++

      +++Google Cloud 플랫폼

      다음 정보를 지정하여 Google Cloud 플랫폼 계정을 구성합니다.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **프로젝트 ID**] | Google Cloud 프로젝트 ID입니다. [프로젝트 ID 가져오기에 대한 Google Cloud 설명서](https://cloud.google.com/resource-manager/docs/creating-managing-projects#identifying_projects)를 참조하십시오. |

      {style="table-layout:auto"}

      +++

      +++Azure SAS

      다음 정보를 지정하여 Azure SAS 계정을 구성합니다.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **애플리케이션 ID**] | 만든 Azure 애플리케이션에서 이 ID를 복사합니다. 이 정보는 Microsoft Azure의 애플리케이션 내부 **개요** 탭에 있습니다. 자세한 내용은 [Microsoft ID 플랫폼으로 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app)를 참조하십시오. |
      | [!UICONTROL **테넌트 ID**] | 만든 Azure 애플리케이션에서 이 ID를 복사합니다. 이 정보는 Microsoft Azure의 애플리케이션 내부 **개요** 탭에 있습니다. 자세한 내용은 [Microsoft ID 플랫폼으로 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app)를 참조하십시오. |
      | [!UICONTROL **키 자격 증명 모음 URI**] | <p>Azure Key Vault의 SAS 토큰에 대한 경로입니다.  Azure SAS를 구성하려면 Azure Key Vault를 사용하여 SAS 토큰을 암호로 저장해야 합니다. 자세한 내용은 [Azure Key Vault에서 암호를 설정 및 검색하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations)를 참조하십시오.</p><p>키 자격 증명 모음 URI이 생성되면<ul><li>만든 Azure 애플리케이션에 대한 권한을 부여하려면 Key Vault에서 액세스 정책을 추가합니다.</li><li>키 자격 증명 모음 UR에 액세스하려면 `Key Vault Certificate User` 기본 제공 역할에 애플리케이션 ID가 부여되었는지 확인합니다.</br><p>자세한 내용은 [Azure 기본 제공 역할](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles)을 참조하십시오.</p></li></ul><p>자세한 내용은 [Azure 키 액세스 정책을 할당하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/key-vault/general/assign-access-policy?tabs=azure-portal)를 참조하십시오.</p> |
      | [!UICONTROL **키 자격 증명 모음 암호 이름**] | Azure Key Vault에 암호를 추가할 때 만든 암호 이름입니다. 이 정보는 Microsoft Azure의 **Key Vault** 설정 페이지에서 만든 Key Vault에 있습니다. 자세한 내용은 [Azure Key Vault에서 암호를 설정 및 검색하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations)를 참조하십시오. |
      | [!UICONTROL **암호**] | 만든 Azure 애플리케이션에서 암호를 복사합니다. 이 정보는 Microsoft Azure의 애플리케이션 내부 **인증서 및 암호** 애플리케이션 탭에 있습니다. 자세한 내용은 [Microsoft ID 플랫폼으로 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app)를 참조하십시오. |

      {style="table-layout:auto"}

      +++

      +++Azure RBAC

      다음 정보를 지정하여 Azure RBAC 계정을 구성합니다.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **애플리케이션 ID**] | 만든 Azure 애플리케이션에서 이 ID를 복사합니다. 이 정보는 Microsoft Azure의 애플리케이션 내부 **개요** 탭에 있습니다. 자세한 내용은 [Microsoft ID 플랫폼으로 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app)를 참조하십시오. |
      | [!UICONTROL **테넌트 ID**] | 만든 Azure 애플리케이션에서 이 ID를 복사합니다. 이 정보는 Microsoft Azure의 애플리케이션 내부 **개요** 탭에 있습니다. 자세한 내용은 [Microsoft ID 플랫폼으로 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app)를 참조하십시오. |
      | [!UICONTROL **암호**] | 만든 Azure 애플리케이션에서 암호를 복사합니다. 이 정보는 Microsoft Azure의 애플리케이션 내부 **인증서 및 암호** 애플리케이션 탭에 있습니다. 자세한 내용은 [Microsoft ID 플랫폼으로 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app)를 참조하십시오. |

      {style="table-layout:auto"}

      +++

      +++이메일

      다음 정보를 지정하여 이메일 계정을 구성합니다.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **수신자**] | 보고서 전송 시 특정 사용자에게 이메일 알림을 보낼 수 있습니다. 단일 이메일 주소 또는 쉼표로 구분된 이메일 주소 목록을 지정합니다. <!-- How does this differ from the Notification email tab? --> |

   1. [!UICONTROL **위치 추가**]를 선택하고 다음 정보를 지정합니다.
|필드 | 기능 |
|---------|----------|
| [!UICONTROL **이름**] | 위치의 이름입니다.  |
| [!UICONTROL **설명**] | 동일한 계정 유형의 다른 계정과 구분할 수 있도록 계정에 대한 간단한 설명을 제공합니다. |
| [!UICONTROL **위치 계정**] | [계정 추가](#add-an-account)에서 만든 위치 계정을 선택합니다. |

   1. [!UICONTROL **위치 속성**] 섹션에서 위치 계정의 계정 유형과 관련된 정보를 지정합니다.

      구성 지침을 보려면 이전에 선택한 [!UICONTROL **계정 유형**]&#x200B;에 해당하는 아래 섹션을 확장합니다.

      +++Amazon S3

      다음 정보를 지정하여 Amazon S3 위치를 구성합니다.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **버킷 이름**] | Adobe Analytics 데이터를 전송할 Amazon S3 계정 내부 버킷입니다. <p>이 버킷에 파일을 업로드하려면 Adobe에서 제공한 사용자 ARN에 `S3:PutObject` 권한이 있는지 확인합니다. 이 권한을 사용하면 사용자 ARN에서 초기 파일을 업로드하고 후속 업로드에 파일을 덮어쓸 수 있습니다.</p> |
      | [!UICONTROL **키 접두사**] | 데이터를 입력할 버킷 내부 폴더입니다. 폴더 이름을 지정한 다음 이름 뒤에 백슬래시를 추가하여 폴더를 만듭니다. 예를 들어 폴더 이름/ |

      {style="table-layout:auto"}

      +++

      +++Google Cloud 플랫폼

      다음 정보를 지정하여 Google Cloud 플랫폼 위치를 구성합니다.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **버킷 이름**] | Adobe Analytics 데이터를 전송할 GCP 계정 내부 버킷입니다. <p>Adobe에서 제공하는 주체에게 다음 권한 중 하나를 부여했는지 확인합니다.<ul><li>`roles/storage.objectCreator`: 주체를 제한하여 GCP 계정에서만 파일을 만들려는 경우 이 권한을 사용합니다. </br>**중요:** 예약된 보고에 이 권한을 사용하는 경우 새로 예약된 각 내보내기에 고유 파일 이름을 사용해야 합니다. 그렇지 않으면 주체가 기존 파일 덮어쓰기에 액세스할 수 없기 때문에 보고서를 생성할 수 없습니다.</li><li>`roles/storage.objectUser`: 주체가 GCP 계정에서 파일을 보고, 나열하고, 업데이트하고, 삭제할 수 있는 액세스 권한이 있는 경우 이 권한을 사용합니다.</br>이 권한을 사용하면 주체는 새로 예약된 각 내보내기에 고유 파일 이름을 자동 생성하지 않고도 후속 업로드에 기존 파일을 덮어쓸 수 있습니다.</li></ul><p>권한 부여에 대한 자세한 내용은 Google Cloud 설명서에서 [버킷 수준 정책에 주체 추가](https://cloud.google.com/storage/docs/access-control/using-iam-permissions#bucket-add)를 참조하십시오.</p> |
      | [!UICONTROL **키 접두사**] | 데이터를 입력할 버킷 내부 폴더입니다. 폴더 이름을 지정한 다음 이름 뒤에 백슬래시를 추가하여 폴더를 만듭니다. 예를 들어 폴더 이름/ |

      {style="table-layout:auto"}

      +++

      +++Azure SAS

      다음 정보를 지정하여 Azure SAS 위치를 구성합니다.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **컨테이너 이름**] | Adobe Analytics 데이터 전송 위치를 지정한 계정 내 컨테이너입니다. |
      | [!UICONTROL **키 접두사**] | 데이터를 입력할 컨테이너 내부 폴더입니다. 폴더 이름을 지정한 다음 이름 뒤에 백슬래시를 추가하여 폴더를 만듭니다. 예를 들어 `folder_name/`<p>Azure SAS 계정 구성 시 Key Vault 암호 이름 필드에 지정된 SAS 토큰 저장소에 `Write` 권한이 있는지 확인합니다. 이렇게 하면 SAS 토큰이 Azure 컨테이너에서 파일을 만들 수 있습니다. <p>SAS 토큰을 사용하여 파일을 덮어쓰려면 SAS 토큰 저장소에 `Delete` 권한이 있는지 확인합니다.</p><p>자세한 내용은 Azure Blob Storage 설명서에서 [Blob 스토리지 리소스](https://learn.microsoft.com/en-us/azure/storage/blobs/storage-blobs-introduction#blob-storage-resources) 를 참조하십시오.</p> |

      {style="table-layout:auto"}

      +++

      +++Azure RBAC

      다음 정보를 지정하여 Azure RBAC 위치를 구성합니다.

      | 필드 | 함수 |
      |---------|----------|
      | [!UICONTROL **컨테이너 이름**] | Adobe Analytics 데이터 전송 위치를 지정한 계정 내 컨테이너입니다. 앞서 만든 Azure 애플리케이션에 파일을 업로드할 권한을 부여하고 있는지 확인합니다. |
      | [!UICONTROL **키 접두사**] | 데이터를 입력할 컨테이너 내부 폴더입니다. 폴더 이름을 지정한 다음 이름 뒤에 백슬래시를 추가하여 폴더를 만듭니다. 예를 들어 `folder_name/`<p>컨테이너(폴더)에 액세스하려면 Azure RBAC 계정 구성 시 지정한 애플리케이션 ID에 `Storage Blob Data Contributor` 역할이 부여되었는지 확인합니다.</p> <p>자세한 내용은 [Azure 기본 제공 역할](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles)을 참조하십시오.</p> |
      | [!UICONTROL **계정 이름**] | Azure 스토리지 계정. |

      {style="table-layout:auto"}

      +++

1. [!UICONTROL **보고서 옵션**] 탭에서 Data Warehouse 요청을 계속 구성합니다. 자세한 내용은 [Data Warehouse 요청에 대한 보고서 옵션](/help/export/data-warehouse/create-request/dw-request-report-options.md)을 참조하십시오.

## 기존 대상

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
