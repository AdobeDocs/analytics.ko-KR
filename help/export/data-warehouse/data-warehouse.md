---
description: Data Warehouse는 데이터를 필터링하여 실행할 수 있는 스토리지 및 사용자 지정 보고서에 대한 Analytics 데이터 사본을 참조합니다. 특별한 질문에 따라 원시 데이터의 고급 데이터 관계를 표시하는 보고서를 요청할 수 있습니다. Data Warehouse 보고서는 FTP를 통해 전송되거나 메일로 보내지며 처리하는 데 72시간까지 소요될 수 있습니다. 처리 시간은 쿼리의 복잡성과 요청된 데이터의 양에 따라 달라집니다.
seo-description: Data Warehouse는 데이터를 필터링하여 실행할 수 있는 스토리지 및 사용자 지정 보고서에 대한 Analytics 데이터 사본을 참조합니다. 특별한 질문에 따라 원시 데이터의 고급 데이터 관계를 표시하는 보고서를 요청할 수 있습니다. Data Warehouse 보고서는 FTP를 통해 전송되거나 메일로 보내지며 처리하는 데 72시간까지 소요될 수 있습니다. 처리 시간은 쿼리의 복잡성과 요청된 데이터의 양에 따라 달라집니다.
seo-title: 데이터 웨어하우스 개요
solution: Analytics
title: 데이터 웨어하우스 개요
topic: Data Warehouse
uuid: 768557 DD -1644-4 CE 6-BFC 2-8 C 46 DD 6 E 1 CD 1
translation-type: tm+mt
source-git-commit: 15d49195e5d555adcc37366d679d6b971972504b

---


# 데이터 웨어하우스 개요

Data Warehouse는 데이터를 필터링하여 실행할 수 있는 스토리지 및 사용자 지정 보고서에 대한 Analytics 데이터 사본을 참조합니다. 특별한 질문에 따라 원시 데이터의 고급 데이터 관계를 표시하는 보고서를 요청할 수 있습니다. Data Warehouse 보고서는 FTP를 통해 전송되거나 메일로 보내지며 처리하는 데 72시간까지 소요될 수 있습니다. 처리 시간은 쿼리의 복잡성과 요청된 데이터의 양에 따라 달라집니다.

Adobe는 관리자 수준 사용자에 대해서만 특정 보고서 세트에 대해 Data Warehouse를 사용할 수 있도록 합니다. (Data Warehouse는 전체 및 하위 보고서 세트를 활성화할 수 있지만 롤업 보고서 세트는 활성화할 수 없습니다.) 관리자는 데이터 웨어하우스에 대한 액세스 권한이 있는 그룹을 만든 다음 해당 그룹에 비관리자 수준의 사용자를 연결할 수 있습니다.

Data Warehouse는 크기가 1MB를 초과하는 모든 파일을 자동으로 압축합니다. 최대 이메일 첨부 파일 크기는 10MB입니다.

Data Warehouse는 개별적으로 예약하고 다운로드한 보고서를 한 번 요청하여 행 수에 관계없이 처리할 수 있습니다.

>[!NOTE]
>
>데이터 웨어하우스는 보고 기간에 발생한 첫 번째 값을 보고합니다.

>[!IMPORTANT]
>
>분류된 값에 세그먼트화할 때 분석 작업 공간과 데이터 웨어하우스는'지정되지 않음'값을 다르게 처리합니다. Workspace에서 '지정되지 않음'은 분류되지 않은 값을 나타내지만, Data Warehouse에서 '지정되지 않음'은 "지정되지 않음"으로 분류한 값을 나타냅니다.

## Data Warehouse 요청 설명 {#section_F21C78ED36884C389C852E876AF5CDE8}

다음 표에서는 [!UICONTROL Data Warehouse 요청] 탭에 대한 필드 및 옵션에 대해 설명합니다.

<table id="table_7325A2466866460E8B0AF7D696152713"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 요소 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 요청 이름</span> </td> 
   <td colname="col2"> 요청을 식별합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 보고 날짜</span> </td> 
   <td colname="col2"> <p>요청의 날짜 및 세부기간  </p> 
    <ul id="ul_C00F4529BD9E4113B517A61751B1DD5C"> 
     <li id="li_4D7C26812DF94ED7B64F985309541F46"> <span class="wintitle"> 사용자 지정</span>: 달력에서 사용자가 구성하는 날짜 범위입니다. </li> 
     <li id="li_2B272087006847148A936350D1B2D523"> <span class="wintitle">사전 설정</span>: 범위를 사전에 설정합니다. 사전 설정된 범위는 보고서 날짜에 대해 상대적입니다. </li> 
     <li id="li_745989965BB94D489FF7046587E13C42"> <span class="wintitle">세부기간</span>: 시간을 세부적으로 분할합니다. 유효한 값은 없음, 시간대별, 일일, 주간, 월간, 분기별 및 연간입니다. </li> 
    </ul> <p>가상 보고서 세트에 대한 Data Warehouse 보고는 가상 보고서 세트에서 구성된 대체 시간대를 지원합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 사용 가능한 세그먼트</span> </td> 
   <td colname="col2"> <p>복잡한 세그먼트를 검사 및 생성할 방문자 인구의 일부를 선택할 수 있도록 해줍니다. 사전 구성된 세그먼트를 로드하고 새 세그먼트를 만들고 추가 세그먼트를 작성하는 데 사용할 세그먼트 구성 요소를 라이브러리에 저장할 수 있습니다. </p> <p>이제 세그먼트를 스택할 수 있습니다. 여러 개의 세그먼트를 선택할 때 미리 보기 영역, 요청 관리자 및 요청 세부 사항 팝업에 쉼표로 구분된 이름 목록이 표시됩니다(예: Segment1, Segment2). </p> <p>자세한 내용은 [세그멘테이션 가이드] (/help/components/c-segmentation/seg-home. md) 를 참조하십시오. </p> <p>참고: 세그먼트 필터와 분류를 동일한 Data Warehouse 보고서의 동일한 세그먼트에 포함할 수 없습니다. 그렇게 하면 오류가 발생합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 분류</span> </td> 
   <td colname="col2"> <p>분류를 사용하여 데이터를 분류할 수 있도록 해줍니다. 세그먼트와 분류는 세그먼트가 데이터 세트에서 데이터를 필터링하고, 분류는 분류를 위해 데이터를 유효한 모든 값으로 구분한다는 점에서 서로 다릅니다.  </p> 하나 이상의 세그먼트로 보고서를 분류할 수도 있습니다. 하지만 세그먼트 필터와 분류를 동일한 Data Warehouse 보고서의 동일한 세그먼트에 포함할 수 없습니다. 그렇게 하면 오류가 발생합니다. <p> 예를 들어 데이터 세트에서 성을 제거하려면 세그먼트를 하지만 데이터를 성별로 구분하여 보려면 분류를 사용합니다. </p> <p>Data Warehouse 요청이 여러 개의 다중 값 측정기준과 함께 제출되면(예: 다양한 모바일 보고서), 행이 하나의 히트로부터 기하급수적으로 생성될 수 있습니다. 하나의 히트로부터 출력할 수 있는 행의 개수는 100개(이전에는 1,000개)로 제한됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 지표</span> </td> 
   <td colname="col2">보고할 지표를 추가할 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="wintitle"> 지표 정렬</span> </td> 
   <td colname="col2">Reports &amp; Analytics 사용자 인터페이스, Data Workbench 등에 표시되는 항목과 유사하고, 내림차순 지표 값을 기준으로 정렬된 등급 분류 보고서를 제공합니다. <a href="../../export/data-warehouse/sorting-by-metric.md#concept_7B7BDE3D42E549389DACA1E33B2FC1CC" format="dita" scope="local"> 자세히...</a> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 배달 예약</span> </td> 
   <td colname="col2"> <p>선택한 간격으로 또는 일회성 보고서로서 요청에 대한 자동 배달 일정을 예약할 수 있도록 해줍니다. 기본 양식을 사용할 경우 보고서는 이메일에 .csv 파일로 도착합니다. </p> <p>데이터 범위를 추가하려면 파일 이름에 <span class="filepath">%R</span>을 포함시킵니다. 이 값은 보고서에서 요청되는 날짜 값을 나타냅니다. 예를 들어 2013년 5월 1일부터 2013년 5월 7일까지의 데이터를 요청하는 경우 <span class="filepath">%R</span>은 20130501 - 20130507 날짜 범위를 포함하는 파일 이름을 보여줍니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

