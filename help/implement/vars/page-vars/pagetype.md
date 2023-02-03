---
title: pageType
description: 현재 페이지가 404 오류인지 판단합니다.
feature: Variables
exl-id: e61ef82d-b583-4230-b904-5ea3584910be
source-git-commit: 8a6c639af7427a9975ccd061d059696d4611dff3
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 56%

---

# pageType

`pageType` 변수는 404 오류와 같이 사이트에서 오류 페이지를 지정하는 데 사용되는 플래그입니다. 이 변수에 문자열이 포함되어 있으면 `errorPage`를 채우며 &#39;페이지를 찾을 수 없음&#39;을 표시합니다 [차원](/help/components/dimensions/pages-not-found.md) 및 [지표](/help/components/metrics/pages-not-found.md).

>[!IMPORTANT]
>
>오류가 아닌 페이지에서 이 변수를 설정하지 마십시오.

## 웹 SDK를 사용한 페이지 유형

페이지 유형: [Adobe Analytics용 매핑](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) XDM 필드 아래 `web.webPageDetails.isErrorPage`. 이 XDM 필드는 부울입니다. 설정 `true` 오류 페이지로 플래그를 지정하거나 `false` 오류 페이지가 아닌 경우 Adobe은 부울을 문자열 값으로 자동으로 변환합니다 `errorPage` analytics 보고서 세트로 전송됩니다.

## Adobe Analytics 확장을 사용한 페이지 유형

Adobe Analytics 확장에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 정의 코드 편집기를 사용하십시오.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.pageType

`s.pageType` 변수는 값 `errorPage`가 유일하게 유효한 값인 문자열입니다. 이 변수는 404 페이지처럼 사이트의 어떤 오류 페이지에서든 이 값으로 설정하십시오.

```js
s.pageType = "errorPage";
```

>[!TIP]
>
>방문자가 사이트에서 당면하는 특정 오류에 대한 자세한 정보를 사용자가 알 수 있도록 오류 코드를 수집하려면 eVar를 사용하십시오.
