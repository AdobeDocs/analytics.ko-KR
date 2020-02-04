---
title: 목록에 있는 참조 페이지를 나타냅니다
description: 동일한 히트에 여러 값이 있는 사용자 지정 변수.
translation-type: tm+mt
source-git-commit: 664d0cde8b8b17c86b47858611d459026aab0bef

---


# 목록에 있는 참조 페이지를 나타냅니다

목록 변수는 원하는 대로 사용할 수 있는 사용자 지정 변수입니다. 이 변수들은 동일한 히트에서 여러 값을 포함할 수 있다는 점을 제외하면 eVar와 유사하게 작동합니다. 목록 변수에는 문자 제한이 없습니다.

각 목록 변수와 [솔루션 디자인 문서에서](../../prepare/solution-design.md)해당 논리를 사용하는 방법을 기록해야 합니다.

> [!NOTE] 목록 변수는 방문자당 가장 최근 250개의 값을 저장합니다. 주어진 방문자에 대해 250개 이상의 고유 값이 있는 경우 가장 오래된 값은 지표에 귀속되지 않습니다.

## 보고서 세트 설정에서 목록 변수 설정

구현에서 각 목록 변수를 사용하기 전에 보고서 세트 설정에서 각 목록 변수를 구성해야 합니다. See [Conversion variables](/help/admin/admin/conversion-var-admin/list-var-admin.md) in the Admin guide.

## Adobe Experience Platform Launch의 목록 변수

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용합니다.

## s.list1 - s.list3 in AppMeasurement and Launch 사용자 지정 코드 편집기

각 목록 변수는 조직 고유의 사용자 지정 값을 포함하는 문자열입니다. 최대 바이트 수가 없습니다.그러나 각 개별 값의 최대 길이는 255바이트입니다. 사용하는 구분 기호는 보고서 세트 설정에서 변수를 설정할 때 결정됩니다. 여러 항목을 구분할 때 공백을 사용하지 마십시오.

```js
// A list variable configured with a comma as a delimiter
s.list1 = "Example value 1,Example value 2,Example value 3";
```

> [!TIP] 동일한 히트에서 중복 값을 설정하면 Adobe는 해당 값의 모든 인스턴스를 중복 제거합니다. 예를 들어, 설정하면 `s.list1 = "Example,Example";`보고서에서 하나의 인스턴스가 카운트됩니다.

## 목록 prop과 목록 변수 비교

목록 Prop 및 목록 변수는 모두 동일한 히트에 여러 값을 포함할 수 있습니다. 그러나 이러한 두 변수 유형에는 몇 가지 주요 차이점이 있습니다.

* 모든 prop은 목록 prop이 될 수 있습니다. 모든 prop이 목록 Prop인 경우 최대 75개의 목록 Prop을 효과적으로 보유할 수 있습니다. 사용할 수 있는 목록 변수는 3개뿐입니다.
* 목록 prop에는 전체 변수에 대해 100바이트 제한이 있습니다. 목록 변수에는 값당 255바이트 제한이 있고 총 바이트 제한이 없습니다.
* 목록 Prop은 설정된 히트를 넘어서까지 지속되지 않습니다. 목록 변수에는 원하는 만료 설정이 있습니다. 그러나 [보고서 시간 처리를](/help/components/vrs/vrs-report-time-processing.md)사용하면 목록 prop 및 목록 변수 모두에 사용자 지정 속성을 적용할 수 있습니다.
