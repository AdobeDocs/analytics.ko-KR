---
title: 검색 결과
description: 히트가 외부 검색 기준과 일치한 횟수입니다.
feature: Metrics
exl-id: b84c895d-e678-47a1-9e41-500970e0a80c
TQID: https://experienceleague.adobe.com/bcK-h9tkOKRHFoZ5EbX05ppNtV5S8Kok8dhMJZxf-ao
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 88%

---

# 검색 결과

&#39;검색&#39; [지표](overview.md)은(는) Adobe의 외부 검색 감지와 일치하는 히트의 수를 보여줍니다. 이 지표는 비검색 차원 항목을 보고 이 값이 검색 엔진 트래픽에 어떻게 기여했는지 보려는 경우 유용합니다.

## 이 지표의 계산 방법

이 지표는 Adobe의 외부 검색 감지와 일치하는 히트의 수를 계산합니다. 다음 두 조건을 만족해야 합니다.

* 히트의 레퍼러 값이 Adobe에서 인식하는 검색 도메인입니다.
* 히트의 참조 URL에 키워드 쿼리 문자열 매개 변수가 포함되어 있습니다. 최신 개인 정보 보호 정책 때문에 이 쿼리 문자열 값은 일반적으로 비어 있습니다. Adobe는 빈 키워드 쿼리 문자열을 검색 감지의 일부로 인식합니다.
