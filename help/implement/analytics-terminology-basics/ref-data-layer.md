---
description: '데이터 계층은 개발자가 페이지에 삽입하는 JavaScript 개체의 프레임워크입니다. '
keywords: Analytics 구현;데이터 계층;digitalData
seo-description: 데이터 계층은 개발자가 페이지에 삽입하는 JavaScript 개체의 프레임워크입니다. 데이터 계층은 보고서를 채우기 위해 추적 도구(Dynamic Tag Management와 같은 태그 관리 시스템 포함)에서 사용할 수 있습니다.
seo-title: 데이터 레이어
solution: Analytics
title: 데이터 레이어
topic: 개발자 및 구현
uuid: dedb2a50-06f3-4354-8993-a25d4952ce1e
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# 데이터 레이어

_데이터 계층_&#x200B;은 개발자가 페이지에 삽입하는 JavaScript 개체의 프레임워크입니다. 데이터 계층은 보고서를 채우기 위해 추적 도구(Adobe Experience Platform Launch 및 Dynamic Tag Management와 같은 태그 관리 시스템 포함)에서 사용할 수 있습니다.

사이트에서 데이터 계층을 구현하면 구현에 대한 최상의 제어와 유연성을 제공하고 향후 단계에서 가장 쉬운 유지 관리를 허용할 수 있습니다. 이러한 JavaScript 개체의 이름은 이론적으로 임의로 지정되지만, 권장 지침은 일관되고 예측 가능한 이름을 사용하는 것입니다. 개발자에게 이미 데이터 계층 또는 해당 형식에 대한 환경 설정이 있을 수 있습니다. 추적 커뮤니티가 시작 지점으로 작성한 여러 가지 표준이 있습니다. [Analytics 구현을 위한 데이터 계층](assets/datalayer-documentation.pdf) 사양 문서에서는 이 DTM 구현에 데이터 계층을 사용해야 하는 경우 가장 광범위한 추적 기술에서 허용한 W3C 표준 "digitalData" 개체를 사용합니다.
