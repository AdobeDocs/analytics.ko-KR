---
title: 현재 Adobe Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 46d2360e8314d5b21e141799477b0f67367e56df
workflow-type: tm+mt
source-wordcount: '1256'
ht-degree: 83%

---

# 최신 Adobe Analytics 릴리스 정보 (2025년 10월 릴리스)

**마지막 업데이트**: 2025년 10월 14일 수요일

이 릴리스 정보는 2025년 10월부터 11월 초까지의 릴리스 기간을 다룹니다. Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 새로운 기능 또는 개선 사항 {#features}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **선 시각화 및 스파크라인에 포함된 필터 조건** | 자유 형식 테이블 필터에 적용하는 모든 검색 필터 조건은 이제 항상 스파크라인에 포함됩니다. 또한 연결된 선 시각화에 검색 필터 기준을 포함할 수 있습니다.<p>연결된 테이블의 지표 열 헤더에서 스파크라인을 선택하여 검색 필터 기준을 포함하도록 라인 시각화를 구성할 수 있습니다.</p><p>이전에는 검색 필터 기준이 스파크라인 또는 연결된 라인 시각화에 포함되지 않았습니다.</p><p>자세한 내용은 [자유 형식 테이블에 대한 트렌드 데이터 보기](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table-trended-data.md)를 참조하십시오.</p> | | 2025년 10월 15일 |
| **새로운 레퍼러 유형 차원 항목으로 AI 트래픽 분석** | AI 도구에서 유입되는 트래픽을 분석하는 데 도움이 되는 새로운 레퍼러 유형 차원 항목이 제공됩니다. <p>대화형 AI 도구라고 불리는 이 새로운 레퍼러 유형 차원 항목은 주요 AI 도구의 참조 도메인을 그룹화하여 그룹 전체의 추세를 살펴볼 수 있도록 해 줍니다. 이 새로운 카테고리의 참조 도메인의 초기 목록에는 다음과 같은 항목이 포함되며, 이에 국한되지 않습니다.</p><ul><li>chatgpt.com</li><li>claude.ai</li><li>m365.cloud.Microsoft</li><li>grok.com</li><li>gemini.google.com</li><li>perplexity.ai</li></ul><p>새로운 차원 항목은 Analysis Workspace, Report Builder, Data Warehouse, Data Feeds 등 모든 Adobe Analytics 관련 도구에서 사용할 수 있습니다.</p><p>이 새로운 차원 항목을 사용할 때 다음 사항을 고려하십시오.</p><ul><li>검색 엔진에서 “AI 모드”로 제공된 결과에서 나온 레퍼러 트래픽과 클릭스루에서 나온 트래픽을 전통적인 검색 결과와 구별하는 것이 항상 가능한 것은 아닙니다.</li><li>새로운 대화형 AI 도구 차원 항목은 트래픽이 가장 많은 주요 공급업체에 초점을 맞춥니다. 새로운 추세에 따르면 주요 AI 도구 제공업체와 유사한 도메인을 가진 사칭 사이트가 증가하고 있습니다. 이는 개인이나 그룹이 자신만의 AI 도구를 만들고 인터넷에 호스팅하는 것이 쉬워졌기 때문일 가능성이 높습니다. 이 분야는 빠르게 변화하고 있으므로 인기 있는 사이트가 포함되지 않은 경우 Adobe 지원 팀에 문의하십시오.</li><li>새로운 대화형 AI 도구 차원 항목을 포함한 레퍼러 유형 차원은 Adobe Analytics에서 처리하는 데이터에만 사용할 수 있습니다. </li></ul><p>(참조할 설명서 링크입니다.)</p> |   | 2025년 10월 15일 |
| **스트리밍 미디어 서비스: 일정 데이터 지원** | 이제 과거 라이브 스트리밍 미디어 콘텐츠의 예약된 데이터를 업로드하여 시청자 수를 보다 쉽고 정확하게 추적할 수 있습니다.<p>다음은 일정 데이터 업로드가 지원되는 라이브 콘텐츠의 예입니다.</p><ul><li>FAST(무료 광고 지원 TV) 플랫폼</li><li>로컬 스트림</li><li>라이브 스포츠</li></ul><p>일정 데이터를 업로드하면 업로드 파일에서 지정한 시간 동안 실행된 개별 프로그램의 시청자 수 데이터를 추적할 수 있습니다. 특정 주제나 프로그램 세그먼트에 대한 시청자 수 데이터를 수집할 수도 있습니다.</p><p>이러한 기능은 스트리밍 미디어 컬렉션을 어떻게 구현하든 관계없이 사용할 수 있습니다.</p><p>이전에는 라이브 콘텐츠를 분석할 때 주어진 세션을 특정 프로그램에 정확하게 연결하는 것이 어려웠고, 주어진 세션을 개별 주제나 프로그램 세그먼트에 연결하는 것도 불가능했습니다.</p><p>(참조할 설명서 링크입니다.)<!--For more information, see [Upload schedule data to track live content](https://experienceleague.adobe.com/en/docs/media-analytics/using/media-use-cases/track-schedule-data)--></p> |  | 2025년 10월 29일 |
| **스트리밍 미디어 서비스: 스트리밍 미디어 데이터를 Adobe Experience Platform으로 수집하기 위한 업데이트된 XDM 필드** | 스트리밍 미디어 데이터를 Adobe Experience Platform으로 수집할 때, 스트리밍 미디어 매개변수 설명서의 “XDM 필드 경로” 제목 아래에 표시된 XDM 필드 경로는 더 이상 사용해서는 안 됩니다. 대신, 2025년 5월 9일 이전에 플랫폼으로 스트리밍 미디어 데이터를 수집하기 위해 Analytics 소스 커넥터를 구현한 고객은 스트리밍 미디어 매개변수 설명서의 “보고 XDM 필드 경로” 제목 아래에 표시된 대로 기존 구성을 mediaReporting 필드 경로로 마이그레이션해야 합니다.<p> 이러한 필드 경로는 다음 페이지에서 찾을 수 있으며 “더 이상 사용되지 않음”으로 표시됩니다. [오디오 및 비디오 매개변수](https://experienceleague.adobe.com/ko/docs/media-analytics/using/implementation/variables/audio-video-parameters), [광고 매개변수](https://experienceleague.adobe.com/ko/docs/media-analytics/using/implementation/variables/ad-parameters), [챕터 매개변수](https://experienceleague.adobe.com/ko/docs/media-analytics/using/implementation/variables/chapter-parameters), [플레이어 상태 매개변수](https://experienceleague.adobe.com/ko/docs/media-analytics/using/implementation/variables/player-state-parameters) 및 [품질 매개변수](https://experienceleague.adobe.com/ko/docs/media-analytics/using/implementation/variables/quality-parameters). (2025년 5월 9일 이후에 Analytics 소스 커넥터를 구현하고 이미 mediaReporting XDM 경로만 사용하고 있는 고객은 아무런 조치가 필요하지 않습니다.)</p><p>더 이상 사용되지 않는 XDM 필드 경로에 대한 데이터 수집은 2025년 10월 말까지 계속됩니다. 그 후에는 사용되지 않는 필드 경로가 완전히 제거되어 Adobe Experience Platform 스키마 UI에서 더 이상 표시되지 않으며, 데이터는 mediaReporting 필드 경로만 사용하여 전송됩니다.</p><p>자세한 내용은 [Analytics Source Connector 구현을 업데이트된 XDM 스트리밍 미디어 필드로 마이그레이션](https://experienceleague.adobe.com/ko/docs/media-analytics/using/media-use-cases/xdm-updates/updated-xdm-fields)을 참조하십시오.</p><p>마이그레이션 지원에 대해서는 Adobe Consulting 서비스 또는 계정 팀에 문의해 주십시오. </p> |  | 2025년 10월 |
| **Adobe Analytics 2.0 API 보고서 세트 만들기** | 2.0 API를 사용하여 Adobe Analytics에서 보고서 세트를 만듭니다. 새로운 POST 메서드는 다가오는 1.4 API의 사용 중단에 대비하여 1.4 보고서 세트 API 생성을 대체합니다. | | 2025년 10월 15일 |

## Adobe Analytics의 수정 사항

**Activity Map**:
**Analysis Workspace**: AN-399209, AN-397146, AN-394992, AN-390795
**분류**: AN-400583, AN-399205, AN-398580, AN-398257, AN-395921, AN-394973
**데이터 수집**:
**데이터 피드 및 Data Warehouse**: AN-400938, AN-399075, AN-398924, AN-398573, AN-396574, AN-393946
**개인 정보**:
**Report Builder**: AN-401127, AN-400618, AN-392971, AN-391692
**보고**:
**예약된 보고서**:
**세그먼트 비교**:
**기타**: AN-396084


## 서비스 종료(EOL) 알림 {#eol}

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **레거시 Report Builder** | 2025년 6월 18일 | 기존 Report Builder 추가 기능은 2026년 6월에 지원이 중단됩니다. 모든 사용자는 기존 통합 문서를 새로운 [Report Builder](/help/analyze/report-builder/rb-overview.md)로 업그레이드해야 합니다. 새로운 Report Builder는 Adobe Analytics와 Customer Journey Analytics 고객 모두에게 제공됩니다. 이는 [거의 동일한 기능](/help/analyze/report-builder/convert-workbooks.md#unsupported)과 더불어 여러 가지 편리하고 새로운 기능과 개선된 UI를 제공합니다. 업그레이드 프로세스를 용이하게 하기 위해 새로운 Report Builder에는 간편한 통합 문서 변환 기능이 포함되어 있습니다. 새로운 Report Builder는 Microsoft Store를 통해 다운로드할 수 있는 추가 기능으로만 제공됩니다. 대부분의 조직에서는 사용자에게 추가 기능을 제공하기 전에 내부 승인 절차를 거쳐야 합니다. 이 프로세스에 시간을 할애하고 지금부터 조직과 협력하여 EOL 날짜 전에 통합 문서를 업그레이드할 충분한 시간을 확보하십시오. |
| **레거시 도메인 또는 레거시 SSO를 통한 액세스** | 2025년 4월 10일 | Adobe는 보안을 강화하고 로그인 환경을 간소화하기 위해 사용자가 Adobe Analytics에 액세스하는 방식을 업데이트할 계획입니다. 이러한 업데이트의 일환으로 `my.omniture.com`을 비롯한 기존 도메인 또는 기존 SSO를 통한 액세스는 **2026년 1월 2일**&#x200B;부터 영구 중단됩니다. 이 날짜 이후에는 기존 로그인 자격 증명과 기존 SSO가 더 이상 작동하지 않습니다. 모든 사용자는 Adobe Experience Cloud ID를 사용하여 `experience.adobe.com`을 통해 로그인해야 합니다. Experience Cloud ID와 관련하여 도움이 필요한 경우, 조직의 Adobe Analytics 관리자 또는 [Adobe 고객 지원 센터](https://helpx.adobe.com/kr/contact.html)에 문의하십시오. |
| **Adobe Analytics API (버전 1.4)** | 2024년 7월 17일 | **2026년 8월 12일**&#x200B;에 다음과 같은 Analytics Legacy API 서비스가 종료되며 해당 서비스를 사용하여 빌드한 현재 모든 통합 기능은 더 이상 작동하지 않습니다.<ul><li>Adobe Analytics API (버전 1.4)</li><li>Adobe Analytics WSSE 인증</li></ul><p>Adobe Analytics API(버전 1.4)를 사용하는 통합은 [Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)로 마이그레이션되어야 하며 WSSE 통합은 [Adobe Developer Console](https://developer.adobe.com/console)의 OAuth 기반 인증 프로토콜로 마이그레이션되어야 합니다.</p><p>자주 묻는 질문에 대한 답변과 자세한 안내는 [Adobe Analytics 1.4 API EOL FAQ](https://developer.adobe.com/analytics-apis/docs/1.4/guides/eol/)를 참조하십시오.</p> |


## AppMeasurement

AppMeasurement 릴리스에 대한 최신 업데이트는 [AppMeasurement 릴리스 정보](https://github.com/adobe/appmeasurement/releases)를 참조하십시오.


## 관련 리소스

* [2025년 이전 릴리스 정보](/help/release-notes/2025.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [스트리밍 미디어 서비스 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트
