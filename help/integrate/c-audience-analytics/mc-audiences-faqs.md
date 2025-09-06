---
description: Audience Analytics을 구현할 때 나올 수 있는 질문에 대한 답변입니다.
solution: Experience Cloud
title: Audience Analytics에 대해 자주 묻는 질문
feature: Audience Analytics
exl-id: 86e7967c-030c-44d6-8294-e7e6d41f6fc3
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '1090'
ht-degree: 31%

---

# FAQ

Audience Analytics을 구현할 때 나올 수 있는 질문에 대한 답변입니다.

## 법적 FAQ {#legal}

+++ 내 Analytics 데이터에 PII (개인 식별 정보)가 있는지 어떻게 알 수 있습니까? 그렇다면 어떻게 해야 합니까?

prop 또는 eVar에 이메일/주소 등이 있는 경우 수집하는 동안 데이터를 해싱하는 것이 좋습니다. 해당 국가에서 IP 주소를 PII로 고려하는 경우 [IP 난독화를 켭니다](/help/admin/tools/exclude-ip.md). 수집 중인 항목을 확인하려면 Analytics 관리자에게 문의하십시오. 법무 부서에 문의하여 PII에 대해 어떻게 생각하는지 확인하십시오.

+++

+++ 보고서 세트에서 온사이트 개인화를 수행하는지 아니면 오프사이트/온사이트 타기팅을 수행하는지 어떻게 알 수 있습니까?

이러한 사항은 Adobe Analytics 데이터를 Adobe Audience Manager으로 전송하는 데는 적용되지 않습니다. 자문해 보십시오.

* Analytics 공유 세그먼트를 MCA 차원과 다시 Experience Cloud으로 공유하시겠습니까?

* 이러한 목적에 사용되는 BI (비즈니스 인텔리전스) 시스템으로 데이터 피드 등을 통해 내보내시겠습니까?

+++

## Adobe Audience Manager 관련 FAQ {#aam-specific}

+++ Audience Manager에서 Analytics 대상을 만들려면 어떻게 합니까?

[Adobe Audience Manager에서 Analytics 대상 구성](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/experience-cloud-destinations/create-analytics-destination.html?lang=ko-KR)&quot;을 참조하십시오.

+++

+++ Analytics 대상을 만들고 저장한 후 선택한 보고서 세트에 데이터가 표시되려면 얼마나 걸립니까?

새 데이터로 보고서 세트를 채우는 데 몇 시간이 걸릴 수 있습니다.

+++

+++ 새 Analytics 대상을 만들었지만 사용 가능한 세그먼트의 대상 매핑 섹션에 표시되지 않습니다. 그 목적지는 어디로 갔나요, 아니면 어떻게 찾을 수 있나요?

**[!UICONTROL 세그먼트 매핑]**&#x200B;에서 **[!UICONTROL 자동으로 모든 현재 및 향후 세그먼트 매핑]** 옵션을 선택하면 세그먼트의 대상 매핑 섹션에서 Analytics 대상이 사라집니다. 이를 방지하려면 자동 옵션 대신 **[!UICONTROL 수동으로 세그먼트 매핑]**&#x200B;을 선택하십시오.

+++

이렇게 하면 Analytics의 Adobe Audience Manager에서 모든 정보를 제공합니까?

아니요. Audience Manager 대상 지원 중 또는 후에 그리고 세그먼트 선별 중/후에 사이트를 방문한 사람과 관련된 데이터만 제공합니다.

+++

+++ 이렇게 하면 세그먼트당 총 주소 지정 가능한 대상이 제공됩니까?

실제로 그렇지 않습니다. 세그먼트 선별 중 또는 후에 사이트로 돌아온 해당 세그먼트의 방문자 수를 알려 줍니다.

+++

+++ Analytics에 대한 기존 쿠키 대상과 어떻게 다릅니까?

세그먼트는 자격이 있고 동일한 히트에서 실시간으로 반환됩니다. 친숙한 이름이 자동으로 표시됩니다.

+++

+++ 내 보고서 세트 중 일부에 개인 데이터가 있고 다른 일부는 없는 경우 어떻게 합니까?&lt;

팁: 두 개의 대상을 만들어 한 대상에는 개인 데이터 보고서 세트를 추가하고 다른 대상에는 비개인 데이터 보고서 세트를 추가합니다.

+++

## Analytics 관련 FAQ {#aa-specific}

+++ 이 통합은 Analytics에서 차원 또는 세그먼트로 표시됩니까?

차원으로: 대상 ID 및 대상 이름.

+++

+++Analytics에서 이러한 차원을 사용할 수 있는 곳은 어디입니까?

모든 곳에서, Analytics에서 수집된 다른 차원과 마찬가지로 처리됩니다.

+++

+++ Analytics에 데이터가 전달되지 않는 이유는 무엇입니까?

데이터 소스와 대상 간에 Adobe Audience Manager 개인정보 컨트롤이 충돌할 수 있습니다.

+++

+++ 모든 세그먼트를 보내도록 선택했지만, 일부 세그먼트가 Analytics에 표시되지 않는 이유는 무엇입니까?&lt;

* 대상 및 세그먼트의 데이터 소스에 있는 Adobe Audience Manager 데이터 내보내기 컨트롤이 충돌하여 특정 세그먼트가 전송되지 않을 수 있습니다.

* 세그먼트에서 서드파티 데이터 트레이트를 사용하는 경우 해당 세그먼트를 개인 데이터가 포함된 대상 (보고서 세트)에 공유할 수 없습니다.

+++

+++ 내 Analytics 보고서에 &quot;대상 제한에 도달했습니다.&quot;가 표시되는 이유는 무엇입니까? (참고: 이 값은 Data Warehouse에서도 Audience ID = -1 및 `::max_audiences_exceeded::`(으)로 표시됩니다.)

기본적으로 Adobe Audience Manager용 Audience Analytics 통합은 방문자가 적격한 모든 세그먼트를 히트별로 Analytics에 보냅니다. 방문자가 단일 히트에서 150개가 넘는 Adobe Audience Manager 세그먼트에 속하는 경우 **가장 최근에 자격을 얻은 세그먼트**&#x200B;이(가) Analytics로 전송되고, 나머지 목록은 잘립니다. 세그먼트 목록이 잘렸음을 나타내는 추가 플래그가 Analytics에 전송되고, 대상자 이름 차원에 “대상자 한도 도달”로 표시되고 대상자 ID 차원에 “-1”로 표시됩니다.

방문자가 특정 히트에서 150개 이상의 세그먼트에 대해 자격을 얻는 것은 거의 불가능하지만 가끔 발생할 수 있습니다. 보고서에 “대상자 한도 도달” 메시지가 표시되면 다음 두 가지 옵션을 사용할 수 있습니다.

* 옵션 1: 특정 방문자에 대해 가장 최근에 자격을 갖춘 150개의 세그먼트를 보내면서 통합이 기본 제공 상태에서 작동하도록 계속 합니다.

* 옵션 2: Adobe Audience Manager에서 통합을 위해 비즈니스에 가장 중요한 150개의 세그먼트를 선택합니다. 그런 다음 Adobe Audience Manager은 해당 150개 세그먼트에 대해서만 방문자를 확인합니다. 이 방법의 단점은 모든 방문자에 대해 그러한 150개의 세그먼트만 수신한다는 것입니다. 반면에 옵션 1 방법은 통합의 히트별 특성으로 인해 세그먼트를 무제한으로 전달할 수 있습니다.

+++

+++ 이 통합에 대해 추가 서버 호출이 Analytics에 청구됩니까?

아니요. Adobe Audience Manager 대상은 Analytics 히트 서버측에 통합됩니다. 이 경우 Analytics에 대한 추가 서버 호출이 발생하지 않습니다(기본 또는 보조).

+++

## SSF (서버측 전달) FAQ {#SSF}

+++ 기존 SSF가 구현된 경우 Analytics 관리로 이동하여 보고서 세트 SSF도 켜야 합니까?

예. Adobe Audience Manager 대상 설정에서 SSF가 켜진 보고서 세트만 표시됩니다.

+++

+++ Analytics 관리자의 SSF에 대한 특정 보고서 세트를 켤 수 없는 이유는 무엇입니까?

Experience Cloud 조직에 매핑된 세트만 활성화할 수 있습니다.

이 항목에 대한 자세한 FAQ는 [서버측 전달 FAQ](/help/admin/tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf-faq.md)를 참조하십시오.

+++

## 일반 FAQ {#section_E55410BBFB624AAFB87ADCF7F036DDA3}

+++ Audience Manager과 Analytics 간에 세그먼트 방문자 수가 다른 이유는 무엇입니까?

[방문자 수 차이](/help/integrate/c-audience-analytics/visitor-count-reconciliation.md)를 참조하십시오.

+++

+++ Adobe Audience Manager의 &quot;대상&quot;과 Analytics의 &quot;세그먼트&quot; 간의 차이점은 무엇입니까?

[Analytics 및 Audience Manager의 세그먼트 이해](/help/integrate/c-audience-analytics/aam-analytics-segments.md)를 참조하십시오. Adobe Audience Manager 대상자는 Analytics에서 사용할 &quot;차원&quot; 구성 요소로 전송되고 공유됩니다. 이러한 세그먼트는 세그먼트 빌더에서 세그먼트 등으로 표시되지 않고 세그먼트를 작성할 수 있는 차원으로 표시됩니다.

+++

+++ Adobe Audience Manager에서 통합된 고객 특성과 고객 데이터의 차이점은 무엇입니까?

고객 속성은 시간을 기반으로 하지 않습니다. 소급하여 적용됩니다. Adobe Audience Manager 통합 데이터는 시간 기반이며 앞으로 나아갈 때에만 사용됩니다. 또한 고객 속성은 Experience Cloud 방문자 ID에 대한 조회 테이블이지만, Adobe Audience Manager 통합은 방문자에 대한 각 히트에 결합된 데이터입니다.

+++

+++ 이전 Beta 또는 컨설팅 플러그인 쿠키 대상 등, 이 문제에 대한 기존 접근 방식은 어떻게 됩니까?

새 통합을 구현하고 이전 대상을 제거하는 것이 좋습니다.

+++
