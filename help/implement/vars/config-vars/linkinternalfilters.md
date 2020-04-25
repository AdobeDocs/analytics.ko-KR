---
title: linkInternalFilters
description: linkInternalFilters 변수를 사용하여 자동 종료 링크 추적을 돕습니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# linkInternalFilters

AppMeasurement는 사이트 외부를 가리키는 링크를 자동으로 추적하는 기능을 제공합니다. If [`trackExternalLinks`](trackexternallinks.md) is enabled, an image request is sent to Adobe right as a visitor clicks a link to leave your site. [`linkExternalFilters`](linkexternalfilters.md) 및 `linkInternalFilters` 변수는 내부/외부로 간주되는 링크를 파악합니다.

이 변수에 값이 있으면 자동 종료 링크 추적은 블랙리스트와 같은 방식으로 동작합니다. 링크 클릭이 `linkInternalFilters` 값과 일치하지 않으면 종료 링크로 간주됩니다. 전체 URL은 이 변수에 따라 검사됩니다. If [`linkLeaveQueryString`](linkleavequerystring.md) is enabled, the query string is also examined.

`linkInternalFilters`와 `linkExternalFilters`를 동시에 사용하는 경우 클릭한 링크는 `linkExternalFilters`를 **만족하고** 종료 링크로 간주되는 `linkInternalFilters`는 만족하지 않아야 합니다. 클릭한 링크가 종료 링크와 다운로드 링크 기준을 모두 만족하는 경우에는 다운로드 링크 유형이 우선합니다.

>[!NOTE] `linkInternalFilters`[](/help/admin/admin/internal-url-filter-admin.md)와 내부 URL 필터는 별개의 목적을 수행하는 별개의 기능입니다. `linkInternalFilters` 변수는 특히 종료 링크 추적에 작동합니다. 내부 URL 필터는 참조 도메인같은 트래픽 소스 차원에 도움이 되는 관리 설정입니다.

## Adobe Experience Platform Launch의 아웃바운드 링크 - 추적 안 함

추적 안 함 필드는 Adobe Analytics 확장을 구성할 때 [!UICONTROL 링크 추적] 아코디언 아래에 있는 쉼표로 구분된 필터 목록(일반적으로 도메인)입니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 [!UICONTROL 구성] 단추를 클릭합니다.
4. [!UICONTROL 링크 추적] 아코디언을 확장합니다. 그러면 [!UICONTROL 아웃바운드 링크 - 추적 안 함] 필드가 표시됩니다.

이 필드에는 종료 링크로 추적하지 않을 필터를 배치하십시오. 여러 도메인은 공백 없이 쉼표로 구분합니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.linkInternalFilters

`s.linkInternalFilters` 변수는 사이트 내부로 간주하는 필터(예: 도메인)가 포함된 문자열입니다. 여러 필터는 공백 없이 쉼표로 구분하십시오.

```js
s.linkInternalFilters = "example.com,example.net,example.org";
```

다음 구현 예를 `adobe.com`에 있는 것처럼 간주하십시오.

```html
<script>
  s.trackExternalLinks = true;
  s.linkInternalFilters = "adobe.com";
</script>

<!-- The following link is an exit link because it does not match the anything under linkInternalFilters -->
<a href = "example.com">Example link 2</a>
```
