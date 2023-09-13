---
description: Data Warehouse 요청을 만드는 방법을 설명하는 단계입니다.
title: Data Warehouse 요청에 대한 보고서 대상 구성
feature: Data Warehouse
source-git-commit: 393355cd971f264da3e3e1b8736f5752fc4bdc62
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 13%

---

# Data Warehouse 요청에 대한 예약 옵션 구성

{{release-limited-testing}}

Data Warehouse 요청을 만들 때 사용할 수 있는 구성 옵션은 다양합니다. 다음 정보는 요청에 대한 예약 옵션을 구성하는 방법을 설명합니다.

요청 만들기를 시작하는 방법과 기타 중요한 구성 옵션에 대한 링크에 대한 자세한 내용은 을 참조하십시오. [Data Warehouse 요청 만들기](/help/export/data-warehouse/create-request/t-dw-create-request.md).

Data Warehouse 요청에 대한 예약 옵션을 구성하려면 다음을 수행합니다.

1. 다음을 선택하여 Adobe Analytics에서 요청 만들기 시작 **[!UICONTROL 도구]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **추가**].

   자세한 내용은 [Data Warehouse 요청 만들기](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. 새 Data Warehouse 요청 페이지에서 [!UICONTROL **예약 옵션**] 탭.

   ![보고서 대상 탭](assets/dw-scheduling-options.png) <!-- update screenshot -->

1. 다음 필드를 완료합니다. 

   | 옵션 | 함수 |
   |---------|----------|
   | 지금 보고서 보내기 | 보고서를 일회성 보고서로 보냅니다. 이 옵션을 선택하면 모든 예약 옵션이 숨겨집니다. |
   | 나중으로 예약 | 보고서 배달 예약 옵션을 제공합니다. 모든 옵션은 아래에 설명되어 있습니다. |
   | 보고 빈도 | 보고서가 배달되는 빈도입니다. <p>다음 옵션을 사용할 수 있습니다.</p><ul><li>시간별</li><p>[!UICONTROL **시간별**] 은(는) [!UICONTROL **날짜 범위**] 옵션 [!UICONTROL **일반 설정**] 탭이 다음으로 설정됨: [!UICONTROL **지난 시간**].</p><li>일별</li><li>주별</li><li>월별</li><li>연간</li></ul>  <!-- Is this valid? Was in the old docs: "To schedule Data Warehouse requests for Daily, Weekly, Monthly, or Yearly, make sure *Preset* is correctly selected" --> |
   | 월별 반복 | 보고서가 전송되는 월 사이의 간격입니다. |
   | 일 | 보고서를 전송하는 매월 날짜입니다.<p>이 옵션을 사용할 수 있는 경우 [!UICONTROL **해당 월의 주**] 및 [!UICONTROL **요일**] 옵션이 아님. 다음 항목 선택 [!UICONTROL **대체 형식**] 단추를 클릭하여 앞뒤로 전환합니다. </p> |
   | 주 | 보고서를 전송해야 하는 매월 주입니다. <p>다음 옵션을 사용할 수 있습니다.</p><ul><li>첫 번째 날</li><li>초</li><li>세 번째</li><li>네 번째</li><p>보고서는 4주 차, 심지어 5주 차 달에도 보내세요. 선택 [!UICONTROL **마지막**] 보고서를 매월 마지막 주에 보내려면</p><li>마지막</li></ul><p>이 옵션을 사용할 수 있는 경우 [!UICONTROL **날짜**] 옵션이 아님. 다음 항목 선택 [!UICONTROL **대체 형식**] 단추를 클릭하여 앞뒤로 전환합니다. </p> |
   | 요일 | 보고서를 전송해야 하는 요일입니다. <p>이 옵션을 사용할 수 있는 경우 [!UICONTROL **날짜**] 옵션이 아님. 다음 항목 선택 [!UICONTROL **대체 형식**] 단추를 클릭하여 앞뒤로 전환합니다. </p> |
   | 에 시작 | 새 일정이 시작될 날짜. |
   | 하루 중 시간 | 보고서를 전송해야 하는 시간. |
   | 게재 종료 옵션 | 예약된 게재를 종료할 시기를 선택합니다. 종료되지 않거나, 특정 발생 횟수 이후에 종료되거나, 특정 날짜에 종료되도록 선택할 수 있습니다. |

   {style="table-layout:auto"}

1. 에서 Data Warehouse 요청 구성 계속 [!UICONTROL **알림 이메일**] 탭. 자세한 내용은 [Data Warehouse 요청에 대한 알림 이메일 구성](/help/export/data-warehouse/create-request/dw-request-email.md).

