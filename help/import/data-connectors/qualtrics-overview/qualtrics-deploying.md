---
description: 이 통합 배포는 다음 작업이 필요한 간단한 프로세스입니다.
seo-description: 이 통합 배포는 다음 작업이 필요한 간단한 프로세스입니다.
seo-title: 통합 배포
solution: Analytics
subtopic: Qualtrics
title: 통합 배포
topic: Data connectors
uuid: 9bdc233d-63f6-456d-8c26-b5736dfdef09
translation-type: tm+mt
source-git-commit: f326b29bb73fd6e8630957c43dfd89f47b711986

---


# 통합 배포{#deploying-the-integration}

이 통합 배포는 다음 작업이 필요한 간단한 프로세스입니다.

## Adobe 통합 마법사 완료{#completing-the-adobe-integration-wizard}

통합을 활성화하려면 데이터 커넥터 인터페이스 내에서 Qualtrics 통합 마법사를 완료해야 합니다

1. 데이터 커넥터로 이동하고 Qualtrics 통합 마법사를 시작합니다.
1. 이 통합에 사용할 보고서 세트를 선택하고 이름을 제공합니다.

   다음 단계에 설명된 정보를 제공하여 통합 마법사를 완료합니다. 1.마법사 **1단계**

   | Email Address | 기본 연락처 이메일 주소입니다. |
   |---|---|
   | 설명 | (선택 사항) 이 통합 설정에 대한 설명입니다. |
   | Qualtrics 조직 ID | [Qualtrics 조직 ID 조회](../qualtrics-overview/qualtrics-org-id.md) |
   | Adobe SiteCatalyst 토큰 | [Adobe Analytics 토큰 생성](../qualtrics-overview/qualtrics-token.md) |

1. **마법사 2단계 - 변수 매핑**| Qualtrics 응답 목록| 보고서 세트에서 사용 가능한 목록 변수를 선택합니다. (보고서 세트 관리자에서 새 listVar를 활성화해야 할 수 있습니다.)  ||—|—|| Qualtrics 응답 ID| 보고서 세트에서 사용 가능한 eVar 또는 prop을 선택합니다. (보고서 세트 관리자에서 새 listVar를 활성화해야 할 수 있습니다.)  || 추적 서버|Adobe Analytics 데이터를 추적하는 데 사용하는 추적 서버(도메인) 설정을 제공합니다. Use the  tracking server if it differs from your standard tracking server setting.  `trackingServerSecure`  |
|  Qualtrics Survey Submissions  | Select an available event from your report suite (you may need to enable a new event from within the Report Suite Manager).  |

1. **Wizard Step 3: Nothing required, informational only.**

   단계 결과 1. **Wizard Step 4 - Export Settings**

   | eVar | Select up to five of your eVars to expose for exporting to Qualtrics |
   |---|---|
   | 이벤트 | Select up to five of your custom events to expose for exporting to Qualtrics |
   | Prop | Select up to five of your Props to expose for exporting to Qualtrics |
   | Access Requests | Check the box for any of the standard metrics and dimensions that you wish to export to Qualtrics. 내보내기가 제대로 작동하도록 허용하려면 `visitor_id` 이 필요합니다. |

1. **Wizard Step 5: Review configuration and then click Activate Now.******

## Enabling the Integration in Qualtrics Research Suite{#enabling-the-integration-in-qualtrics-research-suite}

After completing the integration wizard, you must activate the integration for each Qualtrics survey that you want connected.

1. Log in to the Qualtrics Research Suite.
1. On the My Surveys tab, click the Edit button for the survey that you want to integrate.********
1. Click the Advanced Options menu and select Adobe Analytics. ******** 이 옵션이 표시되지 않으면 관리자에게 필요한 권한을 요청하십시오.

   ![](assets/advanced_options.png)

1. Adobe Analytics 구성을 선택한 다음 저장을 **[!UICONTROL 클릭합니다]**. 사용할 수 있는 구성이 없는 경우 Adobe 통합 마법사를 아직 완료하지 않았을 수 있습니다.
   1. 부분 **[!UICONTROL 응답 포함]** 확인란을 사용하여 각 부분 설문 조사 화면이 완료된 후 Adobe Analytics로 데이터를 캡처할 수 있습니다. 선택하지 않으면 완료된 설문 조사에 대해서만 데이터가 전송됩니다.
   1. 타임스탬프를 **[!UICONTROL 비콘으로]** 보내기 확인란은 타임스탬프가 지정된 데이터를 수신하도록 구성된 보고서 세트와 통합할 때만 사용해야 합니다(일반적이지 않음).
   ![](assets/integration_config.png)

## 통합 확인{#verifying-the-integration}

모든 배포 단계가 완료되면 통합이 성공적으로 데이터를 전송하고 있는지 확인할 수 있습니다.

1. **통합 작업 로그**:데이터 커넥터 UI에서 Qualtrics **[!UICONTROL 통합의 지원]** 탭을 봅니다. 통합 활동 로그 **[!UICONTROL 제목]** 아래에서 가져온 성공적인 분류 데이터를 설명하는 항목이 표시됩니다.

   >[!NOTE]
   >
   >이러한 항목은 성공적으로 배포한 후 1시간 이내에 표시됩니다.

   ![](assets/verify-1.png)

1. **보고 데이터**:Qualtrics 설문 조사 보고([목록 변수] 아래)를 탐색하여 마케팅 보고 및 분석 UI로 Qualtrics **[!UICONTROL 설문 조사 보고서를 봅니다]**.

   >[!NOTE]
   >
   >통합 설문 조사가 응답을 적극적으로 수신한다고 가정할 경우 이 데이터는 성공적인 배포 후 24-48시간 이내에 나타나야 합니다.

   ![](assets/verify-2.png) ![](assets/verify-3.png)


