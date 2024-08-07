---
description: 특정 차원에 대한 다음 또는 이전 차원 항목을 표시하는 패널입니다.
title: 다음 또는 이전 항목 패널
feature: Panels
role: User, Admin
exl-id: 9f2f8134-2a38-42bb-b195-5e5601d33c4e
source-git-commit: d173a6c6c9751a86f4218ec842da17da14f8485b
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 6%

---

# 다음 또는 이전 항목 패널

이 패널에는 특정 차원에 대한 다음 또는 이전 차원 항목을 쉽게 식별할 수 있는 많은 표와 시각화가 포함되어 있습니다. 예를 들어 고객이 홈 페이지를 방문한 후 가장 자주 방문한 페이지를 탐색할 수 있습니다.

## 패널 액세스

[!UICONTROL 보고서] 또는 [!UICONTROL Workspace] 내에서 패널에 액세스할 수 있습니다.

| 액세스 지점 | 설명 |
| --- | --- |
| [!UICONTROL 보고서] | <ul><li>패널이 이미 프로젝트에 드롭되었습니다.</li><li>왼쪽 레일이 무너졌습니다.</li><li>[!UICONTROL 다음 페이지]을(를) 선택한 경우 [!UICONTROL Dimension Dimension]의 경우 [!UICONTROL 페이지], [!UICONTROL 방향]의 경우 [!UICONTROL 다음], [!UICONTROL 컨테이너]의 경우 [!UICONTROL 방문]과 같이 기본 설정이 이미 적용되었습니다.  이 모든 설정을 수정할 수 있습니다.</li></ul>![다음/이전 패널](assets/next-previous.png) |
| 작업 영역 | 새 프로젝트를 만들고 왼쪽 레일에서 패널 아이콘을 선택합니다. 그런 다음 [!UICONTROL 다음 또는 이전 항목] 패널을 자유 형식 테이블 위로 드래그합니다. [!UICONTROL Dimension] 및 [!UICONTROL Dimension 항목] 필드가 비어 있습니다. 드롭다운 목록에서 차원을 선택합니다. [!UICONTROL Dimension 항목]은(는) 선택한 [!UICONTROL 차원]을(를) 기반으로 채워집니다. 상위 차원 항목이 추가되지만 다른 항목을 선택할 수 있습니다. 기본값은 다음 및 방문자입니다. 이러한 매개 변수도 수정할 수 있습니다.<p>![다음/이전 패널](assets/next-previous2.png) |

{style="table-layout:auto"}

## 패널 입력 {#Input}

다음 입력 설정을 사용하여 [!UICONTROL 다음 또는 이전 항목] 패널 패널을 구성할 수 있습니다.

| 설정 | 설명 |
| --- | --- |
| 세그먼트(또는 기타 구성 요소) 드롭 영역 | 세그먼트 또는 다른 구성 요소를 드래그하여 놓아 패널 결과를 추가로 필터링할 수 있습니다. |
| 차원 | 다음 또는 이전 항목을 탐색할 차원입니다. |
| 차원 항목 | 다음/이전 문의 중심에 있는 특정 항목. |
| 방향 | [!UICONTROL 다음] 또는 [!UICONTROL 이전] 차원 항목을 찾고 있는지 여부를 지정하십시오. |
| 컨테이너 | [!UICONTROL Visit] 또는 [!UICONTROL Visitor](기본값)에서 조회 범위를 결정합니다. |

{style="table-layout:auto"}

패널을 빌드하려면 **[!UICONTROL 빌드]**&#x200B;를 클릭하십시오.

## 패널 출력 {#output}

[!UICONTROL 다음 또는 이전 항목] 패널은 특정 차원 항목의 다음 또는 이전 발생 횟수를 더 잘 이해할 수 있도록 풍부한 데이터 및 시각화를 반환합니다.

![다음/이전 패널 출력](assets/next-previous-output.png)

![다음/이전 패널 출력](assets/next-previous-output2.png)

| 시각화 | 설명 |
| --- | --- |
| 가로 막대 | 선택한 차원 항목을 기반으로 다음(또는 이전) 항목을 나열합니다. 개별 막대에 마우스를 가져다 대면 자유 형식 테이블에서 해당 항목이 강조 표시됩니다. |
| 요약 번호 | 현재 월에 대한 모든 다음 또는 이전 차원 항목 발생의 높은 수준 요약 번호(현재까지)입니다. |
| 자유 형식 테이블 | 선택한 차원 항목을 기반으로 다음(또는 이전) 항목을 테이블 형식으로 나열합니다. 예를 들어, 사람들이 홈 페이지 또는 작업 영역 페이지 뒤(또는 이전)로 이동한 가장 방문 빈도가 높은 페이지(발생 횟수별)입니다. |

{style="table-layout:auto"}
