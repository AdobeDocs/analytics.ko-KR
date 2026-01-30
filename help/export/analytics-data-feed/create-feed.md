---
title: 데이터 피드 만들기
description: 데이터 피드를 만드는 방법과 Adobe에 제공할 파일 정보에 대해 알아봅니다.
feature: Data Feeds
exl-id: 36c8a40e-6137-4836-9d4b-bebf17b932bc
source-git-commit: ee29f837d72cf3243e92230dbee5b379d1c6c415
workflow-type: tm+mt
source-wordcount: '4257'
ht-degree: 99%

---

# 데이터 피드 만들기

데이터 피드를 만들 때 Adobe에 다음 기능을 제공합니다.

* 원시 데이터 파일을 전송할 대상에 대한 정보
* 각 파일에 포함할 데이터

데이터 피드를 만들기 전에 데이터 피드에 대해 기본적으로 이해하고 모든 전제 조건을 충족하는지 확인하는 것이 중요합니다. 자세한 내용은 [데이터 피드 개요](data-feed-overview.md)를 참조하십시오.

## 데이터 피드 만들기 및 구성 {#create-and-configure-data-feed}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_datafeed_os_strings"
>title="운영 체제 문자열 바꾸기"
>abstract="이 옵션은 고객 데이터에 임베드된 다음 문자열 시퀀스를 감지하고 공백으로 대체하여 데이터 출력을 정리합니다. <br/>Windows: CRLF, CR 또는 TAB<br/>Mac 및 Linux: \n, \r 또는 \t"

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_datafeed_export_file"
>title="매니페스트"
>abstract="각 데이터 피드 게재에 매니페스트 파일을 포함할지 여부를 선택합니다. 매니페스트 파일에는 데이터 피드에 포함된 각 파일에 대한 정보가 있습니다. 데이터 피드 데이터를 하나의 패키지로 보낼 때, 완료한 파일을 포함하도록 선택할 수도 있지만, 매니페스트 파일이 권장됩니다. "

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_datafeed_notify"
>title="완료되면 알림"
>abstract="데이터 피드를 보낸 후 알림을 배달해야 하는 이메일 주소를 하나 이상 지정합니다. 여러 이메일 주소는 쉼표로 구분해야 합니다."

<!-- markdownlint-enable MD034 -->

1. Adobe ID 자격 증명을 사용하여 [experiencecloud.adobe.com](https://experiencecloud.adobe.com)에 로그인합니다.
1. 오른쪽 상단에 있는 9제곱 아이콘을 선택한 다음 [!UICONTROL **Analytics**]&#x200B;을 선택합니다.
1. 맨 위 탐색 막대에서 [!UICONTROL **관리자**] > [!UICONTROL **데이터 피드**]&#x200B;로 이동합니다.
1. [!UICONTROL **추가**]&#x200B;를 선택합니다.

   ![데이터 피드 추가](assets/datafeed-add.png)

   [!UICONTROL **피드 정보**], [!UICONTROL **대상**] 및 [!UICONTROL **데이터 열 정의**], 이렇게 세 가지 주요 카테고리로 페이지가 표시됩니다.
1. [!UICONTROL **피드 정보**] 섹션에서 다음 필드를 작성합니다.

   | 필드 | 함수 |
   |---------|----------|
   | [!UICONTROL **이름**] | 데이터 피드의 이름. 선택된 보고서 세트 내에서 고유해야 하며 최대 255자까지 사용할 수 있습니다. [자세히 알아보기](/help/export/analytics-data-feed/df-faq.md#must-feed-names-be-unique) |
   | [!UICONTROL **보고서 세트**] | 데이터 피드의 기반이 되는 보고서 세트. 동일한 보고서 세트에 대해 여러 데이터 피드를 만드는 경우 데이터 피드의 열 정의가 서로 달라야 합니다. 소스 보고서 세트만 데이터 피드를 지원합니다. 가상 보고서 세트는 지원되지 않습니다. |
   | [!UICONTROL **완료 시 이메일 보내기**] | 피드의 처리가 완료되면 알림을 받을 이메일 주소. 이메일 주소 포맷을 제대로 지정해야 합니다. |
   | [!UICONTROL **피드 간격**] | 채우기 또는 내역 데이터에 대해 **일별**&#x200B;을 선택합니다. 일별 피드에는 보고서 세트 시간대의 자정부터 자정까지 하루 분량의 데이터가 포함됩니다. 데이터를 계속 사용하려면 **시간별**&#x200B;을 선택합니다(원하는 경우 일별 피드 계속 사용 가능). 시간별 피드에는 1시간 동안의 데이터가 포함됩니다. |
   | [!UICONTROL **처리 지연**] | 데이터 피드 파일을 처리하기 전에 지정된 시간을 대기합니다. 지연은 오프라인 디바이스를 온라인 상태로 전환하여 데이터를 전송할 수 있는 기회를 모바일 구현에 제공하는 데 유용합니다. 또한 이전에 처리된 파일을 관리할 때 조직의 서버측 프로세스를 수용하는 데 사용할 수도 있습니다. 대부분의 경우에는 지연이 필요하지 않습니다. 피드는 최대 120분 정도 지연될 수 있습니다. |
   | [!UICONTROL **시작 및 종료 일자**] | 시작 일자는 데이터 피드를 시작할 일자를 나타냅니다. 내역 데이터에 대한 데이터 피드를 즉시 처리하려면, 데이터가 수집되던 과거의 날짜로 이 날짜를 설정합니다. 시작 및 종료 일자는 보고서 세트의 시간대를 기반으로 합니다. |
   | [!UICONTROL **지속 피드**] | 이 확인란을 선택하면 종료 일자가 제거되어 피드가 무기한 실행될 수 있습니다. 한 피드가 이전 데이터 처리를 완료하면 한 피드가 지정된 시간 또는 날 동안 데이터 수집이 완료되기를 기다립니다. 현재 시간 또는 날이 끝나면 지정된 지연 후 처리가 시작됩니다. |

1. [!UICONTROL **대상**] 섹션의 [!UICONTROL **유형**] 드롭다운 메뉴에서 데이터를 전송할 대상을 선택합니다.

   >[!NOTE]
   >
   >보고서 대상 구성 시 다음과 같은 사항을 고려하십시오.
   >
   >* 보고서 대상에 클라우드 계정을 사용하는 것이 좋습니다. [이전 FTP 및 SFTP 계정](#legacy-destinations)은 사용할 수 있지만 권장되지 않습니다.
   >* 이전에 구성한 모든 클라우드 계정을 데이터 피드에 사용할 수 있습니다. 다음 방법 중 하나로 클라우드 계정을 구성할 수 있습니다.
   >
   >   * [Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)에 대한 클라우드 계정을 구성할 때
   >   
   >   * [Adobe Analytics 분류 데이터를 가져올 때](/help/components/locations/locations-manager.md)(분류 데이터를 가져오도록 구성된 모든 위치를 사용할 수 없음).
   >   
   >   * [구성 요소 > 위치](/help/components/locations/configure-import-accounts.md)의 위치 관리자에서
   >
   >* 클라우드 계정은 Adobe Analytics 사용자 계정과 연계되어 있습니다. 다른 사용자는 구성된 클라우드 계정을 사용하거나 볼 수 없습니다.
   >
   >* [구성 요소 > 위치](/help/components/locations/configure-import-accounts.md)의 위치 관리자에서 생성한 모든 위치를 편집할 수 있습니다.

   ![데이터 피드 대상 드롭다운 메뉴](assets/datafeed-destinations-dropdown.png)

   데이터 피드를 만들 때 다음 대상 유형 중 하나를 사용합니다. 구성 지침을 보려면 대상 유형을 확장합니다. (추가 [기존 대상](#legacy-destinations)은 사용할 수도 있지만 권장되지 않습니다.)

   +++Amazon S3

   피드를 Amazon S3 버킷으로 직접 보낼 수 있습니다. 이 대상 유형에는 Amazon S3 계정과 위치(버킷)만 필요합니다.

   Adobe Analytics는 교차 계정 인증을 사용하여 Adobe Analytics의 파일을 Amazon S3 인스턴스의 지정된 위치로 업로드합니다.

   데이터 피드와 함께 Amazon S3를 사용하는 경우 SSE-S3 암호화만 지원됩니다.

   Amazon S3 버킷을 데이터 피드의 대상으로 구성하려면 다음 작업을 수행합니다.

   1. [데이터 피드 만들기 및 구성](#create-and-configure-a-data-feed)에 설명된 대로 데이터 피드 만들기를 시작합니다.

   1. [!UICONTROL **대상**] 섹션의 [!UICONTROL **유형**] 드롭다운 메뉴에서 [!UICONTROL **Amazon S3**]&#x200B;를 선택합니다.

      ![Amazon S3 대상](assets/datafeed-destination-amazons3.png)

   1. [!UICONTROL **위치 선택**]&#x200B;을 선택합니다.

      Amazon S3 내보내기 위치 페이지가 표시됩니다.

   1. (조건부) Adobe Analytics에 Amazon S3 계정(및 해당 계정의 위치)이 이미 구성된 경우, 데이터 피드 대상으로 사용할 수 있습니다.

      >[!NOTE]
      >
      >계정은 귀하가 구성했거나 귀하가 속한 조직과 공유된 경우에만 사용할 수 있습니다.

      1. [!UICONTROL **계정 선택**] 드롭다운 메뉴에서 계정을 선택합니다.

         Adobe Analytics의 다음 영역 중 하나에서 구성한 모든 클라우드 계정을 사용할 수 있습니다.

         * [스키마](/help/components/classifications/sets/manage/schema.md)에 설명된 대로 Adobe Analytics 분류 데이터를 가져올 때

           하지만 분류 데이터 가져오기에 대해 구성된 위치는 사용할 수 없습니다. 대신 아래 설명된 대로 새 대상을 추가합니다.

         * [클라우드 가져오기 및 내보내기 계정 구성](/help/components/locations/configure-import-accounts.md) 및 [클라우드 가져오기 및 내보내기 위치 구성](/help/components/locations/configure-import-locations.md)에 설명된 대로 위치 영역에서 계정 및 위치를 구성할 때

      1. [!UICONTROL **위치 선택**] 드롭다운 메뉴에서 위치를 선택합니다.

      1. [!UICONTROL **저장**] > [!UICONTROL **저장**]&#x200B;을 선택합니다.

      이제 대상이 지정한 Amazon S3 위치로 데이터를 전송하도록 구성됩니다.

   1. (조건부) 이전에 Amazon S3 계정을 추가하지 않은 경우

      1. [!UICONTROL **계정 추가**]&#x200B;를 선택하고 다음 정보를 지정합니다.

         | 필드 | 함수 |
         |---------|----------|
         | [!UICONTROL **계정 이름**] | 계정 이름. 원하는 이름을 선택할 수 있습니다. |
         | [!UICONTROL **계정 설명**] | 계정에 대한 설명. |
         | [!UICONTROL **Role ARN**] | Adobe가 Amazon S3 계정에 액세스하는 데 사용할 수 있는 Role ARN(Amazon 리소스 이름)을 제공해야 합니다. 이렇게 하려면 소스 계정에 대한 권한 정책을 만들고 해당 정책을 사용자에게 첨부한 다음 대상 계정에 대한 역할을 생성합니다. 자세한 내용은 [이 AWS 설명서](https://aws.amazon.com/premiumsupport/knowledge-center/cross-account-access-iam/)를 참조하십시오. |
         | [!UICONTROL **사용자 ARN**] | 사용자 ARN(Amazon 리소스 이름)은 Adobe에서 제공합니다. 사용자가 만든 정책에 이 사용자를 첨부해야 합니다. |

         {style="table-layout:auto"}

      1. [!UICONTROL **위치 추가**]&#x200B;를 선택하고 다음 정보를 지정합니다.

         | 필드 | 함수 |
         |---------|----------|
         | [!UICONTROL **이름**] | 계정 이름. |
         | [!UICONTROL **설명**] | 계정에 대한 설명. |
         | [!UICONTROL **버킷**] | Adobe Analytics 데이터를 전송할 Amazon S3 계정 내부 버킷입니다. <p>이 버킷에 파일을 업로드하려면 Adobe에서 제공한 사용자 ARN에 `S3:PutObject` 권한이 있는지 확인합니다. 이 권한을 사용하면 사용자 ARN에서 초기 파일을 업로드하고 후속 업로드에 파일을 덮어쓸 수 있습니다.</p><p>버킷 이름은 특정 이름 지정 규칙을 충족해야 합니다. 예를 들면 3~63자 사이여야 하며 소문자, 숫자, 점(.), 하이픈(-)만 사용할 수 있고 문자나 숫자로 시작하고 끝나야 합니다. [이름 지정 규칙의 전체 목록은 AWS 설명서에서 확인할 수 있습니다](https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html). </p> |
         | [!UICONTROL **접두사**] | 데이터를 입력할 버킷 내부 폴더입니다. 폴더 이름을 지정한 다음 이름 뒤에 백슬래시를 추가하여 폴더를 만듭니다. 예를 들어 `folder_name/` |

         {style="table-layout:auto"}

      1. [!UICONTROL **만들기**] > [!UICONTROL **저장**]&#x200B;을 선택합니다.

         이제 대상이 지정한 Amazon S3 위치로 데이터를 전송하도록 구성됩니다.

      1. (조건부) 방금 만든 대상(계정 및 위치)을 관리해야 하는 경우 [위치 관리자](/help/components/locations/locations-manager.md)에서 사용할 수 있습니다.

   +++

   +++Azure RBAC

   RBAC 인증을 사용하여 Azure 컨테이너로 직접 피드를 보낼 수 있습니다. 이 대상 유형에는 애플리케이션 ID, 테넌트 ID 및 암호가 필요합니다.

   Azure RBAC 계정을 데이터 피드의 대상으로 구성하려면 다음을 수행합니다.

   1. 아직 인증하지 않았다면 Adobe Analytics에서 인증에 사용할 수 있는 Azure 애플리케이션을 만든 다음 액세스 제어(IAM)에서 액세스 권한을 부여합니다.

      자세한 내용은 Azure Active Directory 애플리케이션을 만드는 방법에 대한 [Microsoft Azure 설명서](https://learn.microsoft.com/ko-kr/azure/active-directory/develop/howto-create-service-principal-portal)를 참조하십시오.

   1. Adobe Analytics Admin Console의 [!UICONTROL **대상**] 섹션의 [!UICONTROL **유형**] 드롭다운 메뉴에서 [!UICONTROL **Azure RBAC**]&#x200B;를 선택합니다.

      ![Azure RBAC 대상](assets/datafeed-destination-azurerbac.png)

   1. [!UICONTROL **위치 선택**]&#x200B;을 선택합니다.

      Azure RBAC 내보내기 위치 페이지가 표시됩니다.

   1. (조건부) Adobe Analytics에 Azure RBAC 계정(및 해당 계정의 위치)이 이미 구성된 경우, 데이터 피드 대상으로 사용할 수 있습니다.

      >[!NOTE]
      >
      >계정은 귀하가 구성했거나 귀하가 속한 조직과 공유된 경우에만 사용할 수 있습니다.

      1. [!UICONTROL **계정 선택**] 드롭다운 메뉴에서 계정을 선택합니다.

      Adobe Analytics의 다음 영역 중 하나에서 구성한 모든 클라우드 계정을 사용할 수 있습니다.

      * [스키마](/help/components/classifications/sets/manage/schema.md)에 설명된 대로 Adobe Analytics 분류 데이터를 가져올 때

        하지만 분류 데이터 가져오기에 대해 구성된 위치는 사용할 수 없습니다. 대신 아래 설명된 대로 새 대상을 추가합니다.

      * [클라우드 가져오기 및 내보내기 계정 구성](/help/components/locations/configure-import-accounts.md) 및 [클라우드 가져오기 및 내보내기 위치 구성](/help/components/locations/configure-import-locations.md)에 설명된 대로 위치 영역에서 계정 및 위치를 구성할 때

      1. [!UICONTROL **위치 선택**] 드롭다운 메뉴에서 위치를 선택합니다.

      1. [!UICONTROL **저장**] > [!UICONTROL **저장**]&#x200B;을 선택합니다.

         이제 대상이 지정한 Azure RBAC 위치로 데이터를 전송하도록 구성됩니다.

   1. (조건부) 이전에 Azure RBAC 계정을 추가하지 않은 경우

      1. [!UICONTROL **계정 추가**]&#x200B;를 선택하고 다음 정보를 지정합니다.

         | 필드 | 함수 |
         |---------|----------|
         | [!UICONTROL **계정 이름**] | Azure RBAC 계정 이름. 이 이름은 [!UICONTROL **계정 선택**] 드롭다운 필드에 표시되며, 선택한 이름을 사용할 수 있습니다. |
         | [!UICONTROL **계정 설명**] | Azure RBAC 계정에 대한 설명. 이 설명은 [!UICONTROL **계정 선택**] 드롭다운 필드에 표시되며, 선택한 이름을 사용할 수 있습니다. |
         | [!UICONTROL **애플리케이션 ID**] | 만든 Azure 애플리케이션에서 이 ID를 복사합니다. 이 정보는 Microsoft Azure의 애플리케이션 내부 **개요** 탭에 있습니다. 자세한 내용은 [Microsoft ID 플랫폼으로 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app)를 참조하십시오. |
         | [!UICONTROL **테넌트 ID**] | 만든 Azure 애플리케이션에서 이 ID를 복사합니다. 이 정보는 Microsoft Azure의 애플리케이션 내부 **개요** 탭에 있습니다. 자세한 내용은 [Microsoft ID 플랫폼으로 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app)를 참조하십시오. |
         | [!UICONTROL **암호**] | 만든 Azure 애플리케이션에서 암호를 복사합니다. 이 정보는 Microsoft Azure의 애플리케이션 내부 **인증서 및 암호** 애플리케이션 탭에 있습니다. 자세한 내용은 [Microsoft ID 플랫폼으로 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app)를 참조하십시오. |

         {style="table-layout:auto"}

      1. [!UICONTROL **위치 추가**]&#x200B;를 선택하고 다음 정보를 지정합니다.

         | 필드 | 함수 |
         |---------|----------|
         | [!UICONTROL **이름**] | 위치의 이름. 이 이름은 [!UICONTROL **위치 선택**] 드롭다운 필드에 표시되며, 선택한 이름을 사용할 수 있습니다. |
         | [!UICONTROL **설명**] | 위치에 대한 설명. 이 설명은 [!UICONTROL **위치 선택**] 드롭다운 필드에 표시되며, 선택한 이름을 사용할 수 있습니다. |
         | [!UICONTROL **계정**] | Azure 스토리지 계정. |
         | [!UICONTROL **컨테이너**] | Adobe Analytics 데이터 전송 위치를 지정한 계정 내 컨테이너입니다. 앞서 만든 Azure 애플리케이션에 파일을 업로드할 권한을 부여하고 있는지 확인합니다. |
         | [!UICONTROL **접두사**] | 데이터를 입력할 컨테이너 내부 폴더입니다. 폴더 이름을 지정한 다음 이름 뒤에 백슬래시를 추가하여 폴더를 만듭니다. 예를 들어 `folder_name/`<p>컨테이너(폴더)에 액세스하려면 Azure RBAC 계정 구성 시 지정한 애플리케이션 ID에 `Storage Blob Data Contributor` 역할이 부여되었는지 확인합니다.</p> <p>자세한 내용은 [Azure 기본 제공 역할](https://learn.microsoft.com/ko-kr/azure/role-based-access-control/built-in-roles)을 참조하십시오.</p> |

         {style="table-layout:auto"}

      1. [!UICONTROL **만들기**] > [!UICONTROL **저장**]&#x200B;을 선택합니다.

         이제 대상이 지정한 Azure RBAC 위치로 데이터를 전송하도록 구성됩니다.

      1. (조건부) 방금 만든 대상(계정 및 위치)을 관리해야 하는 경우 [위치 관리자](/help/components/locations/locations-manager.md)에서 사용할 수 있습니다.

   +++

   +++Azure SAS

   SAS 인증을 사용하여 Azure 컨테이너로 직접 피드를 보낼 수 있습니다. 이 대상 유형에는 애플리케이션 ID, 테넌트 ID, 키 자격 증명 모음 URI, 키 자격 증명 모음 암호 이름 및 암호가 필요합니다.

   Azure SAS를 데이터 피드의 대상으로 구성하려면:

   1. 아직 만들지 않은 경우 Adobe Analytics에서 인증에 사용할 수 있는 Azure 애플리케이션을 만듭니다.

      자세한 내용은 Azure Active Directory 애플리케이션을 만드는 방법에 대한 [Microsoft Azure 설명서](https://learn.microsoft.com/ko-kr/azure/active-directory/develop/howto-create-service-principal-portal)를 참조하십시오.

   1. Adobe Analytics Admin Console의 [!UICONTROL **대상**] 섹션에서 [!UICONTROL **Azure SAS**]&#x200B;를 선택합니다.

      ![Azure SAS 대상](assets/datafeed-destination-azuresas.png)

   1. [!UICONTROL **위치 선택**]&#x200B;을 선택합니다.

      Azure SAS 내보내기 위치 페이지가 표시됩니다.

   1. (조건부) Adobe Analytics에 Azure SAS 계정(및 해당 계정의 위치)이 이미 구성된 경우, 데이터 피드 대상으로 사용할 수 있습니다.

      >[!NOTE]
      >
      >계정은 귀하가 구성했거나 귀하가 속한 조직과 공유된 경우에만 사용할 수 있습니다.

      1. [!UICONTROL **계정 선택**] 드롭다운 메뉴에서 계정을 선택합니다.

         Adobe Analytics의 다음 영역 중 하나에서 구성한 모든 클라우드 계정을 사용할 수 있습니다.

         * [스키마](/help/components/classifications/sets/manage/schema.md)에 설명된 대로 Adobe Analytics 분류 데이터를 가져올 때

           하지만 분류 데이터 가져오기에 대해 구성된 위치는 사용할 수 없습니다. 대신 아래 설명된 대로 새 대상을 추가합니다.

         * [클라우드 가져오기 및 내보내기 계정 구성](/help/components/locations/configure-import-accounts.md) 및 [클라우드 가져오기 및 내보내기 위치 구성](/help/components/locations/configure-import-locations.md)에 설명된 대로 위치 영역에서 계정 및 위치를 구성할 때

      1. [!UICONTROL **위치 선택**] 드롭다운 메뉴에서 위치를 선택합니다.

      1. [!UICONTROL **저장**] > [!UICONTROL **저장**]&#x200B;을 선택합니다.

         이제 대상이 지정한 Azure SAS 위치로 데이터를 전송하도록 구성됩니다.

   1. (조건부) 이전에 Azure SAS 계정을 추가하지 않은 경우

      1. [!UICONTROL **계정 추가**]&#x200B;를 선택하고 다음 정보를 지정합니다.

         | 필드 | 함수 |
         |---------|----------|
         | [!UICONTROL **계정 이름**] | Azure SAS 계정 이름. 이 이름은 [!UICONTROL **계정 선택**] 드롭다운 필드에 표시되며, 선택한 이름을 사용할 수 있습니다. |
         | [!UICONTROL **계정 설명**] | Azure SAS 계정에 대한 설명. 이 설명은 [!UICONTROL **계정 선택**] 드롭다운 필드에 표시되며, 선택한 이름을 사용할 수 있습니다. |
         | [!UICONTROL **애플리케이션 ID**] | 만든 Azure 애플리케이션에서 이 ID를 복사합니다. 이 정보는 Microsoft Azure의 애플리케이션 내부 **개요** 탭에 있습니다. 자세한 내용은 [Microsoft ID 플랫폼으로 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app)를 참조하십시오. |
         | [!UICONTROL **테넌트 ID**] | 만든 Azure 애플리케이션에서 이 ID를 복사합니다. 이 정보는 Microsoft Azure의 애플리케이션 내부 **개요** 탭에 있습니다. 자세한 내용은 [Microsoft ID 플랫폼으로 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app)를 참조하십시오. |
         | [!UICONTROL **키 자격 증명 모음 URI**] | <p>Azure Key Vault의 SAS URI에 대한 경로. Azure SAS를 구성하려면 Azure Key Vault를 사용하여 SAS URI를 암호로 저장해야 합니다. 자세한 내용은 [Azure Key Vault에서 암호를 설정 및 검색하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations)를 참조하십시오.</p><p>키 자격 증명 모음 URI이 생성되면<ul><li>만든 Azure 애플리케이션에 대한 권한을 부여하려면 Key Vault에서 액세스 정책을 추가합니다.<p>자세한 내용은 [Azure 키 액세스 정책을 할당하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/key-vault/general/assign-access-policy?tabs=azure-portal)를 참조하십시오.</p><p>또는</p><p>액세스 정책을 만들지 않고 직접 액세스 역할을 부여하려면 Azure 포털을 사용하여 Azure 역할을 할당하는 방법에 대한 [Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/role-based-access-control/role-assignments-portal)를 참조하십시오. 이렇게 하면 키 자격 증명 모음 URI에 액세스할 수 있는 애플리케이션 ID의 역할 할당이 추가됩니다. </p></li><li>키 자격 증명 모음 UR에 액세스하려면 `Key Vault Certificate User` 기본 제공 역할에 애플리케이션 ID가 부여되었는지 확인합니다.</br><p>자세한 내용은 [Azure 기본 제공 역할](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles)을 참조하십시오.</p></li></ul> |
         | [!UICONTROL **키 자격 증명 모음 암호 이름**] | Azure Key Vault에 암호를 추가할 때 만든 암호 이름입니다. 이 정보는 Microsoft Azure의 **Key Vault** 설정 페이지에서 만든 Key Vault에 있습니다. 자세한 내용은 [Azure Key Vault에서 암호를 설정 및 검색하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/key-vault/secrets/quick-create-portal?source=recommendations)를 참조하십시오. |
         | [!UICONTROL **암호**] | 만든 Azure 애플리케이션에서 암호를 복사합니다. 이 정보는 Microsoft Azure의 애플리케이션 내부 **인증서 및 암호** 애플리케이션 탭에 있습니다. 자세한 내용은 [Microsoft ID 플랫폼으로 애플리케이션을 등록하는 방법에 대한 Microsoft Azure 설명서](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app)를 참조하십시오. |

         {style="table-layout:auto"}

      1. [!UICONTROL **위치 추가**]&#x200B;를 선택하고 다음 정보를 지정합니다.

         | 필드 | 함수 |
         |---------|----------|
         | [!UICONTROL **이름**] | 위치의 이름. 이 이름은 [!UICONTROL **위치 선택**] 드롭다운 필드에 표시되며, 선택한 이름을 사용할 수 있습니다. |
         | [!UICONTROL **설명**] | 위치에 대한 설명. 이 설명은 [!UICONTROL **위치 선택**] 드롭다운 필드에 표시되며, 선택한 이름을 사용할 수 있습니다. |
         | [!UICONTROL **컨테이너**] | Adobe Analytics 데이터 전송 위치를 지정한 계정 내 컨테이너입니다. |
         | [!UICONTROL **접두사**] | 데이터를 입력할 컨테이너 내부 폴더입니다. 폴더 이름을 지정한 다음 이름 뒤에 백슬래시를 추가하여 폴더를 만듭니다. 예를 들어 `folder_name/`<p>Azure SAS 계정 구성 시 Key Vault 암호 이름 필드에 지정된 SAS URI 저장소에 `Write` 권한이 있는지 확인합니다. 이렇게 하면 SAS URI가 Azure 컨테이너에서 파일을 만들 수 있습니다. <p>SAS URI를 사용하여 파일을 덮어쓰려면 SAS URI 저장소에 `Delete` 권한이 있는지 확인합니다.</p><p>자세한 내용은 Azure Blob Storage 설명서에서 [Blob 스토리지 리소스](https://learn.microsoft.com/ko-kr/azure/storage/blobs/storage-blobs-introduction#blob-storage-resources) 를 참조하십시오.</p> |

         {style="table-layout:auto"}

      1. [!UICONTROL **만들기**] > [!UICONTROL **저장**]&#x200B;을 선택합니다.

         이제 대상이 지정한 Azure SAS 위치로 데이터를 전송하도록 구성됩니다.

      1. (조건부) 방금 만든 대상(계정 및 위치)을 관리해야 하는 경우 [위치 관리자](/help/components/locations/locations-manager.md)에서 사용할 수 있습니다.

   +++

   +++Google Cloud Platform

   피드를 Google Cloud Platform(GCP) 버킷으로 직접 전송할 수 있습니다. 이 대상 유형은 GCP 계정 이름과 위치(버킷) 이름만 필요합니다.

   Adobe Analytics는 교차 계정 인증을 사용하여 Adobe Analytics의 파일을 GCP 인스턴스의 지정된 위치로 업로드합니다.

   GCP 버킷을 데이터 피드의 대상으로 구성하려면 다음 작업을 수행합니다.

   1. Adobe Analytics Admin Console의 [!UICONTROL **대상**] 섹션에서 [!UICONTROL **Google Cloud Platform**]&#x200B;을 선택합니다.

      ![Google Cloud Platform 대상](assets/datafeed-destination-gcp.png)

   1. [!UICONTROL **위치 선택**]&#x200B;을 선택합니다.

      GCP 내보내기 위치 페이지가 표시됩니다.

   1. (조건부) Adobe Analytics에 Google Cloud Platform 계정(및 해당 계정의 위치)이 이미 구성된 경우, 데이터 피드 대상으로 사용할 수 있습니다.

      >[!NOTE]
      >
      >계정은 귀하가 구성했거나 귀하가 속한 조직과 공유된 경우에만 사용할 수 있습니다.

      1. [!UICONTROL **계정 선택**] 드롭다운 메뉴에서 계정을 선택합니다.

         Adobe Analytics의 다음 영역 중 하나에서 구성한 모든 클라우드 계정을 사용할 수 있습니다.

         * [스키마](/help/components/classifications/sets/manage/schema.md)에 설명된 대로 Adobe Analytics 분류 데이터를 가져올 때

           하지만 분류 데이터 가져오기에 대해 구성된 위치는 사용할 수 없습니다. 대신 아래 설명된 대로 새 대상을 추가합니다.

         * [클라우드 가져오기 및 내보내기 계정 구성](/help/components/locations/configure-import-accounts.md) 및 [클라우드 가져오기 및 내보내기 위치 구성](/help/components/locations/configure-import-locations.md)에 설명된 대로 위치 영역에서 계정 및 위치를 구성할 때

      1. [!UICONTROL **위치 선택**] 드롭다운 메뉴에서 위치를 선택합니다.

      1. [!UICONTROL **저장**] > [!UICONTROL **저장**]&#x200B;을 선택합니다.

         이제 대상이 지정한 Google Cloud Platform 위치로 데이터를 보내도록 구성됩니다.

   1. (조건부) 이전에 GCP 계정을 추가하지 않은 경우

      1. [!UICONTROL **계정 추가**]&#x200B;를 선택하고 다음 정보를 지정합니다.

         | 필드 | 함수 |
         |---------|----------|
         | [!UICONTROL **계정 이름**] | 계정 이름. 원하는 이름을 선택할 수 있습니다. |
         | [!UICONTROL **계정 설명**] | 계정에 대한 설명. |
         | [!UICONTROL **프로젝트 ID**] | Google Cloud 프로젝트 ID입니다. [프로젝트 ID 가져오기에 대한 Google Cloud 설명서](https://cloud.google.com/resource-manager/docs/creating-managing-projects#identifying_projects)를 참조하십시오. |

         {style="table-layout:auto"}

      1. [!UICONTROL **위치 추가**]&#x200B;를 선택하고 다음 정보를 지정합니다.

         | 필드 | 함수 |
         |---------|----------|
         | [!UICONTROL **주체**] | 주체는 Adobe에서 제공합니다. 이 주체에게 피드를 받을 수 있는 권한을 부여해야 합니다. |
         | [!UICONTROL **이름**] | 계정 이름. |
         | [!UICONTROL **설명**] | 계정에 대한 설명. |
         | [!UICONTROL **버킷**] | Adobe Analytics 데이터를 전송할 GCP 계정 내부 버킷입니다. <p>Adobe에서 제공하는 주체에 다음 권한 중 하나를 부여했는지 확인하십시오. (권한 부여에 대한 자세한 내용은 Google Cloud 설명서의 [버킷 수준 정책에 주체 추가](https://cloud.google.com/storage/docs/access-control/using-iam-permissions#bucket-add)를 참조하십시오.)<ul><li>`roles/storage.objectCreator`: 주체를 제한하여 GCP 계정에서만 파일을 만들려는 경우 이 권한을 사용합니다. </br>**중요:** 예약된 보고에 이 권한을 사용하는 경우 새로 예약된 각 내보내기에 고유 파일 이름을 사용해야 합니다. 그렇지 않으면 주체가 기존 파일 덮어쓰기에 액세스할 수 없기 때문에 보고서를 생성할 수 없습니다.</li><li>(권장) `roles/storage.objectUser`: 주체가 GCP 계정에서 파일을 보고, 나열하고, 업데이트하고, 삭제할 수 있는 액세스 권한이 있는 경우 이 권한을 사용합니다.</br>이 권한을 사용하면 주체는 새로 예약된 각 내보내기에 고유 파일 이름을 자동 생성하지 않고도 후속 업로드에 기존 파일을 덮어쓸 수 있습니다.</li></ul><p>귀사에서 [조직 정책 제한 사항](https://cloud.google.com/storage/docs/org-policy-constraints)을 사용하여 허용 목록에 Google Cloud Platform 계정만 허용하는 경우 다음과 같은 Adobe 소유의 Google Cloud Platform 조직 ID가 필요합니다. <ul><li>`DISPLAY_NAME`: `adobe.com`</li><li>`ID`: `178012854243`</li><li>`DIRECTORY_CUSTOMER_ID`: `C02jo8puj`</li></ul> </p> |
         | [!UICONTROL **접두사**] | 데이터를 입력할 버킷 내부 폴더입니다. 폴더 이름을 지정한 다음 이름 뒤에 백슬래시를 추가하여 폴더를 만듭니다. 예를 들어 `folder_name/` |

         {style="table-layout:auto"}

      1. [!UICONTROL **만들기**] > [!UICONTROL **저장**]&#x200B;을 선택합니다.

         이제 대상이 지정한 GCP 위치로 데이터를 전송하도록 구성됩니다.

      1. (조건부) 방금 만든 대상(계정 및 위치)을 관리해야 하는 경우 [위치 관리자](/help/components/locations/locations-manager.md)에서 사용할 수 있습니다.

   +++

1. [!UICONTROL **데이터 열 정의**] 섹션의 드롭다운 메뉴에서 최신 [!UICONTROL **모든 Adobe 열**] 템플릿을 선택한 후 다음 필드를 작성합니다.

   | 필드 | 함수 |
   |---------|----------|
   | [!UICONTROL **이스케이프 처리된 문자 제거**] | 데이터를 수집할 때 일부 문자 (예: 줄바꿈)가 문제를 초래할 수 있습니다. 피드 파일에서 이러한 문자를 제거하려면 이 확인란을 선택하십시오. |
   | [!UICONTROL **압축 포맷**] | 사용된 압축 유형. **Gzip**&#x200B;은 파일을 `.tar.gz` 포맷으로 출력합니다. **Zip**&#x200B;은 파일을 `.zip` 포맷으로 출력합니다. |
   | [!UICONTROL **패키징 유형**] | 대부분의 데이터 피드에 대해 [!UICONTROL **여러 파일**]&#x200B;을 선택합니다. 이 옵션은 데이터를 압축되지 않은 2GB 청크로 페이지를 매깁니다. [!UICONTROL **여러 파일**] 옵션을 선택하고 보고 기간의 압축되지 않은 데이터가 2GB 미만이면 하나의 파일이 전송됩니다.) **단일 파일**&#x200B;을 선택하면 `hit_data.tsv` 파일이 하나의 파일로 출력됩니다. |
   | [!UICONTROL **매니페스트**] | 피드 간격에 대한 데이터가 수집되지 않을 때 Adobe에서 [매니페스트 파일](c-df-contents/datafeeds-contents.md#feed-manifest)을 대상에 전송할지 여부를 결정합니다. **매니페스트 파일**&#x200B;을 선택하면 데이터가 수집되지 않을 때 다음과 유사한 매니페스트 파일이 수신됩니다.<p>`text`</p><p>`Datafeed-Manifest-Version: 1.0`</p><p>`Lookup-Files: 0`</p><p>`Data-Files: 0`</p><p> `Total-Records: 0`</p> |
   | [!UICONTROL **열 템플릿**] | Adobe는 다수의 데이터 피드를 만들 때 열 템플릿을 만들 것을 권장합니다. 열 템플릿을 선택하면 지정된 열이 템플릿에 자동으로 포함됩니다. Adobe도 기본적으로 여러 템플릿을 제공합니다. |
   | [!UICONTROL **사용 가능한 열**] | Adobe Analytics에서 사용 가능한 모든 데이터 열. 데이터 피드에 모든 열을 포함하려면 [!UICONTROL 모두 추가]를 클릭하십시오. |
   | [!UICONTROL **포함된 열**] | 데이터 피드에 포함할 열. 데이터 피드에 모든 열을 제거하려면 [!UICONTROL 모두 제거]를 클릭하십시오. |
   | [!UICONTROL **CSV 다운로드**] | 포함된 모든 열이 들어 있는 CSV 파일을 다운로드합니다. |

1. 오른쪽 상단에 있는 [!UICONTROL **저장**]&#x200B;을 선택합니다.

   내역 데이터 처리가 즉시 시작됩니다. 데이터 처리가 하루에 완료되면 파일이 설정한 대상으로 전송됩니다.

   데이터 피드에 액세스하는 방법과 데이터 피드의 내용을 더 잘 이해하는 방법에 대한 자세한 내용은 [데이터 피드 내용 - 개요](/help/export/analytics-data-feed/c-df-contents/datafeeds-contents.md)를 참조하십시오.

## 기존 대상

>[!IMPORTANT]
>
>이 섹션에 설명된 대상은 기존 대상으로 권장되지 않습니다. 대신 Amazon S3, Google Cloud Platform, Azure RBAC 또는 Azure SAS와 같은 데이터 피드를 만드는 경우 대상 중 하나를 사용합니다. 각 권장 대상에 대한 자세한 내용은 [데이터 피드 만들기 및 구성](#create-and-configure-a-data-feed)을 참조하십시오.


다음 정보는 각 기존 대상에 대한 구성 정보를 제공합니다.

### FTP

데이터 피드 데이터는 Adobe 또는 고객이 호스팅하는 FTP 위치로 전달될 수 있습니다. FTP 호스트, 사용자 이름 및 암호가 필요합니다. 폴더에 피드 파일을 배치하려면 경로 필드를 사용하십시오. 폴더는 이미 있어야 합니다. 지정된 경로가 존재하지 않을 경우 피드에서 오류가 발생합니다.

사용 가능한 필드가 완료되면 다음 정보를 사용합니다.

* [!UICONTROL **호스트**]: 원하는 FTP 대상 URL을 입력합니다. (예: `ftp://ftp.omniture.com`)
* [!UICONTROL **경로**]: 비워 둘 수 있습니다.
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
  >Amazon S3 버킷에 대한 각 업로드의 경우 [!DNL Analytics]는 버킷에 필요한 정책이 있는지 여부에 관계없이 버킷 소유자를 BucketOwnerFullControl ACL에 추가합니다. 자세한 내용은 “[Amazon S3 데이터 피드에 대한 BucketOwnerFullControl 설정은 무엇입니까?](df-faq.md#BucketOwnerFullControl)”를 참조하십시오.

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
