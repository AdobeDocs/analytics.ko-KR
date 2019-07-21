---
description: HTML 이미지 태그를 사용하여 Analytics를 구현합니다(하드코드된 이미지 요청).
keywords: Analytics 구현; HTML image tag; 하드코드된 이미지 요청
seo-description: HTML 이미지 태그를 사용하여 Analytics를 구현합니다(하드코드된 이미지 요청).
seo-title: HTML 이미지 태그를 사용하여 Analytics 구현
solution: Analytics
title: HTML 이미지 태그를 사용하여 Analytics 구현
topic: 개발자 및 구현
uuid: 0 C 098 A 57-7 C 71-4362-812 C -36 E 37848 A 5 AE
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# HTML 이미지 태그를 사용하여 Analytics 구현

HTML 이미지 태그를 사용하여 Analytics를 구현합니다(하드코드된 이미지 요청).

이렇게 되면 브라우저는 이미지를 요청합니다. 데이터는 이미지 요청 쿼리 문자열에서 변수를 통해 이 이미지 요청에 따라 이동합니다. JavaScript는 브라우저 수준 변수를 포괄적인 데이터 수집 솔루션을 위해 페이지 수준 변수와 결합합니다. 어떤 경우에는, 완전히 서버에서 만들어진 이미지 태그가 적절합니다. JavaScript 기반 구현의 표준 요소는 다음과 같습니다.

<table id="table_20BBE4387F234CF199E6C99741AF265C"> 
 <tbody> 
  <tr> 
   <td> HTML 코드 </td> 
   <td> 이 부분은 JavaScript 변수의 값을 설정하는 HTML 페이지(또는 템플릿)에 삽입된 JavaScript 코드로 구성됩니다. </td> 
  </tr> 
  <tr> 
   <td> JavaScript 라이브러리 </td> 
   <td> <p>이 파일에는 다음과 같은 일반적인 코드가 들어 있습니다. </p> 
    <ul id="ul_ED50D66F2B2B476E8D9063099995998D"> 
     <li id="li_E88F6F28EC8946469ADCEAFF2F0A4EBA">JavaScript 버전, OS 버전, 사용되는 모니터의 크기 및 해상도, 그리고 기타 변수와 같은 다양한 속성에 대해 쿼리하는 코드 </li> 
     <li id="li_5CEBE37709D943B7921447FA7054A565">모든 변수를 인코딩하고 이러한 변수를 데이터 수집 서버로 전송하는 이미지 요청(&lt;img&gt;)에 연결합니다. 그런 다음 JavaScript 라이브러리 파일을 참조하면 JavaScript 라이브러리 파일이 로드되어 실행됩니다. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> &lt;noscript&gt; 태그 </td> 
   <td> 사용자가 JavaScript를 비활성화했거나, 사용자에게 JavaScript 기능이 없을 경우 실행되는 &lt;noscript&gt; 태그 내에 단순화된 이미지 요청 버전을 삽입합니다. 이 구현 부분은 선택 사항으로서, 일반적으로 인터넷 사용 인구의 약 2%에 적용됩니다. </td> 
  </tr> 
 </tbody> 
</table>

JavaScript는 브라우저 창 높이/너비, 모니터 해상도 및 Netscape 플러그인과 같이, 서버에 사용할 수 없는 브라우저 설정을 감지할 수 있습니다. 이러한 변수들은 서버측 방법을 사용하여 이미지 태그를 만드는 것으로는 캡처할 수 없습니다. JavaScript는 브라우저 및 프록시 서버 캐싱을 극복하기 위해 이미지 요청에서 무작위 숫자를 설정합니다. 이렇게 하면 모든 페이지 보기를 정확하게 추적할 수 있습니다. 특정 상황에서는, 서버측 코드가 JavaScript 기반 코드에 비해 다음을 포함한 장점을 가집니다.

* JavaScript는 매우 정확합니다(98-100%). 사용자가 JavaScript를 실행하기 전에 다른 페이지를 재빨리 클릭하는 상황에서도 극도의 정확성이 요구될 때가 있습니다. 이미지 태그 서버측을 만들면 정확도 수준을 몇 퍼센트 증가시킵니다.
* 구입과 같이 정확성이 매우 중요한 전환 이벤트 추적에서 그렇습니다.
* 이 전략은 <noscript> Javascript가 없거나 javascript가 비활성화되어 있는 사용자를 추적하기 위한 태그입니다.

>[!NOTE]
>
>서버가 생성한 이미지 태그의 사용은 구현에 추가적인 시간이 필요하며, 디버그, 배포 및 유지 관리가 더 어렵습니다. Adobe에서는 클라이언트가 가능한 모든 페이지에서 JavaScript 기반 데이터를 사용할 것을 적극적으로 권장합니다. 방문자 클릭 맵, 다운로드 링크, 종료 링크 및 브라우저 기반 변수(브라우저 너비/높이 등)를 포함한, 다양한 보고서 및 기능은 이 구현 방법을 사용하여 모으거나 지원할 수 없습니다.

