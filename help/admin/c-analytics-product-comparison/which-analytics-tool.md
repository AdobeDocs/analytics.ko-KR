---
description: 이 도움말 페이지에는 각 Adobe Analytics 도구에 대한 권장 사용 사례가 포함되어 있습니다. 도구는 나열된 순서대로 고려해야 합니다. 특정 도구가 요구 사항에 맞지 않으면 다음 도구로 이동하여 고려하십시오.
title: 어떤 Adobe Analytics 도구를 사용해야 합니까?
uuid: 1179e49d-3cfc-4abd-a8eb-35c5ae380c16
translation-type: tm+mt
source-git-commit: f7125e6845a653ca3d4dd3f1313d1b39f564459c

---


# 어떤 Adobe Analytics 도구를 사용해야 합니까?

이 도움말 페이지에는 각 Adobe Analytics 도구에 대한 권장 사용 사례가 포함되어 있습니다. 도구는 나열된 순서대로 고려해야 합니다. 특정 도구가 요구 사항에 맞지 않으면 다음 도구로 이동하여 고려하십시오.

Adobe Analytics 제품 비교에 대한 자세한 내용은 [여기를](/help/admin/c-analytics-product-comparison/analytics-product-comparison.md)참조하십시오.

## Adobe Analytics 보고 사용자 인터페이스 {#section_8265460EBB47405AB19A3B2B0729C8A4}

**[Analysis Workspace](/help/analyze/analysis-workspace/analysis-workspace-features.md)**는 모든 보고 및 분석 요구를 위해 꼭 이용하는 사용자 인터페이스여야 합니다. Adobe는 이 제품에 대한 투자와 월별 업데이트 릴리스를 계속 수행합니다. Analysis Workspace에서 작업을 수행할 수 없는 경우 아래의 다른 인터페이스를 고려하십시오.**

**[Reports &amp; Analytics](/help/analyze/reports-analytics/overview/report-overview.md)**는 다음 경우에 사용해야 합니다.

* 쉽게 탐색할 수 있는 사전 빌드된 보고에 액세스해야 하는 초보 사용자가 사용해야 합니다.
* Target 활동(Target/A4T용 Analytics) 향상도 및 신뢰도를 파악하려면
* UI에서 실시간 데이터에 액세스하려면
* 달력 이벤트를 설정하려면
* 대상을 설정하려면
* 보트 보고를 보려면
* 동시 뷰어, 비디오 시간 파트 및 뷰어 드롭다운의 고유한 비디오 시각화에 액세스하려면
* 예약된 보고에서 게시 목록을 활용하려면

**[Mobile Services UI](https://docs.adobe.com/content/help/en/mobile-services/using/home.html)**는 다음 경우에 사용해야 합니다.

* 모바일 앱 데이터의 격리된 보기가 필요한 경우
* 모바일 앱 SDK의 구현을 관리합니다.
* 인앱 메시지, 푸시 메시지 및 위치 타깃팅과 같은 모바일 광고를 설정하려면
* 앱 데이터(선버스트)에 대해 더 많은 대화형 시각화가 필요한 경우.
* 지도에서 관심 영역을 시각화하려면
* 라이프타임 값 지표의 경우.

**[Ad Hoc Analysis](/help/analyze/ad-hoc-analysis/adhoc-home.md)**는 다음 경우에 사용해야 합니다.

* 50,000개의 데이터 행을 내보내려면
* 프로젝트 작업의 탭 구성을 원하는 경우
* 사이트 분석 보고서(3D 경로 지정 보고서)를 사용하려면

**[Data Workbench](https://docs.adobe.com/content/help/en/data-workbench/using/home.html)**는 다음 경우에 사용합니다.

* 가장 유연한 Analytics 도구 옵션(방문자 수준, 히트 수준 분석까지)입니다.
* CRM에서 POS에서 웹에 이르는 온라인 및 오프라인 상호 작용의 다중 채널 데이터 세트를 만들려면
* 고급 속성(규칙 기반 및 알고리즘 모델)의 경우
* 예측, 통계 모델링(성향 점수, 클러스터링, 상관 관계 등)의 경우
* 지연 분석의 경우(이벤트 전/이후 시간).
* Adobe Experience Cloud에서 복잡한 세그먼트를 식별하고 내보낼 수 있습니다.

## Adobe Analytics로 데이터 가져오기 {#section_B42B998D6E3E4357B024AEFA4EC69A23}

**[분류](/help/components/c-classifications2/c-classifications.md)**는 다음 경우에 사용합니다.

* 수집 값(eVar, prop, 마케팅 채널)에 연결할 메타데이터가 있는 경우
* 옵션:

   * 규칙 빌더:변수(예: 구분된 값)에 대해 수집되는 예측 가능한 형식 값이 있을 때 사용합니다. 이 방법을 사용하면 규칙을 한 번 설정해 두면 대부분 &quot;설정 및 삭제&quot;할 수 있습니다.
   * 브라우저 가져오기: 예측 가능한 값이 없거나 일회성 업데이트가 필요한 유한 값 목록이 있는 경우에 사용합니다. 이 방법에서는 새 값에 대한 분류를 지속적으로 모니터링해야 합니다.

**[데이터 소스](/help/import/c-data-sources/datasrc-home.md)**는 다음 경우에 사용해야 합니다.

* Adobe Analytics에 영구적으로 작성하려는 오프라인 데이터가 있을 때
* 옵션:

   * 요약:일 또는 제한된 차원별 단순 데이터 업로드
   * 거래 ID:온라인 끝점을 오프라인 데이터에 연결하고 가져온 데이터를 온라인으로 캡처한 방문자 스냅샷에 완전히 연결하는 데이터 업로드(예: 온라인으로 완료 주문 및 오프라인으로 반환)
   * 전체 처리:타임스탬프가 있는 데이터 소스. Adobe 서버에서 수집한 히트처럼 처리됩니다. 즉, 데이터는 방문자 여정에 직접 삽입됩니다.

**[Data Connectors](https://www.adobeexchange.com/experiencecloud.html)(이전의 Genesis)**는 다음 경우에 사용해야 합니다.

* Adobe Analytics와 지원되는 연결을 빌드한 타사 제공업체를 이용하는 경우 데이터 커넥터는 일반적으로 요약 수준 데이터를 Adobe Analytics에 영구적으로 자동으로 반복해서 통합합니다.

**[Data Insertion API](https://marketing.adobe.com/developer/documentation/data-insertion/c-data-insertion-api)**는 다음 경우에 사용해야 합니다.

* 데이터를 Adobe Analytics에 업로드해야 할 때 사용해야 하며, Adobe AppMeasurement나 모바일 SDK 코드는 사용할 수 없습니다.

**[사용자 특성](/help/components/c-variables/dimensionslist/reports-customer-attributes.md)**은 다음 경우에 사용합니다.

* 고객 관계 관리(CRM) 데이터베이스에서 기업 고객 데이터를 캡처하고 Experience Cloud에 데이터를 업로드하려는 경우.
* Analytics의 심층적인 분석을 위해 또는 Adobe Target의 타깃팅 기준으로 CRM 데이터를 사용하려는 경우

**[Audience Analytics](/help/integrate/c-audience-analytics/mc-audiences-aam.md)**는 다음 경우에 사용해야 합니다.

* 인구 통계 정보(예: 성별 또는 소득 수준), 심리통계적 정보(예: 관심사 및 취미), CRM 데이터 또는 광고 노출 데이터 등의 Adobe Audience Manager(AAM) 대상 데이터를 Analytics 워크플로우에 통합하려는 경우
* 업로드된 CRM 데이터를 시간 기반으로 하려는 경우 이 통합은 히트로 인해 Analytics에 새 정보를 보내기 때문입니다.

## Adobe Analytics에서 데이터 내보내기 {#section_901C06ABF2014E92B2952906723DF235}

**[Report Builder](/help/analyze/report-builder/home.md)**는 다음 경우에 사용해야 합니다.

* Workspace의 사용자 지정 레이아웃 옵션이 제한되는 경우(Excel의 제한 범위 내에서 Report Builder에서 가능한 모든 것).
* 사용자 입력 또는 오프라인 데이터 소스(노출 수, 비용)를 Adobe 데이터에 느슨하게 연결합니다. 영구적인 데이터 연결 솔루션은 데이터 소스입니다(Analytics로 데이터 가져오기 참조).
* 여러 차원 보고서의 데이터를 병합하려면(예: 프로모션 클릭에서 전환 보고서로 연결된 프로모션 노출 수 보고서)
* 보고서 세트 간 보기의 경우
* 예약을 통한 자동화가 필요한 경우(XLSX, XLSM, CSV, PDF, TXT, XML, MHT)

**[Data Warehouse](/help/export/data-warehouse/data-warehouse.md)**는 다음 경우에 사용해야 합니다.

* UI에 숨겨진 변수에 액세스 - IP 주소, Experience Cloud ID, Analytics 방문자 ID, 페이지 URL)
* UI보다 더 세분화된 데이터에 액세스하려면(비정규화된 테이블 보기)
* 피벗 테이블 입력에 적합한 형식으로 데이터를 다운로드하려면
* 클라이언트가 Adobe 데이터를 타사 데이터 시각화 도구에 입력하려는 경우(히트 수준이 아니라 약간 요약됨)
* Adobe Analytics에서 &quot;낮은 트래픽&quot;으로 실행 중인 경우 모든 고유 차원 값에 액세스

**[Analytics 데이터 피드](/help/export/analytics-data-feed/c-df-contents/datafeeds-contents.md)**는 다음 경우에 사용해야 합니다.

* 제공할 수 있는 가장 세부적인 데이터 피드(방문자 ID, 히트)를 활용합니다.
* 클라이언트가 Adobe 데이터를 클라이언트 측 데이터베이스에 저장하기를 원하는 경우 전송할 수 있는 가장 세부적인 수준으로 저장할 수 있습니다.
* 클라이언트가 BI(Business Intelligence) 도구를 개발하거나 히트 수준 Adobe 데이터를 타사 도구에 입력하려는 경우

**[보고 API](https://marketing.adobe.com/developer/get-started/introduction/c-introduction)**는 다른 시각화 옵션이 사용자의 요구를 충족하지 못할 때 사용해야 합니다. 3가지 API 옵션은 다음과 같습니다.

* **완전히 처리됨**:기능을 갖춘 데이터(방문, 방문자 및 세그먼트 포함)를 원할 때 이는 30-90분 이내에 사용할 수 있는 일반적인 Analytics UI의 요약 데이터입니다. 리포트 빌더를 통해 사용할 수 있습니다.
* **실시간**:몇 개의 지표 및 차원을 몇 초 지연으로 보려는 경우. 이것은 30초 이내에 사용할 수 있는 제한적이고 부분적으로 처리된 요약된 데이터입니다. 가장 인기 있는 승자 및 패자의 고유한 알고리즘을 포함합니다. 리포트 빌더를 통해 사용할 수 있습니다.
* **[!UICONTROL Live Stream]**:부분적으로 처리된 히트 수준 Analytics 데이터 스트림을 수집 후 몇 초 내에 원하는 경우 이것은 30초 이내에 사용 가능한 부분적으로 처리된 데이터입니다. Analytics Premium에서만 사용할 수 있습니다. 일반적으로 엔지니어링 서비스 참여를 통해 데이터를 시각화하는 방법이 필요합니다.

## 맞춤 솔루션 {#section_4A212F26A15947599DFB0399A0440CB6}

다음의 경우 엔지니어링 서비스가 필요합니다.

* 다른 Adobe 도구가 사용자의 요구를 충족하지 못합니다.
* 사용자 정의 경험을 원합니다.
* 자동화된 솔루션을 원하는 경우
* 많은 디바이스에 도달해야 합니다.
* 여러 데이터 소스가 있습니다.
* 복잡한 데이터 ETL(Extract-Transform-Load) 요구 사항이 있습니다.
* 맞춤형 브랜딩을 원합니다.
* 시각화하고 [!UICONTROL Analytics Live Stream]싶겠죠
