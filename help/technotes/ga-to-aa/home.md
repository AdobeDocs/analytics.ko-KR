---
title: 타사 분석 플랫폼에서 Adobe Analytics로 전환
description: Google Analytics와 같이 다른 플랫폼에 익숙한 사용자를 위한 보고서를 얻으려면 주요 개념을 학습합니다.
translation-type: tm+mt
source-git-commit: a5f612ba5e8446a56bc2bd252a8781e8ab1de403

---


# 타사 분석 플랫폼에서 Adobe Analytics로 전환

본 가이드는 Adobe Analytics의 핵심 개념 및 워크플로우에 대한 일반적인 보고서 유형을 소개하고 Adobe와 기타 인기 있는 툴 간의 주요 유사점과 차이점을 중점적으로 살펴봅니다. 이 가이드는 기본적인 디지털 분석 개념에 익숙한 분석가를 위해 설계되었지만 Adobe Analytics를 처음 접하는 사용자를 위해 고안되었습니다. 여기서는 조직에 Adobe 데이터 수집 서버로 데이터를 보내는 작업 구현이 있다고 가정합니다. If your organization has not yet set up an Adobe Analytics implementation, start with the [Adobe Analytics First Admin Guide](../../admin/admin-console/first-admin-guide.md).

Google Analytics와 Adobe Analytics는 웹 사이트 성과에 대한 중요한 통찰력을 얻을 수 있는 강력한 플랫폼입니다. 각각의 고유한 처리 아키텍처와 유저 인터페이스를 갖추고 있어 각 플랫폼에 고유한 이점이 있습니다. 이 가이드는 Adobe Analytics로 Google Analytics를 사용하는 사용자에게 도움이 되도록 설계되었습니다.

Adobe Analytics 에서는 Adobe Experience Cloud에 로그인한 다음 기본 보고서를 가져오는 두 가지 기본 방법이 있습니다.

* **보고 및 분석은** 기본 보고서를 가져오는 내역 방법입니다. 왼쪽 메뉴는 미리 작성된 보고서 목록을 제공하며 사용자가 원하는 보고서로 이동하고 데이터를 가져올 수 있도록 합니다. 세그먼트와 지표는 추가적인 사용자 지정을 제공할 수 있습니다. Google Analytics 보고서에 익숙한 사용자는 이 레이아웃을 익숙하게 찾을 수 있습니다.
* **분석 작업 공간은** 대부분의 보고서를 가져오는 데 권장되는 현재 방법입니다. 왼쪽 메뉴를 사용하면 구성 요소를 드래그 앤 드롭하여 보고서를 직접 작성할 수 있습니다. 이를 통해 정확한 보고 요구 사항을 보다 자유롭게 충족할 수 있습니다. Google Analytics 대시보드 및 사용자 지정 보고서 만들기에 익숙한 사용자는 이 레이아웃을 익숙하게 찾을 수 있습니다.

대부분의 보고서는 보고 및 분석 및 분석 작업 공간에서 만들 수 있습니다. 하지만 일부 보고서는 하나의 플랫폼 또는 다른 플랫폼에서만 가져올 수 있습니다. 대부분의 경우, 특정 기능이 보고 및 분석에서만 사용할 수 없는 경우 분석 작업 공간을 사용하는 것이 좋습니다.

## 권장되는 학습 경로

Adobe 에서는 보고서 데이터를 가져오는 기본 기본 사항으로 시작할 것을 권장합니다.

* [GA 사용자를 위한 분석 작업 공간에서 기본 보고서 만들기](reports/create-report.md)

분석 작업 공간의 구성 요소에 익숙해지면 올바른 구성 요소를 사용하여 대부분의 보고서를 다시 만드는 방법을 배울 수 있습니다.

* [Adobe Analytics에서 실시간 보고서 작성](reports/realtime-reports.md)
* [Adobe Analytics에서 대상 보고서 만들기](reports/audience-reports.md)
* [Adobe Analytics에서 획득 보고서 만들기](reports/acquisition-reports.md)
* [Adobe Analytics에서 동작 보고서 만들기](reports/behavior-reports.md)
* [Adobe Analytics에서 전환 보고서 만들기](reports/conversions-reports.md)

After learning to pull reports, understanding [processing and architecture differences](processing-differences.md) can help reconcile the different numbers obtained between platforms. [FAQ](faq.md) 도 제공됩니다.
