---
title: 고유 방문자 수
description: 고유 개인(또는 장치)의 수입니다.
translation-type: tm+mt
source-git-commit: 8cfd797e336e006bf4134a2c10a89ad1003c53dc
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 10%

---


# 고유 방문자 수

&#39;고유 방문자 수&#39; 지표는 차원 값에 대한 방문자 ID 수를 보여줍니다. 이것은 차원 값의 인기에 대한 높은 수준의 개요를 제공하므로 트래픽을 결정할 때 사용되는 가장 일반적인 지표 중 하나입니다. 예를 들어 방문자가 한 달 동안 매일 사이트를 방문할 수 있지만 여전히 단일 고유 방문자로 카운트됩니다.

장치 [간 분석을](../cda/cda-home.md)사용하는 경우 이 지표의 이름이 &#39;고유 장치&#39;로 바뀝니다.

## 일별, 주별, 월별, 분기별 및 연간 고유 방문자

보고 및 Analytics은 일별, 주별, 월별, 분기별 및 연간 고유 방문자에 대한 옵션을 제공합니다. 전체 기간 동안 단일 고유 방문자를 계산하는 대신 고유 방문자는 선택한 지표를 기반으로 계산됩니다. 예를 들어 사이트에 대한 일별 고유 방문자를 확인하려고 합니다. 방문자가 아침 및 밤에 사이트를 방문하는 경우 일일 고유 방문자로 카운트됩니다. 방문자가 월요일과 화요일에 다시 사이트를 방문하는 경우 일별 고유 방문자 2명으로 카운트됩니다.

Analysis Workspace은 보고서의 세부기간을 기준으로 고유 방문자를 처리합니다. 예를 들어 [일](../dimensions/day.md) 차원을 사용하는 경우 각 차원 값에 대한 일별 고유 방문자를 보게 됩니다. 하지만 보고서 합계에 대해 자유 형식 테이블의 날짜 범위에 대한 고유 방문자의 중복 제거가 수행됩니다.

## 이 지표의 계산 방법

이 지표는 주어진 차원 값에 대한 고유 방문자 ID 수를 계산합니다. 여러 가지 방법으로 방문자를 식별할 수 있으므로 여러 고급 메커니즘을 사용하여 고유 방문자를 식별합니다. 다음 표는 방문자가 우선 순위와 함께 식별되는 방법을 보여줍니다. 일부 히트에는 여러 방문자 식별 방법이 있을 수 있습니다. 이 경우 우선 순위가 높은 방법이 사용됩니다.

| 사용된 명령 | 쿼리 매개 변수(수집 방법) | 제공 시점 |
| --- | --- | --- |
| 1 | `vid` | 변수가 [`visitorID`](/help/implement/vars/config-vars/visitorid.md) 설정되어 있습니다. |
| 2 | `aid` | 방문자에게 기존 [`s_vi`](https://docs.adobe.com/content/help/ko-KR/core-services/interface/ec-cookies/cookies-analytics.html) 쿠키가 있습니다. 방문자 ID 서비스를 구현하지 않거나 이전에 구현을 설정합니다. |
| 3 | `mid` | 방문자에게 기존 [`s_ecid`](https://docs.adobe.com/content/help/ko-KR/core-services/interface/ec-cookies/cookies-analytics.html) 쿠키가 있습니다. Adobe [Experience Cloud Identity 서비스를 사용하여 구현을 설정합니다](https://docs.adobe.com/content/help/ko-KR/id-service/using/home.html). |
| 4 | `fid` | 방문자에게 기존 [`s_fid`](https://docs.adobe.com/content/help/ko-KR/core-services/interface/ec-cookies/cookies-analytics.html) 쿠키가 있거나, 어떤 이유에서든 `aid` 설정할 수 `mid` 없을 경우. |
| 5 | IP 주소, 사용자 에이전트, 게이트웨이 IP 주소 | 방문자의 브라우저가 쿠키를 수락하지 않는 경우 고유 방문자를 식별하는 마지막 방법입니다. |

>[!NOTE] 각 Analytics 방문자 ID는 Adobe 서버의 프로필에 연결되어 있습니다. 이러한 방문자 프로필은 방문자 ID 쿠키 만료와 상관없이 최소 13개월 동안 활동이 없는 경우 삭제됩니다.

## 고유 방문자 수에 영향을 주는 동작

고유 방문자 식별자는 일반적으로 브라우저 쿠키에 저장됩니다. 새 고유 방문자가 다음 중 하나를 수행하는 경우 계산됩니다.

* 언제든지 캐시를 지웁니다.
* 동일한 컴퓨터에서 다른 브라우저를 엽니다. 브라우저당 한 명의 고유 방문자가 계산됩니다.
* 다른 디바이스에서 사이트를 검색하는 동일한 사람입니다. 개별 고유 방문자는 장치당 계산됩니다. 장치 [간 분석을](../cda/cda-home.md) 사용하여 사람 지표를 사용하여 방문자를 결합할 [수](people.md) 있습니다.
* 비공개 브라우징 세션(Chrome의 Incognito 탭 등)을 엽니다.

쿠키 식별자가 보존된 경우 새 고유 방문자는 카운트되지 *않습니다* .

* 장기간 브라우저 닫기
* 브라우저를 최신 버전으로 업그레이드
