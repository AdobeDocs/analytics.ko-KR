---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: b38ba4222951d957c607cd764224028527835c7e

---


# s.trackExternalLinks

If  is 'true,'  and  are used to determine whether any link clicked is an exit link.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | N/A | True |

사이트의 다운로드 가능 파일에 대한 링크가 없거나, 다운로드 가능 파일을 클릭한 횟수를 추적하는 데 관심이 없을 경우에만 *`trackExternalLinks`*&#x200B;변수를 'false'로 설정해야 합니다. 종료 링크는 방문자를 사이트 외부로 보내는 모든 링크입니다. If *`trackExternalLinks`* is 'true,' then when you click an exit link, tracking data is immediately sent. 종료 링크와 함께 전송되는 데이터에는 링크 URL, 링크 이름, 및 해당 링크의 방문자 클릭 맵 데이터가 포함됩니다. If *`trackExternalLinks`* is 'false,' then visitor click map data for exit links on your site is likely to be under reported.

## 구문 및 가능한 값

*`trackExternalLinks`변수는 'true' 또는 'false'입니다.*

```
js
s.trackExternalLinks=true|false
```

## 예

```
js
s.trackExternalLinks=true 
```

```
js
s.trackExternalLinks=false
```

## 구성 설정

없음

## 함정, 질문 및 팁

* When *`trackExternalLinks`* is 'false,' links that take people away from your site are likely to be under reported in visitor click map.

* When *`trackExternalLinks`* is 'true,' data is sent each time a visitor clicks on an exit link (before link target loads).
