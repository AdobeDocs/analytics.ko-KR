---
description: 보고 데이터에 대한 액세스를 제어할 수 있도록 해줍니다. 어려운 암호, 암호 만료, IP 로그인 제한 및 이메일 도메인 제한 옵션이 제공됩니다.
solution: Analytics
title: 보안 관리자
topic: Admin tools
uuid: b3fbdba0-e2bf-4d67-92e3-ef05711141d4
translation-type: tm+mt
source-git-commit: 229ce50a24bd7b86e3859775bb4fbeba1c6a5668

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
   <td colname="col2"> <p>(이 기능은 Experience Cloud 로그인과 함께 사용할 수 없습니다. 이 기능은 2020년 10월부터 더 이상 사용할 수 없습니다.) 특정 IP 주소 또는 IP 주소 범위에 대한 보고서 액세스를 제한합니다. </p> <p>IP 주소 필터 목록에서 최대 100개의 항목을 추가할 수 있으며 각 항목은 특정 주소 또는 주소 범위일 수 있습니다. </p> <p>  IP 주소 필터 목록에 하나 이상의 항목이 있을 때까지 <span class="wintitle">IP 로그인 제한 적용</span>은 시행되지 않습니다. </p> <p> <span class="uicontrol"> 허용된 IP 주소</span>:IP 주소 범위를 지정하려면 대괄호로 범위를 묶습니다(예: <code>
       192.168.10.[20-240]
     </code>). You can also use wildcards (*) to specify any number from 0 to 255 (for example, 
     <code>
       192.168.[10-14].*
     </code>) </p> <p>실패한 로그인은 기록되며 <a href="/help/admin/admin/logs.md#section_6FBAF92D9EA244809C45A78A2F0A7232">사용 및 액세스 로그</a>에서 볼 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 이메일 도메인 제한 적용</span> </td> 
   <td colname="col2"> <p>Analytics가 책갈피, 다운로드 가능한 보고서 및 경고를 보내는 이메일 주소 및 도메인을 필터링합니다. </p> <p>이메일 필터 목록은 최대 100개의 항목을 지원하며, 각 항목은 이메일 주소 또는 전체 이메일 도메인일 수 있습니다. </p> <p>예약된 보고서에 승인되지 않은 이메일 대상이 있는 경우 Analytics는 해당 문제에 대한 이메일 알림 및 이 보고서의 예약을 취소할 수 있는 링크를 보냅니다. </p> <p> <span class="wintitle"> 허가한 이메일 도메인 필터</span> 목록에 하나 이상의 항목이 있을 때까지 <span class="wintitle">이메일 도메인 제한 적용</span>은 시행되지 않습니다. </p> <p> <span class="uicontrol"> 수락된 이메일 주소 및 도메인</span>:IP 주소 범위를 지정하려면 대괄호로 범위를 묶습니다(예: <code>
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

## IP 로그인 제한 [!UICONTROL 적용을 위한 수명 종료]

IP **[!UICONTROL 로그인 제한]** 적용 기능은 안전한 것으로 간주되는 특정 IP 주소를 허용 목록에 추가하여 로그인 성공 및 Adobe Analytics 환경에 액세스할 수 있도록 하는 곧 사용 가능한 레거시 분석 기능입니다. 대부분의 경우 이 기능은 사용자가 로그인할 수 있는 유일한 보안 IP 주소로 회사 IP 주소를 설정하는 데 사용됩니다. 따라서 Adobe Analytics를 사용하려면 사용자가 회사 사무실에 있거나 VPN을 통해 네트워크에 로그인해야 합니다.

### 왜 우리는 그것을 인생의 종말을 고려하고 있는가?

이 기능은 Experience Cloud 로그인 마이그레이션 및/또는 Experience Cloud 로그인으로 인해 일부 상황에서 중단됩니다. 고객 속성 또는 대상 라이브러리를 사용하는 고객의 경우 **[!UICONTROL 중단되는]** 것으로 **[!UICONTROL 알려져 있습니다]**.

또한, 여러 Experience Cloud 솔루션을 소유하고 있는 경우, 이 기능이 존재하지 않거나 Analytics 자체 외부에서 지원되지 않으므로 다른 솔루션과 함께 Experience Cloud에 로그인하여 이 요구 사항을 우회할 수 있습니다. 사용자는 IP 스푸핑을 통해 이 문제를 해결할 수도 있습니다.

마지막으로 Adobe는 SSO(Single-Sign-On) 및 Federated ID를 통해 완벽하게 작동하는 탁월한 대체 솔루션을 제공합니다. 이 기능을 사용하면 사용자의 로그인 경험을 보다 효과적으로 제어하고 보안을 강화할 수 있습니다.

### 이 기능의 제거는 어떤 영향을 미칩니까?

IP 로그인 제한 **[!UICONTROL 적용을]** 설정한 모든 고객의 경우 이 기능은 2020년 10월에 제거됩니다. 이때 IP 로그인 제한 사항은 더 이상 적용되지 않습니다. 여전히 IP 주소로 로그인을 제한해야 하는 경우 SSO(Single-Sign-On) 및 Federated ID의 권장 솔루션을 검토하고 구현해야 합니다(자세한 정보 및 리소스).

또한 **[!UICONTROL IP 로그인 제한]** 적용 관리자는 Analytics UI의 **[!UICONTROLAdmin &gt; 회사 설정 &gt; 보안 관리자에서]** 제거됩니다(아래 참조).

![](assets/sec-manager2.png)

### 다른 선택사항은 무엇입니까?

위에서 설명한 바와 같이 이 Analytics 기능은 사용이 종료됩니다. SSO 및 Federated ID를 구현할 수 있는 시간을 제공하기 위해 EOL 날짜가 2020년 10월로 연기되었습니다.

SSO와 Federated ID는 모두 IP 로그인 제한 기능보다 뛰어난 솔루션이며 더 많은 제어, 보안 및 기능을 제공합니다.

SSO/Federated ID 설정 방법에 대한 자세한 내용은 다음 도움말 설명서를 참조하십시오. IT 부서에서 이를 철저히 읽고 이를 구현하도록 권장합니다.

* [Single Sign-On 및 Experience Cloud](https://spark.adobe.com/page/JeSB8EPEQIvjD/)
* [관리 콘솔 - ID 설정 설명서](https://helpx.adobe.com/enterprise/using/set-up-identity.html)
* [관리 콘솔 - ID 설정 자습서(비디오)](https://helpx.adobe.com/enterprise/how-to/identity-directories-domains.html?playlist=/ccx/v1/collection/product/enterprise/topics/enterprise-identity/collection.ccx.js&ref=helpx.adobe.com)
* [Federated ID 튜토리얼 구성(비디오)](https://helpx.adobe.com/enterprise/how-to/identity-configure-ids.html?playlist=/ccx/v1/collection/product/enterprise/topics/enterprise-identity/collection.ccx.js&ref=helpx.adobe.com)
* [Single Sign-On - 일반적인 질문](https://helpx.adobe.com/enterprise/using/sso-faq.html)
* [Adobe에서 지원하는 ID 유형](https://helpx.adobe.com/enterprise/using/identity.html)

IP 로그인 제한 사항에 대한 지원을 계속 요청하고 Experience Cloud에서 제공하도록 요청하려면 포럼 페이지에서 [이 기능에 대해 투표할 수](https://forums.adobe.com/ideas/11648)있습니다. SSO/Federated ID 및 EXC에 대한 추가 질문이나 정보는 Ryan Monger(monger@adobe.com)에게 문의하십시오.
