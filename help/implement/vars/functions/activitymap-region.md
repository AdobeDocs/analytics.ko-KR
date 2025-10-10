---
title: ActivityMap.region
description: Activity Map에서 클릭한 영역을 수집하는 방법을 사용자 지정합니다.
feature: Appmeasurement Implementation
role: Admin, Developer
exl-id: 9bbdb124-b865-4431-8a98-9814c3f2e65c
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 13%

---

# ActivityMap.region

`ActivityMap.region` 변수를 사용하면 Activity Map에서 지역 값을 설정하는 데 사용하는 논리를 재정의할 수 있습니다. 이 변수는 [`ActivityMap.regionExclusions`](../config-vars/activitymap-regionexclusions.md)에서 제공하는 것보다 더 많은 컨트롤을 원하는 영역에서 유용합니다.

>[!CAUTION]
>이 변수는 Activity Map 논리를 완전히 무시합니다. 여기서 잘못된 값을 반환하는 재정의 함수를 설정하면 Activity Map 차원 및 Activity Map 오버레이에 데이터 수집 문제가 발생할 수 있습니다.

## 웹 SDK을 사용하여 영역 값 재정의

[`OnBeforeLinkClickSend`](https://experienceleague.adobe.com/ko/docs/experience-platform/web-sdk/commands/configure/onbeforelinkclicksend) 콜백을 사용하여 웹 SDK 페이로드를 변경하거나 데이터 전송을 중단할 수 있습니다.

## Adobe Analytics 확장을 사용한 영역 재정의

Adobe Analytics 확장에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 정의 코드 편집기를 사용하십시오.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 ActivityMap.region

이 변수에 다음과 같은 함수를 지정합니다.

* 클릭한 HTML 요소를 받습니다.
* 문자열 값을 반환합니다. 이 문자열 값은 [Activity Map 지역](/help/components/dimensions/activity-map-region.md) 차원에 사용되는 최종 값입니다.

반환 값이 [falsy](https://developer.mozilla.org/ko-KR/docs/Glossary/Falsy)이면 모든 Activity Map 컨텍스트 데이터 변수가 지워지고 링크 데이터가 추적되지 않습니다.

## 예

소문자 태그 이름을 영역으로 사용:

```js
s.ActivityMap.region = function(clickedElement) {
  while (clickedElement && (clickedElement = clickedElement.parentNode)) {
    var regionId = clickedElement.tagName;
    if (regionId) {
      return regionId.toLowerCase();
    }
  }
}
```

원하는 특정 클래스 이름을 영역으로 사용:

```js
s.ActivityMap.region = function(ele) {
  var className,
  classNames = {
    'header': 1,
    'navbar': 1,
    'left-content': 1,
    'main-content': 1,
    'footer': 1,
  };
  while ((ele && (ele = ele.parentNode))) {
    if ((className = ele.className)) {
      let classes = className.split(' ');
      for (let i = 0; i < classes.length; i++) {
        if (classNames[classes[i]]) {
          return classes[i];
        }
      }
    }
  }
  return "BODY";
}
```
