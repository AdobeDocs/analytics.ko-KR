---
title: eVar
description: 구현에 사용할 수 있는 사용자 지정 변수입니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# eVar

*이 도움말 페이지에서는 eVar 구현 방법에 대해 설명합니다. eVar가 차원으로 작동하는 방법에 대한 자세한 내용은 구성[요소](../../../components/c-variables/dimensionslist/reports-conversion.md)사용 안내서의 eVar를 참조하십시오.*

eVar는 원하는 대로 사용할 수 있는 사용자 지정 변수입니다.

>[!TIP] 대부분의 경우 prop보다 eVar를 사용하는 것이 좋습니다. 이전 버전의 Adobe Analytics에서는 prop 및 eVar가 서로 장단점이 있었습니다. 그러나 Adobe는 prop에 대한 거의 모든 사용 사례를 충족하도록 eVar를 개선했습니다.

[솔루션 디자인 문서](../../prepare/solution-design.md)에 각 eVar의 사용 방법과 해당 논리를 반드시 기록하십시오.

## 보고서 세트 설정에서 eVar 설정

구현에서 eVar를 사용하기 전에 보고서 세트 설정에서 각 eVar를 구성해야 합니다. 관리 안내서에서 [전환 변수](/help/admin/admin/conversion-var-admin/conversion-var-admin.md)를 참조하십시오.

## Adobe Experience Platform Launch의 eVar

Analytics 확장(전역 변수)을 구성하는 동안 또는 규칙에서 eVar를 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. Go to the [!UICONTROL Rules] tab, then click the desired rule (or create a rule).
4. 아래에서 [!UICONTROL Actions]기존 [!UICONTROL Adobe Analytics - Set Variables] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. 드롭다운을 [!UICONTROL Extension] Adobe Analytics로 설정하고 [!UICONTROL Action Type] 을 [!UICONTROL Set Variables]설정합니다.
6. Locate the [!UICONTROL eVars] section.

eVar를 선택하여 값 또는 데이터 요소를 설정할 수 있습니다. 다른 Analytics 변수에서 값을 복사할 수도 있습니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.eVar1 - s.eVar250

각 eVar는 조직에 관련된 사용자 지정 값을 포함하는 문자열입니다. 최대 길이는 255바이트이고, 255바이트보다 긴 값은 Adobe에 전송될 때 자동으로 잘립니다.

```js
s.eVar1 = "Example custom value";
```

## 카운터 eVar

eVar 값은 일반적으로 문자열 값을 포함합니다. 하지만, 대신 카운터를 포함하도록 eVar를 구성할 수 있습니다. 예를 들어 구매 전에 수행한 내부 검색의 수를 계산하려는 경우가 있을 수 있습니다. 이런 경우 텍스트 값을 설정하는 대신 다음 구문을 사용합니다.

```js
// Increment a counter eVar by 1
s.eVar1 = "+1";

// Increment a counter eVar by 12.49
s.eVar1 = "+12.49";
```

소수점 이하 자리 수가 세 자리 이상인 수가 지정되는 경우, eVar 카운터는 소수점 이하 두 자리로 반올림합니다. eVar 카운터에는 음수가 들어 있을 수 없습니다.

>[!IMPORTANT] 먼저 카운터 eVar를 사용하기 전에 관리 콘솔에서 &#39;카운터&#39;에 eVar를 구성해야 합니다. 관리 안내서에서 [전환 변수](/help/admin/admin/conversion-var-admin/conversion-var-admin.md)를 참조하십시오.

## Prop 또는 eVar에 대한 고급 이점

현재 버전의 Adobe Analytics에서 prop 및 eVar는 모두 유사한 기능을 가진 사용자 지정 변수입니다. 하지만, 몇 가지 주요한 차이점이 있습니다.

* prop의 데이터는 수 분 내에 보고에서 사용할 수 있습니다. eVar는 보고에 표시되는 데 30분 이상 소요될 수 있습니다.
* prop은 보고서에서 100바이트로 제한됩니다. eVar는 255바이트로 제한됩니다.
* prop은 동일한 히트에서 여러 값을 수락하는 목록 prop이 될 수 있습니다. 목록 변수는 별개의 변수이며 사용할 수 있는 목록 변수는 세 개뿐입니다.
* 기본적으로 prop은 prop이 설정된 히트 이후에 지속되지 않습니다. eVar에는 사용자 지정 만료가 있으므로, eVar가 후속 이벤트에 대한 크레딧을 더 이상 받지 않는 시기를 결정할 수 있습니다. 그러나 [보고서 시간 처리를](../../../components/vrs/vrs-report-time-processing.md)사용하는 경우 prop과 eVar 모두 사용자 지정 속성 모델을 사용할 수 있습니다.
