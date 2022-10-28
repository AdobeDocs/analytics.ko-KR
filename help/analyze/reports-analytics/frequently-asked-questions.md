---
description: 가장 자주 묻는 일부 Analytics 질문에 대한 답변 및 문제 해결 제안 사항을 제공합니다.
keywords: Analytics 문제 해결
title: Reports & Analytics에 대해 자주 묻는 질문
feature: Reports & Analytics Basics
role: User, Admin
exl-id: 99702728-971f-484a-91f5-f3210b89485c
source-git-commit: 4ddc2640aa8b3a22411c86ff8bfe0ecf345a3d63
workflow-type: ht
source-wordcount: '843'
ht-degree: 100%

---

# FAQ

{{ra-eol}}

Reports &amp; Analytics에 대한 대부분의 FAQ 중 일부에 대한 답변 및 문제 해결 제안 사항을 제공합니다. 구현에 대한 FAQ에 대해서는 구현 안내서의 [FAQ](/help/implement/faq.md)를 참조하십시오.

>[!IMPORTANT]
>**2023년 12월 31일**&#x200B;부로 Adobe는 Reports &amp; Analytics 및 관련 보고서와 기능에 대한 서비스를 중단할 예정입니다. 해당 시점에 Reports &amp; Analytics 및 모든 관련 보고서와 일정이 작동 중단될 예정입니다. Reports &amp; Analytics가 제공하는 보고서, 시각화 및 기반 기술은 더 이상 Adobe의 기술 표준을 충족하지 않습니다. 대부분의 Reports &amp; Analytics 기능은 Analysis Workspace 내에서 사용할 수 있습니다. 2015년 Analysis Workspace가 출시된 이후 Reports &amp; Analytics 기능이 Analysis Workspace로 이전되면서 워크플로 패리티의 한계점에 도달했습니다. 이 공지 사항은 서비스 종료 프로세스에 대해 설명합니다.

**내 계정이 잠겼습니다. 어떻게 잠금을 해제합니까?**

계정을 다시 활성화하려면 조직 내 관리자에게 문의하십시오. Technotes 사용 안내서의 [Adobe Analytics 로그인 문제 해결](/help/technotes/troubleshoot-login.md)도 참조하십시오.

**데이터가 수집되는 것을 알지만 빈 보고서가 표시되는 이유는 무엇입니까?**

보고서 데이터 문제를 해결하기 위해 몇 가지 확인할 사항이 있습니다.

* 사용된 지표 확인: 일부 보고서는 Reports &amp; Analytics에서 기본적으로 매출로 설정됩니다. 보고 있는 지표가 보고서와 관련이 있는지 확인합니다.
* 날짜 범위 확인: 날짜 범위, 특히 조직의 데이터 유지 정책을 벗어나는 날짜 범위는 데이터를 반환하지 않을 수 있습니다. 날짜 범위가 올바르게 설정되어 있는지 확인합니다.
* 내부 URL 필터 확인: 일부 트래픽 소스 보고서는 내부 URL 필터를 올바르게 정의해야 작동합니다.

**탐색 메뉴에 일부 보고서가 없는 이유는 무엇입니까?**

메뉴에서 누락된 보고서는 주로 제한된 권한 또는 메뉴 사용자 지정에서 비롯됩니다. 필요한 모든 차원과 지표에 대한 액세스 권한이 있고 보고서 세트의 메뉴 구조가 사용자 지정되지 않았는지 조직 내 제품 관리자에게 문의하십시오.

**일부 긴 값이 잘리는 이유는 무엇입니까?**

Adobe Analytics의 거의 모든 변수에는 문자 제한이 있습니다. 페이지 이름은 100자로 제한되어 있고, 사용자 지정 전환 변수 (eVar)는 255자로 제한되어 있습니다. Adobe로 보내는 값이 잘리지 않도록 간결한 것이 좋습니다.

**보고에서 중요한 지연이 발생하는 이유는 무엇입니까?**

보통 전환 및 다른 처리량이 많은 데이터는 30-90분 내에 사용할 수 있는 반면 실시간 보고에서는 일부 트래픽 지표를 수 분 내에 사용할 수 있습니다. 강력한 Experience Cloud 플랫폼을 사용해도 보고가 지연되는 경우가 있습니다. 이러한 지연을 지연이라고 합니다. 자세한 내용은 Technotes 사용 안내서의 [지연](/help/technotes/latency.md)을 참조하십시오.

**iPhone에서 디바이스 버전을 볼 수 없는 이유는 무엇입니까?**

Apple 디바이스는 디바이스 버전이 아니라 사용자 에이전트 문자열에 있는 펌웨어 버전을 보고합니다. Adobe Analytics에서 사용할 수 있는 정보를 사용하여 iPhone 디바이스 버전을 확인하는 것은 어렵습니다. 자세한 내용은 Analytics KB의 [iPhone 디바이스 버전 비교](https://helpx.adobe.com/kr/analytics/kb/comparing-iphone-device-versions.html)를 참조하십시오.

**값을 합할 때 보고서 하단의 합계가 일치하지 않는 이유는 무엇입니까?**

차원 항목은 여러 위치에 적용할 수 있습니다 (예: 자정 또는 단일 주문에 속하는 여러 제품에 걸친 방문 수). 차원 항목은 적용 가능한 모든 라인 항목에 걸쳐 보고되지만 보고서의 합계에 중복됩니다. 자세한 내용은 Analytics KB의 [라인 항목 합계와 보고서 합계 비교](https://helpx.adobe.com/kr/analytics/kb/sum-line-items-different-from-total.html)를 참조하십시오.

**내 보고서 세트에 있는 특정 IP 주소에서 데이터를 제외하려면 어떻게 합니까?**

보고서에서 사이트 테스트 및 직원 사용과 같은 내부 웹 사이트 활동 데이터를 제거할 수 있습니다. 이 기능을 사용하면 본인과 동료가 트래픽 데이터를 왜곡하지 않고 사이트를 방문할 수 있습니다. 자세한 내용은 관리자 가이드의 [IP 주소 기준 제외](/help/admin/admin/exclude-ip.md)를 참조하십시오.

**보고서 세트를 삭제할 수 있습니까?**

보고서 세트는 삭제할 수 없습니다. 하지만 Adobe Analytics의 모든 보기에서 보고서 세트를 숨길 수 있습니다. 숨겨진 보고서 세트로 전송된 서버 호출은 여전히 월별 계약 제한에 포함됩니다. 자세한 내용은 관리자 가이드의 [보고서 세트 숨기기](/help/admin/company/c-hide-report-suites.md)를 참조하십시오.

**세그먼테이션을 사용할 때 페이지 보기, 방문 또는 방문자 중 어떤 컨테이너를 사용해야 합니까?**

사용하는 세그먼트 컨테이너는 데이터를 캡처하려는 범위에 따라 다릅니다. 페이지 보기 컨테이너는 세그먼트 기준과 일치하는 히트만 가져오므로 관련이 없는 방문 수 부분을 필터링하는 데 유용합니다. 방문 컨테이너는 하나 이상의 히트가 세그먼트 기준과 일치하는 방문의 모든 히트를 가져오므로 일반적으로 세션을 보는 데 유용합니다. 방문자 컨테이너는 히트가 세그먼트 기준과 일치하는 모든 방문 수를 가져오므로 사람을 보는 데 유용합니다. 분석가로서 가장 사용하기 좋은 세그먼트 컨테이너를 결정할 수 있습니다. 자세한 내용은 구성 요소 사용 안내서의 [세그먼테이션 개요](/help/components/segmentation/seg-overview.md)를 참조하십시오.

**내 세그먼트가 Data Warehouse에 표시되지 않는 이유는 무엇입니까?**

Data Warehouse의 고유한 처리 아키텍처로 인해 플랫폼은 경로 지정과 같은 일부 유형의 데이터를 처리하도록 최적화되지 않았습니다. 자세한 내용은 구성 요소 사용 안내서의 [Data Warehouse 세그먼트 호환성](/help/components/segmentation/seg-reference/seg-compatibility.md)을 참조하십시오.
