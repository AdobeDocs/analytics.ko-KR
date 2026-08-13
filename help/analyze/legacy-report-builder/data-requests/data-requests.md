---
description: Report Builder에서 요청을 만드는 첫 번째 단계입니다.
title: 데이터 요청 - 요청 마법사 1단계
feature: Report Builder
role: User, Admin
exl-id: 698662a8-8b6b-4338-a315-b41cf6a9424e
TQID: https://experienceleague.adobe.com/87MzdxBePRZKBttF3P6XhuDq5hR6XpEWaLdrYDMu-5Y
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2: id: ac8a38fa-dec3-4581-8f64-178fde9f64e8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 401
ht-degree: 59%

---

# 데이터 요청 - 요청 마법사 1단계

{{legacy-arb}}

요청 마법사 1단계 양식에서는 보고서 세트, 보고서 유형, 세그먼트를 선택하고 날짜를 구성합니다.

![요청 마법사: 1단계 양식을 보여 주는 스크린샷](assets/rw1_overview.png)

1. **[!UICONTROL 보고서 세트]**: 로그인 자격 증명에 따라 사용할 수 있는 보고서 세트 목록입니다. [보고서 세트 선택](/help/analyze/legacy-report-builder/data-requests/selecting-report-suites/t-select-report-suites.md)을 참조하세요.

1. **범위 선택기**: Excel의 셀에서 보고서 세트 ID를 선택할 수 있습니다. [보고서 세트 선택](/help/analyze/legacy-report-builder/data-requests/selecting-report-suites/t-select-report-suites.md)을 참조하세요.

1. **세그먼트**: 는 데이터의 사용자 정의 하위 세트이거나 작성한 규칙으로 필터링된 데이터입니다. 세그먼트는 히트 수, 방문 횟수 및 방문자 수를 기반으로 합니다. 세그먼트에 대한 자세한 내용은 [분석 세그멘테이션 안내서](/help/components/segmentation/seg-home.md)를 참조하십시오.

   예를 들어 [!UICONTROL 페이지 보고서]를 실행한 다음 최초 방문 세그먼트를 적용할 수 있습니다.

1. **게시 목록 재정의 허용**: 게시 목록은 Reports &amp; Analytics의 기능으로, [서비스 종료](https://new.express.adobe.com/webpage/WFCyq7w8kijmB?)되었습니다.

1. **보고서 유형**: 데이터 요청에서 실행할 기본 보고서를 지정합니다. 요청당 하나의 보고서를 실행하며 해당 보고서에는 일대다 차원과 일대다 지표가 있을 수 있습니다. 보고서 유형에 대한 지표 및 차원은 [!UICONTROL 요청 마법사; 2단계] 인터페이스에 표시됩니다. [보고서 유형 선택](/help/analyze/legacy-report-builder/data-requests/c-report-types/select-report-types.md)을 참조하세요.

1. **날짜 범위**: 요청이 다루는 시간 범위를 정의합니다. 사전 설정, 고정 및 순환과 같은 여러 유형의 요청 기간을 사용할 수 있습니다. 최대 기간 수는 366개입니다. 셀에서 지정된 날짜 범위를 선택할 수도 있고, 날짜 범위를 나중에 사용할 수 있도록 템플릿으로 저장할 수도 있습니다.  [보고서 날짜 구성](/help/analyze/legacy-report-builder/data-requests/configuring-report-dates/custom-calendar.md)을 참조하십시오.

1. **세부 기간 적용**: 보고서에 포함된 시간 기반 세부 사항의 수준을 지정합니다. [세부 기간](/help/analyze/legacy-report-builder/data-requests/configuring-report-dates/granularity.md)을 참조하십시오.

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
