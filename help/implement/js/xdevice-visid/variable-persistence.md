---
description: 방문자 프로필이 동일한 방문자 ID 변수와 연결된 후 병합되면, 내역 데이터 세트에서 속성이 변경되지 않습니다.
keywords: Analytics Implementation
title: 속성 및 지속성
topic: Developer and implementation
uuid: 5dd706be-83f6-498a-a856-e3c5af995348
translation-type: tm+mt
source-git-commit: ebf149df7974f9f2889b6fe938088eda90c84051

---


# 속성 및 지속성

> [!IMPORTANT] 장치 간에 방문자를 식별하는 이 방법은 더 이상 권장되지 않습니다. 구성 [요소](/help/components/cda/cda-home.md) 사용 안내서의 장치 간 분석을 참조하십시오.

방문자 프로필이 동일한 방문자 ID 변수와 연결된 후 병합되면, 내역 데이터 세트에서 속성이 변경되지 않습니다.

* When the variable `s.visitorID` is set and sent on a hit, Adobe checks for any other visitor profiles that have a matching visitor ID.
* 일치하는 프로필이 있으면 그때부터 이미 시스템에 있는 방문자 프로필을 사용하고, 이전 방문자 프로필은 더 이상 사용하지 않습니다.
* 일치하는 방문자 ID가 없으면, 새 프로필이 만들어집니다.

인증되지 않은 고객이 먼저 사이트에 도달하면, 해당 고객은 Adobe Analytics에 의해 방문자 프로필에 지정됩니다. 새 프로필이 만들어지면, 한 방문이 종료되고 다른 방문이 시작됩니다.

## 예제 1

아래 예는 고객이 첫 번째 장치에서 처음으로 인증될 때 데이터가 Adobe Analytics로 전송되는 방법을 나타냅니다.

* `eVar16`에는 1일의 만료 기한이 있고 `evar17`은 방문 시 만료됩니다.
* `post_visitor_id` 열은 Adobe Analytics에 의해 유지 관리되는 프로필을 나타냅니다. 게시물 열은 일반적으로 데이터 피드에서 표시됩니다. 내보내기 [사용 안내서의 데이터 피드를](/help/export/analytics-data-feed/data-feed-overview.md) 참조하십시오.
* `post_evar16` 및 `post_evar17` 열은 eVar의 지속성을 나타냅니다.
* `cust_visid`는 `s.visitorID`에 설정된 값을 나타냅니다.
* 각 행은 하나의 &#39;히트&#39;로서, Adobe Analytics 데이터 수집 서버로 전송된 단일 요청입니다.

![장치 간 예 1](assets/xdevice_first.jpg)

On the first data connection containing a previously unrecognized `s.visitorID` value (`u999` above), a new profile is created. 이전 프로필의 영구 값은 새 프로필로 전송됩니다.

* 방문 시 만료되도록 설정된 eVar는 인증된 프로필에 복사되지 않습니다. 위의 값 `car`는 지속되지 않습니다.
* 다른 방법에 의해 만료되도록 설정된 eVar는 인증된 프로필에 복사됩니다. 값 `apple`은 지속됩니다.
* 지속되는 eVar의 경우 인스턴스 지표가 기록되지 않습니다. 이것은 장치 간 방문자 식별을 사용할 때 eVar 값에 대한 고유 방문 수 지표가 인스턴스 지표보다 클 때 보고서를 볼 수 있음을 의미합니다.

> [!NOTE] 사용자가 사이트를 처음 방문하고(이 장치에서 전에 방문한 적이 없음) 도착 후 약 3분 이내에 인증을 받으면, 인증된 프로필에는 값이 지속되지 않습니다.

## 예제 2

아래 예제는 고객이 다른 장치에서 이전에 인증한 후 새 장치에서 인증될 때 데이터가 Adobe Analytics로 전송되는 방법을 나타냅니다.

![크로스 디바이스 예 2](assets/xdevice-subsequent.jpg)

고객이 인증을 받으면 이전 &#39;인증된&#39; 프로필과 일치하게 됩니다 - `2947539300`. 이 방문의 시작 시 사용된 프로필(`5477766334477`)이 더 이상 사용되지 않고, 파일에서 지속되는 데이터가 없습니다.

* 지리 특성 데이터는 방문의 첫 번째 히트를 기반으로 기록되며, 사용된 장치에 상관없이 하나의 방문에 대해서는 변경되지 않습니다. 이것은 후속 데이터 연결 시 새 장치에서 지리 특성 데이터가 일반적으로 포함되지 않음을 의미합니다.
* 브라우저, 운영 체제 및 색상 깊이와 같은 기술 열은 방문의 첫 번째 히트에서 기록됩니다. 지리 특성 값과 마찬가지로 이 값은 연결된 프로필에 복사되지 않습니다.
* 마케팅 채널은 해당 장치에 대한 첫 번째 인증이 들어 있는 후속 데이터 연결의 다른 채널을 덮어씁니다.
