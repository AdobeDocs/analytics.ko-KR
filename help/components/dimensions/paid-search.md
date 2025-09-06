---
title: 유료 검색
description: 유료 검색과 자연어 검색 지표를 구분합니다.
feature: Dimensions
exl-id: b12665a3-e92f-4fc1-acd3-ea17a316e5e5
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 87%

---

# 유료 검색

&#39;유료 검색&#39; [차원](overview.md)을(를) 사용하면 모든 지표를 보고 유료 검색과 자연어 검색 간에 비교할 수 있습니다. 검색 엔진 외부의 다른 모든 히트는 생략됩니다. 이 차원은 유료 검색 노력에서 유기 검색과 비교하는 방식을 이해하는 데 유용합니다.

## 이 차원을 데이터로 채우기

이 차원이 제대로 작동하기 위한 유일한 요구 사항은 보고서 세트 설정에 [유료 검색 감지](/help/admin/tools/manage-rs/edit-settings/general/paid-search-detection/paid-search-detection.md)가 올바로 구성되어 있는 것입니다. 유료 검색 감지가 올바로 구성되어 있고 보고서 세트에 데이터가 있다면 이 차원은 항상 작동합니다.

## 차원 항목

차원 항목에는 `"Natural"`와 `"Paid"`, 이렇게 두 개의 정적 값이 포함됩니다. 방문이 검색 엔진의 기준과 일치하고 유료 검색 감지와도 일치하면 이 방문은 `"Paid"` 차원 항목에 속합니다. 방문이 검색 엔진의 기준과 일치하고 유료 검색 감지와 일치하지 *않으면* 이 방문은 `"Natural"` 차원 항목에 속합니다.
