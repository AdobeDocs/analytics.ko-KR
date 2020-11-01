---
description: 데이터 피드에 대한 FAQ
keywords: Data Feed;job;pre column;post column;case sensitivity
title: 데이터 피드 FAQ
translation-type: tm+mt
source-git-commit: a94b8e090b9a3c75a57fd396cac8486bba2e5d79
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 77%

---


# 데이터 피드 FAQ

데이터 피드에 대한 FAQ.

## `post_` 접두사가 있는 열과 `post_` 접두사가 없는 열 간의 차이점은 무엇입니까?

`post_` 접두사가 없는 열에는 데이터 수집에 전송된 것과 정확히 동일한 데이터가 포함됩니다. `post_` 접두사가 있는 열에는 처리 후 값이 포함됩니다. 값을 변경할 수 있는 예는 변수 지속성, 처리 규칙, VISTA 규칙, 통화 전환 또는 Adobe가 적용하는 서버측 논리입니다. 가능하면 열의 `post_` 버전을 사용하는 것이 좋습니다.

열에 `post_` 버전이 없다면(예: `visit_num`) 이 열은 이후 열로 간주할 수 있습니다.

## 데이터 피드는 대소문자 구분을 어떻게 처리합니까?

Adobe Analytics에서는 대부분의 변수가 보고 목적으로 대소문자를 구분하지 않는 것으로 간주됩니다. 예를 들어 &#39;snow&#39;, &#39;Snow&#39;, &#39;SNOW&#39; 및 &#39;sNow&#39;는 모두 동일한 값으로 간주됩니다. 대소문자 구분은 데이터 피드에서 유지됩니다.

이후가 아닌 열과 이후 열 간에 동일한 값의 대소문자가 다르게 되어 있다면(예: 이전 열에는 &quot;snow&quot;, 이후 열에는 &quot;Snow&quot;) 구현은 사이트 전체에서 대문자 값과 소문자 값을 모두 사용합니다. 이후 열에서 대소문자가 다른 값은 이전에 전달되어 가상 쿠키에 저장되어 있거나, 해당 보고서 세트에 대해 동일한 시간 동안 처리되었습니다.

## 보트는 데이터 피드에 포함된 Admin Console 보트 규칙으로 필터링됩니까?

데이터 피드는 [Admin Console 보트 규칙](https://docs.adobe.com/content/help/ko-KR/analytics/admin/admin-tools/bot-removal/bot-removal.html)으로 필터링된 보트를 포함하지 않습니다.

## 데이터 피드 열 `000` 또는 `event_list` `post_event_list` 데이터 피드 열에 여러 값이 표시되는 이유는 무엇입니까?

일부 스프레드시트 편집자, 특히 Microsoft Excel은 매우 많은 수의 파일을 자동으로 전달합니다. 열에는 쉼표로 구분된 숫자가 많이 포함되어 있어 Excel에서 이 값을 큰 수로 처리하는 경우가 있습니다. `event_list` 마지막 몇 자리를 다음으로 회전합니다 `000`.

Adobe은 Microsoft Excel에서 파일을 자동으로 열지 않도록 `hit_data.tsv` 권장합니다. 대신 Excel의 데이터 가져오기 대화 상자를 사용하여 모든 필드가 텍스트로 취급되었는지 확인합니다.
