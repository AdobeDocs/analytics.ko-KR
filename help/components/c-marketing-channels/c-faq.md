---
description: 마케팅 채널용으로 설정할 수 있는 다양한 규칙을 채우는 방법에 대한 우수 사례 및 예제를 참조하십시오.
title: 마케팅 채널 FAQ 및 예제
translation-type: tm+mt
source-git-commit: 21f4b9df688776f7a1db96f76e258031ae3abb3d

---


# 마케팅 채널 FAQ 및 예제

See [Create Marketing Channel Processing Rules](/help/components/c-marketing-channels/c-rules.md) for definitions of fields displayed on the [!UICONTROL Marketing Channel Processing Rules] page.

## FAQ {#faq}

모든 마케팅 채널 처리 규칙 구현은 추적 코드에 따라 다를 수 있습니다. 원하는 결과를 제공하는 규칙을 구성하려면 문제 해결을 위한 어느 정도의 창의적인 사고가 필요할 수 있습니다.

**질문**: 내 추적 코드가 패턴을 따르지 않으며, 제휴 채널에 대해 지정해야 하는 코드가 수천 개나 있습니다.

*  제거 프로세스를 사용하십시오. 이메일 및 제휴 채널에서 동일한 쿼리 문자열 매개 변수를 사용하지만 몇 개의 이메일 추적 코드만 있는 경우에는 email을 정의하는 규칙 세트에 이메일 추적 코드를 지정할 수 있습니다. 그런 다음 *`affiliates.`*
* 이메일 시스템에서 쿼리 문자열 매개 변수를 모든 랜딩 페이지 URL에 추가합니다(예: *`&ch=eml`*). ch 쿼리 매개 변수가 *`eml`*. *`eml`*&#x200B;이 포함되어 있지 않다면 이 규칙 세트는 제휴입니다.

**질문**: 참조 도메인에 예상보다 많은 데이터가 있습니다.

* 처리 규칙 목록에서 참조 도메인이 너무 클 수 있습니다. 처리 순서가 중요하므로 마지막 규칙 세트 중 하나여야 합니다.

**질문**: 쿼리 문자열 매개 변수와 일치하는 규칙을 만들었지만 해당 규칙이 작동하지 않습니다.

*  쿼리 문자열 매개 변수 필드에 매개 변수 이름(보통 영숫자 값)이 지정되어 있고 매개 변수 값이 연산자 뒤에 있는지 확인하십시오(다음 이메일 규칙 예 참조).

   ![](assets/example_email.png)

**질문**: 내가 마지막으로 접촉한 트래픽이 내부 도메인에 귀속되는 이유는 무엇입니까?

*  내부 트래픽에 일치하는 규칙을 가지고 있는 것입니다. 방문자가 사용자 사이트에서 만든 모든(첫 방문만이 아닌) 히트에 대해 이러한 규칙이 처리된다는 점을 염두에 두십시오. 다른 기준 없이 *`Page URL exists`* 와 같은 규칙을 가지고 있는 경우, 페이지 URL이 항상 존재하기 때문에 해당 채널은 사용자 사이트의 연속되는 각 히트에 대해 일치합니다.

**질문**: 보고서에서 [식별된 채널 없음]에 표시되는 트래픽을 디버깅하려면 어떻게 합니까?

*  규칙은 순서대로 처리됩니다. 특정 기준이 일치하지 않으면 히트가 다음 세 가지 카테고리 중 하나에 속하게 됩니다.

1. 레퍼러 없음(직접 방문)

2. 방문 첫 페이지의 내부 레퍼러

3. 페이지의 작은 문제 처리

다음 세 가지 가능성에 대한 채널이 있는지 확인합니다. 예를 들어 다음과 같은 규칙을 만듭니다.

1. **[!UICONTROL Referrer]** 및 **[!UICONTROL Does Not Exist]** 를 **[!UICONTROL Is First Page of Visit]**&#x200B;참조하십시오. [직접 방문](/help/components/c-marketing-channels/c-faq.md) 참조.

2. **[!UICONTROL Referrer Matches Internal URL Filters]** 및 **[!UICONTROL Is First page of Visit]**. ([내부 방문](/help/components/c-marketing-channels/c-faq.md) 참조)

3. **[!UICONTROL Referrer]** 및 **[!UICONTROL Exists]** 를 **[!UICONTROL Referrer Does Not Match Internal URL Filters]**&#x200B;참조하십시오.

끝으로, [식별된 채널 없음](/help/components/c-marketing-channels/c-faq.md#no-channel-identified)에 설명된 대로, 나머지 히트를 캡처하는 *다른* 채널을 만듭니다.

## 식별된 채널 없음 {#no-channel-identified}

When your rules do not capture data, or if rules are not configured correctly, the report displays the data in the [!UICONTROL No Channel Identified] row on the report. 가령 처리 순서의 끝에, 내부 트래픽까지 식별하는 *기타*&#x200B;라는 규칙 세트를 만들 수 있습니다.

![](assets/example_other.png)

This kind of rule serves as a catch-all to ensure that channel traffic always matches external traffic, and typically does not end up in **[!UICONTROL No Channel Identified]**. 내부 트래픽까지 식별하는 규칙을 만들지 않도록 주의하십시오. Setting the channel&#39;s value to **[!UICONTROL Referring Domain]** or to **[!UICONTROL Page URL]** are the most common, useful ways to create an effective Other rule.

> [!NOTE] 식별된 채널 없음 카테고리에 포함될 수 있는 일부 채널 트래픽이 아직 있을 수 있습니다. 예: 방문자가 사이트를 방문하고 페이지를 책갈피로 지정한 다음 책갈피를 통해 동일한 방문 내에서 페이지로 다시 돌아옵니다. 방문의 첫 페이지가 아니므로 참조 도메인이 없기 때문에 직접 채널이나 기타 채널로 이동하지 않습니다.

## 유료 검색 {#paid-search}

유료 검색은 검색 결과에 배치하기 위해 검색 엔진에 비용을 지불하는 단어 또는 구문입니다. To match paid search detection rules, the marketing channel uses settings configured on the [!UICONTROL Paid Search Detection] page. ( **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Paid Search Detection]**). 대상 URL은 해당 검색 엔진에 대한 기존 유료 검색 감지 규칙을 일치시킵니다.

For the marketing channel rule, the [!UICONTROL Paid Search] settings are as follows:

![](assets/example_paid_search.png)

자세한 내용은 관리의 [유료 검색 감지](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/paid-search-detection/paid-search-detection.html)를 참조하십시오.

## 자연어 검색 {#natural-search}

자연어 검색은 비용을 지불하지 않고 검색 엔진이 사이트 등급을 지정하는 웹 검색을 통해 방문자가 웹사이트를 찾을 때 발생합니다. 검색 엔진이 사이트에 연결하는 데 사용하는 대상 URL을 제어할 수 있습니다. 이 URL을 사용하면 Analytics에서 검색이 자연어인지를 식별할 수 있습니다.

Analytics에는 자연어 검색 감지 기능이 없습니다. 유료 검색 감지가 설정되면 검색 레퍼러가 유료 검색 레퍼러가 아닌 경우 시스템에서 자연어 검색 레퍼러로 인식합니다. 자연어 검색의 경우, 대상 URL은 해당 검색 엔진에 대한 기존 유료 검색 탐지 규칙을 일치시키지 않습니다.

마케팅 채널 규칙의 경우, 자연어 검색 설정은 다음과 같습니다.

![](assets/example_natural_search.png)

자세한 내용은 관리의 [유료 검색 감지](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/paid-search-detection/paid-search-detection.html)를 참조하십시오.

## 제휴 {#afilliates}

제휴 규칙은 지정된 참조 도메인에서 온 방문자를 식별합니다. 규칙에서, 추적할 방문자의 제휴의 도메인을 다음과 같이 나열합니다.

![](assets/example_affiliates.png)

## 소셜 네트워크 {#social-networks}

이 규칙은 Facebook* 같은 소셜 네트워크에서 온 방문자를 식별합니다. 설정은 다음과 같습니다.

![](assets/example_social.png)

## 표시 {#display}

이 규칙은 배너 광고로부터 온 방문자를 식별합니다. 대상 URL의 쿼리 문자열 매개 변수( *`Ad_01`*.

![](assets/example_display.png)

## 내부 {#internal}

이 규칙은 보고서 세트에 대한 내부 URL 필터를 일치시키는 레퍼러를 통해서 온 방문자를 식별합니다.

![](assets/example_internal.png)

## 이메일 {#email}

이 규칙을 설정하려면 이메일 캠페인에 대한 쿼리 문자열 매개 변수를 제공합니다. 이 예에서 매개 변수는 *`eml`*:

![](assets/example_email.png)

규칙에 추적 코드가 포함된 경우, 여기 보여진 것처럼 라인당 하나의 값을 입력하십시오.

![](assets/tracking_code.png)

## 직접 {#direct}

이 규칙은 참조 도메인이 없는 방문자를 식별합니다. 이 규칙에는 즐겨찾기 링크를 사용하거나 링크를 브라우저에 붙여 넣는 방식으로 직접 사이트를 방문한 방문자가 포함됩니다.

![](assets/example_direct.png)

