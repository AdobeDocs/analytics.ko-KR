---
title: pageName
description: 사이트에 있는 페이지의 이름입니다.
translation-type: ht
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# pageName

`pageName` 변수는 일반적으로 주어진 페이지의 이름을 저장합니다. 이 변수는 가장 인기 있는 개별 페이지를 결정하는 데 유용합니다. 이 변수는 &#39;페이지 이름&#39; 차원을 채웁니다.

>[!NOTE] 이 차원은 항상 링크 추적 호출에서 제거됩니다. 링크가 추적된 페이지 이름을 보려면 이 변수를 eVar에 복사하는 것이 좋습니다.

이 변수가 주어진 페이지 추적 호출에 정의되어 있지 않은 경우 [`pageURL`](pageurl.md) 변수가 대신 사용됩니다.

## Adobe Experience Platform Launch의 페이지 이름

Analytics 확장(전역 변수)을 구성하는 동안 또는 규칙에서 페이지 이름을 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 규칙] 탭으로 이동한 다음, 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [!UICONTROL 작업]에서 기존 [!UICONTROL Adobe Analytics - 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. [!UICONTROL 확장] 드롭다운을 Adobe Analytics로 설정하고 [!UICONTROL 작업 유형]을 [!UICONTROL 변수 설정]으로 설정합니다.
6. [!UICONTROL 페이지 이름] 섹션을 찾습니다.

페이지 이름을 데이터 요소를 포함한 어떤 문자열 값으로든 설정할 수 있습니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.pageName

`s.pageName` 변수는 일반적으로 페이지 이름을 포함하는 문자열입니다. 이 변수의 값은 최대 100바이트이며 더 긴 값은 잘립니다. 이렇게 잘리게 되면 이 변수가 비어 있을 경우 다시 `pageURL`이 되는 인스턴스가 발생합니다.

```js
// Set page name to a static value
s.pageName = "Example page name";

// Set page name to the page's title
s.pageName = window.document.title;
```
