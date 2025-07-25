---
title: 데이터 증가 및 감소 문제 해결
description: 트렌드 보고서에서 극적인 증가 또는 감소를 볼 수 있는 가능한 이유를 알아봅니다.
exl-id: 1a91f95e-818f-423d-9247-e0bb96bd0018
feature: Curate and Share, Data Configuration and Collection
source-git-commit: 29ab0cc535bd8f74b50428c11756bf8b446a23ab
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 100%

---

# 데이터 증가 및 감소 문제 해결

사이트에서 데이터를 수집함에 따라 데이터 수집이나 보고에 크게 영향을 줄 수 있는 외부 요인이 많습니다. 다음은 특정 변수나 전체 트래픽이 동적으로 증가 또는 감소하는 이유에 대한 가능한 설명들의 목록입니다.

원인을 파악하고 해결 방법을 찾기 위해 노력할 때 이벤트가 데이터에 미치는 영향을 측정하고 진행할 방법을 결정할 수 있습니다. 자세한 내용은 [개요  페이지](overview.md)를 참조하십시오.

## 급격한 트래픽 감소

급격한 트래픽 감소는 부분 데이터와 제로 데이터, 이렇게 두 섹션으로 분류됩니다.

### 데이터 완전 손실의 잠재적 원인(0 보고)

* **보고서 세트 지연**: 간혹 보고서 세트는 많은 요인으로 인해 [지연](../latency.md)을 경험할 수 있습니다. 지연 문제 대부분은 1시간 이내에 해결됩니다. 특정 보고서 세트에 관심이 있는 경우 영향을 받는 보고서 세트 ID를 사용하여 Adobe 고객 지원 센터에 문의하십시오.
* **구현 제거**: 조직에서 구현을 변경하거나 사이트를 재구성할 때 Analytics를 다시 구현하는 것은 간과되는 경우가 있습니다. 조직의 개발자와 협력하여 사이트의 코드를 다시 구현하십시오.
* **Analytics 인터페이스/캐싱 문제**: 드문 경우, 브라우저의 캐시에 모든 보고서가 0을 반환하도록 하는 잘못된 데이터가 포함됩니다. 브라우저의 쿠키와 캐시를 지우면 문제가 해결됩니다. 쿠키/캐시를 지워도 문제가 해결되지 않으면, 고객 지원 센터에 연락하여 누락된 보고서와 날짜 범위를 알려 주십시오. 담당자가 문제를 재현하여 추가 정보를 제공할 수 있습니다.
* **Analytics 가용성**: 데이터 수집이나 처리와 관련한 문제에 대해서는 [status.adobe.com](https://status.adobe.com/products/1173/)에서 확인하십시오.

### 데이터 부분 누락 또는 트래픽 감소의 잠재적 원인

* **구현 변경**: [디버거](/help/implement/validate/debugger.md)를 사용하여 원하는 차원이 작동하는지 확인하십시오.
* **참조 트래픽 감소**: 다른 사이트의 인기 있는 배너 광고나 하이퍼링크를 제거하면 트래픽이 크게 감소할 수 있습니다. 더 자세히 조사하려면 감소 전후의 [참조 도메인](/help/components/dimensions/referring-domain.md) 차원에 대한 트렌드를 확인합니다.
* **사이트 성능 문제**: 로드 밸런서를 통한 트래픽 분배가 잘못되거나 사이트를 호스팅하는 서버에 문제가 있으면 Analytics 보고에서 감소가 발생할 수 있습니다. 조직 내에서 사이트의 무결성과 상태를 관리하는 팀과 협력하여 가능한 모든 성과 문제를 조사하십시오.
* **자연어 검색 순위 변경**: 다른 사이트가 일부 키워드에 대한 자연어 검색 등급을 배제하는 경우 트래픽이 잠재적으로 감소할 수 있습니다. 사이트가 더 이상 검색 결과의 첫 페이지에 있지 않다면 이러한 감소는 특히 두드러질 수 있습니다. 더 자세히 조사하려면 [검색 엔진](/help/components/dimensions/search-engine.md) 차원의 트렌드를 확인하십시오.
* **PPC 광고의 변경**: 기존 캠페인에 대한 광고 제목이나 설명을 변경하면 품질 점수가 달라질 수 있습니다. 일반적으로 높은 품질 점수는 키워드가 광고를 더 높은 위치에서 더 낮은 클릭당 비용으로 트리거함을 의미합니다. 더 자세히 조사하려면 [검색 키워드 - 유료](/help/components/dimensions/search-keyword.md) 차원의 트렌드를 확인하십시오.

## 급격한 트래픽 증가

급격한 트래픽 증가는 중복 데이터와 기타 원인, 이렇게 두 섹션으로 분류됩니다.

### 예상 데이터가 거의 또는 정확히 2배 증가하는 잠재적 원인

* **구현 내에서 여러 이미지 요청**: 구현에 페이지당 두 개 이상의 [`t()`](/help/implement/vars/functions/t-method.md) 메서드 호출이 포함되어 있는 경우 수집된 모든 데이터가 사실상 두 배가 됩니다. 중복 항목을 포착하려면 사이트의 디버거를 사용하여 여러 이미지 요청이 있는지 확인하십시오.
* **중복하는 데이터 소스 파일이 업로드됨**: 조직에서 [데이터 소스](/help/import/data-sources/overview.md)를 사용하는 경우 조직의 사용자가 동일한 파일을 Adobe Analytics에 두 번 업로드할 수 있습니다. 이 중복 업로드를 수행하면 보고서에서 해당 데이터가 효과적으로 두 배가 되어 트래픽 증가가 발생합니다.

### 트래픽 증가에 대한 기타 잠재적 원인

* **스파이더 또는 보트**: 큰 트래픽 증가가 갑자기 발생하는 경우 가장 먼저 찾아볼 사항은 스파이더나 보트의 가능성입니다. 각 보트에는 사이트에서 코드를 실행하는 자체 방법이 있으므로, 때때로 보트 식별이 까다로울 수 있습니다. IP를 차원으로 사용하여 Data Warehouse 보고서를 만들어 트래픽을 가장 많이 발생시키는 주소를 확인하십시오. 그런 다음 [보트 규칙](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md)이나 VISTA 규칙을 사용하여 이후 보고에서 보트 트래픽을 제거할 수 있습니다.
* **시작한 캠페인**: 이메일 캠페인이나 검색 엔진 최적화와 같은 마케팅 활동으로 인해 사이트에 급격한 트래픽 증가가 발생할 수 있습니다. 더 자세히 조사하려면 [추적 코드](/help/components/dimensions/tracking-code.md) 차원의 트렌드를 확인하십시오. 또한 마케팅 팀에 연락하여 급격한 증가가 의도적인지 확인하는 것이 도움이 될 수도 있습니다.
* **환경 또는 상황적 원인**: 휴일 또는 정황 이벤트가 발생한 경우(사이트가 알려진 리소스인 큰 이벤트나 다른 조직의 잔여 마케팅 활동 중) 사이트 트래픽이 증가할 수 있습니다. 트래픽이 증가할 수 있는 정황적 이유는 거의 무제한으로 있기 때문에 정확한 원인을 해결하는 것은 어렵습니다. 그러나 이러한 원인은 파악해야 할 가장 중요한 사항 중 일부이며, 조직에서는 이를 활용하고 그에 따라 비즈니스 결정을 내릴 수 있습니다. [페이지](/help/components/dimensions/page.md)나 [레퍼러](/help/components/dimensions/referrer.md) 차원의 트렌드를 확인하는 것은 트래픽의 출처를 결정하는 데 가장 좋은 시작 지점일 수 있습니다.

위의 이유 중 사이트에서 트래픽이 증가 또는 감소하는 잠재적인 원인이 없는 경우 Adobe 고객 지원 센터에 문의하십시오. 트래픽 증가 또는 감소의 출처를 찾는 데 도움이 될 수 있습니다. 인시던트 생성 시 갑작스런 증가 또는 감소를 명확하게 보여주는 특정 보고서를 다시 만드는 방법을 에이전트에게 알려 주십시오.
