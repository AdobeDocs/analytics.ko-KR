---
title: Launch를 사용한 구현 개요
description: Adobe Experience Platform Launch를 사용하여 Adobe Analytics를 구현하는 방법을 알아봅니다.
translation-type: ht
source-git-commit: d1db8da65faac1bf09fa2a290a2645092b542a35

---


# Launch를 사용한 구현 개요

Adobe Analytics의 서비스 제공 기간 동안 Adobe는 데이터 수집을 위해 사이트에서 코드를 구현하는 여러 가지 방법을 제공했습니다. Adobe의 현재 추천 방법은 Adobe Experience Platform Launch를 사용하는 것입니다.

Launch는 다른 태그 지정 요구 사항과 함께 Analytics 코드를 배포할 수 있도록 해주는 태그 관리 솔루션입니다. Adobe는 다른 솔루션 및 제품과의 통합을 제공하며 사용자 지정 코드를 배포할 수 있도록 해줍니다. 따라서 사이트에서 코드를 업데이트하기 위해 조직의 개발 팀에 의존하지 않고도 이러한 모든 작업을 수행할 수 있습니다.

유효한 Adobe Experience Cloud 계약을 보유한 모든 고객은 Launch를 사용할 수 있습니다. 액세스 권한이 있는지 확실하지 않은 경우 조직의 Experience Cloud 시스템 관리자에게 문의하십시오.

## 전체 워크플로우

Launch를 사용하여 구현을 실행하는 절차는 다음과 같습니다.

1. **Launch 액세스 권한 얻기**: 조직의 시스템 관리자를 통해 Launch 액세스 권한을 받습니다.
2. **속성 만들기**: 속성은 태그 관리 데이터를 참조하는 데 사용되는 매우 중요한 컨테이너입니다.
3. **개발 환경에 배포**: 태그 개발을 반복적으로 수행할 수 있는 환경을 마련합니다.
4. **유효성 검사 및 프로덕션에 게시**: 모든 것이 제대로 작동하는지 확인한 후 실시간으로 게시하십시오.

시작하려면 [Adobe Experience Platform Launch에서 Analytics 속성 만들기](create-analytics-property.md)를 참조하십시오.

## 추가 리소스

Launch를 사용자 지정할 수 있습니다. 구현에 적합한 데이터를 포함하여 Adobe Analytics를 최대한 활용할 수 있는 방법에 대해 자세히 알아봅니다.

* [Launch 설명서](https://docs.adobe.com/content/help/ko-KR/launch/using/overview.html): 인터페이스 작동 방식과 사용 가능한 확장에 대해 알아봅니다.
* [Adobe Analytics 확장](https://docs.adobe.com/content/help/ko-KR/launch/using/extensions-ref/adobe-extension/analytics-extension/overview.html): Analytics 확장을 사용하여 데이터를 Adobe Analytics에 보냅니다.
* [구현 변수](../vars/overview.md): 데이터 수집 서버에 전송할 변수를 결정합니다.
