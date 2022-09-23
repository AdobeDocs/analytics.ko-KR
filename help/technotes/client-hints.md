---
title: 클라이언트 힌트
description: 클라이언트 힌트가 장치 정보의 소스로 사용자 에이전트를 점진적으로 교체하는 방법에 대해 알아봅니다.
source-git-commit: 72ef2d5e34220f1703714fac40a9dae4e76c1ab1
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 5%

---


# 클라이언트 힌트 개요 및 FAQ

클라이언트 힌트는 사용자의 장치에 대한 개별 정보입니다. 이러한 쿠키는 Google Chrome 및 Microsoft Edge와 같은 Chromium 브라우저에서 제공됩니다. 이러한 브라우저의 경우 클라이언트 힌트가 장치 정보의 소스로 사용자 에이전트를 점진적으로 바꿉니다. Adobe Analytics은 장치 조회 프로세스를 업데이트하여 사용자-에이전트 외에 클라이언트 힌트를 사용하여 장치 정보를 결정합니다.

Google은 사용자-에이전트 클라이언트 힌트를 두 가지 카테고리로 나눕니다. 낮은 엔트로피 및 높은 엔트로피 힌트입니다.

* **낮은 엔트로피 힌트** 장치에 대한 자세한 일반 정보를 포함합니다. 이러한 힌트는 Chromium 브라우저에서 자동으로 제공됩니다.

* **높은 엔트로피** 힌트에는 더 자세한 정보가 포함되어 있습니다. 이러한 힌트는 요청에서만 사용할 수 있습니다. AppMeasurement 및 Web SDK 모두 [구성할 수 있습니다](/help/implement/vars/config-vars/collecthighentropyuseragenthints.md) 높은 엔트로피 힌트를 요청합니다. 기본적으로 두 라이브러리는 모두 수행합니다 **not** 높은 엔트로피 힌트를 요청합니다.

>[!NOTE]
>
>2022년 10월부터 새로운 버전의 Chromium 브라우저는 사용자 에이전트 문자열에 표시되는 운영 체제 버전을 &#39;동결&#39;합니다. 사용자가 장치를 업그레이드할 때 사용자 에이전트의 운영 체제는 변경되지 않습니다. 따라서 시간이 지남에 따라 사용자-에이전트에 표시되는 운영 버전 정보가 정확도가 낮아집니다. 운영 체제 버전은 높은 엔트로피 힌트입니다. 따라서 보고에서 운영 체제 버전의 정확도를 유지하기 위해 이러한 높은 엔트로피 힌트를 수집하도록 컬렉션 라이브러리를 구성해야 합니다. 시간이 지나면서 User-Agent의 다른 장치 정보가 동결되어 클라이언트 힌트가 장치 보고 정확도를 유지해야 합니다.

## 자주 묻는 질문

+++**클라이언트 힌트에 대한 자세한 내용은 어디에서 확인할 수 있습니까?**

이 [Google 블로그 게시물](https://web.dev/user-agent-client-hints/) 는 좋은 참조 및 시작점입니다.

+++

+++**클라이언트 힌트 컬렉션을 활성화하려면 어떻게 합니까?**

낮은 엔트로피 힌트는 브라우저가 자동으로 제공하며 장치 및 브라우저 정보를 도출하는 Adobe 프로세스에 포함됩니다. 최신 버전의 AppMeasurement(2.23.0부터 시작) 및 웹 SDK(2.12.0부터 시작)는 높은 엔트로피 힌트를 수집하도록 구성할 수 있습니다. 두 라이브러리 모두에 대해 높은 엔트로피 힌트의 컬렉션은 **기본적으로 비활성화됨**.

+++

+++**높은 엔트로피 힌트를 캡처하려면 어떻게 합니까?**

높은 엔트로피 힌트는 해당 태그 확장을 통해 웹 SDK 및 AppMeasurement 라이브러리로 구성하거나 collectHighEntropyUserAgentHints 플래그를 사용하여 직접 구성할 수 있습니다.

+++

+++**어떤 높은 엔트로피 힌트를 수집할지 선택할 수 있습니까?**

지금은 아니에요 모든 높은 엔트로피 힌트를 수집하도록 선택하거나 없음을 선택할 수 있습니다.

+++

+++**Analytics에서 장치 보고에 변경 사항이 있습니까?**

보고에 사용할 수 있는 장치 필드는 변경되지 않습니다. 이러한 필드에 대해 캡처된 데이터는 클라이언트 힌트에 대한 컬렉션을 구성한 방법 및 필드에 따라 변경될 수 있습니다.

+++

+++**사용자-에이전트에서 파생되는 Analytics 보고 필드는 무엇입니까?**

* [브라우저](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser.html?lang=en)
* [브라우저 유형](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser-type.html?lang=en)
* [운영 체제](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-systems.html?lang=en)
* [운영 체제 유형](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-system-types.html?lang=en)
* [모바일 장치 및 모바일 장치 유형](https://experienceleague.adobe.com/docs/analytics/components/dimensions/mobile-dimensions.html?lang=en)
* [데이터 피드](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html?lang=ko-kr)

+++

+++**높은 엔트로피 힌트에 저장된 값에서 파생되는 Analytics 보고 필드는 무엇입니까?**

2022년 9월 현재, Google에서 &quot;동결&quot; 사용자 에이전트 힌트에 대해 게시된 타임라인은 운영 체제 버전이 2022년 10월부터 업데이트되지 않을 것임을 나타냅니다. 사용자가 OS를 업그레이드할 때 사용자 에이전트의 OS 버전은 업데이트되지 않습니다. 높은 엔트로피 힌트가 없으면 Analytics &quot;운영 체제&quot; 차원에 포함된 운영 체제 버전의 정확도가 점진적으로 저하됩니다.

자세한 내용은 [Google이 게시한 타임라인](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html) 사용자 에이전트의 다른 부분을 동결하는 시간을 확인합니다.

+++

+++**Adobe은 클라이언트 힌트를 사용하여 장치 정보를 파생하려면 어떻게 해야 합니까?**

Adobe은 클라이언트 힌트와 사용자-에이전트를 모두 사용하여 장치 정보를 파생시키는 타사 Device Atlas를 사용합니다.

+++

+++**클라이언트 힌트의 영향을 받는 브라우저는 무엇입니까?**

클라이언트 힌트는 Google Chrome 및 Microsoft Edge와 같은 Chromium 브라우저에만 적용됩니다. 다른 브라우저 또는 모바일 앱의 데이터는 변경되지 않습니다.

+++

+++**Adobe 소스 커넥터를 통해 AEP 및 CJA로 전송되는 데이터에서 클라이언트 힌트를 사용할 수 있습니까?**

2023년 상반기에 Adobe 소스 커넥터를 통해 데이터에 클라이언트 힌트를 포함할 계획입니다.

+++

+++**XDM에서 클라이언트 힌트는 어떻게 표시됩니까?**

자세한 내용은 [스키마 설명서](https://github.com/adobe/xdm/blob/master/components/datatypes/browserdetails.schema.json#L121) Adobe Experience Platform.

+++

+++**다양한 힌트 필드는 무엇입니까? 장치 보고에 영향을 주는 것은 무엇입니까?**

아래 표에서는 2022년 9월 현재 클라이언트 힌트에 대해 설명합니다.

| 힌트 | 설명 | 높은 엔트로피 또는 낮은 엔트로피 | 예 |
| --- | --- | --- | --- | 
| Sec-CH-UA | 브라우저 및 중요한 버전 | 낮음 | &quot;Google Chrome 84&quot; |
| Sec-CH-UA-Mobile | 모바일 장치(true 또는 false) | 낮음 | TRUE |
| Sec-CH-UA-Platform | 운영 체제/플랫폼 | 낮음 | &quot;Android&quot; |
| Sec-CH-UA-Arch | 사이트의 아키텍처 | 높음 | &quot;arm&quot; |
| Sec-CH-UA-Bitness | 아키텍처 비트 | 높음 | &quot;64&quot; |
| Sec-CH-UA-Full-Version | 브라우저의 전체 버전 | 높음 | &quot;84.0.4143.2&quot; |
| Sec-CH-UA-Full-Version-List | 버전이 있는 브랜드 목록 | 높음 | &quot;Not A;Brand&quot;;v=&quot;99&quot;, &quot;Chromium&quot;;v=&quot;98&quot;, &quot;Google Chrome&quot;;v=&quot;98&quot; |
| Sec-CH-UA-Model | 장치 모델 | 높음 | &quot;Pixel 3&quot; |
| Sec-CH-UA-Platform-Version | 운영 체제/플랫폼 버전 | 높음 | &quot;10&quot; |

+++



+++**사용자-에이전트의 어떤 부분이 &quot;동결됨&quot;이며, 언제 중단됩니까?**

자세한 내용은 [Google이 게시한 타임라인](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html). 이것은 변경될 수 있습니다.

+++
