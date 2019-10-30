---
description: 페이지 로드 시간을 10분의 1초 단위로 파악하고 값을 prop, eVar 및/또는 숫자 이벤트로 저장할 수 있습니다.
keywords: Analytics 구현
seo-description: 페이지 로드 시간을 10분의 1초 단위로 파악하고 값을 prop, eVar 및/또는 숫자 이벤트로 저장할 수 있습니다.
seo-title: getLoadTime
solution: Analytics
title: getLoadTime
topic: 개발자 및 구현
uuid: 5d26a69b-cbde-4be1-bac1-5ee8a4e55ca3
translation-type: ht
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# getLoadTime

페이지 로드 시간을 10분의 1초 단위로 파악하고 값을 prop, eVar 및/또는 숫자 이벤트로 저장할 수 있습니다.

이 플러그인을 사용하려면 함수 코드를 삽입한 후 [!DNL s_code.js] 파일에서 함수를 두 번 호출합니다. 파일 시작 부분에서 한 번 호출하고 `doPlugins` 섹션에서 다시 한 번 호출합니다. 이 플러그인은 의도적으로 s 개체의 방법으로 정의되지 않았습니다. 그렇게 한다면 페이지 로드 시간 계산에 추가될 것입니다.

>[!NOTE]
>
>다음 지침을 따르려면 사이트에서 데이터 수집 코드를 변경해야 합니다. 이 작업은 사이트의 데이터 수집에 영향을 줄 수 있으며 [!DNL Analytics] 사용 및 구현 경험이 풍부한 개발자가 수행해야만 합니다.

## 플러그인 코드 및 구현 {#section_968AC379C3004C359A85AFED5A48D5AE}

**함수 추가**

`s_getLoadTime` 함수에 대한 다음 정의를 [!DNL s_code.js]에서 모든 "DO NOT ALTER ANYTHING BELOW THIS LINE" 섹션 앞에 추가합니다.

```js
function s_getLoadTime(){if(!window.s_loadT){var b=new Date().getTime(),o=window.performance?performance.timing:0,a=o?o.requestStart:window.inHeadTS||0;s_loadT=a?Math.round((b-a)/100):''}return s_loadT}
```

**초기 함수 호출 만들기**

`s_getLoadTime()`에 대한 호출을 함수 바깥의 [!DNL s_code.js] 시작 부분 근처에 추가합니다.

**최종 함수 호출 만들기**

`s_getLoadTime()`에 대한 다른 호출을 `s_doPlugins()` 함수에 추가하여 반환된 값을 prop, eVar 및/또는 숫자 이벤트에 저장합니다.

사용 예제 1 - prop10 및 eVar20의 페이지 로드 시간 저장:

```js
s.eVar20=s.prop10=s_getLoadTime();
```

사용 예제 2 - 페이지 로드 시간을 숫자 이벤트로 저장99:

```js
if(s_getLoadTime())s.events=s.apl(s.events,'event90='+s_getLoadTime(),',',1);
```

**(선택 사항) 오래된 브라우저에 대한 지원 추가**

[window.performance.timing](https://www.html5rocks.com/ko/tutorials/webperformance/basics/) 속성을 제공하지 않는 오래된 브라우저를 지원하려면 페이지 HTML의 시작 부분의 HEAD 섹션과 .js, .css 또는 다른 파일 호출 앞에 다음 라인을 추가합니다.

```
<script type="text/javascript">var inHeadTS=(new Date()).getTime();</script>
```

