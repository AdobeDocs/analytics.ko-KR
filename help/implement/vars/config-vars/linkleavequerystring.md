---
title: linkLeaveQueryString
description: 링크 추적 차원에 쿼리 문자열을 유지할 수 있습니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# linkLeaveQueryString

AppMeasurement는 기본적으로 링크 추적 URL에서 쿼리 문자열을 제거합니다. Use the `linkLeaveQueryString` variable to preserve query strings in link tracking dimensions.

일부 종료 링크 및 다운로드 링크의 경우 URL의 중요한 부분이 쿼리 문자열에 있을 수 있습니다. 예를 들어, `https://example.com/download.asp?filename=myfile.exe`와 같은 다운로드 링크의 쿼리 문자열에는 중요한 링크 정보가 들어 있습니다.

링크 추적 정보가 사이트의 URL에 없는 경우에는 이 변수를 사용할 필요가 없습니다. 링크 추적 URL에서 쿼리 문자열을 제거하는 것은 차원에 포함된 고유한 값의 수를 제한하는 데 도움이 됩니다.

`linkLeaveQueryString` 활성화는 모든 링크 추적 차원(사용자 지정 링크, 종료 링크 및 다운로드 링크 포함)에 적용됩니다.

>[!TIP] 이 변수는 링크 추적 외부의 차원에는 영향을 주지 않고, 사용자 지정 링크, 종료 링크 및 다운로드 링크에만 영향을 줍니다.

## Adobe Experience Platform Launch에서 URL 매개 변수 유지

[!UICONTROL URL 매개 변수 유지]는 Adobe Analytics 확장을 구성할 때 [!UICONTROL 링크 추적] 아코디언 아래에 있는 확인란입니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 [!UICONTROL 구성] 단추를 클릭합니다.
4. [!UICONTROL 링크 추적] 아코디언을 확장합니다. 그러면 [!UICONTROL URL 매개 변수 유지] 확인란이 표시됩니다.

링크 추적 차원에 쿼리 문자열을 포함하려면 이 확인란을 선택하십시오.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.linkLeaveQueryString

`s.linkLeaveQueryString` 변수는 부울입니다. 기본값은 `false`입니다.

* 이 변수가 `true`로 설정되어 있으면 쿼리 문자열이 링크 추적 URL에서 유지됩니다.
* 이 변수가 `false`로 설정되어 있거나 정의되어 있지 않으면 쿼리 문자열이 링크 추적 URL에서 제거됩니다.

```js
s.linkLeaveQueryString = true;
```

## 예

이 변수는 [`linkInternalFilters`](linkinternalfilters.md), [`linkExternalFilters`](linkexternalfilters.md) 및 [`linkDownloadFiletypes`](linkdownloadfiletypes.md)같은 링크 추적 필터에 영향을 줄 수 있으므로 이 변수를 true로 설정할 때에는 주의하십시오.

다음 예를 `adobe.com`에 있는 것처럼 간주하십시오.

```html
<script>
  s.linkInternalFilters = "adobe.com";
  s.linkLeaveQueryString = true;
</script>

<!--This link is not an exit link because the internal filter matches part of the query string -->
<a href = "example.com?r=adobe.com">Example link</a>
```
