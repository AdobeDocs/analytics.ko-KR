---
description: Report Builder에서 요청을 만드는 첫 번째 단계입니다.
title: 데이터 요청 - 요청 마법사 1단계
feature: Report Builder
role: User, Admin
exl-id: 698662a8-8b6b-4338-a315-b41cf6a9424e
source-git-commit: d5d4d1c9274bba8c3a40ee8fe86da311c1d1220b
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 100%

---

# 데이터 요청 - 요청 마법사 1단계

요청 마법사 1단계 양식에서는 보고서 세트, 보고서 유형, 세그먼트를 선택하고 날짜를 구성합니다.

![](assets/rw1_overview.png)

1. **[!UICONTROL 보고서 세트]**: 로그인 자격 증명을 기반으로 사용할 수 있는 보고서 세트 목록. See [보고서 세트 선택](/help/analyze/report-builder/data-requests/selecting-report-suites/t-select-report-suites.md).

1. **범위 선택기**: Excel의 셀에서 보고서 세트 ID를 선택할 수 있습니다. 자세한 내용은 [보고서 세트 선택](/help/analyze/report-builder/data-requests/selecting-report-suites/t-select-report-suites.md).

1. **세그먼트**: 는 데이터의 사용자 정의 하위 세트이거나 작성한 규칙으로 필터링된 데이터입니다. 세그먼트는 히트 수, 방문 횟수 및 방문자 수를 기반으로 합니다. 세그먼트에 대한 자세한 내용은 [Analytics 세그멘테이션 안내서](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html)를 참조하십시오.

   예를 들어 [!UICONTROL 페이지 보고서]를 실행한 다음 최초 방문 세그먼트를 적용할 수 있습니다.

1. **보고서 유형**: 데이터 요청에서 실행할 기본 보고서를 지정합니다. 요청당 하나의 보고서를 실행하며 이 보고서는 일 대 다 차원 및 일 대 다 지표를 가질 수 있습니다. 보고서 유형에 대한 지표 및 차원은 [!UICONTROL 요청 마법사: 2단계] 인터페이스에 표시됩니다. 자세한 내용은 [보고서 유형을 선택](/help/analyze/report-builder/data-requests/c-report-types/select-report-types.md)합니다.

1. **날짜 범위**: 요청이 적용되는 시간 범위를 정의합니다. 사전 설정, 고정 및 롤링과 같이 몇 가지 유형의 요청 기간을 사용할 수 있습니다. 기간의 최대 개수는 366개입니다. 셀에서 지정된 날짜 범위를 선택할 수도 있고, 날짜 범위를 나중에 사용할 수 있도록 템플릿으로 저장할 수도 있습니다. [보고서 날짜 구성](/help/analyze/report-builder/data-requests/configuring-report-dates/custom-calendar.md)을 참조하십시오.

1. **세부기간 적용**: 보고서에 포함된 시간 기반 세부 사항의 수준을 지정합니다. [세부기간](/help/analyze/report-builder/data-requests/configuring-report-dates/granularity.md)을 참조하십시오.

## 문제 해결

특히 모니터 설정 간을 이동하는 사용자의 경우 때로 요청 마법사가 화면 밖으로 나타나는 경우가 있습니다. 예를 들어 직장에서 도킹 스테이션을 사용하고 집에서 노트북 화면을 사용하는 경우입니다. 요청 마법사가 이미 열려 있는 동안 &#39;만들기&#39;를 다시 클릭하면 다음 오류가 표시됩니다.

&quot;새 프로세스를 시작하기 전에 먼저 요청 마법사 프로세스를 완료해야 합니다.&quot;

요청 마법사를 다시 화면으로 이동하면 이 문제가 해결됩니다.

1. Microsoft Excel을 열고 Report Builder에 로그인합니다.
2. [!UICONTROL 만들기]를 클릭하면 요청 마법사가 화면 밖에서 열립니다.
3. 누르기 `[Alt]` + `[Space]`.
4. 누르기 `[M]`.
5. 아무 화살표 키나 누릅니다.
6. 마우스를 움직입니다. 그러면 요청 마법사가 커서에 연결됩니다.
7. 마우스를 클릭하여 요청 마법사를 화면에 표시합니다.
