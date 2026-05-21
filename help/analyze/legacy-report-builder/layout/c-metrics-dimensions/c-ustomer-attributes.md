---
description: 고객 속성은 VisAttr이라는 새로운 유형의 요소에 저장되며 이것은 차원이나 지표로 구성할 수 있습니다.
title: 고객 속성
feature: Report Builder
role: User, Admin
exl-id: b5855ce0-6d17-4690-a2c2-366b66ab8e83
TQID: https://experienceleague.adobe.com/J-KoYBPg-bECW1utOk2L0YLtBWd9-jHT6gwAEm54fs4
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 7d733a6375f6c6009563bc53f5a3ff090dbc48ed
workflow-type: tm+mt
source-wordcount: 135
ht-degree: 69%

---

# 고객 속성

{{legacy-arb}}

고객 속성은 VisAttr이라는 새로운 유형의 요소에 저장되며 이것은 차원이나 지표로 구성할 수 있습니다.

고객 특성을 업로드하는 방법에 대한 자세한 내용은 [CX Enterprise 도움말](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html)을 참조하십시오.

* 지표로 구성된 경우 VisAttr은 지표와 &quot;차원&quot;으로 모두 노출됩니다.

  ![지표 및 차원 고객 특성을 보여 주는 스크린샷입니다.](assets/ca_metrics.png) ![](assets/ca_dimension.png)

* eVar와 동일한 분류를 지원합니다(모두를 무엇으로든 분류 가능).
* VisAttr은 모든 eVar 지표를 지원합니다.
* 지표로서의 VisAttr은 &quot;버킷화&quot;(0~ 30, 31~ 60 등 사이트에서 보낸 시간)를 지원합니다.
* VisAttr은 세그멘테이션 차원으로 사용할 수 있습니다.
