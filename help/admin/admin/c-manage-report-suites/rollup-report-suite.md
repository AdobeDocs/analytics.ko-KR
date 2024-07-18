---
description: 글로벌 보고서 세트의 설명
title: 글로벌 보고서 세트
feature: Report Suite Settings
exl-id: 97bdc9bd-2212-436b-b3b4-ec518624f9e6
role: Admin
source-git-commit: 938795c7378cb1f0537ff84eddeab3feddf8d073
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 100%

---

# 글로벌 보고서 세트

글로벌 보고서 세트는 조직이 소유하는 모든 도메인 및 앱에서 데이터를 수집합니다. 모든 이미지 요청을 단일 보고서 세트로 보내려면 구현이 필요합니다.

대부분의 경우 글로벌 보고서 세트를 구현하는 것이 좋습니다. 글로벌 보고서 세트 구현의 이점은 “[글로벌 보고서 세트 고려 사항](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/global-rs.html?lang=ko-KR)”을 참조하십시오.

*다중 세트 태그 지정* 및 *가상 보고서 세트* 접근 방식을 사용하여 회사의 글로벌 보고서 세트 데이터 하위 집합을 다양한 최종 사용자에게 제공할 수 있습니다.

* **다중 세트 태그 지정**: 다중 세트 태그 지정을 사용하면 글로벌 보고서 세트뿐만 아니라 개별 하위 보고서 세트에도 이미지 요청을 보낼 수 있습니다. 글로벌 보고서 데이터는 모든 보고서 세트에서 중복 제거됩니다.

  예를 들어 모든 데이터를 하나의 글로벌 보고서 세트에 수집할 수도 있지만 브랜드, 지역 또는 다른 차별화 요소를 기반으로 보조 보고서 세트를 설정할 수도 있습니다. 그러면 회사의 여러 팀이 자신과 관련된 보고서 세트의 데이터에 집중할 수 있습니다.

  다중 세트 태그 지정을 사용하려면 하위 보고서 세트와 하위 보고서 세트의 모든 데이터를 포함하는 글로벌 보고서 세트를 구현하십시오. 웹 페이지 및 앱의 추적 코드에는 글로벌 보고서 세트의 RSID(보고서 세트 ID)와 해당 하위 보고서 세트의 RSID가 포함됩니다.<!-- Wording/be more specific? And include any links? -->

  이미지 요청의 각 보고서 세트에 대해 별도의 서버 호출이 수행됩니다. 하위 보고서 세트에 대한 호출은 보조 호출입니다.

* **가상 보고서 세트**: [가상 보고서 세트](/help/components/vrs/vrs-about.md)는 글로벌 보고서 세트에서 수집된 지정된 세그먼트에 대한 쿼리이며 지정된 사용자 그룹에서 사용할 수 있습니다. 가상 보고서 세트를 사용하면 다중 세트 태그 지정을 사용하지 않고 다양한 최종 사용자에 대한 보고서 요소를 선별할 수 있으므로 보조 서버 호출을 피할 수 있습니다.

  가상 보고서 세트를 사용하려면 글로벌 보고서 세트를 구현한 다음 데이터를 구문 분석하여 특정 세그먼트가 적용되고 특정 그룹 권한이 있는 가상 보고서 세트를 만드십시오. 가상 보고서 세트 관리자([!UICONTROL 구성 요소] > [!UICONTROL 가상 보고서 세트])에서 가상 보고서 세트를 만들 수 있습니다. 자세한 내용은 “[가상 보고서 세트 워크플로](/help/components/vrs/c-workflow-vrs/vrs-workflow.md)”를 참조하십시오.

다중 세트 태그 지정 대신 가상 보고서 세트를 사용하는 것이 모범 사례인 경우가 많지만 가상 보고서 세트에는 몇 가지 제한 사항이 있습니다. 귀하의 비즈니스 요구에 가장 적합한 보고서 세트 접근 방식을 결정하려면 “[가상 보고서 세트 및 다중 세트 태그 지정 고려 사항](/help/components/vrs/vrs-considerations.md)”를 참조하십시오. 가상 보고서 세트와 다중 세트 태그 지정에 대한 자세한 비교는 “[가상 보고서 세트 vs. 다중 세트 태그 지정](/help/components/vrs/vrs-about.md#section_317E4D21CCD74BC38166D2F57D214F78)”을 참조하십시오.

<!---## Rollup reports

>[!NOTE]
>
>[!DNL Reports & Analytics] is the only tool that supported rollup reports. Reports & Analytics was end-of-lifed on January 17, 2024.

Limitations of Rollup Reports {#limitations-rollups}

* Rollups provide total data, but they do not report individual values in reports. For example, eVar1 values are not included, but their aggregate total can be.
* Data is not deduplicated when the rollup combines data across report suites.
* Rollups run nightly at midnight.
* When you add a report suite to an existing rollup, historical data is not included in the rollup.
* All child report suites must have data in them for a rollup to function. If new report suites are included in a rollup, make sure to send at least one page view to each of those report suites.
* Rollup report suites can include a maximum of 40 child report suites.
* Rollup report suites can include a maximum of 100 events.
* Data contained in rollup report suites does not support breakdowns or segments.
* The Pages report is replaced with the Most Popular Sites report, which reports on metrics at the child-suite level.

## Comparison of Global Report Suite and Rollup Report  Features

**Secondary server calls**: Rollups do not incur any additional server calls beyond what a single report suite collects. If your organization uses multi-suite tagging, secondary server calls are made for each additional report suite included in an image request.

>[!TIP]
>
>If you use only a global report suite with [virtual report suites](/help/components/vrs/vrs-considerations.md), no secondary server calls are needed.

**Implementation changes**: Rollups do not require any implementation changes, while global report suites require you to include the global report suite ID in your implementation.

**Duplication**: Global report suites deduplicate unique visitors, while rollups do not. For example, if a user visits three of your domains in the same day, rollups would count three daily unique visitors. Global report suites would record one unique visitor.

**Time frame**: Rollups are only processed at midnight each night, while global report suites report data with standard latency.

**Breadth**: Rollups have no way to communicate between report suites. Global report suites can attribute credit to conversion variables between report suites and provide pathing across report suites.

**Historical data**: Rollups can aggregate historical data, while global report suites only report data from the point they were implemented.

**Reports**: Global report suites provide data on all dimensions; rollups provide aggregate data on only high-level reports.

**Supported products**: Rollups could only be used in Reports & Analytics. They are not supported in Analysis Workspace, or Data Warehouse. Global report suites can be used across all products.

**Number of aggregated report suites**: Rollups only support a maximum of 40 child report suites. Global report suites can be implemented on any number of domains or apps that you own.--->
