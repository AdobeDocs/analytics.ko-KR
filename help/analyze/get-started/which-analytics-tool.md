---
description: 이 도움말 페이지에서는 각 Adobe Analytics 도구에 대한 권장 사용 사례를 제공합니다. 도구는 나열된 순서대로 고려해야 합니다. 특정 도구가 요구 조건을 충족하지 못한다면 그 다음 도구를 사용해 볼 것을 고려해 보십시오.
title: 어떤 Adobe Analytics 도구를 사용해야 합니까?
feature: Analytics Basics
exl-id: d65575df-19c6-4129-89c8-d36de7bb6b2f
source-git-commit: a40f30bbe8fdbf98862c4c9a05341fb63962cdd1
workflow-type: tm+mt
source-wordcount: '1122'
ht-degree: 100%

---

# 어떤 Adobe Analytics 도구를 사용해야 합니까?

이 도움말 페이지에서는 각 Adobe Analytics 도구에 대한 권장 사용 사례를 제공합니다. 도구는 나열된 순서대로 고려해야 합니다. 특정 도구가 요구 조건을 충족하지 못한다면 그 다음 도구를 사용해 볼 것을 고려해 보십시오.

Adobe Analytics 제품 비교에 대한 자세한 내용은 [Analytics 제품 비교](/help/analyze/get-started/analytics-product-comparison.md)를 참조하십시오.


>[!BEGINSHADEBOX]

데모 비디오를 보려면 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [도구 비교](https://video.tv.adobe.com/v/27220?quality=12&learn=on){target="_blank"}를 확인하십시오.

>[!ENDSHADEBOX]


## Adobe Analytics 보고 사용자 인터페이스 {#user-interfaces}

**[Analysis Workspace](/help/analyze/analysis-workspace/home.md)**&#x200B;는 모든 보고 및 분석 요구를 위해 꼭 이용하는 사용자 인터페이스여야 합니다. Adobe는 이 제품에 대한 투자와 월별 업데이트 릴리스를 계속 수행합니다. Analysis Workspace에서 작업을 수행할 수 없는 경우 아래의 다른 인터페이스를 고려하십시오.**

**[Adobe Analytics 대시보드](/help/analyze/mobile-app/home.md)**&#x200B;를 통해 직관적인 스코어카드에 사용자가 모바일 액세스할 수 있습니다. 스코어카드는 더 자세한 분류 및 트렌드 보고서용으로 탭할 수 있는 타일식 레이아웃에 표시되는 주요 지표 및 기타 구성 요소의 컬렉션입니다. 모바일 앱은 iOS 및 Android 운영 체제에서 모두 지원됩니다.

**[Report Builder](/help/analyze/report-builder/rb-overview.md)**&#x200B;는 Mac, Windows 및 웹 브라우저에서 실행되는 Microsoft Excel용 추가 기능입니다. Adobe Analytics 데이터로 만들어진 맞춤화된 요청을 작성할 수 있고 이러한 요청은 Excel 워크시트에 삽입할 수 있습니다. 요청은 워크시트의 셀을 동적으로 참조할 수 있으며, Report Builder의 데이터 표시 방식을 업데이트하고 사용자 정의할 수 있습니다.

**[레거시 Report Builder](/help/analyze/legacy-report-builder/home.md)**&#x200B;는 Windows에서만 실행되는 Microsoft Excel용 추가 기능입니다. Adobe Analytics 데이터로 만들어진 맞춤화된 요청을 작성할 수 있고 이러한 요청은 Excel 워크시트에 삽입할 수 있습니다. 요청은 워크시트의 셀을 동적으로 참조할 수 있으며, Report Builder의 데이터 표시 방식을 업데이트하고 사용자 정의할 수 있습니다.

**[Activity Map](/help/analyze/activity-map/overview.md)**&#x200B;은 웹 페이지 및 모바일 앱에서의 사용자 참여를 시각적으로 표현하는 Adobe Analytics의 기능입니다. 이를 통해 마케팅 담당자와 분석가는 클릭, 호버링 및 스크롤 동작과 같은 사용자 상호 작용을 추적하고 분석할 수 있습니다.

## Adobe Analytics로 데이터 가져오기 {#import}

**[분류](/help/components/classifications/classifications-overview.md)**&#x200B;는 다음 경우에 사용합니다.

* eVar, Prop, 마케팅 채널 등의 수집 값에 연결하려는 메타데이터가 있는 경우. Adobe는 [분류 세트](/help/components/classifications/sets/overview.md)를 사용할 것을 권장합니다. 분류 규칙 빌더와 분류 가져오기 도구는 분류 데이터를 Adobe Analytics로 가져오기 위한 기존 방법입니다.

**[Data Sources](/help/import/data-sources/overview.md)**&#x200B;는 다음 경우에 사용합니다.

* Adobe Analytics에 영구적으로 작성하려는 오프라인 데이터가 있을 때
* 옵션:
   * 요약: 일별 또는 제한된 측정기준의 단순 데이터 업로드
   * 거래 ID: 온라인 엔드포인트를 오프라인 데이터에 연결하고 가져온 데이터를 온라인으로 캡처한 방문자 스냅숏에 완전히 연관시키는 데이터 업로드 (예: 온라인으로 주문하고 오프라인으로 반환)

**[Adobe Exchange 통합](https://www.adobeexchange.com/experiencecloud.html)**&#x200B;은 다음의 경우에 사용되어야 합니다.

* 지원되는 Adobe Analytics 연결을 구축한 서드파티 공급자와 일하는 경우. 통합 앱은 일반적으로 요약 수준 데이터를 Adobe Analytics에 영구적으로, 자동으로 그리고 반복적으로 통합합니다.

**[대량 데이터 삽입 API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md)**

* 대량 데이터 삽입 API는 한 행에 한 이벤트씩, 이벤트 데이터를 포함하는 CSV 형식의 파일을 수락합니다. Adobe는 서버측 코드가 필요하거나 AppMeasurement 또는 Web SDK를 사용하여 데이터를 수집할 수 없는 모든 구현에 대량 삽입 API를 사용할 것을 권장합니다.

**[데이터 삽입 API(레거시)](/help/import/c-data-insertion-api/c-data-insertion-api.md)**&#x200B;는 다음과 같은 경우에 사용합니다.

* Adobe Analytics로 데이터를 가져와야 하지만 AppMeasurement, Web SDK 또는 대량 데이터 삽입 API를 사용할 수 없는 경우.

**[고객 속성](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html)**&#x200B;은 다음 경우에 사용합니다.

* 고객 관계 관리 (CRM) 데이터베이스에서 기업 고객 데이터를 캡처하고, 이 데이터를 Experience Cloud에 업로드하려는 경우.
* CRM 데이터를 Analytics에서 더 자세한 분석에 사용하거나 Adobe Target에서 타기팅 기준으로 사용하려는 경우.

**[Audience Analytics](/help/integrate/c-audience-analytics/mc-audiences-aam.md)**&#x200B;는 다음 경우에 사용합니다.

* 인구 통계학적 정보(예: 성별 또는 수입 수준), 대상 데이터(예: 인구 통계 정보), 사이코그래픽 정보(예: 관심사 및 취미), CRM 데이터 또는 광고 노출 데이터와 같은 Adobe Audience Manager 대상자 데이터를 Analytics 워크플로에 통합하려는 경우.
* 이 통합에서는 새 정보를 조회수별로 Analytics에 전송하므로 업로드한 CRM 데이터를 시간 기반으로 변환하려는 경우.

## Adobe Analytics에서 데이터 내보내기 {#export}

**[Report Builder](/help/analyze/report-builder/rb-overview.md)**&#x200B;는 다음 경우에 사용합니다.

* 작업 영역의 사용자 정의 레이아웃 옵션이 제한적인 경우(Excel의 제한 이내에서 Report Builder로 모든 작업 가능).
* 사용자 입력 또는 오프라인 데이터 소스(노출 수, 비용)를 Adobe 데이터에 느슨하게 연결합니다. 영구적인 데이터 연결 솔루션은 데이터 소스입니다(Analytics로 데이터 가져오기 참조).
* 서로 다른 측정기준의 보고서의 데이터 병합(예: 프로모션 노출 수 보고서와 프로모션 클릭에서 전환 보고서 결합).
* 서로 다른 보고서 세트의 데이터를 합치거나 나란히 같은 테이블에 표시하여 병합합니다.
* 예약을 통한 자동화가 필요한 경우(XLSX, XLSM, CSV, PDF, TXT, XML, MHT).

**[Data Warehouse](/help/export/data-warehouse/data-warehouse.md)**&#x200B;는 다음 경우에 사용합니다.

* UI에 숨겨진 변수에 액세스 - IP 주소, Experience Cloud ID, Analytics 방문자 ID, 페이지 URL)
* UI보다 세부적인 데이터에 액세스 (비정규화된 테이블 보기)
* 피벗 테이블 입력에 적합한 형식으로 데이터 다운로드
* 클라이언트에서 Adobe 데이터를 서드파티 데이터 시각화 도구에 입력하려는 경우 (히트 수준은 아니며 약간 요약됨)
* Adobe Analytics에서 “낮은 트래픽”으로 실행 중인 경우 모든 고유 차원 항목에 액세스

**[Analytics 데이터 피드](/help/export/analytics-data-feed/c-df-contents/datafeeds-contents.md)**&#x200B;는 다음 경우에 사용합니다.

* 제공할 수 있는 가장 세부적인 데이터 피드 활용(방문자 ID, 히트).
* 클라이언트에서 클라이언트측 데이터베이스에 저장된 Adobe 데이터를 보낼 수 있는 가장 세부적인 수준으로 원하는 경우.
* 클라이언트에서 비즈니스 인텔리전스 (BI) 도구를 개발하거나 히트 수준의 Adobe 데이터를 서드파티 도구에 입력하려는 경우.

**[보고 API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/reporting-guide.md)**&#x200B;는 다른 시각화 옵션이 사용자의 요구를 충족하지 못할 때 사용해야 합니다. 다음은 API 옵션 세 가지입니다.

* **완전 처리**: 방문 수, 방문자 수 및 세그먼트 수 등 풍부한 데이터를 원하는 경우. 30~90분 이내에 사용할 수 있는 일반적인 Analytics UI 요약 데이터입니다. Report Builder를 통해 사용할 수 있습니다.
* **실시간**: 실제 상황보다 조금 지연된 상태로 몇 가지 지표 및 측정기준을 보려는 경우. 30초 이내에 사용할 수 있는 제한적이고 부분적으로 처리된 요약 데이터입니다. 가장 인기 있는 승자 및 패자의 고유한 알고리즘을 포함합니다. Report Builder를 통해 사용할 수 있습니다.
* **[!UICONTROL 라이브 스트리밍]**: 몇 초 간 수집한 데이터 내에서 부분적으로 처리된 히트 수준의 Analytics 데이터 스트림을 원하는 경우. 30초 이내에 사용할 수 있는 부분적으로 처리된 데이터입니다. Analytics Premium에서만 사용할 수 있습니다. 일반적으로 엔지니어링 서비스 계약을 통해 데이터를 시각화할 수 있는 방법이 필요합니다.

## 사용자 정의 솔루션 {#custom-solutions}

다음의 경우 엔지니어링 서비스가 필요합니다.

* 다른 Adobe 도구가 사용자의 요구를 충족하지 못합니다.
* 맞춤 경험을 원합니다.
* 완전히 자동화된 솔루션을 원합니다.
* 많은 디바이스에 연결하려고 합니다.
* 여러 데이터 소스가 있습니다.
* 복잡한 데이터 ETL (Extract-Transform-Load) 요구 사항이 있습니다.
* 맞춤 브랜딩을 원합니다.
* [!UICONTROL Analytics 라이브 스트림]을 시각화하려고 합니다.
