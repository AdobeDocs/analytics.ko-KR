---
title: 쿠키 지원
description: 브라우저가 쿠키를 지원하는지 여부를 결정합니다.
feature: Dimensions
exl-id: 07d4fe12-0d60-469d-98b1-e93ce5a0fd21
TQID: https://experienceleague.adobe.com/axOR-Ut8kkRSCTYPescoSCa44g25E8xxp4gg-yQlyYw
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 188
ht-degree: 92%

---

# 쿠키 지원

&#39;쿠키 지원&#39; [차원](overview.md)은(는) 브라우저가 지정된 히트에 대한 쿠키를 지원하는지 여부를 보고합니다. 쿠키를 지원하는 브라우저를 사용하는 방문자와 쿠키를 의도적으로 비활성화하는 방문자의 비율을 파악하는 것이 유용합니다.

## 이 차원을 데이터로 채우기

이 차원은 이미지 요청의 [`k` 쿼리 문자열](/help/implement/validate/query-parameters.md)에서 데이터를 수집합니다. AppMeasurement는 `s_cc`라는 쿠키를 설정한 다음 쿠키가 존재하는지 감지합니다. 그 결과가 쿼리 문자열 매개 변수 값 `Y`(브라우저가 지원하고 쿠키가 활성되어 있는 경우) 또는 `N`(브라우저에 쿠키가 비활성화되어 있는 경우)입니다. AppMeasurement 라이브러리를 사용하는 경우(Adobe Experience Platform의 태그 등을 통해) 이 차원은 즉시 작동합니다. AppMeasurement 외부의 데이터 수집 방법을 사용하는 경우 (API 등을 통해)에는 값 `Y` 또는 `N`으로 각 히트에서 `k` 쿼리 문자열 매개 변수를 포함해야 합니다.

## 차원 항목

차원 항목은 `Enabled`, `Disabled` 및 `Unknown`을 포함합니다.

* **`Enabled`**: 브라우저가 쿠키를 지원하고 브라우저에 쿠키가 활성화되어 있습니다.
* **`Disabled`**: 브라우저가 쿠키를 지원하지 않거나 방문자가 쿠키를 비활성화했습니다.
* **`Unknown`**: AppMeasurement가 쿠키 지원을 확인할 수 없습니다. 이미지 요청에 `k` 쿼리 문자열이 없습니다.
