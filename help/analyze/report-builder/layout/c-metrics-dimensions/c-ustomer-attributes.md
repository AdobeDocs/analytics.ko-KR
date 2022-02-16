---
description: 사용자 특성은 VisAttr이라는 새로운 유형의 요소에 저장되며 이것은 차원이나 지표로 구성할 수 있습니다.
title: 고객 속성
feature: Report Builder
role: User, Admin
exl-id: b5855ce0-6d17-4690-a2c2-366b66ab8e83
source-git-commit: 4daa5c8bdbcb483f23a3b8f75dde9eeb48516db8
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 100%

---

# 고객 속성

사용자 특성은 VisAttr이라는 새로운 유형의 요소에 저장되며 이것은 차원이나 지표로 구성할 수 있습니다.

사용자 특성을 업로드하는 방법에 대한 자세한 내용은 [Experience Cloud 도움말](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html?lang=ko-KR)을 참조하십시오.

* VisAttr을 지표로 구성하는 경우 &quot;차원&quot;과 지표 모두로 노출됩니다.

   ![](assets/ca_metrics.png) ![](assets/ca_dimension.png)

* eVar와 동일한 분류를 지원합니다(모두를 무엇으로든 분류 가능).
* VisAttr은 모든 eVar 지표를 지원합니다.
* 지표로서의 VisAttr은 &quot;버킷화&quot;(0~ 30, 31~ 60 등 사이트에서 보낸 시간)를 지원합니다.
* VisAttr은 세그멘테이션 차원으로 사용할 수 있습니다.
