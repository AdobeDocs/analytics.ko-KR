---
title: ActivityMap.link
description: Activity Map에서 클릭한 링크를 수집하는 방법을 사용자 지정합니다.
feature: Appmeasurement Implementation
role: Admin, Developer
exl-id: 3a31f80b-dbee-4a45-ac3c-0b8ca198c95a
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 9%

---

# ActivityMap.link

`ActivityMap.link` 변수를 사용하면 Activity Map에서 링크 값을 설정하는 데 사용하는 논리를 재정의할 수 있습니다. 이 변수는 [`ActivityMap.linkExclusions`](../config-vars/activitymap-linkexclusions.md)에서 제공하는 것보다 더 많은 컨트롤을 원하는 영역에서 유용합니다.

>[!CAUTION]
>이 변수는 Activity Map 논리를 완전히 무시합니다. 여기서 잘못된 값을 반환하는 재정의 함수를 설정하면 Activity Map 차원 및 Activity Map 오버레이에 데이터 수집 문제가 발생할 수 있습니다.

## 웹 SDK을 사용하여 링크 값 재정의

[`OnBeforeLinkClickSend`](https://experienceleague.adobe.com/ko/docs/experience-platform/web-sdk/commands/configure/onbeforelinkclicksend) 콜백을 사용하여 웹 SDK 페이로드를 변경하거나 데이터 전송을 중단할 수 있습니다.

## Adobe Analytics 확장을 사용한 링크 재정의

Adobe Analytics 확장에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 정의 코드 편집기를 사용하십시오.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 ActivityMap.link

이 변수에 다음과 같은 함수를 지정합니다.

* 클릭한 HTML 요소를 받습니다.
* 문자열 값을 반환합니다. 이 문자열 값은 [Activity Map 링크](/help/components/dimensions/activity-map-link.md) 차원에 사용되는 최종 값입니다.

반환 값이 [falsy](https://developer.mozilla.org/ko-KR/docs/Glossary/Falsy)이면 모든 Activity Map 컨텍스트 데이터 변수가 지워지고 링크 데이터가 추적되지 않습니다.

## 예

`<a>` 태그의 제목 특성만 사용하십시오. 제목 속성이 없으면 링크가 추적되지 않습니다.

```js
s.ActivityMap.link = function(clickedElement) {
  var linkId;
  if (clickedElement && clickedElement.tagName.toUpperCase() === 'A') {
    linkId = clickedElement.getAttribute('title');
  }
  return linkId;
}
```

`s.tl`에 수동으로 설정된 링크 이름이 있으면 이를 반환하고, 그렇지 않으면 링크 URL을 반환합니다.

```js
s.ActivityMap.link = function(ele, linkName) {
  if (linkName) {
    return linkName;
  }
  if (ele && ele.tagName == 'A' && ele.href) {
    return ele.href;
  }
}
```

기본 링크 논리를 완전히 대체하는 대신 조건부로 변경할 수 있습니다.

```html
<script>
  // Copy the original link function
  var originalLinkFunction = s.ActivityMap.link;
  // Return the link name from s.tl, a modified activity map value, or the original activity map value
  s.ActivityMap.link = function(element,linkName)
  {
    return linkName || customFunction(element) || originalLinkFunction(element,linkName);
  };
</script>

<button type="button" onclick="s.tl(this,'o',customFunction(this)">Add To Cart</button>
```

1. `linkName`이(가) 전달되면 `tl()`에 의해 메서드가 호출됩니다. `linkName`(으)로 전달된 `tl()`을(를) 반환합니다.
2. Activity Map에서 호출하는 경우 `linkName`이(가) 전달되지 않으므로 링크 요소를 사용하여 `customFunction()`을(를) 호출하십시오. 값을 반환하려는 사용자 지정 함수를 사용할 수 있습니다.
3. 위의 반환 값이 모두 아닌 경우 일반적으로 수집된 링크 이름을 대체 항목으로 사용하십시오.
