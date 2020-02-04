---
title: 론치 개요로 구현
description: Adobe Experience Platform Launch를 사용하여 Adobe Analytics를 구현하는 방법 살펴보기
translation-type: tm+mt
source-git-commit: d1db8da65faac1bf09fa2a290a2645092b542a35

---


# 론치 개요로 구현

Adobe Analytics의 수명 동안 Adobe는 데이터 수집을 위해 사이트에서 코드를 구현하는 여러 가지 방법을 제공했습니다. Adobe의 현재 추천 방법은 Adobe Experience Platform Launch를 통해 제공됩니다.

Launch는 다른 태그 지정 요구 사항과 함께 Analytics 코드를 배포할 수 있는 태그 관리 솔루션입니다. Adobe는 다른 솔루션 및 제품과의 통합을 제공하며 사용자 정의 코드를 배포할 수 있습니다. 조직의 모든 개발 팀이 사이트의 코드를 업데이트하지 않아도 이러한 모든 작업을 수행할 수 있습니다.

유효한 Adobe Experience Cloud 계약을 보유한 모든 고객은 Launch를 사용할 수 있습니다. 액세스 권한이 있는지 확실하지 않은 경우 조직의 Experience Cloud 시스템 관리자에게 문의하십시오.

## 전체 워크플로우

Launch를 사용하여 구현을 실행하면 다음 단계가 수행됩니다.

1. **Launch에 액세스 권한**&#x200B;확보:조직의 시스템 관리자를 통해 Launch에 액세스할 수 있습니다.
2. **속성**&#x200B;만들기:속성은 태그 관리 데이터를 참조하는 데 사용되는 컨테이너 오버레이입니다.
3. **개발 환경에**&#x200B;배포:태그 개발을 반복적으로 수행할 수 있는 환경이 있습니다.
4. **프로덕션**&#x200B;확인 및 게시:모든 것이 제대로 작동하는지 확인한 다음 실시간으로 게시할 수 있습니다.

시작하려면 [Adobe Experience Platform Launch에서](create-analytics-property.md) Analytics 속성 만들기를 참조하십시오.

## 추가 리소스

Launch를 사용자 정의할 수 있습니다. 구현에 적합한 데이터를 포함하여 Adobe Analytics를 최대한 활용하는 방법에 대한 자세한 내용을 살펴보십시오.

* [설명서](https://docs.adobe.com/content/help/en/launch/using/overview.html)시작:인터페이스 작동 방식과 사용 가능한 익스텐션에 대해 알아봅니다.
* [Adobe Analytics 확장](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/analytics-extension/overview.html):Analytics 확장을 사용하여 데이터를 Adobe Analytics로 보냅니다.
* [구현 변수](../vars/overview.md):데이터 수집 서버로 전송할 변수를 결정합니다.
