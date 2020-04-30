---
description: 'null'
keywords: Analytics Implementation;implementation method;dynamic tag management;dtm
title: DTM 구현 개요
topic: Developer and implementation
uuid: 2d40cb7a-5c69-4f41-81a7-c48373c2d720
translation-type: tm+mt
source-git-commit: 3fe3442eae1bdd8b90acffc9c25d184714613c16

---


# DTM 구현 개요

Dynamic Tag Management를 사용하여 태그를 관리하고 디지털 마케팅 시스템에서 데이터를 수집 및 배포합니다. Dynamic Tag Management는 여러 소스의 데이터를 푸시하는 단일 데이터 계층을 제공합니다. Dynamic Tag Management를 사용하면 사용자별 컨텐츠를 반응형으로 게재할 수 있습니다.

이 도움말 섹션에서는 Dynamic Tag Management를 사용하여 Adobe Analytics를 구현하는 방법에 대한 특정 정보를 제공합니다. 다이내믹 태그 관리에 대한 자세한 내용은 [다이내믹 태그 관리 제품 설명서](https://docs.adobe.com/content/help/ko-KR/dtm/using/dtm-home.html)를 참조하십시오. DTM을 사용하기 시작할 때 DTM 및 일반 작업에 액세스하는 방법에 대한 자세한 내용은 다이내믹 태그 관리 제품 설명서의 [시작](https://docs.adobe.com/content/help/en/dtm/using/getting-started/get-started.html)을 참조하십시오.

다이내믹 태그 관리 구현 단계에 대한 자세한 요약은 Adobe Analytics 시작의 [다이내믹 태그 관리를 사용하여 배치 Adobe Analytics 배포](https://docs.adobe.com/content/help/en/analytics/implementation/other/dtm/dtm-implementation-overview.html)를 참조하십시오.

## 구현 단계 개요 {#section_D0BBB82486F44699AC7FF5E76E27434C}

이 안내서는 DTM을 사용하여 Analytics를 구현하는 다음 단계를 안내합니다.

1. [웹 속성을 만듭니다](/help/implement/other/dtm/t-create-web-property.md).
1. [호스팅 옵션을 구성합니다](/help/implement/other/dtm/t-configure-hosting.md).
1. [머리글 및 바닥글 코드를 각 관리 페이지에 추가합니다](/help/implement/other/dtm/c-headers-footers/t-header-footer-code.md).
1. [Adobe Analytics 도구 추가](/help/implement/other/dtm/c-aa-tool/analytics-dtm.md).
1. [데이터 요소](/help/implement/other/dtm/t-data-element.md), [규칙 및 조건](/help/implement/other/dtm/c-rules/t-rules-create.md) 및 [작업](/help/implement/other/dtm/c-rules/t-rules-actions.md)을 만듭니다.

1. 도구 및 규칙을 프로덕션 서버에 게시합니다.

