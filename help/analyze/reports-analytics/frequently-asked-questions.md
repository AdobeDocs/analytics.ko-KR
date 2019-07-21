---
description: 대부분의 FAQ 질문 중 일부에 대한 답변 및 문제 해결 제안 사항을 제공합니다.
keywords: Analytics 문제 해결
seo-description: 대부분의 FAQ 질문 중 일부에 대한 답변 및 문제 해결 제안 사항을 제공합니다.
seo-title: FAQ
title: FAQ
uuid: 285 B 0 EA 4-AA 07-4 D 39-A 74 F -37 B 1 D 02 D 19 F 1
translation-type: tm+mt
source-git-commit: fd1e2f1789ed9c8c31c89f0e7b6b7b2dd3ee114d

---


# FAQ

보고 및 분석에 대한 가장 자주 묻는 분석 질문 중 일부에 대한 답변 및 문제 해결 제안을 제공합니다. For frequently asked implementation questions, see the [FAQ](../../implement/faq.md) in the Implement user guide.

**내 계정이 잠겼습니다. 잠금을 해제하는 방법**

계정을 다시 활성화하려면 조직 내 관리자에게 문의하십시오. See also [Troubleshoot login issues with Adobe Analytics](../../technotes/troubleshoot-login.md) in the Technotes user guide.

**데이터가 수집되었다는 것을 알고 있어도 빈 보고서가 표시되는 이유는 무엇입니까?**

보고서 데이터 문제를 해결하기 위해 몇 가지 사항이 있습니다.

* 사용된 지표를 확인합니다. 일부 보고서는 보고 및 분석의 매출액에 기본적으로 사용됩니다. 보고 있는 지표가 보고서와 관련이 있는지 확인합니다.
* 날짜 범위 확인: 날짜 범위, 특히 조직의 데이터 유지 정책을 벗어나는 날짜 범위는 데이터를 반환하지 않을 수 있습니다. 날짜 범위가 올바르게 설정되어 있는지 확인합니다.
* 내부 URL 필터 확인: 일부 트래픽 소스 보고서는 내부 URL 필터를 올바로 정의하기 전까지는 작동하지 않습니다.

**탐색 메뉴에 일부 보고서가 누락되는 이유는 무엇입니까?**

메뉴에서 누락된 보고서는 제한된 권한 또는 메뉴 사용자 지정에서 가장 일반적으로 발생합니다. 필요한 모든 차원과 지표에 대한 액세스 권한이 있고 보고서 세트의 메뉴 구조를 사용자 지정하지 않았는지 확인하려면 조직 내에서 제품 관리자에게 문의하십시오.

**일부 긴 값이 잘리는 이유는 무엇입니까?**

Adobe Analytics의 거의 모든 변수는 문자 제한이 있습니다. 페이지 이름의 문자 제한은 100 자, 사용자 지정 전환 변수 (Evar) 의 길이는 255 자입니다. Adobe에 보내는 값이 잘리는 것을 방지하기 위해 간결하다는 것을 확인하는 것이 좋습니다.

**보고에서 주요 지연이 표시되는 이유는 무엇입니까?**

보통 전환 및 다른 처리량이 많은 데이터는 30-90분 내에 사용할 수 있는 반면, 실시간 보고에서는 일부 트래픽 지표를 수 분 내에 사용할 수 있습니다. 강력한 Experience Cloud 플랫폼을 사용해도 보고가 지연되는 경우가 있습니다. 지연을 지연이라고 합니다. See [Latency](../../technotes/latency.md) in the Technotes user guide for more information.

**Iphone에서 장치 버전이 표시되지 않는 이유는 무엇입니까?**

Apple 장치는 장치 버전이 아닌 사용자 에이전트 문자열에서 펌웨어 버전을 보고합니다. Adobe Analytics에서 사용 가능한 정보를 사용하여 iPhone 장치 버전을 판단하기는 어렵습니다. See [Comparing iPhone device versions](https://helpx.adobe.com/analytics/kb/comparing-iphone-device-versions.html) in the Analytics KB for more information.

**값을 합계하면 보고서 하단에 합계가 일치하지 않는 이유는 무엇입니까?**

차원 값이 여러 곳에 적용되는 경우가 종종 있습니다. 예를 들어, 자정을 확장하거나 단일 주문에 속하는 여러 제품을 방문하는 방문입니다. 차원 값은 해당되는 모든 라인 항목에 보고되지만 보고서 총계에서 중복 제거됩니다. See [Compare sum of line items to report total](https://helpx.adobe.com/analytics/kb/sum-line-items-different-from-total.html) in the Analytics KB for more information.

**내 보고서 세트에 있는 특정 IP 주소에서 데이터를 제외하려면 어떻게 합니까?**

보고서에서 사이트 테스트 및 직원 사용과 같은 내부 웹 사이트 활동 데이터를 제거할 수 있습니다. 이 기능을 사용하면 본인과 동료가 트래픽 데이터를 왜곡하지 않고 사이트를 방문할 수 있습니다. See [Exclude by IP Address](../../admin/admin/exclude-ip.md) in the Admin user guide for more information.

**보고서 세트를 삭제할 수 있습니까?**

보고서 세트 삭제는 불가능합니다. 하지만 Adobe Analytics의 모든 보기에서 보고서 세트를 숨길 수 있습니다. 숨겨진 보고서 세트로 전송된 서버 호출은 여전히 월별 계약 제한으로 계산됩니다. See [Hide report suites](../../admin/company/c-hide-report-suites.md) in the Admin user guide for more information.

**세그멘테이션을 사용할 때 어떤 컨테이너를 사용해야 합니까? Page view, visit, or visitor?**

사용하는 세그먼트 컨테이너는 데이터 캡처 범위에 따라 달라집니다. 페이지 보기 컨테이너는 세그먼트 기준과 일치하는 히트를 가져오기만 하면 방문의 관련 없는 부분을 필터링하는데 유용합니다. 방문 컨테이너는 하나 이상의 히트가 세그먼트 기준과 일치하는 방문의 모든 히트를 가져오도록 하며, 일반적으로 세션을 볼 때 유용합니다. 방문자 컨테이너는 세그먼트 기준과 일치하는 히트가 있는 모든 방문을 가져와서 사람을 찾는 데 유용합니다. 사용하기 가장 좋은 세그먼트 컨테이너를 결정하는 것은 분석가로서의 선택입니다. See [Segmentation overview](../../components/c-segmentation/seg-overview.md) in the Components user guide for more information.

**데이터가 데이터 웨어하우스에 표시되지 않는 이유는 무엇입니까?**

데이터 웨어하우스의 고유한 처리 아키텍처로 인해 플랫폼은 경로 지정과 같은 일부 데이터 유형을 처리하도록 최적화되지 않습니다. See [Data Warehouse segment compatibility](../../components/c-segmentation/seg-reference/seg-compatibility.md) in the Components user guide for more information.
