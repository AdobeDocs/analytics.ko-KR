---
title: Adobe Analytics로 마이그레이션할 때 자주 묻는 질문
description: 서드파티 플랫폼에서 Adobe로 이동할 때 자주 묻는 질문에 대한 답변을 얻을 수 있습니다.
feature: Third-party Integration
exl-id: 1201909e-b20c-48c5-b287-393da8e22d78
source-git-commit: c53f886d5329e2a3b5023f9396c3aa2360a86901
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 95%

---

# Adobe Analytics로 마이그레이션할 때 자주 묻는 질문

**서드파티 플랫폼에서 Adobe Analytics로 이전 데이터를 마이그레이션하려면 어떻게 해야 합니까?**

모든 Analytics 플랫폼에는 데이터를 수집, 처리 및 저장하는 다양한 방법이 있습니다. 이전 데이터를 마이그레이션하지 않고 Adobe Analytics 내에서 데이터를 수집하고 사용하기 시작하려면 명확한 전환 날짜를 설정하는 것이 좋습니다. 자주 사용되는 전환 날짜는 회계 연도의 시작 날짜, 해당 연도의 시작 날짜 또는 달력의 시작 날짜입니다. 사용자가 이전 데이터를 보려는 경우 서드파티 플랫폼에 로그인하여 구체적인 이전 보고 내용을 볼 수 있습니다.

조직에서 내역 데이터를 Adobe에 포팅하려는 의지가 확고한 경우 Adobe 계정 팀에 문의하십시오. 구현 컨설턴트는 조직과 협력하여 Google Analytics 데이터 내보내기를 Adobe 데이터 수집 서버에서 수집할 수 있는 데이터 소스로 변환할 수 있습니다.

과거 데이터를 이동하려면 모든 옴니채널 데이터 소스를 사용할 수 있는 [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html)를 사용하는 것을 권장합니다.

**이전에는 많은 보고서에서 세그먼테이션 드롭다운을 사용했습니다. [!UICONTROL Analysis Workspace]에서 이를 다시 만들 수 있습니까?**

드롭다운 필터는 세그먼테이션 드롭다운을 허용하는 [!UICONTROL Analysis Workspace]의 유연하고 강력한 기능입니다. 작업 영역 프로젝트에서 다음 작업을 수행하십시오.

1. 드롭다운에 포함할 구성 요소를 ctrl+클릭 (Windows)하거나 cmd+클릭 (Mac)합니다. 세그먼트에만 국한되지 않고, 모든 구성 요소를 드롭다운 필터에 포함할 수 있습니다.
2. 구성 요소 그룹을 &#39;여기에 세그먼트 놓기&#39;라는 작업 공간 영역으로 끌어 놓습니다. 이동하기 전에 Shift 키를 누릅니다.

이제 이 [!UICONTROL Workspace] 프로젝트에 액세스하는 사용자는 이 드롭다운을 사용하여 세그먼트 또는 다른 구성 요소를 프로젝트에 적용할 수 있습니다. 자세한 내용은 Adobe Analytics 도구 안내서의 [패널 개요](/help/analyze/analysis-workspace/c-panels/panels.md)를 참조하십시오.

**이전에는 차원 항목을 클릭해서 드릴다운을 확인했습니다. Analysis Workspace에서 이러한 간편한 워크플로를 복제하려면 어떻게 합니까?**

또한 [!UICONTROL Analysis Workspace]의 차원 항목에는 간편한 분류 워크플로가 있습니다. 마우스 왼쪽 버튼 대신 마우스 오른쪽 버튼을 클릭하여 액세스합니다. 차원 항목을 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL 분류]를 클릭한 후 원하는 구성 요소를 선택합니다. 각 값을 ctrl+클릭 (Windows)하거나 cmd+클릭 (Mac)하여 여러 차원 항목에 동일한 분류를 적용할 수 있습니다.
