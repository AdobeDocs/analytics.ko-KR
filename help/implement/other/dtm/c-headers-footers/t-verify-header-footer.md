---
description: Dynamic Tag Management 라이브러리가 사이트에 제대로 로드되는지 확인합니다.
keywords: Analytics 구현;구현 방법;dynamic tag management;dtm;코드;페이지 코드;머리글 코드;바닥글 코드;포함 코드;코드 확인;머리글 코드 확인;바닥글 코드 확인;포함 탭;포함
title: 머리글 및 바닥글 코드 확인
topic-fix: Developer and implementation
uuid: d395a417-0c61-41a6-a124-d2f400f4626f
exl-id: bed44ba7-8e0e-49e2-bedc-fb1ba66e5b18
translation-type: ht
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: ht
source-wordcount: '162'
ht-degree: 100%

---

# 머리글 및 바닥글 코드 확인

Dynamic Tag Management 라이브러리가 사이트에 제대로 로드되는지 확인합니다.

1. 브라우저에서 사이트를 엽니다.
1. 마우스 오른쪽 단추를 클릭하고 [!UICONTROL 요소 검사] > **[!UICONTROL 콘솔]**&#x200B;을 선택하여 **[!UICONTROL 개발자 콘솔]**&#x200B;을 엽니다.
1. **[!UICONTROL Enter]** 키를 누릅니다.

   코드가 제대로 설치되어 있으면 콘솔에 *`true`*&#x200B;가 표시됩니다.

   코드가 제대로 설치되지 않으면, 참조 오류가 표시됩니다.

   `_satellite is not defined`

   이 오류가 표시된다면 다음 사항을 확인하십시오.

* [!DNL HEAD] 섹션에서 사이트의 모든 페이지에 대한 전체 머리글 코드를 가능한 한 `<head>` 태그에 가깝게 포함했습니다.
* 코드 조각에, 형식이 지정된 문서에서 복사하여 붙여넣은 결과로서 발생할 수 있는, 예상하지 못한 문자가 나타나고 있습니다.
