---
description: Analysis Workspace에서 사용자 정의 날짜 범위를 만든 후 시간 구성 요소로 저장합니다.
keywords: Analysis Workspace
title: 사용자 정의 날짜 범위 만들기
feature: Date Ranges
role: User, Admin
exl-id: 586bb120-3f20-452c-9867-0b93d2e794bc
source-git-commit: 1281bdc569c9ebc5d8daa151b19dc21710633eab
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 100%

---

# 사용자 정의 날짜 범위 만들기

Analysis Workspace에서 사용자 정의 날짜 범위를 만들고 시간 구성 요소로 저장할 수 있습니다.

프로젝트에 기존 날짜 범위를 추가하는 방법에 대한 자세한 내용은 [캘린더 및 날짜 범위 개요](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md)를 참조하십시오.

사용자 정의 날짜 범위 만드는 방법:

1. Adobe Analytics에서 **[!UICONTROL 구성 요소]** > **[!UICONTROL 날짜 범위]**&#x200B;를 선택합니다.

   ![날짜 범위 페이지](assets/date-ranges.png)

1. [!UICONTROL **새 날짜 범위 만들기**]&#x200B;를 선택합니다.

1. 날짜 범위 빌더에서 다음 정보를 지정합니다.

   | 옵션 | 설명 |
   |---------|----------|
   | [!UICONTROL **제목**] | Analysis Workspace에서 사용자가 날짜 범위를 선택할 때 표시되는 날짜 범위의 제목. |
   | [!UICONTROL **설명**] | 날짜 범위에 대한 설명. |
   | [!UICONTROL **태그**] | 날짜 범위에 적용하려는 태그. |
   | [!UICONTROL **날짜 범위**] | 사용자 정의 날짜 범위를 선택할 수 있습니다. 기본적으로 지난 30일이 선택됩니다. |
   | [!UICONTROL **사전 설정**] | [!UICONTROL **어제**], [!UICONTROL **지난 7일**], [!UICONTROL **지난 30일**] 등 미리 설정된 날짜 범위 목록에서 선택할 수 있습니다. |
   | [!UICONTROL **시작 시간**] | 날짜 범위가 시작되는 시간. |
   | [!UICONTROL **종료 시간**] | 날짜 범위가 종료되는 시간. |
   | [!UICONTROL **순환 날짜 사용**] | 순환 날짜를 사용하면 보고서를 실행한 때를 기반으로 설정된 기간에 대해 앞 또는 뒤는 보는 동적 보고서를 생성할 수 있습니다. 예를 들어 &quot;지난달&quot;에 수행한 모든 주문에 대해 보고하려 하고 (생성일 필드를 기반으로 한), 12월에 해당 보고서를 실행한 경우, 11월에 수행한 주문이 표시됩니다. 동일한 보고서를 1월에 실행한 경우에는 12월에 수행한 주문이 표시됩니다.<ul><li>**[!UICONTROL 날짜 미리보기]**: 롤링 캘린더가 포함하는 기간을 가리킵니다.</li><li>**[!UICONTROL 시작]**: 오늘, 이번 주, 이번 달, 이번 분기, 올해 중에서 선택할 수 있습니다.</li><li>**[!UICONTROL 끝]**: 오늘, 이번 주, 이번 달, 이번 분기, 올해 중에서 선택할 수 있습니다.</li></ul><br>기본적으로 선택되어 있습니다. |

1. [!UICONTROL **저장**]&#x200B;을 선택합니다.

## 예: “2개월 전”에 대한 날짜 범위 {#section_C4109C57CB444BB2A79CC8082BD67294}

다음 사용자 정의 날짜 범위는 방향 변경을 보여 주는 요약 변경 사항 시각화가 있는 “2개월 전”에 대한 날짜 범위를 보여 줍니다.

![](assets/date-range-two-months-ago.png)

사용자 정의 날짜 범위는 프로젝트의 [!UICONTROL 날짜 범위] 구성 요소 패널의 맨 위에 표시됩니다.

![](assets/date-range-panel-two-months-ago.png)

비교를 위해 [지난 달] 사전 설정을 사용하는 사용자 정의 월별 롤링 날짜 범위와 함께 이 사용자 정의 날짜 범위를 열로 드래그할 수 있습니다. 요약 변경 사항 시각화를 추가하고, 각 열에서 합계를 선택하여 방향 변경 사항을 표시합니다.

![](assets/date-range-two-months-table.png)

## 예: 7일 순환 날짜 범위 사용 {#section_7EF63B2E9FF54D2E9144C4F76956A8DD}

1주일 전에 끝나는 7일 순환 기간을 지정하는 날짜 범위를 만들 수 있습니다.

![](assets/create_date_range.png)

*`rolling daily`* 사용.

* 시작 설정은 *`current day minus 6 days`*.

* 끝 설정은 *`current day minus 7 days`*.

이 날짜 범위는 임의의 자유 형식 테이블로 드래그하는 구성 요소일 수 있습니다.
