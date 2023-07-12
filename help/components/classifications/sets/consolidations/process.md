---
title: 분류 세트 통합 프로세스
description: 분류 세트를 통합하는 전체 프로세스
exl-id: 315d45fa-2819-4778-a88e-65a7cce64148
feature: Classifications
source-git-commit: c697530103ea7cd279cc3560c1daec796759e7a1
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# 분류 세트 통합 프로세스

이 인터페이스를 사용하여 처음부터 끝까지 분류 세트 통합을 생성합니다.

## 생성

**[!UICONTROL 구성 요소]** > **[!UICONTROL 분류 세트]** > **[!UICONTROL 통합]** > **[!UICONTROL 추가]**

통합을 생성할 때 사용할 수 있는 필드는 다음과 같습니다.

* **[!UICONTROL 이름]**: 통합의 이름입니다.
* **[!UICONTROL 문제 알림]**: 이 통합과 관련된 문제를 알리는 쉼표로 구분된 이메일 주소 목록입니다.
* **[!UICONTROL 일치시킬 데이터 세트]**: 모든 분류 세트의 드롭다운 목록입니다.

분류 세트를 선택하면 두 개의 열이 있는 테이블이 나타납니다.

* 오른쪽 열에는 통합할 모든 분류 세트가 포함되어 있습니다. 위의 드롭다운 목록을 사용하여 선택한 분류 세트로 시작합니다.
* 왼쪽 열에는 원래 선택한 데이터 세트와 병합할 수 있는 모든 분류 세트가 포함되어 있습니다. **스키마가 정확히 일치해야 통합에 적합합니다.**. 스키마가 선택한 분류 세트와 일치하지 않으면 이 왼쪽 열에 표시되지 않습니다.

왼쪽의 사용 가능한 열에서 오른쪽의 통합 열로 원하는 분류 세트를 드래그합니다. 통합에 이름이 지정되고 오른쪽 열에 두 개 이상의 분류 세트가 있는 경우 **[!UICONTROL 저장 및 계속]**.

## 유효성 검사

통합을 만들면 소스 데이터 세트 목록이 오른쪽에 나타납니다. 다음 **[!UICONTROL 유효성 검사]** 버튼을 클릭하면 각 개별 분류 세트가 이 통합에 유효한지 확인할 수 있습니다. 여기에서 분류 단계를 재정렬하여 분류 값이 일치하지 않는 경우의 우선 순위를 결정할 수 있습니다. **목록에서 가장 높은 분류 세트는 다른 분류 세트의 일치하지 않는 값을 덮어씁니다.**

## 먼저

통합이 검증되면 이를 실행할 수 있습니다. 통합을 실행하면 다음 테이블 열이 있는 유사성 보고서가 제공됩니다.

* **[!UICONTROL 데이터 세트 이름]**: 분류 세트의 이름입니다.
* **[!UICONTROL 불일치]**: 키 값이 소스 분류 세트와 일치하지 않는 행의 백분율입니다. 불일치 비율이 높은 경우 분류 데이터가 너무 다를 수 있습니다. 선택한 분류 세트에 유사한 분류 데이터가 있는지 확인하십시오.
* **[!UICONTROL 결석]**: 해당 분류 세트에는 있지만 소스 분류 세트에는 없는 행의 백분율입니다. 없는 모든 행은 통합 분류 세트에 추가됩니다.

## 승인

개별 분류 세트를 제거하고 통합 분류 세트를 만들기 전에 마지막 호출로 작동합니다. 모든 항목이 올바른지 확인한 다음 **[!UICONTROL 승인]**.

승인되면 통합된 분류 세트가 생성됩니다. 상태가 (으)로 설정됩니다. [!UICONTROL 완료], 통합에 대해 추가적인 작업이 필요하지 않습니다.