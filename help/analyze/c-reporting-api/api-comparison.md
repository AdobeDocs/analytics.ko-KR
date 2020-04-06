---
description: Analytics 보고 API에 대한 비교 표. 지원 설명서에 대한 링크가 제공됩니다.
title: Analytics 보고 API 비교
uuid: fa533a8e-33c0-42f4-a294-cabee0258c8f
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Analytics 보고 API 비교

Analytics 보고 API에 대한 비교 표. 지원 설명서에 대한 링크가 제공됩니다.

>[!NOTE] 지연과 관련하여 타겟 분석(A4T)은 통합 보고를 위해 같은 히트에 분석 데이터와 타겟 데이터를 결합합니다. Analytics와 Target의 호출은 서로 다른 시간에 발생하므로, 히트는 처리가 발생하기 전에 저장되어 두 솔루션에서 데이터를 수집합니다. 이 프로세스에서는 **추가적인 7-10분** 지연을 모든 체크포인트에 추가합니다.

<table id="table_7AF4FD678D494063ADF459B3CBC3EF3F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> API 유형 </th> 
   <th colname="col2" class="entry"> 완전히 처리됨 </th> 
   <th colname="col3" class="entry"> 실시간 </th> 
   <th colname="col4" class="entry"> 라이브 스트림 </th> 
   <th colname="col5" class="entry"> Data Warehouse </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <b>설명</b> </td> 
   <td colname="col2"> 모든 Analytics 인터페이스에서 사용할 수 있는 완전히 처리된 완료된 데이터입니다. </td> 
   <td colname="col3"> 컬렉션 후 몇 초 이내에 일부 처리된 제한된 지표를 사용할 수 있습니다. </td> 
   <td colname="col4"> 부분적으로 처리된 히트 데이터는 수집 후 몇 초 이내에 사용할 수 있습니다. </td> 
   <td colname="col5"> 대용량 데이터 내보내기를 가져오는 데 사용되는 완전히 처리되고 완료된 데이터입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="https://marketing.adobe.com/resources/help/en_US/analytics/whitepapers/analytics-data-availability.pdf"  > 지연</a> </p> </td> 
   <td colname="col2"> 30-90분 </td> 
   <td colname="col3"> * 초 - 10분 </td> 
   <td colname="col4"> 초 - 10분 </td> 
   <td colname="col5"> 90분 + </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>처리 완료</b> </td> 
   <td colname="col2"> 전체 </td> 
   <td colname="col3"> 부분 </td> 
   <td colname="col4"> 부분 </td> 
   <td colname="col5"> 전체 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="https://marketing.adobe.com/resources/help/ko_KR/reference/"  > 보고 인터페이스</a> </td> 
   <td colname="col2"> 보고 및 분석, 리포트 빌더, API </td> 
   <td colname="col3"> 보고 및 분석, 리포트 빌더, API의 실시간 보고서 </td> 
   <td colname="col4"> API만 해당 </td> 
   <td colname="col5"> 데이터 웨어하우스 및 API </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>데이터 세부기간</b> </td> 
   <td colname="col2"> 요약 </td> 
   <td colname="col3"> 요약 </td> 
   <td colname="col4"> 히트 수준 </td> 
   <td colname="col5"> 요약 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>방문자 프로필 처리</b> </td> 
   <td colname="col2"> 예 </td> 
   <td colname="col3"> 아니오 </td> 
   <td colname="col4"> 아니오 </td> 
   <td colname="col5"> 예 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>세그먼트 지원</b> </td> 
   <td colname="col2"> 예 </td> 
   <td colname="col3"> 아니오 </td> 
   <td colname="col4"> 아니오 </td> 
   <td colname="col5"> 예(하지만 데이터 웨어하우스 호환 세그먼트만) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Analytics SKU</b> </td> 
   <td colname="col2"> 표준+ </td> 
   <td colname="col3"> 표준+ </td> 
   <td colname="col4"> 프리미엄 전체 또는 예측 기반의 대응 </td> 
   <td colname="col5"> 표준+ </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>설명서</b> </td> 
   <td colname="col2"> <p> <a href="https://marketing.adobe.com/developer/documentation/analytics-reporting-1-4/get-started%E2%80%8B"  > 웹 서비스</a> </p> </td> 
   <td colname="col3"> <p> <a href="https://marketing.adobe.com/developer/documentation/analytics-reporting-1-4/real-time"  > 실시간 보고서</a> </p> </td> 
   <td colname="col4"> <p> <a href="https://marketing.adobe.com/developer/documentation/analytics-live-stream/overview-1%E2%80%8B"  > 라이브 스트리밍 개요</a> </p> </td> 
   <td colname="col5"> <p><a href="https://marketing.adobe.com/resources/help/ko_KR/reference/data_warehouse.html"  > Data Warehouse</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

**관련 도움말**

* [Adobe/IO](https://www.adobe.io/) - Adobe 기술을 애플리케이션에 통합하는 데 필요한 기술 문서 및 툴의 포괄적인 소스입니다.
* [데이터 워크벤치 쿼리 API](https://marketing.adobe.com/developer/documentation/data-workbench-query-api/c-ins-qry-api)

