---
title: 음성 분석 차원
description: 음성 분석 차원
feature: Dimensions
exl-id: 6e1275c4-3b17-4c65-a308-d420ea1acdf6
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 4%

---

# 음성 분석 차원

[!UICONTROL 응용 프로그램 보고]에서 [[!UICONTROL 음성 및 챗봇]](/help/admin/tools/manage-rs/edit-settings/app-reporting.md)을 사용하도록 설정하면 다음 차원(및 [지표](../metrics/voice-metrics.md))이 만들어집니다. [컨텍스트 데이터 변수](/help/implement/vars/page-vars/contextdata.md)를 사용하여 원하는 문자열 값으로 설정할 수 있습니다. 보고서 세트 설정에서 활성화하면 음성 분석 차원을 연결된 컨텍스트 데이터 변수에 매핑하는 [처리 규칙](/help/admin/tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md)이 자동으로 만들어집니다.

| 차원 이름 | 설명 | 컨텍스트 데이터 변수 |
| --- | --- | --- |
| 음성 오류 유형 | 발생한 오류 유형. | `a.voiceerrortype` |
| 음성 언어 | 사용자가 음성 앱과 상호 작용하는 언어입니다. | `a.voicelanguage` |
| 음성 의도 | 사용자가 실행하려는 명령입니다. | `a.voiceintent` |
| 음성 앱 응답 | 음성 앱이 사용자에게 반환한 응답입니다. | `a.voiceappresponse` |
| 음성 인증 | 음성 앱과 상호 작용할 때 사용자의 인증된 상태입니다. | `a.voiceauthentication` |
| 관심 영역 ID | 관심 영역 ID입니다. | `a.loc.poi.id` |

{style="table-layout:auto"}
