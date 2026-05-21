---
title: 페이지 조회수
description: 차원 항목이 Adobe Analytics에서 설정되거나 지속된 횟수입니다.
feature: Metrics
exl-id: 6b4fb7af-03e2-49e8-a431-f7746c89a626
TQID: https://experienceleague.adobe.com/ZJOoxc3imuMfVTa7caV5eQ6-XJh0amCRq65ByuANFq0
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 100%

---

# 페이지 조회수

**[!UICONTROL 페이지 조회수]** [지표](overview.md)는 주어진 차원 항목이 페이지에 설정되거나 지속된 횟수를 보여 줍니다. 보고서에서 가장 일반적이고 기본적인 지표 중 하나입니다.

## 이 지표의 계산 방법

이 지표는 보고서 세트의 모든 페이지 조회수 추적 호출 ([`t()`](/help/implement/vars/functions/t-method.md))을 계산합니다. 차원에는 차원 항목이 설정되거나 지속된 히트가 포함됩니다. 링크 추적 호출([`tl()`](/help/implement/vars/functions/tl-method.md)) 또는 [데이터 소스](/help/import/data-sources/overview.md)의 데이터는 포함하지 않습니다.

## 유사한 지표와 비교

* **페이지 조회수 및 [방문 횟수](visits.md)**: 페이지 조회수는 페이지가 조회된 횟수를 계산합니다. 방문 횟수는 방문자의 세션 수를 계산합니다. 방문 횟수 1회는 1회 이상의 페이지 조회수로 구성됩니다.
* **페이지 조회수 및 [페이지 이벤트](page-events.md)**: 페이지 조회수는 페이지 조회수 추적 호출(`t()`) 수를 계산하며, 여기에서 링크 추적 호출(`tl()`)은 제외됩니다. 이와 반대로 페이지 이벤트는 링크 추적 호출 수를 계산하며 페이지 조회수 추적 호출을 제외합니다.
