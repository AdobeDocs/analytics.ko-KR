---
description: 사전 정의된 템플릿을 선택하거나 기존 보고서 세트 중 하나를 모델로 사용하여 새 보고서 세트를 생성할 수 있습니다.
seo-description: 사전 정의된 템플릿을 선택하거나 기존 보고서 세트 중 하나를 모델로 사용하여 새 보고서 세트를 생성할 수 있습니다.
seo-title: 새 보고서 세트 - 설정
solution: Analytics
title: 새 보고서 세트 - 설정
topic: 관리 도구
uuid: 3508 F 684-11 A 3-4 C 8 F-A 233-BEA 6 BAFD 57 C 0
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 새 보고서 세트 - 설정

사전 정의된 템플릿을 선택하거나 기존 보고서 세트 중 하나를 모델로 사용하여 새 보고서 세트를 생성할 수 있습니다.

Descriptions of the elements used when [creating a report suite](../../../admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md#task_67033B9710CB49F9B71A4DE374A538A0).

>[!NOTE]
>
>[가상 보고서 세트 설명서는](/help/components/vrs/c-workflow-vrs/vrs-create.md) 가상 보고서 세트를 만드는 방법을 보여줍니다.

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
   <td colname="col2"> <p>영숫자만 포함한 고유 ID를 지정합니다. 이 ID는 생성하고 나면 변경할 수 없습니다. Adobe가 필수 ID 접두사를 설정하므로 어느 것도 변경할 수 없습니다. </p> <p>여러 보고서 세트를 생성할 경우, 고유한 보고서 세트 ID를 보장할 수 있는 이름 지정 규칙을 사용해야 합니다. </p> </td> 
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
   <td colname="col2"> (선택 사항) 보고서 세트에 대한 기준 도메인을 정의합니다. 보고서 세트의 내부 URL 필터를 명시적으로 정의하지 않는 경우 이 URL은 내부 URL 필터로 작동합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 기본 페이지</span> </td> 
   <td colname="col2"> <p>(선택 사항) <span class="wintitle">기본 페이지</span> 값이 발생하는 URL에서 해당 값 발생을 제거합니다. <span class="wintitle">최대 방문 페이지</span> 보고서가 페이지 이름이 아닌 URL을 포함하는 경우 이 설정은 동일한 웹 페이지에 대한 여러 URL을 방지합니다. </p> <p>For example, the URLs<span class="filepath"> https://mysite.com</span> and <span class="filepath"> https://mysite.com/index.html</span> are typically the same page. You can remove extraneous filenames so that both these URLs show up as <span class="filepath"> https://mysite.com</span> in your reports. </p> <p>이 값을 설정하지 않으면 Analytics는 URL에서 파일 이름 <span class="filepath">index.htm</span>, <span class="filepath">index.html</span>, <span class="filepath">index.cgi</span>, <span class="filepath">index.asp</span>, <span class="filepath">default.htm</span>, <span class="filepath">default.html</span>, <span class="filepath">default.cgi</span>, <span class="filepath">default.asp</span>, <span class="filepath">home.htm</span>, <span class="filepath">home.html</span>, <span class="filepath">home.cgi</span> 및<span class="filepath"> home.asp</span>를 자동으로 제거합니다. </p> <p>파일 이름 제거를 비활성화하려면 URL에서 발생하지 않는 기본 페이지 값을 지정합니다.  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Go Live 날짜 </p> </td> 
   <td colname="col2">이 보고서 세트가 활성화될 것으로 예상하는 날짜를 Adobe에 알려줍니다. If your deployment schedule changes, provide an updated traffic estimate using the <span class="wintitle"> Permanent Expected Traffic</span> tool in <a href="../../../admin/c-traffic-management/traffic-management.md#concept_8BD651EE8B84434CB4D6308BC6C01B79" format="dita" scope="local"> Traffic Management</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 예상 일일 페이지 보기 횟수</span> </td> 
   <td colname="col2"> 이 보고서 세트가 하루에 지원할 수 있을 것으로 예상되는 페이지 보기 횟수를 식별합니다. 트래픽 볼륨이 크면 승인 프로세스에 더 오랜 시간이 걸립니다. 처리 지연을 방지하기 위해 가능한 정확하게 이 수를 예상하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 기본 통화</span> </td> 
   <td colname="col2"> <p>모든 통화 데이터를 저장하는 데 사용되는 기본 통화를 지정합니다. Analytics는 데이터를 받을 때 현재 전환율을 사용하여 다른 통화의 거래를 기본 통화로 전환합니다. </p> <p> Analytics 보고 기능은 <span class="varname"> Currencycode</span> JavaScript 변수를 사용하여 주어진 거래의 통화를 식별합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 멀티바이트 문자 지원 비활성화 </span> </td> 
   <td colname="col2"> <p>보고서 세트에 대한 멀티바이트 문자 지원을 비활성화합니다. 멀티바이트 문자 지원을 비활성화하면 시스템에서는 데이터를 ISO-8859-1 형식으로 간주합니다. 웹 페이지는 <span class="varname"> Charset</span> JavaScript 변수를 참조하십시오. </p> <p>멀티바이트 문자 지원은 UTF-8을 사용하여 보고서 세트의 문자를 저장합니다. 수신할 때, 시스템에서는 웹 페이지의 문자 집합 데이터를 UTF-8 문자 집합으로 전환하므로 마케팅 보고서에서 모든 언어를 사용할 수 있습니다. </p> <p>기존 보고서 세트에 대한 멀티바이트 문자 지원을 변경하려면 계정 관리자 또는 고객 지원 센터에 문의하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 이 세트에 대한 Ad Hoc Analysis 활성화</span> </td> 
   <td colname="col2"> Ad Hoc Analysis을 수행할 때 이 보고서 세트를 볼 수 있도록 합니다. </td> 
  </tr> 
 </tbody> 
</table>

