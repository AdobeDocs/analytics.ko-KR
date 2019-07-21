---
description: 페이지 로드 시간을 10분의 1초 단위로 파악하고 값을 prop, eVar 및/또는 숫자 이벤트로 저장할 수 있습니다.
keywords: Analytics 구현
seo-description: 페이지 로드 시간을 10분의 1초 단위로 파악하고 값을 prop, eVar 및/또는 숫자 이벤트로 저장할 수 있습니다.
seo-title: getLoadTime
solution: Analytics
title: getLoadTime
topic: 개발자 및 구현
uuid: 5 d 26 a 69 b-cbde -4 be 1-bac 1-5 ee 8 a 4 e 55 ca 3
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# getLoadTime

페이지 로드 시간을 10분의 1초 단위로 파악하고 값을 prop, eVar 및/또는 숫자 이벤트로 저장할 수 있습니다.

이 플러그인을 사용하려면 함수 코드를 삽입한 후 [!DNL s_code.js] 파일에서 함수를 두 번 호출합니다. Once at the beginning of the file, and then again in the `doPlugins` section. 이 플러그인은 의도적으로 s 개체의 방법으로 정의되지 않았습니다. 그렇게 한다면 페이지 로드 시간 계산에 추가될 것입니다.

>[!NOTE]
>
>다음 지침을 따르면 사이트에서 데이터 수집 코드를 수정해야 합니다. 이 작업은 사이트의 데이터 수집에 영향을 줄 수 있으며 [!DNL Analytics] 사용 및 구현 경험이 풍부한 개발자가 수행해야만 합니다.

## 플러그인 코드 및 구현 {#section_968AC379C3004C359A85AFED5A48D5AE}

**함수 추가**

`s_getLoadTime` 함수에 대한 다음 정의를 [!DNL s_code.js]에서 모든 "DO NOT ALTER ANYTHING BELOW THIS LINE" 섹션 앞에 추가합니다.

```js
function s_getLoadTime(){if(!window.s_loadT){var b=new Date().getTime(),o=window.performance?performance.timing:0,a=o?o.requestStart:window.inHeadTS||0;s_loadT=a?Math.round((b-a)/100):''}return s_loadT}
```

**초기 함수 호출 만들기**

Add a call to `s_getLoadTime()` near the beginning of [!DNL s_code.js], outside of any function.

**최종 함수 호출 만들기**

Add another call to `s_getLoadTime()` in the `s_doPlugins()` function, saving the returned value in a prop, eVar, and/or a numeric event.

사용 예제 1 - prop10 및 eVar20의 페이지 로드 시간 저장:

```js
s.eVar20=s.prop10=s_getLoadTime();
```

사용 예제 2 - 페이지 로드 시간을 숫자 이벤트로 저장99:

```js
if(s_getLoadTime())s.events=s.apl(s.events,'event90='+s_getLoadTime(),',',1);
```

**(선택 사항) 오래된 브라우저에 대한 지원 추가**

[window.performance.timing](https://www.html5rocks.com/en/tutorials/webperformance/basics/) 속성을 제공하지 않는 오래된 브라우저를 지원하려면 페이지 HTML의 시작 부분과 .js, .css 또는 다른 파일 호출 앞의 HEAD 섹션에 다음 라인을 추가합니다.

```
<script type="text/javascript">var inHeadTS=(new Date()).getTime();</script>
```

