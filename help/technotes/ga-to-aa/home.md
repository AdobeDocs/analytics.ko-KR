---
title: 타사 분석 플랫폼에서 Adobe Analytics로 전환
description: Google Analytics 같은 다른 플랫폼에 익숙한 사용자에 초점을 맞춰, 보고서를 얻기 위한 주요 개념을 알아봅니다.
translation-type: tm+mt
source-git-commit: 3211598c2ff43493b329a9be4fb6877ae29cf08b
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 88%

---


# 타사 분석 플랫폼에서 Adobe Analytics로 전환

이 안내서에서는 Adobe 도구와 많이 사용되는 다른 도구의 주요 유사성 및 차이점을 중심으로, Adobe Analytics의 핵심 개념과 워크플로우를 학습하는 데 도움이 되는 일반적인 보고서 유형을 제공합니다. 이 안내서는 기본 디지털 분석 개념에 익숙하지만 Adobe Analytics를 처음 사용하는 분석가를 위해 마련되었습니다. 이 안내서에서는 조직에서 Adobe 데이터 수집 서버로 데이터를 전송하는 구현을 현재 운영 중이라고 가정합니다. 조직에서 아직 Adobe Analytics 구현을 설정하지 않은 경우 [Adobe Analytics 첫 번째 관리 안내서](/help/admin/admin-console/first-admin-guide.md)로 시작하십시오.

Google Analytics와 Adobe Analytics는 모두 웹 사이트 성능에 대한 중요한 통찰력을 얻을 수 있는 강력한 플랫폼입니다. 각 플랫폼에는 고유한 이점을 가진 자체 처리 아키텍처와 사용자 인터페이스가 있습니다. 이 안내서는 Google Analytics 사용 경험이 있는 사용자가 Adobe Analytics를 습득하는 데 도움을 주기 위해 설계되었습니다.

Adobe Analytics에는 Adobe Experience Cloud에 로그인한 후 기본 보고서를 가져오는 두 가지 기본 방법이 있습니다.

* **Reports &amp; Analytics**&#x200B;는 기본 보고서를 가져오는 이전 방법입니다. 왼쪽 메뉴에 미리 작성된 보고서 목록이 표시되어 사용자가 원하는 보고서를 탐색하고 데이터를 가져올 수 있습니다. 세그먼트와 지표는 추가 사용자 지정을 제공할 수 있습니다. Google Analytics 보고서를 사용한 적이 있는 사용자는 이 레이아웃이 익숙할 수 있습니다.
* **Analysis Workspace**&#x200B;는 현재 대부분의 보고서를 가져오는 데 권장되는 방법입니다. 왼쪽 메뉴를 사용하여 사용자는 구성 요소를 끌어 놓아 자신의 보고서를 작성할 수 있습니다. 이렇게 하면 훨씬 자유롭게 정확한 보고 요구 사항을 충족할 수 있습니다. Google Analytics 대시보드 및 사용자 지정 보고서를 만든 경험이 있는 사용자는 이 레이아웃이 익숙할 수 있습니다.

Most reports can be created in both [!UICONTROL Reports &amp; Analytics] and [!UICONTROL Analysis Workspace]. 그러나 일부 보고서는 한 플랫폼 또는 다른 플랫폼을 사용해서만 가져올 수 있습니다. In most cases, Adobe recommends using [!UICONTROL Analysis Workspace], unless a specific feature is only available in [!UICONTROL Reports &amp; Analytics].

## 권장 학습 경로

보고서 데이터 가져오기의 기본 사항으로 시작하는 것이 좋습니다.

* [GA 사용자를 위한 Analysis Workspace에서 기본 보고서 만들기](reports/create-report.md)

Once you are familiar with components in [!UICONTROL Analysis Workspace], you can learn how to recreate most reports using the right components.

* [Adobe Analytics에서 실시간 보고서 만들기](reports/realtime-reports.md)
* [Adobe Analytics에서 대상 보고서 만들기](reports/audience-reports.md)
* [Adobe Analytics에서 고객 확보 보고서 만들기](reports/acquisition-reports.md)
* [Adobe Analytics에서 동작 보고서 만들기](reports/behavior-reports.md)
* [Adobe Analytics에서 전환 보고서 만들기](reports/conversions-reports.md)

보고서를 가져오는 방법을 학습한 후 [처리 및 아키텍처 차이점](processing-differences.md)을 이해하면 플랫폼 간에 획득한 다른 숫자를 조정하는 데 도움이 됩니다. [FAQ](faq.md)도 이용할 수 있습니다.
