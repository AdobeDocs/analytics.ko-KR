---
title: 페이지를 찾을 수 없음 (지표)
description: 오류가 포함된 히트의 수입니다.
feature: Metrics
exl-id: 71e138b5-69bb-41b0-852c-ca4af22be1f3
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 48%

---

# 페이지를 찾을 수 없음

*이 도움말 페이지에서는 &#39;페이지를 찾을 수 없음&#39;이 지표로 작동하는 방식을 설명합니다. 자세한 내용은 [페이지를 찾을 수 없음](../dimensions/pages-not-found.md) 차원을 참조하십시오.*

&#39;페이지를 찾을 수 없음&#39; [지표](overview.md)은(는) 방문자에게 오류가 발생한 시점에 차원이 설정되었거나 지속된 히트 수를 보여줍니다. 이 지표는 오류 메시지(예: 404)가 포함된 페이지 또는 URL을 확인하려는 경우 유용합니다. 그런 다음 이 정보를 웹 개발 팀에 전달하여 오류의 원인을 파악하고 수정할 수 있습니다.

## 이 지표의 계산 방법

이 지표는 [`pageType`](/help/implement/vars/page-vars/pagetype.md) 변수가 `"errorPage"`의 값과 같은 모든 히트를 계산합니다. [페이지를 찾을 수 없음](../dimensions/pages-not-found.md) 차원에 해당하는 지표입니다.
