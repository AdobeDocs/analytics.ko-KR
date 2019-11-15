---
description: 가져오고 내보내는 파일에는 각 숫자 2 분류의 6개 열이 포함되어 있습니다.
solution: Analytics
subtopic: Classifications
title: 숫자 2 분류 가져오기
topic: Admin tools
uuid: 82a3034c-e002-4991-900f-22dd45d54910
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 숫자 2 분류 가져오기

>[!IMPORTANT]
>
>숫자 2와 활성화된 날짜 분류를 가져오는 기능이 코드 베이스에서 제거되었습니다. 이 변경 사항은 2019년 7월 유지 관리 릴리스에 적용됩니다. 가져온 파일에 숫자 또는 활성화된 날짜 열이 있는 경우 해당 셀은 자동으로 무시되며, 해당 파일의 다른 모든 데이터는 정상적으로 가져와집니다. 기존 분류는 여전히 표준 분류 워크플로우를 통해 내보낼 수 있으며, 보고에서 계속 사용할 수 있습니다.

가져오고 내보내는 파일에는 각 숫자 2 분류의 6개 열이 포함되어 있습니다.

다음 정의는 숫자 2 분류 이름이 MyCost라고 가정합니다.

**~MyCost:** 행의 설명적인 이름입니다.

**~~MyCost^~id**:기존 행을 편집하는 ID입니다. 새 행을 추가할 때 빈 칸이어야 합니다. 분류 관리자에서 내보낼 때 ID가 자동으로 할당됩니다.

**~~MyCost^~value**:행의 값입니다. 비율 열이 고정되면 이것은 전체 기간에 배포된 일반 값입니다. 비율 열이 이벤트이면 이것은 해당 이벤트의 승수입니다. 이 항목에는 쉼표(,)를 포함할 수 없습니다.

**~~MyCost^~period**:이 행이 대응하는 기간. 여기에는 대시로 구분된 시작 및 종료 날짜가 포함되어야 합니다. 대시는 공백으로 둘러싸야 합니다. 정의는 다음과 같은 형식이어야 합니다.

YYYY/MM/DD - YYYY/MM/DD

**~~MyCost^~rate**:값 열에 곱할 [!UICONTROL 이벤트입니다] . 유효한 값:

* fixed - 값이 기간 전체에 해당하는 일반 값임을 나타낼 때 사용됩니다.
* revenue
* order
* unit
* scOpen
* scviews
* instance
* click
* checkout
* scAdd
* scRemove
* event1
* event2
* etc

**~~MyCost^~hinge**:분류 중에 값을 배포하는 데 사용할 이벤트입니다. This value is often the same as [!UICONTROL ~MyCost^~rate~], unless you are using [!UICONTROL fixed]. The valid values for this column are identical to that of [!UICONTROL ~MyCost^~rate~], with the addition of [!UICONTROL none].
