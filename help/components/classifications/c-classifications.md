---
title: 분류 개요
description: 차원 항목 그룹을 사용자 지정합니다.
exl-id: 0d2c77ea-610f-48e0-b6a2-6e91794783b1
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '605'
ht-degree: 100%

---

# 분류 개요

분류란 Analytics 변수 데이터를 카테고리별로 분류하여 보고서를 생성할 때 여러 다른 방법으로 데이터를 표시하는 방법입니다.

[분석 분류](https://video.tv.adobe.com/v/16853/)의 비디오 개요

**[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]** > **[!UICONTROL 설정 편집]** > *`<Traffic or Conversion>`*

분류 시 변수 및 해당 변수와 관련된 메타데이터 간의 관계를 설정하려고 합니다. 분류는 캠페인에서 가장 흔하게 사용됩니다. 변수 (eVars, prop 및 이벤트) 정보를 사용하여 수집된 데이터는 변수에서 수집된 값에 메타데이터를 적용하여 롤업할 수 있습니다.

![단계 정보](assets/sub_class_create.png)

한 번 분류하면, 키 변수를 사용하여 생성할 수 있는 모든 보고서를 연관된 특성을 사용하여 생성할 수 있습니다. 예를 들어 제품 이름, 색상, 크기, 설명 및 SKU와 같은 추가 제품 특성을 사용하여 [!UICONTROL 제품 ID]를 분류할 수 있습니다. 추가 특성을 사용하여 Reports &amp; Analytics 데이터를 늘리면 보다 심도 있고 복잡한 보고 기회를 제공할 수 있습니다.

분류를 만든 후 Adobe Analytics 전체에서 새로운 데이터 특성을 활용할 수 있습니다.

## 추적 코드 예제

단지 추적 코드별로 캠페인을 보는 것이 아니라 검색 엔진, 키워드, 캠페인 채널별로 캠페인 결과를 보기를 원한다고 가정해 보겠습니다. 각각에 대한 전환 변수에 집중하는 것이 아니라 3가지 캠페인 변수 분류를 만들어 검색 엔진, 키워드, 캠페인 채널을 나타낼 수 있습니다. 이 전략을 사용하면 추가 태그를 지정하지 않아도 4가지 모든 변수를 기준으로 사이트 성공 이벤트를 볼 수 있습니다.

Reports &amp; Analytics에는 추적 코드 변수를 위해 사전 정의된 분류가 포함되어 있으며, 크리에이티브 요소 및 캠페인이라고 하는 분류 기반 보고서를 제공합니다. 다른 모든 전환 및 트래픽 변수에 대한 분류를 수동으로 구성해야 합니다.

[트래픽 분류](/help/admin/admin/c-traffic-variables/traffic-classifications.md) 및 [전환 분류](https://docs.adobe.com/content/help/ko-KR/analytics/admin/admin-tools/conversion-variables/conversion-classifications.html)를 참조하십시오.

다음 표는 사용 가능한 분류의 다양한 유형과 각 분류를 지원하는 변수 유형을 나타냅니다. 데이터 파일을 업로드하기 전에 [일반 파일 구조](/help/components/classifications/importer/c-saint-data-files.md)의 정보를 검토하십시오.

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
   <td colname="col3"> <p>텍스트 분류는 범주를 정의하여 보고를 위한 변수 데이터를 그룹화합니다. </p> <p>예를 들어 셔츠를 판매할 경우 셔츠 판매를 색상, 크기 및 스타일별로 분류하면, 해당 범주별로 구성된 셔츠 판매를 확인할 수 있는 보고서를 생성할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="wintitle"> 활성화된 날짜 텍스트</span> </p> <p>참고: Adobe는 2018년 5월 10일, Analytics 유지 관리 릴리스에서 날짜 사용 분류 기능에 대한 제한을 시작했습니다. 이러한 분류 유형은 관리자 및 분류 가져오기 인터페이스에서 제거되었습니다. 날짜 사용 분류를 새로 추가할 수 없습니다. 기존 분류는 여전히 표준 분류 워크플로를 통해 관리 (업로드, 삭제)할 수 있으며 보고에서 계속 사용할 수 있습니다. </p> </td> 
   <td colname="col2"> <p>전환 변수 </p> </td> 
   <td colname="col3"> <p>활성화된 날짜 텍스트 분류를 사용하면 날짜 범위를 텍스트 분류에 할당할 수 있습니다. 이것은 일반적으로 캠페인 분류에 사용되기 때문에 <span class="wintitle">캠페인</span> 보고서에서 간트 차트 보기를 이용할 수 있습니다. </p> <p>분류 데이터를 채우는 데이터 파일의 실제 캠페인 날짜를 포함할 수 있습니다. </p> <p>Reports &amp; Analytics는 캠페인 종료 날짜가 이미 경과한 경우에도 캠페인 추적 코드를 수집하지만 캠페인 종료 날짜 이후에 수집된 캠페인 데이터는 캠페인과 관련이 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="wintitle"> 숫자</span> <p>참고: Adobe는 2018년 5월 10일, Analytics 유지 관리 릴리스에서 숫자 분류 기능에 대한 제한을 시작했습니다. 이러한 분류 유형은 관리자 및 분류 가져오기 인터페이스에서 제거되었습니다. 숫자 분류를 새로 추가할 수 없습니다. 기존 분류는 여전히 표준 분류 워크플로를 통해 관리 (업로드, 삭제)할 수 있으며 보고에서 계속 사용할 수 있습니다. </p> </p> </td> 
   <td colname="col2"> <p>전환 변수 </p> </td> 
   <td colname="col3"> <p>숫자 분류를 사용하면 고정된 숫자 값을 <span class="wintitle">전환</span> 보고서에 적용할 수 있습니다. 이러한 분류는 보고서에 지표로 나타납니다. </p> <p><span class="wintitle">숫자</span> 분류를 추가할지 여부를 결정하는 경우 숫자 값이 고정되어 있고 시간이 지나도 변경되지 않아야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
