---
description: 관리자는 데이터 사전 상태를 모니터링할 책임이 있습니다. 여기에는 구성 요소가 데이터를 수집 중인지, 승인되었는지, 설명이 들어 있는지, 그리고 중복되지 않았는지 등이 포함됩니다.
title: 데이터 사전 상태 모니터링
feature: Components
role: Admin
source-git-commit: 5bfbc3059526527e35f26b750d048efebee68e9e
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# 데이터 사전 상태 모니터링

{{release-limited-testing}}

Analytics 관리자는 건강한 데이터 사전을 유지 관리할 책임이 있습니다.

## 건강정보 사전의 특성

건강한 데이터 사전은 모든 구성 요소 중 하나입니다.

* 사용 중이며 데이터를 수집하고 있습니다.

* 유용한 설명을 포함하여 사용자가 설명을 가장 잘 사용하는 방법을 알 수 있습니다

* 불필요한 중복이 없습니다.

* 관리자가 승인

## 데이터 사전의 상태를 확인합니다

데이터 사전에서 상태 문제를 식별하려면

1. Analysis Workspace 프로젝트를 엽니다.

1. Analysis Workspace 왼쪽의 데이터 사전 아이콘을 선택합니다. (데이터 사전에 액세스하는 다른 방법은 [데이터 사전 개요](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md))

   데이터 사전 창이 표시됩니다.

   ![데이터 사전 관리 보기](assets/data-dictionary-admin.png)

1. 드롭다운 메뉴에서 올바른 보고서 세트가 선택되었는지 확인합니다.

1. 설정 [!UICONTROL **사전 상태**] 탭, 선택 [!UICONTROL **보기**] 다음 옵션 옆에 있습니다.

   * [!UICONTROL **구성 요소에 설명이 없습니다.**]

   * [!UICONTROL **구성 요소가 중복 항목을 가지고 있습니다**]

   * [!UICONTROL **구성 요소가 연결된 데이터가 없습니다.**]

   선택한 내용에 따라 적절한 필터가 데이터 사전에 적용되며 관련 구성 요소만 표시됩니다.

1. 데이터 사전의 상태를 개선하려면 구성 요소를 편집합니다. 데이터 사전에서 구성 요소를 편집하는 방법에 대한 자세한 내용은 [데이터 사전에서 구성 요소 항목 편집](/help/analyze/analysis-workspace/components/data-dictionary/edit-entries-data-dictionary.md).