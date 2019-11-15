---
description: 다양한 광고 추적 코드가 사이트의 여러 전환 이벤트에 미치는 영향을 측정합니다. 이 보고서를 사용하여 성공 이벤트에 대해 더 좋은 성과를 내는 특정 캠페인을 확인하거나, 가장 큰 매출을 생성하는 캠페인과 같이 사이트 이니셔티브에 도움 또는 방해가 되는 캠페인을 확인할 수 있습니다.
solution: Analytics
title: 추적 코드
topic: Reports
uuid: c893d592-10fd-4b40-84b3-8c8949a67b25
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 추적 코드

다양한 광고 추적 코드가 사이트의 여러 전환 이벤트에 미치는 영향을 측정합니다. 이 보고서를 사용하여 성공 이벤트에 대해 더 좋은 성과를 내는 특정 캠페인을 확인하거나, 가장 큰 매출을 생성하는 캠페인과 같이 사이트 이니셔티브에 도움 또는 방해가 되는 캠페인을 확인할 수 있습니다.

**일반 속성**

* 이 보고서는 웹 사이트에 구현된 [s.campaign](/help/implement/js-implementation/c-variables/page-variables.md) 변수에서 직접 데이터를 참조합니다.
* 이 보고서가 기반으로 하는 변수는 [전환 변수](/help/admin/admin/conversion-var-admin/conversion-var-admin.md)입니다. 즉, 페이지 보기를 넘어서까지 지속되며 지정된 기간 내의 지표와 연결됩니다.
* 보고서의 기본 지표는 매출입니다. [!UICONTROL 관리 도구]의 [!UICONTROL 보고서 세트 관리자]에서 이 기본값을 변경할 수 있습니다. ( **[!UICONTROL Edit Settings]** &gt; **[!UICONTROL Individual Report Settings]** &gt; **[!UICONTROL Default Metrics]**.)

* 이 보고서는 트렌드 및 등급 형식 모두로 볼 수 있습니다.
* 이 보고서에서 검색 필터를 사용하여 특정 라인 항목을 찾을 수 있습니다.
* [!UICONTROL 캠페인] 및 [!UICONTROL 크리에이티브 요소] 보고서는 이 보고서를 기반으로 한 분류이며 각 보고서 세트와 함께 자동으로 생성됩니다.

* 이 보고서에서 SAINT 분류를 사용하면 라인 항목을 통합하고 이름을 변경할 수 있습니다.
* 조직 및 보고서 세트 설정에 따라 이 보고서를 다음 보고서로 분류할 수 있습니다.

   * 방문당 체류 시간
   * 페이지 및 사이트 섹션 보고서, 모든 관련 분류 포함
   * 페이지 깊이, 시작 페이지 및 원래 시작 페이지
   * 대부분의 트래픽 소스 보고서
   * 방문 횟수 및 고객 충성도
   * 여러 방문자 프로필 및 기술 보고서, 지리 특성 제외
   * 모든 사용자 지정 전환 변수

* 이 보고서에서는 조직 및 보고서 세트 설정에 따라 다음 지표를 활용할 수 있습니다.

   * 클릭스루: *`s.campaign`* 변수가 정의된 횟수
   * 모든 표준 전자 상거래 지표: 매출, 주문, 판매량, 장바구니, 장바구니 보기, 체크아웃, 장바구니 추가, 장바구니 제거
   * 모든 사용자 지정 이벤트: 이벤트 1-80, H22 코드 이상인 경우는 이벤트 81-100도 포함
   * 방문 및 방문자: 조직 및 보고서 세트에 따라 사용 가능 여부가 결정됩니다. 자세한 내용은 계정 관리자에게 문의하십시오.

**Reports &amp; Analytics 속성**

* Click **[!UICONTROL Conversion]** &gt; **[!UICONTROL Campaigns]** &gt; **[!UICONTROL Tracking Code]** to locate this report, unless the menu is customized.

* 이 보고서는 모든 [목록 변수](https://marketing.adobe.com/resources/help/en_US/sc/implement/list_var.html)로도 분류할 수 있습니다.
* 페이지 보기, 방문, 및 고유 방문자를 지표로 사용할 수 있습니다.
* 이 보고서는 세그먼트를 사용할 수 있습니다.

**Ad Hoc Analysis 속성**

* 대부분의 기본 전환 변수 외에도, 보고 인터페이스 내의 다른 모든 보고서를 기준으로 추적 코드 보고서를 분류할 수 있습니다.
* 전자 상거래 및 사용자 지정 이벤트 외에도, 모든 전환 및 트래픽 지표와 모든 전환 지표에 대한 다른 할당을 사용할 수 있습니다.
* 이 보고서는 고급 세그먼트를 사용할 수 있습니다.

