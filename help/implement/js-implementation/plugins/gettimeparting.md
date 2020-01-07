---
description: getTimeParting 플러그인은 사용자 지정 변수를 시간, 요일, 주말 및 평일 값으로 사용자 지정 변수에 채웁니다. Analysis Workspace는 기본 시간 나누기 차원을 제공합니다. 이 플러그인은 Analysis Workspace 외부의 다른 Analytics 솔루션에서 시간 나누기 차원이 필요한 경우 사용해야 합니다.
keywords: Analytics Implementation
subtopic: Plug-ins
title: getTimeParting
topic: Developer and implementation
uuid: 74f696a3-7169-4560-89b2-478b3d8385e1
translation-type: tm+mt
source-git-commit: 73d20b23e38bc619c156c418c95096a94d2fdfce

---


# getTimeParting

getTimeParting 플러그인은 사이트에서 측정 가능한 활동이 발생하는 시간을 세부적으로 캡처할 수 있는 완벽한 분석 솔루션을 제공합니다.

지정된 날짜 범위에서 반복 가능한 시간 분할로 지표를 분류하려면 getTimeParting 플러그인을 사용해야 합니다.  예를 들어 getTimeParting 플러그인을 사용하면 2일의 다른 요일(예: 모든 일요일과 모든 목요일), 2개의 다른 기간(예: 모든 아침과 모든 저녁) 또는 2분(예: 모든 10:00 AM 인스턴스와 모든 10:01 AM 인스턴스) 간의 전환율을 비교할 수 있습니다. 에 대해 값을 지정합니다.

[!DNL Analysis Workspace] 이 플러그인이 제공하는 것과 약간 다른 방식으로 서식이 지정된 유사한 기본 크기( [여기](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/dimensions/time-parting-dimensions.html)참조)를 제공합니다.  Adobe Consulting에서는 이 도움말 섹션의 나머지 부분에서 이 플러그인이 요구 사항에 보다 적합한 방식으로 데이터를 제공하는지 여부를 확인할 것을 권장합니다.

특정 날짜 범위에서 반복 가능한 시간 분할로 지표를 분류할 필요가 없는 경우 getTimeParting 플러그인을 사용할 필요가 없습니다.  또한 시간 분할 [!DNL Analysis Workspace] 차원으로도 충분하다면 이 플러그인을 구현할 필요가 없습니다.

>[!CAUTION] getTimeParting 플러그인의 버전 4.0+가 제공하는 솔루션은 플러그인의 이전 버전과 매우 다릅니다.  4.0 이전 버전에서 업그레이드하려는 경우 &quot;처음부터&quot; 솔루션을 구현해야 합니다.  즉, 플러그인에서 제공하는 데이터를 보유하고 이 설명서를 주의 깊게 읽어서 솔루션을 구현하기 전에 완전히 새로운 eVar(하나의 eVar)를 설정해야 합니다.

>[!CAUTION] 또한:이 버전의 플러그인은 Microsoft Internet Explorer 브라우저와 *완전히* 호환되지 않지만 Microsoft Edge 브라우저와 호환됩니다.   Internet Explorer를 사용하는 방문자는 지정된 시간대로 전환하지 않고 *로컬* 시간대에서만 시간을 제공할 수 있습니다.  Internet Explorer 브라우저의 데이터는 포함되지 않지만 존재여부는 아래의 예를 참조하십시오.

> [!NOTE] 다음 지침을 따르려면 사이트에서 데이터 수집 코드를 변경해야 합니다. 이 작업은 사이트의 데이터 수집에 영향을 줄 수 있으며 [!DNL Analytics] 사용 및 구현 경험이 풍부한 개발자가 수행해야만 합니다.

> [!WARNING] 프로덕션에 배포하기 전에 항상 모든 플러그인 구현을 테스트하여 데이터 수집이 예상대로 작동하는지 확인합니다.

## 전제 조건

없음

## 구현 방법

* 복사 + 다음 코드를 AppMeasurement 코드의 Plugins 섹션 내 어디에나 붙여넣습니다.

```function getTimeParting(a){a=document.documentMode?void 0:a||"Etc/GMT";a=(new Date).toLocaleDateString("en-US",{timeZone:a, minute:"numeric",hour:"numeric",weekday:"long",day:"numeric",year:"numeric",month:"long"});a=/([a-zA-Z]+).*?([a-zA-Z]+).*?([0-9]+).*?([0-9]+)(.*?)([0-9])(.*)/.exec(a);return"year="+a[4]+" | month="+a[2]+" | date="+a[3]+" | day="+a[1]+" | time="+(a[6]+a[7])}```

> [!NOTE] 또한 Adobe Launch와 같은 태그 관리자를 사용하여 플러그인 코드를 AppMeasurement 또는 기타 분석 솔루션에 첨부하지 않고도 배포할 수 있습니다

* doPlugins 함수 내에서 또는 시간 분할 데이터를 캡처해야 하는 다른 위치에서 아래에 설명된 대로 getTimeParting 함수를 실행합니다

**전달할 인수**

* t:(**선택 사항이지만 권장**&#x200B;문자열) 방문자의 현지 시간을 변환할 시간대의 이름입니다.  기본값은 &quot;Etc/GMT&quot; 또는 설정되지 않은 경우 UTC/GMT 시간으로 설정됩니다.  입력할 [값의 전체 목록은 https://en.wikipedia.org/wiki/List_of_tz_database_time_zones] 를 참조하십시오.

일반적인 값은 다음과 같습니다.

* 동부 표준시로 &quot;America/New_York&quot;
* &quot;미국/시카고&quot;(중부 표준시)
* Mountain Time의 &quot;America/Denver&quot;
* 태평양 표준시 기준 &quot;미국/로스앤젤레스&quot;

## 반환

getTimeParting 플러그인은 다음을 포함하는 문자열을 반환합니다.

* 올해
* 현재 달
* 현재 날짜(즉, 월의 날)
* 현재 일(예: 요일)
* 현재 시간(비군사적 시간)

위의 각 항목은 파이프(&quot;|&quot;) 문자로 구분됩니다.

## 호출 예

프랑스 파리의 eVar10(Adobe Analytics)을 사용하여 시간 분할 데이터를 캡처하려는 경우 다음 코드를 사용합니다.

```s.eVar10 = getTimeParting("Europe/Paris")```

캘리포니아 주 산호세에 위치한 경우 다음 코드를 사용하십시오.

```s.eVar10 = getTimeParting("America/Los_Angeles")```

가나의 아프리카 국가에 위치한 경우 다음 코드를 사용하십시오.

```s.eVar10 = getTimeParting();```

가나는 UTC/GMT 표준 시간대 내에 있습니다.  따라서 이 예에서는 이러한 상황에서 플러그인 인수가 필요하지 않음을 보여줍니다.

Internet Explorer 방문자의 데이터를 포함하지 않으려는 경우(IE 브라우저에서 반환된 값은 방문자의 현지 시간에서만 제공할 수 있으므로) 다음 코드를 사용하십시오.

```if(!document.documentMode) s.eVar10 = getTimeParting("America/New_York");```
```else s.eVar10 = "Internet Explorer Visitors";```

**호출 결과**

콜로라도주 덴버에서 온 방문자가 2020년 8월 31일 오전 9:15에 사이트를 방문하는 경우 다음 코드...

```s.eVar10 = getTimeParting("Europe/Athens");```

...s.eVar10을 **year=2020과 같게 설정합니다.| 월=8월| date=31| day=월요일| time=6:15 PM**

다음 코드...

```s.eVar10 = getTimeParting("America/Nome");```

... 대신 s.eVar10을 **year=2020과 같게 설정합니다.| 월=8월| date=31| day=월요일| time=6:15 AM**

다음 코드...

```s.eVar10 = getTimeParting("Asia/Calcutta");```

... 대신 s.eVar10을 **year=2020과 같게 설정합니다.| 월=8월| date=31| day=월요일| time=8:45 PM**

다음 코드...

```s.eVar10 = getTimeParting("Australia/Sydney");```

... 대신 s.eVar10을 **year=2020과 같게 설정합니다.| 월=9월| date=1| day=화요일| time=1:15 AM**

## Adobe Analytics 설정

Adobe Analytics에서 시간 분할 데이터를 캡처하려면 다음 특성을 가진 새 eVar를 설정하십시오.

* 이름:시간 분할
* 할당:최근(마지막)
* 만료 날짜:방문
* 다른 모든 속성은 제공된 기본값을 사용합니다
