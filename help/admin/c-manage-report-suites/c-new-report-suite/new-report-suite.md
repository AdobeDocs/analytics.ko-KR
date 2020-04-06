---
description: 사전 정의된 템플릿을 선택하거나 기존 보고서 세트 중 하나를 모델로 사용하여 새 보고서 세트를 생성할 수 있습니다.
title: 새 보고서 세트 - 설정
topic: Admin tools
uuid: 3508f684-11a3-4c8f-a233-bea6bafd57c0
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 새 보고서 세트 - 설정

사전 정의된 템플릿을 선택하거나 기존 보고서 세트 중 하나를 모델로 사용하여 새 보고서 세트를 생성할 수 있습니다.

[보고서 세트를 만들](/help/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md) 때 사용되는 요소에 대한 설명입니다.

>[!NOTE] [가상 보고서 세트 설명서](/help/components/vrs/c-workflow-vrs/vrs-create.md)는 가상 보고서 세트를 생성하는 방법을 보여줍니다.

<table id="table_F739FBD8DB8D409E916F12F61C5953D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 요소 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 보고서 세트 ID </span> </td> 
   <td colname="col2"> <p>영숫자만 포함할 수 있는 고유한 ID를 지정합니다. 이 ID를 만든 후에는 변경할 수 없습니다. Adobe는 필수 ID 접두사를 설정하며 변경할 수도 없습니다. </p> <p>여러 보고서 세트를 생성할 경우, 고유한 보고서 세트 ID를 보장할 수 있는 이름 지정 규칙을 사용해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 사이트 제목</span> </td> 
   <td colname="col2"><span class="wintitle">관리 도구</span>에서 보고서 세트를 식별합니다. 이 제목은 세트 헤더의 <span class="wintitle">보고서 세트</span> 드롭다운 목록에서도 사용됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 시간대</span> </td> 
   <td colname="col2"> 이벤트 및 타임스탬프 데이터를 예약합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 기본 URL</span> </td> 
   <td colname="col2"> (선택 사항) 보고서 세트의 기본 도메인을 정의합니다. 이 URL은 보고서 세트에 대한 내부 URL 필터를 명시적으로 정의하지 않는 경우 내부 URL 필터로 작동합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 기본 페이지</span> </td> 
   <td colname="col2"> <p>(선택 사항) <span class="wintitle">기본 페이지</span> 값이 발생하는 URL에서 해당 값을 제거합니다. <span class="wintitle">가장 방문 빈도가 높은 페이지</span> 보고서가 페이지 이름이 아닌 URL을 포함하는 경우 이 설정은 동일한 웹 페이지에 대한 여러 URL을 방지합니다. </p> <p>예를 들어 URL <span class="filepath">https://mysite.com</span> 및 <span class="filepath">https://mysite.com/index.html</span>은 일반적으로 동일한 페이지입니다. 필요 없는 파일 이름을 제거하여 보고서에서 이러한 URL을 모두 <span class="filepath">https://mysite.com</span>으로 표시되도록 할 수 있습니다. </p> <p>이 값을 설정하지 않으면 Analytics는 URL에서 파일 이름 <span class="filepath">index.htm</span>, <span class="filepath">index.html</span>, <span class="filepath">index.cgi</span>, <span class="filepath">index.asp</span>, <span class="filepath">default.htm</span>, <span class="filepath">default.html</span>, <span class="filepath">default.cgi</span>, <span class="filepath">default.asp</span>, <span class="filepath">home.htm</span>, <span class="filepath">home.html</span>, <span class="filepath">home.cgi</span> 및<span class="filepath"> home.asp</span>를 자동으로 제거합니다. </p> <p>파일 이름 제거를 비활성화하려면 URL에서 발생하지 않는 기본 페이지 값을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Go Live 날짜 </p> </td> 
   <td colname="col2">이 보고서 세트가 활성화될 것으로 예상되는 날짜를 Adobe에 알려줍니다. 배포 일정이 변경되면 <a href="/help/admin/c-traffic-management/traffic-management.md">트래픽 관리</a>에서 <span class="wintitle">영구적인 예상 트래픽 도구</span>를 사용하여 업데이트된 예상 트래픽을 제공합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 예상 일별 페이지 보기 수</span> </td> 
   <td colname="col2"> 이 보고서 세트가 하루에 지원할 것으로 예상되는 페이지 보기 횟수를 식별합니다. 대량의 트래픽 볼륨은 더 긴 승인 프로세스를 필요로 합니다. 처리 지연을 방지하려면 이 예상치를 최대한 정확하게 사용하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 기본 통화</span> </td> 
   <td colname="col2"> <p>모든 통화 데이터를 저장하는 데 사용되는 기본 통화를 지정합니다. Analytics 보고 기능은 데이터를 받을 때 현재 전환율을 사용하여 다른 통화의 거래를 기본 통화로 전환합니다. </p> <p> Analytics 보고는 통화 코드 <span class="varname"> JavaScript</span> 변수를 사용하여 지정된 거래의 통화를 식별합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 멀티바이트 문자 지원 비활성화 </span> </td> 
   <td colname="col2"> <p>보고서 세트에 대한 멀티바이트 문자 지원을 비활성화합니다. 멀티바이트 문자 지원을 비활성화하면 시스템에서 데이터가 ISO-8859-1 형식으로 되어 있다고 가정합니다. 웹 페이지는 charSet JavaScript 변수에서 해당 문자 집합을 <span class="varname"> 지정해야</span> 합니다. </p> <p>멀티바이트 문자 지원은 UTF-8을 사용하여 보고서 세트의 문자를 저장합니다. 수신 시 시스템은 웹 페이지의 문자 집합에서 UTF-8 문자 집합으로 데이터를 변환하므로 마케팅 보고서에서 모든 언어를 사용할 수 있습니다. </p> <p>기존 보고서 세트에 대한 멀티바이트 문자 지원을 변경하려면 계정 관리자 또는 고객 지원 센터에 문의하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 이 세트에 대한 Ad Hoc Analysis 활성화</span> </td> 
   <td colname="col2"> Ad Hoc Analysis를 수행할 때 이 보고서 세트를 볼 수 있도록 합니다. </td> 
  </tr> 
 </tbody> 
</table>

