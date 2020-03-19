---
title: linkInternalFilters
description: linkInternalFilters 변수를 사용하여 자동 종료 링크 추적을 돕습니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# linkInternalFilters

AppMeasurement는 사이트 외부의 링크를 자동으로 추적하는 기능을 제공합니다. 이 [`trackExternalLinks`](trackexternallinks.md) 옵션이 활성화되어 있으면 방문자가 링크를 클릭하여 사이트를 떠날 때 이미지 요청이 Adobe로 바로 전송됩니다. 및 [`linkExternalFilters`](linkexternalfilters.md) `linkInternalFilters` 변수는 내부/외부 링크로 간주되는 링크를 결정합니다.

이 변수에 값이 포함되어 있으면 자동 종료 링크 추적은 블랙 리스트 같은 방식으로 동작합니다. 링크 클릭이 `linkInternalFilters` 값과 일치하지 않으면 종료 링크로 간주됩니다. 이 변수에 대해 전체 URL이 검사됩니다. 이 [`linkLeaveQueryString`](linkleavequerystring.md) 옵션이 활성화되어 있으면 쿼리 문자열도 검사됩니다.

동시에 `linkInternalFilters` 사용하는 경우 클릭한 링크가 `linkExternalFilters` 일치해야 하고 `linkExternalFilters` 종료 링크로 **** `linkInternalFilters` 간주되지 않습니다. 클릭한 링크가 종료 링크와 다운로드 링크 기준을 모두 만족하는 경우 다운로드 링크 유형이 우선순위가 지정됩니다.

> [!NOTE] 및 `linkInternalFilters` 내부 URL [필터는](/help/admin/admin/internal-url-filter-admin.md) 별도의 목적을 수행하는 별도의 기능입니다. 이 `linkInternalFilters` 변수는 종료 링크 추적에 특히 작동합니다. 내부 URL 필터는 참조 도메인과 같은 트래픽 소스 차원에 도움이 되는 관리 설정입니다.

## 아웃바운드 링크 - Adobe Experience Platform 실행에서 추적 안 함

추적 안 함 필드는 Adobe Analytics 확장 기능을 구성할 때 [!UICONTROL Link Tracking] 아코디언 아래에 쉼표로 구분된 필터(일반적으로 도메인) 목록입니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 탭으로 이동한 [!UICONTROL Extensions] 다음 Adobe Analytics 아래의 [!UICONTROL Configure] 단추를 클릭합니다.
4. 필드를 나타내는 [!UICONTROL Link Tracking] [!UICONTROL Outbound Links - Never Track] 아코디언을 확장합니다.

이 필드에 종료 링크로 추적하지 않을 필터를 배치합니다. 공백 없이 여러 도메인을 쉼표로 구분합니다.

## s.linkInternalFilters in AppMeasurement and Launch 사용자 지정 코드 편집기

이 `s.linkInternalFilters` 변수는 사이트 내부로 간주하는 필터(예: 도메인)가 포함된 문자열입니다. 공백 없이 쉼표를 사용하여 여러 필터를 구분합니다.

```js
s.linkInternalFilters = "example.com,example.net,example.org";
```

다음 구현 예를 설정 `adobe.com`그대로 고려하십시오.

```html
<script>
  s.trackExternalLinks = true;
  s.linkInternalFilters = "adobe.com";
</script>

<!-- The following link is an exit link because it does not match the anything under linkInternalFilters -->
<a href = "example.com">Example link 2</a>
```
