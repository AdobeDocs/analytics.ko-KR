---
title: H 코드 구현 문제 해결
description: 이전 JavaScript 구현과 관련된 몇 가지 일반적인 문제를 알아봅니다.
translation-type: tm+mt
source-git-commit: 69138bdedb42b66449426fee39822520ee4b1198

---


# H 코드 구현 문제 해결

다음은 H 코드 구현과 관련된 문제 해결 단계입니다.

## 헤드 태그에 Analytics 코드 넣기

> [!NOTE] H 코드 구현은 `<body>` 태그에서 코드를 참조해야 하지만, 다른 구현(예: Adobe Experience Platform Launch 사용)에서는 `<head>` 태그에서 코드를 참조해야 합니다.

Analytics 코드는 보이지 않는 1x1 픽셀 이미지를 만듭니다. 이전에는 일반적인 구현 방법이 `s_code.js` `<head>` 태그에 참조를 배치하는 것이었습니다. 여기에 코드를 삽입하면 이미지가 어떤 식으로든 페이지 레이아웃에 영향을 주지 않습니다. 또한 더 빨리 실행되므로 부분 페이지 로드에 대한 페이지 보기를 보다 효과적으로 카운트할 수 있습니다.

However, certain elements of the code require the existence of the `<body>` object. Analytics JavaScript 코드가 `<head>` 태그에 있으면 `<body>` 개체가 존재하기 전에 실행됩니다. As a result, your implementation does not collect [!UICONTROL ClickMap] data, automatic tracking of file downloads or exit links, or connection type data. 태그에 스크립트 참조를 `s_code.js` 삽입하는 `<head>` 것은 작동하지만 결과는 매우 제한된 버전의 Analytics입니다.

The Analytics code can be placed anywhere inside the `<body>` tag of a well-formed HTML page. Adobe에서는 Analytics 코드를 가능한 한 `<body>` 태그의 맨 위에 가깝게 배치하는 것이 좋습니다. 모든 페이지 변수가 `s_code.js` 파일이 로드된 후 설정되었는지 확인합니다.

> [!TIP] Adobe Analytics를 Adobe Target과 통합하려면 JavaScript 포함 파일을 페이지 하단에 배치해야 합니다.
