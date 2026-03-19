---
title: 단일 페이지 방문 횟수 (지표)
description: 방문에서 '페이지' 차원 항목이 변경되지 않은 횟수입니다.
feature: Metrics
exl-id: 086235d0-4542-4e82-96ab-28c47c842ecf
source-git-commit: 6d2c278c5525c89b73c39bbfcedbe644806bf989
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 34%

---

# 단일 페이지 방문 횟수

*이 도움말 페이지에서는 &#39;단일 페이지 방문 횟수&#39;가 지표로 작동하는 방식을 설명합니다. 자세한 내용은 [단일 페이지 방문 횟수](../dimensions/single-page-visits.md) 차원을 참조하십시오.*

**[!UICONTROL 단일 페이지 방문]** [지표](overview.md)은(는) 전체 방문에 대해 [페이지](../dimensions/page.md) 차원 항목에 단일 값만 포함된 방문 횟수를 보여줍니다. 이 지표는 짧은 방문을 보고 싶지만 [[!UICONTROL 바운스]](bounces.md)만큼 엄격한 규칙이 없는 차원의 컨텍스트에서 유용합니다.

## 이 지표의 계산 방법

이 지표의 정의는 [[!UICONTROL 반복 인스턴스 계산]](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md#project-info-settings)의 프로젝트 설정에 따라 다릅니다.

* **[!UICONTROL 반복 인스턴스 계산] 사용**: [!UICONTROL 페이지] 차원에 방문에 대한 단일 값이 포함된 방문 수를 계산합니다. 방문자가 페이지를 다시 로드하면 단일 페이지 방문이 실패합니다.
* **[!UICONTROL 반복 인스턴스 계산] 사용 안 함**: [!UICONTROL 페이지] 차원에 전체 방문에 대한 단일 고유 값이 포함된 방문의 수를 계산합니다.

&#39;[!UICONTROL 반복 인스턴스 계산]&#39; 프로젝트 설정에 관계없이 이 지표는 다음 규칙을 준수합니다.

* 방문자가 링크 추적 호출을 실행하는 경우에도 방문은 여전히 단일 페이지 방문으로 유효합니다([!UICONTROL Page] 차원은 모든 링크 추적 호출에서 제거됨).
* [!UICONTROL 페이지] 차원이 두 번째 고유 값으로 바뀌자마자 이 방문은 더 이상 단일 페이지 방문으로 분류되지 않습니다.

지표 간의 비교에 대해서는 [단일 액세스](single-access.md)를 참조하십시오.
