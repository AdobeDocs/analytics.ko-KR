---
title: prop
description: 구현에 사용할 수 있는 사용자 지정 변수입니다.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 80%

---


# prop

*이 도움말 페이지에서는 prop을 구현하는 방법을 설명합니다. For information on how props work as a dimension, see[prop](/help/components/dimensions/prop.md)in the Components user guide.*

prop은 원하는 대로 사용할 수 있는 사용자 지정 변수입니다. 설정된 히트 이후로 지속되지 않습니다.

>[!TIP]
>
>Adobe recommends using [eVars](evar.md) in most cases. 이전 버전의 Adobe Analytics에서는 prop 및 eVar가 서로 장단점이 있었습니다. 그러나 Adobe는 prop에 대한 거의 모든 사용 사례를 충족하도록 eVar를 개선했습니다.

솔루션 디자인 문서 [](/help/implement/prepare/solution-design.md)가 있는 경우 이러한 사용자 지정 차원을 조직 고유의 값에 할당할 수 있습니다. 사용 가능한 prop의 수는 Adobe와의 계약에 따라 달라집니다. Adobe와의 계약이 지원하는 경우 최대 75개의 prop을 사용할 수 있습니다.

## Adobe Experience Platform Launch의 prop

Analytics 확장(전역 변수)을 구성하는 동안 또는 규칙에서 prop을 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 규칙] 탭으로 이동한 다음, 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [!UICONTROL 작업]에서 기존 [!UICONTROL Adobe Analytics - 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. [!UICONTROL 확장] 드롭다운을 Adobe Analytics로 설정하고 [!UICONTROL 작업 유형]을 [!UICONTROL 변수 설정]으로 설정합니다.
6. [!UICONTROL prop] 섹션을 찾습니다.

prop을 값 또는 데이터 요소로 설정할 수 있습니다. 다른 Analytics 변수에서 값을 복사할 수도 있습니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.prop1 - s.prop75

각 prop 변수는 조직에 관련된 사용자 지정 값을 포함하는 문자열입니다. 최대 길이는 100바이트이고, 100바이트보다 긴 값은 Adobe에 전송될 때 자동으로 잘립니다.

```js
s.prop1 = "Example custom value";
```

## 목록 Prop

목록 prop은 변수가 동일한 히트에서 여러 값을 보유할 수 있도록 하는 prop에 적용되는 설정입니다. 이 설정이 활성화되어 있지 않거나 잘못된 구분 기호를 사용하는 경우 변수가 단일 값으로 처리됩니다.

### 목록 Prop 구성

보고서 세트 설정에서 목록 prop을 활성화합니다. 관리자 가이드의 [트래픽 변수](/help/admin/admin/c-traffic-variables/traffic-var.md)를 참조하십시오. 원하는 구분 기호가 올바로 구성되었는지 확인하십시오. Adobe에서는 기본 구분 기호를 제공하지 않습니다.

>[!TIP]
>
> 구현에 사용되는 일반적인 구분 기호는 쉼표(`,`), 콜론(`:`), 세미콜론(`;`) 또는 파이프(`|`)입니다. 구현에 가장 적합한 구분 기호를 사용할 수 있습니다.

### 목록 Prop 설정

원하는 구분 기호가 있는 보고서 세트 설정에서 목록 prop을 구성하면 구분 기호를 사용하는 것 외에는 구현에 차이가 없습니다.

```js
// List prop delimited with a comma
s.prop1 = "value1,value2,value3";
```

>[!IMPORTANT]
>
>목록 prop은 여전히 100바이트라는 최대 길이의 영향을 받습니다. 목록 prop은 여러 값을 포함할 수 있으므로 이 제한에 더 쉽게 도달하고 잘립니다. 이 100바이트 제한에 도달할 수 있는 경우에는 약어 또는 단축 값을 사용하는 것이 좋습니다.

목록 속성에서 동일한 값을 두 번 이상 설정하면 보고에서 중복되지 않습니다. Analysis Workspace는 값이 표시되는 히트 수를 계산하며, 데이터에 값이 존재하는 회수를 계산하지 않습니다.
