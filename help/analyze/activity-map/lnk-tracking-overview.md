---
description: 'Activity Map은 다음과 같은 더 강력한 알고리즘으로 링크를 추적합니다. '
title: 강력한 링크 추적
topic: Activity map
uuid: a72b1652-2e69-41c7-8cf2-d39e9c705302
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 강력한 링크 추적

Activity Map은 다음과 같은 강력한 알고리즘으로 링크를 추적합니다.

* 링크가 페이지의 다른 위치에 표시되므로 동일한 링크가 다른 장치에서 혼동되는 경우를 방지하기 위해 페이지 영역의 추적을 포함합니다.
* LinkID와 관련된 문제나 다른 브라우저 업무에서 발생하는 문제로 인해 서로 다른 링크를 하나로 혼동하지 않도록 링크 고유성을 보장합니다.

Activity Map의 링크 추적에 대한 자세한 내용을 보려면 [여기로 이동하십시오](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md).

## Activity Map 링크 추적에서 PII 데이터를 수집하는 방법 {#section_AEE57510D17B4C21A7D49D32D21D67B9}

>[!CAUTION] Activity Map 추적을 켜면 개인 식별 정보(PII) 데이터를 수집할 수 있습니다. 이 데이터는 단독으로 사용하거나 다른 정보와 함께 사용하여 한 개인을 식별, 연락 또는 위치를 파악하거나, 혹은 컨텍스트에서 개인을 식별하는 데 쓰일 수 있습니다.

다음은 Activity Map 추적을 사용하여 PII 데이터를 수집할 수 있는 알려진 몇 가지 경우입니다.

* `Mailto` 링크. mailto 링크는 이메일을 보내기 위해 컴퓨터에서 기본 메일 클라이언트를 활성화하는 HTML 링크의 유형입니다.
* `User ID`. 사용자가 로그인한 후 웹 사이트의 머리글/바닥글에 표시될 수 있는 링크입니다.
* 금융 기관의 경우 계정 번호가 링크로 표시될 수 있습니다. 클릭하면 링크의 텍스트가 수집됩니다.
* 보건 의료 웹 사이트에도 링크로 표시된 PII 데이터가 있을 수 있습니다. 이러한 링크를 클릭하면 링크의 텍스트가 수집되어 PII 데이터가 수집됩니다.
