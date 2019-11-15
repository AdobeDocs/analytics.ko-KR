---
description: 각 사이트 방문의 깊이를 백분율과 총 계수로 나타냅니다. 즉, 사이트의 평균 방문자가 떠나기 전에 보게 되는 페이지 수를 보여줍니다.
solution: Analytics
title: 경로 길이
topic: Reports
uuid: f1c29e78-279a-46a5-b758-d4f0da629239
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 경로 길이

각 사이트 방문의 깊이를 백분율과 총 계수로 나타냅니다. 즉, 사이트의 평균 방문자가 떠나기 전에 보게 되는 페이지 수를 보여줍니다.

사용자 지정 링크(s.tl 호출)는 페이지에 대한 경로 길이에 추가되지 않습니다. 하지만, prop(트래픽 변수)에 대한 경로 길이 계산에 포함됩니다.

동일한 값의 여러 인스턴스(재로드)는 경로 길이를 증가시키지 않습니다. 예:

**[!UICONTROL 페이지 A]** &gt; **[!UICONTROL 페이지]** B **[!UICONTROL &gt;]** 사용자 지정 링크 **[!UICONTROL &gt;]** 페이지 B= 경로 길이 2입니다. (사용자 지정 링크 및 페이지 B의 재로드는 경로 길이에 포함되지 않습니다.)

**[!UICONTROL Prop A]** &gt; **[!UICONTROL 사용자 지정]** 링크는 Prop B **[!UICONTROL &gt; Prop]** C= 경로 길이 3을 전달합니다. (Prop B에 대한 사용자 지정 링크는 경로 길이에 포함됩니다.)
