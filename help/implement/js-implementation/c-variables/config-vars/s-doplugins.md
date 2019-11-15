---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics Implementation
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---



# s.doPlugins

 변수는 함수 참조로서, 이 변수를 사용하면 JavaScript 파일 내의 적절한 위치에서 함수를 호출할 수 있습니다.

*`s_doPlugins`* 함수는 다음 중 하나가 발생할 때마다 호출됩니다.

* *`t()`* 함수가 호출될 때
* *`tl()`* 함수가 호출될 때
* 종료 또는 다운로드 링크를 클릭할 때
* 방문자 클릭 맵이 추적하는 페이지 요소를 클릭할 때

The *`doPlugins`*&#x200B;함수는 데이터를 모으거나 바꾸는 사용자 지정 루틴을 실행하는 데 사용됩니다. s 이외의 개체 이름을 사용하는 경우 *`s_doPlugins`*&#x200B;의 이름을 적절하게 다시 지정합니다. 예를 들어 개체 이름이 s_mc이면 *`s_doPlugins`* 함수를 called s_mc_doPlugins라고 해야 합니다.

## 구문 및 가능한 값

*`s_doPlugins`* 함수는 따옴표로 묶으면 안 되며, 항상 *`doPlugins`*&#x200B;를 항상 *`s_doPlugins`* 함수의 정확한 이름에 지정해야 합니다(함수의 이름이 변경된 경우).

```js
s.doPlugins=s_doPlugins;
```

## 예

```js
s.doPlugins=s_doPlugins;
```

```js
s_mc.doPlugins=s_mc_doPlugins;
```

## 구성 설정

없음

## 함정, 질문 및 팁

* 개체 이름을 변경(s에서 s_mc으로 변경하는 등)하는 유일한 이유는 컨텐츠를 다른 고객과 공유하거나 다른 고객의 컨텐츠를 가져오는 경우입니다. 이름 바꾸기 *`s_doPlugins`* 함수 이름을 [!UICONTROL s_mc_doPlugins]로 바꾸면 다른 클라이언트의 JavaScript 파일이 *`doPlugins`* 함수를 덮어쓰지 않습니다.

* 예기치 않게 다른 Adobe 고객의 콘텐츠를 가져와서 *`s_doPlugins`* 함수를 덮어쓰는 경우 개체 이름을 변경하지 않고 간단하게 *`s_doPlugins`* 함수의 이름을 변경할 수 있습니다. 같은 페이지에서 다른 JavaScript 파일이 아닌 다른 개체 이름을 사용하는 것이 최고의 솔루션일 경우에는 그렇게 할 필요가 없습니다.
