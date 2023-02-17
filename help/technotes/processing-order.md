---
title: Adobe Analytics의 데이터 처리 순서
description: Adobe Analytics에서 데이터를 처리하는 구성 요소 순서 및 서비스에 대해 알아봅니다.
exl-id: a8dc9c12-07d3-4dc8-b2df-136f7a7a1e77
source-git-commit: 1ca7040156f7f2105a9625f921de3d90b4175056
workflow-type: ht
source-wordcount: '588'
ht-degree: 100%

---

# Adobe Analytics의 데이터 처리 순서

Adobe는 보고에 표시되기 전에 데이터를 변경하거나 조작할 수 있는 다양한 방법을 제공합니다. 이 페이지에는 다양한 Adobe Analytics 기능이 데이터를 처리하는 순서가 표시됩니다. 이 목록을 사용하면 데이터 불일치 문제 해결이나 데이터 조정이 필요한 경우 사용할 최적의 기능을 결정할 수 있습니다.

![처리 순서](assets/processing-order.png)

## Adobe로 전송되기 전의 데이터

데이터가 Adobe로 전송되기 전에 일반적으로 다음 방법 중 하나를 사용하여 클라이언트측에서 컴파일됩니다.

* **AppMeasurement**: 사이트에서 호스팅되고 각 페이지에서 참조되는 JavaScript 파일. 데이터는 Adobe Analytics로 직접 전송됩니다.
* **Adobe Experience Platform Web SDK**: 사이트에서 호스팅되고 각 페이지에서 참조되는 JavaScript 파일. 데이터가 Adobe Experience Edge로 전송됩니다.
* **Adobe Experience Cloud Data Collection의 태그**: 각 페이지에서 참조되는 JavaScript 파일로, 데이터 수집 UI 내에서 생성된 규칙이 포함되어 있습니다. Adobe Analytics 확장을 사용하면 AppMeasurement를 보다 쉽게 구현할 수 있습니다. Web SDK 확장을 사용하면 Web SDK를 보다 쉽게 구현할 수 있습니다.

Adobe Experience Edge로 데이터를 전송하는 경우 Adobe Analytics(및 기타 많은 Adobe Experience Cloud 솔루션)로 데이터를 전송하도록 구성할 수 있습니다. 구현 방법에 관계없이 최종적으로 필요한 변수를 포함한 이미지 요청이 Adobe 데이터 수집 서버로 전송됩니다.

## Adobe Analytics 데이터 수집 서버로 전송되는 데이터

데이터가 Adobe Analytics로 전송되면 필요에 따라 다음과 같은 기능이 데이터를 조정합니다.

1. **조회 테이블**: Adobe 내부 조회 테이블에 의존하는 차원(예: [브라우저](/help/components/dimensions/browser.md) 차원)은 해당 값과 일치합니다.
2. [**동적 변수**](/help/implement/vars/page-vars/dynamic-variables.md): 이미지 요청의 어느 부분에서든 동적 변수가 표시되면 값이 복사되어 향후 독립적인 값으로 처리됩니다.
3. [**보트 규칙**](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md): 표준 또는 사용자 정의 보트 필터링을 적용하여 해당 데이터를 보고에서 제외합니다.
4. [**처리 규칙**](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md): 조직에서 데이터에 적용하는 사용자 정의 규칙. [컨텍스트 데이터 변수](/help/implement/vars/page-vars/contextdata.md)를 해당 변수에 매핑하는 기능을 포함합니다.
5. **VISTA 규칙**: Adobe 컨설턴트가 데이터에 적용하는 유연한 사용자 정의 규칙. VISTA 규칙은 조직의 필요에 따라 처리 규칙 이전 또는 이후에 실행될 수 있습니다. 대부분의 VISTA 규칙은 일반적으로 처리 규칙 이후에 실행되지만 각 조직은 다르게 설정됩니다. 기존 VISTA 규칙에 대한 자세한 내용은 Adobe 계정 관리자에게 문의하십시오.
6. [**마케팅 채널 처리 규칙**](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-rules.md): [처리 규칙](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md)을 사용하여 마케팅 채널 처리 규칙에 사용할 데이터를 준비할 수 있습니다.
7. **지리적 위치 데이터**: IP 주소 조회에 의존하는 차원(예: [국가](/help/components/dimensions/countries.md) 차원)이 채워집니다.
8. [**IP 난독화**](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md): 조직에서 원시 데이터의 IP 주소를 난독화하기로 선택한 경우, 다른 모든 처리 기능이 완료된 후에 수행됩니다.

이 시점에서 개별 히트는 보고서 세트 데이터 테이블에 기록됩니다. 표준 [지연](latency.md) 시간이 경과하면 보고에서 사용할 수 있습니다.

## 데이터 처리 후 변경

Adobe Analytics의 데이터는 대부분 영구적이지만 선택적으로 데이터를 조정하거나 삭제할 수 있는 몇 가지 기능이 있습니다.

* [**데이터 복구 API**](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/data-repair/): 특정 열을 편집하거나 원하는 데이터 행을 삭제합니다.
* [**데이터 거버넌스**](/help/technotes/c-data-governance/an-gdpr-workflow.md): 데이터를 영구적으로 삭제할 수 있도록 개인정보 보호 요청을 수용합니다.
* [**분류**](/help/components/classifications/c-classifications.md): 다양한 방식으로 데이터를 구성할 수 있는 규칙이나 업로드된 데이터를 기반으로 차원을 만듭니다. 기본 보고서 세트 데이터는 변경되지 않으므로 분류 데이터를 자유롭게 편집하거나 덮어쓸 수 있습니다.
* [**가상 보고서 세트**](/help/components/vrs/vrs-about.md): 방문 시간 초과를 변경하거나 [크로스 디바이스 분석](/help/components/cda/overview.md)을 허용할 수 있는 대체 보고서 세트 보기를 만듭니다.
