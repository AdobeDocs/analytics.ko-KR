---
title: 고유 방문자 수
description: 고유 방문자 ID의 수입니다.
exl-id: 56e7bad4-4802-49ac-a0f1-ae77441fc016
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '564'
ht-degree: 100%

---

# 고유 방문자 수

고유 방문자 수 지표는 차원 항목에 대한 방문자 ID의 수를 보여줍니다. 차원 항목의 인기도에 대한 높은 수준의 개요를 제공하므로 트래픽을 결정할 때 사용되는 가장 일반적인 지표 중 하나입니다. 예를 들어 방문자는 한 달 동안 매일 사이트를 방문할 수 있지만 여전히 하나의 고유 방문자로 계산됩니다.

[디바이스 간 분석](../cda/overview.md)을 사용하는 경우 지표는 [고유 장치](unique-devices.md) 지표로 대체됩니다.

## 일별, 주별, 월별, 분기별 및 연간 고유 방문자 수

Reports &amp; Analytics는 일별, 주별, 월별, 분기별 및 연간 고유 방문자 수에 대한 옵션을 제공합니다. 고유 방문자 수는 전체 기간 동안 한 명의 고유 방문자를 계산하지 않고 선택한 지표를 기반으로 계산됩니다. 예를 들어 사이트에 대한 일별 고유 방문자 수를 확인하려고 합니다. 방문자가 아침과 밤에 사이트를 방문한다면 이 방문자는 한 명의 일별 고유 방문자로 계산됩니다. 방문자가 월요일과 화요일에 사이트를 방문한다면 2명의 일별 고유 방문자로 계산됩니다.

Analysis Workspace는 보고서의 세부기간을 기준으로 고유 방문자를 처리합니다. 예를 들어 [일](../dimensions/day.md) 차원을 사용하는 경우 각 차원 항목에 대한 일별 고유 방문자 수를 보게 됩니다. 하지만 보고서 합계의 경우에는 자유 형식 테이블의 날짜 범위에 대해 중복이 제거된 고유 방문자 수입니다.

## 이 지표의 계산 방법

이 지표는 주어진 차원 항목에 대한 고유 방문자 ID의 수를 계산합니다. 방문자를 식별하는 방법에는 몇 가지가 있으므로 여러 고급 메커니즘을 사용하여 고유 방문자를 식별하게 됩니다. 다음 표에는 방문자가 식별되는 방법을 그 우선 순위와 함께 나열합니다. 일부 히트에는 여러 방문자 식별 방법이 있을 수 있습니다. 이러한 경우 우선 순위가 높은 방법이 사용됩니다.

| 사용된 명령 | 쿼리 매개 변수 (수집 방법) | 제공 시점 |
| --- | --- | --- |
| 1 | `vid` | [`visitorID`](/help/implement/vars/config-vars/visitorid.md) 변수가 설정되어 있습니다. |
| 2 | `aid` | 방문자에게 기존 [`s_vi`](https://docs.adobe.com/content/help/ko-KR/core-services/interface/ec-cookies/cookies-analytics.html) 쿠키가 있습니다. 방문자 ID 서비스를 구현하지 않은 상태에서 또는 구현하기 전에 구현을 설정하십시오. |
| 3 | `mid` | 방문자에게 기존 [`s_ecid`](https://docs.adobe.com/content/help/ko-KR/core-services/interface/ec-cookies/cookies-analytics.html) 쿠키가 있습니다. [Adobe Experience Cloud ID 서비스](https://docs.adobe.com/content/help/ko-KR/id-service/using/home.html)를 사용하여 구현을 설정하십시오. |
| 4 | `fid` | 방문자에게 기존 [`s_fid`](https://docs.adobe.com/content/help/ko-KR/core-services/interface/ec-cookies/cookies-analytics.html) 쿠키가 있습니다. 또는 어떤 이유에서든 `aid`와 `mid`를 설정할 수 없을 경우입니다. |
| 5 | IP 주소, 사용자 에이전트, 게이트웨이 IP 주소 | 방문자의 브라우저가 쿠키를 허용하지 않는 경우 고유 방문자를 식별하는 마지막 방법입니다. |

>[!NOTE]
>
>각 Analytics 방문자 ID는 Adobe 서버에 있는 프로필에 연결되어 있습니다. 이러한 방문자 프로필은 모든 방문자 ID 쿠키 만료와 관계없이 13개월 이상 방문하지 않으면 삭제됩니다.

## 고유 방문자 수에 영향을 주는 행동

고유 방문자 식별자는 일반적으로 브라우저 쿠키에 저장되어 있습니다. 새 고유 방문자는 다음 중 하나를 수행하는 경우 계산에 포함됩니다.

* 언제든지 캐시를 지웁니다.
* 동일한 컴퓨터에서 다른 브라우저를 엽니다. 브라우저당 한 명의 고유 방문자가 계산됩니다.
* 동일한 사람이 다른 장치에서 사이트를 탐색합니다. 장치별로 별도의 고유 방문자가 계산됩니다. [교차 장치 분석](../cda/overview.md)을 사용하면 [사람](people.md) 지표를 사용하여 방문자를 함께 결합할 수 있습니다.
* 비공개 탐색 세션을 엽니다 (Chrome의 Incognito 탭 등).

쿠키 식별자가 보존되는 한 다음의 경우 새 고유 방문자는 계산에 포함되지 *않습니다*.

* 연장된 기간 동안 브라우저를 닫습니다.
* 브라우저를 최신 버전으로 업그레이드합니다.
