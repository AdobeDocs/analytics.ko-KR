---
title: eVar
description: 구현에 사용할 수 있는 사용자 지정 변수입니다.
translation-type: tm+mt
source-git-commit: 10e157e370367374b55ee9c87c0e5c7ca9e99c1a
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 86%

---


# eVar

*이 도움말 페이지에서는 eVar 구현 방법에 대해 설명합니다. eVar가 차원으로 작동하는 방법에 대한 자세한 내용은 구성 요소 사용 안내서의[eVar](/help/components/dimensions/evar.md)를 참조하십시오.*

eVar는 원하는 대로 사용할 수 있는 사용자 지정 변수입니다. [솔루션 디자인 문서](/help/implement/prepare/solution-design.md)가 있는 경우 조직 고유의 차원은 대부분 eVar로 끝납니다. 기본적으로 eVar는 설정된 히트를 넘어서까지 지속됩니다. You can customize their expiration and allocation under [Conversion variables](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) in Report suite settings.

사용 가능한 eVar 수는 Adobe와의 계약에 따라 다릅니다. Adobe와의 계약이 지원하는 경우 최대 250개의 eVar를 사용할 수 있습니다.

## 보고서 세트 설정에서 eVar 설정

구현에서 eVar를 사용하기 전에 보고서 세트 설정에서 각 eVar를 구성해야 합니다. 관리 안내서에서 [전환 변수](/help/admin/admin/conversion-var-admin/conversion-var-admin.md)를 참조하십시오.

## Adobe Experience Platform Launch의 eVar

Analytics 확장(전역 변수)을 구성하는 동안 또는 규칙에서 eVar를 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 규칙] 탭으로 이동한 다음, 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [!UICONTROL 작업]에서 기존 [!UICONTROL Adobe Analytics - 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. [!UICONTROL 확장] 드롭다운을 Adobe Analytics로 설정하고 [!UICONTROL 작업 유형]을 [!UICONTROL 변수 설정]으로 설정합니다.
6. [!UICONTROL eVar] 섹션을 찾습니다.

eVar를 값 또는 데이터 요소로 설정할 수 있습니다. 다른 Analytics 변수에서 값을 복사할 수도 있습니다.

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

> [!IMPORTANT] 먼저 카운터 eVar를 사용하기 전에 Admin Console에서 eVar를 &#39;카운터&#39;로 구성해야 합니다. 관리 안내서에서 [전환 변수](/help/admin/admin/conversion-var-admin/conversion-var-admin.md)를 참조하십시오.
