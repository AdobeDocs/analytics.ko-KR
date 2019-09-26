---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: 60dd1b300035e5149f53870239de85fb3174a77a

---



# s.doPlugins

 변수는 함수 참조로서, 이 변수를 사용하면 JavaScript 파일 내의 적절한 위치에서 함수를 호출할 수 있습니다.

The *`s_doPlugins`* function is called each time any of the following occurs:

* 이 *`t()`* 함수는
* 이 *`tl()`* 함수는
* 종료 또는 다운로드 링크를 클릭할 때
* 방문자 클릭 맵이 추적하는 페이지 요소를 클릭할 때

The *`doPlugins`*&#x200B;함수는 데이터를 모으거나 바꾸는 사용자 지정 루틴을 실행하는 데 사용됩니다. If you are using an object name other than "s," make sure that the *`s_doPlugins`* is renamed appropriately. 예를 들어 개체 이름이 s_mc인 경우 이 *`s_doPlugins`* 함수를 s_mc_doPlugins라고 해야 합니다.

## 구문 및 가능한 값

이 *`s_doPlugins`* 함수는 따옴표로 묶으면 안 되며, 항상 *`doPlugins`* *`s_doPlugins`* 함수의 정확한 이름(함수의 이름이 변경된 경우)에 할당되어야 합니다.

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

* 개체 이름을 변경(s에서 s_mc으로 변경하는 등)하는 유일한 이유는 컨텐츠를 다른 고객과 공유하거나 다른 고객의 컨텐츠를 가져오는 경우입니다. 이름 바꾸기 *`s_doPlugins`* function to [!UICONTROL s_mc_doPlugins] ensures that another client's JavaScript file does not overwrite your *`doPlugins`* function.

* 예기치 않게 다른 Adobe 고객의 컨텐츠를 가져오기 시작하고 *`s_doPlugins`* 기능을 덮어쓰는 경우 개체 이름을 변경하지 않고 간단하게 *`s_doPlugins`* 함수의 이름을 변경할 수 있습니다. 같은 페이지에서 다른 JavaScript 파일이 아닌 다른 개체 이름을 사용하는 것이 최고의 솔루션일 경우에는 그렇게 할 필요가 없습니다.