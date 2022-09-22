---
title: 클라이언트 힌트
description: 알아보기
source-git-commit: b99852f4b8e0a3034ea8965e5646b1ab2f1a8c4c
workflow-type: tm+mt
source-wordcount: '889'
ht-degree: 4%

---


# 클라이언트 힌트 개요 및 FAQ

클라이언트 힌트는 사용자의 장치에 대한 개별 정보입니다. 이러한 쿠키는 Google Chrome 및 Microsoft Edge와 같은 Chromium 브라우저에서 제공됩니다. 이러한 브라우저의 경우 클라이언트 힌트는 사용자 에이전트를 장치 정보의 소스로 점진적으로 바꿉니다. Adobe Analytics은 장치 조회 프로세스를 업데이트하여 사용자 에이전트 외에도 클라이언트 힌트를 사용하여 장치 정보를 결정합니다.

Google은 사용자 에이전트 클라이언트 힌트를 두 가지 카테고리로 나눕니다. 낮은 엔트로피 및 높은 엔트로피 힌트입니다.

* 낮은 엔트로피 힌트는 장치에 대한 일반적인 정보를 가지고 있습니다. 이러한 힌트는 Chromium 브라우저에서 자동으로 제공됩니다.

* 높은 엔트로피 힌트는 더 자세한 정보를 가집니다. 이러한 힌트는 요청에서만 사용할 수 있습니다. 높은 엔트로피 힌트를 요청하도록 AppMeasurement 및 Web SDK를 모두 구성할 수 있습니다. 기본적으로 두 라이브러리는 모두 수행합니다 **not** 높은 엔트로피 힌트를 요청합니다.

>[!NOTE]
>
>2022년 10월부터 Chromium 브라우저의 새 버전에서 사용자 에이전트 문자열에 표시되는 운영 체제 버전을 &#39;동결&#39;하기 시작합니다. 즉, 시간이 지남에 따라 사용자 에이전트에 표시된 운영 버전 정보가 정확도가 떨어집니다. 운영 체제 버전은 높은 엔트로피 힌트입니다. 따라서 보고에서 운영 체제 버전의 정확도를 유지하기 위해 이러한 높은 엔트로피 힌트를 수집하도록 컬렉션 라이브러리를 구성해야 합니다. 시간이 지나면서 사용자 에이전트의 다른 장치 정보가 중단되므로 클라이언트 힌트가 장치 보고 정확도를 유지해야 합니다.

## 자주 묻는 질문

+++**클라이언트 힌트 컬렉션을 활성화하려면 어떻게 합니까?**

낮은 엔트로피 힌트는 브라우저가 자동으로 제공하며 장치 정보에 대한 Adobe 프로세스에 포함됩니다. 높은 엔트로피 힌트를 수집하도록 최신 버전의 AppMeasurement(TBD 시작) 및 웹 SDK(시작 TBD)를 구성할 수 있습니다. 두 라이브러리 모두에 대해 높은 엔트로피 힌트의 컬렉션은 **기본적으로 비활성화됨**. 이 구현을 위한 자세한 내용은 여기 를 참조하십시오.

+++**어떤 높은 엔트로피 힌트를 수집할지 선택할 수 있습니까?**

지금은 아니에요 모든 높은 엔트로피 힌트를 수집하도록 선택하거나 없음을 선택할 수 있습니다.

+++**Analytics에서 장치 보고에 변경 사항이 있습니까?**

보고에 사용할 수 있는 장치 필드는 변경되지 않습니다. 해당 필드에 대해 캡처된 데이터는 클라이언트 힌트에 대한 수집을 구성한 방법 및 어느 필드에 따라 변경될 수 있습니다.

+++**사용자 에이전트에서 파생되는 Analytics 보고 필드는 무엇입니까?**

* [브라우저](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser.html?lang=en)
* [브라우저 유형](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser-type.html?lang=en)
* [운영 체제](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-systems.html?lang=en)
* [운영 체제 유형](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-system-types.html?lang=en)
* [모바일 장치 및 모바일 장치 유형](https://experienceleague.adobe.com/docs/analytics/components/dimensions/mobile-dimensions.html?lang=en)??
* 데이터 피드 (사용자가 이러한 필드를 캡처하도록 업데이트해야 합니다.) 또한 장치 정보와 함께 모바일 ID를 노출할 수 없는 종속성이 있습니다.)
* Analytics 소스 커넥터 (준비되지 않음)

+++**높은 엔트로피 힌트에 저장된 값에서 파생되는 Analytics 보고 필드는 무엇입니까?**

2022년 9월 현재, Google에서 게시된 사용자 에이전트 힌트 동결에 대한 타임라인은 운영 체제 버전이 2022년 10월부터 업데이트되지 않을 것임을 나타냅니다. 높은 엔트로피 힌트가 없으면 Analytics &quot;운영 체제&quot; 차원에 포함된 운영 체제 버전의 정확도가 점진적으로 저하됩니다.

자세한 내용은 [Google이 게시한 타임라인](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html) 사용자 에이전트를 동결하는 시간을 확인합니다.

+++**클라이언트 힌트의 영향을 받는 브라우저는 무엇입니까?**

클라이언트 힌트는 Google Chrome 및 Microsoft Edge와 같은 Chromium 브라우저에만 적용됩니다. 다른 브라우저 또는 모바일 앱의 데이터는 변경되지 않습니다.

+++**Adobe은 클라이언트 힌트를 사용하여 장치 정보를 파생하려면 어떻게 해야 합니까?**

Adobe은 클라이언트 힌트와 사용자 에이전트를 모두 사용하여 장치 정보를 파생시키는 타사 Device Atlas를 사용합니다.

+++**클라이언트 힌트를 데이터 피드에서 사용할 수 있습니까?**

예. 설명서 를 참조하십시오(계속 진행).

+++**Adobe 소스 커넥터를 통해 AEP 및 CJA로 전송되는 데이터에서 클라이언트 힌트를 사용할 수 있습니까?**

2023년 상반기에 Adobe 소스 커넥터를 통해 데이터에 클라이언트 힌트를 포함할 계획입니다.

+++**XDM에서 클라이언트 힌트는 어떻게 표시됩니까?**

자세한 내용은 [스키마 설명서](https://github.com/adobe/xdm/blob/master/components/datatypes/browserdetails.schema.json#L121) Adobe Experience Platform.

+++**클라이언트 힌트에 대한 자세한 내용은 어디에서 확인할 수 있습니까?**

이 [Google 블로그 게시물](https://web.dev/user-agent-client-hints/) 는 좋은 참조 및 시작점입니다.

+++**다양한 힌트 필드는 무엇입니까? 장치 보고에 영향을 주는 것은 무엇입니까?**

아래 표에서는 2022년 9월 현재 클라이언트 힌트에 대해 설명합니다.

| 힌트(헤더) | 힌트 | 높은 엔트로피 또는 낮은 엔트로피 | 예 | Analytics 보고 필드 |
| --- | --- | --- | --- | --- |
| Sec-CH-UA | 브라우저 및 중요한 버전 | 낮음 | Google Chrome 84 | [브라우저](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser.html?lang=en) 및 [브라우저 유형](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser-type.html?lang=en) |
| Sec-CH-UA-Mobile | 모바일 장치(true 또는 false) | 낮음 | TRUE | [모바일 장치 및 모바일 장치 유형](https://experienceleague.adobe.com/docs/analytics/components/dimensions/mobile-dimensions.html?lang=en)?? |
| Sec-CH-UA-Platform | 운영 체제/플랫폼 | 낮음 | Android | [운영 체제](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-systems.html?lang=en) |
| Sec-CH-UA-Arch | 사이트의 아키텍처 | 높음 | &quot;arm&quot; | 없음? |
| Sec-CH-UA-Bitness | Sec-CH-UA-Bitness | 높음 |  | 없음? |
| Sec-CH-UA-Full-Version | 브라우저의 전체 버전 | 높음 | &quot;84.0.4143.2&quot; | 없음? |
| Sec-CH-UA-Full-Version-List | ??? | 높음 | ??? | 없음? |
| Sec-CH-UA-Model | 장치 모델 | 높음 | &quot;Pixel 3&quot; | 없음? |
| Sec-CH-UA-Platform-Version | 운영 체제/플랫폼 버전 | 높음 | &quot;10&quot; | [운영 체제](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-systems.html?lang=en) |

+++**높은 엔트로피 힌트를 캡처하려면 어떻게 합니까?**

높은 엔트로피 힌트를 구성할 수 있습니다

* AppMeasurement가 직접 [구현 안내서의 플래그 항목에 대한 링크]
* 태그 Analytics 확장에서
* 를 클릭합니다.

+++**사용자 에이전트에서 제거되는 데이터와 그 시기**

자세한 내용은 [Google이 게시한 타임라인](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html). 이것은 변경될 수 있습니다.

+++