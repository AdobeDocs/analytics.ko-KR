---
description: 분류 데이터를 업로드할 수 있는 클라우드 가져오기 계정 및 위치를 구성합니다.
keywords: Analysis Workspace
title: 클라우드 가져오기 및 내보내기 계정 구성
feature: Classifications
exl-id: 40d3d3f1-1047-4c37-8caf-6b0aabaa590a
source-git-commit: 8a9c51d46195737b5321cc617913261c059f651d
workflow-type: tm+mt
source-wordcount: '1470'
ht-degree: 56%

---

# 클라우드 가져오기 및 내보내기 계정 구성

<!-- This page is almost duplicated with the "Configure cloud export locations" article in CJA. Differences are that Snowflake isn't supported here and there is a Suffix field for each account type. -->

>[!NOTE]
>
>계정을 만들고 편집할 때 다음 사항을 고려하십시오. <ul><li>시스템 관리자는 [사용자가 계정을 만들 수 있는지 여부 구성](/help/components/locations/locations-manager.md#configure-whether-users-can-create-accounts)에 설명된 대로 사용자가 계정을 만들지 못하도록 제한할 수 있습니다. 이 섹션에 설명된 대로 계정을 만들 수 없는 경우 시스템 관리자에게 문의하십시오.</li><li>계정은 계정을 만든 사용자 또는 시스템 관리자만 편집할 수 있습니다.</li></ul>

다음 목적 중 하나 또는 모두에 사용되는 클라우드 계정을 구성할 수 있습니다.

* [데이터 피드](/help/export/analytics-data-feed/create-feed.md)를 사용하여 파일 내보내기
* [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)을(를) 사용하여 보고서 내보내기
* [분류 세트](/help/components/classifications/sets/overview.md)를 사용하여 스키마를 가져오는 중

클라우드 계정에 액세스하려면 필요한 정보로 Adobe Analytics을 구성해야 합니다. 이 프로세스는 이 문서에 설명된 대로 계정을 추가 및 구성(예: Amazon S3 역할 ARN, Google Cloud Platform 등)한 다음 [클라우드 가져오기 및 내보내기 위치 구성](/help/components/locations/configure-import-locations.md)에 설명된 대로 해당 계정 내에서 위치(예: 계정 내 폴더)를 추가 및 구성하는 과정으로 구성됩니다.

기존 계정을 보고 삭제하는 방법에 대한 자세한 내용은 [위치 관리자](/help/components/locations/locations-manager.md)를 참조하세요.

클라우드 가져오기 또는 내보내기 계정을 구성하려면 다음을 수행합니다.

1. Adobe Analytics에서 [!UICONTROL **구성 요소**] > [!UICONTROL **위치**]&#x200B;를 선택합니다.
1. [!UICONTROL 위치] 페이지에서 [!UICONTROL **위치 계정**] 탭을 선택합니다.
1. (조건부) 시스템 관리자인 경우 [!UICONTROL **모든 사용자의 계정 보기**] 옵션을 활성화하여 조직의 모든 사용자가 만든 계정을 볼 수 있습니다.
   ![모든 사용자의 계정 보기](assets/accounts-all-users.png)
1. 새 계정을 만들려면 [!UICONTROL **계정 추가**]&#x200B;를 선택합니다.

   [!UICONTROL **위치 계정 세부 정보**] 대화 상자가 표시됩니다.

   또는

   기존 계정을 편집하려면 편집할 계정을 찾은 다음 [!UICONTROL **세부 정보 편집**] 단추를 선택합니다.

   [!UICONTROL **계정 추가**] 대화 상자가 표시됩니다.

1. 다음 정보를 지정합니다.

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
   >전자 메일 계정은 [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)에서만 사용할 수 있습니다. (전자 메일 계정은 [데이터 피드](/help/export/analytics-data-feed/create-feed.md) 또는 [분류 세트](/help/components/classifications/sets/overview.md)에서 지원되지 않습니다.)

   Azure RBAC 계정을 구성하려면 다음 정보를 지정합니다.

   | 필드 | 함수 |
   |---------|----------|
   | [!UICONTROL **수신자**] | 보고서 전송 시 특정 사용자에게 이메일 알림을 보낼 수 있습니다. 단일 이메일 주소 또는 쉼표로 구분된 이메일 주소 목록을 지정하십시오. |

   {style="table-layout:auto"}

+++

   **이전 계정 유형**

   이러한 레거시 계정 유형은 [데이터 피드](/help/export/analytics-data-feed/create-feed.md) 및 [Data Warehouse](/help/export/data-warehouse/create-request/t-dw-create-request.md)을 사용하여 데이터를 내보내는 경우에만 사용할 수 있습니다. [분류 세트](/help/components/classifications/sets/manage/schema.md)를 사용하여 데이터를 가져올 때는 이러한 옵션을 사용할 수 없습니다.

   +++FTP

   데이터 피드 데이터는 Adobe 또는 고객이 호스팅하는 FTP 위치에 전달할 수 있습니다. FTP 호스트, 사용자 이름 및 암호가 필요합니다. 폴더에 피드 파일을 배치하려면 경로 필드를 사용하십시오. 폴더는 이미 있어야 합니다. 지정된 경로가 존재하지 않을 경우 피드에서 오류가 발생합니다.

   | 필드 | 함수 |
   |---------|----------|
   | [!UICONTROL **호스트**] | 원하는 FTP 대상 URL을 입력합니다. (예: `ftp.adobe.com`) |
   | [!UICONTROL **경로**] | 비워 둘 수 있습니다. |
   | [!UICONTROL **사용자 이름**] | FTP 사이트에 로그인할 사용자 이름을 입력합니다. |
   | [!UICONTROL **암호 및 암호 확인**] | FTP 사이트에 로그인할 암호를 입력합니다. |

   {style="table-layout:auto"}

+++

   +++SFTP

   데이터 피드에 대한 SFTP 지원을 사용할 수 있습니다. 유효한 RSA 또는 DSA 공개 키를 포함하기 위해 SFTP 호스트, 사용자 이름 및 대상 사이트가 필요합니다. 피드를 만들 때 적절한 공개 키를 다운로드할 수 있습니다.

+++

   +++S3

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

+++

   +++Azure Blob

   Data Warehouse는 Azure Blob 대상을 지원합니다. 컨테이너, 계정 및 키가 필요합니다. Amazon은 데이터를 사용하지 않을 때 자동으로 암호화합니다. 데이터를 다운로드할 때 데이터 암호화는 자동으로 해제됩니다. 자세한 내용은 Microsoft Azure 문서 내에서 [저장소 계정 만들기](https://docs.microsoft.com/ko-kr/azure/storage/common/storage-quickstart-create-account?tabs=azure-portal#view-and-copy-storage-access-keys)를 참조하십시오.

   >[!NOTE]
   >
   >Data Warehouse 대상의 디스크 공간을 관리하려면 자체 프로세스를 구현해야 합니다. Adobe는 서버에서 데이터를 삭제하지 않습니다.

+++

1. [!UICONTROL **저장**]&#x200B;을 선택합니다.

1. [클라우드 가져오기 및 내보내기 위치 구성](/help/components/locations/configure-import-locations.md)을 계속합니다.
