---
description: pageType 변수는 404(페이지가 없습니다) 오류 페이지를 지정하는 데에만 사용됩니다.
keywords: Analytics 구현
seo-description: pageType 변수는 404(페이지가 없습니다) 오류 페이지를 지정하는 데에만 사용됩니다.
seo-title: 잘못된 PageType 변수 설정
solution: Analytics
subtopic: 문제 해결
title: 잘못된 PageType 변수 설정
topic: 개발자 및 구현
uuid: eafaf58e-ba07-416f-89b9-694687cc4802
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# 잘못된 PageType 변수 설정

pageType 변수는 404(페이지가 없습니다) 오류 페이지를 지정하는 데에만 사용됩니다.

여기에는 errorPage, 이 하나의 값만 가능합니다.

```js
pageType="errorPage"
```

404 오류 페이지에서는 *`pageName`*&#x200B;변수를 채우지 말아야 합니다. *`pageType`* 변수는 지정된 404 오류 페이지에서만 설정해야 합니다. 콘텐츠가 들어 있는 모든 페이지에는 *`pageType`* 변수의 값이 있지 않아야 합니다. 컨텐츠가 들어 있는 페이지의 경우, 변수를 아래에서 보듯이 설정할 수 있습니다.

```js
pageType=""
```

변수의 목적과 관련하여 혼동이 생기지 않게 하려면 이 변수는 컨텐츠가 들어 있는 페이지에서 완전히 삭제하는 것이 가장 좋습니다.
