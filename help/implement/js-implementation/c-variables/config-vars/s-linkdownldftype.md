---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics Implementation
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: f1ebe5e89f62957c8bcc829be4b1a97463210f93

---


# s.linkDownloadFileTypes

 변수는 쉼표로 구분된 확장자 목록입니다.

사이트에 이러한 확장자를 가진 파일에 대한 링크가 포함된 경우 해당 링크의 URL이 [!UICONTROL 파일 다운로드] 보고서에 나타납니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|--- |--- |--- |--- |
| N/A | N/A | 트래픽 &gt; 사이트 트래픽 &gt; 파일 다운로드 | "exe, zip, wav, mp3, mov, mpg, avi, wmv, doc, pdf, xls" |

The *`linkDownloadFileTypes`* 변수는 *`trackDownloadLinks`*&#x200B;이 ‘True’로 설정된 경우에만 관련이 있습니다.

링크를 마우스 왼쪽 단추로 클릭해야만 [!UICONTROL 파일 다운로드] 보고서에서 계산됩니다. 페이지가 로드될 때 자동으로 시작되거나, 리디렉션 후에만 다운로드되는 모든 파일 다운로드는 [!UICONTROL 파일 다운로드] 보고서에서 계산되지 않습니다. 파일을 마우스 오른쪽 단추로 클릭하고 "다른 이름으로 대상 저장..." 옵션을 선택하면, [!UICONTROL 파일 다운로드] 보고서에서 계산되지 않습니다.

The *`linkDownloadFileTypes`*&#x200B;변수를 사용하여 RSS 피드 클릭을 추적할 수 있습니다. 다음 .xml 또는 다른 확장명을 가진 RSS 피드에 대한 링크가 있는 경우 *`linkDownloadFileTypes`* 목록에 ".xml"을 추가하면 각 RSS 링크를 클릭하는 빈도를 확인할 수 있습니다.

## 구문 및 가능한 값

파일 확장자만 포함(공백 없음).

```js
s.linkDownloadFileTypes="type1[,type2[,type3[...]]]"
```

모든 확장자를 목록에 포함할 수 있습니다. htm 또는 aspx와 같은 일반적인 파일 확장자가 *`linkDownloadFileTypes`*. 클릭할 때마다 추가 이미지 요청이 전송되어 주 서버 호출로 청구될 수 있습니다.

## 예

```js
s.linkDownloadFileTypes="exe,zip,wav,mp3,mov,mpg,avi,wmv,doc,pdf,xls"
```

```js
s.linkDownloadFileTypes="exe,zip,wav,mp3,mov,mpg,avi,wmv,doc,pdf,xls,xml"
```

## 구성 설정*

없음

## 함정, 질문 및 팁

* 다운로드 파일을 마우스 왼쪽 단추로 클릭한 경우에만 [!UICONTROL 파일 다운로드 보고서]에 URL이 나타납니다.
* 일반 파일 확장자를 *`linkDownloadFileTypes`* 에 포함하면 Adobe 서버로 전송되는 전체 서버 호출이 심각하게 증가할 수 있습니다.
* 파일 확장자가 *`linkDownloadFileTypes`*.
* JavaScript를 사용하는 링크(즉, javascript:openLink( ))는 파일 다운로드에서 카운트되지 않습니다.

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