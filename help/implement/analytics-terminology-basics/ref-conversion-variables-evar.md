---
description: 사용자 지정 인사이트 전환 변수(또는 eVar)는 사이트에서 선택된 웹 페이지의 Adobe 코드에 삽입됩니다. eVar의 기본 목적은 사용자 지정 마케팅 보고서의 전환 성공 지표를 세그먼트화하는 것입니다.
keywords: Analytics 구현;eVar;전환 변수;eVar 값;전환;성공 이벤트
seo-description: 사용자 지정 인사이트 전환 변수(또는 eVar)는 사이트에서 선택된 웹 페이지의 Adobe 코드에 삽입됩니다. eVar의 기본 목적은 사용자 지정 마케팅 보고서의 전환 성공 지표를 세그먼트화하는 것입니다.
seo-title: 전환 변수(eVar)
solution: Analytics
title: 전환 변수(eVar)
topic: 개발자 및 구현
uuid: 50071c1c-be00-4b3a-a7ee-5d129acf498b
translation-type: tm+mt
source-git-commit: 57fe1f6d613b9f54a5191ac8684d36bccfebf4e5

---


# 전환 변수(eVar)

사용자 지정 인사이트 전환 변수(또는 eVar)는 사이트에서 선택된 웹 페이지의 Adobe 코드에 삽입됩니다. eVar의 기본 목적은 사용자 지정 마케팅 보고서의 전환 성공 지표를 세그먼트화하는 것입니다.

eVar는 다음과 같은 원인과 결과를 측정하는 데 가장 적절하게 사용됩니다.

* 매출액에 영향을 준 내부 캠페인
* 등록에 결정적인 영향을 준 배너 광고
* 주문을 하기 전에 내부 검색을 사용한 횟수

>[!IMPORTANT]
>
>Analytics를 구현할 때 사용할 eVar 및 개수를 알아야 합니다. 관리 콘솔에서 그러한 eVar를 구성하는 방법도 알고 있어야 합니다. eVar에 대한 자세한 내용은 Analytics 도움말 및 참조서에서 [변환 변수(eVar)](https://marketing.adobe.com/resources/help/en_US/reference/conversion_var_admin.html)를 참조하십시오.

eVar는 방문 기준이며 쿠키와 유사한 기능을 수행할 수 있습니다. eVar 변수로 전달된 값은 사전 결정된 기간 동안 사용자를 따릅니다.

eVar이 방문자에 대한 값으로 설정될 때 Adobe는 값이 만료될 때까지 해당 값을 자동으로 기억합니다. eVar 값이 활성일 때 방문자가 발견하는 성공 이벤트는 eVar 값으로 카운트됩니다.

> [!NOTE] 단일 값만 이미지 요청 시 eVar에 저장할 수 있습니다. eVar 값에 여러 값을 사용할 수 있는 경우 [](/help/implement/js-implementation/c-variables/page-variables.md)목록 변수(list vars)를 구현하는 것이 좋습니다.

변수에 대한 자세한 내용은 다음을 참조하십시오.

* [이 도움말의](/help/implement/js-implementation/c-variables/sc-variables.md) Analytics 구현 및 보고에 대한 변수
* [변수 - 변수가 보고에 사용되는 방법](https://marketing.adobe.com/resources/help/en_US/reference/variable_definitions.html)
* [페이지 변수](/help/implement/js-implementation/c-variables/page-variables.md)
* [캠페인 변수](/help/implement/js-implementation/c-variables/page-variables.md)
* [products 변수](/help/implement/js-implementation/c-variables/page-variables.md)
* 모바일 SDK 설명서의 [제품 변수](https://marketing.adobe.com/resources/help/en_US/mobile/android/products.html)

