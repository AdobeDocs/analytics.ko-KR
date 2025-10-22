---
title: Adobe Analytics의 방문자 식별
description: 최신 모범 사례를 사용하여 Adobe Analytics에서 방문자를 식별하는 방법을 알아봅니다.
source-git-commit: 98e9dc4932bd23d3e0b632705945f56c243750c5
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 10%

---

# Adobe Analytics의 방문자 식별

방문자 식별은 Adobe Analytics이 온라인 사용자 행동을 이해하기 위해 제공하는 값의 중심입니다. 여기에는 공통 식별자를 사용하여 시간에 따라 히트를 동일한 사람에게 연결하는 작업이 포함됩니다. 정확한 방문자 식별은 신뢰할 수 있는 지표를 보장하며 올바른 구현 전략을 지원합니다. Adobe은 여러 플랫폼에서 일관성과 데이터 무결성을 위해 최신 id 서비스의 우선 순위를 지정할 것을 권장합니다.

Adobe Analytics의 방문자 식별은 다음 구성 요소로 구성됩니다.

* 클라이언트측 식별자: 일반적으로 자사 쿠키에 저장됩니다. 서드파티 쿠키에 의존하는 구현은 최신 브라우저 개인 정보 보호 표준으로 인해 방문자 식별과 일관성이 낮습니다.
* 서버측 식별자: 각 Analytics 방문자 ID는 Adobe 서버의 프로필에 연결되어 있습니다. 이러한 방문자 프로필은 [eVar](/help/components/dimensions/evar.md)과(와) 같은 변수에서의 지속성을 허용합니다. 프로필은 모든 방문자 ID 쿠키 만료와 관계없이 비활성 기간 13개월 후에 삭제됩니다.

## Adobe Analytics 작업 식별 순서

Adobe이 히트를 받으면 다음 검사가 순서대로 수행됩니다. 주어진 속성이 있으면 Adobe은 히트에 해당 식별자를 사용합니다. 히트에 여러 식별자가 있으면 첫 번째 메서드만 사용됩니다. 작업 순서는 Adobe에서 방문자 식별을 권장하는 순서를 반영하지 않습니다.

| 사용된 순서 | 쿼리 매개변수 | 제공 시점 |
|---|---|---|
| **1<sup>번째</sup>** | `vid` | [`visitorID`](/help/implement/vars/config-vars/visitorid.md) 변수가 설정되어 있습니다. |
| **2<sup>번째</sup>** | `aid` | 방문자에게 기존 [`s_vi`](https://experienceleague.adobe.com/ko/docs/core-services/interface/data-collection/cookies/analytics) 쿠키가 있습니다. 방문자 ID 서비스를 구현하지 않은 상태에서 또는 구현하기 전에 구현을 설정하십시오. |
| **3<sup>rd</sup>** | `mid` | 방문자에게 기존 [`s_ecid`](https://experienceleague.adobe.com/ko/docs/core-services/interface/data-collection/cookies/analytics) 쿠키가 있습니다. [Adobe Experience Cloud ID 서비스](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ko)를 사용하여 구현을 설정하십시오. Adobe 가능한 경우 모든 구현에 ID 서비스를 사용하는 것이 좋습니다. |
| **4<sup>번째</sup>** | `fid` | 방문자에게 기존 [`s_fid`](https://experienceleague.adobe.com/ko/docs/core-services/interface/data-collection/cookies/analytics) 쿠키가 있습니다. 어떤 이유로든 `aid` 및 `mid`을(를) 설정할 수 없는 경우 AppMeasurement에서 대체 ID를 자동으로 생성합니다. |
| **5<sup>번째</sup>** | IP 주소 + 사용자 에이전트 | 방문자의 브라우저가 쿠키를 허용하지 않는 경우 고유 방문자를 식별하는 마지막 수단으로 사용됩니다. 해시된 방문자 ID는 [IP 난독화](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md) 전에 생성됩니다. IP 주소를 사용할 수 없는 경우 다른 IP 세부 정보(예: 게이트웨이 IP)가 대신 사용됩니다. |

그러면 선택한 방문자 ID가 해시되고 해당 서버측 식별자가 됩니다. 이 서버측 식별자는 `visid_high`데이터 피드`visid_low`에서 [&#x200B; + &#x200B;](/help/export/analytics-data-feed/data-feed-overview.md)(으)로 사용할 수 있습니다.

## 고유 방문자 수에 영향을 주는 행동

고유 방문자 식별자는 일반적으로 브라우저 쿠키에 저장되어 있습니다. 방문자가 다음 작업을 수행하는 경우 새 고유 방문자가 계산됩니다.

* 언제든지 쿠키를 지웁니다. 캐시가 지워질 때마다 히트에 대해 한 명의 고유 방문자가 계산됩니다.
* 방문자 ID 쿠키는 브라우저의 개인 정보 설정으로 인해 만료됩니다. 일부 브라우저에는 쿠키의 수명을 제한하는 추적 방지 방법이 포함되어 있습니다.
* 동일한 컴퓨터에서 다른 브라우저를 엽니다. 브라우저당 한 명의 고유 방문자가 계산됩니다.
* 비공개 탐색 세션을 엽니다(Chrome의 시크릿 탭 등). 모든 탭이 닫힌 후에는 탐색 세션당 하나의 고유 방문자가 계산됩니다.
* 다른 디바이스에서 사이트를 방문합니다. 장치당 한 명의 고유 방문자가 계산됩니다.
* 13개월 이상 활동이 없으면 사이트를 방문합니다.

여러 브라우저나 여러 장치를 사용하는 동일한 사용자를 식별하기 위해 Customer Journey Analytics에서 [결합](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/stitching/overview)을 사용하는 것이 좋습니다.

## 고유 방문자 수에 영향을 주지 않는 비헤이비어

방문자 식별자가 보존되는 한 새 고유 방문자는 *계산되지 않습니다*.

* 브라우저를 닫습니다(13개월 미만).
* 브라우저를 최신 버전으로 업그레이드합니다.
* 컴퓨터 다시 시작
