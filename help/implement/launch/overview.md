---
title: Adobe Experience Platform에서 태그를 사용하여 Adobe Analytics 구현
description: 태그를 사용하는 Adobe Analytics 구현 방법 알아보기
feature: Launch Implementation
exl-id: 52990731-8a68-4779-ad42-6ec94b0aabd1
source-git-commit: 99fc7814eaa12d0d9e8e478629a4c2134a577aaa
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Adobe Experience Platform에서 태그를 사용하여 Adobe Analytics 구현

Adobe Analytics의 서비스 제공 기간 동안 Adobe는 데이터 수집을 위해 사이트에서 코드를 구현하는 여러 가지 방법을 제공했습니다. Adobe의 현재 권장 방법은 Adobe Experience Platform의 태그를 사용하는 것입니다.

Adobe Experience Platform의 태그는 다른 태그 지정 요구 사항과 함께 Analytics 코드를 배포할 수 있도록 해 주는 태그 관리 솔루션입니다. Adobe는 다른 솔루션 및 제품과의 통합을 제공하며 사용자 지정 코드를 배포할 수 있도록 해 줍니다. 따라서 사이트에서 코드를 업데이트하기 위해 조직의 개발 팀에 의존하지 않고도 이러한 모든 작업을 수행할 수 있습니다.

활성 Adobe Experience Cloud 계약을 보유한 모든 고객은 태그를 사용할 수 있습니다. 액세스 권한이 있는지 확실하지 않은 경우 조직의 Experience Cloud 시스템 관리자에게 문의하십시오.

## 전체 워크플로

태그를 사용하여 구현을 실행하는 방법은 다음 단계를 따르십시오.

1. **태그에 대한 액세스 권한 획득**: 조직 내 시스템 관리자를 통해 Platform 태그에 대한 액세스 권한을 획득할 수 있습니다.
2. **태그 속성 만들기**: 속성은 태그 관리 데이터를 참조하는 데 사용하는 중요한 컨테이너입니다.
3. **개발 환경에 배포**: 태그 개발을 반복적으로 수행할 수 있는 환경을 마련합니다.
4. **유효성 검사 및 프로덕션에 게시**: 모든 것이 제대로 작동하는지 확인한 후 실시간으로 게시하십시오.

시작하려면 [Analytics 태그 속성 만들기](create-analytics-property.md)를 참조하십시오.

## 추가 리소스

태그는 높은 자유도로 사용자 지정할 수 있습니다. 구현에 적합한 데이터를 포함하여 Adobe Analytics를 최대한 활용할 수 있는 방법에 대해 자세히 알아봅니다.

* [태그 설명서](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=ko-KR#): 인터페이스의 작동 방식과 이요 가능한 확장 유형에 대해 알아봅니다.
* [Adobe Analytics 확장](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html?lang=ko-KR): Analytics 확장을 사용하여 데이터를 Adobe Analytics에 보냅니다.
* [구현 변수](../vars/overview.md): 데이터 수집 서버에 전송할 변수를 결정합니다.
