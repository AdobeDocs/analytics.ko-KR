---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: 8c06a54ccd652f3f915af3af040e9cc69f01d0c1

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

## 종료 링크 및 파일 다운로드 자동 추적

파일 다운로드 파일 형식 및 종료 링크를 정의하는 매개 변수를 기준으로 파일 다운로드 및 종료 링크를 자동으로 추적하도록 JavaScript를 구성할 수 있습니다.

자동 추적을 제어하는 매개 변수는 다음과 같습니다.

```
s.trackDownloadLinks=true 
s.trackExternalLinks=true 
s.linkDownloadFileTypes="exe,zip,wav,mp3,mov,mpg,avi,doc,pdf,xls" 
s.linkInternalFilters="javascript:,mysite.com,[more filters here]" 
s.linkLeaveQueryString=false 
```

매개변수 `trackDownloadLinks` and `trackExternalLinks` determine if automatic file download and exit link tracking are enabled. 활성화하면 에서 값 중 하나와 일치하는 파일 유형이 있는 모든 링크가 파일 다운로드로 `linkDownloadFileTypes` 자동 추적됩니다. 에 있는 값 중 하나를 포함하지 않는 URL이 있는 모든 링크는 자동으로 종료 링크로 `linkInternalFilters` 추적됩니다.

In JavaScript H.25.4 (released February 2013), automatic exit link tracking was updated to always ignore links with `HREF` attributes that start with `#`, `about:`, or `javascript:`.

### 예제 1

파일 유형을 `.jpg` 위에 포함하지 `.aspx` `linkDownloadFileTypes` 않으므로 파일 다운로드로 자동 추적되고 보고되지 않습니다.

The parameter `linkLeaveQueryString` modifies the logic used to determine exit links. When `linkLeaveQueryString`=false, exit links are determined using only the domain, path, and file portion of the link URL. When `linkLeaveQueryString`=true, the query string portion of the link URL is also used to determine an exit link.

### 예제 2

다음과 같이 설정하면 아래 예제가 종료 링크로 카운트됩니다.

```
//JS file  
s.linkInternalFilters="javascript:,mysite.com" 
s.linkLeaveQueryString=false 
 
//HTML file 
<a href='https://othersite.com/index.html?r=mysite.com'>Visit Other Site!</a> 
```

### 예제 3

다음과 같이 설정하면 아래 링크가 종료 링크로 카운트되지 않습니다.

```
//JS file  
s.linkInternalFilters="javascript:,mysite.com" 
s.linkLeaveQueryString=true 
 
//HTML  
<a href='https://othersite.com/index.html?r=mysite.com'>Visit Other Site</a> 
```

*참고: 하나의 링크는 파일 다운로드 또는 종료 링크로만 추적할 수 있습니다. 단, 파일 다운로드의 우선 순위가 높습니다. 링크가 매개 변수를 기반으로 하는 종료 링크와 파일 다운로드인`linkDownloadFileTypes``linkInternalFilters`경우 종료 링크가 아닌 파일 다운로드로 추적 및 보고됩니다.*