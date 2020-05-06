---
title: FAQ
description: 타사 플랫폼에서 Adobe로 이동할 때 자주 묻는 질문에 대한 답변을 얻을 수 있습니다.
translation-type: tm+mt
source-git-commit: 3211598c2ff43493b329a9be4fb6877ae29cf08b
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 75%

---


# FAQ

**내 기존 데이터를 타사 플랫폼에서 Adobe Analytics로 마이그레이션하려면 어떻게 해야 합니까?**

모든 Analytics 플랫폼에는 데이터를 수집, 처리 및 저장하는 다양한 방법이 있습니다. 이전 데이터를 마이그레이션하지 않고 Adobe Analytics 내에서 데이터를 수집하고 사용하기 시작하려면 명확한 전환 날짜를 설정하는 것이 좋습니다. 자주 사용되는 전환 날짜는 회계 연도의 시작 날짜, 해당 연도의 시작 날짜 또는 달력의 시작 날짜입니다. 사용자가 이전 데이터를 보려는 경우 타사 플랫폼에 로그인하여 구체적인 이전 보고 내용을 볼 수 있습니다.

조직에서 이전 데이터를 Adobe에 포팅하려는 의지가 확고한 경우에는 조직의 계정 관리자에게 문의하십시오. 구현 컨설턴트는 조직과 협력하여 Google Analytics 데이터 내보내기를 Adobe 데이터 수집 서버에서 수집할 수 있는 데이터 소스로 변환할 수 있습니다.

이전 데이터를 새 플랫폼으로 이전하는 것은 복잡한 과정이며 조직에 너무 많은 비용 부담을 주기 때문에 Adobe에서는 권장하지 않습니다. 방문자 정보는 플랫폼마다 서로 다른 쿠키에 저장되고 서로 다른 형식으로 저장되므로 방문자 ID를 Adobe로 원활하게 옮길 수도 없습니다.

**이전에는 많은 보고서에서 세그멘테이션 드롭다운을 사용했습니다. How can I recreate that in[!UICONTROL Analysis Workspace]?**

Dropdown filters are a flexible and robust feature in [!UICONTROL Analysis Workspace] that allows a segmentation dropdown. 작업 영역 프로젝트에서 다음을 수행하십시오.

1. 드롭다운에 포함할 구성 요소를 ctrl+클릭(Windows)하거나 cmd+클릭(Mac)합니다. 세그먼트에만 국한되지 않고, 모든 구성 요소를 드롭다운 필터에 포함할 수 있습니다.
2. 구성 요소 그룹을 &#39;여기에 세그먼트 놓기&#39;라는 작업 공간 영역으로 끌어 놓습니다. 이동하기 전에 Shift 키를 누릅니다.

Users accessing this [!UICONTROL Workspace] project can now use this dropdown to apply segments or other components to the project. See [Panels Overview](/help/analyze/analysis-workspace/c-panels/panels.md) in the Adobe Analytics Tools guide for more information.

**이전에는 차원 값을 클릭해서 드릴다운을 확인했습니다. Analysis Workspace에서 이러한 간편한 워크플로우를 복제하려면 어떻게 합니까?**

분석 작업 공간 [!UICONTROL 의] 차원 값에는 간편한 분류 워크플로우가 있습니다. 마우스 왼쪽 단추 클릭 대신 마우스 오른쪽 단추를 클릭하여 액세스합니다. Right-click on a dimension value, click **[!UICONTROL Breakdown], then select the desired component. 각 값을 ctrl+클릭(Windows)하거나 cmd+클릭(Mac)하여 여러 차원 값에 동일한 분류를 적용할 수 있습니다.
