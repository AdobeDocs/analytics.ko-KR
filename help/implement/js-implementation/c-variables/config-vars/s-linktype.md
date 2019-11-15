---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics Implementation
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: 21f278017472ae39c6066ca7694a5cdbbfde41f3

---


# s.linkType

자동으로 결정된 링크 유형이 들어 있습니다(있을 경우). 다음 중 하나로 설정할 수 있습니다.

    * 'd'(다운로드)
    * 'e'(종료)
    * 'o'(사용자 지정/기타)

이미지 요청의 `pe` 매개 변수입니다. If set with  [`linkURL`](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linkURL.html) or [`linkName`](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linkname.html), a server call is sent as a download, custom, or exit link.

*참고:각 링크 유형은 페이지 보기가 아니며 연결된 페이지 이름이 없으므로 파일 다운로드, 종료 링크 또는 사용자 지정 링크에 대해 변수를 설정할 수[`pageName`](https://docs.adobe.com/content/help/en/analytics/implementation/testing-and-validation/optimize-implementation/page-naming-strategies.html)없습니다.*


**예**

```js
function s_doPlugins(s) { 
    if (s.linkType == "d" && s.linkURL.indexOf(".aspx?f=") { 
        //special tracking for .aspx file download script 
        s.eVar11 = s.linkURL.substring(s.linkURL.lastIndexOf("?f=") + 3, s.linkURL.length); 
    } 
  
    else if (s.linkType == "o" ) { 
        // note: linkType is set to "o" only if you make a custom call 
        // to s.tl() and set the link type to "o". Automatically tracked 
        // links are set to "d" or "e" only. 
        s.eVar10 = s.LinkURL; 
    } 
}
```
