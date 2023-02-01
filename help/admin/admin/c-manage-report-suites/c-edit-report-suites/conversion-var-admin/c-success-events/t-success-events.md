---
description: 성공 이벤트를 구성하는 방법을 설명하는 단계입니다.
title: 성공 이벤트 구성
feature: Event
exl-id: 0e9a6d8f-2ce7-4551-885d-bd77ff131da0
source-git-commit: 3f5834bb8a6460acacc806839a6d9ae45b2e7afd
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 89%

---

# 성공 이벤트 구성

성공 이벤트를 구성하는 방법을 설명하는 단계입니다.

1. **[!UICONTROL Analytics]** > **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]**&#x200B;를 클릭합니다.
1. 보고서 세트 선택.
1. **[!UICONTROL 설정 편집]** > **[!UICONTROL 변환]** > **[!UICONTROL 성공 이벤트]**&#x200B;를 클릭합니다.

   ![단계 결과](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/assets/success_event_page.png)

1. **[!UICONTROL 이름]** 열에서 각 항목 옆의 확인란을 선택하여 편집을 활성화한 다음 원하는 이름을 지정합니다.
1. **[!UICONTROL 유형]** 열에서 각 항목 옆의 확인란을 선택하여 드롭다운 목록을 활성화하고 원하는 유형을 선택합니다.

   >[!NOTE]
   >
   >이벤트 유형을 변경하기 전에 [이벤트 유형 변경](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/event-type.md)을 참조하십시오.

   이 요소에 대한 자세한 내용은 [성공 이벤트 페이지 - 설명](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/success-event.md)을 참조하십시오.

1. **[!UICONTROL 극성]** 열에서 이 지표에 대한 증가 트렌드가 좋은 것인지 아니면 나쁜 것인지를 지정합니다.
1. **[!UICONTROL 가시성]** 열에서 표준(내장된) 지표, 사용자 지정 이벤트, 내장 이벤트를 메뉴, 지표 선택기, 계산된 지표 빌더, 세그먼트 빌더에서 숨길 수 있습니다.

   이 설정은 해당 지표 또는 이벤트에 대한 데이터 수집에는 영향을 주지 않습니다. 다음과 같이 사용자 인터페이스의 가시성에만 영향을 줍니다.


   | 설정 | 표시되는 위치 | 표시되지 않는 위치 |
   |---------|----------|---------|
   | [!UICONTROL **어디에서나 볼 수 있습니다.**] | <ul><li>Reports &amp; Analytics(메뉴 및 지표 선택기)</li><li>Analysis Workspace</li><li>세그먼트 빌더</li><li>계산된 지표 빌더에서 계산된 지표를 작성합니다.</li></ul> | 해당 없음 |
   | [!UICONTROL **빌더**] | <ul><li>세그먼트 빌더</li><li>계산된 지표 빌더에서 계산된 지표를 작성합니다.</li></ul> | <ul><li>Reports &amp; Analytics(메뉴 및 지표 선택기)</li><li>Analysis Workspace</li></ul> |
   | [!UICONTROL **어디에나 숨겨져 있습니다.**] | 해당 없음 | <ul><li>Reports &amp; Analytics(메뉴 및 지표 선택기)</li><li>Analysis Workspace</li><li>세그먼트 빌더</li><li>계산된 지표 빌더에서 계산된 지표를 작성합니다.</li></ul> |

1. 설명을 제공합니다.
1. 이벤트를 항상 기록할 것인지 여부를 확인합니다.
1. 기여도 지표를 활성화 또는 비활성화합니다.

   >[!NOTE]
   >
   >최대 100개의 사용자 지정 이벤트에 대한 기여도를 활성화할 수 있습니다. 그 외에도 [계산된 지표](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/participation-metric.md) 빌더에서 기여도 지표를 만들 수 있습니다.

1. **[!UICONTROL 저장을 클릭합니다]**.
