---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# s.trackExternalLinks

true면 및 를 사용하여 클릭된 링크가 종료 링크인지 여부를 결정합니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| N/A | N/A | N/A | True |

사이트의 다운로드 가능 파일에 대한 링크가 없거나, 다운로드 가능 파일을 클릭한 횟수를 추적하는 데 관심이 없을 경우에만 *`trackExternalLinks`*&#x200B;변수를 'false'로 설정해야 합니다. 종료 링크는 방문자를 사이트 외부로 보내는 모든 링크입니다. If *`trackExternalLinks`*&#x200B;가 'true'일 경우 종료 링크를 클릭하면 즉시 추적 데이터가 전송됩니다. 종료 링크와 함께 전송되는 데이터에는 링크 URL, 링크 이름, 및 해당 링크의 방문자 클릭 맵 데이터가 포함됩니다. If *`trackExternalLinks`*&#x200B;가 'false'이면 사이트의 종료 링크에 대한 방문자 클릭 맵 데이터가 제대로 보고되지 않을 수 있습니다.

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

* *`trackExternalLinks`*&#x200B;가 'false'이면 방문자가 사이트에서 떠나도록 하는 링크가 방문자 클릭 맵에 제대로 보고되지 않을 수 있습니다.

* *`trackExternalLinks`*&#x200B;가 'true'이면 방문자가 종료 링크를 클릭할 때마다(링크 대상이 로드되기 전에) 데이터가 전송됩니다.
