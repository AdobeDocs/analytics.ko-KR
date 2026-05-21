---
title: 발생 횟수
description: 변수가 설정되었거나 지속된 히트의 수입니다.
feature: Metrics
exl-id: 8428e813-0fb4-4620-884e-1aa92fe33209
TQID: https://experienceleague.adobe.com/04bDCj1dkVb9gIDMbpvvGea92oOzd-N0XLfzf4t-6iA
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 280
ht-degree: 66%

---

# 발생 횟수

“발생 횟수” [지표](overview.md)는 지정된 차원이 설정되거나 지속된 히트 수를 보여 줍니다. Workspace의 차원을 빈 캔버스로 드래그하면 이 지표가 프로젝트에 자동으로 적용됩니다.

## 이 지표의 계산 방법

보고서 세트의 모든 히트 중에서 차원 항목이 정의되어 있거나 지속되는 히트를 포함하십시오. [eVar](../dimensions/evar.md)와 같은 일부 차원은 이 차원이 설정된 히트 이후에 유지됩니다. 이 지표는 초기 값과 지속된 값을 모두 계산합니다.

## 유사한 지표와 비교

* **발생 횟수와 [인스턴스](instances.md)** 비교: 발생 횟수는 차원 항목이 설정되어 있거나 지속된 히트를 계산합니다. 인스턴스는 차원 항목이 지속되는 히트를 포함하지 않습니다.
* **발생 횟수와 [페이지 조회수](page-views.md)** 비교: 발생 횟수에는 페이지 조회수 추적 호출 ([`t()`](/help/implement/vars/functions/t-method.md)), 링크 추적 호출 ([`tl()`](/help/implement/vars/functions/tl-method.md)) 및 요약 [데이터 소스](/help/import/data-sources/overview.md)의 데이터를 포함하여 모든 히트 유형이 포함됩니다. 페이지 조회수 지표에는 페이지 조회수 추적 호출만 포함되며 링크 추적 호출 및 요약 데이터 소스는 제외됩니다.

## 지속성

지속성 은 특정 차원 값과 설정된 이벤트에서 벗어난 지표의 관계를 설정할 수 있습니다. 지속성은 할당과 만료의 조합입니다. 단일 열에서 한 번에 두 개 이상의 차원 항목이 지속되는 경우 할당을 통해 보존되는 값을 결정할 수 있습니다. 만료 설정을 통해 설정된 이벤트에서 벗어난 차원 항목의 지속 기간을 결정할 수 있습니다.

지속성 은 차원에서만 사용할 수 있고 적용 대상 데이터에 대해 소급적입니다. 필터링이나 다른 분석 작업이 적용되기 전에 발생하는 즉각적인 데이터 변환입니다. 지속성 설정이 활성화되지 않으면 차원은 동일한 이벤트에 존재하는 지표에만 관련됩니다.