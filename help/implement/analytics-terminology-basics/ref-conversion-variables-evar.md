---
description: 사용자 지정 인사이트 전환 변수(또는 eVar)는 사이트에서 선택된 웹 페이지의 Adobe 코드에 삽입됩니다. eVar의 기본 목적은 사용자 지정 마케팅 보고서의 전환 성공 지표를 세그먼트화하는 것입니다.
keywords: Analytics 구현; Evar; 전환 변수; Evar 값; 전환; 성공 이벤트
seo-description: 사용자 지정 인사이트 전환 변수(또는 eVar)는 사이트에서 선택된 웹 페이지의 Adobe 코드에 삽입됩니다. eVar의 기본 목적은 사용자 지정 마케팅 보고서의 전환 성공 지표를 세그먼트화하는 것입니다.
seo-title: 전환 변수 (Evar)
solution: Analytics
title: 전환 변수 (Evar)
topic: 개발자 및 구현
uuid: 50071 c 1 c-be 00-4 b 3 a-a 7 ee -5 d 129 acf 498 b
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 전환 변수 (Evar)

사용자 지정 인사이트 전환 변수(또는 eVar)는 사이트에서 선택된 웹 페이지의 Adobe 코드에 삽입됩니다. eVar의 기본 목적은 사용자 지정 마케팅 보고서의 전환 성공 지표를 세그먼트화하는 것입니다.

eVar는 다음과 같은 원인과 결과를 측정하는 데 가장 적절하게 사용됩니다.

* 매출액에 영향을 준 내부 캠페인
* 등록에 결정적인 영향을 준 배너 광고
* 주문을 하기 전에 내부 검색을 사용한 횟수

>[!IMPORTANT]
>
>Analytics 구현 시, 어떤 evar를 사용할지, 그리고 얼마나 많은 evar를 사용하는지 아는 것이 중요합니다. 관리 콘솔에서 그러한 eVar를 구성하는 방법도 알고 있어야 합니다. eVar에 대한 자세한 내용은 Analytics 도움말 및 참조서에서 [변환 변수(eVar)](https://marketing.adobe.com/resources/help/en_US/reference/conversion_var_admin.html)를 참조하십시오.

eVar는 방문 기준이며 쿠키와 유사한 기능을 수행할 수 있습니다. eVar 변수로 전달된 값은 사전 결정된 기간 동안 사용자를 따릅니다.

eVar이 방문자에 대한 값으로 설정될 때 Adobe는 값이 만료될 때까지 해당 값을 자동으로 기억합니다. eVar 값이 활성일 때 방문자가 발견하는 성공 이벤트는 eVar 값으로 카운트됩니다.

>[!NOTE]
>
>단일 값만 이미지 요청의 Evar에 저장할 수 있습니다. eVar 값에 여러 값을 사용할 수 있는 경우 [](/help/implement/js-implementation/c-variables/page-variables.md)목록 변수(list vars)를 구현하는 것이 좋습니다.

변수에 대한 자세한 내용은 다음을 참조하십시오.

* [이 도움말의](../../implement/js-implementation/c-variables/sc-variables.md#concept_E10E43221A2740FAAF900B79CE1EC5FB) Analytics 구현 및 보고에 대한 변수
* [변수 - 변수가 보고에 사용되는 방법](https://marketing.adobe.com/resources/help/en_US/reference/variable_definitions.html)
* [페이지 변수](/help/implement/js-implementation/c-variables/page-variables.md)
* [캠페인 변수](/help/implement/js-implementation/c-variables/page-variables.md)
* [products 변수](/help/implement/js-implementation/c-variables/page-variables.md)
* 모바일 SDK 설명서의 [제품 변수](https://marketing.adobe.com/resources/help/en_US/mobile/android/products.html)

