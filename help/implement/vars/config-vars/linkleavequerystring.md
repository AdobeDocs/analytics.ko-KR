---
title: linkLeaveQueryString
description: 링크 추적 차원에 쿼리 문자열을 유지할 수 있습니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# linkLeaveQueryString

AppMeasurement는 기본적으로 링크 추적 URL에서 쿼리 문자열을 제거합니다. 이 `linkLeaveQueryString` 변수를 사용하여 링크 추적 차원의 쿼리 문자열을 유지합니다.

일부 종료 링크 및 다운로드 링크의 경우 URL의 중요한 부분은 쿼리 문자열에 있을 수 있습니다. 예를 들어, 쿼리 문자열에 중요한 링크 정보가 `https://example.com/download.asp?filename=myfile.exe` 포함된 다운로드 링크가 있습니다.

링크 추적 정보가 사이트의 URL에 없는 경우 이 변수를 사용할 필요가 없습니다. 링크 추적 URL에서 쿼리 문자열을 제거하면 차원에 포함된 고유한 값의 수를 제한할 수 있습니다.

활성화는 모든 링크 추적 차원에 `linkLeaveQueryString` 적용됩니다(사용자 지정 링크, 종료 링크 및 다운로드 링크 포함).

> [!TIP] 이 변수는 링크 추적 외부의 차원에는 영향을 주지 않습니다. 사용자 지정 링크, 종료 링크 및 다운로드 링크에만 영향을 줍니다.

## Adobe Experience Platform Launch에서 URL 매개 변수 유지

[!UICONTROL Keep URL Parameters] 는 Adobe Analytics 확장을 구성할 때 [!UICONTROL Link Tracking] 아코디언 아래에 있는 확인란입니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 탭으로 이동한 [!UICONTROL Extensions] 다음 Adobe Analytics 아래의 [!UICONTROL Configure] 단추를 클릭합니다.
4. 확인란을 표시하는 [!UICONTROL Link Tracking] 아코디언을 [!UICONTROL Keep URL Parameters] 확장합니다.

링크 추적 차원에 쿼리 문자열을 포함하려면 이 상자를 선택합니다.

## s.linkLeaveQueryString in AppMeasurement 및 Launch 사용자 지정 코드 편집기

이 `s.linkLeaveQueryString` 변수는 부울입니다. Its default value is `false`.

* 이 변수가 로 설정된 `true`경우 쿼리 문자열은 링크 추적 URL에 유지됩니다.
* 이 변수가 정의되지 `false` 않았거나 설정된 경우 쿼리 문자열은 링크 추적 URL에서 제거됩니다.

```js
s.linkLeaveQueryString = true;
```

## 예

이 변수는 [`linkInternalFilters`](linkinternalfilters.md), [`linkExternalFilters`](linkexternalfilters.md)및 [`linkDownloadFiletypes`](linkdownloadfiletypes.md)같은 링크 추적 필터에 영향을 줄 수 있으므로 이 변수를 true로 설정할 때는 주의하십시오.

다음 예를 켜진 것처럼 `adobe.com`생각해 보십시오.

```html
<script>
  s.linkInternalFilters = "adobe.com";
  s.linkLeaveQueryString = true;
</script>

<!--This link is not an exit link because the internal filter matches part of the query string -->
<a href = "example.com?r=adobe.com">Example link</a>
```
