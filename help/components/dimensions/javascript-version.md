---
title: JavaScript 버전
description: 방문자의 브라우저에서 지원하는 JavaScript 버전입니다.
feature: Dimensions
source-git-commit: a68e13c9232ef8d975fd1256168a0addf677f5ac
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 10%
---
# JavaScript 버전

&#39;JavaScript 버전&#39; [차원](overview.md)은(는) 방문자의 브라우저에서 지원하는 JavaScript 버전을 보고합니다. AppMeasurement 라이브러리의 버전은 보고하지 않습니다.

>[!IMPORTANT]
>
>이 차원은 Data Warehouse에서만 사용할 수 있습니다. 다른 Analytics 솔루션에서 JavaScript 버전을 사용하려면 모든 히트에서 값을 [eVar](evar.md)에 복사하는 것이 좋습니다.

## 이 차원을 데이터로 채우기

AppMeasurement은 브라우저에서 JavaScript 기능을 자동으로 감지하고 `j` 쿼리 문자열 매개 변수에서 버전 값을 보냅니다. 설정할 구현 변수가 없습니다. 이 감지는 기존 JavaScript 버전 레이블을 사용하지만 최신 ECMAScript 기능 지원에 대한 포괄적인 측정은 아닙니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | 없음(자동 수집됨) |
| **웹 SDK/XDM 필드** | [`environment.browserDetails.javaScriptVersion`](/help/implement/aep-edge/xdm-var-mapping.md) |
| **쿼리 매개 변수** | [`j`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **XML 태그** | [`<javaScriptVersion>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **대량 데이터 삽입 API 열** | [`javaScriptVersion`](https://developer.adobe.com/analytics-collection-apis/methods/bulk-data-insertion/column-reference) |
| **바이트 제한** | 5바이트 |
| **지속성** | 히트 |

## 차원 항목

Dimension 항목에는 `1.5` 및 `1.6`과(와) 같은 방문자의 브라우저에서 수집된 JavaScript 버전 값이 포함됩니다.
