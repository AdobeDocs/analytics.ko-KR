---
description: 계산 및 고급 계산 (또는 파생) 지표는 기존의 지표에서 만들 수 있는 사용자 지정 지표입니다.
keywords: 계산된 지표;파생 지표;고급 계산된 지표
title: 계산 및 고급 계산 (파생) 지표
feature: Calculated Metrics
exl-id: 9bf8239f-cf74-4feb-85e5-d47805e90afb
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: ht
source-wordcount: '605'
ht-degree: 100%

---

# 계산 및 고급 계산 (파생) 지표

계산 및 고급 계산 (또는 파생) 지표는 기존의 지표에서 만들 수 있는 사용자 지정 지표입니다.

Adobe의 계산된 지표 도구에서는 지표를 작성하고, 관리하고, 조정하는 유연한 방법을 제공합니다. 이 도구를 사용하는 마케터, 제품 관리자 및 분석가는 [!DNL Analytics] 구현을 변경하지 않아도 데이터에 대해 질문할 수 있습니다. 각 [!DNL Analytics] 패키지에서 사용할 수 있는 사용자 지정 지표는 다음과 같습니다.

* Adobe [!DNL Analytics] Foundation: 계산된 지표
* [Adobe Analytics Select](https://www.adobe.com/kr/data-analytics-cloud/analytics/select.html): 계산된 + 고급 계산된 지표
* [Adobe Analytics Prime](https://www.adobe.com/kr/data-analytics-cloud/analytics/prime.html): 계산된 + 고급 계산된 지표
* [Adobe Analytics Ultimate](https://www.adobe.com/kr/data-analytics-cloud/analytics/ultimate.html): 계산된 + 고급 계산된 지표

다음은 계산된 지표와 고급 계산 지표 기능을 비교한 것입니다.

| Builder 옵션 | 계산된 지표 | 고급 계산 (파생) 지표 |
|---|---|---|
| [형식 유형 (십진수, 시간, 퍼센트, 통화)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md) | 예 | 예 |
| [기여도 분석 변경 (기본값, 선형, 기여도 등)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md) | 예 | 예 |
| [지표 유형 (표준, 전체)](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md) | 예 | 예 |
| 기본 연산자 (더하기, 빼기, 곱하기, 나눗셈) | 예 | 예 |
| [세그먼트 적용](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/metrics-with-segments.md) | 아니요 | 예 |
| [기본 함수 (수, 절대값, 평균 등)](/help/components/c-calcmetrics/cm-reference/cm-functions.md) | 아니요 | 예 |
| [고급 함수 (회귀, if/then, T 스코어 등)](/help/components/c-calcmetrics/cm-reference/cm-adv-functions.md) | 아니요 | 예 |

## 기능 {#section_A0A5C275B68A4D628950BBB0B1EE631F}

다음과 같은 작업을 수행할 수 있습니다.

* [!UICONTROL Analysis Workspace], [!UICONTROL Reports &amp; Analytics], [!UICONTROL Report Builder], [!UICONTROL Anomaly Detection], [!UICONTROL Contribution Analysis]에서 지표를 만들 수 있습니다.
* 구현을 변경하지 않고도 보고서 실행 시 파생된 세그먼트화된 지표를 만들 수 있습니다. 이러한 지표는 세그먼트를 기반으로 하므로 기록에서 볼 수 있습니다. 다음은 구현 불가 메트릭에 대한 비디오입니다.

   >[!VIDEO](https://video.tv.adobe.com/v/25407/?quality=12)

* 보고서 세트 간에 지표를 공유할 수 있습니다. 이것은 새로 만들어진 모든 지표가 동일한 로그인 회사에 있는 모든 보고서 세트에 적용됨을 의미합니다.
* (고급 계산 지표만 해당) 지표의 세그먼트 예를 들어 첫 번째 세션에 참여한 사람의 수로, &quot;새 방문자 수&quot;에 대한 지표를 만들 수 있습니다. 다음은 해당 주제에 대한 비디오입니다.

   >[!VIDEO](https://video.tv.adobe.com/v/25409/?quality=12)

* (고급 계산 지표만 해당) 통계 함수를 통합하여 데이터를 더욱 효율적으로 설명할 수 있습니다. 예를 들어 보고서에 있는 항목의 수를 계산하거나 각 항목에 대한 표준 편차의 수를 추가할 수 있습니다.

## 제한 사항 {#section_CB878B02451541D68A68B508D4DBD19A}

일부 [!DNL Analytics] 기능은 이벤트를 사용할 수 있지만 계산된 지표는 사용할 수 없습니다.

* Reports &amp; Analytics의 유입경로
* Analysis Workspace의 폴아웃
* [!UICONTROL Analysis Workspace의 집단 분석]
* [!UICONTROL Data Warehouse]
* [!UICONTROL 세그먼트]
* [!UICONTROL 실시간 보고서]
* [!UICONTROL 현재 데이터 보고서]
* [!DNL Analytics] for [!DNL Target]

## 도구 {#section_D65E9C067E9C45E1A50DD30F50561BB2}

다음은 [!UICONTROL 계산된 지표] 도구에 대한 간략한 개요입니다.

<table id="table_520AFE97DB514958ABE23FD3C9CE0ABD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 도구 </th> 
   <th colname="col2" class="entry"> 기능 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md"  >계산된 지표 빌더</a>에서 계산된 지표를 작성합니다. </td> 
   <td colname="col2"> 
    <ul id="ul_E6F02AB9DF204C2F9A0AC92A31594B3E"> 
     <li id="li_A4A6E716374243A190C539A3F4A41C0C">고급 할당 모델을 사용하여 계산된 지표 및 고급 계산된 지표를 생성합니다. </li> 
     <li id="li_C8C97BA4E227463E98077ABA5818FFC6">인라인 세그먼트를 지표 공식에 추가할 수 있습니다. </li> 
     <li id="li_8503D9E06A3C46569B5CDB4B90F72446">동일한 보고서에서 세그먼트들을 비교할 수 있습니다. 예를 들어 로컬 방문자와 해외 방문자를 비교할 수 있습니다. </li> 
     <li id="li_4B528FDE1F96400DBA0D3276408FF919">통계 함수를 사용할 수 있습니다. </li> 
     <li id="li_C1162B1EA6784B8189A8A87E2B0DA79A">상세한 지표 설명을 제공할 수 있습니다(수행하는 작업, 사용할 곳, 사용하지 말아야 곳을 보여줌). </li> 
     <li id="li_DEA13F5E8BF94AF1B311C467FE6E2A74">정의를 새 지표에 복사할 수 있습니다. </li> 
     <li id="li_8C21F55015D44910904202D2BF74221C">인라인 지표 미리보기를 제공할 수 있습니다. </li> 
     <li id="li_3704F66C321C477F9D4F52E068C231BD">주어진 사용자 정의 이벤트 (지표)가 상승한다면 이것이 좋은 것인지 나쁜 것인지를 가리키는 지표 극성을 설정할 수 있습니다. </li> 
     <li id="li_9D45319FA965476FB1C90DE8AA72BBD7">지표에 태그를 지정할 수 있습니다. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-manager.md"  > 계산된 지표 관리자</a> </td> 
   <td colname="col2"> 
    <ul id="ul_E4D20D5DD3904CC6A85785B5BD4C1B1E"> 
     <li id="li_E0B216BA1478406EB6212263DF71D85B">지표를 다른 사람과 공유할 수 있습니다. </li> 
     <li id="li_96EB16FAF3454211AAEF78EA5B08927F">지표를 승인 및 조정할 수 있습니다. </li> 
     <li id="li_3ADBD2428EAC4B0AA61222D87C3AF2B7">사람들이 찾을 수 있도록 지표를 정리 (태그 지정)할 수 있습니다. </li> 
     <li id="li_726F3C3390744E49BA63606FE196880E">지표를 삭제할 수 있습니다. </li> 
     <li id="li_F306BA4FA8AF4A6E987BA62634659A2F">지표의 이름을 변경할 수 있습니다. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 지표 선택기 레일 </td> 
   <td colname="col2"> <p>Reports &amp; Analytics에서 <span class="uicontrol">지표 표시</span><span class="uicontrol"> 팝업을 대체합니다</span>. </p> <p>지표를 검색하고 보고서에 추가/적용할 수 있도록 해 줍니다. 또한 <a href="/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-finding.md"  >정렬</a> 순서(옵션: 알파벳, 권장, 자주 사용하는 항목, 최근에 사용한 항목)를 변경할 수도 있습니다. 또한, 보고서 세트에 대해 필터링하여 특정 보고서 세트에서 만든 지표만 표시할 수 있습니다. </p> <p>지표 선택기에 액세스하려면 보고서 왼쪽에 있는 지표 아이콘 <img placement="inline"  src="assets/metrics_icon.png" width="30px" id="image_2C6F20B4E634486B95BACD4CA47EF991" />을 클릭합니다. 다음은 지표 선택기의 모습입니다. </p> <p><img src="assets/metrics_rail.png" width="200px" id="image_379523E9AFEC4CF08D20C42C740AA358" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/README.md"  > 계산된 지표에 대한 API</a> </td> 
   <td colname="col2"> <p>Adobe Analytics 2.0 API 세트의 일부. </p> </td> 
  </tr> 
 </tbody> 
</table>
