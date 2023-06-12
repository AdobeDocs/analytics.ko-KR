---
title: 데이터 피드 만들기
description: 데이터 피드를 만드는 방법을 알아봅니다.
feature: Data Feeds
exl-id: 36c8a40e-6137-4836-9d4b-bebf17b932bc
source-git-commit: 35f33c026a679526309b09b5af61fc3fd8041c39
workflow-type: tm+mt
source-wordcount: '3209'
ht-degree: 21%

---

# 데이터 피드 만들기

>[!AVAILABILITY]
>
>이 페이지에 설명된 대상 유형 중 일부는 릴리스의 제한된 테스트 단계에 있으며 사용자 환경에서 아직 사용하지 못할 수 있습니다. 기능이 일반적으로 제공되면 이 메모는 제거됩니다. Analytics 릴리스 프로세스에 대한 자세한 내용은 [Adobe Analytics 기능 릴리스](/help/release-notes/releases.md)를 참조하십시오.

데이터 피드를 만들 때 Adobe에게 다음 내용을 제공합니다.

* 원시 데이터 파일을 전송할 대상에 대한 정보입니다

* 각 파일에 포함할 데이터

>[!NOTE]
>
>데이터 피드를 만들기 전에 데이터 피드에 대해 기본적으로 이해하고 모든 필요한 사전 요구 사항을 충족해야 합니다. 자세한 내용은 [데이터 피드 개요](data-feed-overview.md).

## 데이터 피드 만들기 및 구성

1. Adobe ID 자격 증명을 사용하여 [experiencecloud.adobe.com](https://experiencecloud.adobe.com)에 로그인합니다.
1. 오른쪽 상단의 9제곱 아이콘을 선택한 다음 을 선택합니다 [!UICONTROL **분석**].
1. 위쪽 탐색 모음에서 로 이동합니다. [!UICONTROL **관리자**] > [!UICONTROL **데이터 피드**].
1. 선택 [!UICONTROL **추가**].

   ![데이터 피드 추가](assets/datafeed-add.png)

   세 가지 주요 범주가 있는 페이지가 표시됩니다. [!UICONTROL **피드 정보**], [!UICONTROL **대상**], 및 [!UICONTROL **데이터 열 정의**].
1. 다음에서 [!UICONTROL **피드 정보**] 섹션에서 다음 필드를 작성합니다.

   | 필드 | 함수 |
   |---------|----------|
   | [!UICONTROL **이름**] | 데이터 피드의 이름입니다. 선택된 보고서 세트 내에서 고유해야 하며 최대 255자까지 사용할 수 있습니다. |
   | [!UICONTROL **보고서 세트**] | 데이터 피드의 기반이 되는 보고서 세트입니다. 동일한 보고서 세트에 대해 여러 데이터 피드를 만드는 경우 데이터 피드의 열 정의가 서로 달라야 합니다. 소스 보고서 세트만 데이터 피드를 지원합니다. 가상 보고서 세트는 지원되지 않습니다. |
   | [!UICONTROL **완료 시 이메일**] | 피드의 처리가 완료되면 알림을 받을 이메일 주소. 이메일 주소 형식을 제대로 지정해야 합니다. |
   | [!UICONTROL **피드 간격**] | 선택 **매일** 채우기 또는 내역 데이터. 일별 피드에는 보고서 세트 시간대의 자정부터 자정까지 하루 분량의 데이터가 포함됩니다.  선택 **시간별** 데이터를 계속하는 경우(원하는 경우 피드를 계속하는 경우에도 일별 사용 가능). 시간별 피드에는 1시간 동안의 데이터가 포함됩니다. |
   | [!UICONTROL **처리 지연**] | 데이터 피드 파일을 처리하기 전에 지정된 시간을 대기하십시오. 지연은 오프라인 디바이스를 온라인 상태로 전환하여 데이터를 전송할 수 있는 기회를 모바일 구현에 제공하는 데 유용합니다. 또한 이전에 처리된 파일을 관리할 때 조직의 서버측 프로세스를 수용하는 데 사용할 수도 있습니다. 대부분의 경우에는 지연이 필요하지 않습니다. 피드는 최대 120분 정도 지연될 수 있습니다. |
   | [!UICONTROL **시작 및 종료 날짜**] | 시작 날짜는 데이터 피드를 원하는 첫 번째 날짜를 나타냅니다. 이전 데이터에 대한 데이터 피드 처리를 즉시 시작하려면 이 날짜를 과거로 설정하십시오. 피드는 종료 날짜가 될 때까지 계속 처리합니다. 시작 및 종료 날짜는 보고서 세트의 시간대를 기반으로 합니다. |
   | [!UICONTROL **연속 공급**] | 이 확인란을 선택하면 종료 날짜가 제거되어 피드가 무기한 실행될 수 있습니다. 한 피드가 이전 데이터 처리를 완료하면 한 피드가 지정된 시간 또는 날 동안 데이터 수집이 완료되기를 기다립니다. 현재 시간 또는 날이 끝나면 지정된 지연 후 처리가 시작됩니다. |

1. 다음에서 [!UICONTROL **대상**] 섹션, [!UICONTROL **유형**] 드롭다운 메뉴에서 데이터를 전송할 대상을 선택합니다.

   ![데이터 피드 대상 드롭다운 메뉴](assets/datafeed-destinations-dropdown.png)

   데이터 피드를 만들 때 다음 대상 유형을 사용하십시오. 구성 지침을 보려면 대상 유형을 확장합니다. (추가 [이전 대상](#legacy-destinations) 사용할 수도 있지만 권장되지는 않습니다.)

   +++Amazon S3

   피드를 Amazon S3 버킷으로 직접 보낼 수 있습니다. 이 대상 유형에는 Amazon S3 계정과 위치(버킷)만 필요합니다.

   Adobe Analytics은 계정 간 인증을 사용하여 Adobe Analytics의 파일을 Amazon S3 인스턴스의 지정된 위치로 업로드합니다.

   Amazon S3 버킷을 데이터 피드의 대상으로 구성하려면 다음 작업을 수행하십시오.

   1. Adobe Analytics Admin Console의 [!UICONTROL **대상**] 섹션, 선택 [!UICONTROL **Amazon**].

      ![Amazon 대상](assets/datafeed-destination-amazons3.png)

   1. 선택 [!UICONTROL **위치 선택**].

      Amazon S3 내보내기 위치 페이지가 표시됩니다.

   1. (조건부) 이전에 Amazon S3 계정 및 위치를 추가한 경우:

      1. 에서 계정 선택 [!UICONTROL **계정 선택**] 드롭다운 메뉴.

      1. 에서 위치 선택 [!UICONTROL **위치 선택**] 드롭다운 메뉴.

      1. 선택 [!UICONTROL **저장**] > [!UICONTROL **저장**].

         이제 대상이 지정한 Amazon S3 위치로 데이터를 보내도록 구성되었습니다.

   1. (조건부) Amazon S3 계정을 이전에 추가하지 않은 경우:

      1. 선택 [!UICONTROL **계정 추가**]&#x200B;을(를) 클릭한 후 다음 정보를 지정합니다.

         | 필드 | 함수 |
         |---------|----------|
         | [!UICONTROL **계정 이름**] | 계정 이름. 원하는 이름을 지정할 수 있습니다. |
         | [!UICONTROL **계정 설명**] | 계정에 대한 설명. |
         | [!UICONTROL **역할 ARN**] | Adobe이 Amazon S3 계정에 대한 액세스 권한을 받는 데 사용할 수 있는 역할 ARN(Amazon 리소스 이름)을 제공해야 합니다. 이렇게 하려면 소스 계정에 대한 IAM 권한 정책을 만들고, 이 정책을 사용자에게 연결한 다음 대상 계정에 대한 역할을 만듭니다. 자세한 내용은 다음을 참조하십시오. [이 AWS 설명서](https://aws.amazon.com/premiumsupport/knowledge-center/cross-account-access-iam/). |
         | [!UICONTROL **사용자 ARN**] | Adobe ARN(Amazon 리소스 이름)은 사용자가 제공합니다. 이 사용자를 생성한 정책에 첨부해야 합니다. |

         {style="table-layout:auto"}

         1. 선택 [!UICONTROL **위치 추가**]&#x200B;을(를) 클릭한 후 다음 정보를 지정합니다.

         | 필드 | 함수 |
         |---------|----------|
         | [!UICONTROL **이름**] | 계정 이름. |
         | [!UICONTROL **설명**] | 계정에 대한 설명. |
         | [!UICONTROL **버킷**] | Adobe Analytics 데이터를 전송할 Amazon S3 계정 내의 버킷입니다. Adobe이 제공한 사용자 ARN이 이 버킷에 파일을 업로드할 수 있는 액세스 권한이 있는지 확인하십시오. |
         | [!UICONTROL **접두사**] | 데이터를 저장할 버킷 내의 폴더입니다. 폴더 이름을 지정한 다음 이름 뒤에 백슬래시를 추가하여 폴더를 만듭니다. 예, `folder_name/` |

         {style="table-layout:auto"}

      1. 선택 [!UICONTROL **만들기**] > [!UICONTROL **저장**].

         이제 대상이 지정한 Amazon S3 위치로 데이터를 보내도록 구성되었습니다.

+++

   +++Azure RBAC

   RBAC 인증을 사용하여 Azure 컨테이너로 직접 피드를 보낼 수 있습니다. 이 대상 유형에는 버킷 이름, 응용 프로그램 ID, 테넌트 ID 및 비밀 키가 필요합니다.

   Azure RBAC 버킷을 데이터 피드의 대상으로 구성하려면 다음을 수행합니다.

   1. 아직 인증하지 않았다면 Adobe Analytics에서 인증에 사용할 수 있는 Azure 애플리케이션을 만든 다음 IAM(액세스 제어)에서 액세스 권한을 부여합니다.

      자세한 내용은 [Azure Active Directory 응용 프로그램을 만드는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/howto-create-service-principal-portal).

   1. Adobe Analytics Admin Console의 [!UICONTROL **대상**] 섹션, 선택 [!UICONTROL **Azure RBAC**].

      ![Azure RBAC 대상](assets/datafeed-destination-azurerbac.png)

   1. 선택 [!UICONTROL **위치 선택**].

      [Azure RBAC 내보내기 위치] 페이지가 표시됩니다.

   1. (조건부) 이전에 Azure RBAC 계정 및 위치를 추가한 경우:

      1. 에서 계정 선택 [!UICONTROL **계정 선택**] 드롭다운 메뉴.

      1. 에서 위치 선택 [!UICONTROL **위치 선택**] 드롭다운 메뉴.

      1. 선택 [!UICONTROL **저장**] > [!UICONTROL **저장**].

         이제 대상이 지정한 Azure RBAC 위치로 데이터를 보내도록 구성되었습니다.

   1. (조건부) 이전에 Azure RBAC 계정을 추가하지 않은 경우:

      1. 선택 [!UICONTROL **계정 추가**]&#x200B;을(를) 클릭한 후 다음 정보를 지정합니다.

         | 필드 | 함수 |
         |---------|----------|
         | [!UICONTROL **계정 이름**] | Azure RBAC 계정의 이름입니다. 이 이름은 다음에 표시됩니다. [!UICONTROL **계정 선택**] 드롭다운 필드 및 은(는) 선택한 모든 이름일 수 있습니다. |
         | [!UICONTROL **계정 설명**] | Azure RBAC 계정에 대한 설명입니다. 이 설명은 다음에 표시됩니다. [!UICONTROL **계정 선택**] 드롭다운 필드 및 은(는) 선택한 모든 이름일 수 있습니다. |
         | [!UICONTROL **애플리케이션 ID**] | 생성한 Azure 애플리케이션에서 이 ID를 복사합니다. Microsoft Azure에서 이 정보는 **개요** 응용 프로그램 내의 탭입니다. 자세한 내용은 [Microsoft ID 플랫폼을 사용하여 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
         | [!UICONTROL **테넌트 ID**] | 생성한 Azure 애플리케이션에서 이 ID를 복사합니다. Microsoft Azure에서 이 정보는 **개요** 응용 프로그램 내의 탭입니다. 자세한 내용은 [Microsoft ID 플랫폼을 사용하여 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
         | [!UICONTROL **비밀**] | 생성한 Azure 애플리케이션에서 암호를 복사합니다. Microsoft Azure에서 이 정보는 **인증서 및 암호** 응용 프로그램 내의 탭입니다. 자세한 내용은 [Microsoft ID 플랫폼을 사용하여 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |

         {style="table-layout:auto"}

      1. 선택 [!UICONTROL **위치 추가**]&#x200B;을(를) 클릭한 후 다음 정보를 지정합니다.

         | 필드 | 함수 |
         |---------|----------|
         | [!UICONTROL **이름**] | 위치의 이름입니다. 이 이름은 다음에 표시됩니다. [!UICONTROL **위치 선택**] 드롭다운 필드 및 은(는) 선택한 모든 이름일 수 있습니다. |
         | [!UICONTROL **설명**] | 위치에 대한 설명. 이 설명은 다음에 표시됩니다. [!UICONTROL **위치 선택**] 드롭다운 필드 및 은(는) 선택한 모든 이름일 수 있습니다. |
         | [!UICONTROL **계정**] | Azure 스토리지 계정입니다. |
         | [!UICONTROL **컨테이너**] | Adobe Analytics 데이터를 전송할 지정한 계정 내의 컨테이너입니다. 이전에 만든 Azure 애플리케이션에 파일을 업로드할 수 있는 권한을 부여했는지 확인하십시오. |
         | [!UICONTROL **접두사**] | 데이터를 저장할 컨테이너 내의 폴더입니다. 폴더 이름을 지정한 다음 이름 뒤에 백슬래시를 추가하여 폴더를 만듭니다. 예, `folder_name/` |

         {style="table-layout:auto"}

      1. 선택 [!UICONTROL **만들기**] > [!UICONTROL **저장**].

         이제 대상이 지정한 Azure RBAC 위치로 데이터를 보내도록 구성되었습니다.

+++

   +++Azure SAS

   SAS 인증을 사용하여 Azure 컨테이너로 직접 피드를 보낼 수 있습니다. 이 대상 유형에는 버킷 이름, 응용 프로그램 ID, 테넌트 ID, 주요 자격 증명 모음 URI, 주요 자격 증명 모음 암호 이름 및 비밀 키가 필요합니다.

   Azure SAS 버킷을 데이터 피드의 대상으로 구성하려면:

   1. Adobe Analytics에서 인증에 사용할 수 있는 Azure 애플리케이션을 아직 만들지 않은 경우 만듭니다.

      자세한 내용은 [Azure Active Directory 응용 프로그램을 만드는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/howto-create-service-principal-portal).

   1. Adobe Analytics Admin Console의 [!UICONTROL **대상**] 섹션, 선택 [!UICONTROL **Azure SAS**].

      ![Azure SAS 대상](assets/datafeed-destination-azuresas.png)

   1. 선택 [!UICONTROL **위치 선택**].

      Azure SAS 내보내기 위치 페이지가 표시됩니다.

   1. (조건부) 이전에 Azure SAS 계정 및 위치를 추가한 경우:

      1. 에서 계정 선택 [!UICONTROL **계정 선택**] 드롭다운 메뉴.

      1. 에서 위치 선택 [!UICONTROL **위치 선택**] 드롭다운 메뉴.

      1. 선택 [!UICONTROL **저장**] > [!UICONTROL **저장**].

         이제 대상이 지정한 Azure SAS 위치로 데이터를 보내도록 구성되었습니다.

   1. (조건부) 이전에 Azure SAS 계정을 추가하지 않은 경우:

      1. 선택 [!UICONTROL **계정 추가**]&#x200B;을(를) 클릭한 후 다음 정보를 지정합니다.

         | 필드 | 함수 |
         |---------|----------|
         | [!UICONTROL **계정 이름**] | Azure SAS 계정의 이름입니다. 이 이름은 다음에 표시됩니다. [!UICONTROL **계정 선택**] 드롭다운 필드 및 은(는) 선택한 모든 이름일 수 있습니다. |
         | [!UICONTROL **계정 설명**] | Azure SAS 계정에 대한 설명. 이 설명은 다음에 표시됩니다. [!UICONTROL **계정 선택**] 드롭다운 필드 및 은(는) 선택한 모든 이름일 수 있습니다. |
         | [!UICONTROL **애플리케이션 ID**] | 생성한 Azure 애플리케이션에서 이 ID를 복사합니다. Microsoft Azure에서 이 정보는 **개요** 응용 프로그램 내의 탭입니다. 자세한 내용은 [Microsoft ID 플랫폼을 사용하여 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
         | [!UICONTROL **테넌트 ID**] | 생성한 Azure 애플리케이션에서 이 ID를 복사합니다. Microsoft Azure에서 이 정보는 **개요** 응용 프로그램 내의 탭입니다. 자세한 내용은 [Microsoft ID 플랫폼을 사용하여 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |
         | [!UICONTROL **키 자격 증명 모음 URI**] | <p>Azure Key Vault의 SAS 토큰 경로.  Azure SAS를 구성하려면 Azure 키 자격 증명 모음을 사용하여 SAS 토큰을 비밀로 저장해야 합니다. 자세한 내용은 [Azure Key Vault에서 암호를 설정하고 검색하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations).</p><p>Key Vault URI가 만들어진 후 Key Vault에 액세스 정책을 추가하여 만든 Azure 애플리케이션에 권한을 부여합니다. 자세한 내용은 [주요 자격 증명 모음 액세스 정책을 할당하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/key-vault/general/assign-access-policy?tabs=azure-portal).</p> |
         | [!UICONTROL **키 자격 증명 모음 암호 이름**] | Azure Key Vault에 암호를 추가할 때 만든 암호 이름입니다. Microsoft Azure에서 이 정보는 만든 Key Vault의 **주요 자격 증명 모음** 설정 페이지를 참조하십시오. 자세한 내용은 [Azure Key Vault에서 암호를 설정하고 검색하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations). |
         | [!UICONTROL **비밀**] | 생성한 Azure 애플리케이션에서 암호를 복사합니다. Microsoft Azure에서 이 정보는 **인증서 및 암호** 응용 프로그램 내의 탭입니다. 자세한 내용은 [Microsoft ID 플랫폼을 사용하여 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app). |

         {style="table-layout:auto"}

      1. 선택 [!UICONTROL **위치 추가**]&#x200B;을(를) 클릭한 후 다음 정보를 지정합니다.

         | 필드 | 함수 |
         |---------|----------|
         | [!UICONTROL **이름**] | 위치의 이름입니다. 이 이름은 다음에 표시됩니다. [!UICONTROL **위치 선택**] 드롭다운 필드 및 은(는) 선택한 모든 이름일 수 있습니다. |
         | [!UICONTROL **설명**] | 위치에 대한 설명. 이 설명은 다음에 표시됩니다. [!UICONTROL **위치 선택**] 드롭다운 필드 및 은(는) 선택한 모든 이름일 수 있습니다. |
         | [!UICONTROL **컨테이너**] | Adobe Analytics 데이터를 전송할 지정한 계정 내의 컨테이너입니다. |
         | [!UICONTROL **접두사**] | 데이터를 저장할 컨테이너 내의 폴더입니다. 폴더 이름을 지정한 다음 이름 뒤에 백슬래시를 추가하여 폴더를 만듭니다. 예, `folder_name/` |

         {style="table-layout:auto"}

      1. 선택 [!UICONTROL **만들기**] > [!UICONTROL **저장**].

         이제 대상이 지정한 Azure SAS 위치로 데이터를 보내도록 구성되었습니다.

+++

   +++Google Cloud 플랫폼

   피드를 GCP(Google Cloud Platform) 버킷으로 직접 보낼 수 있습니다. 이 대상 유형에는 GCP 계정 이름과 위치(버킷) 이름만 필요합니다.

   Adobe Analytics은 계정 간 인증을 사용하여 Adobe Analytics의 파일을 GCP 인스턴스의 지정된 위치로 업로드합니다.

   GCP 버킷을 데이터 피드의 대상으로 구성하려면 다음 작업을 수행하십시오.

   1. Adobe Analytics Admin Console의 [!UICONTROL **대상**] 섹션, 선택 [!UICONTROL **Google 클라우드 플랫폼**].

      ![Google Cloud Platform 대상](assets/datafeed-destination-gcp.png)

   1. 선택 [!UICONTROL **위치 선택**].

      [GCP 내보내기 위치] 페이지가 표시됩니다.

   1. (조건부) 이전에 GCP 계정 및 위치를 추가한 경우:

      1. 에서 계정 선택 [!UICONTROL **계정 선택**] 드롭다운 메뉴.

      1. 에서 위치 선택 [!UICONTROL **위치 선택**] 드롭다운 메뉴.

      1. 선택 [!UICONTROL **저장**] > [!UICONTROL **저장**].

         이제 대상이 지정한 GCP 위치로 데이터를 보내도록 구성되었습니다.

   1. (조건부) 이전에 GCP 계정을 추가하지 않은 경우:

      1. 선택 [!UICONTROL **계정 추가**]&#x200B;을(를) 클릭한 후 다음 정보를 지정합니다.

         | 필드 | 함수 |
         |---------|----------|
         | [!UICONTROL **계정 이름**] | 계정 이름. 원하는 이름을 지정할 수 있습니다. |
         | [!UICONTROL **계정 설명**] | 계정에 대한 설명. |
         | [!UICONTROL **프로젝트 ID**] | Google Cloud 프로젝트 ID입니다. 다음을 참조하십시오. [프로젝트 ID 가져오기에 대한 Google Cloud 설명서](https://cloud.google.com/resource-manager/docs/creating-managing-projects#identifying_projects). |
         | [!UICONTROL **주체**] | 원칙은 Adobe에서 제공합니다. 피드를 받으려면 이 사용자에게 권한을 부여해야 합니다. 다음을 참조하십시오. [정책에 주도자 추가에 대한 Google Cloud 설명서](https://cloud.google.com/storage/docs/access-control/using-iam-permissions#bucket-iam). |

         {style="table-layout:auto"}

         1. 선택 [!UICONTROL **위치 추가**]&#x200B;을(를) 클릭한 후 다음 정보를 지정합니다.

         | 필드 | 함수 |
         |---------|----------|
         | [!UICONTROL **주체**] | 원칙은 Adobe에서 제공합니다. 이 사용자에게 피드를 수신할 수 있는 권한을 부여해야 합니다. |
         | [!UICONTROL **이름**] | 계정 이름. |
         | [!UICONTROL **설명**] | 계정에 대한 설명. |
         | [!UICONTROL **버킷**] | Adobe Analytics 데이터를 전송할 GCP 계정 내의 버킷입니다. 이 버킷에 파일을 업로드할 수 있도록 Adobe이 제공한 사용자에 대한 권한을 부여했는지 확인하십시오. |
         | [!UICONTROL **접두사**] | 데이터를 저장할 버킷 내의 폴더입니다. 폴더 이름을 지정한 다음 이름 뒤에 백슬래시를 추가하여 폴더를 만듭니다. 예, `folder_name/` |

         {style="table-layout:auto"}

      1. 선택 [!UICONTROL **만들기**] > [!UICONTROL **저장**].

         이제 대상이 지정한 GCP 위치로 데이터를 보내도록 구성되었습니다.

+++

1. 다음에서  [!UICONTROL **데이터 열 정의**] 섹션, 최신 항목 선택 [!UICONTROL **모든 Adobe Columns**] 드롭다운에서 템플릿을 만든 다음 다음 다음 필드를 작성합니다.

   | 필드 | 함수 |
   |---------|----------|
   | [!UICONTROL **이스케이프 처리된 문자 제거**] | 데이터를 수집할 때 일부 문자(예: 줄바꿈)가 문제를 초래할 수 있습니다. 피드 파일에서 이러한 문자를 제거하려면 이 확인란을 선택하십시오. |
   | [!UICONTROL **압축 포맷**] | 사용된 압축 유형입니다. **** Gzip은 파일을 `.tar.gz` 형식으로 출력합니다. **** Zip은 파일을 `.zip` 형식으로 출력합니다. |
   | [!UICONTROL **패키징 타입**] | 선택 **여러 파일** 대부분의 데이터 피드에 사용됩니다. 이 옵션은 데이터를 압축되지 않은 2GB 청크로 페이지를 매깁니다. (여러 파일을 선택하고 보고 기간의 압축되지 않은 데이터가 2GB 미만이면 하나의 파일이 전송됩니다.) 선택 **단일 파일** 다음을 출력합니다. `hit_data.tsv` 하나의 파일로 된 파일로, 규모가 클 수 있습니다. |
   | [!UICONTROL **매니페스트**] | Adobe이 다음을 전달해야 하는지 여부 [매니페스트 파일](c-df-contents/datafeeds-contents.md#feed-manifest) 피드 간격에 대한 데이터가 수집되지 않을 때 대상으로 전송됩니다. 다음을 선택하는 경우 **매니페스트 파일**, 수집된 데이터가 없을 때 다음과 유사한 매니페스트 파일을 받게 됩니다.<p>`text`</p><p>`Datafeed-Manifest-Version: 1.0`</p><p>`Lookup-Files: 0`</p><p>`Data-Files: 0`</p><p> `Total-Records: 0`</p> |
   | [!UICONTROL **열 템플릿**] | Adobe 많은 데이터 피드를 만들 때는 열 템플릿을 만드는 것이 좋습니다. 열 템플릿을 선택하면 지정된 열이 템플릿에 자동으로 포함됩니다. Adobe도 기본적으로 여러 템플릿을 제공합니다. |
   | [!UICONTROL **사용 가능한 열**] | Adobe Analytics에서 사용 가능한 모든 데이터 열. 데이터 피드에 모든 열을 포함하려면 [!UICONTROL 모두 추가]를 클릭하십시오. |
   | [!UICONTROL **포함된 열**] | 데이터 피드에 포함할 열입니다. 데이터 피드에 모든 열을 제거하려면 [!UICONTROL 모두 제거]를 클릭하십시오. |
   | [!UICONTROL **CSV 다운로드**] | 포함된 모든 열이 포함된 CSV 파일을 다운로드합니다. |

1. 선택 [!UICONTROL **저장**] 오른쪽 상단에서

   내역 데이터 처리는 즉시 시작됩니다. 하루 동안 데이터 처리가 완료되면 파일이 구성한 대상으로 전송됩니다.

   데이터 피드에 액세스하고 데이터 피드의 콘텐츠를 더 잘 이해하는 방법에 대한 자세한 내용은 을 참조하십시오. [데이터 피드 콘텐츠 - 개요](/help/export/analytics-data-feed/c-df-contents/datafeeds-contents.md).

## 이전 대상

>[!IMPORTANT]
>
>이 섹션에 설명된 대상은 기존 대상이며, 권장되지 않습니다. 대신 데이터 피드를 만들 때 Amazon S3, Google Cloud Platform, Azure RBAC 또는 Azure SAS 대상 중 하나를 사용합니다. 다음을 참조하십시오 [데이터 피드 만들기 및 구성](#create-and-configure-a-data-feed) 이러한 각 권장 대상에 대한 자세한 내용은 를 참조하십시오.


다음 정보는 각 기존 대상에 대한 구성 정보를 제공합니다.

### FTP

데이터 피드 데이터는 Adobe 또는 고객이 호스팅하는 FTP 위치에 전달할 수 있습니다. FTP 호스트, 사용자 이름 및 암호가 필요합니다. 폴더에 피드 파일을 배치하려면 경로 필드를 사용하십시오. 폴더는 이미 있어야 합니다. 지정된 경로가 존재하지 않을 경우 피드에서 오류가 발생합니다.

사용 가능한 필드를 완성할 때 다음 정보를 사용하십시오.
* [!UICONTROL **호스트**]: 원하는 FTP 대상 URL을 입력합니다. (예: `ftp://ftp.omniture.com`)
* [!UICONTROL **경로**]: 비워 둘 수 있음
* [!UICONTROL **사용자 이름**]: FTP 사이트에 로그인할 사용자 이름을 입력합니다.
* [!UICONTROL **암호 및 암호 확인**]: FTP 사이트에 로그인할 암호를 입력합니다.

### SFTP

데이터 피드에 대한 SFTP 지원을 사용할 수 있습니다. 유효한 RSA 또는 DSA 공개 키를 포함하기 위해 SFTP 호스트, 사용자 이름 및 대상 사이트가 필요합니다. 피드를 만들 때 적절한 공개 키를 다운로드할 수 있습니다.

### S3

피드를 Amazon S3 버킷으로 직접 보낼 수 있습니다. 이 대상 유형에는 버킷 이름, 액세스 키 ID 및 보안 키가 필요합니다. 자세한 내용은 Amazon S3 문서 내의 [Amazon S3 버킷 이름 지정 요구 사항](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-s3-bucket-naming-requirements.html)을 참조하십시오.

데이터 피드 업로드를 위해 제공한 사용자는 다음 [권한](https://docs.aws.amazon.com/AmazonS3/latest/API/API_Operations_Amazon_Simple_Storage_Service.html)이 있어야 합니다.

* s3:GetObject
* s3:PutObject
* s3:PutObjectAcl

  >[!NOTE]
  >
  >Amazon S3 버킷에 대한 각 업로드의 경우 [!DNL Analytics]는 버킷에 필요한 정책이 있는지 여부에 관계없이 버킷 소유자를 BucketOwnerFullControl ACL에 추가합니다. 자세한 내용은 &quot;[Amazon S3 데이터 피드에 대한 BucketOwnerFullControl 설정은 무엇입니까?](df-faq.md#BucketOwnerFullControl)&quot;

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

데이터 피드는 Azure Blob 대상을 지원합니다. 컨테이너, 계정 및 키가 필요합니다. Amazon은 데이터를 사용하지 않을 때 자동으로 암호화합니다. 데이터를 다운로드할 때 데이터 암호화는 자동으로 해제됩니다. 자세한 내용은 Microsoft Azure 문서 내에서 [저장소 계정 만들기](https://docs.microsoft.com/ko-kr/azure/storage/common/storage-quickstart-create-account?tabs=azure-portal#view-and-copy-storage-access-keys)를 참조하십시오.

>[!NOTE]
>
>피드 대상의 디스크 공간을 관리하려면 자체 프로세스를 구현해야 합니다. Adobe는 서버에서 데이터를 삭제하지 않습니다.
