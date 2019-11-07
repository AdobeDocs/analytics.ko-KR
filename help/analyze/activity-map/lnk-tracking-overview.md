---
description: 'Activity Map은 다음과 같은 더 강력한 알고리즘으로 링크를 추적합니다. '
seo-description: 'Activity Map은 다음과 같은 더 강력한 알고리즘으로 링크를 추적합니다. '
seo-title: 강력한 링크 추적
solution: Analytics
title: 강력한 링크 추적
topic: Activity Map
uuid: a72b1652-2e69-41c7-8cf2-d39e9c705302
translation-type: ht
source-git-commit: 38eb2298a2fc351591542bdfac9016ce4497c484

---


# 강력한 링크 추적

Activity Map은 다음과 같은 더 강력한 알고리즘으로 링크를 추적합니다.

* 장치에 따라 페이지에서 링크가 표시되는 위치가 서로 달라서 여러 다른 장치에서 동일한 링크를 혼동하게 되는 문제가 발생하지 않도록 페이지 영역에 대한 추적을 포함합니다.
* LinkID 문제나 서로 다른 브라우저 업체 문제로 인해 다른 링크가 같은 것으로 혼동되지 않도록 링크 고유성을 보장합니다.

Activity Map에서의 링크 추적에 대한 자세한 내용을 보려면 [여기](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md)로 이동하십시오.

## Activity Map 링크 추적에서 PII 데이터를 수집하는 방법 {#section_AEE57510D17B4C21A7D49D32D21D67B9}

> [!CAUTION] Activity Map 추적을 켜면 개인 식별 정보(PII) 데이터를 수집할 수 있습니다. 이 데이터는 단독으로 사용하거나 다른 정보와 함께 사용하여 한 개인을 식별, 연락 또는 위치를 파악하거나, 혹은 컨텍스트에서 개인을 식별하는 데 쓰일 수 있습니다.

다음은 Activity Map 추적을 사용하여 PII 데이터를 수집할 수 있는 알려진 몇 가지 경우입니다.

* `Mailto` 링크. mailto 링크는 이메일을 보내기 위해 컴퓨터에서 기본 메일 클라이언트를 활성화하는 HTML 링크의 유형입니다.
* `User ID`. 사용자가 로그인한 후 웹 사이트의 머리글/바닥글에 표시될 수 있는 링크입니다.
* 금융 기관의 경우 계정 번호가 링크로 표시될 수 있습니다. 클릭하면 링크의 텍스트가 수집됩니다.
* Healthcare 웹 사이트에는 링크로 표시된 PII 데이터가 있을 수 있습니다. 이러한 링크를 클릭하면 링크의 텍스트를 수집하므로 PII 데이터가 수집됩니다.
