---
description: 분류란 Analytics 변수 데이터를 카테고리별로 분류하여 보고서를 생성할 때 여러 다른 방법으로 데이터를 표시하는 방법입니다.
subtopic: Classifications
title: 분류 정보
topic: Admin tools
uuid: abc1a1be-8e37-4b7e-81fd-3e99ac27fc6a
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 분류 정보

분류란 Analytics 변수 데이터를 카테고리별로 분류하여 보고서를 생성할 때 여러 다른 방법으로 데이터를 표시하는 방법입니다.

[분석 분류](https://video.tv.adobe.com/v/16853/?captions=kor)의 비디오 개요

**[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > *`<Traffic or Conversion>`*

분류할 때 변수와 해당 변수와 관련된 메타데이터 간의 관계를 설정하는 것입니다. 분류는 캠페인에서 가장 자주 사용됩니다. 변수(eVar, prop 및 이벤트) 정보를 사용하여 수집된 데이터는 변수에서 수집된 값에 메타데이터를 적용하여 롤업할 수 있습니다.

![단계 정보](assets/sub_class_create.png)

분류하면, 키 변수를 사용하여 생성할 수 있는 모든 보고서를 연관된 속성을 사용하여 생성할 수도 있습니다. 예를 들어 제품 이름, 색상, 크기, 설명 및 SKU와 같은 추가 제품 속성을 [!UICONTROL Product IDs] 사용하여 분류할 수 있습니다. 추가 속성을 사용하여 보고 및 분석 데이터를 늘리면 보다 심층적이고 복잡한 보고 기회를 제공할 수 있습니다.

>[!IMPORTANT]
>
>숫자 2와 활성화된 날짜 분류를 가져오는 기능이 코드 베이스에서 제거되었습니다. 이 변경 사항은 2019년 6월 유지 관리 릴리스에서 적용됩니다. 가져온 파일에 숫자 또는 활성화된 날짜 열이 있는 경우 해당 셀은 자동으로 무시되며, 해당 파일의 다른 모든 데이터는 정상적으로 가져와집니다. 기존 분류는 여전히 표준 분류 워크플로우를 통해 내보낼 수 있으며, 보고에서 계속 사용할 수 있습니다.

>[!NOTE] Adobe는 2018년 5월 10일, Analytics 유지 관리 릴리스에서 날짜 사용 및 숫자 분류 기능에 대한 제한을 시작했습니다. 이러한 분류 유형은 관리자 및 분류 가져오기 인터페이스에서 제거되었습니다. 새 날짜가 활성화되지 않고 숫자 분류를 추가할 수 없습니다. 기존 분류는 여전히 표준 분류 워크플로우를 통해 관리(업로드, 삭제)할 수 있으며 보고에서 계속 사용할 수 있습니다.

분류를 만든 후 Adobe Analytics 전체에서 새로운 데이터 특성을 활용할 수 있습니다.

**추적 코드 예**

추적 코드로만 캠페인을 보는 대신 검색 엔진, 키워드 및 캠페인 채널별로 캠페인 결과를 보려고 한다고 가정합니다. 각 변수에 대한 전환 변수를 투표하지 않고 캠페인 변수의 세 가지 분류를 만들어 검색 엔진, 키워드 및 캠페인 채널을 나타낼 수 있습니다. 이 전략을 사용하면 추가적인 태그 지정 없이 네 가지 변수를 모두 기준으로 사이트 성공 이벤트를 볼 수 있습니다.

보고 및 분석에는 추적 코드 변수에 대한 사전 정의된 분류가 포함되어 있으며, 이 변수에는 크리에이티브 요소 및 캠페인이라는 분류 기반 보고서가 제공됩니다. 다른 모든 전환 및 트래픽 변수에 대한 분류를 수동으로 구성해야 합니다.

트래픽 [분류](/help/admin/admin/c-traffic-variables/traffic-classifications.md) 및 전환 [분류를 참조하십시오](https://marketing.adobe.com/resources/help/ko_KR/reference/conversion_classifications.html).

다음 표에서는 사용 가능한 여러 유형의 분류와 이를 지원하는 변수 유형에 대해 설명합니다. 데이터 파일을 업로드하기 전에 일반 [파일 구조의](/help/components/c-classifications2/c-classifications-importer/c-saint-data-files.md) 정보를 검토하십시오.

<table id="table_279728C28D9C40EE832ACC9F211B5F17"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>유형 </p> </th> 
   <th colname="col2" class="entry"> <p>가용성 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="wintitle"> 텍스트</span> </p> </td> 
   <td colname="col2"> <p>전환 및 트래픽 변수 </p> </td> 
   <td colname="col3"> <p>텍스트 분류는 보고를 위해 변수 데이터를 그룹화할 수 있는 카테고리를 정의합니다. </p> <p>예를 들어 셔츠를 판매하는 경우 셔츠 판매(전환)를 색상, 크기 및 스타일별로 분류하여 이러한 카테고리별로 구성된 셔츠 판매를 볼 수 있는 보고서를 생성할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="wintitle"> 활성화된 날짜 텍스트</span> </p> <p>참고: Adobe는 2018년 5월 10일, Analytics 유지 관리 릴리스에서 날짜 사용 분류 기능에 대한 제한을 시작했습니다. 이러한 분류 유형은 관리자 및 분류 가져오기 인터페이스에서 제거되었습니다. 날짜 사용 분류를 새로 추가할 수 없습니다. 기존 분류는 여전히 표준 분류 워크플로우를 통해 관리(업로드, 삭제)할 수 있으며 보고에서 계속 사용할 수 있습니다. </p> </td> 
   <td colname="col2"> <p>전환 변수 </p> </td> 
   <td colname="col3"> <p>날짜 사용 텍스트 분류를 사용하면 날짜 범위를 텍스트 분류에 지정할 수 있습니다. 이것은 일반적으로 캠페인 분류에 사용되기 때문에 <span class="wintitle">캠페인</span> 보고서에서 간트 차트 보기를 이용할 수 있습니다. </p> <p>분류 데이터를 채우는 데이터 파일의 실제 캠페인 날짜를 포함할 수 있습니다. </p> <p>Reports &amp; Analytics는 캠페인 종료 날짜가 이미 경과한 경우에도 캠페인 추적 코드를 수집하지만 캠페인 종료 날짜 이후에 수집된 캠페인 데이터는 캠페인과 관련이 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="wintitle"> 숫자</span> <p>참고: Adobe는 2018년 5월 10일, Analytics 유지 관리 릴리스에서 숫자 분류 기능에 대한 제한을 시작했습니다. 이러한 분류 유형은 관리자 및 분류 가져오기 인터페이스에서 제거되었습니다. 숫자 분류를 새로 추가할 수 없습니다. 기존 분류는 여전히 표준 분류 워크플로우를 통해 관리(업로드, 삭제)할 수 있으며 보고에서 계속 사용할 수 있습니다. </p> </p> </td> 
   <td colname="col2"> <p>전환 변수 </p> </td> 
   <td colname="col3"> <p>숫자 분류를 사용하면 고정된 숫자 값을 <span class="wintitle">전환</span> 보고서에 적용할 수 있습니다. 이러한 분류는 보고서에 지표로 나타납니다. </p> <p><span class="wintitle">숫자</span> 분류를 추가할지 여부를 결정하는 경우 숫자 값이 고정되어 있고 시간이 지나도 변경되지 않아야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

