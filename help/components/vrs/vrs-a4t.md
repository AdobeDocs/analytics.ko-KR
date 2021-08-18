---
description: 'A4T 및 Adobe Analytics 가상 보고서 세트를 사용할 때의 특별한 고려 사항 '
title: 가상 보고서 세트 및 Target 분석(A4T)
source-git-commit: 6a47ebc58cb36079940cfc4e5cdc80cf99c18a50
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# 가상 보고서 세트 및 Target 분석(A4T)

Adobe Target 컨텍스트에서 가상 보고서 세트를 사용할 때는 다음 주의 사항을 고려하십시오.

* 데이터를 Target에서 가상 보고서 세트로 직접 보낼 수 없으며 실제 보고서 세트로만 보낼 수 없습니다.
* 가상 보고서 세트 내에서 A4T 활동에 대해 보고할 수 있습니다. 그러나 A4T 데이터는 가상 보고서 세트 세그먼트와 일치하는 행(및 적용된 다른 세그먼트)으로 제한됩니다. 예를 들어 EMEA 고객을 위해 가상 보고서 세트를 만든 경우 해당 가상 보고서 세트의 A4T 데이터는 EMEA 고객을 위한 Target 데이터만 반영합니다.
* 가상 보고서 세트의 세그먼트를 활성화를 위해 Target에 다시 게시할 수 없습니다.