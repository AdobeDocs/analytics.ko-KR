---
title: 클라이언트 힌트
description: 알아보기 클라이언트 힌트가 점차 디바이스 정보의 소스로 사용자 에이전트를 대체하는 방법.
source-git-commit: 55747b79851696fd1bff8fb7cb4849dc8c813fc0
workflow-type: tm+mt
source-wordcount: '947'
ht-degree: 78%

---


# 클라이언트 힌트 개요 및 FAQ

클라이언트 힌트는 사용자 디바이스에 대한 개별 정보입니다. Google Chrome 및 Microsoft Edge와 같은 Chromium 브라우저에서 사용할 수 있습니다. 이러한 브라우저의 경우 클라이언트 힌트가 점차 디바이스 정보의 소스로 사용자 에이전트를 대체합니다. Adobe Analytics는 사용자 에이전트뿐만 아니라 클라이언트 힌트를 사용하여 디바이스 정보를 확인하도록 디바이스 조회 프로세스를 업데이트합니다.

Google은 사용자 에이전트 클라이언트 힌트를 낮은 엔트로피 힌트와 높은 엔트로피 힌트의 두 가지 범주로 나눕니다.

* **낮은 엔트로피 힌트**&#x200B;에는 보다 일반적인 디바이스 정보가 포함되어 있습니다. 이러한 힌트는 Chromium 브라우저에서 자동으로 제공됩니다.

* **높은 엔트로피** 힌트에는 보다 자세한 정보가 포함되어 있습니다. 이러한 힌트는 요청 시에만 사용할 수 있습니다. AppMeasurement 및 Web SDK는 모두 높은 엔트로피 힌트를 요청하도록 [구성할 수 있습니다](/help/implement/vars/config-vars/collecthighentropyuseragenthints.md). 기본적으로 두 라이브러리 모두 높은 엔트로피 힌트를 요청하지 **않습니다**.

>[!NOTE]
>
>2022년 10월부터 Chromium 브라우저의 새 버전은 사용자 에이전트 문자열에 표시된 운영 체제 버전을 “중단”할 예정입니다. 운영 체제 버전은 높은 엔트로피 힌트이므로 보고에서 운영 체제 버전의 정확도를 유지하려면 이러한 높은 엔트로피 힌트를 수집하도록 수집 라이브러리를 구성해야 합니다. 시간이 지남에 따라 사용자 에이전트의 다른 디바이스 정보가 동결되어 디바이스 보고의 정확도를 유지하기 위한 클라이언트 힌트가 필요합니다.

>[!NOTE]
>
>AAM에서는 전체 기능을 유지하려면 높은 엔트로피 힌트를 수집해야 합니다. 사용 중인 경우 [AAM에 서버측 전달](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html?lang=ko-KR) 그런 다음 높은 엔트로피 힌트의 컬렉션을 활성화할 수 있습니다.

## FAQ

+++**클라이언트 힌트에 대한 자세한 내용은 어디에서 살펴볼 수 있습니까?**

이 [Google 블로그 게시물](https://web.dev/user-agent-client-hints/)은 좋은 참고 자료이자 출발점이기도 합니다.

+++

+++**클라이언트 힌트 수집을 활성화하려면 어떻게 해야 합니까?**

낮은 엔트로피 힌트는 브라우저에서 자동으로 제공되며 Adobe의 디바이스 가져오기 및 브라우저 정보 프로세스에 포함됩니다. AppMeasurement(2.23.0 시작) 및 Web SDK(2.12.0 시작)의 최신 버전은 높은 엔트로피 힌트를 수집하도록 구성할 수 있습니다. 두 라이브러리 모두에서 높은 엔트로피 힌트 수집은 **기본적으로 비활성화**&#x200B;되어 있습니다.

+++

+++**높은 엔트로피 힌트를 수집하려면 어떻게 해야 합니까?**

높은 엔트로피 힌트를 구성할 수 있습니다. Web SDK 및 AppMeasurement 라이브러리를 사용하거나(각 태그를 통해) collectHighEntropyUserAgentHints 플래그를 사용하여 직접 구성하면 됩니다.

+++

+++**수집할 높은 엔트로피 힌트를 선택할 수 있습니까?**

지금은 가능하지 않습니다. 높은 엔트로피 힌트를 모두 수집하거나 수집하지 않도록 선택할 수 있습니다.

+++

+++**다양한 클라이언트 힌트 값은 무엇입니까?**

아래 표에서는 2022년 10월부터 클라이언트 힌트에 대해 설명합니다.

| 힌트 | 설명 | 높은 엔트로피 또는 낮은 엔트로피 | 예 |
| --- | --- | --- | --- | 
| Sec-CH-UA | 브라우저 및 주요 버전 | 낮음 | “Google Chrome 84” |
| Sec-CH-UA-Mobile | 모바일 디바이스 (참 또는 거짓) | 낮음 | TRUE |
| Sec-CH-UA-Platform | 운영 체제/플랫폼 | 낮음 | “Android” |
| Sec-CH-UA-Arch | 사이트의 아키텍처 | 높음 | “arm” |
| Sec-CH-UA-Bitness | Architecture Bitness | 높음 | “64” |
| Sec-CH-UA-Full-Version | 브라우저의 전체 버전 | 높음 | &quot;84.0.4143.2&quot; |
| Sec-CH-UA-Full-Version-List | 버전이 포함된 브랜드 목록 | 높음 | &quot;Not A;Brand&quot;;v=&quot;99&quot;, &quot;Chromium&quot;;v=&quot;98&quot;, &quot;Google Chrome&quot;;v=&quot;98&quot; |
| Sec-CH-UA-Model | 디바이스 모델 | 높음 | “픽셀 3” |
| Sec-CH-UA-Platform-Version | 운영 체제/플랫폼 버전 | 높음 | “10” |

+++

+++**Analytics의 디바이스 보고에 변경 사항이 있습니까?**

보고에 사용할 수 있는 디바이스 필드는 변경되지 않습니다. 이러한 필드에서 수집된 데이터는 클라이언트 힌트에 대한 수집을 구성한 필드 및 방법에 따라 변경될 수 있습니다.

+++

+++**사용자 에이전트에서 파생된 Analytics 보고 필드는 무엇입니까?**

이러한 필드는 사용자 에이전트에서 직접 파생되지만 사용자 에이전트는 장치 세부 사항에 따라 다른 장치 관련 필드에 대한 값을 도출하는 데 사용할 수 있습니다.

* [브라우저](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser.html?lang=ko)
* [브라우저 유형](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser-type.html?lang=ko)
* [운영 체제](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-systems.html?lang=ko)
* [운영 체제 유형](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-system-types.html?lang=ko)
* [모바일 디바이스 및 모바일 디바이스 유형](https://experienceleague.adobe.com/docs/analytics/components/dimensions/mobile-dimensions.html?lang=ko)

+++

+++**높은 엔트로피 힌트에 저장된 값에서 파생되는 Analytics 보고 필드는 무엇입니까?**

Google이 사용자 에이전트의 더 많은 부분을 &#39;정지&#39;하므로 시간이 지나면서 변경됩니다. 직접적으로 영향을 받는 첫 번째 필드는 운영 체제 버전을 포함하는 &quot;운영 체제&quot;입니다. Google에서 사용자-에이전트 힌트를 &quot;동결&quot;하기 위해 게시한 타임라인에 따라 운영 체제 버전은 2022년 10월 말부터 Chromium 버전 107부터 동결됩니다. 이때 사용자 에이전트의 운영 체제 버전이 일부 경우에 부정확할 수 있습니다.

사용자 에이전트의 중단 시기를 자세히 확인하려면 [Google에서 발표한 타임라인](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html)을 참조하십시오.

+++

+++**Adobe가 클라이언트 힌트를 사용하여 디바이스 정보를 얻는 방법은 무엇입니까?**

Adobe는 클라이언트 힌트와 사용자 에이전트를 모두 사용하여 디바이스 정보를 도출하는 서드파티 Device Atlas를 사용합니다.

+++

+++**클라이언트 힌트의 영향을 받는 브라우저는 무엇입니까?**

클라이언트 힌트는 Google Chrome 및 Microsoft Edge와 같은 Chromium 브라우저에만 적용됩니다. 다른 브라우저나 모바일 앱의 데이터는 변경되지 않습니다.

+++

+++**비보안 연결에 대해 클라이언트 힌트가 지원됩니까?**

아니요. 클라이언트 힌트는 HTTPS와 같은 보안 HTTP 연결을 통해서만 수집할 수 있습니다.

+++

+++**Adobe Source Connector를 통해 AEP 및 CJA로 전송된 데이터에서 클라이언트 힌트를 사용할 수 있습니까?**

Adobe는 2023년 상반기에 Adobe Source Connector를 통해 데이터에 클라이언트 힌트를 포함할 계획입니다.

+++

+++**클라이언트 힌트는 XDM에서 어떻게 표현됩니까?**

Adobe Experience Platform의 [스키마 설명서](https://github.com/adobe/xdm/blob/master/components/datatypes/browserdetails.schema.json#L121)를 참조하십시오.

+++

+++**사용자 에이전트에서 “중단”되는 부분은 무엇이며 언제 중단됩니까?**

[Google에서 발표한 타임라인](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html)을 참조하십시오. 이는 변경될 수 있습니다.

+++

+++**AAM 서버측 전달이 클라이언트 힌트를 지원합니까?**

예. 클라이언트 힌트는 AAM에 전달된 데이터에 포함됩니다. AAM에서는 전체 기능을 유지하려면 높은 엔트로피 힌트를 수집해야 합니다. 사용 중인 경우 [AAM에 서버측 전달](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html) 그런 다음 높은 엔트로피 힌트의 컬렉션을 활성화할 수 있습니다.

+++

