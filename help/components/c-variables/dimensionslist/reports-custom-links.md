---
description: 방문자가 선호하는 링크를 표시합니다. 예를 들어 사이트의 홈 페이지에 같은 페이지를 표시하는 링크가 여러 개 있을 수 있습니다. 같은 페이지로 연결되는 그래픽 링크와 텍스트 링크가 모두 있는 경우입니다. 이 보고서는 방문자가 그래픽 링크와 텍스트 링크를 사용한 비율을 보여줍니다.
title: 사용자 지정 링크
topic: Reports
uuid: 2e0d0175-d5e4-4919-b601-3f488ef3e090
translation-type: ht
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# 사용자 지정 링크

방문자가 선호하는 링크를 표시합니다. 예를 들어 사이트의 홈 페이지에 같은 페이지를 표시하는 링크가 여러 개 있을 수 있습니다. 같은 페이지로 연결되는 그래픽 링크와 텍스트 링크가 모두 있는 경우입니다. 이 보고서는 방문자가 그래픽 링크와 텍스트 링크를 사용한 비율을 보여줍니다.

추적하기를 원하는 특정 링크는 특수 태그로 수정해야 합니다. [링크 추적](https://docs.adobe.com/content/help/ko-KR/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linktrackvars.html)을 참조하십시오.

[!UICONTROL 사용자 지정 링크 보고서]를 사용하여 다음을 수행할 수 있습니다.

* 방문자가 선호하는 링크 유형을 파악하여 가장 적합하게 사이트를 디자인합니다
* 단일 페이지에 중복 링크가 필요한지 여부를 검증합니다

## 모바일 SDK 링크 이름 {#section_70C91FE794104B5FBF289B19CC02EA8E}

[모바일 SDK](https://marketing.adobe.com/resources/help/ko_KR/mobile/home.html)에서는 사용자 지정 링크를 사용하여 작업 및 라이프사이클 지표를 추적합니다. 모바일 앱을 측정하는 데 사용되는 보고서 세트에서는 SDK에서 설정된 다음 링크 이름을 볼 수도 있습니다.

| ADBINTERNAL:Lifecycle | 4.x SDK에서 라이프사이클 호출에 의해 전송됨. |
|---|---|
| AMACTION:[작업 이름] | 4.x SDK에서 trackAction() 메서드에 의해 전송됨. 여기서 작업 이름은 메서드를 호출할 때 설정된 이름입니다. |
| ADMS BP Event | 3.x SDK에서 라이프사이클 호출에 의해 전송됨. |

