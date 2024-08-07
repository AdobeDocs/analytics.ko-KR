---
description: 다음 정보는 분석 데이터의 보고서 세트 지연 문제를 해결하는 데 도움이 될 수 있습니다.
keywords: 데이터 누락, 느림
title: 데이터 가용성 및 지연
feature: Data Configuration and Collection
exl-id: fedef3ea-dde6-460f-90e3-1e661ed29b78
source-git-commit: a17297af84e1f5e7fe61f886eb3906c462229087
workflow-type: tm+mt
source-wordcount: '818'
ht-degree: 100%

---

# Adobe Analytics의 데이터 가용성 및 지연

일반적으로 데이터가 수집되고 2시간 후에 보고서에서 전체 데이터를 볼 수 있습니다. 다음 정보는 분석 데이터의 보고서 세트 지연 문제를 해결하는 데 도움이 될 수 있습니다.

## 데이터 배치 이해

각 데이터 수집 서버는 원시 분석 데이터를 캡처하고 처리한 다음 묶인 데이터를 보고를 위해 시간별로 업로드합니다. 전환 프로세스에는 일반적으로 30분이 소요되므로, 이전 업로드 처리가 완료된 직후에 발생하는 트래픽의 일반 지연은 약 90분 (다음 묶음 업로드가 발생할 때까지 60분, 그런 다음 파일 전송 및 표시에 30분)입니다. 업로드하기 직전에 발생하는 트래픽의 경우 데이터 지연이 30분 (다음 배치 업로드가 발생할 때까지 0분, 그런 다음 파일 전송 및 표시에 30분)으로 하락할 수 있습니다.

필요한 경우 Adobe 고객 지원 센터에서 최상위 보고서 세트에 대해 30분 (시간별 대신) 일괄 데이터 업로드를 가능하게 할 수 있습니다.

## 지연 기여자

지연은 데이터 수집 서버가 데이터를 완전히 처리하는 데 걸리는 2시간보다 긴 지연입니다. 데이터 수집에는 영향을 주지 않습니다. 보고서 세트가 지연된 방식에 관계없이 작동 중인 구현을 위해 여전히 데이터가 수집됩니다. 심각도 (데이터의 최신 여부)와 길이 (해결에 소요되는 시간)가 크게 다를 수 있습니다. 일반적으로 지연은 단일 보고서 세트로 제한됩니다.

지연은 다음과 같은 일반 카테고리 중 하나에 의해 발생합니다.

* **예기치 않은 트래픽 스파이크:** 이 유형의 지연은 계약상으로 약정된 양 또는 예상보다 많은 데이터가 보고서 세트로 전송된 경우에 발생합니다. 지연이 일어나는 가장 흔한 원인입니다.
* **일반적인 하드웨어 문제:** Adobe는 데이터 센터 관리 및 모니터링, 데이터 중복, 하드웨어 안정성 면에서 최상의 전략을 사용하고 있습니다. 하드웨어는 발표된 유지 관리 기간 동안 정기적으로 업데이트됩니다. 하드웨어 문제를 긴급하게 보수하는 경우 교체 하드웨어가 온라인이 될 때까지 일시적으로 데이터 처리가 중지될 수 있습니다 (데이터 수집은 예외). 이러한 일시적인 처리 중지로 인해 눈에 띄는 지연이 생길 수 있습니다.
* **비정상 데이터:** 보트나 크롤러에 의한 비이상적인 긴 방문 등의 부자연스러운 데이터 패턴이 있으면 일시적으로 특정 처리 부담이 커져 지연이 생길 수 있습니다.

## 지연에 의존하는 기능

Adobe Experience Cloud의 일부 기능은 표준 처리 시간 외에 기본적인 지연 시간이 있습니다.

* Analytics for Target (A4T)에는 두 플랫폼에서 수집된 데이터를 동일한 히트에 저장할 수 있도록 하기 위해 5~10분 지연이 추가로 필요합니다.
* 타임스탬프가 지정된 데이터는 이 데이터가 처리되는 다른 서버로 인해 추가 시간이 필요합니다. 실시간으로 또는 실시간에 가깝게 수신된 타임스탬프 히트는 최대 15분이 소요될 수 있습니다. 어제 타임스탬프와 함께 받은 히트는 최대 2시간이 소요될 수 있습니다. 오래된 히트는 시간이 더 오래 걸리며, 매일 약 24시간까지 늘어납니다.

## 지연 완화 또는 방지 방법

지연을 방지하고 지연이 발생했을 때 복구 시간을 줄이기 위한 전략이 몇 가지 있습니다.

* **예상되는 트래픽 스파이크에 대해 Adobe에 알림:** 사이트의 모든 트래픽 스파이크를 예상할 수는 없지만 트래픽이 크게 증가할 것으로 예상되는 경우가 있을 수 있습니다. 예를 들면 특히 성공적인 휴일 기간 또는 대규모 캠페인 푸시 직후 등이 포함됩니다. 그런 경우 Adobe에서 제공하는 방법을 통해 조직에서 예상되는 트래픽 증가에 대해 알리면 보고서 세트에 추가 처리 리소스를 할당할 수 있습니다. Adobe에 트래픽 증가를 알리는 방법에 대한 자세한 내용은 관리 사용 안내서의 [트래픽 스파이크 예약](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/c-traffic-management/t-traffic-schedule-spike.md)을 참조하십시오.
* **새 기능을 활성화할 때 처리 부담 고려:** 일부 기능은 다른 기능에 비해 처리 부담이 큽니다. 보고서 세트에서 활성화된 기능이 많을수록 지연에서 복구하기도 어렵습니다. 보고서 세트에서 기능을 활성화할 때에는 처리할 데이터를 늘리는 다음 기능에 주의하십시오.

   * 동일한 페이지에서 20개 이상의 이벤트 구현
   * 복잡한 VISTA 규칙
   * 제품 변수에서 값 20개 초과
   * 이벤트 직렬화

* IAB 보트 필터링 활성화: [보트 필터링](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-removal.md)은 보고서 세트에 보트나 크롤러가 많이 등장하는 경우 지연을 줄이는 데 효과적입니다. IAB 보트 목록은 [Interactive Advertising Bureau](https://www.iab.net/about_the_iab)에서 업데이트 및 유지 관리되므로 이 목록을 사용하는 것이 좋습니다. 사용자가 보트 규칙을 사용자 지정하여 IAB의 규칙을 보완할 수도 있습니다.

## 지연 대응

지연이 발생하는 경우 Adobe는 처리 파이프라인을 적극적으로 모니터링하고 가능한 한 빨리 처리 시간을 정상으로 되돌리기 위해 가능한 모든 조치를 수행합니다. 지연 문제 대부분은 1시간 이내에 해결됩니다. 특정 보고서 세트가 걱정되는 경우에는 지원되는 사용자 중 한 사람이 지연되는 보고서 세트 ID를 고객 지원 센터에 알리고 문의하십시오. Adobe 담당자가 지연을 확인하고 문제 상황의 개선 및 해결에 대해 알려줄 수 있습니다.
