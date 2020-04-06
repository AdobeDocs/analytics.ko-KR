---
title: s_objectID
description: Activity Map은 사이트에서 고유 링크를 식별하는 데 도움이 됩니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# s_objectID

`s_objectID` 변수는 링크에 대한 고유 식별자를 제공합니다. 이 변수는 [Activity Map](/help/analyze/activity-map/activity-map.md)의 보고서를 더 정확하게 만드는 데 사용됩니다. 자주 변경되는 페이지에 링크가 있는 경우 데이터를 원하는 대로 올바로 그룹화할 수 있도록 `s_objectID` 변수를 사용하여 Activity Map에 고유한 링크 위치를 알려줄 수 있습니다.

Activity Map 정확도가 조직에 중요한 경우에는 사이트에 있는 링크의 `onClick` 이벤트에 `s_objectID` 변수를 포함하는 것이 좋습니다. 자세한 내용은 분석 사용 안내서의 [Activity Map 링크 추적 사용 사례](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-use-case.md)를 참조하십시오.

## Adobe Experience Platform Launch의 개체 ID

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용하십시오.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s_objectID

`s_objectID` 변수는 전역 변수입니다. 이것은 이 변수가 Analytics 추적 개체(기본적으로 `s`)와는 독립적으로 작동함을 의미합니다. 이 변수에 유효한 값은 최대 100바이트 길이의 모든 문자열일 수 있습니다. 이 변수가 정의되지 않으면 Activity Map에서는 링크 URL을 링크의 식별자로 사용합니다.

이 변수는 일반적으로 HTML 링크의 `onClick` 이벤트에서 설정됩니다.

```HTML
<a href="https://example.com" onClick="s_objectID='Example identifier';">Example link</a>
```

>[!NOTE] 항상 JavaScript 문을 완료하는 세미콜론을 포함하십시오. Activity Map이 기능하려면 세미콜론이 필요합니다.

## 사용 사례

`s_objectID` 변수는 Activity Map 보고에서 정확도를 높이고자 할 때 유용합니다.

### 수시로 바뀌는 다이내믹 컨텐츠의 링크 집계

일부 사이트에는 빈번하게 회전하는 항목이 있는 뉴스 사이트나 소매 사이트와 같이 수시로 바뀌는 다이내믹 컨텐츠가 있습니다. Activity Map에서는 기본적으로 링크 URL을 식별자로 사용하므로 링크가 빈번히 변경되는 페이지에서 가장 많이 클릭한 영역을 알기 어렵습니다. 이러한 링크 내에서 `s_objectID`를 사용하는  경우, Activity Map은 링크가 가리키는 URL에 관계없이 집계할 수 있는 링크를 파악합니다.

```HTML
<a href="story1.html" onClick="s_objectID='Top left link';">Story 1</a>
<a href="story2.html" onClick="s_objectID='Top center link';">Story 2</a>
<a href="story3.html" onClick="s_objectID='Top right link';">Story 3</a>
```

Activity Map은 링크가 가리키는 위치나 이러한 링크를 변경하는 빈도에 관계없이 `s_objectID`의 값을 기반으로 데이터를 집계합니다.

### 페이지에서 링크를 개별적으로 유지

일부 사이트에는 서로 다른 곳에서 동일한 위치를 가리키는 링크가 있습니다. 예를 들어 사이트의 머리글과 바닥글 모두에서 홈 페이지에 연결되는 링크가 있을 수 있습니다. 이러한 링크에는 동일한 URL이 있으므로 Activity Map이 해당 데이터를 집계합니다. 그러면 `s_objectID` 변수를 사용하여 분리할 수 있습니다.

```HTML
<a href="index.html" onClick="s_objectID='Header home link';">Example link in Header</a>
<a href="index.html" onClick="s_objectID='Footer home link';">Example link in Footer</a>
```

링크가 동일한 URL을 가리키더라도, Activity Map에서는 `s_objectID` 변수를 사용하여 보고에서 해당 링크를 올바로 구분할 수 있습니다.
