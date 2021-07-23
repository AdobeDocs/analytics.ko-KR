---
title: Adobe Experience Platform에서 태그를 사용한 구현
description: 태그를 사용하여 Adobe Analytics을 구현하는 방법 알아보기
exl-id: 52990731-8a68-4779-ad42-6ec94b0aabd1
source-git-commit: 562ed0e190954b7687fa79efaf5c5c54eb202af8
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 43%

---

# Adobe Experience Platform에서 태그를 사용한 구현

>[!NOTE]
>Adobe Experience Platform Launch은 Experience Platform에서 데이터 수집 기술 세트로 브랜딩되었습니다. 그 결과 제품 설명서에서 몇 가지 용어 변경 사항이 롤아웃되었습니다. 용어 변경 내용을 통합 참조하려면 다음 [document](https://experienceleague.adobe.com/docs/experience-platform/tags/term-updates.html?lang=en)을 참조하십시오.

Adobe Analytics의 서비스 제공 기간 동안 Adobe는 데이터 수집을 위해 사이트에서 코드를 구현하는 여러 가지 방법을 제공했습니다. Adobe의 현재 추천 방법은 Adobe Experience Platform에서 태그를 사용하는 것입니다.

Adobe Experience Platform 데이터 컬렉션의 태그는 다른 태깅 요구 사항과 함께 Analytics 코드를 배포할 수 있도록 해주는 태그 관리 솔루션입니다. Adobe는 다른 솔루션 및 제품과의 통합을 제공하며 사용자 지정 코드를 배포할 수 있도록 해줍니다. 따라서 사이트에서 코드를 업데이트하기 위해 조직의 개발 팀에 의존하지 않고도 이러한 모든 작업을 수행할 수 있습니다.

유효한 Adobe Experience Cloud 계약을 보유한 모든 고객은 태그를 사용할 수 있습니다. 액세스 권한이 있는지 확실하지 않은 경우 조직의 Experience Cloud 시스템 관리자에게 문의하십시오.

## 전체 워크플로

태그를 사용하여 구현을 실행하는 절차는 다음과 같습니다.

1. **태그에 대한 액세스** 권한 얻기: 조직의 시스템 관리자를 통해 Platform 태그에 대한 액세스 권한을 얻을 수 있습니다.
2. **태그 속성을 만듭니다**. 속성은 태그 관리 데이터를 참조하는 데 사용되는 매우 중요한 컨테이너입니다.
3. **개발 환경에 배포**: 태그 개발을 반복적으로 수행할 수 있는 환경을 마련합니다.
4. **유효성 검사 및 프로덕션에 게시**: 모든 것이 제대로 작동하는지 확인한 후 실시간으로 게시하십시오.

시작하려면 [Analytics 태그 속성 만들기](create-analytics-property.md) 를 참조하십시오.

## 추가 리소스

태그는 사용자 지정할 수 있습니다. 구현에 적합한 데이터를 포함하여 Adobe Analytics를 최대한 활용할 수 있는 방법에 대해 자세히 알아봅니다.

* [태그 설명서](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=en#): 인터페이스 작동 방식과 사용 가능한 확장에 대해 알아봅니다.
* [Adobe Analytics 확장](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html?lang=en): Analytics 확장을 사용하여 데이터를 Adobe Analytics에 보냅니다.
* [구현 변수](../vars/overview.md): 데이터 수집 서버에 전송할 변수를 결정합니다.
