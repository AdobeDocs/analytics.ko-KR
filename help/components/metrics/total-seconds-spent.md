---
title: 총 체류 시간 (초)
description: 차원 항목에서 보낸 총 시간 (초)입니다.
feature: Metrics
exl-id: 02302982-ce8c-44e9-9967-0a4f226f5e9e
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 90%

---

# 총 체류 시간 (초)

&#39;총 체류 시간(초)&#39; [지표](overview.md)은 방문자가 주어진 차원 항목에서 보낸 총 시간(초)을 보여줍니다. 이 지표는 주어진 차원 항목에서 보낸 원시 시간 크기를 원하는 경우 유용하며 지표가 제공하는 다른 체류 시간과 같은 평균은 아닙니다.

Report Builder에서는 이 지표를 &#39;총 체류 시간&#39;이라고 합니다.

## 이 지표의 계산 방법

이 지표는 다음 절차를 사용하여 계산을 측정합니다.

1. 주어진 히트의 타임스탬프를 확인합니다.
2. 이 히트를 방문에서 다음 히트의 타임스탬프와 비교합니다. 페이지 보기와 링크 추적 히트가 모두 계산됩니다.
3. 두 히트 사이에 경과된 시간 (초)이 차원 항목에 기여합니다.

[eVar](../dimensions/evar.md)와 같이 지속되는 변수는 총 체류 시간 (초)에 계산됩니다. [prop](../dimensions/prop.md)과 같은 트래픽 변수는 이후의 링크 추적 호출 간 체류 시간 (초)을 포함합니다.

>[!TIP]
>
>경과 시간을 측정할 후속 이미지 요청이 없기 때문에 페이지에서 체류한 시간은 방문의 마지막 히트에 대해서는 측정되지 않습니다. 이 개념은 단일 히트 (바운스)로 구성된 방문에도 적용됩니다.

체류 시간에 대한 일반적인 정보가 필요하면 [체류 시간 개요](time-spent.md)를 참조하십시오.
