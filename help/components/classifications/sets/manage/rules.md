---
title: 분류 세트 규칙
description: 개별 분류 세트에 대한 규칙을 보고 편집합니다.
exl-id: 1ccb6a20-1993-4fd3-90eb-9154d12d0ec7
feature: Classifications
source-git-commit: de12253f6db798f49d0cae34bf9cb6b7a3de17db
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 1%

---

# 분류 세트 규칙

분류 세트 규칙을 사용하면 변수가 설정된 값을 기준으로 값을 자동으로 분류할 수 있습니다. 이러한 규칙은 분류 세트의 모든 가입에 대한 모든 수신 변수 값에 적용됩니다.

**[!UICONTROL 구성 요소]** > **[!UICONTROL 분류 세트]** > **[!UICONTROL 세트]** > 원하는 분류 세트 이름 클릭 > **[!UICONTROL 규칙]**

![분류 집합 규칙 UI](../../assets/csets-rules.png)

## 규칙 설정

전체 규칙 세트에 적용되는 설정입니다.

* **[!UICONTROL 규칙 덮어쓰기]**: 분류 값이 있는 경우 모든 규칙의 동작을 결정합니다.
   * **[!UICONTROL 모든 값에 적용]**: 규칙이 일치하는 경우 항상 분류 값을 덮어씁니다.
   * **[!UICONTROL 설정이 해제된 값에만 적용]**: 규칙이 일치하는 경우 비어 있는 경우에만 분류 값을 작성하십시오. 분류 값이 있으면 아무 작업도 하지 마십시오.
* **[!UICONTROL 전환 확인 기간]**: 이 규칙이 활성화되면 모든 규칙은 여기에 설정된 전환 확인 기간 내에 표시되는 모든 고유 값에 대해 실행됩니다.

## 규칙

각 고유 값에 대해 실행되는 규칙 목록입니다.

* **[!UICONTROL 검색]**: 일치 조건으로 규칙을 필터링할 수 있는 검색 상자입니다.
* **[!UICONTROL 규칙 추가]**: 규칙 테이블에 빈 행을 추가합니다.
* **[!UICONTROL 테스트 규칙 집합]**: 규칙의 유효성을 검사할 수 있는 테스트 UI를 표시합니다. 왼쪽에서 수동으로 키 값을 입력하거나 분류 파일을 드래그 앤 드롭하여 테스트할 많은 값을 가져올 수 있습니다. 오른쪽에는 규칙 세트가 활성화된 경우 분류된 값이 어떤 모습인지에 대한 사전 결과를 보여주는 테이블이 있습니다. 이 인터페이스는 유효성 검사용으로만 사용되므로 값이 분류되지 않습니다.

원하는 규칙 옆에 있는 확인란을 클릭하여 하나 이상의 규칙을 선택합니다. 규칙을 선택하면 다음 옵션이 표시됩니다.

* **[!UICONTROL 삭제]**: 규칙 테이블에서 행을 삭제합니다.
* **[!UICONTROL 복제]**: 선택한 행을 규칙 테이블의 새 행에 복사합니다.

## 규칙 테이블

규칙 테이블은 일치하는 조건과 분류 작업이라는 두 가지 주요 부분으로 세로로 구분됩니다. 각 행(개별 규칙)에는 일치하는 조건 및 분류 작업이 포함되어 있습니다.

* **규칙 번호**: 규칙은 규칙 테이블을 구성하는 순서와 동일한 순서로 실행됩니다. [!UICONTROL 규칙 덮어쓰기]가 [!UICONTROL 모든 값에 적용]&#x200B;(으)로 설정된 경우 마지막으로 일치하는 규칙이 동일한 분류 차원에 대한 이전 규칙을 덮어씁니다. [!UICONTROL 규칙 덮어쓰기]가 [!UICONTROL 설정이 해제된 값에만 적용]&#x200B;(으)로 설정된 경우 분류 값을 설정하는 첫 번째 규칙이 적용됩니다.
* **[!UICONTROL 규칙 유형 선택]**: 규칙 기준입니다. 옵션에는 [!UICONTROL 포함], [!UICONTROL 다음으로 끝남], [!UICONTROL 정규식], [!UICONTROL 정규식] 및 [!UICONTROL 다음으로 시작]이 있습니다.
* **[!UICONTROL 일치 조건을 입력하십시오]**: 일치시킬 텍스트 문자열입니다. 규칙 유형으로 [!UICONTROL 정규 표현식]을(를) 선택하면 값을 입력하고 정규 표현식을 테스트하며 샘플 구문을 제공하는 오버레이가 나타납니다.
* **[!UICONTROL 분류 설정]**: 값을 할당할 분류 차원을 설정하는 드롭다운 목록입니다. 유효한 옵션에는 [스키마](schema.md)의 요소가 포함됩니다.
* **[!UICONTROL To]**: 분류된 값을 설정할 텍스트 문자열입니다. 규칙 유형이 [!UICONTROL 정규 표현식]인 경우 텍스트와 일치 그룹의 조합을 포함할 수 있습니다.
