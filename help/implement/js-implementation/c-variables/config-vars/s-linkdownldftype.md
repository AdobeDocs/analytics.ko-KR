---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: 60dd1b300035e5149f53870239de85fb3174a77a

---


# s.linkDownloadFileTypes

 변수는 쉼표로 구분된 확장자 목록입니다.

사이트에 이러한 확장자를 가진 파일에 대한 링크가 포함된 경우 해당 링크의 URL이 [!UICONTROL 파일 다운로드] 보고서에 나타납니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|--- |--- |--- |--- |
| N/A | N/A | 트래픽 &gt; 사이트 트래픽 &gt; 파일 다운로드 | "exe, zip, wav, mp3, mov, mpg, avi, wmv, doc, pdf, xls" |

The  variable is only relevant when  is set to 'True.'*`linkDownloadFileTypes`**`trackDownloadLinks`*

링크를 마우스 왼쪽 단추로 클릭해야만 [!UICONTROL 파일 다운로드] 보고서에서 계산됩니다. 페이지가 로드될 때 자동으로 시작되거나, 리디렉션 후에만 다운로드되는 모든 파일 다운로드는 [!UICONTROL 파일 다운로드] 보고서에서 계산되지 않습니다. 파일을 마우스 오른쪽 단추로 클릭하고 "다른 이름으로 대상 저장..." 옵션을 선택하면, [!UICONTROL 파일 다운로드] 보고서에서 계산되지 않습니다.

The *`linkDownloadFileTypes`*&#x200B;변수를 사용하여 RSS 피드 클릭을 추적할 수 있습니다. If you have links to RSS feeds with a .xml or other extension, appending ",xml" to the  list allows you to see how often each RSS link is clicked.*`linkDownloadFileTypes`*

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