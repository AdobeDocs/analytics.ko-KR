---
title: 다양한 구현 유형 추적
description: 서로 다른 구현 유형을 사용하고 이러한 유형 간에 방문자를 원활하게 추적합니다.
feature: Implementation Basics
exl-id: 18aa5595-d2a7-4df2-a4ef-a5040c097483
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: ht
source-wordcount: '102'
ht-degree: 100%

---

# 다양한 구현 유형 추적

이 정보는 보고와 구현 모두에 능숙한 고급 사용자를 위한 것입니다. 발생할 수 있는 모든 결과에 대해 알고 있지 않다면 구현을 편집하지 마십시오. 구현 변경이 필요한 경우에는 조직의 계정 관리자에게 문의하십시오.

두 개 이상의 구현 유형을 사용하는 경우에는 (JavaScript와 하드 코드 이미지 요청 등) 다음 변수가 지정되어 있으며 서로 일치하는지 확인하십시오.

* *`s_account`*
* *`s.visitorNamespace`*
* *`s.trackingServer`*
* *`s.trackingServerSecure`*  (SSL을 사용하는 경우)

각각의 변수가 구현 간에 일치하지 않는 경우 사용자가 독립된 방문자로 추적될 수 있습니다.
