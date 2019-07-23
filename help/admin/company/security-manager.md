---
description: 보고 데이터에 대한 액세스를 제어할 수 있도록 해줍니다. 어려운 암호, 암호 만료, IP 로그인 제한 및 이메일 도메인 제한 옵션이 제공됩니다.
seo-description: 보고 데이터에 대한 액세스를 제어할 수 있도록 해줍니다. 어려운 암호, 암호 만료, IP 로그인 제한 및 이메일 도메인 제한 옵션이 제공됩니다.
seo-title: 보안 관리자
solution: Analytics
title: 보안 관리자
topic: 관리 도구
uuid: B 3 FBDBA 0-E 2 BF -4 D 67-92 E 3-EF 05711141 D 4
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 보안 관리자

보고 데이터에 대한 액세스를 제어할 수 있도록 해줍니다. 어려운 암호, 암호 만료, IP 로그인 제한 및 이메일 도메인 제한 옵션이 제공됩니다.

**[!UICONTROL Analytics]** &gt; **[!UICONTROL 관리]** &gt; **[!UICONTROL 회사 설정]** &gt; **[!UICONTROL 보안]**

<table id="table_F1AD9DE5094A4FC2B9DA8D01198F944B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 요소 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 강력한 암호 필요 </span> </td> 
   <td colname="col2">다음 규칙을 준수하는 것보다 안전한 암호를 사용하도록 강제로 설정합니다. 
    <ul id="ul_100CC57EB4374DAA87B2074BA8B46F26"> 
     <li id="li_4D9102C361044FADBC14402A8398F2F3">최소 8자 길이여야 합니다. </li> 
     <li id="li_AFE9568C14894E93BFDFDC84DCD2838D">첫 문자와 마지막 문자 사이에 기호나 숫자가 한 개 이상 있어야 합니다. </li> 
     <li id="li_ECA05BEF7BFD4430B09D4A953B41D2A6">하나 이상의 알파벳 문자가 있어야 합니다. </li> 
     <li id="li_6928045588E94E28851BB15991C8D51E">사전에서 찾을 수 없거나 사전의 단어(영어)를 포함하지 않아야 합니다. </li> 
     <li id="li_C3DD4608CA6F43E4B1E4FCFC6D116371">로그인 사용자 이름에 있는 연속하는 세 개의 문자를 포함할 수 없습니다. </li> 
     <li id="li_687838CA01B94EE29EF4C09F485C5537">이전 10개 암호와 달라야 합니다. </li> 
    </ul> <p>참고: 이 기능은 앞으로 새 암호로 시행됩니다. 이것은 기존 암호를 확인하거나 사용자가 기존 암호를 변경하게 하지 않습니다. 따라서 암호 만료일을 활성화하여 사용자가 암호를 변경하고 강력한 암호 규칙을 따르게 하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 암호 만료일</span> </td> 
   <td colname="col2"> 사용자가 계정 암호를 정기적으로 변경하도록 강제로 설정합니다. 암호를 만료할 간격을 지정하고, 즉각 암호 만료를 시행할 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> IP 로그인 제한 적용</span> </td> 
   <td colname="col2"> <p>특정 IP 주소 또는 IP 주소 범위에 대한 보고서 액세스를 제한합니다. </p> <p>IP 주소 필터 목록에서 최대 100개의 항목을 추가할 수 있으며 각 항목은 특정 주소 또는 주소 범위일 수 있습니다. </p> <p>  IP 주소 필터 목록에 하나 이상의 항목이 있을 때까지 <span class="wintitle">IP 로그인 제한 적용</span>은 시행되지 않습니다. </p> <p> <span class="uicontrol"> 허용되는 IP 주소</span>: IP 주소 범위를 지정하려면 대괄호로 범위를 묶습니다 (예:
   <code> 
    192.168.10.[20-240]
   </code>). You can also use wildcards (*) to specify any number from 0 to 255 (for example, 
   <code>
    192.168.[10-14].*
   </code>) </p> <p>실패한 로그인은 기록되며 <a href="../../admin/admin/logs.md#section_6FBAF92D9EA244809C45A78A2F0A7232" format="dita" scope="local">사용 및 액세스 로그</a>에서 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 이메일 도메인 제한 적용</span> </td> 
   <td colname="col2"> <p>Analytics가 책갈피, 다운로드 가능한 보고서 및 경고를 보내는 이메일 주소 및 도메인을 필터링합니다. </p> <p>이메일 필터 목록은 최대 100개의 항목을 지원하며, 각 항목은 이메일 주소 또는 전체 이메일 도메인일 수 있습니다. </p> <p>예약된 보고서에 승인되지 않은 이메일 대상이 있는 경우 Analytics는 해당 문제에 대한 이메일 알림 및 이 보고서의 예약을 취소할 수 있는 링크를 보냅니다. </p> <p> <span class="wintitle"> 허가한 이메일 도메인 필터</span> 목록에 하나 이상의 항목이 있을 때까지 <span class="wintitle">이메일 도메인 제한 적용</span>은 시행되지 않습니다. </p> <p> <span class="uicontrol"> 허용되는 이메일 주소 및 도메인</span>: IP 주소 범위를 지정하려면 대괄호로 범위를 묶습니다 (예: <code>
     192.168.10.[20-240]
   </code>). You can also use wildcards (*) to specify any number from 0 to 255 (for example, 
   <code>
     192.168.[10-14].*
   </code>) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 암호 복구 알림</span> </td> 
   <td colname="col2"> <p>사용자가 사용자 계정 암호를 재설정하려고 할 때, 지정된 관리자에게 알립니다. </p> <p> <span class="uicontrol"> 사용 가능한 관리자</span>: 모든 관리자를 표시합니다. Ctrl 키 및 Shift 키를 누른 상태로 여러 관리자를 선택할 수 있습니다. </p> <p> <span class="uicontrol">이메일 구성원</span>: 현재 정의된 이메일 그룹을 표시합니다.  </p> </td> 
  </tr> 
 </tbody> 
</table>

