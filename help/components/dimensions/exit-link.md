---
title: 종료 링크
description: 종료 링크의 이름입니다.
feature: Dimensions
exl-id: 090d5fee-4b35-4be7-866c-5ef1d1c4c0a6
source-git-commit: 418e8d467ca29267314e14fba99783d0cb3d05a9
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 22%

---

# 종료 링크

&#39;종료 링크&#39; [차원](overview.md)은(는) 사이트에 구현된 종료 링크의 이름을 보고합니다. 종료 링크는 방문자를 현재 도메인에서 멀리 이동하는 아웃바운드 클릭을 추적합니다. 이 차원은 가장 자주 클릭하는 아웃바운드 링크를 이해하려 할 때 유용합니다.

## 이 차원을 데이터로 채우기

이 차원은 `pe` 쿼리 문자열의 값에 따라 이미지 요청의 [`pev2` 쿼리 문자열](/help/implement/validate/query-parameters.md)에서 데이터를 수집합니다. `pe` 쿼리 문자열은 `pev2` 값을 받는 링크 차원을 결정합니다.

* **[사용자 지정 링크](custom-link.md)**: `lnk_o`
* **[다운로드 링크](download-link.md)**: `lnk_d`
* **종료 링크**(이 페이지): `lnk_e`

`pev2`이(가) 제공되지 않으면 링크 URL(`pev1`)이 대신 차원 값으로 사용됩니다. 링크 이름이 명시적으로 제공된 경우 최대 길이는 100바이트입니다. 링크 URL에서 파생된 값은 이 제한을 받지 않습니다.

AppMeasurement을 사용하여 이 차원을 채우려면 `"e"`의 링크 유형 인수로 [`tl()`](/help/implement/vars/functions/tl-method.md) 이미지 요청을 보냅니다. 링크 이름 인수를 원하는 값으로 설정합니다.

```js
s.tl(true,"e","Example exit link");
```

## 차원 항목

이 변수는 구현의 사용자 지정 문자열에 기반하므로 조직에서 차원 항목을 결정합니다. 보고 요구 사항에 따라 링크를 의미 있는 카테고리로 그룹화하는 것이 좋습니다. 링크 이름이 제공되지 않으면 차원 항목이 원시 URL로 대신 표시됩니다. 이러한 원시 URL은 보고서에서 해석하기가 더 어려우므로 가능한 한 수사적 링크 이름을 제공합니다.
