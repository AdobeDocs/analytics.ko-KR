---
title: eVar
description: 구현에 사용할 수 있는 사용자 지정 변수.
translation-type: tm+mt
source-git-commit: 8a090574a6822a76366343ad5c657280bf7475eb

---


# eVar

eVar는 원하는 대로 사용할 수 있는 사용자 지정 변수입니다.

> [!TIP] 대부분의 경우 prop보다 eVar를 사용하는 것이 좋습니다. 이전 버전의 Adobe Analytics에서는 prop 및 eVar가 서로 장단점이 있었습니다. 그러나 Adobe는 prop에 대한 거의 모든 사용 사례를 충족하는 eVar를 개선했습니다.

각 eVar의 사용 방법과 [솔루션 디자인 문서에서](../../prepare/solution-design.md)해당 논리를 기록해야 합니다.

## 보고서 세트 설정에서 eVar 설정

구현에서 eVar를 사용하기 전에 보고서 세트 설정에서 각 eVar를 구성해야 합니다. See [Conversion variables](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) in the Admin guide.

## Adobe Experience Platform Launch의 eVar

Analytics 확장 기능(전역 변수)을 구성하는 동안 또는 규칙에서 eVar를 설정할 수 있습니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 규칙 [!UICONTROL 탭으로 이동한] 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [ [!UICONTROL 동작]]에서 기존 Adobe Analytics - [!UICONTROL 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. 확장 [!UICONTROL 프로그램 드롭다운을 Adobe] Analytics로 설정하고 작업 [!UICONTROL 유형을 변수][!UICONTROL 설정으로]설정합니다.
6. eVar [!UICONTROL 섹션을] 찾습니다.

eVar를 선택하여 값 또는 데이터 요소를 설정할 수 있습니다. 다른 Analytics 변수에서 값을 복사할 수도 있습니다.

## s.eVar1 - s.eVar250 in AppMeasurement and Launch 사용자 지정 코드 편집기

각 eVar는 조직에 고유한 사용자 지정 값을 포함하는 문자열입니다. 최대 길이는 255바이트입니다.255바이트보다 긴 값은 Adobe로 전송될 때 자동으로 잘립니다.

```js
s.eVar1 = "Example custom value";
```

## 카운터 eVar

eVar 값은 일반적으로 문자열 값을 포함합니다. 하지만, 대신 카운터를 포함하도록 eVar를 구성할 수 있습니다. 예를 들어 구매 전에 수행한 내부 검색 수를 카운트하려는 경우 텍스트 값을 설정하는 대신 다음 구문을 사용합니다.

```js
// Increment a counter eVar by 1
s.eVar1 = "+1";

// Increment a counter eVar by 12.49
s.eVar1 = "+12.49";
```

소수점 이하 자리 수가 세 자리 이상인 수가 지정되는 경우, eVar 카운터는 소수점 이하 두 자리로 반올림합니다. eVar 카운터는 음수를 포함할 수 없습니다.

## prop 또는 eVar에 대한 이점

현재 버전의 Adobe Analytics에서 prop 및 eVar는 모두 유사한 기능을 가진 사용자 지정 변수입니다. 하지만, 그들은 몇 가지 주요한 차이점이 있습니다.

* prop의 데이터는 몇 분 내에 보고할 수 있습니다. eVar는 보고에 나타나는 데 30분 이상 걸릴 수 있습니다.
* Prop은 보고서에서 100바이트 제한을 갖습니다. eVar에는 255바이트 제한이 있습니다.
* Prop은 동일한 히트에서 여러 값을 허용하는 목록 Prop이 될 수 있습니다. 목록 변수는 별도의 변수이며 사용할 수 있는 목록 변수는 세 개뿐입니다.
* 기본적으로 Prop은 설정된 히트를 초과하지 않습니다. eVar에는 사용자 지정 만료가 있으므로, eVar가 이후 이벤트에 대한 크레딧을 더 이상 받지 않는 시기를 결정할 수 있습니다. 보고서 [시간 처리를](../../../components/vrs/vrs-report-time-processing.md)사용하는 경우 prop과 eVar 모두 원하는 속성 모델을 사용할 수 있습니다.
