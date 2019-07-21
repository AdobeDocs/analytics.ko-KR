---
description: 계산 및 고급 계산(또는 파생) 지표는 기존의 지표에서 만들 수 있는 사용자 지정 지표입니다.
keywords: 계산된 지표; 파생된 지표; 고급 계산된 지표
seo-description: 계산 및 고급 계산(또는 파생) 지표는 기존의 지표에서 만들 수 있는 사용자 지정 지표입니다.
seo-title: 계산 및 고급 계산(파생) 지표
title: 계산 및 고급 계산(파생) 지표
uuid: 2553 C 115-B 15 A -4109-8 DE 2-733 DBC 1 EEB 9 E
translation-type: tm+mt
source-git-commit: fb27d500a725a540e632952295aa2ea3a3a21fb6

---


# 계산 및 고급 계산(파생) 지표

계산 및 고급 계산(또는 파생) 지표는 기존의 지표에서 만들 수 있는 사용자 지정 지표입니다.

>[!IMPORTANT]
>
>In July 2018, Adobe introduced [Attribution IQ](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/attribution.html), which revised the way allocation models in calculated metrics are evaluated. 이 변경의 일부로, 기본이 아닌 할당 모델을 사용하는 계산된 지표는 개선된 새로운 속성 모델로 마이그레이션되었습니다.
>
>* «마케팅 채널 마지막 터치» 및 «마케팅 채널 첫 번째 터치» 할당 모델이 각각 새로운 «마지막 터치» 및 «첫 번째 터치» 기여도 모델로 마이그레이션되었습니다 (참고: «마케팅 채널» 는 더 이상 사용되지 않으며 계산된 지표에 나타나는 두 개의 할당 모델만 있습니다.
>* 선형 할당이 계산되는 방식을 수정했습니다. 고객이 선형 할당 모델에 계산된 지표를 사용하는 경우 수정된 새로운 속성 모델을 반영하도록 보고서가 약간 변경될 수 있습니다. This change to calculated metrics is reflected in [!UICONTROL Analysis Workspace], [!UICONTROL Reports &amp; Analytics], the Reporting API, Report Builder, and Ad Hoc Analysis. 자세한 내용은 [2018년 7월 19일부터 선형 할당이 작동하는 방식](../../components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md#section_EDBB2E14A6C248C5A79C0913C02D7CA1)을 참조하십시오.


Adobe의 계산된 지표 도구에서는 지표를 작성하고, 관리하고, 조정하는 유연한 방법을 제공합니다. They allow you as marketers, product managers and analysts to ask questions of the data without having to change your [!DNL Analytics] implementation. The custom metrics available in each [!DNL Analytics] package are:

* Adobe [!DNL Analytics] Foundation: Calculated
* [Adobe Analytics Select](https://www.adobe.com/data-analytics-cloud/analytics/select.html): 계산됨 + 고급 계산됨
* [Adobe Analytics Prime](https://www.adobe.com/data-analytics-cloud/analytics/prime.html): 계산된 + 고급 계산된 지표
* [Adobe Analytics Ultimate](https://www.adobe.com/data-analytics-cloud/analytics/ultimate.html): 계산된 + 고급 계산된 지표

다음은 계산된 지표와 고급 계산 지표 기능을 비교한 것입니다.

| Builder 옵션 | 계산된 지표 | 고급 계산(파생) 지표 |
|---|---|---|
| [형식 유형(십진수, 시간, 퍼센트, 통화)](../../components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md#concept_5EC82A91EB9C44FC870326C85F9D0B18) | 예 | 예 |
| [속성 변경(기본값, 선형, 기여도 등)](../../components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md#concept_B7A1FCFEFA9D4C4883208ACE8C9C8E5E) | 예 | 예 |
| [지표 유형(표준, 전체)](../../components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md#concept_B7A1FCFEFA9D4C4883208ACE8C9C8E5E) | 예 | 예 |
| 기본 연산자(더하기, 빼기, 곱하기, 나눗셈) | 예 | 예 |
| [세그먼트 적용](../../components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/metrics-with-segments.md#concept_21C77BD86E7E45E79AF030D8ED54DB3E) | 아니요 | 예 |
| [기본 함수(수, 절대값, 평균 등)](../../components/c-calcmetrics/cm-reference/cm-functions.md#concept_E3022D5EEEE145B69A23438BAF7016B2) | 아니요 | 예 |
| [고급 함수(회귀, if/then, T 스코어 등)](../../components/c-calcmetrics/cm-reference/cm-adv-functions.md#concept_A5FB9127D70F4E1AA02D1ACBF4F54174) | 아니요 | 예 |

## 기능 {#section_A0A5C275B68A4D628950BBB0B1EE631F}

You can

* [!UICONTROL 분석 작업 공간], [!UICONTROL 보고 및 분석], [!UICONTROL 애드혹 분석], [!UICONTROL 리포트 빌더], [!UICONTROL 예외 항목 탐지]및 [!UICONTROL 기여도 분석에 대한 지표를 만듭니다].
* [구현을 변경하지 않고도](https://youtu.be/CuQTm9RaUpY) 보고서 실행 시 파생된 세그먼트화된 지표를 만들 수 있습니다. 이러한 지표는 세그먼트를 기반으로 하므로 기록에서 볼 수 있습니다.
* 보고서 세트 간에 지표를 공유할 수 있습니다. 이것은 새로 만들어진 모든 지표가 동일한 로그인 회사에 있는 모든 보고서 세트에 적용됨을 의미합니다.
* (고급 계산 지표만 해당) 지표의 세그먼트 예를 들어 이번이 첫 번째 세션인 사람의 수로, "새 방문자 수"에 대한 지표를 만들 수 있습니다.
* (고급 계산 지표만 해당) 통계 함수를 통합하여 데이터를 더욱 효율적으로 설명할 수 있습니다. 예를 들어, 보고서에 있는 항목의 수를 계산하거나 각 항목에 대한 표준 편차의 수를 추가할 수 있습니다.
* Utilize metrics created in [!UICONTROL Ad Hoc Analysis] in the other [!DNL Analytics] tools and vice versa.

   >[!NOTE]
   >
   >애드혹 분석에서 지표를 계속 만들 수 있습니다. 이제 이 분석의 계산된 지표 빌더 사용자 인터페이스는 새 지표 빌더와 비슷합니다.

## 제한 {#section_CB878B02451541D68A68B508D4DBD19A}

Some [!DNL Analytics] features let you use events but not calculated metrics:

* Reports &amp; Analytics의 유입경로
* Analysis Workspace의 폴아웃
* [!UICONTROL Analysis Workspace의 집단 분석]
* [!UICONTROL Data Warehouse]
* [!UICONTROL 세그먼트]
* [!UICONTROL 실시간 보고서]
* [!UICONTROL 현재 데이터 보고서]
* [!DNL Analytics] for [!DNL Target]

## 도구 {#section_D65E9C067E9C45E1A50DD30F50561BB2}

[!UICONTROL 다음은 계산된 지표] 도구에 대한 간단한 개요입니다.

<table id="table_520AFE97DB514958ABE23FD3C9CE0ABD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 도구 </th> 
   <th colname="col2" class="entry"> 기능 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="../../components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md#concept_5EC82A91EB9C44FC870326C85F9D0B18" format="dita" scope="local">계산된 지표 빌더</a>에서 계산된 지표를 작성합니다. </td> 
   <td colname="col2"> 
    <ul id="ul_E6F02AB9DF204C2F9A0AC92A31594B3E"> 
     <li id="li_A4A6E716374243A190C539A3F4A41C0C">고급 할당 모델을 사용하여 계산된 지표 및 고급 계산된 지표를 생성합니다. </li> 
     <li id="li_C8C97BA4E227463E98077ABA5818FFC6">인라인 세그먼트를 지표 공식에 추가할 수 있습니다. </li> 
     <li id="li_8503D9E06A3C46569B5CDB4B90F72446">동일한 보고서에서 세그먼트들을 비교할 수 있습니다. 예를 들어 로컬 방문자와 해외 방문자를 비교할 수 있습니다.  </li> 
     <li id="li_4B528FDE1F96400DBA0D3276408FF919">통계 함수를 사용할 수 있습니다. </li> 
     <li id="li_C1162B1EA6784B8189A8A87E2B0DA79A">상세한 지표 설명을 제공할 수 있습니다(수행하는 작업, 사용할 곳, 사용하지 말아야 곳을 보여줌). </li> 
     <li id="li_DEA13F5E8BF94AF1B311C467FE6E2A74">정의를 새 지표에 복사할 수 있습니다. </li> 
     <li id="li_8C21F55015D44910904202D2BF74221C">인라인 지표 미리 보기를 제공할 수 있습니다. </li> 
     <li id="li_3704F66C321C477F9D4F52E068C231BD">주어진 사용자 지정 이벤트(지표)가 상승한다면 이것이 좋은 것인지 나쁜 것인지를 가리키는 지표 극성을 설정할 수 있습니다. </li> 
     <li id="li_9D45319FA965476FB1C90DE8AA72BBD7">지표에 태그를 지정할 수 있습니다. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="../../components/c-calcmetrics/c-workflow/cm-workflow/cm-manager.md#concept_BA6815CB06D842D5825766396B691653" format="dita" scope="local"> 계산된 지표 관리자</a> </td> 
   <td colname="col2"> 
    <ul id="ul_E4D20D5DD3904CC6A85785B5BD4C1B1E"> 
     <li id="li_E0B216BA1478406EB6212263DF71D85B">지표를 다른 사람과 공유할 수 있습니다. </li> 
     <li id="li_96EB16FAF3454211AAEF78EA5B08927F">지표를 승인 및 조정할 수 있습니다. </li> 
     <li id="li_3ADBD2428EAC4B0AA61222D87C3AF2B7">사람들이 찾을 수 있도록 지표를 정리(태그 지정)할 수 있습니다. </li> 
     <li id="li_726F3C3390744E49BA63606FE196880E">지표를 삭제할 수 있습니다. </li> 
     <li id="li_F306BA4FA8AF4A6E987BA62634659A2F">지표의 이름을 변경할 수 있습니다. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 지표 선택기 레일 </td> 
   <td colname="col2"> <p>Replaces the <span class="uicontrol"> Show Metrics</span> popup in [!UICONTROL Reports &amp; Analytics]. </p> <p>지표를 검색하고 보고서에 추가/적용할 수 있도록 해줍니다.   <a href="../../components/c-calcmetrics/c-workflow/cm-workflow/cm-finding.md#concept_A09845053A934CB7B755391D76E76C08" format="dita" scope="local">정렬</a> 순서(옵션: 알파벳, 권장, 자주 사용하는 항목, 최근에 사용한 항목)를 변경할 수도 있습니다. 또한, 보고서 세트에 대해 필터링하여 특정 보고서 세트에서 만든 지표만 표시할 수 있습니다. </p> <p>지표 선택기에 액세스하려면 보고서 왼쪽에 있는 지표 아이콘 <img placement="inline"  src="assets/metrics_icon.png" width="30px" id="image_2C6F20B4E634486B95BACD4CA47EF991" />을 클릭합니다. 다음은 지표 선택기의 모습입니다. </p> <p><img placement="break" align="center"  src="assets/metrics_rail.png" width="200px" id="image_379523E9AFEC4CF08D20C42C740AA358" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/README.md" format="https" scope="external"> 계산된 지표에 대한 API</a> </td> 
   <td colname="col2"> <p>Adobe Analytics 2.0 API 세트의 일부입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

