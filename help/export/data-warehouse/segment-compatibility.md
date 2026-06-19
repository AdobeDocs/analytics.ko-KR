---
title: Data Warehouse 세그먼트 호환성
description: Data Warehouse에서 사용할 수 있는 세그먼트 정의가 무엇인지 알아봅니다.
feature: Data Warehouse
exl-id: 66b86226-ef4c-4a1a-abe1-3c3accf419e5
TQID: https://experienceleague.adobe.com/7CrArNYD-8ZXVpfO86d1l42ySkTuv8V04PWJFeNWx3s
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7
subfeature_v2: id: a544b409-2610-410d-a842-474ac1d0d54eid: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: d4db20e3498d54162806b3fdef0b34f45c93a6ff
workflow-type: tm+mt
source-wordcount: 456
ht-degree: 9%

---

# Data Warehouse 세그먼트 호환성

세그먼트 빌더에 내장된 모든 세그먼트를 Data Warehouse에서 사용할 수 있는 것은 아닙니다. 이 페이지에서는 [Data Warehouse 요청을 만들](/help/export/data-warehouse/create-request/t-dw-create-request.md)때 선택할 수 있도록 Data Warehouse과 호환되는 세그먼트 정의를 알아봅니다.

다음 중 **모두**&#x200B;이(가) 참인 경우에만 세그먼트가 Data Warehouse과 호환됩니다.

* **지원되는 구성 요소**: 세그먼트는 Data Warehouse에서 지원하는 차원과 지표만 사용합니다.
* **지원되는 구조**: 세그먼트의 구조는 Data Warehouse에서 시행하는 규칙을 따릅니다.

두 조건 중 하나를 충족하지 않으면 Data Warehouse 요청을 작성할 때 세그먼트가 옵션으로 표시되지 않으며, 호환되지 않는 세그먼트가 포함된 가상 보고서 세트를 선택하면 오류가 표시됩니다.

## 지원되는 구성 요소

세그먼트가 적용되는 요청과 동일한 데이터에 대해 평가되기 때문에 **Data Warehouse 요청에서 지원되지 않는 모든 구성 요소도 세그먼트에서 지원되지 않습니다.** Data Warehouse에서 지원하지 않는 차원 및 지표의 전체 목록은 [Data Warehouse의 구성 요소 지원](component-support.md)을 참조하십시오.

[구성 요소 지원](component-support.md)에 나열된 차원 및 지표 외에 다음 차원은 Data Warehouse *요청*&#x200B;에서 사용할 수 있지만 **세그먼트 정의 내에서 사용할 수 없습니다**.

* [[!UICONTROL 날짜]](/help/components/dimensions/day-of-month.md)
* [[!UICONTROL 요일]](/help/components/dimensions/day-of-week.md)
* [[!UICONTROL 일 (한 해 기준)]](/help/components/dimensions/day-of-year.md)
* [[!UICONTROL 시간 (일 기준)]](/help/components/dimensions/hour-of-day.md)
* [[!UICONTROL 마케팅 채널]](/help/components/dimensions/marketing-channel.md)(대신 [[!UICONTROL 마지막 터치 채널]](/help/components/dimensions/last-touch-channel.md) 사용)
* [[!UICONTROL 월 (연 기준)]](/help/components/dimensions/month-of-year.md)
* [[!UICONTROL 페이지를 찾을 수 없음]](/help/components/dimensions/pages-not-found.md)(대신 [[!UICONTROL 페이지 유형 오류]](/help/components/dimensions/pages-not-found.md) 사용)
* [[!UICONTROL 사분기]](/help/components/dimensions/quarter-of-year.md)
* [[!UICONTROL 평일/주말]](/help/components/dimensions/weekday-weekend.md)

## 지원되는 구조

세그먼트가 지원되는 구성 요소만 사용하는 경우에도 해당 구조는 Data Warehouse에서 시행하는 규칙을 따라야 합니다. 세그먼트 구조는 완전히 지원되거나, 부분적으로 지원되거나, 지원되지 않습니다.

**지원됨**:

* **세그먼트 스택**: 여러 세그먼트를 단일 Data Warehouse 요청에 적용할 수 있습니다.
* **중첩된 컨테이너**: 지원되는 경우 각 수준에서 범위가 줄어듭니다(방문자→ 방문 → 히트). 범위가 증가하는 컨테이너는 지원되지 않습니다.

**부분적으로 지원됨**:

* **컨테이너 제외**: 최상위 수준에서만 지원됩니다. Data Warehouse은 `A AND NOT B`(으)로 표시할 수 있는 세그먼트만 지원합니다. 즉, **이 특성을 포함** 및 **이 특성을 제외**&#x200B;합니다. 다른 컨테이너 내에 중첩된 컨테이너는 제외할 수 없습니다.
* **AND/OR 논리**: 제한 사항에서 지원됩니다. `exclusion` 또는 `without` 컨테이너를 AND/OR 논리와 함께 사용하면 `A AND NOT B`(으)로 다시 쓸 수 있는 세그먼트만 지원됩니다.

**지원되지 않음**:

* **순차적 세그먼트**: THEN 연산자를 사용하여 정렬된 방문자 탐색 시퀀스를 정의하는 세그먼트는 지원되지 않습니다.
* **&quot;다음 중 1개 이상의 항목과 같음&quot; 및 &quot;다음 중 같은 항목 없음&quot; 연산자**: 이러한 연산자는 Data Warehouse 세그먼트에서 지원되지 않습니다.

## 차원으로 사용되는 세그먼트

Data Warehouse 보고서에서 세그먼트를 차원으로 사용하면 보고서는 `"0"` 또는 `"1"`이(가) 포함된 열을 반환합니다.

* **`"0"`**: 차원 항목이 세그먼트의 기준을 충족하지 않았습니다.
* **`"1"`**: 차원 항목이 세그먼트의 기준을 충족했습니다.
