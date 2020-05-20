---
title: H 코드 구현 문제 해결
description: 이전 JavaScript 구현과 관련된 몇 가지 일반적인 문제를 알아봅니다.
translation-type: ht
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# H 코드 구현 문제 해결

다음은 H 코드 구현과 관련된 문제 해결 단계입니다.

## 헤드 태그에 Analytics 코드 넣기

>[!NOTE] H 코드 구현은 `<body>` 태그에서 코드를 참조해야 하지만, 다른 구현(예: Adobe Experience Platform Launch를 사용하는 구현)에서는 `<head>` 태그에서 코드를 참조해야 합니다.

Analytics 코드는 보이지 않는 1x1 픽셀 이미지를 생성합니다. 이전에는 일반적인 구현 방법이 `<head>` 태그에서 `s_code.js` 참조를 배치하는 것이었습니다. 여기에 코드를 삽입하면 이미지가 어떤 식으로든 페이지 레이아웃에 영향을 주지 않았습니다. 또한 코드가 더 일찍 실행되어, 부분적 페이지 로드에 대해 더 효과적으로 페이지 보기를 카운트할 수 있습니다.

하지만, 코드의 특정 요소에는 `<body>` 개체가 있어야 합니다. Analytics JavaScript 코드가 `<head>` 태그에 있으면 `<body>` 개체가 존재하기 전에 실행됩니다. 그 결과, 구현은 [!UICONTROL ClickMap] 데이터, 파일 다운로드나 종료 링크에 대한 자동 추적 또는 연결 유형 데이터를 수집하지 않습니다. `s_code.js`에 대한 스크립트 참조를 `<head>` 태그에 삽입하는 것은 효과가 있지만 그 결과는 매우 제한된 버전의 Analytics입니다.

Analytics 코드는 형식이 잘 지켜진 HTML 페이지의`<body>` 태그 내부의 어느 곳에든 삽입할 수 있습니다. Analytics 코드는 가능한 한 `<body>` 태그의 맨 위에 가깝게 배치하는 것이 좋습니다. 모든 페이지 변수가 `s_code.js` 파일이 로드된 후 설정되었는지 확인합니다.

>[!TIP] Adobe Analytics를 Adobe Target과 통합하려면, JavaScript 포함 파일을 페이지 하단에 삽입해야 합니다.
