---
description: 이 도움말 페이지에서는 각 Adobe Analytics 도구에 대한 권장 사용 사례를 제공합니다. 도구는 나열된 순서대로 고려해야 합니다. 특정 도구가 필요를 충족하지 못하면 다음 도구로 이동하여 고려하십시오.
title: 어떤 Adobe Analytics 도구를 사용해야 합니까?
uuid: 1179e49d-3cfc-4abd-a8eb-35c5ae380c16
translation-type: tm+mt
source-git-commit: 8e8eb2c7787f97104c983cc4b0f11e5ed57de069
workflow-type: tm+mt
source-wordcount: '1093'
ht-degree: 100%

---


# 어떤 Adobe Analytics 도구를 사용해야 합니까?

이 도움말 페이지에서는 각 Adobe Analytics 도구에 대한 권장 사용 사례를 제공합니다. 도구는 나열된 순서대로 고려해야 합니다. 특정 도구가 필요를 충족하지 못하면 다음 도구로 이동하여 고려하십시오.

Adobe Analytics 제품 비교에 대해 자세히 알아보려면 [여기](/help/admin/c-analytics-product-comparison/analytics-product-comparison.md)에서 확인하십시오.

## Adobe Analytics 보고 사용자 인터페이스 {#section_8265460EBB47405AB19A3B2B0729C8A4}

**[Analysis Workspace](/help/analyze/analysis-workspace/home.md)**는 모든 보고 및 분석 요구를 위해 꼭 이용하는 사용자 인터페이스여야 합니다. Adobe는 이 제품에 대한 투자와 월별 업데이트 릴리스를 계속 수행합니다. Analysis Workspace에서 작업을 수행할 수 없는 경우 아래의 다른 인터페이스를 고려하십시오.**

**[Reports &amp; Analytics](/help/analyze/reports-analytics/overview/report-overview.md)**는 다음 경우에 사용해야 합니다.

* 쉽게 탐색할 수 있는 사전 빌드된 보고에 액세스해야 하는 초보 사용자가 사용해야 합니다.
* UI에서 실시간 데이터에 액세스하려는 경우
* 달력 이벤트를 설정하려는 경우
* 대상을 설정하려는 경우
* 보트 보고를 보려는 경우
* Concurrent Viewer, Video Daypart 및 Viewer Drop-off의 고유한 비디오 시각화에 액세스하려는 경우
* 예약된 보고에서 게시 목록을 활용하려는 경우

**[Ad Hoc Analysis](/help/analyze/ad-hoc-analysis/adhoc-home.md)**는 다음 경우에 사용해야 합니다.

* 50,000행의 데이터 내보내기
* 프로젝트 작업의 탭 구성이 필요한 경우.
* 사이트 분석 보고서를 사용해야 하는 경우(3D 경로 지정 보고서).

**[Data Workbench](https://docs.adobe.com/content/help/en/data-workbench/using/home.html)**는 다음 경우에 사용합니다.

* 가장 유연한 Analytics 도구 옵션(방문자 수준, 히트 수준 분석까지).
* CRM에서 POS 웹에 이르는 온라인 및 오프라인 상호 작용의 다중 채널 데이터 세트 생성.
* 고급 속성(규칙 기반 및 알고리즘 모델).
* 예측, 통계 모델링(성향 점수, 클러스터링, 상관 관계 등).
* 지연 분석(이벤트 전/후 시간).
* Adobe Experience Cloud에서 복잡한 세그먼트를 식별 및 내보내기.

## Adobe Analytics로 데이터 가져오기 {#section_B42B998D6E3E4357B024AEFA4EC69A23}

**[분류](/help/components/c-classifications2/c-classifications.md)**는 다음 경우에 사용합니다.

* eVar, Prop, 마케팅 채널 등의 수집 값에 연결하려는 메타데이터가 있는 경우
* 옵션:

   * 규칙 빌더: 구분된 값과 같이 예측 가능한 형식으로 된 값의 변수를 수집할 때 사용합니다. 이 방법을 통해 규칙을 한 번 설정하면 대부분 &quot;설정해 놓고 잊어도 됩니다&quot;.
   * 브라우저 가져오기: 예측 가능한 값이 없거나 일회성 업데이트가 필요한 유한 값 목록이 있는 경우에 사용합니다. 이 방법에서는 새 값에 대한 분류를 지속적으로 모니터링해야 합니다.

**[데이터 소스](/help/import/c-data-sources/datasrc-home.md)**는 다음 경우에 사용해야 합니다.

* Adobe Analytics에 영구적으로 작성하려는 오프라인 데이터가 있을 때
* 옵션:

   * 요약: 일별 또는 제한된 측정기준의 단순 데이터 업로드
   * 거래 ID: 온라인 종단점을 오프라인 데이터에 연결하고 가져온 데이터를 온라인으로 캡처한 방문자 스냅숏에 완전히 연관시키는 데이터 업로드(예: 온라인으로 주문하고 오프라인으로 반환)
   * 전체 처리: Adobe 서버에서 수집한 히트처럼 처리되었으며 타임스탬프가 있는 데이터 소스입니다. 즉, 데이터가 방문자 움직임에 직접 삽입됩니다.

**[Data Connectors](https://www.adobeexchange.com/experiencecloud.html)(이전의 Genesis)**는 다음 경우에 사용해야 합니다.

* 지원되는 Adobe Analytics 연결을 구축한 타사 공급자와 일하는 경우. Data Connectors는 일반적으로 요약 수준 데이터를 Adobe Analytics에 영구적으로, 자동으로 그리고 반복적으로 통합합니다.

**[Data Insertion API](/help/import/c-data-insertion-api/c-data-insertion-api.md)**는 다음 경우에 사용해야 합니다.

* 데이터를 Adobe Analytics에 업로드해야 할 때 사용해야 하며, Adobe AppMeasurement나 모바일 SDK 코드는 사용할 수 없습니다.

**[사용자 특성](/help/components/c-variables/dimensionslist/reports-customer-attributes.md)**은 다음 경우에 사용합니다.

* 고객 관계 관리(CRM) 데이터베이스에서 기업 고객 데이터를 캡처하고, 이 데이터를 Experience Cloud에 업로드하려는 경우.
* CRM 데이터를 Analytics에서 더 자세한 분석에 사용하거나 Adobe Target에서 타깃팅 기준으로 사용하려는 경우.

**[Audience Analytics](/help/integrate/c-audience-analytics/mc-audiences-aam.md)**는 다음 경우에 사용해야 합니다.

* 인구 통계학적 정보(예: 성별 또는 수입 수준), 대상 데이터(예: 인구 통계 정보), 사이코그래프 정보(예: 관심사 및 취미), CRM 데이터 또는 광고 노출 데이터와 같은 Adobe Audience Manager(AAM) 대상 데이터를 Analytics 워크플로우에 통합하려는 경우.
* 이 통합에서는 새 정보를 조회수별로 Analytics에 전송하므로 업로드한 CRM 데이터를 시간 기반으로 변환하려는 경우.

## Adobe Analytics에서 데이터 내보내기 {#section_901C06ABF2014E92B2952906723DF235}

**[Report Builder](/help/analyze/report-builder/home.md)**는 다음 경우에 사용해야 합니다.

* Workspace의 사용자 정의 레이아웃 옵션이 제한적인 경우(Excel의 제한 이내에서 Report Builder로 모든 작업 가능).
* 사용자 입력 또는 오프라인 데이터 소스(노출 수, 비용)를 Adobe 데이터에 느슨하게 연결합니다. 영구적인 데이터 연결 솔루션은 데이터 소스입니다(Analytics로 데이터 가져오기 참조).
* 서로 다른 측정기준의 보고서의 데이터 병합(예: 프로모션 노출 수 보고서와 프로모션 클릭에서 전환 보고서 결합).
* 교차 보고서 세트 보기.
* 예약을 통한 자동화가 필요한 경우(XLSX, XLSM, CSV, PDF, TXT, XML, MHT).

**[Data Warehouse](/help/export/data-warehouse/data-warehouse.md)**는 다음 경우에 사용해야 합니다.

* UI에 숨겨진 변수에 액세스 - IP 주소, Experience Cloud ID, Analytics 방문자 ID, 페이지 URL)
* UI보다 세부적인 데이터에 액세스(비정규화된 표보기)
* 피벗 테이블 입력에 적합한 형식으로 데이터 다운로드
* 클라이언트에서 Adobe 데이터를 타사 데이터 시각화 도구에 입력하려는 경우(히트 수준은 아니며 약간 요약됨)
* Adobe Analytics에서 &quot;낮은 트래픽&quot;으로 실행 중인 경우 모든 고유 차원 값에 액세스

**[Analytics 데이터 피드](/help/export/analytics-data-feed/c-df-contents/datafeeds-contents.md)**는 다음 경우에 사용해야 합니다.

* 제공할 수 있는 가장 세부적인 데이터 피드 활용(방문자 ID, 히트).
* 클라이언트에서 클라이언트 측 데이터베이스에 저장된 Adobe 데이터를 보낼 수 있는 가장 세부적인 수준으로 원하는 경우.
* 클라이언트에서 비즈니스 인텔리전스(BI) 도구를 개발하거나 히트 수준의 Adobe 데이터를 타사 도구에 입력하려는 경우.

**[보고 API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/reporting-guide.md)**는 다른 시각화 옵션이 사용자의 요구를 충족하지 못할 때 사용해야 합니다. 다음은 API 옵션 세 가지입니다.

* **완전 처리**: 방문 수, 방문자 수 및 세그먼트 수 등 풍부한 데이터를 원하는 경우. 30~90분 이내에 사용할 수 있는 일반적인 Analytics UI 요약 데이터입니다. Report Builder를 통해 사용할 수 있습니다.
* **실시간**: 실제 상황보다 조금 지연된 상태로 몇 가지 지표 및 측정기준을 보려는 경우. 30초 이내에 사용할 수 있는 제한적이고 부분적으로 처리된 요약 데이터입니다. 가장 인기 있는 승자 및 패자의 고유한 알고리즘을 포함합니다. Report Builder를 통해 사용할 수 있습니다.
* **[!UICONTROL 라이브 스트리밍]**: 몇 초 간 수집한 데이터 내에서 부분적으로 처리된 히트 수준의 Analytics 데이터 스트림을 원하는 경우. 30초 이내에 사용할 수 있는 부분적으로 처리된 데이터입니다. Analytics Premium에서만 사용할 수 있습니다. 일반적으로 엔지니어링 서비스 계약을 통해 데이터를 시각화할 수 있는 방법이 필요합니다.

## 맞춤 솔루션 {#section_4A212F26A15947599DFB0399A0440CB6}

다음의 경우 엔지니어링 서비스가 필요합니다.

* 다른 Adobe 도구가 사용자의 요구를 충족하지 못합니다.
* 맞춤 경험을 원합니다.
* 완전히 자동화된 솔루션을 원합니다.
* 많은 장치에 연결하려고 합니다.
* 여러 데이터 소스가 있습니다.
* 복잡한 데이터 ETL(Extract-Transform-Load) 요구 사항이 있습니다.
* 맞춤 브랜딩을 원합니다.
* [!UICONTROL Analytics 라이브 스트림]을 시각화하려고 합니다.
