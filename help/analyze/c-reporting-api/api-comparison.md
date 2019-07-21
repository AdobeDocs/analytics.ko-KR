---
description: Analytics 보고 API에 대한 비교 표입니다. 지원 문서에 대한 링크가 제공됩니다.
seo-description: Analytics 보고 API에 대한 비교 표입니다. 지원 문서에 대한 링크가 제공됩니다.
seo-title: Analytics 보고 API 비교
solution: Analytics
title: Analytics 보고 API 비교
uuid: FA 533 A 8 E -33 C 0-42 F 4-A 294-Cabee 0258 C 8 F
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Analytics 보고 API 비교

Analytics 보고 API에 대한 비교 표입니다. 지원 문서에 대한 링크가 제공됩니다.

>[!NOTE]
>
>지연과 관련해서, Target (A 4 T) 용 Analytics는 Analytics와 Target 데이터를 통합하여 통합 보고를 위해 결합합니다. 분석 호출과 타겟 호출이 다른 시간에 발생하므로 두 솔루션에서 데이터를 수집하기 위해 처리가 발생하기 전에 히트가 저장됩니다. 이 프로세스에서 모든 체크포인트에 **7-10분**&#x200B;의 지연을 추가합니다.

<table id="table_7AF4FD678D494063ADF459B3CBC3EF3F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> API 유형 </th> 
   <th colname="col2" class="entry"> 완전히 처리됨 </th> 
   <th colname="col3" class="entry"> 실시간 </th> 
   <th colname="col4" class="entry"> 라이브 스트리밍 </th> 
   <th colname="col5" class="entry"> Data Warehouse </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <b>설명</b> </td> 
   <td colname="col2"> 모든 Analytics 인터페이스에서 사용할 수 있는 완료된 데이터로, 완전히 처리되었습니다. </td> 
   <td colname="col3"> 컬렉션이 발생하면 바로 사용할 수 있는 제한된 지표로, 부분적으로 처리되었습니다. </td> 
   <td colname="col4"> 컬렉션이 발생하면 바로 사용할 수 있는 히트 데이터로, 부분적으로 처리되었습니다. </td> 
   <td colname="col5"> 가져온 대용량 데이터 내보내기에 사용되는 완료된 데이터로, 완전히 처리되었습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="https://marketing.adobe.com/resources/help/en_US/analytics/whitepapers/analytics-data-availability.pdf" format="https" scope="external"> 지연</a> </p> </td> 
   <td colname="col2"> 30-90분 </td> 
   <td colname="col3"> * 초 -10분 </td> 
   <td colname="col4"> 초 -10분 </td> 
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
   <td colname="col1"> <a href="https://marketing.adobe.com/resources/help/en_US/reference/" format="https" scope="external"> 보고 인터페이스</a> </td> 
   <td colname="col2"> Reports &amp; Analytics, Report Builder, API </td> 
   <td colname="col3"> Reports &amp; Analytics, Report Builder, API의 실시간 보고서 </td> 
   <td colname="col4"> API 전용 </td> 
   <td colname="col5"> Data Warehouse 및 API </td> 
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
   <td colname="col5"> 예(단, Data Warehouse 호환 가능한 세그먼트만) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Analytics SKU</b> </td> 
   <td colname="col2"> 표준+ </td> 
   <td colname="col3"> 표준+ </td> 
   <td colname="col4"> 프리미엄 완료 또는 예측 인텔리전스 </td> 
   <td colname="col5"> 표준+ </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>설명서</b> </td> 
   <td colname="col2"> <p> <a href="https://marketing.adobe.com/developer/documentation/analytics-reporting-1-4/get-started%E2%80%8B" format="https" scope="external"> Web Services</a> </p> </td> 
   <td colname="col3"> <p> <a href="https://marketing.adobe.com/developer/documentation/analytics-reporting-1-4/real-time" format="https" scope="external"> 실시간 보고서</a> </p> </td> 
   <td colname="col4"> <p> <a href="https://marketing.adobe.com/developer/documentation/analytics-live-stream/overview-1%E2%80%8B" format="https" scope="external"> 라이브 스트리밍 개요</a> </p> </td> 
   <td colname="col5"> <p><a href="https://marketing.adobe.com/resources/help/en_US/reference/data_warehouse.html" format="https" scope="external"> Data Warehouse</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

**관련 도움말**

* [Adobe/IO](https://www.adobe.io/) - Adobe 기술을 애플리케이션에 통합하는 데 필요한 기술 설명서 및 도구에 대한 포괄적인 소스입니다.
* [Data Workbench 쿼리 API](https://marketing.adobe.com/developer/documentation/data-workbench-query-api/c-ins-qry-api)

