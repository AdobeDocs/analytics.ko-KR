---
description: pageType 변수는 404(페이지가 없습니다) 오류 페이지를 지정하는 데에만 사용됩니다.
keywords: Analytics 구현
seo-description: pageType 변수는 404(페이지가 없습니다) 오류 페이지를 지정하는 데에만 사용됩니다.
seo-title: Pagetype 변수 잘못 설정
solution: Analytics
subtopic: 문제 해결
title: Pagetype 변수 잘못 설정
topic: 개발자 및 구현
uuid: eafaf 58 e-ba 07-416 f -89 b 9-694687 cc 4802
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Pagetype 변수 잘못 설정

pageType 변수는 404(페이지가 없습니다) 오류 페이지를 지정하는 데에만 사용됩니다.

여기에는 errorPage, 이 하나의 값만 가능합니다.

```js
pageType="errorPage"
```

404 오류 페이지에서는 *`pageName`*&#x200B;변수를 채우지 말아야 합니다. *`pageType`* 이 변수는 지정된 404 오류 페이지에서만 설정해야 합니다. Any page containing content should never have a value in the *`pageType`* variable. 컨텐츠가 들어 있는 페이지의 경우, 변수를 아래에서 보듯이 설정할 수 있습니다.

```js
pageType=""
```

변수의 목적과 관련하여 혼동이 생기지 않게 하려면 이 변수는 컨텐츠가 들어 있는 페이지에서 완전히 삭제하는 것이 가장 좋습니다.
