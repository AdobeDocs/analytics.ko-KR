---
title: 운영 체제
description: 방문자의 운영 체제입니다.
feature: Dimensions
exl-id: e3911ae0-d242-4da2-a4bc-b2f4877f9dd2
source-git-commit: 17c441f8855b8ca0604076763817de8d4d3b8efb
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 34%

---

# 운영 체제

운영 체제 차원은 방문자가 사용한 운영 체제와 버전을 보여 줍니다. 웹 속성에 OS별 기능이 있는 경우 이 차원을 통해 가장 일반적인 운영 체제를 파악할 수 있습니다.

## 이 차원을 데이터로 채우기

이 차원은 Adobe 내부의 조회 테이블을 참조합니다. 조회 값은 이미지 요청에 있는 `User-Agent` HTTP 헤더를 기반으로 합니다. AppMeasurement 라이브러리를 사용하는 경우(Adobe Experience Platform의 태그 등을 통해) 이 차원은 즉시 작동합니다.

## 차원 항목

차원 항목에는 방문자가 사용하는 운영 체제가 포함됩니다. 예로는 `"Windows 10"`, `"OS X 10.15"` 및 `"Android 9"`가 있습니다.

## 레이블 지정 및 정의 변경

다음은 사용자 에이전트 및 Adobe Analytics 보고에서 운영 체제가 표시되는 방식과 관련된 특정 문제 목록입니다.

### Apple 운영 체제에 대한 명명 규칙 변경:

버전 11부터는 OS X 대신 MacOS을 사용하여 Apple 운영 체제를 참조합니다.

예:

* &quot;OS X 10.15&quot;(UA 문자열의 표현보다 버전 10.15.7에 대한 아래 참고 사항 참조)
* &quot;MacOS 11.0.0

### 버전 10.15.7 이후의 사용자 에이전트에서 Mac OS 버전이 올바르지 않음 

Apple 컴퓨터의 사용자 에이전트는 최신 버전인 경우에도 OS 버전을 10.15.7로 표시합니다. 이는 UA에서 버전 11을 포함하는 것이 일부 웹 사이트에 문제를 일으켰기 때문에 수행되었습니다. 다음에 대해 true입니다. *모든 브라우저* 및 는 Chromium 브라우저에서 Google의 사용자 에이전트 &#39;중단&#39;과 관련이 없습니다.

클라이언트 힌트에는 플랫폼 버전 힌트에 올바른 버전이 포함되어 있습니다(&quot;Sec-CH-UA-Platform-Version&quot;). 이는 높은 엔트로피 힌트이므로 Adobe에 의해 자동으로 수집되지 않습니다. 다음을 참조하십시오. [Adobe Analytics 힌트 FAQ](https://experienceleague.adobe.com/docs/analytics/technotes/client-hints.html?lang=en) 높은 엔트로피 힌트를 수집하는 방법에 대한 자세한 정보입니다.

### Windows 11로 시작하는 사용자 에이전트에서 Windows 버전이 올바르지 않음

2023년 1월 현재 모든 브라우저의 사용자 에이전트는 Windows 11을 Windows 10으로 표시합니다.

클라이언트 힌트에는 플랫폼 버전 힌트에 올바른 버전이 포함되어 있습니다(&quot;Sec-CH-UA-Platform-Version&quot;). 이는 높은 엔트로피 힌트이므로 Adobe에 의해 자동으로 수집되지 않습니다. 다음을 참조하십시오. [Adobe Analytics 힌트 FAQ](https://experienceleague.adobe.com/docs/analytics/technotes/client-hints.html?lang=en) 높은 엔트로피 힌트를 수집하는 방법에 대한 자세한 정보입니다.
