---
description: 분류 데이터를 업로드할 수 있는 클라우드 가져오기 계정 및 위치를 구성합니다.
keywords: Analysis Workspace
title: 클라우드 가져오기 위치 구성
feature: Classifications
source-git-commit: 8d6ee33e867da274334c8adc557105af4942c894
workflow-type: tm+mt
source-wordcount: '1356'
ht-degree: 6%

---

# 클라우드 가져오기 위치 구성

<!-- This page is almost duplicated with the "Configure cloud export locations" article in CJA. Differences are that Snowflake isn't supported here and there is a Suffix field for each account type. -->

클라우드 대상에서 Adobe Analytics 분류 데이터를 가져오려면 먼저 분류 데이터를 수집할 위치를 추가하고 구성해야 합니다.

이 프로세스는 계정(예: Amazon S3 역할 ARN, Google Cloud Platform 등)과 계정 내 위치(예: 계정 내 폴더)를 추가하고 구성하는 것으로 구성됩니다.

## 계정 추가

클라우드 대상 계정에 액세스하려면 필요한 정보로 Adobe Analytics을 구성해야 합니다.

1. Adobe Analytics에서 [!UICONTROL **구성 요소**] > [!UICONTROL **위치**].
1. 다음에서 [!UICONTROL 위치] 페이지에서 [!UICONTROL **위치 자격 증명**] 탭.
1. 선택 [!UICONTROL **계정 추가**]. <!-- add screenshot? -->

   계정 추가 대화 상자가 표시됩니다.
1. 다음 정보를 지정합니다. |필드 | 함수 | ------------------- | [!UICONTROL **위치 계정 이름**] | 위치 계정 이름입니다. 이 이름은 위치를 만들 때 나타납니다 | | [!UICONTROL **위치 계정 설명**] | 같은 계정 유형의 다른 계정과 구분할 수 있도록 계정에 대한 간단한 설명을 제공합니다. | | [!UICONTROL **계정 유형**] | 클라우드 계정 유형을 선택합니다. 각 계정 유형에 대해 해당 계정 내에서 필요에 따라 여러 위치가 있는 단일 계정을 사용하는 것이 좋습니다. |
1. 다음에서 [!UICONTROL **계정 속성**] 섹션에서 선택한 계정 유형과 관련된 정보를 지정합니다.

   구성 지침을 보려면 아래에 있는 해당 섹션을 확장합니다. [!UICONTROL **계정 유형**] 을(를) 선택합니다.

   +++Amazon S3 Role ARN

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
   | [!UICONTROL **위치 계정 암호**] | 생성한 Azure 애플리케이션에서 암호를 복사합니다. Microsoft Azure에서 이 정보는 **인증서 및 암호** 응용 프로그램 내의 탭입니다. 자세한 내용은 [Microsoft ID 플랫폼을 사용하여 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |

   {style="table-layout:auto"}

+++

   +++Azure RBAC

   Azure RBAC 계정을 구성하려면 다음 정보를 지정하십시오.

   | 필드 | 함수 |
   |---------|----------|
   | [!UICONTROL **애플리케이션 ID**] | 생성한 Azure 애플리케이션에서 이 ID를 복사합니다. Microsoft Azure에서 이 정보는 **개요** 응용 프로그램 내의 탭입니다. 자세한 내용은 [Microsoft ID 플랫폼을 사용하여 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
   | [!UICONTROL **테넌트 ID**] | 생성한 Azure 애플리케이션에서 이 ID를 복사합니다. Microsoft Azure에서 이 정보는 **개요** 응용 프로그램 내의 탭입니다. 자세한 내용은 [Microsoft ID 플랫폼을 사용하여 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
   | [!UICONTROL **위치 계정 암호**] | 생성한 Azure 애플리케이션에서 암호를 복사합니다. Microsoft Azure에서 이 정보는 **인증서 및 암호** 응용 프로그램 내의 탭입니다. 자세한 내용은 [Microsoft ID 플랫폼을 사용하여 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |

   {style="table-layout:auto"}

+++

1. [!UICONTROL **저장**]&#x200B;을 선택합니다.

1. 계속 [위치 추가](#add-a-location).

## 위치 추가

1. 위치를 추가하려면 먼저 계정을 추가해야 합니다. [계정 추가](#add-an-account) 아직 안왔으면
1. Adobe Analytics에서 [!UICONTROL **구성 요소**] > [!UICONTROL **위치**].
1. 다음에서 [!UICONTROL 위치] 페이지에서 [!UICONTROL **위치**] 탭.
1. 선택 [!UICONTROL **위치 추가**]. <!-- add screenshot? -->

   위치 대화 상자가 표시됩니다.
1. 다음 정보를 지정합니다. |필드 | 함수 | ------------------- | [!UICONTROL **이름**] | 위치의 이름입니다.  | | [!UICONTROL **설명**] | 같은 계정 유형의 다른 계정과 구분할 수 있도록 계정에 대한 간단한 설명을 제공합니다. | | [!UICONTROL **위치 계정**] | 만든 위치 계정 선택 [계정 추가](#add-an-account). |

1. 다음에서 [!UICONTROL **위치 속성**] 섹션에서 위치 계정의 계정 유형과 관련된 정보를 지정합니다.

   구성 지침을 보려면 아래에서 선택한 계정 유형에 해당하는 아래 섹션을 확장합니다. [!UICONTROL **위치 계정**] 필드.

   +++Amazon S3 Role ARN

   Amazon S3 역할 ARN 위치를 구성하려면 다음 정보를 지정하십시오.

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
   | [!UICONTROL **버킷 이름**] | Adobe Analytics 데이터를 전송할 GCP 계정 내의 버킷입니다. 이 버킷에 파일을 업로드할 수 있도록 Adobe이 제공한 사용자에 대한 권한을 부여했는지 확인하십시오. |
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