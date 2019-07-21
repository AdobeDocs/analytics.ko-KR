---
description: '이전 열에는 데이터 수집으로 전송된 상태의 데이터가 있습니다. 이후 열에는 처리된 후의 값이 있습니다. '
keywords: 데이터 피드; 작업; pre column; 이후 열; 대/소문자 구분
seo-description: '이전 열에는 데이터 수집으로 전송된 상태의 데이터가 있습니다. 이후 열에는 처리된 후의 값이 있습니다. '
seo-title: 이전 열과 이후 열
solution: Analytics
title: 이전 열과 이후 열
topic: Reports & Analytics
uuid: A 415327 B -6151-4 D 08-B 8 B 9-5 AAA 2348 EB 0 C
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 이전 열과 이후 열

이전 열에는 데이터 수집으로 전송된 상태의 데이터가 있습니다. 이후 열에는 처리된 후의 값이 있습니다. 

예를 들어 변수 지속성, 처리 규칙, VISTA 규칙 및 통화 변환은 이후 열에 표시되는 변수에 대해 기록된 최종 값을 바꿀 수 있습니다. 사용자 지정 비즈니스 로직을 적용하는 경우(예를 들어 속성 결정을 위해 사용자 지정 공식 적용)를 제외하고 대부분의 계산에서 이후 열을 사용하는 것이 좋습니다.

열에 이전 또는 이후 버전이 없는 경우(예: `visit_num`) 이 열은 이후 열로 간주할 수 있습니다. Columns prefixed with " `pre_`" typically contain data that was populated by Adobe and not sent by your implementation. For example, `pre_browser` is populated by Adobe, but `evar1` is populated by your implementation. Both of these columns have a " `post_`" column ( `post_browser`, `post_evar1`), which contains the value used by reporting.

## 값에서의 대소문자 구분 {#section_F979E099BFAB4AFEBEA2D7E228963CE8}

대부분의 Analytics 변수는 보고 목적으로 대소문자를 구분하지 않는 것으로 간주되며, 이것은 대소문자가 달라도 동일한 값으로 간주됨을 의미합니다("snow", "Snow", "SNOW", 및 "sNow"가 모두 동일한 값으로 간주됨). 하지만, 대부분의 고객은 보고서 표시를 위해 대소문자를 혼합하여 보낼 수 있기를 원하므로 표시 목적으로 대소문자 구분 상태가 보존됩니다.

데이터 피드를 처리할 때, 표시 목적으로 대소문자 구분을 보존하고 싶더라도, 비교를 위해 소문자로 변환할 수 있습니다.

이전 열과 이후 열에서 동일한 값이 대소문자가 다르게 되어 있는 경우(예: 이전 열에는 "snow", 이후 열에는 "Snow") 사이트에서 동일한 값의 대문자 버전과 소문자 버전 모두를 전달한다는 의미입니다. 이후 열에서 대소문자가 다른 값은 이전에 전달되어 가상 쿠키에 저장되어 있거나, 해당 보고서 세트에 대해 동일한 시간 동안 처리되었습니다. 예:

히트 1: s.list1="Tabby,Persian,Siamese”;

히트 2: s.list1=“tabby,persian,siamese”;

히트 2가 데이터 피드에서 보고되면, 이전 열에는 전달된 정확한 대소문자가 들어 있게 됩니다(tabby,persian,siamese). 하지만 히트 1에서 나온 값은 해당 방문 동안 지속될 가능성이 높고, 대소문자 구분 없이 비교할 때는 정확하게 동일한 값이 히트 1과 2에 들어 있으므로 이 값은 이후 열에 보고됩니다(Tabby,Persian,Siamese).
