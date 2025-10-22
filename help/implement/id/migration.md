---
title: Adobe Analytics에 대한 방문자 ID 서비스 마이그레이션 고려 사항
description: Adobe Analytics이 방문자 ID 서비스와 상호 작용하는 방법에 대한 개요입니다.
source-git-commit: f682f9c8533536e9b33f320f2a420055c6f4e397
workflow-type: tm+mt
source-wordcount: '617'
ht-degree: 0%

---

# Adobe Analytics에 대한 방문자 ID 서비스 마이그레이션 고려 사항

기존 Analytics 구현을 사용하여 방문자 ID 서비스로 이동하려는 경우 고려해야 할 몇 가지 중요한 주제가 있습니다. 이러한 고려 사항을 사용하면 방문자 식별 무결성을 유지하고 기존 Analytics 구현이 있는 경우 ID 서비스가 작동하는 방식을 이해할 수 있습니다.

>[!TIP]
>
>이 페이지는 기존 AppMeasurement 또는 Analytics 확장 구현에만 적용되며 방문자 ID 서비스를 추가하거나 웹 SDK 구현으로 업그레이드하고 있습니다. 즉, 구현은 기존 Analytics ID(`aid`)를 사용하며 Experience Cloud ID(`mid`)를 사용하는 방향으로 이동하고 있습니다. 모든 웹 SDK 구현은 기본적으로 이미 Experience Cloud ID(`mid`)를 사용합니다.

## 방문자 ID 서비스가 기존 Analytics 방문자 쿠키와 상호 작용하는 방법

AppMeasurement에는 방문자를 식별하는 자체 메서드가 있으므로 조직에서 방문자 ID 서비스를 배포할 때 일부 방문자에게 이전 Analytics 쿠키가 있을 수 있습니다. 다음 목록은 방문자가 다양한 상황에서 어떻게 식별되는지 설명합니다.

* **방문자 쿠키가 없음**: ID 서비스에서 Experience Cloud ID(`mid`)를 할당합니다.
* **`s_vi` 쿠키가 있음**: ID 서비스가 Experience Cloud ID(`aid`)와 함께 기존 레거시 Analytics ID(`AMCV`)를 `mid` 쿠키에 씁니다. `aid`이(가) [작업 순서](overview.md)에서 더 높으므로 `AMCV` 쿠키가 만료되거나 지워질 때까지 기존 Analytics ID가 방문자 식별자입니다. 유예 기간을 사용하도록 설정하면 ID 서비스는 해당 응답에 `mid` 및 `aid`을(를) 모두 포함합니다.
* **대체 쿠키가 있습니다**: ID 서비스가 `fid` 쿠키에 대체 쿠키(`AMCV`)를 쓰지 않습니다. 대신 방문자는 새 방문자인 것처럼 Experience Cloud ID(`mid`)를 받습니다.

## 방문자 ID 서비스 유예 기간

동일한 보고서 세트에 데이터를 전송하는 구현이 여러 개 있고 일부 구현에서만 방문자 ID 서비스를 구현할 수 있는 경우, Adobe에서는 유예 기간을 구성하는 것이 좋습니다. 예를 들어, 사이트의 지원 섹션이 별도의 태그 지정 솔루션에 의해 관리되는 경우 지원 섹션 앞에 방문자 ID 서비스가 나머지 사이트에 배포되어 있을 수 있습니다. 유예 기간이 없으면 지원 섹션을 보는 새 방문자는 이전 Analytics 방문자 ID를 받게 되므로 두 명의 개별 방문자가 계산됩니다. 유예 기간을 사용하면 방문자 ID 서비스에서 Experience Cloud ID(`mid`)와 레거시 Analytics 방문자 ID(`aid`)를 모두 발행하므로 ID 서비스가 없는 사이트 영역이 방문자를 식별하는 일관된 상태로 유지됩니다.

사이트의 모든 영역에 걸쳐 방문자 ID 서비스 배포를 조정하는 경우 유예 기간이 필요하지 않습니다. 유예 기간을 구성하려면 [Adobe 고객 지원 센터](https://helpx.adobe.com/marketing-cloud/contact-support.html)에 문의하십시오. 유예 기간은 최대 180일 동안 구성할 수 있으며 갱신할 수 있습니다. Adobe 전체 속성이 ID 서비스를 사용하도록 구성된 경우 유예 기간을 중단하는 것이 좋습니다.

## 도메인 간 추적

일부 이전 Analytics 방문자 ID 구현에서는 두 도메인이 `data.example.com`과(와) 같은 공통 도메인에서 동일한 방문자 쿠키를 공유하는 &quot;친숙한 타사 쿠키&quot;를 사용할 수 있습니다. 친숙한 타사 쿠키는 여전히 타사 쿠키이므로 많은 최신 브라우저가 해당 쿠키를 거부하므로 Analytics가 방문자 식별을 위해 대체 ID(`fid`)에 의존하게 됩니다. ID 서비스로 이동하면 모든 도메인이 자사 컨텍스트에서 `AMCV` 쿠키를 설정하여 방문자 ID를 유지할 수 있는 가능성을 높일 수 있습니다.

방문자 ID 서비스는 도메인 간 추적을 위해 타사 쿠키([`demdex` 쿠키](https://experienceleague.adobe.com/en/docs/id-service/using/intro/cookies))를 설정하려고 하지만, 최신 브라우저에서는 이를 거부하는 경우가 많습니다. [`appendVisitorIDsTo`](https://experienceleague.adobe.com/en/docs/id-service/using/id-service-api/methods/appendvisitorid) 메서드를 사용하여 소유하고 있는 도메인 간에 방문자의 Experience Cloud ID(`mid`)를 전달하는 것이 좋습니다.

## 서버측 추적

[`getMarketingCloudVisitorID`](https://experienceleague.adobe.com/en/docs/id-service/using/id-service-api/methods/getmcvid)을(를) 호출하여 Experience Cloud ID(`mid`)를 가져오고 [`getAnalyticsVisitorID`](https://experienceleague.adobe.com/en/docs/id-service/using/id-service-api/methods/getanalyticsvisitorid)을(를) 호출하여 기존 Analytics ID(`aid`)를 가져올 수 있습니다. Adobe은 방문자 식별 논리를 유지하기 위해 두 가지를 모두 확인하는 것을 권장합니다.
