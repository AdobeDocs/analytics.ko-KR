---
description: 다이내믹 태그 관리 라이브러리가 사이트에 제대로 로드되는지 확인합니다.
keywords: Analytics 구현; 구현 방법; 다이내믹 태그 관리; DTM; code; 페이지 코드; 머리글 코드; 바닥글 코드; 포함 코드; 코드 확인; header code; 바닥글 코드 확인; 포함 탭; 임베드
seo-description: 다이내믹 태그 관리 라이브러리가 사이트에 제대로 로드되는지 확인합니다.
seo-title: 머리글 및 바닥글 코드 확인
solution: Analytics
title: 머리글 및 바닥글 코드 확인
topic: 개발자 및 구현
uuid: D 395 A 417-0 C 61-41 A 6-A 124-D 2 F 400 F 4626 F
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 머리글 및 바닥글 코드 확인

다이내믹 태그 관리 라이브러리가 사이트에 제대로 로드되는지 확인합니다.

1. 브라우저에서 사이트를 엽니다.
1. Open the [!UICONTROL Developer Console] by right-clicking and choosing **[!UICONTROL Inspect Element]** &gt; **[!UICONTROL Console]**.
1. **[!UICONTROL Enter]**&#x200B;키를 누릅니다.

   If the code was properly installed, you will see *`true`* display in the console.

   코드가 제대로 설치되지 않으면, 참조 오류가 표시됩니다.

   `_satellite is not defined`

   이 오류가 표시된다면 다음 사항을 확인하십시오.

* You have included the full header code on every page of the site in the [!DNL HEAD] section, as close to the [!DNL <head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">] 태그에 가깝게 넣으십시오.
* 코드 조각에, 형식이 지정된 문서에서 복사하여 붙여넣은 결과로서 발생할 수 있는, 예상하지 못한 문자가 나타나고 있습니다.

