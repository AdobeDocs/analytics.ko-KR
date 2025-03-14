---
description: 보고서 처리 시간은 데이터를 비파괴적이고 소급적인 방식으로 처리할 수 있는 가상 보고서 세트 설정입니다.
title: 보고서 처리 시간
role: Admin
solution: Analytics
feature: VRS
exl-id: 3742b9d1-f1fb-4690-bd44-b4719ff9d9bc
source-git-commit: 08e29da4847e8ef70bd4435949e26265d770f557
workflow-type: tm+mt
source-wordcount: '1319'
ht-degree: 71%

---

# 보고서 처리 시간

[!UICONTROL 보고서 처리 시간]은(는) Analysis Workspace의 데이터를 비파괴적이고 소급적인 방식으로 처리할 수 있는 가상 보고서 세트 설정입니다.

[!UICONTROL 보고서 처리 시간] 가상 보고서 세트의 데이터에만 영향을 주고 기본 보고서 세트의 데이터 또는 데이터 수집에는 영향을 주지 않습니다. [!UICONTROL 보고서 처리 시간]과 기존 Analytics 처리 간의 차이점은 다음 다이어그램을 사용하여 가장 잘 이해할 수 있습니다.

![기존 처리 파이프라인](assets/google1.jpg)

Analytics 데이터 처리 중 데이터는 데이터 수집 파이프라인을 통해 보고를 위한 데이터를 준비하는 사전 처리 단계로 흐릅니다. 이 사전 처리 단계는 데이터가 수집될 때 방문 만료 논리 및 eVar 지속성 논리(여러 가지 말 중에서도)를 해당 데이터에 적용합니다. 이 사전 처리 모델의 주요 단점은 데이터를 수집하기 전에 미리 구성해야 한다는 것입니다. 이는 사전 처리 설정의 모든 변경 사항은 해당 시점부터 새 데이터에만 적용됨을 의미합니다. 데이터 도착이 잘못되거나 설정이 잘못 구성된 경우 문제가 발생합니다.

[!UICONTROL 보고서 처리 시간]은 보고를 위해 Analytics 데이터를 처리하는 근본적으로 다른 방법입니다. 데이터를 수집하기 전에 처리 논리를 미리 결정하는 대신 Analytics는 사전 처리 단계에서 데이터 세트를 무시하고 보고서가 실행될 때마다 이 논리를 적용합니다.

![파이프라인 처리 시간 보고](assets/google2.jpg)

이 처리 아키텍처는 훨씬 더 유연한 보고 옵션을 제공합니다. 예를 들어 방문 시간 초과 기간을 비파괴적인 방식으로 원하는 기간으로 변경할 수 있으며 이러한 변경 사항은 전체 보고 기간 동안 eVar 지속성 및 세그먼트 컨테이너에 반영됩니다. 또한 기본 보고서 세트의 데이터를 변경하지 않고 동일한 기본 보고서 세트를 기반으로 각각 다양한 보고서 처리 시간 옵션이 있는 가상 보고서 세트를 원하는 만큼 만들 수 있습니다.

[!UICONTROL 보고서 처리 시간]을 사용하면 Analytics에서 배경 히트가 새로운 방문을 시작하지 못하도록 차단하고 [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/mobile.html?lang=ko-KR)에서는 앱 실행 이벤트가 발생할 때마다 새로운 방문을 시작할 수 있습니다.

## 구성 옵션

보고서 처리 시간이 활성화된 가상 보고서 세트에서는 현재 다음 구성 옵션을 사용할 수 있습니다.

* **[!UICONTROL 방문 시간 초과]:** 방문 시간 제한 설정은 새 방문이 자동으로 시작되기 위해 필요한 고유 방문자의 비활성 시간의 크기를 정의합니다. 기본값은 30분입니다. 예를 들어 방문 시간 제한을 15분으로 설정하면 15분의 비활동 상태로 구분되는 수집된 일련의 히트마다 새로운 방문 그룹이 생성됩니다. 이 설정은 방문 카운트뿐 아니라 방문 세그먼트 컨테이너를 평가하는 방법 및 방문 시 만료되는 eVar에 대한 방문 만료 논리에도 영향을 줍니다. 방문 시간 제한을 줄이면 보고의 총 방문 횟수가 늘어나고 방문 시간 제한을 늘리면 보고의 총 방문 횟수가 줄어들 수 있습니다.
* **[!UICONTROL 모바일 앱 방문 설정]:** [Adobe Mobile SDK](https://experienceleague.adobe.com/docs/mobile.html?lang=ko-KR)를 통해 모바일 앱에서 생성된 데이터가 들어 있는 보고서 세트에 대해 추가적인 방문 설정을 사용할 수 있습니다. 이 설정은 비파괴적이고 Mobile SDK를 통해 수집된 히트에만 영향을 줍니다. 또한 Mobile SDK의 외부에서 수집된 데이터에는 영향을 주지 않습니다.
* **[!UICONTROL 배경 히트 수로 새로운 방문이 시작되지 않도록 차단]:** 배경 히트 수는 앱이 배경 상태일 때 Mobile SDK에 의해 수집됩니다.
* **[!UICONTROL 앱 실행 시마다 새 방문 시작]:** 방문 시간 제한 외에도 비활성 창에 관계없이 Mobile SDK에서 앱 실행 이벤트가 기록될 때마다 방문이 시작되도록 할 수 있습니다. 이 설정은 eVar의 방문 만료 논리뿐 아니라 방문 지표 및 방문 세그먼트 컨테이너에도 영향을 줍니다.
* **[!UICONTROL 이벤트로 새 방문 시작]:** 세션 시간이 초과되었는지 여부에 관계없이 이벤트가 발생하면 새 세션이 시작됩니다. 새로 생성된 세션에는 세션을 시작한 이벤트가 포함됩니다. 또한 여러 이벤트를 사용하여 세션을 시작할 수 있으며, 새 세션은 데이터에서 이러한 이벤트가 관찰되면 시작됩니다. 이 설정은 방문 카운트, 방문 세그먼테이션 컨테이너 및 eVar의 방문 만료 논리에 영향을 줍니다.


>[!BEGINSHADEBOX]

데모 비디오는 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [이벤트로 새 방문 시작](https://video.tv.adobe.com/v/23129?quality=12&learn=on){target="_blank"}을 참조하세요.

>[!ENDSHADEBOX]



## 보고서 시간 처리 제한 사항

보고서 처리 시간이 기존 Analytics 보고에서 사용 가능한 모든 지표 및 차원을 지원하는 것은 아닙니다. 보고서 처리 시간을 활용하는 가상 보고서 세트는 Analysis Workspace에서만 액세스할 수 있으며 Data Warehouse, Report Builder, 데이터 피드 또는 Reporting API에서는 액세스할 수 없습니다.

또한 보고서 처리 시간은 보고 날짜 범위 (이하 &quot;날짜 범위&quot;) 내에 발생하는 데이터만 처리합니다. 이는 보고 날짜 범위 이전의 방문자에 대해 &quot;만료 기간 제한 없음&quot;으로 설정된 eVar 값은 보고 날짜 범위까지 지속되지 않으며 보고서에 나타나지 않음을 의미합니다. 이는 또한 고객 충성도 측정이 보고 날짜 범위 이전의 전체 기록이 아닌, 보고 날짜 범위에 있는 데이터에만 기반함을 의미합니다.

다음 차원 및 지표는 보고서 처리 시간에서 지원되지 않습니다.

* **Target용 Analytics**
* **Advertising Cloud 차원/지표에 대한 분석**
* **카운터 eVar**
* [**첫 구매까지 소요된 일 수**](/help/components/dimensions/days-before-first-purchase.md)
* [**마지막 구매 이후 일 수**](/help/components/dimensions/days-since-last-purchase.md)
* [**마지막 방문 이후 일 수**](/help/components/dimensions/days-since-last-visit.md)
* **원래 시작 페이지**
* **선형 할당 eVar**
* **목록 변수**
* [**마케팅 채널 차원**](/help/components/dimensions/marketing-channel.md)
* [**최초 참조 도메인**](/help/components/dimensions/original-referring-domain.md)
* [**반환 주기**](/help/components/dimensions/return-frequency.md)
* [**단일 액세스**](/help/components/metrics/single-access.md)
* **거래 ID 데이터 원본**
* [**방문 번호**](/help/components/dimensions/visit-number.md)

## 영향을 받는 차원 및 지표

다음은 선택한 보고서 처리 시간 설정에 따라 영향을 받는 차원 및 지표 목록입니다.

* 배경 히트 수로 새로운 방문이 시작되지 않도록 차단이 활성화되면 다음 변경 사항이 발생합니다. 자세한 내용은 [컨텍스트 인식 세션화](vrs-mobile-visit-processing.md)를 참조하십시오.
   * [**바운스 수**](/help/components/metrics/bounces.md) / [**바운스 수:**](/help/components/metrics/bounce-rate.md) 전경 히트가 따르지 않는 배경 히트는 바운스 수로 간주되지 않으며 바운스 수에 기여하지 않습니다.
   * [**방문 당 초 단위 체류 시간:**](/help/components/metrics/time-spent-per-visit.md) 전경 히트를 포함하는 방문만 이 지표에 기여합니다.
   * **방문 당 체류 시간:** 전경 히트를 포함하는 방문만 이 지표에 기여합니다.
   * [**시작 지표**](/help/components/metrics/entries.md) / [**종료 지표:**](/help/components/metrics/exits.md) 전경 히트가 발생한 방문의 시작 및 종료만 이 차원에 표시됩니다.
   * [**시작 차원**](/help/components/dimensions/entry-dimensions.md) / [**종료 차원:**](/help/components/dimensions/exit-dimensions.md) 전경 히트가 발생한 방문의 시작 및 종료만 이 차원에 표시됩니다.
   * [**고유 방문자 수 지표:**](/help/components/metrics/unique-visitors.md) 고유 방문자 수는 보고 기간에 배경 히트 수만 기록한 방문자를 포함하지 않습니다.
* [**방문 횟수:**](/help/components/metrics/visits.md) 방문 횟수는 가상 보고서 세트가 구성한 설정을 반영하며 기본 보고서 세트와는 다를 수 있습니다.
* **이벤트 ID가 있는 일련화된 이벤트:** 이벤트 ID와 함께 이벤트 일련화를 사용하는 이벤트는 한 방문자의 보고 기간 내에 발생하는 이벤트들에 대해서만 중복이 제거됩니다. 이러한 이벤트는 보고서 처리 시간 날짜 범위로 인해 전역적으로 모든 날짜 또는 방문자에 대해서는 중복 제거되지 않습니다.
* **구매** / [**매출**](/help/components/metrics/revenue.md) / [**주문**](/help/components/metrics/orders.md) / [**단위:**](/help/components/metrics/units.md) 구매 ID가 사용되는 경우 이러한 지표는 보고서 처리 시간 날짜 범위로 인해 전역적으로 모든 날짜 또는 방문자가 아닌 한 방문자의 보고 날짜 범위 내에 발생하는 중복 구매 ID에 대해서만 중복이 제거됩니다.
* [**비머천다이징 eVar**](/help/components/dimensions/evar.md) / **예약된 eVar:** eVar에 설정된 값은 보고서 처리 시간 날짜 범위로 인해 해당 값이 보고 날짜 범위 내에 설정된 경우에만 지속됩니다. 또한 지속 시간이 일광 절약 시간 변경까지 지속되는 경우 시간 기반 만료는 한 시간 일찍 또는 한 시간 늦게 만료될 수 있습니다.
* [**머천다이징 eVar**](/help/components/dimensions/evar-merchandising.md) / **예약된 eVar:** 위 내용을 참조하십시오. 또한 전환 구문의 경우, 바인딩이 &#39;모든 이벤트&#39;로 설정되어 있으면 &#39;모든 히트&#39;가 대신 사용됩니다.
* [**히트 유형:**](/help/components/dimensions/hit-type.md) 이 차원은 히트가 전경인지 배경인지를 지정합니다.
* **(낮은 트래픽) 또는 “고유 수 초과됨” 차원:** (낮은 트래픽) 라인 항목은 보고서 처리 시간을 사용할 때 약간 다르게 결정되며 기본 보고서 세트에서 보고할 때 관찰되는 항목과 일치하지 않습니다. 낮은 트래픽에 속하지 않는 Dimension 라인 항목은 해당 라인 항목에 대한 데이터의 100%를 나타낼 수 없습니다. 이러한 차이는 차원에 고유 값의 수가 많을수록 더욱 뚜렷해질 수 있습니다.
