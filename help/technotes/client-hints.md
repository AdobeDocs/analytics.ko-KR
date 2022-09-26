---
title: 클라이언트 힌트
description: 알아보기 클라이언트 힌트가 장치 정보의 소스로 사용자 에이전트를 점진적으로 교체하는 방법.
source-git-commit: 72ef2d5e34220f1703714fac40a9dae4e76c1ab1
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 55%

---


# 클라이언트 힌트 개요 및 FAQ

클라이언트 힌트는 사용자 디바이스에 대한 개별 정보입니다. Google Chrome 및 Microsoft Edge와 같은 Chromium 브라우저에서 사용할 수 있습니다. 이러한 브라우저의 경우 클라이언트 힌트가 장치 정보의 소스로 사용자 에이전트를 점진적으로 바꿉니다. Adobe Analytics은 장치 조회 프로세스를 업데이트하여 사용자-에이전트 외에 클라이언트 힌트를 사용하여 장치 정보를 결정합니다.

Google은 사용자-에이전트 클라이언트 힌트를 두 가지 카테고리로 나눕니다. 낮은 엔트로피 및 높은 엔트로피 힌트입니다.

* **낮은 엔트로피 힌트** 장치에 대한 자세한 일반 정보를 포함합니다. 이러한 힌트는 Chromium 브라우저에서 자동으로 제공됩니다.

* **높은 엔트로피** 힌트에는 더 자세한 정보가 포함되어 있습니다. 이러한 힌트는 요청 시에만 사용할 수 있습니다. AppMeasurement 및 Web SDK 모두 [구성할 수 있습니다](/help/implement/vars/config-vars/collecthighentropyuseragenthints.md) 높은 엔트로피 힌트를 요청합니다. 기본적으로 두 라이브러리 모두 높은 엔트로피 힌트를 요청하지 **않습니다**.

>[!NOTE]
>
>2022년 10월부터 새로운 버전의 Chromium 브라우저는 사용자 에이전트 문자열에 표시되는 운영 체제 버전을 &#39;동결&#39;합니다. 사용자가 장치를 업그레이드할 때 사용자 에이전트의 운영 체제는 변경되지 않습니다. 따라서 시간이 지남에 따라 사용자-에이전트에 표시되는 운영 버전 정보가 정확도가 낮아집니다. 운영 체제 버전은 높은 엔트로피 힌트이므로 보고에서 운영 체제 버전의 정확도를 유지하려면 이러한 높은 엔트로피 힌트를 수집하도록 수집 라이브러리를 구성해야 합니다. 시간이 지나면서 User-Agent의 다른 장치 정보가 동결되어 클라이언트 힌트가 장치 보고 정확도를 유지해야 합니다.

## 자주 묻는 질문

+++**클라이언트 힌트에 대한 자세한 내용은 어디에서 살펴볼 수 있습니까?**

이 [Google 블로그 게시물](https://web.dev/user-agent-client-hints/)은 좋은 참고 자료이자 출발점이기도 합니다.

+++

+++**클라이언트 힌트 수집을 활성화하려면 어떻게 해야 합니까?**

낮은 엔트로피 힌트는 브라우저가 자동으로 제공하며 장치 및 브라우저 정보를 도출하는 Adobe 프로세스에 포함됩니다. 최신 버전의 AppMeasurement(2.23.0부터 시작) 및 웹 SDK(2.12.0부터 시작)는 높은 엔트로피 힌트를 수집하도록 구성할 수 있습니다. 두 라이브러리 모두에서 높은 엔트로피 힌트 수집은 **기본적으로 비활성화**&#x200B;되어 있습니다.

+++

+++**높은 엔트로피 힌트를 수집하려면 어떻게 해야 합니까?**

높은 엔트로피 힌트를 구성할 수 있습니다. 각각의 태그 확장을 통해 또는 collectHighEntropyUserAgentHints 플래그를 사용하여 직접 웹 SDK 및 AppMeasurement 라이브러리를 사용합니다.

+++

+++**수집할 높은 엔트로피 힌트를 선택할 수 있습니까?**

지금은 가능하지 않습니다. 높은 엔트로피 힌트를 모두 수집하거나 수집하지 않도록 선택할 수 있습니다.

+++

+++**Analytics의 디바이스 보고에 변경 사항이 있습니까?**

보고에 사용할 수 있는 디바이스 필드는 변경되지 않습니다. 이러한 필드에 대해 캡처된 데이터는 클라이언트 힌트에 대한 컬렉션을 구성한 방법 및 필드에 따라 변경될 수 있습니다.

+++

+++**사용자-에이전트에서 파생되는 Analytics 보고 필드는 무엇입니까?**

* [브라우저](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser.html?lang=ko)
* [브라우저 유형](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser-type.html?lang=ko)
* [운영 체제](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-systems.html?lang=ko)
* [운영 체제 유형](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-system-types.html?lang=ko)
* [모바일 장치 및 모바일 장치 유형](https://experienceleague.adobe.com/docs/analytics/components/dimensions/mobile-dimensions.html?lang=ko)
* [데이터 피드](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html?lang=ko-kr)

+++

+++**높은 엔트로피 힌트에 저장된 값에서 파생되는 Analytics 보고 필드는 무엇입니까?**

2022년 9월 현재, Google에서 &quot;동결&quot; 사용자 에이전트 힌트에 대해 게시된 타임라인은 운영 체제 버전이 2022년 10월부터 업데이트되지 않을 것임을 나타냅니다. 사용자가 OS를 업그레이드할 때 사용자 에이전트의 OS 버전은 업데이트되지 않습니다. 높은 엔트로피 힌트가 없으면 Analytics &quot;운영 체제&quot; 차원에 포함된 운영 체제 버전의 정확도가 점진적으로 저하됩니다.

자세한 내용은 [Google이 게시한 타임라인](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html) 사용자 에이전트의 다른 부분을 동결하는 시간을 확인합니다.

+++

+++**Adobe가 클라이언트 힌트를 사용하여 디바이스 정보를 얻는 방법은 무엇입니까?**

Adobe은 클라이언트 힌트와 사용자-에이전트를 모두 사용하여 장치 정보를 파생시키는 타사 Device Atlas를 사용합니다.

+++

+++**클라이언트 힌트의 영향을 받는 브라우저는 무엇입니까?**

클라이언트 힌트는 Google Chrome 및 Microsoft Edge와 같은 Chromium 브라우저에만 적용됩니다. 다른 브라우저나 모바일 앱의 데이터는 변경되지 않습니다.

+++

+++**Adobe Source Connector를 통해 AEP 및 CJA로 전송된 데이터에서 클라이언트 힌트를 사용할 수 있습니까?**

2023년 상반기에 Adobe Source Connector를 통해 데이터에 클라이언트 힌트를 포함할 계획입니다.

+++

+++**클라이언트 힌트는 XDM에서 어떻게 표현됩니까?**

Adobe Experience Platform의 [스키마 설명서](https://github.com/adobe/xdm/blob/master/components/datatypes/browserdetails.schema.json#L121)를 참조하십시오.

+++

+++**다양한 힌트 필드는 무엇입니까? 다음 중 디바이스 보고에 영향을 미치는 것은 무엇입니까?**

아래 표에서 2022년 9월 시점의 클라이언트 힌트를 확인할 수 있습니다.

| 힌트 | 설명 | 높은 엔트로피 또는 낮은 엔트로피 | 예 |
| --- | --- | --- | --- | 
| Sec-CH-UA | 브라우저 및 주요 버전 | 낮음 | &quot;Google Chrome 84&quot; |
| Sec-CH-UA-Mobile | 모바일 디바이스 (참 또는 거짓) | 낮음 | TRUE |
| Sec-CH-UA-Platform | 운영 체제/플랫폼 | 낮음 | &quot;Android&quot; |
| Sec-CH-UA-Arch | 사이트의 아키텍처 | 높음 | “arm” |
| Sec-CH-UA-Bitness | 아키텍처 비트 | 높음 | &quot;64&quot; |
| Sec-CH-UA-Full-Version | 브라우저의 전체 버전 | 높음 | &quot;84.0.4143.2&quot; |
| Sec-CH-UA-Full-Version-List | 버전이 있는 브랜드 목록 | 높음 | &quot;Not A;Brand&quot;;v=&quot;99&quot;, &quot;Chromium&quot;;v=&quot;98&quot;, &quot;Google Chrome&quot;;v=&quot;98&quot; |
| Sec-CH-UA-Model | 디바이스 모델 | 높음 | “픽셀 3” |
| Sec-CH-UA-Platform-Version | 운영 체제/플랫폼 버전 | 높음 | “10” |

+++



+++**사용자-에이전트의 어떤 부분이 &quot;동결됨&quot;이며, 언제 중단됩니까?**

[Google에서 발표한 타임라인](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html)을 참조하십시오. 이는 변경될 수 있습니다.

+++
