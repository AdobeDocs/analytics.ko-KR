---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# s.currencyCode

 변수는 매출에 적용할 전환율을 결정합니다.

모든 금액은 선택한 통화로 저장됩니다. 해당 통화가 *`currencyCode`*&#x200B;에 지정된 통화와 동일하거나 *`currencyCode`*&#x200B;가 비어 있는 경우 전환이 적용되지 않습니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|--- |--- |--- |--- |
| N/A | cc | 전환 &gt; 구매 &gt; 매출 매출이나 통화 가치를 보여 주는 모든 전환 보고서 | "USD" |

사이트에서 방문자가 여러 통화로 구매할 수 있는 경우, *`currencyCode`* 변수를 사용하여 매출이 적절한 통화로 저장되었는지 확인해야 합니다. 예를 들어 보고서 세트에 대한 기본 통화가 USD이고 한 품목을 40유로에 파는 경우 HTML 페이지에서 *`currencyCode`*&#x200B;를 "EUR"로 채워야 합니다. 데이터 수집에서는 데이터를 받자마자 현재 전환율을 사용하여 40유로를 해당 USD로 전환합니다.

여러 통화로 판매하는 경우에는 JavaScript 파일 대신 HTML 페이지에서 *`currencyCode`* 변수를 채우는 것이 좋습니다. Adobe에서 사용하는 전환율 대신 사용자의 전환율을 사용하려면 *`currencyCode`*&#x200B;를 보고서 세트의 기본 통화와 동일하게 설정합니다. 그런 다음 모든 매출을 [!DNL Analytics]로 보내기 전에 전환합니다.

통화 전환은 매출과 모든 통화 이벤트 모두에 적용됩니다. 이러한 이벤트들은 세금이나 배송과 같이, 매출과 유사한 값들을 합하는 데 사용되는 이벤트입니다. 매출 및 통화 이벤트는 제품 문자열에서 지정됩니다. 제품에 대한 자세한 내용은 [events](https://docs.adobe.com/content/help/en/analytics/implementation/analytics-basics/ref-events.html).

## 구문 및 가능한 값

```js
s.currencyCode="currency_code"
```

## 예

```js
s.currencyCode="GBP"
```

```js
s.currencyCode="EUR"
```

## 구성 설정

Adobe [!DNL Customer Care]에서는 보고서 세트에 대한 기본 통화 설정을 변경할 수 있습니다. 보고서 세트에 대한 기본 통화를 변경할 경우, 시스템에 있는 기존 매출은 전환되지 않습니다. 모든 새 매출액은 변경된 설정에 따라 전환됩니다.

## 함정, 질문 및 팁

* 보고서에서 확인한 매출액이 대단히 많은 경우 보고서 세트의 *`currencyCode`* 변수와 기본 통화가 올바르게 설정되었는지 확인하십시오.
* *`currencyCode`* 변수는 지속적이지 않습니다. 즉, 매출이나 다른 통화 관련 지표와 동일한 이미지 요청에서 이 변수를 전달해야 합니다.
* 통화 이벤트는 비통화 목적으로는 사용하면 안 됩니다. 통화가 아닌 임의의 또는 동적인 값을 계산해야 하는 경우에는 [!UICONTROL 숫자] 이벤트 유형을 사용하십시오.
* When the *`currencyCode`* 변수가 비어 있으면, 전환이 적용되지 않습니다.

자세한 내용은 통화 [코드를 참조하십시오](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/currency.html).
