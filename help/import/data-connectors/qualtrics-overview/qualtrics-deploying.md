---
description: 이 통합 배포는 다음 작업이 필요한 간단한 프로세스입니다.
subtopic: Qualtrics
title: 통합 배포
topic: Data connectors
uuid: 9bdc233d-63f6-456d-8c26-b5736dfdef09
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# 통합 배포{#deploying-the-integration}

이 통합 배포는 다음 작업이 필요한 간단한 프로세스입니다.

## Adobe 통합 마법사 완료{#completing-the-adobe-integration-wizard}

통합을 활성화하려면 Data Connectors 인터페이스 내에서 Qualtrics 통합 마법사를 완료해야 합니다.

1. Data Connectors로 이동하고 Qualtrics 통합 마법사를 시작합니다.
1. 이 통합에 사용할 보고서 세트를 선택하고 이름을 제공합니다.

   다음 단계에 설명된 정보를 제공하여 통합 마법사를 완료합니다. 1. 마법사 **1단계**

   | 이메일 주소 | 기본 연락처 이메일 주소입니다. |
   |---|---|
   | 설명 | (선택 사항) 이 통합 설정에 대한 설명입니다. |
   | Qualtrics 조직 ID | [Qualtrics 조직 ID 조회](../qualtrics-overview/qualtrics-org-id.md) |
   | Adobe SiteCatalyst 토큰 | [Qualtrics Adobe Analytics 토큰 생성](../qualtrics-overview/qualtrics-token.md) |

1. **마법사 2단계 - 변수 매핑**|  Qualtrics 응답 목록  | 보고서 세트에서 사용 가능한 목록 변수를 선택합니다. (보고서 세트 관리자에서 새 listVar를 활성화해야 할 수 있습니다.)  |
|---|---|
|  Qualtrics 응답 ID  | 보고서 세트에서 사용 가능한 eVar 또는 prop을 선택합니다 (보고서 세트 관리자에서 새 listVar를 활성화해야 할 수 있습니다.)  |
|  추적 서버  |Adobe Analytics 데이터를 추적하는 데 사용하는 추적 서버(도메인) 설정을 제공합니다. 표준 추적 서버 설정과 다른 경우 `trackingServerSecure` 추적 서버를 사용합니다.  |
|  Qualtrics 설문 조사 제출  | 보고서 세트에서 사용 가능한 이벤트를 선택합니다(보고서 세트 관리자 내에서 새 이벤트를 활성화해야 할 수 있습니다).  |

1. **마법사 3단계**: 필요한 것이 없으며 정보 제공용입니다.

   단계 결과 1. **마법사 4단계 - 내보내기 설정**

   | eVar | Qualtrics로 내보내기 위해 노출할 eVar 중 최대 5개를 선택 |
   |---|---|
   | 이벤트 | Qualtrics로 내보내기 위해 노출할 사용자 지정 이벤트 중 최대 5개를 선택 |
   | Prop | Qualtrics로 내보내기 위해 노출할 Prop 중 최대 5개를 선택 |
   | 액세스 요청 | Qualtrics로 내보내려는 표준 지표 및 차원에 대한 확인란을 선택합니다. 내보내기가 제대로 작동하게 하려면 `visitor_id`이 필요합니다. |

1. **마법사 5단계**: 구성을 검토하고 **[!UICONTROL 지금 활성화]**&#x200B;를 클릭합니다.

## Qualtrics Research Suite의 통합 활성화{#enabling-the-integration-in-qualtrics-research-suite}

통합 마법사를 완료한 후 연결하려는 각 Qualtrics 설문 조사에 대한 통합을 활성화해야 합니다.

1. Qualtrics Research Suite에 로그인합니다.
1. **[!UICONTROL 내 설문 조사]** 탭에서 통합하려는 설문 조사의 **[!UICONTROL 편집]** 단추를 클릭합니다.
1. **[!UICONTROL 고급 옵션]** 메뉴를 클릭하고 **[!UICONTROL Adobe Analytics]**&#x200B;를 선택합니다. (이 옵션이 표시되지 않으면 관리자에게 필요한 권한을 확보하는 방법에 대해 문의하십시오.)

   ![](assets/advanced_options.png)

1. Adobe Analytics 구성을 선택한 다음 **[!UICONTROL 저장]**&#x200B;을 클릭합니다. 사용할 수 있는 구성이 없다면 Adobe 통합 마법사를 아직 완료하지 않았을 수 있습니다.
   1. **[!UICONTROL 부분 응답 포함]** 확인란을 사용하여 각 부분 설문 조사 화면이 완료된 후 Adobe Analytics로 데이터를 캡처할 것임을 나타낼 수 있습니다. 선택하지 않으면 완료된 설문 조사에 대해서만 데이터가 전송됩니다.
   1. **[!UICONTROL 타임스탬프를 비콘으로 보내기]** 확인란은 타임스탬프가 지정된 데이터를 수신하도록 구성된 보고서 세트와 통합할 때만 사용해야 합니다(일반적이지 않음).
   ![](assets/integration_config.png)

## 통합 확인{#verifying-the-integration}

모든 배포 단계가 완료되면 통합이 성공적으로 데이터를 전송하고 있는지 확인할 수 있습니다.

1. **통합 활동 로그**: Data Connectors UI의 Qualtrics 통합에서 **[!UICONTROL 지원]** 탭을 확인합니다. **[!UICONTROL 통합 활동 로그]** 제목 아래에 가져온 성공적인 분류 데이터를 설명하는 항목이 표시됩니다.

   >[!NOTE]
   >
   >이러한 항목은 성공적으로 배포한 후 1시간 이내에 표시됩니다.

   ![](assets/verify-1.png)

1. **보고 데이터**: Qualtrics 설문 조사 보고를 탐색하여 Marketing Reports and Analytics UI에서 Qualtrics 설문 조사 보고서를 봅니다(**[!UICONTROL 목록 변수]** 아래).

   >[!NOTE]
   >
   >통합 설문 조사가 응답을 적극적으로 수신한다고 가정할 경우 이 데이터는 성공적인 배포 후 24-48시간 이내에 나타나야 합니다.

   ![](assets/verify-2.png) ![](assets/verify-3.png)


