---
description: 다이내믹 태그 관리의 [라이브러리 관리] 설정에 있는 필드 및 옵션에 대한 설명입니다.
keywords: 라이브러리 관리; 페이지 코드; 라이브러리 로드 위치; Adobe에서 관리; 사용자 지정; 호스팅된 코드; s_ code hosted
seo-description: 다이내믹 태그 관리의 [라이브러리 관리] 설정에 있는 필드 및 옵션에 대한 설명입니다.
seo-title: 라이브러리 관리
solution: Marketing Cloud, 다이내믹 태그 관리
title: 라이브러리 관리
uuid: 4 cfa 47 f 9-ae 98-4 feb-a 58 d-a 3 a 6 e 45 f 8 d 5 b
translation-type: tm+mt
source-git-commit: 3489f00bd7dddefda0420fc361056416f6f10d3f

---


# 라이브러리 관리

다이내믹 태그 관리의 [라이브러리 관리] 설정에 있는 필드 및 옵션에 대한 설명입니다.

**[!UICONTROL *`Property`*]** &gt; ![](assets/settings_gear.png)**[!UICONTROL 편집 도구]** &gt; **[!UICONTROL 라이브러리 관리]**

>[!NOTE]
>
>하나의 웹 속성에서 둘 이상의 Adobe Analytics 도구를 사용하는 경우 각 도구에 고유한 추적기 변수 이름이 있어야 합니다. 단일 웹 속성 내에서 Adobe Analytics 도구 간에 개체 변수 이름이 중복 사용되면 충돌을 일으킵니다.

<table id="table_2758C770C91B4025AD74009B360D71F7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 요소 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>페이지 코드가 이미 있습니다. </p> </td> 
   <td colname="col2"> <p> <span class="keyword">Adobe Analytics</span> 페이지 코드가 이미 사이트에 있을 경우 다이내믹 태그 관리가 Adobe Analytics 페이지 코드를 설치하지 못하도록 합니다. </p> <p>이 기능을 사용하면 처음부터 새로 시작하지 않고 다이내믹 태그 관리를 사용하여 기존 구현에 추가할 수 있습니다. 이 확인란을 선택할 때는 추적기 변수 이름을 적절히 설정해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>라이브러리 로드 위치: &lt;<span class="term"> 페이지 상단</span> 또는 <span class="term"> 페이지 하단</span>&gt; </p> </td> 
   <td colname="col2"> <p>페이지 코드를 로드할 위치와 시간을 지정합니다. 어느 항목을 선택하든 관계없이 Analytics 도구를 사용하는 모든 규칙의 설정이 동일해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Adobe에서 관리(권장) </p> </td> 
   <td colname="col2"> <p>다이내믹 태그 관리를 활성화하여 라이브러리를 관리합니다. </p> <p>이 옵션을 선택하면 다음 옵션을 사용할 수 있습니다. </p> <p> <b>라이브러리 버전: </b><span class="wintitle">라이브러리 버전</span> 메뉴에서 최신 버전을 선택합니다. 다이내믹 태그 관리는 새 버전이 출시되면 알림을 보냅니다. 필요할 때 이전 버전으로 되돌릴 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 사용자 지정 </p> </td> 
   <td colname="col2"> <p>라이브러리 코드를 구성할 수 있습니다. </p> <p>이 옵션을 선택하면 아래 옵션이 활성화됩니다. </p> <p> <b>아래의 사용자 지정 코드를 사용하여 보고서 세트 설정: </b>이 확인란을 선택하면 다이내믹 태그 관리가 <span class="varname"> s_account</span>. 이 변수에는 데이터를 전송하려는 보고서 세트의 쉼표로 구분된 목록이 포함됩니다. </p> <p> <b>호스팅된 코드: </b><span class="filepath">s_code</span>를 호스팅하려면 다음 옵션을 선택합니다. </p> 
    <ul id="ul_FC395283365A4BBAA8A5FE5871D16EC6"> 
     <li id="li_36D733C533CE40F1868309130551D4DE"> <b>DTM</b>: 다이내믹 태그 관리 내에 <span class="filepath">s_code</span>를 호스팅할 수 있습니다. <span class="uicontrol">코드 편집</span>을 클릭하여 파일을 잘라 편집기에 바로 붙여넣을 수 있습니다. </li> 
     <li id="li_A64734C66D254079A5E16DC8DBEDA3F6"> <b>URL</b>: 양호한 <span class="filepath">s_code</span> 파일이 있고 이 파일의 업데이트 프로세스에 만족하는 경우 여기에서 파일에 URL을 제공할 수 있습니다. 그러면 다이내믹 태그 관리에서는 <span class="filepath">Adobe Analytics</span> 구현에 이 <span class="keyword">s_code</span> 파일을 사용합니다. </li> 
    </ul> <p> <b>편집기 열기: </b>핵심 Appmeasurement 코드를 <a href="../../../implement/c-implement-with-dtm/c-aa-tool/t-appmeasurement-code.md#task_068D72664B2743359A64ADB8692D3658" format="dita" scope="local"> 삽입할 수</a>있습니다. This code is populated automatically when using the automatic configuration method described in <a href="../../../implement/c-implement-with-dtm/c-aa-tool/analytics-dtm.md#concept_FBA6679A0B79490F8296437F11E5E4F8" format="dita" scope="local"> Adobe Analytics Settings</a>. </p> <p> <b>추적기 변수 이름: </b>두 개의 <span class="keyword"> Adobe Analytics</span> 인스턴스를 동시에 실행하려는 경우 (하나는 다이내믹 태그 관리 내에서, 하나는 기본적으로) 기본 <span class="term"> s</span> 개체 이름을 변경할 수 있습니다. 개체의 이름을 변경하면 충돌을 피할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

