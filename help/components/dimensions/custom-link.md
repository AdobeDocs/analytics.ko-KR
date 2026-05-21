---
title: 사용자 정의 링크
description: 사용자 지정 링크의 이름입니다.
feature: Dimensions
exl-id: c153f710-f03f-4be6-8e18-5ebf2ed80f01
TQID: https://experienceleague.adobe.com/x4IAGJjozPnLsft1e9xs68L6TNDJbHW0H4Z23p9EDNg
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 9b4525e014170b72688044a6ead344b1bde8c39b
workflow-type: tm+mt
source-wordcount: 242
ht-degree: 21%

---

# 사용자 정의 링크

&#39;사용자 지정 링크&#39; [차원](overview.md)은(는) 사이트에 구현된 사용자 지정 링크의 이름을 보고합니다. 사용자 지정 링크는 파일 다운로드나 아웃바운드 탐색이 아닌 모든 상호 작용에 대한 유연한 추적 메커니즘입니다. 일반적인 예로는 버튼 클릭, 내부 탐색 또는 양식 상호 작용이 있습니다. 이 차원은 방문자가 가장 많이 참여하는 상호 작용을 이해하려 할 때 유용합니다.

## 이 차원을 데이터로 채우기

이 차원은 `pe` 쿼리 문자열의 값에 따라 이미지 요청의 [`pev2` 쿼리 문자열](/help/implement/validate/query-parameters.md)에서 데이터를 수집합니다. `pe` 쿼리 문자열은 `pev2` 값을 받는 링크 차원을 결정합니다.

* **사용자 지정 링크**(이 페이지): `lnk_o`
* **[다운로드 링크](download-link.md)**: `lnk_d`
* **[종료 링크](exit-link.md)**: `lnk_e`

`pev2`이(가) 제공되지 않으면 링크 URL(`pev1`)이 대신 차원 값으로 사용됩니다. 링크 이름이 명시적으로 제공된 경우 최대 길이는 100바이트입니다. 링크 URL에서 파생된 값은 이 제한을 받지 않습니다.

AppMeasurement을 사용하여 이 차원을 채우려면 `"o"`의 링크 유형 인수로 [`tl()`](/help/implement/vars/functions/tl-method.md) 이미지 요청을 보냅니다. 링크 이름 인수를 원하는 값으로 설정합니다.

```js
s.tl(true,"o","Example custom link");
```

## 차원 항목

이 변수는 구현의 사용자 지정 문자열에 기반하므로 조직에서 차원 항목을 결정합니다. 보고 요구 사항에 따라 링크를 의미 있는 카테고리로 그룹화하는 것이 좋습니다. 링크 이름이 제공되지 않으면 차원 항목이 원시 URL로 대신 표시됩니다. 이러한 원시 URL은 보고서에서 해석하기가 더 어려우므로 가능한 한 수사적 링크 이름을 제공합니다.
