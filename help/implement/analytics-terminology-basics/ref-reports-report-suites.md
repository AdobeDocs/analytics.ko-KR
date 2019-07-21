---
description: 보고서 세트는 선택한 웹 사이트, 웹 사이트 집합 또는 웹 페이지의 하위 집합에 대한 전체적이고 독립적인 보고를 정의합니다. 일반적으로 보고서 세트는 하나의 웹 사이트지만 합계를 얻기 위해 여러 사이트의 번호를 결합한 글로벌 세그먼트가 될 수 있습니다. 마케팅 보고, 애드혹 분석, 및 리포트 빌더에 로그인할 때 사용할 보고서 세트를 하나 선택합니다(보고서 세트들을 결합하는 롤업을 사용할 때 제외).
keywords: Analytics 구현; 보고서; 보고서 세트; Analytics 보고서; 글로벌 세그먼트; 롤업; 롤업; 보고서 세트 결합; 트래픽; 전환; path
seo-description: 보고서 세트는 선택한 웹 사이트, 웹 사이트 집합 또는 웹 페이지의 하위 집합에 대한 전체적이고 독립적인 보고를 정의합니다. 일반적으로 보고서 세트는 하나의 웹 사이트지만 합계를 얻기 위해 여러 사이트의 번호를 결합한 글로벌 세그먼트가 될 수 있습니다. 마케팅 보고, 애드혹 분석, 및 리포트 빌더에 로그인할 때 사용할 보고서 세트를 하나 선택합니다(보고서 세트들을 결합하는 롤업을 사용할 때 제외).
seo-title: 보고서 및 보고서 세트
solution: Analytics
title: 보고서 및 보고서 세트
topic: 개발자 및 구현
uuid: 288203 F 6-CD 13-4 E 01-9950-2 C 7 E 5 CFB 8 A 17
translation-type: tm+mt
source-git-commit: 797eda5d8f9e9d4cba25f643e318a7be9c22a252

---


# 보고서 및 보고서 세트

보고서 세트는 선택한 웹 사이트, 웹 사이트 집합 또는 웹 페이지의 하위 집합에 대한 전체적이고 독립적인 보고를 정의합니다. 일반적으로 보고서 세트는 하나의 웹 사이트지만 합계를 얻기 위해 여러 사이트의 번호를 결합한 글로벌 세그먼트가 될 수 있습니다. 마케팅 보고, 애드혹 분석, 및 리포트 빌더에 로그인할 때 사용할 보고서 세트를 하나 선택합니다(보고서 세트들을 결합하는 롤업을 사용할 때 제외).

![](assets/how-data-is-collected-6.png)

보고서는 특정 매개 변수를 기반으로 Analytics에서 수집한 데이터에 대한 정보를 제공합니다.

Adobe Analytics를 구현한 후에 *Analytics 보고서*&#x200B;를 실행할 수 있습니다. 보고 기능을 통해 모바일, 비디오 및 소셜 네트워킹과 같이 계속 변화하는 채널을 물론 종래의 웹 기반 채널들에 대해서도 통찰력을 가질 수 있습니다. 마케팅 보고의 일부 예에는 다음과 같습니다.

* 사이트 방문자 수
* 해당 방문자 중 고유 방문자 수(한 번만 카운트)
* 방문자의 사이트 방문 경로(예: 링크를 따라 사이트를 방문했는지 또는 사이트에 직접 방문했는지 여부)
* 방문자가 사이트 컨텐츠를 검색하는 데 사용한 키워드
* 특정 페이지 또는 전체 사이트에서 머문 시간
* 방문자가 클릭한 링크와 사이트를 떠난 시점
* 매출 생성이나 전환 이벤트 생성에 가장 효과적인 마케팅 채널
* 비디오 보는 데 걸린 시간
* 방문자가 사이트를 방문하는 데 사용한 브라우저 및 장치

높은 수준의 보고서 유형은 다음과 같습니다.

* [트래픽:](https://marketing.adobe.com/resources/help/en_US/reference/reports_traffic.html) 방문자가 웹 사이트와 상호 작용하는 방법 및 사용자 지정된 트래픽 통계에 대한 심층적인 통찰력을 제공합니다.
* [변환:](https://marketing.adobe.com/resources/help/en_US/reference/reports_conversion.html) 사용자가 정의하는 성공 지표에 대한 정보를 표시합니다.
* [경로:](https://marketing.adobe.com/resources/help/en_US/reference/reports_paths.html) 방문자의 전체 탐색 경로를 추적하고 기록할 수 있습니다.

[Analysis Workspace](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/)를 사용하여 단일 Analytics 보고서의 일반적인 제한 사항을 제거할 수 있습니다. 사용자 지정 분석 프로젝트를 작성하기 위한 강력하고 유연한 캔버스를 제공합니다. 원하는 수의 데이터 테이블, 시각화 및 구성 요소(차원, 지표, 세그먼트 및 시간 세부기간)를 프로젝트에 드래그하여 놓으십시오. 즉시 분류 및 세그먼트를 만들고, 분석할 집단을 만들고, 경고를 만들고, 세그먼트를 만들고, 회사 동료와 공유할 보고서를 조정하십시오. 

<p class="head"> <b>참고 항목</b> </p>

* [Analysis Workspace 도움말](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/)
* [Reports and Analytics](https://marketing.adobe.com/resources/help/en_US/sc/user/) 도움말
* [실시간 보고서](https://marketing.adobe.com/resources/help/en_US/reference/realtime.html)
* [Adobe Report Builder](https://marketing.adobe.com/resources/help/en_US/arb/) 도움말
* [데이터 추출](https://marketing.adobe.com/resources/help/en_US/sc/user/data_extract.html)
* [Activity Map](https://marketing.adobe.com/resources/help/en_US/analytics/activitymap/)
* [보고서 세트 관리자](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)
* [Analytics 제품 비교 및 요구 사항](https://marketing.adobe.com/resources/help/en_US/reference/analytics-product-comparison.html)
* [보고서 설명](https://marketing.adobe.com/resources/help/en_US/reference/reports_descriptions.html)
* [대시보드 및 Reportlet](https://marketing.adobe.com/resources/help/en_US/sc/user/dashboard.html)
* [책갈피](https://marketing.adobe.com/resources/help/en_US/insight/client/c_bookmark_about.html)
* [가상 보고서 세트](https://marketing.adobe.com/resources/help/en_US/reference/virtual-report-suites.html)
* [예외 검색](https://marketing.adobe.com/resources/help/en_US/arb/anomaly_detection.html)
* [기여도 분석](https://marketing.adobe.com/resources/help/en_US/analytics/contribution/ca_main.html)

