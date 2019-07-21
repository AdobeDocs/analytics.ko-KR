---
description: 'null'
seo-description: 'null'
seo-title: 속성 IQ FAQ
title: 속성 IQ FAQ
uuid: 90961172-869 D -4 ED 3-ABA 5-52374 E 53 B 603
translation-type: tm+mt
source-git-commit: ab2cda6d10bfeee13262581578bcdb4746112296

---


# 속성 IQ FAQ

<table id="table_590341C2F0DA4511ADEFDC1DB49CD248"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 질문 </th> 
   <th colname="col2" class="entry"> 답변 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Q: 새로운 속성 모델을 사용할 때 '없음' 라인 항목이 간혹 예상보다 더 많은 크레딧을 받는 이유는 무엇입니까?</b> </p> </td> 
   <td colname="col2"> <p>A: <a href="../../../analyze/analysis-workspace/attribution-iq/attribution.md#section_BC71DA030E45487AA3C3F6ED247A3C4A" format="dita" scope="local">여기</a>에 설명된 대로 선택한 보고 기간 때문일 수 있습니다. 보고 기간이 월의 첫 번째 날에 시작하고 방문자(보고 기간) 전환 확인을 사용하는 경우 가장 자주 발생합니다. 추가 속성 전환 확인을 캡처하고 '없음' 라인 항목을 줄이려면 보고 기간에서 더 긴 시간 범위를 포함하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>질문: 속성 모델을 사용할 때 보고서에 표시되는 보고 기간을 벗어난 날짜가 표시되는 경우가 있습니다. 왜 그런 것입니까?</b> </p> </td> 
   <td colname="col2"> <p>답변: 이러한 추가 날짜는 <a href="../../../analyze/analysis-workspace/attribution-iq/attribution.md" format="dita" scope="local">여기</a>에 설명된 방문자 전환 확인 기간의 아티팩트입니다 . <a href="https://helpx.adobe.com/analytics/kb/data-appearing-outside-reporting-window.html" format="html" scope="external">보고 기간을 벗어나 표시되는 데이터</a> 문서에서 현재 이런 현상이 발생하는 원인에 대해 설명합니다. Adobe Analytics는 향후 릴리스에서 이러한 추가 행을 필터링합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>질문: 내 속성 모델과 함께 사용자 지정 전환 확인 기간을 사용할 수 있습니까?</b> </p> </td> 
   <td colname="col2"> <p>A: Currently, attribution models rely on either a visitor or visit lookback window - but either of these lookback windows are adjustable by either changing the reporting date range (for visitor lookback) or by using a custom visit definition as part of Virtual Report Suites and <a href="https://marketing.adobe.com/resources/help/en_US/reference/vrs-mobile-visit-processing.html" format="html" scope="external"> Context-Aware Sessions </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>질문: '방문' 속성 전환 확인과 '방문자' 속성 전환 확인은 각각 언제 사용해야 합니까?</b> </p> </td> 
   <td colname="col2"> <p>대답: 속성 전환 확인의 선택은 사용 케이스에 따라 다릅니다. 일반적으로 고려 주기가 긴 전환인 경우(단일 방문보다 오래 걸리는 항목) 방문자 전환 확인을 사용하기를 권장합니다. 또는 고려 주기를 보다 정확히 반영하는 더 긴 방문으로 VRS를 생성하는 것이 좋습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>질문: 데이터 피드 또는 Data Warehouse에서 속성 모델을 사용할 수 있습니까?</b> </p> </td> 
   <td colname="col2"> <p>A: 아니요. 속성 모델은 <a href="https://marketing.adobe.com/resources/help/en_US/reference/vrs-report-time-processing.html" format="html" scope="external">보고서 처리 시간</a>을 사용하는 보고 시간에 계산되므로 데이터 피드 또는 Data Warehouse에 반영할 수 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>질문: 보고서 처리 시간이 활성화된 가상 보고서 세트를 사용하는 경우에만 속성 모델을 사용할 수 있습니까?</b> </p> </td> 
   <td colname="col2"> <p>답변: 아니요. 속성 모델이 백엔드에서 <a href="https://marketing.adobe.com/resources/help/en_US/reference/vrs-report-time-processing.html" format="html" scope="external">보고서 처리 시간</a>을 활용하는 동안 당사는 편의를 위해 VRS 및 기본 보고서 세트를 모두 사용할 수 있도록 하였습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>질문: Analysis Workspace의 속성 IQ에서 데이터 기반 또는 알고리즘 속성 모델을 지원합니까?</b> </p> </td> 
   <td colname="col2"> <p>답변: 아직 Analysis Workspace에서는 사용할 수 없지만 적극적으로 방법을 찾고 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>질문: 속성 IQ에서 지원되지 않는 차원이나 지표가 있습니까?</b> </p> </td> 
   <td colname="col2"> <p>A: 기여도 IQ는 모든 차원에서 지원됩니다.</p> 
    <p><u>지원되지 않는 지표</u>(주로 의미가 없는 경우): </p> 
    <ul id="ul_B12A1291DEEF41FDBAD110C4A9265234"> 
     <li id="li_245571C5377C45ADBAE6F735B91FCD1F"> 고유 방문자 수 </li> 
     <li id="li_000CA7680A0745D9860CA7D5F62288D4">방문 횟수 </li> 
     <li id="li_53CAD3ECAE54451BBB0750FB62AF1243">발생 </li> 
     <li id="li_C589008CA92E4C69866E85EEEC88EF90"> 페이지 보기 횟수 </li> 
     <li id="li_ACF8D24E3AC746E280DB0F71D4B772A3">A4T 지표 </li> 
     <li id="li_78BFE0A4F8024301A218C0415537F632">체류 시간 지표 </li> 
     <li id="li_29774EEFE9A04759B7929EA35AA9BEAD">바운스 수 </li> 
     <li id="li_B163C6F24240465F85AB5C9792F0F013">바운스 비율 </li> 
     <li id="li_CF065E227A634C77BC2C48C2A6EC849A">시작 </li> 
     <li id="li_ED962C5063B047F185EFC58EB43C661F">종료 </li> 
     <li id="li_029F6D09433F48A38303E5C96E77480B">페이지를 찾을 수 없음 </li> 
     <li id="li_8410AF29208247B5B3E49F72208913BA">검색 결과 </li> 
     <li id="li_8421F1D5F58148D98B1AB5C04FCCA9CF">단일 페이지 방문 횟수 </li> 
     <li id="li_50D4EA0FF2E6438C8DD2A1B2EAD7B9D7">단일 액세스 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>질문: 속성 IQ가 Data Workbench의 속성과 어떻게 다릅니까?</b> </p> </td> 
   <td colname="col2"> <p>답변: Data Workbench는 점진적으로 다음을 제공합니다. </p> 
    <ul id="ul_5A8C979CDCD04FF5B9625C84B2678CC7"> 
     <li id="li_115DC58D4BDF40A4A0036E76F6E64158">광고 노출 횟수 및 판매 시점과 같은 보다 많은 방문자 수준의 데이터 소스를 파악할 수 있는 기능. </li> 
     <li id="li_C31891A4D5594D93AF97340F6D3A2E3E">Algorithmic(<a href="https://marketing.adobe.com/resources/help/en_US/insight/client/c_attrib_algorithmic.html" format="html" scope="external">최상</a>) 모델링. 속성 IQ에는 규칙 기반 모델만 포함됩니다. </li> 
     <li id="li_749D5D11B34E40E9AB53908A38979CAA"><a href="https://marketing.adobe.com/resources/help/en_US/insight/client/c_lat_tbls.html" format="html" scope="external">지연 테이블</a>과 같은 추가 시각화 요소 . </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Q: 속성 IQ가 데이터 소스에서 작동합니까?</b> </p> </td> 
   <td colname="col2"> <p>A: 현재 속성 IQ는 요약 수준 데이터 소스가 아닌 데이터 소스에서 작동합니다. </p> <p> 요약 수준 데이터 소스는 Analytics 방문자 ID와 연결되지 않으므로 고급 속성이 불가능합니다. 또한 거래 ID 데이터 소스는 <a href="https://marketing.adobe.com/resources/help/en_US/reference/vrs-report-time-processing.html" format="html" scope="external">보고서-시간 처리</a>가 활성화된 가상 보고서 세트에서 사용되지 않는 한 지원됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Q: 속성 IQ가 <a href="https://marketing.adobe.com/resources/help/en_US/analytics/advertising/overview.html" format="html" scope="external">Advertising Analytics</a> 통합에서 작동합니까?</b> </p> </td> 
   <td colname="col2"> <p>A: 노출 수, 비용, 클릭 수, 평균 위치 및 평균 품질 점수를 포함하는 통합 지표는 요약 수준의 데이터 소스이므로 속성 IQ와 호환되지 않습니다. 그러나 메타데이터 차원(예: 일치 유형 및 키워드)은 표준 Analytics 이벤트 또는 지표와 함께 사용할 때 속성에서 작동합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

