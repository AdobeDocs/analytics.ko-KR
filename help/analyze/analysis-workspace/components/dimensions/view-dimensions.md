---
description: Analysis Workspace에서 차원의 세부 정보와 상위 값을 보는 방법에 대해 알아봅니다.
title: 차원 미리 보기
feature: Dimensions
role: User, Admin
exl-id: 897edc76-6744-4d8c-ab0e-20672838f7b3
source-git-commit: ff38740116ac6f12033ebdc17cffa3250a30f3f7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 4%

---

# 차원 미리보기

구성 요소에 대한 [구성 요소 정보](/help/analyze/analysis-workspace/components/use-components-in-workspace.md#component-info)를 사용하여 차원의 상위 항목을 표시할 수 있습니다.

![구성 요소 정보](assets/component-info.png)

<!--
Now, by default, we show dynamic values instead of static ones, with the option to turn them into static values. Other things to note:

* As your data updates, the dynamic dimension columns will update to show the current 5/15 dimension items.
* A dynamic dimension column that is copied or moved will become static.
* When hovering a static dimension column you will see a lock icon, indicating that the dimension is static.

![Dimension column popup highlighting the lock icon.](assets/dimension_static.png)

-->


## 차원 항목 표시

구성 요소 패널에서 차원에 대해 ![V자형 화살표](/help/assets/icons/ChevronRight.svg)를 선택하면 해당 차원 항목 목록이 나타납니다. 차원 항목 목록에는 일반적으로 지난 30일 동안의 상위 항목이 표시됩니다. 더 많은 항목을 사용할 수 있는 경우 패널에 대해 선택한 날짜 범위를 벗어나면 링크를 선택하여 더 많은 항목을 표시합니다. 예를들어 **[!UICONTROL 지난 달의 항목을 표시]**&#x200B;합니다.

![차원 항목 표시](assets/dimension-items.png)


<!--
# Preview dimensions

Hover over the information (i) icon next to a dimension. This shows the top 5 values for non-time dimensions (and 15 for time dimensions). We used to keep those values static (i.e., the 5 values picked never changed).

![](assets/dimension-preview.png)

Now, by default, we show dynamic values instead of static ones, with the option to turn them into static values. Other things to note:

* As your data updates, the dynamic dimension columns will update to show the current 5/15 dimension items.
* A dynamic dimension column that is copied or moved will become static.
* When hovering a static dimension column you will see a lock icon, indicating that the dimension is static.

![](assets/dimension_static.png)

## Show dimension items

When you hover over a dimension and click the grey right-arrow next to it, a list of its dimension items appears. Any list of dimension items usually shows the top items for the last 30 days.

If you scroll down to the bottom of the list, you see **[!UICONTROL Show Top Items From Last 18 Months]**. Click this option to see top dimension items from the last 547 days.

-->
