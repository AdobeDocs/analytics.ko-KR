---
description: 마케팅 채널용으로 설정할 수 있는 다양한 규칙을 채우는 방법에 대한 우수 사례 및 예제를 참조하십시오.
title: 마케팅 채널 FAQ 및 예제
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 마케팅 채널 FAQ 및 예제

See [Create Marketing Channel Processing Rules](/help/components/c-marketing-channels/c-rules.md) for definitions of fields displayed on the [!UICONTROL Marketing Channel Processing Rules] page.

## FAQ {#faq}

모든 마케팅 채널 처리 규칙 구현은 추적 코드에 따라 다를 수 있습니다. 원하는 결과를 제공하는 규칙을 구성하려면 문제를 해결하기 위해 창의적인 사고가 필요할 수 있습니다.

**질문**:내 추적 코드가 패턴을 따르지 않으며, 제휴 채널에 대해 지정해야 하는 코드가 수천 개 있습니다.

* 제거 프로세스를 사용합니다. 이메일 및 제휴 채널에서 동일한 쿼리 문자열 매개 변수를 사용하지만 몇 개의 이메일 추적 코드만 있는 경우 이메일을 정의하는 규칙 세트에 이메일 추적 코드를 지정할 수 있습니다. 그런 다음 *`affiliates.`*
* 이메일 시스템에서 쿼리 문자열 매개 변수를 모든 랜딩 페이지 URL에 추가합니다(예: *`&ch=eml`*). ch 쿼리 매개 변수가 *`eml`*. *`eml`*&#x200B;이 포함되어 있지 않다면 이 규칙 세트는 제휴입니다.

**질문**: 참조 도메인에 예상보다 많은 데이터가 있습니다.

* 처리 규칙 목록에서 참조 도메인이 너무 클 수 있습니다. 처리 순서는 중요하므로 마지막(또는 마지막) 규칙 세트 중 하나여야 합니다.

**질문**:쿼리 문자열 매개 변수와 일치하는 규칙을 만들었는데 작동하지 않습니다.

* 매개 변수 이름이 쿼리 문자열 매개 변수 필드(일반적으로 영숫자 값)에 지정되어 있는지 확인합니다. 또한 다음 이메일 규칙 예와 같이 매개 변수 값이 연산자 뒤에 지정되었는지 확인하십시오.

   ![](assets/example_email.png)

**질문**:마지막 접촉 트래픽이 모두 내부 도메인에 귀속되는 이유는 무엇입니까?

* 내부 트래픽과 일치하는 규칙이 있습니다. 이러한 규칙은 방문자가 사이트에서 수행하는 모든 히트에 대해 첫 번째 방문뿐만 아니라 처리된다는 점을 염두에 두십시오. If you have a rule like *`Page URL exists`* without other criteria, that channel is matched on each successive hit on your site, because a page URL always exists.

**질문**:보고서에서 식별된 채널 없음에 표시되는 트래픽을 디버깅하려면 어떻게 합니까?

* 규칙은 순서대로 처리됩니다. 특정 기준이 일치하지 않으면 히트는 다음 세 가지 카테고리 중 하나로 분류됩니다.

1. 레퍼러 없음(직접 방문)

2. 방문 첫 페이지의 내부 레퍼러

3. 페이지의 작은 문제 처리

이러한 세 가지 가능성을 위한 채널이 있는지 확인합니다. 예를 들어 다음과 같은 규칙을 만듭니다.

1. **[!UICONTROL Referrer]** 및 **[!UICONTROL Does Not Exist]** 를 **[!UICONTROL Is First Page of Visit]**&#x200B;참조하십시오. [직접 방문](/help/components/c-marketing-channels/c-faq.md) 참조.

2. **[!UICONTROL Referrer Matches Internal URL Filters]** 및 **[!UICONTROL Is First page of Visit]**. ([내부 방문](/help/components/c-marketing-channels/c-faq.md) 참조)

3. **[!UICONTROL Referrer]** 및 **[!UICONTROL Exists]** 를 **[!UICONTROL Referrer Does Not Match Internal URL Filters]**&#x200B;참조하십시오.

마지막으로 식별된 채널 *없음에 설명된 대로* 나머지 히트를 캡처하는 기타 [채널을 만듭니다](/help/components/c-marketing-channels/c-faq.md#no-channel-identified).

## No Channel Identified {#no-channel-identified}

규칙이 데이터를 캡처하지 않거나 규칙이 올바르게 구성되지 않은 경우 보고서에 보고서의 [!UICONTROL No Channel Identified] 행에 데이터가 표시됩니다. 예를 들어, 처리 *순서의*&#x200B;끝에 내부 트래픽도 식별하는 기타 규칙 세트를 만들 수 있습니다.

![](assets/example_other.png)

This kind of rule serves as a catch-all to ensure that channel traffic always matches external traffic, and typically does not end up in **[!UICONTROL No Channel Identified]**. 내부 트래픽까지 식별하는 규칙을 만들지 않도록 주의하십시오. Setting the channel&#39;s value to **[!UICONTROL Referring Domain]** or to **[!UICONTROL Page URL]** are the most common, useful ways to create an effective Other rule.

>[!NOTE] 식별된 채널 없음 카테고리에 포함될 수 있는 일부 채널 트래픽이 아직 있을 수 있습니다. 예:방문자가 사이트를 방문하여 페이지를 책갈피로 지정한 후 동일한 방문에서 책갈피를 통해 페이지가 다시 표시됩니다. 방문의 첫 번째 페이지가 아니므로 참조 도메인이 없기 때문에 직접 채널이나 기타 채널에서 이동하지 않습니다.

## 유료 검색 {#paid-search}

유료 검색은 검색 결과에 배치하기 위해 검색 엔진을 지불하는 단어 또는 구문입니다. 마케팅 채널은 유료 검색 감지 규칙을 일치시키기 위해 [!UICONTROL Paid Search Detection] 페이지에 구성된 설정을 사용합니다. ( **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Paid Search Detection]**). 대상 URL은 해당 검색 엔진에 대한 기존 유료 검색 감지 규칙과 일치합니다.

마케팅 채널 규칙의 경우 [!UICONTROL Paid Search] 설정은 다음과 같습니다.

![](assets/example_paid_search.png)

자세한 내용은 관리자의 [유료 검색 감지](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/paid-search-detection/paid-search-detection.html)를 참조하십시오.

## 자연어 검색 {#natural-search}

자연어 검색은 비용을 지불하지 않고 검색 엔진이 사이트의 등급을 매기는 웹 검색을 통해 방문자가 웹 사이트를 찾을 때 발생합니다. 검색 엔진이 사이트에 연결하는 데 사용하는 대상 URL을 제어할 수 있습니다. 이 URL을 사용하면 Analytics에서 검색이 자연스러운지 식별할 수 있습니다.

Analytics에는 자연어 검색 감지 기능이 없습니다. 유료 검색 감지를 설정하면 검색 레퍼러가 유료 검색 레퍼러가 아닌 경우 자연어 검색 레퍼러여야 한다는 것을 시스템에서 알 수 있습니다. 자연어 검색의 경우 대상 URL이 해당 검색 엔진에 대한 기존 유료 검색 감지 규칙과 일치하지 않습니다.

마케팅 채널 규칙의 경우 자연어 검색 설정은 다음과 같습니다.

![](assets/example_natural_search.png)

자세한 내용은 관리자의 [유료 검색 감지](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/paid-search-detection/paid-search-detection.html)를 참조하십시오.

## 계열사 {#afilliates}

제휴 규칙은 지정된 참조 도메인 세트에서 온 방문자를 식별합니다. 규칙에서 추적할 제휴의 도메인을 다음과 같이 나열합니다.

![](assets/example_affiliates.png)

## 소셜 네트워크 {#social-networks}

이 규칙은 Facebook*과 같은 소셜 네트워크에서 온 방문자를 식별합니다. 설정은 다음과 같습니다.

![](assets/example_social.png)

## 표시 {#display}

이 규칙은 배너 광고에서 온 방문자를 식별합니다. 대상 URL에서 쿼리 문자열 매개 변수로 식별됩니다(이 경우) *`Ad_01`*.

![](assets/example_display.png)

## 내부 {#internal}

이 규칙은 보고서 세트에 대한 내부 URL 필터와 일치하는 레퍼러를 사용하여 온 방문자를 식별합니다.

![](assets/example_internal.png)

## 이메일 {#email}

이 규칙을 설정하려면 이메일 캠페인에 대한 쿼리 문자열 매개 변수를 제공합니다. 이 예에서 매개 변수는 *`eml`*&#x200B;다음과 같습니다.

![](assets/example_email.png)

규칙에 추적 코드가 포함되어 있는 경우 다음과 같이 라인당 하나의 값을 입력합니다.

![](assets/tracking_code.png)

## 직접 {#direct}

이 규칙은 참조 도메인이 없는 방문자를 식별합니다. 이 규칙에는 즐겨찾기 링크나 브라우저에 링크를 붙여넣는 등 사이트에 직접 오는 방문자가 포함됩니다.

![](assets/example_direct.png)

