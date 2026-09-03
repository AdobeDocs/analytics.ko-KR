---
description: A4T 및 Adobe Analytics 가상 보고서 세트를 사용할 때 특별한 고려 사항
title: Target(A4T)용 가상 보고서 세트 및 분석
feature: VRS
exl-id: b81e5100-f512-4219-a8ab-5d7f6219d206
TQID: https://experienceleague.adobe.com/SIJbZiyHFtGFUrlno5-Kov3kDP4QOXREW00jyDsIGFI
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 137
ht-degree: 100%

---

# Target(A4T)용 가상 보고서 세트 및 분석

Adobe Target과 관련하여 가상 보고서 세트를 사용할 때 다음 주의 사항을 고려하십시오.

* Target에서 가상 보고서 세트로 직접 데이터를 전송할 수 없으며 실제 보고서 세트로만 전송할 수 있습니다.
* 가상 보고서 세트 내에서 A4T 활동에 대해 보고할 수 있습니다. 그러나 A4T 데이터는 가상 보고서 세트 세그먼트(및 적용된 다른 세그먼트)와 일치하는 행으로 제한됩니다. 예를 들어 EMEA 고객을 위한 가상 보고서 세트를 만든 경우 해당 가상 보고서 세트의 A4T 데이터는 EMEA 고객을 위한 Target 데이터만 반영합니다.
* 활성화를 위해 가상 보고서 세트의 세그먼트를 대상으로 다시 게시할 수 없습니다.
