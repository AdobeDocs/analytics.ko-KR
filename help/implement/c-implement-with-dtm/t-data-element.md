---
description: 다이내믹 태그 관리에서 데이터 요소를 만듭니다.
keywords: 다이내믹 태그 관리; 데이터 요소; 새 데이터 요소 만들기; name; type; 기본값; 소문자 값 강제 적용; 이 값은
seo-description: 다이내믹 태그 관리에서 데이터 요소를 만듭니다.
seo-title: 데이터 요소 만들기
solution: Marketing Cloud, Analytics, Target, 다이내믹 태그 관리
title: 데이터 요소 만들기
uuid: Eacd 5 c 60-6197-4129-A 9 E 1-A 39 E 9 A 58 B 38 A
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 데이터 요소 만들기

다이내믹 태그 관리에서 데이터 요소를 만듭니다.

1. [웹 속성을 아직 만들지 않았으면](../../implement/c-implement-with-dtm/t-create-web-property.md#task_960467FBB7A54499AC228CB3AA3C4123) 만듭니다.
1. In the web property, click **[!UICONTROL Rules]** &gt; **[!UICONTROL Data Elements]**.
1. **[!UICONTROL 새 데이터 요소 만들기]**&#x200B;를 클릭합니다.
1. 다음 필드 및 옵션을 완료합니다. 

   <table id="choicetable_681F7D5B86534FF0B6DB67E117B8E381"> 
    <thead class="chhead sthead"> 
      <th class="choptionhd"> 옵션</th> 
      <th class="chdeschd"> 설명</th> 
    </thead> 
    <tr class="chrow strow"> 
      <td class="choption"><strong>이름</strong></td> 
      <td class="chdesc stentry"> <p>마케터가 알아볼 수 있는 데이터 요소의 친근한 이름입니다. 예를 들어 
        <code>
          제품 ID
        </code>. </p> <p> <p>참고: 규칙 빌더에서 참조하는 이름으로 ID가 아닙니다. 데이터 요소 이름을 변경할 경우 그를 사용하는 모든 규칙에서 참조를 변경해야 합니다. </p> </p> </td> 
    </tr> 
    <tr class="chrow strow"> 
      <td class="choption"><strong>유형</strong></td> 
      <td class="chdesc stentry"> <p> JS 개체, CSS 선택기, 쿠키, URL 매개 변수 또는 사용자 지정 스크립트와 같이 데이터를 가져오는 위치를 지정합니다. </p> <p>선택한 유형에 따라 다른 옵션이 표시됩니다. 자세한 내용 및 예제는 다이내믹 태그 관리 제품 설명서의 </a>데이터 요소 유형<a href="https://marketing.adobe.com/resources/help/en_US/dtm/data_elements.html" format="html" scope="external">을 참조하십시오. </a></p> </td> 
    </tr> 
    <tr class="chrow strow"> 
      <td class="choption"><strong>기본값</strong></td> 
      <td class="chdesc stentry"> <p>기본 요소입니다. 이 값은 URL 매개 변수가 없거나 다이내믹 태그 관리로 찾을 수 없을 경우에도 데이터 요소에는 값이 항상 있도록 해줍니다. </p> <p> <p>참고: 값 및 기본값이 없으면 아무런 결과도 반환되지 않습니다. 해당 데이터 요소를 참조하는 변수가 설정되지 않습니다. 또한 "사용자 지정 코드" 데이터 요소인 경우 기본값 필드가 무시됩니다. </p> </p> </td> 
    </tr> 
    <tr class="chrow strow"> 
      <td class="choption"><strong>소문자 강제 적용 값</strong> </td> 
      <td class="chdesc stentry"> <p>다이내믹 태그 관리가 값을 자동으로 소문자로 바꿉니다. </p> </td> 
    </tr> 
    <tr class="chrow strow"> 
      <td class="choption"><strong>다음 기간 동안 이 값 기억</strong></td> 
      <td class="chdesc stentry"> <p>다이내믹 태그 관리가 이 값을 기억해야 하는 기간입니다. </p> <p> 유효 값 항목: </p> 
      <ul id="ul_52F6CD8FC22942208F3F45492E914104"> 
        <li id="li_32E4366C5B2E46D788CD8478620FE3E0"> <p>세션: 세션 기반 시간 설정은 구현에 따라 달라질 수 있습니다. 세션 데이터 요소는 세션 쿠키로 설정됩니다. 하지만, 이 설정은 웹 서버 또는 브라우저를 기반으로 지정할 수도 있습니다. 마케팅 보고 및 분석에 사용된 세션과는 관련이 없습니다. </p> </li> 
        <li id="li_8A944564BF7643E4B21F0EF2394B3FE8"> <p>페이지 보기 </p> </li> 
        <li id="li_5C8A2F2392FD475AA89DDA7D5B5CF88B"> <p>방문자 </p> </li> 
      </ul> </td> 
    </tr> 
   </table>

   데이터 요소 사용 방법에 대한 자세한 내용은 Adobe 태그 관리 제품 설명서에서 [데이터 요소](https://marketing.adobe.com/resources/help/en_US/dtm/data_elements.html)를 참조하십시오.
1. **[!UICONTROL 데이터 요소 저장을 클릭합니다]**.
