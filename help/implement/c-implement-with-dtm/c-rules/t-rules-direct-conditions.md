---
description: 직접 호출 규칙 조건 만들기.
keywords: 다이내믹 태그 관리;규칙;만들기 규칙;새 규칙;직접 호출 규칙
seo-description: 직접 호출 규칙 조건 만들기.
seo-title: 직접 호출 규칙 조건 만들기
solution: Experience Cloud,Analytics,Target,다이내믹 태그 관리
title: 직접 호출 규칙 조건 만들기
uuid: bab0e058-a5b8-4039-8333-5e8f3d06ade4
translation-type: tm+mt
source-git-commit: e060fb745d611f37f28708b3fe103c1191aa483b

---


# 직접 호출 규칙 조건 만들기

직접 호출 규칙 조건 만들기.

1. In the **[!UICONTROL Conditions]** dialog, specify the string that will be passed to `_satellite.track()` in your direct call, without quotes.

   ![](assets/conditions-direct-call.png)

   >[!NOTE]
   >
   >If you specify the string that will be passed to `_satellite.track()` in your direct call using the UI, as described above, do not use quotation marks. If you insert [customized page code](../../../implement/c-implement-with-dtm/c-aa-tool/customize-page-code.md#concept_7D6390823DFE4D29AF9505CCE1A79C3B) using the editor, you must use quotation marks.

