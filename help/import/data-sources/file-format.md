---
title: 데이터 소스 파일 형식
description: 데이터 소스에 사용할 파일을 올바르게 생성합니다.
source-git-commit: bb3036380eeec9b7a868f60a4c9076f2b772532b
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 7%

---

# 데이터 소스 파일 형식

데이터 소스 파일에는 다음 속성이 있습니다.

* 파일이 `.txt` 형식 지정
* 주석 처리된 줄이 &#39;`#`&#39; 및 는 선택 사항입니다.
* 주석이 없는 첫 번째 줄에는 파일의 헤더가 포함되어 있습니다.
* 모든 행의 첫 번째 값은 형식을 사용하는 날짜입니다 `MM/DD/YYYY` 또는 `MM/DD/YYYY/HH/mm/SS`.
* 머리글을 포함하여 모든 행의 값은 탭으로 구분됩니다.
* 모든 행에는 하나 이상의 차원과 지표가 있어야 합니다.

## 댓글

&#39;`#`&#39; 는 주석입니다. 데이터 소스 템플릿 파일을 다운로드할 때 처음 두 줄은 주석입니다.

* 첫 번째 주석은 데이터 소스에 대해 구성한 템플릿의 유형, 데이터 소스를 만든 백엔드 사용자 ID 및 데이터 소스 ID를 나타냅니다.
* 두 번째 주석에서는 템플릿 파일에 포함된 각 헤더에 대해 친숙한 이름을 제공합니다.

파일이 처리되면 Adobe에서 모든 주석 행을 무시하므로 템플릿 주석을 제거하거나 파일 전체에 직접 추가할 수 있습니다. 전체 행만 주석 처리할 수 있습니다. 개별 필드 또는 부분 행에 주석을 달 수 없습니다.

## 헤더

데이터 소스 파일을 업로드할 때 열 헤더가 필요합니다. 이러한 열 헤더는 대/소문자를 구분하지 않지만, 필요한 공백이 필요합니다(예: `eVar1` 은 잘못된 헤더이며, `EVAR 1` 가 유효합니다. 열 헤더는 모든 보고서 세트에 적용됩니다. 다음 표를 사용하여 데이터 소스 파일의 각 헤더가 올바로 설정되었는지 확인하십시오.

>[!TIP]
>
>데이터 소스 파일에 올바른 헤더를 포함하는 경우 데이터 소스 파일을 처음부터 새로 만들 수 있습니다. 단일 파일 내에 포함할 수 있는 헤더 수에는 제한이 없습니다. 그러나 각 행에는 최대 4096바이트만 사용할 수 있습니다.

| 차원 | 데이터 소스 헤더 |
| --- | --- |
| [범주](/help/components/dimensions/category.md) | `Category` |
| [eVar1 - eVar 250](/help/components/dimensions/evar.md) | `Evar 1` - `Evar 250` |
| [마케팅 채널](/help/components/dimensions/marketing-channel.md) | `Marketing Channel` |
| [마케팅 채널 세부 정보](/help/components/dimensions/marketing-detail.md) | `Marketing Channel Detail` |
| [제품](/help/components/dimensions/product.md) | `Product` |
| [추적 코드](/help/components/dimensions/tracking-code.md) | `Tracking Code` |
| [거래 ID](/help/implement/vars/page-vars/transactionid.md) | `transactionID` |
| [우편 번호](/help/components/dimensions/zip-code.md) | `Zip` |

{style="table-layout:auto"}

Dimension 및 지표는 동일한 헤더 행으로 이동합니다.

| 지표 | 데이터 소스 헤더 |
| --- | --- |
| [장바구니 추가](/help/components/metrics/cart-additions.md) | `Cart Adds` |
| [장바구니 제거](/help/components/metrics/cart-removals.md) | `Cart Removes` |
| [장바구니 보기](/help/components/metrics/cart-views.md) | `Cart Views` |
| [장바구니](/help/components/metrics/carts.md) | `Cart Opens` |
| [체크아웃](/help/components/metrics/checkouts.md) | `Checkouts` |
| [사용자 지정 이벤트](/help/components/metrics/custom-events.md) | `Event 1` - `Event 1000` |
| [주문](/help/components/metrics/orders.md) | `Orders` |
| [매출 ](/help/components/metrics/revenue.md) | `Price` |
| [판매량](/help/components/metrics/units.md) | `Quantity` |

{style="table-layout:auto"}

Adobe은 다른 차원이나 지표에 대한 데이터 소스를 지원하지 않습니다. 위의 표에 나열된 변수 이외의 변수가 필요한 경우 [대량 데이터 삽입 API](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/) 을 가리키도록 업데이트하는 것이 좋습니다.

## 날짜

모든 행의 첫 번째 값 **반드시** 날짜가 되어야 합니다. 날짜 형식은 다음 형식 중 하나여야 합니다.

* **`MM/DD/YY/HH/mm/SS`**
* **`MM/DD/YY`**

시간/분/초를 생략하면 해당 날짜의 타임스탬프가 자동으로 오후 12시로 설정됩니다.

단일 데이터 소스 파일은 최대 90일의 고유한 날짜를 지원합니다. 업로드에 90일 이상의 고유 일을 포함하려면 데이터를 여러 파일로 분할합니다.

## Dimension 및 지표 데이터

각 행의 날짜 후 후속 값에는 업로드할 데이터가 포함됩니다. 모든 행은 해당 타임스탬프에 해당합니다. 모든 행에 동일한 수의 탭이 있는지 확인합니다. 열은 순서에 관계없이 지정할 수 있습니다. 각 행의 데이터가 맨 위의 헤더에 맞아야 합니다. 단일 행의 최대 데이터 양은 4096바이트입니다.

Dimension 데이터에는 세미콜론(`;`). 세미콜론이 포함된 행을 건너뜁니다.

## 다음 단계

[파일 업로드](file-upload.md): Adobe별로 수집하기 위해 데이터 소스 파일을 업로드하는 프로세스를 알아봅니다.
