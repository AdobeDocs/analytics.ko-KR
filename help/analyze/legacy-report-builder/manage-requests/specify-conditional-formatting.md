---
description: 조건부 서식을 통합 문서 셀에 적용하는 방법을 알아봅니다.
title: 통합 문서의 조건부 서식 정보
uuid: 13ac12f1-3498-4bf9-a6d0-c5d84e0125dc
feature: Report Builder
role: User, Admin
exl-id: 5a5f2415-8269-4c8a-9193-784537b29edf
source-git-commit: fcecc8a493852f5682fd7fbd5b9bb484a850922c
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 32%

---

# 조건부 서식 지정

{{legacy-arb}}

포함된 요청이 있는 보고서를 만든 후 조건부 서식을 통합 문서 셀에 적용할 수 있습니다.

Report Builder 도구 모음에서 **[!UICONTROL 서식]**&#x200B;을 클릭합니다.

조건부 서식을 사용하면 모니터링할 결과 또는 값이 들어 있는 셀을 식별할 수 있습니다. 예를 들어 매출액이 예상치보다 낮은 경우 특정 셀에 빨간색 음영 또는 강조 표시를 적용하고 매출액이 예상한 금액을 초과하는 경우 파란색 음영을 적용할 수 있습니다. 요청의 날짜 범위가 변경되어 조건부 서식을 셀 값에 적용하게 되는 조건이 제거되면 해당 조건을 강조 표시하는 형식이 일시적으로 비활성화됩니다. 조건을 충족하지 못하여 지정한 조건부 서식이 변경되지 않으면 조건부 서식은 셀을 제거할 때까지 셀에 계속 적용됩니다.

보안상의 이유로 Excel의 VBA(Visual Basic for Applications) 언어를 사용하여 통합 문서 매크로를 작성하면 매크로를 사용할 수 없습니다.

>[!NOTE]
>
>조건부 서식은 Excel 기능입니다. 서식 규칙 만들기에 대한 자세한 내용은 Excel 설명서를 참조하십시오.
