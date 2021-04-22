---
description: 직접 호출 규칙 조건 만들기.
keywords: Dynamic Tag Management;규칙;규칙 만들기;새 규칙;직접 호출 규칙
solution: Experience Cloud,Analytics,Target
title: 직접 호출 규칙 조건 만들기
uuid: bab0e058-a5b8-4039-8333-5e8f3d06ade4
exl-id: f913a000-cdc1-4e6f-a56f-26c4d73d2299
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '88'
ht-degree: 100%

---

# 직접 호출 규칙 조건 만들기

직접 호출 규칙 조건 만들기.

1. 직접 호출에서 **[!UICONTROL 에 전달되는 문자열을 따옴표 없이]**&#x200B;조건`_satellite.track()` 대화 상자에 지정합니다.

   ![](assets/conditions-direct-call.png)

   >[!NOTE]
   >
   >위에 설명한 대로 UI를 사용하여 직접 호출에서 `_satellite.track()`에 전달되는 문자열을 지정하는 경우 따옴표를 사용하지 마십시오. 편집기를 사용하여 [사용자 지정된 페이지 코드](/help/implement/other/dtm/c-aa-tool/customize-page-code.md)를 삽입하는 경우에는 따옴표를 사용해야 합니다.
