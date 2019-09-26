---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
solution: null
title: 다이내믹 변수
translation-type: tm+mt
source-git-commit: 60dd1b300035e5149f53870239de85fb3174a77a

---


# s.linkLeaveQueryString

기본적으로 쿼리 문자열은 모든 보고서에서 제외됩니다.

일부 종료 링크 및 다운로드 링크의 경우 다음 샘플 URL에서와 같이 URL의 중요한 부분이 쿼리 문자열에 있을 수도 있습니다.

```js
https://www.mycompany.com/download.asp?filename=myfile.exe
```

다운로드 파일 이름은 쿼리 문자열에서 정의할 수 있으므로, [!UICONTROL 파일 다운로드] 보고서를 더 정확하게 만들려면 쿼리 문자열이 필요합니다.

The *`linkLeaveQueryString`* 변수는 [!UICONTROL 종료 링크] 및 [!UICONTROL 파일 다운로드] 보고서에 쿼리 문자열을 포함해야 하는지 여부를 결정합니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|--- |--- |--- |--- |
| N/A | N/A | Exit Links File Downloads | false |

>[!NOTE]
>
>Setting `linkLeaveQueryString=true` includes all query string parameters for all exit links and download links.

## 구문

```js
s.linkLeaveQueryString=[false/true]
```

## 예

```js
s.linkLeaveQueryString=false
```

## 가능한 값

```js
s.linkLeaveQueryString=false
```

```js
s.linkLeaveQueryString=true
```

## 구성 설정

이 변수에는 구성이 필요하지 않습니다.

## 함정, 질문 및 팁

* Setting `s.linkLeaveQueryString=true` includes all query string parameters for all exit links and download links.
* The `linkLeaveQueryString` variable does not affect recorded page URLs, visitor click map, or [!UICONTROL Path] reports.
