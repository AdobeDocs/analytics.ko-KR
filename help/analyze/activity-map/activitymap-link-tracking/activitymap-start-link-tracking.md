---
description: Activity Map 또는 레거시 ClickMap에서의 링크 추적을 시작하는 절차.
seo-description: Activity Map 또는 레거시 ClickMap에서의 링크 추적을 시작하는 절차.
seo-title: 링크 추적 시작
solution: Analytics
title: 링크 추적 시작
topic: Activity Map
uuid: 425 CB 287-F 76 E -4430-802 F -288499711 BA 9
translation-type: tm+mt
source-git-commit: 01a6fc7e44dc71b868bd38a4f6a5a4089eae6349

---


# 링크 추적 시작

Activity Map 또는 레거시 ClickMap에서의 링크 추적을 시작하는 절차.

<table id="table_1745199B3105467CBA26F50B3B1CCE99"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 다음에서 링크 추적을 시작하려면 </th> 
   <th colname="col2" class="entry"> 방법... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Activity Map </td> 
   <td colname="col2"> Appmeasurement.js 파일에서 다음 컨텐츠를 추가하십시오. 
    <code>/* Activity Map 모듈 시작 다음 모듈은 Adobe Analytics 에서 Activity Map 추적을 활성화합니다.Activity Map 에서는 링크 및 컨텐트에 대한 데이터 오버레이를 보고 사용자가 웹 사이트와 어떻게 교류하는지를 이해할 수 있습니다.Activity Map 을 사용하지 않으려면 appmeasurement. js 파일에서 다음 코드 블록을 제거할 수 있습니다.
  Additional documentation on how to configure Activity Map is available at:
      https://marketing.adobe.com/resources/help/en_US/analytics/activitymap/getting-started-admins.html
     */
     function AppMeasurement_Module_Activity Map(g){func
     ...
     /* END Activity Map MODULE */
    </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1">  ClickMap(이전 Visitor ClickMap) </td> 
   <td colname="col2"> <p><a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/trackInlineStats.html" format="https" scope="external">trackInlineStats</a> 변수를 true로 설정하십시오. The syntax reads as follows: 
     <code>
       s.trackInlineStats=true
     </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

