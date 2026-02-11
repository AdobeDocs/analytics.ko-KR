---
title: 현재 Adobe Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: dabcb339238813b1da605a62f9a70599fbcef1bf
workflow-type: tm+mt
source-wordcount: '1436'
ht-degree: 45%

---

# 현재 Adobe Analytics 릴리스 정보 (2026년 2월)

**마지막 업데이트**: 2026년 2월 11일 목요일

이 릴리스 정보는 2026년 2월 릴리스 기간을 다룹니다. Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이러한 릴리스 노트는 한 달에 여러 번 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 새로운 기능 또는 개선 사항 {#features}

| 기능 및 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ---- |
| **개선된 데이터 피드** <p>이제 데이터 피드에 다음과 같은 개선 사항을 사용할 수 있습니다.</p><ul><li>사용자 경험이 개선되었습니다.</li><li>열 템플릿을 만들고 관리할 수 있는 새로운 환경.</li><li>이제 향후 데이터 피드에서 재사용할 열 템플릿을 만들 시기를 선택할 수 있습니다. 템플릿을 삭제, 편집 및 복사할 수도 있습니다.<br/>이전에는 만들어진 각 데이터 피드에 새 열 템플릿이 추가되어 사용하지 않는 열 템플릿이 대량으로 나타나며 삭제하거나 관리할 방법이 없었습니다.</li><li>태그를 기준으로 추가 및 필터링합니다.</li><li>데이터 피드 작업 내역 보기 (요청 기간이 시작되고, 시작되고, 완료되는 등의 시간.)</li><li>데이터 피드를 다시 보내거나 다시 처리합니다. (작업 내역 페이지에서)</li><li>늦게 도착하는 히트를 허용합니다. 이제 데이터 피드 작업이 설정된 보고 빈도 내에서 데이터 처리를 완료한 후에 도착하는 데이터를 포함할 수 있습니다.</li><li>데이터 피드에 대한 종료 날짜를 선택할 때 선택한 종료 날짜가 데이터 피드의 마지막 날로 포함됩니다.<br/>이전에는 데이터 피드에서 종료 날짜가 제외되었습니다.</li><li>이제 15분 내보내기 빈도가 가능하지만 기본적으로 사용할 수 없습니다. 이 옵션을 사용자 환경에서 사용하려면 먼저 Adobe 고객 지원 센터에 문의하여 보고서 세트가 15분 내보내기를 지원하도록 구성되었는지 요청해야 합니다.</li></ul><p>**참고:** 이러한 개선 사항으로 Adobe Analytics의 데이터 피드 페이지에 대한 URL도 업데이트됩니다. 2026년 4월 30일까지 새 데이터 피드 페이지를 가리키도록 기존 책갈피를 업데이트하십시오.</p><p>자세한 내용은 [데이터 피드 만들기](/help/export/analytics-data-feed/create-feed.md) 및 [데이터 피드 관리](/help/export/analytics-data-feed/df-manage-feeds.md)를 참조하십시오.</p> | 2026년 1월 20일 수요일 | 2026년 2월 24일 수요일<p>(원래 2026년 2월 10일 수요일 릴리스로 계획됨)</p> |
| **여러 열을 기준으로 테이블 정렬** <p>이제 Analysis Workspace에서 자유 형식 테이블의 데이터를 차원 또는 지표와 관계없이 여러 열을 기준으로 정렬할 수 있습니다.</p><p>여러 열에 대해 데이터를 정렬할 때 데이터는 각 열에 할당한 우선순위에 따라 정렬됩니다. 우선순위 번호는 정렬 아이콘 옆에 표시됩니다.</p><p>자세한 내용은 [자유 형식 테이블 필터링 및 정렬](/help/analyze/analysis-workspace/visualizations/freeform-table/filter-and-sort.md)을 참조하십시오.</p> | 2026년 1월 28일 | 2026년 2월 18일 |
| **근사 고유 개수 함수 업데이트**<p>근사 고유 개수 함수에서 사용되는 HLL 확률적 알고리즘은 곧 업데이트될 것이다. 이 함수를 사용하는 숫자에 대한 결과 출력은 다음과 같이 과거 숫자에서 약간 변경될 수 있습니다.</p><ul><li>매우 적은 양의 고유 값을 계산할 때 추정치를 사용하지 않고 정확한 개수를 사용하도록 결과가 개선됩니다.</li><li>더 큰 값을 계산할 때 예상 횟수는 이 업데이트 전과 동일한 정확도를 유지합니다(예상 횟수는 정확한 횟수의 5%, 시간의 95% 내에서 정확함).</li></ul><p>근사 고유 개수 함수에 대한 자세한 내용은 [고급 함수](/help/components/calculated-metrics/cm-reference/cm-adv-functions.md#approximate-count-distinct)에서 [근사 고유 개수](/help/components/calculated-metrics/cm-reference/cm-adv-functions.md)를 참조하십시오.</p> |  | 2026년 3월 |
| **스트리밍 미디어 서비스: 일정 데이터 지원** <p>이제 과거 라이브 스트리밍 미디어 콘텐츠의 예약된 데이터를 업로드하여 시청자 수를 보다 쉽고 정확하게 추적할 수 있습니다.</p><p>다음은 일정 데이터 업로드가 지원되는 라이브 콘텐츠의 예입니다.</p><ul><li>FAST(무료 광고 지원 TV) 플랫폼</li><li>로컬 스트림</li><li>라이브 스포츠</li></ul><p>일정 데이터를 업로드하면 업로드 파일에서 지정한 시간 동안 실행된 개별 프로그램의 시청자 수 데이터를 추적할 수 있습니다. 특정 주제나 프로그램 세그먼트에 대한 시청자 수 데이터를 수집할 수도 있습니다.</p><p>이러한 기능은 스트리밍 미디어 컬렉션을 어떻게 구현하든 관계없이 사용할 수 있습니다.</p><p>이전에는 라이브 콘텐츠를 분석할 때 주어진 세션을 특정 프로그램에 정확하게 연결하는 것이 어려웠고, 주어진 세션을 개별 주제나 프로그램 세그먼트에 연결하는 것도 불가능했습니다.</p><p>자세한 내용은 [라이브 콘텐츠를 추적할 일정 데이터 업로드](https://experienceleague.adobe.com/ko/docs/media-analytics/using/media-use-cases/track-schedule-data)를 참조하십시오.</p> | 2025년 10월 29일 | 2026년 상반기<p>(원래 2025년 10월 29일 릴리스로 계획됨)</p> |
| **새 Adobe Analytics 2.0 보고서 세트 API 안내서** <p>보고서 세트 API를 만들고, 검색하고, 업데이트하고, 삭제합니다. 자세한 내용은 [Adobe Analytics 2.0 보고서 세트 API 참조 안내서](https://developer.adobe.com/analytics-apis/docs/2.0/apis/report-suites/) 및 [Adobe Analytics 2.0 보고서 세트 API 끝점 안내서](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/report-suites/)를 참조하십시오.</p> | | 지금 사용 가능 |
| **새 Adobe Analytics 2.0 API 예외 항목 탐지 보고서 가이드** <p>자동화된 API 예외 항목 탐지 보고서를 만듭니다. 자세한 내용은 [예외 항목 탐지 API 보고서 끝점 안내서](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/reports/anomaly/)를 참조하십시오.</p> | | 지금 사용 가능 |
| **새 Adobe Analytics 2.0 API 기본 날짜 트렌드 보고서 가이드** <p>자동화된 API 기본 날짜 트렌드 KPI 보고서 만들기 자세한 내용은 [예외 항목 탐지 API 보고서 끝점 안내서](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/reports/kpi/)를 참조하십시오.</p> | | 지금 사용 가능 |

## Adobe Analytics의 수정 사항

**Activity Map**:
**Analysis Workspace**: AN-424997, AN-424194, AN-425515, AN-423174, AN-425207, AN-428834, AN-306540, AN-426014, AN-427801
**분류**: AN-422723, AN-424467, AN-423724, AN-424003, AN-425217, AN-396062, AN-422744, AN-425456, AN-425271, AN-425655, AN-424894, AN-429236
**데이터 피드 및 Data Warehouse**: AN-427082, AN-405154, AN-406512, AN-423594, AN-425283, AN-425208, AN-422510, AN-421189, AN-428986, AN-426724, AN-401525, AN-426884, AN-425146
**마이그레이션**: AN-421192, AN-423443
**개인 정보**:
**Report Builder**: AN-391415, AN-425125
**보고**: AN-422123, AN-425817, AN-421097, AN-422249, AN-403446, AN-424727, AN-426791, AN-427985
**예약된 보고서**: AN-425484, AN-425137
**세그먼테이션**: AN-428905, AN-428232
**기타**: AN-425054, AN-420190, AN-422248


## 서비스 종료(EOL) 알림 {#eol}

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **실시간 스트리밍 처리 개선 사항** | 2026년 1월 14일 목요일 | Adobe은 라이브 스트림 페이로드의 형식을 개선하고 변경할 계획입니다. 이러한 업데이트는 LiveStream과 Analysis Workspace과 같은 다른 Adobe Analytics 기능 간의 패리티를 향상합니다. 계획된 변경 사항을 테스트할 수 있는 미리보기 엔드포인트를 사용할 수 있습니다. 변경 사항의 전체 목록 및 미리 보기 끝점 세부 정보는 [LiveStream 릴리스 정보](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/livestream/release-notes/)를 참조하십시오. Adobe은 2026년 4월 13일에 업데이트된 페이로드 포맷으로 하드 컷오버를 계획합니다. |
| **TLS 1.2 암호 그룹 제거** | 2026년 2월 11일 목요일 | 관리자에게 알림: Adobe은 2026년 5월 27일에 Adobe 데이터 수집 서버에서 다음 TLS 1.2 암호 세트에 대한 지원을 중단할 예정입니다.<ul><li>`TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA`</li><li>`TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA`</li><li>`TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA`</li><li>`TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA`</li><li>`TLS_RSA_WITH_AES_128_CBC_SHA`</li><li>`TLS_RSA_WITH_AES_256_CBC_SHA`</li></ul><p>대부분의 구현에 고객 작업이 필요하지 않습니다. 이 변경 사항은 주로 오래된 TLS 라이브러리를 사용하는 이전 기본 애플리케이션에서 전송된 Analytics 데이터와 오래된 브라우저나 운영 체제에서 적은 수의 웹 방문자에게 영향을 줍니다. 이러한 암호 세트에 대한 지원을 제거하면 보안이 강화되고 Adobe이 최신 암호화 표준에 맞게 조정됩니다. 현재 데이터 수집 트래픽의 0.1% 미만이 이러한 암호 세트에 의존합니다.</p> |
| **레거시 Report Builder** | 2025년 6월 18일 | 기존 Report Builder 추가 기능은 2026년 6월에 지원이 중단됩니다. 모든 사용자는 기존 통합 문서를 새로운 [Report Builder](/help/analyze/report-builder/rb-overview.md)로 업그레이드해야 합니다. 새로운 Report Builder는 Adobe Analytics와 Customer Journey Analytics 고객 모두에게 제공됩니다. 이는 [거의 동일한 기능](/help/analyze/report-builder/convert-workbooks.md#unsupported)과 더불어 여러 가지 편리하고 새로운 기능과 개선된 UI를 제공합니다. 업그레이드 프로세스를 용이하게 하기 위해 새로운 Report Builder에는 간편한 통합 문서 변환 기능이 포함되어 있습니다. 새로운 Report Builder는 Microsoft Store를 통해 다운로드할 수 있는 추가 기능으로만 제공됩니다. 대부분의 조직에서는 사용자에게 추가 기능을 제공하기 전에 내부 승인 절차를 거쳐야 합니다. 이 프로세스에 시간을 할애하고 지금부터 조직과 협력하여 EOL 날짜 전에 통합 문서를 업그레이드할 충분한 시간을 확보하십시오. |
| **레거시 도메인 또는 레거시 SSO를 통한 액세스** | 2025년 4월 10일 금요일 | Adobe는 보안을 강화하고 로그인 환경을 간소화하기 위해 사용자가 Adobe Analytics에 액세스하는 방식을 업데이트할 계획입니다. 이러한 업데이트의 일환으로 `my.omniture.com`을 비롯한 기존 도메인 또는 기존 SSO를 통한 액세스는 **2026년 1월 2일**&#x200B;부터 영구 중단됩니다. 이 날짜 이후에는 기존 로그인 자격 증명과 기존 SSO가 더 이상 작동하지 않습니다. 모든 사용자는 Adobe Experience Cloud ID를 사용하여 `experience.adobe.com`을 통해 로그인해야 합니다. Experience Cloud ID와 관련하여 도움이 필요한 경우, 조직의 Adobe Analytics 관리자 또는 [Adobe 고객 지원 센터](https://helpx.adobe.com/kr/contact.html)에 문의하십시오. |
| **Adobe Analytics API (버전 1.4)** | 2024년 7월 17일 목요일 | **2026년 8월 12일**&#x200B;에 다음과 같은 Analytics Legacy API 서비스가 종료되며 해당 서비스를 사용하여 빌드한 현재 모든 통합 기능은 더 이상 작동하지 않습니다.<ul><li>Adobe Analytics API (버전 1.4)</li><li>Adobe Analytics WSSE 인증</li></ul><p>Adobe Analytics API(버전 1.4)를 사용하는 통합은 [Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)로 마이그레이션되어야 하며 WSSE 통합은 [Adobe Developer Console](https://developer.adobe.com/console)의 OAuth 기반 인증 프로토콜로 마이그레이션되어야 합니다.</p><p>자주 묻는 질문에 대한 답변과 자세한 안내는 [Adobe Analytics 1.4 API EOL FAQ](https://developer.adobe.com/analytics-apis/docs/1.4/guides/eol/)를 참조하십시오.</p> |


## AppMeasurement

AppMeasurement 릴리스에 대한 최신 업데이트는 [AppMeasurement 릴리스 정보](https://github.com/adobe/appmeasurement/releases)를 참조하십시오.


## 관련 리소스

* [2025년 이전 릴리스 정보](/help/release-notes/2025.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [스트리밍 미디어 서비스 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트
