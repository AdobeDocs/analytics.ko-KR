---
description: 'null'
title: Advertising Analytics 개요
uuid: 00e461ff-3e17-4071-818b-93fd1e4b36f1
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Advertising Analytics 개요

Advertising Analytics를 사용하여 Adobe Analytics 내에서 Google 및 Bing 유료 검색 데이터를 나란히 볼 수 있습니다. 이전에는 모든 Google AdWords/DFA 또는 Microsoft Bing 광고 데이터를 AAC(Adobe Advertising Cloud) 또는 Google/Bing에서 확인해야 했습니다. 이제는 Adobe Analytics 내의 노출 횟수, 클릭 수, 비용, 품질 점수 및 평균 위치 데이터를 검색 엔진과 AMO ID 인스턴스(클릭 인스턴스)에서 직접 가져옵니다.

>[!NOTE] Yahoo Gemini는 2019년 3월 31일에 Microsoft Bing에 병합되었습니다. 따라서 Yahoo Gemini 광고 계정 옵션은 더 이상 사용할 수 없습니다.

Adobe Analytics에서 이러한 검색 엔진의 데이터를 함께 가져오면 강력한 분석 작업 공간을 사용하여 동일한 데이터를 분석할 수 있습니다. A new [Paid Search Performance](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-report-ad-data-an.md) template in Workspace facilitates this analysis.

![](assets/aa_aw.png)

이 통합은 다음 고객을 대상으로 합니다.

* 유료 **검색** 마케터에 대한 성과 보고서를 수집해야 하는 분석가.
* 이러한 **질문에 대한** 답변을 원하는 유료 검색 마케터:우리 사이트로 전송하고 고객이 전환하는 트래픽은 얼마입니까? 비용 효과적인 광고 캠페인은 무엇입니까?

## 전제 조건 {#section_C25E0CA3474C4EDEAEAA9A5B8AAC9299}

* Advertising Analytics is available for Adobe Analytics [Select](https://www.adobe.com/kr/data-analytics-cloud/analytics/select.html), [Prime](https://www.adobe.com/kr/data-analytics-cloud/analytics/prime.html), and [Ultimate](https://www.adobe.com/kr/data-analytics-cloud/analytics/ultimate.html) SKUs only.

* 이 기능은 Advertising Cloud가 아닌 고객과 AMO가 아닌 고객에게 제공됩니다.
* Advertising Analytics에 액세스하려면 Adobe Analytics 관리자여야 합니다. 그런 다음 관리자가 아닌 사람에게 액세스 권한을 [부여할](/help/integrate/c-advertising-analytics/overview.md#section_FCC58EB635954A32990D4E67B52B4369) 수 있습니다.
* Google/Bing 검색 데이터를 보려는 Analytics 보고서 세트는 [Experience Cloud 조직에 매핑](https://marketing.adobe.com/resources/help/ko_KR/mcloud/report-suite-mapping.html)되어 있어야 합니다.
* For any report suite where you want to view Google/Bing search data, you must [enable those report suite/s for Advertising Analytics](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-provision-rs.md) ( **[!UICONTROL Admin]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Advertising Analytics Configuration]**).

* Google 계정 ID 및 암호와 같이 Adobe Analytics와 통합하려는 검색 계정에 대한 편집 권한이 있는 사용자의 로그인 자격 증명이 필요합니다.
* Bing 광고의 경우 Bing 고객 ID도 필요합니다.
* If you use Internet Explorer 11 (or earlier), you will not be able to successfully [set up an advertising account](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-create-ad-account.md) for any of the three search engines. 다른 웹 브라우저를 대신 사용하십시오.

## Advertising Analytics 권한 {#section_FCC58EB635954A32990D4E67B52B4369}

Analytics에는 Analytics 관리자에게 자동으로 부여되는 두 가지 권한이 있습니다. 관리자는 관리자가 아닌 사람에게 이러한 권한을 부여하도록 선택할 수 있습니다.

<table id="table_86256AD8B4554F369439A8FDF2F545E1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 사용 권한 </th> 
   <th colname="col2" class="entry"> 정의 </th> 
   <th colname="col3" class="entry"> Adobe Analytics 내에서 권한 부여 </th> 
   <th colname="col4" class="entry"> Adobe Experience Cloud에 로그인한 경우 권한 부여 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Advertising Analytics 관리 </p> </td> 
   <td colname="col2"> <p>사용자가 광고 검색 계정을 설정/편집/볼 수 있도록 해줍니다. </p> </td> 
   <td colname="col3"><span class="ignoretag"><span class="uicontrol"> 관리</span> &gt; <span class="uicontrol">사용자 관리</span> &gt; <span class="uicontrol">그룹</span> &gt; <span class="uicontrol">모든 보고서 액세스 편집</span> &gt; <span class="uicontrol">Analytics 도구 사용자 지정</span> &gt; <span class="uicontrol">Advertising Analytics 관리</span></span> </td> 
   <td colname="col4"><span class="ignoretag"><span class="uicontrol"> adminconsole.adobe.com에 로그인</span> &gt; <span class="uicontrol">제품</span> &gt; <span class="uicontrol">제품 프로필</span> &gt; <span class="uicontrol">권한 탭</span> &gt; <span class="uicontrol">Analytics 도구</span> &gt; <span class="uicontrol">Advertising Analytics 관리</span></span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Advertising Analytics 구성 </p> </td> 
   <td colname="col2"> <p>사용자가 Advertising Analytics에 대해 제공되도록 보고서 세트를 구성할 수 있습니다. </p> </td> 
   <td colname="col3"><span class="ignoretag"><span class="uicontrol"> 관리</span> &gt; <span class="uicontrol">사용자 관리</span> &gt; <span class="uicontrol">그룹</span> &gt; <span class="uicontrol">모든 보고서 액세스 편집</span> &gt; <span class="uicontrol">보고서 세트 도구 사용자 지정</span> &gt; <span class="uicontrol">Advertising Analytics 구성</span></span> </td> 
   <td colname="col4"><span class="ignoretag"><span class="uicontrol"> adminconsole.adobe.com에 로그인</span> &gt; <span class="uicontrol">제품</span> &gt; <span class="uicontrol">제품 프로필</span> &gt; <span class="uicontrol">권한 탭</span> &gt; <span class="uicontrol">보고서 세트 도구</span> &gt; <span class="uicontrol">Advertising Analytics 구성</span></span> </td> 
  </tr> 
 </tbody> 
</table>

## Advertising Analytics 차원 및 지표 {#section_C0DF4A08EA9E46ADABE9E465AFC11E32}

Advertising Analytics는 분석 작업 공간, 보고 및 분석, 리포트 빌더 및 분석 보고 API에 다음 차원 및 지표를 추가합니다.

**차원**

>[!IMPORTANT]
>
>이 통합은 AMO ID 변수의 분류를 통해 새 차원 집합을 만듭니다. 이러한 새 차원은 기존 마케팅 채널 또는 캠페인 추적 변수 차원에 영향을 주거나 수정하지 않습니다. AMO ID는 방문자가 유료 검색 광고에서 사이트에 들어올 때 방문자의 프로필에 연결됩니다. 따라서 AMO 차원을 사용하여 이 통합에서 제공하는 AMO 지표와 방문자가 다운스트림으로 캡처한 데이터(방문, 방문자, 페이지 보기, 바운스 비율, 주문, 매출액, 사용자 지정 이벤트 등)를 모두 분류할 수 있습니다. 다른 온사이트 지표에 대해 보고할 때 다른 차원으로 분류할 수도 있습니다.
>
>이러한 지표에 대한 분류는 매일 업데이트됩니다. 이와 같이 검색 엔진에서 메타 데이터를 변경하는 경우 분류가 업데이트되는 다음 날까지 변경 사항이 반영되지 않을 수 있습니다.

| 분류(차원) 이름 | 정의 |
|--- |--- |
| 키워드 일치 유형(AMO 파섹) | 키워드 일치 유형입니다.광고 유형에 일치 유형이 없는 경우 일반적으로 값은 광범위, 구문, 정확 또는 값이 없습니다. |
| 광고 플랫폼(AMO ID) | 검색 엔진 이름입니다. 값에는 Google AdWords 또는 Microsoft Bing 광고가 포함될 수 있습니다. |
| 계정(AMO 파섹) | 추적 중인 검색 엔진 계정의 이름입니다. |
| 캠페인(AMO 파섹) | 검색 엔진 계정의 캠페인 이름. |
| 광고 그룹(AMO 파섹) | 검색 엔진 캠페인의 광고 그룹 이름입니다. |
| 광고(AMO ID) | 광고에 사용되는 광고 제목 + 광고 설명입니다. |
| 키워드(AMO 파섹 | 검색 엔진 계정의 키워드 값 |
| 일치 유형(AMO 파섹) | 키워드에 지정된 키워드 일치 유형입니다. 광고 유형에 일치 유형이 없는 경우 일반적으로 값은 확장, 구문, 일치 또는 값 없음 중 하나입니다. |
| 광고 유형(AMO 파섹) | 제공되는 광고의 유형이며, 일반적으로 &quot;텍스트 광고&quot;입니다. |
| 광고 제목(AMO 파섹) | 광고에 사용된 제목 개체. |
| 광고 설명(AMO 파섹) | 광고에 사용된 광고 설명 개체. |
| 광고 표시 URL(AMO ID) | 광고에 사용된 광고 표시 URL 개체. |
| 광고 대상 URL(AMO ID) | 광고에 지정된 랜딩 페이지 URL 또는 최종 URL. |
| 네트워크(AMO ID) | 광고가 제공되는 네트워크입니다. Advertising Analytics의 경우 이 값은 항상 “Search”입니다. |
| 배치(AMO ID) | 관리되는 배치 웹 사이트(컨텐츠 네트워크의 경우)입니다. 관리되는 배치만 이 차원을 사용합니다. |
| 제품 타겟(AMO 파섹) | PLA 광고에 사용되는 제품 타겟의 이름(구입한 실제 제품의 이름이 아님). |
| 최적화(AMO 파섹) | 광고 분석에서는 사용하지 않습니다. Adobe Advertising Cloud 고객만 사용합니다. |
| 장치(AMO ID) | 오늘은 사용되지 않습니다.지정된 대상 장치 유형(예: 모바일, 데스크탑)의 광고(실제 방문자의 장치가 아님)에 대한 향후 제품 개선을 위한 자리 표시자 |

**지표**

>[!IMPORTANT]
>
>Advertising Analytics에서 제공한 지표(아래 나열됨)는 검색 엔진에서 제공하는 요약 수준의 데이터입니다. Analytics 방문자 프로필에 연결되지 않습니다. AMO ID 변수 및 관련 분류 차원에만 연결됩니다. 따라서 AMO ID 차원을 기반으로 하는 차원/세그먼트가 아닌 다른 차원/세그먼트에서 보고해서는 안 됩니다. 이렇게 하면 Analytics에서 데이터에 대해 0을 표시합니다. 다른 지표와 함께 계산된 지표에 포함할 수 있지만, 이러한 계산된 지표는 AMO ID 차원으로만 분류되어야 합니다.
>
>이러한 지표는 일별로 소싱된 데이터이므로 현재 날짜에 대한 데이터가 없습니다. 또한 일보다 작은 세부기간으로 보고해서는 안 됩니다.
>
>랜딩 페이지(예: 클릭스루)에서 AMO ID가 설정될 때 설정되는 AMO ID 인스턴스 지표가 있습니다. 이 지표는 랜딩 페이지 히트와 함께 실시간으로 캡처되며, 랜딩 페이지에서도 다른 차원이 설정된 분류에도 사용할 수 있습니다.

| 지표 이름 | 정의 |
|--- |--- |
| AMO 노출 횟수 | 검색 엔진에서 보고한 광고 노출 수입니다. |
| AMO 클릭 수 | 검색 엔진에서 보고한 광고에 대한 클릭 수입니다. |
| AMO 비용 | 검색 엔진에서 보고한 각 키워드/광고에 대한 비용입니다. |
| 평균 Pos | 검색 엔진에서 보고한 광고의 평균 위치를 반영하는 계산된 지표. |
| 평균 품질 점수입니다 | 검색 엔진에서 보고한 평균 품질 점수를 반영하는 계산된 지표. |
