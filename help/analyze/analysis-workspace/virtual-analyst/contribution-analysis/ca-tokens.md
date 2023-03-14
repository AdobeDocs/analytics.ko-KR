---
description: 기여도 분석을 사용하여 데이터의 통계 이상 및 상관관계를 식별합니다.
title: 기여도 분석 개요
role: User, Admin
exl-id: 86fc8696-90a8-4626-b1c7-6413d3f8a648
source-git-commit: 9b50e77b3998753d45a25799dbed6094b048c118
workflow-type: tm+mt
source-wordcount: '1162'
ht-degree: 100%

---

# 기여도 분석 개요

기여도 분석은 사용자 데이터 안에서 숨겨진 패턴을 발견하여 통계적 예외 항목을 설명하고 전체 수렴된 대상 세그먼트에서 선택된 지표에 대해 예상치 못한 고객 작업, 범위를 벗어나는 값, 급증 또는 급감 뒤의 상관관계를 식별합니다.

>[!VIDEO](https://video.tv.adobe.com/v/25443/?quality=12)

어떤 일이 발생했습니다. 왜일까요? 예외 항목 탐지 보고서는 비정상적인 주문 급증을 보여 주고 사용자는 그 이유를 알고 싶어 합니다. 기준에서 벗어나 무슨 일이 생겼습니까? 어떤 캠페인 또는 참조에 누가 반응하고 있습니까? 어떤 것이 입소문이 났습니까? 이러한 예외 항목에 기여한 특정 요인은 무엇입니까? 그리고 가장 중요한 것으로 손꼽는다면 고객에 대한 중요한 정보를 어떻게 캡처하고 이 활동을 어떻게 반복할 수 있습니까? (또는 지표의 급감 또는 부정적 지표의 증가가 발생했다면 앞으로는 어떻게 이것을 피할 수 있습니까?)

기여도 분석은 예외 항목이 왜 일어났는지 대답하기 위해 사용자 데이터를 즉시 평가하도록 도와줍니다. 기존에는 몇 주가 걸리던 예외 항목에 대한 기여도를 몇 초 만에 분류하여 대상 세그먼트에 대한 패턴을 제공하고 고객 상호 작용에 대한 내러티브를 만드는 데 도움을 줍니다. 기여도 분석을 전략적으로 사용하여 의미 있는 연결을 식별하고 캡처하여 새 대상 세그먼트를 만들거나 경고를 트리거하는 영역 밖의 활동 또는 부정 활동을 식별하는 데 전략적으로 사용합니다.

[예외 항목 탐지](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md)는 선택된 지표와 선택된 대상 세그먼트에 따른 데이터 급증과 극단적 통계 급감을 식별합니다. 교육 기간에 따른 내역 기본값을 설정한 다음 특정 이벤트와 관련 있는 극단적 오프셋을 그래프에 표시합니다. 기여도 분석으로 평가될 통계적으로 관련 있는 데이터 포인트를 캡처하여 양성 주문 지표의 급격한 증가 또는 음성 바운스 지표의 증가 또는 둘 다의 증가를 보고할 수 있습니다. 통계적 예외 항목이 식별되면 기여도 분석을 통해 모든 예외 항목 데이터 포인트에서 관련 있는 마케팅 및 캠페인 변수를 드릴다운하고 평가할 수 있습니다. 고급 알고리즘 및 머신 러닝 프로세스를 실행하여 유의한 급증 또는 급감에 기여한 연관성을 평가합니다. 그런 다음 이러한 계산이 어떤 일이 왜 발생했으며 어떻게 대응해야 하는지에 대한 답을 찾는 데 유익한 다양한 관점을 제공하도록 설계된 상호 작용 시각화에 표시됩니다.

기여도 분석은 관련된 지표를 캡처하고 대상 상호 작용과 고객의 관심 트렌드에 대한 전반적인 이유를 제공하는 숨은 포인트를 식별하여 예외 항목이 발생한 이유와 그에 대응하는 방법을 설명하는 내러티브를 만드는 데 유용합니다. 때때로 예외 항목은 카약 2,000개를 잘못 주문하는 것처럼 쉽게 보고 고칠 수 있습니다. 때때로 특정 대상 캠페인에 대해서만 반응하는 지역에서 전체 기간에 떠오르는 트렌드를 식별하는 것처럼 복잡합니다. 여러 차원 및 그 연관성에 대해 전체 지표에서 기여도 항목을 짜 맞추면 대상 상호 작용에 대한 전반적인 아이디어를 얻게 되며 예외 항목 데이터 포인트에 대한 컨텍스트를 제공하는 데 유용합니다.

다음은 몇 가지 사용 사례입니다.

* 제품 수요 변화를 모니터링하여 재마케팅 가능성을 식별합니다.
* 특정 대상의 관심에 반응하여 고객 경험을 증진합니다.
* 범위를 벗어나는 보고서로 신속하게 부정 주문을 식별합니다.
* 높은 사용량 및 다운로드를 식별하여 산업 스파이로부터 사용자 자신을 보호합니다.
* 누락된 JavaScript 태그 보고와 같이 작업을 모니터링합니다.

예외 항목의 포괄적 분석 후 총 발생 횟수 및 항목의 기여 값 비율별로 순서가 정해진 상위 항목에 대해 기여도 요약이 생성됩니다. 정규화된 기여도 점수를 통해 다른 유의한 차원과 쉽게 비교, 대조 및 연결할 수 있습니다.

## 기여도 분석 토큰 - 개요 {#section_3EF8D2BBCE6E4C309D753BCF04A453D0}

>[!IMPORTANT]
>
>기여도 분석이 Reports &amp; Analytics 기능 집합에서 제거되었으며, 현재 Analysis Workspace을 통해서만 사용할 수 있습니다.

기여도 분석 권한이 있는 모든 고객은 Analysis Workspace에서 매달 제한된 횟수만큼 전체 기여도 분석을 실행할 수 있습니다. 여기에는 기여도 분석을 전혀 받지 않는 포인트 제품 (SiteCatalyst 15) 고객, Analytics Foundation 고객 및 Analytics Select 고객은 **제외됩니다**.

회사마다 실행 횟수는 회사에서 구입한 Adobe Analytics 제품을 기준으로 하여 부여된 월별 토큰에 의해 제한됩니다. 여기에는 토큰 오용을 방지하기 위해 기여도 분석 액세스를 제한하는 기능이 포함됩니다.

## FAQ {#section_11D0431AD2014B96AB9561CA66A367CE}

| 질문 | 답변 |
| --- | --- |
| Adobe에서 토큰을 도입한 이유는 무엇입니까? | Contribution Analysis는 Adobe Analytics에서 가장 공감스러운 기능 중 하나입니다. 일부 Analytics 제품의 경우 3차원이 아닌 매월 &quot;전체&quot; 실행 횟수가 적어 무제한 전체 기여도 분석을 통해 어떤 효과가 있는지 알 수 있습니다. |
| 기여도 분석에서 토큰은 어떻게 작동합니까? 기존 기여도 분석을 사용하여 프로젝트를 로드하는 데 토큰 비용이 듭니까? 또는 새로운 기여도 분석을 실행할 때만 토큰 비용이 필요합니까? | 각 로그인 회사 (각 사용자가 아님)는 한 달에 특정 수의 토큰을 얻으므로, Analysis Workspace에서 &quot;전체&quot; 기여도 분석을 실행할 수 있습니다.  새 기여도 분석을 생성할 때마다 한 개의 토큰 비용을 지불합니다. 사전 실행된 기여도 분석을 사용하여 프로젝트 로드 시 토큰 비용이 들지 않습니다. |
| Reports &amp; Analytics의 기여도 분석에 토큰을 적용합니까? | 아니요. 기여도 분석은 2018년 4월 현재 Reports &amp; Analytics 릴리스에 더 이상 제공되지 않습니다. |
| 회사에 토큰이 없고 추가 기여도 분석을 실행하려는 경우 어떻게 해야 합니까? | 다른 Adobe Analytics 제품으로 업그레이드 할 수 있습니다 (예: Standard (매달 2개 토큰)에서 Ultimate (매달 20개 토큰)로). 더 많은 토큰을 구입할 수 없으며, 기존 패키징 프레임 워크 내에서 업그레이드 해야 합니다. |
| 기여도 분석에 대한 액세스를 어떻게 제한합니까? | 기본적으로 관리자만 기여도 분석을 실행할 권한이 있습니다. 그러나 관리자는 [Adobe Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/home.html)에서 권한 그룹을 생성하여 다른 사용자에게 액세스 권한을 부여할 수 있습니다. 합법적인 이유가 있고 액세스 권한을 남용하지 않을 것으로 신뢰할 수 있는 사용자에게만 기여도 분석을 사용할 수 있는 권한을 부여해야 합니다. 이 권한은 [!UICONTROL 보고서 세트 도구] 하의 [!UICONTROL 기여도 분석]이라고 합니다. [추가 정보](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/permissions/report-suite-tools.html) |
| 한 달에 얼마나 많은 토큰을 받을 수 있고, 얼마나 많은 토큰을 현재 달에 사용했는지 어떻게 알 수 있습니까? | [!UICONTROL 관리자] > [!UICONTROL 모든 관리자] >[!UICONTROL 회사 설정 홈] >[!UICONTROL 기능 액세스 수준 보기]로 이동합니다. 아래를 참조하십시오<ul><li>기여도 분석: 월간 사용 토큰 수</li><li>기여도 분석: 이번 달에 사용된 사용 토큰 수</li></ul> |

## 예외 항목 탐지 및 기여도 분석 권한 {#section_9278D58F21A840AA9B1ED1BD07A1EF0A}

다음은 Analysis Workspace에서 예외 항목 탐지 및 기여도 분석에 대한 상세 권한 목록입니다.

>[!IMPORTANT]
>
>예외 항목 탐지 및 기여도 분석은 Reports &amp; Analytics 기능에서 제거되었으며 이제 Analysis Workspace를 통해서만 사용할 수 있습니다. Adobe Analytics Select 및 Adobe Analytics Foundation 고객은 Workspace의 &quot;일별 세부 기간&quot; 예외 항목 탐지에만 액세스할 수 있습니다.

<table id="table_5C9B7E4AE82640B5A913519E576889B5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Adobe Analytics 권한 </th> 
   <th colname="col2" class="entry"> 예외 항목 탐지 </th> 
   <th colname="col3" class="entry"> 기여도 분석 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Foundation </p> </td> 
   <td colname="col2"> <p>일별 세부 기간만 </p> </td> 
   <td colname="col3" colsep="1"> <p>토큰 없음 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="https://www.adobe.com/kr/data-analytics-cloud/analytics/select.html?promoid=B4XQ3X7G&amp;mv=other"  > 선택 </a> </p> </td> 
   <td colname="col2"> <p>일별 세부 기간만 </p> </td> 
   <td colname="col3"> <p>토큰 없음 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="https://www.adobe.com/kr/data-analytics-cloud/analytics/prime.html?promoid=91BF51TR&amp;mv=other"  > 프라임 </a> </p> </td> 
   <td colname="col2"> <p>예 </p> </td> 
   <td colname="col3"> <p>월별 10개 토큰 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="https://www.adobe.com/kr/data-analytics-cloud/analytics/ultimate.html?promoid=8N4B5F1V&amp;mv=other"  > 최적</a> </p> </td> 
   <td colname="col2"> <p>예 </p> </td> 
   <td colname="col3"> <p>월별 20개 토큰 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>+Predictive Workbench </p> </td> 
   <td colname="col2"> <p>예 </p> </td> 
   <td colname="col3"> <p>무제한 토큰 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>표준 </p> 
    <ul id="ul_73D52020793B44868C9CE0F90893075D"> 
     <li id="li_21EE0871C87E43C8B781219B2BA0FA74">Adobe Analytics 코어 </li> 
     <li id="li_AB3593200F33439BAEE8FEB13CAE57F4">Adobe Analytics OD </li> 
     <li id="li_2B7D625519BC4A4CB598C95F15D3029B">Adobe Analytics MA </li> 
    </ul> </td> 
   <td colname="col2"> <p>예 </p> </td> 
   <td colname="col3"> <p>월별 2개 토큰 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Premium (360, 속성) </p> </td> 
   <td colname="col2"> <p>예 </p> </td> 
   <td colname="col3"> <p>월별 2개 토큰 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Premium (완료, <a href="https://www.adobe.com/kr/data-analytics-cloud/analytics/predictive-intelligence.html"  >예측 인텔리전스</a>) </p> </td> 
   <td colname="col2"> <p>예 </p> </td> 
   <td colname="col3"> <p>무제한 토큰 </p> </td> 
  </tr> 
 </tbody> 
</table>
