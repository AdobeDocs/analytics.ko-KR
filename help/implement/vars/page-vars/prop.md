---
title: prop
description: 구현에 사용할 수 있는 사용자 지정 변수.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# prop

Prop은 원하는 대로 사용할 수 있는 사용자 지정 변수입니다.

> [!TIP] 대부분의 경우 eVar를 사용하는 것이 좋습니다. 이전 버전의 Adobe Analytics에서는 prop 및 eVar가 서로 장단점이 있었습니다. 그러나 Adobe는 prop에 대한 거의 모든 사용 사례를 충족하는 eVar를 개선했습니다. 이러한 [두](evar.md) 사용자 지정 변수 유형 간의 기능 비교는 eVar를 참조하십시오.

조직에서 Prop을 사용하는 경우 [솔루션 디자인 문서에서](../../prepare/solution-design.md)사용 및 로직을 기록해야 합니다.

## Adobe Experience Platform Launch의 Prop

Analytics 확장 기능(전역 변수)을 구성하는 동안 또는 규칙에서 prop을 설정할 수 있습니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 탭으로 이동한 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다. [!UICONTROL Rules]
4. 아래에서 [!UICONTROL Actions]기존 [!UICONTROL Adobe Analytics - Set Variables] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. 드롭다운을 [!UICONTROL Extension] Adobe Analytics로 설정하고 [!UICONTROL Action Type] 을 [!UICONTROL Set Variables]설정합니다.
6. 섹션을 [!UICONTROL Props] 찾습니다.

prop을 선택하여 값 또는 데이터 요소를 설정할 수 있습니다. 다른 Analytics 변수에서 값을 복사할 수도 있습니다.

## s.prop1 - s.prop75 in AppMeasurement and Launch 사용자 지정 코드 편집기

각 prop 변수는 조직 고유의 사용자 지정 값을 포함하는 문자열입니다. 최대 길이는 100바이트입니다.100바이트보다 긴 값은 Adobe로 전송될 때 자동으로 잘립니다.

```js
s.prop1 = "Example custom value";
```

## 목록 Prop

목록 Prop은 변수가 동일한 히트에서 여러 값을 보유할 수 있도록 하는 prop에 적용되는 설정입니다. 이 설정이 활성화되어 있지 않거나 잘못된 구분 기호를 사용하는 경우 변수가 단일 값으로 처리됩니다.

### 목록 Prop 구성

보고서 세트 설정에서 목록 Prop을 활성화합니다. See [Traffic variables](/help/admin/admin/c-traffic-variables/traffic-var.md) in the Admin user guide. 원하는 구분 기호가 올바르게 구성되었는지 확인합니다. Adobe는 기본 구분 기호를 제공하지 않습니다.

> [!TIP] 구현에 사용되는 일반적인 구분 기호는 쉼표(`,`), 콜론(`:`), 세미콜론(`;`) 또는 파이프(`|`)입니다. 구현에 가장 적합한 구분 기호를 사용할 수 있습니다.

### 목록 Prop 설정

원하는 구분 기호가 있는 보고서 세트 설정에서 목록 Prop을 구성하면 구분 기호를 사용하는 것 외에 구현 차이가 없습니다.

```js
// List prop delimited with a comma
s.prop1 = "value1,value2,value3";
```

> [!IMPORTANT] 목록 prop은 여전히 최대 길이 100바이트의 영향을 받습니다. 목록 Prop은 여러 값을 포함할 수 있으므로 이 제한에 도달하고 잘립니다. 이 100바이트 제한에 도달하는 경우 약어 또는 단축 값을 사용하는 것이 좋습니다.

목록 Prop에서 동일한 값을 두 번 이상 설정하면 보고에서 중복 제거됩니다. 분석 작업 공간은 값이 표시되는 히트 수와 값이 데이터에 존재하는 횟수를 카운트하지 않습니다.
