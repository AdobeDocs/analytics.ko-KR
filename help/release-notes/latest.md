---
title: 현재 Adobe Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 58098a24e826161bbd7aadb98abe050fd944791e
workflow-type: tm+mt
source-wordcount: '1221'
ht-degree: 49%

---

# 최신 Adobe Analytics 릴리스 정보 (2026년 1월)

**마지막 업데이트**: 2026년 1월 14일 목요일

이 릴리스 노트는 2026년 1월 릴리스 기간에 대해 설명합니다. Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 새로운 기능 또는 개선 사항 {#features}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **분류 집합 규칙 빌더** | 이제 분류 세트에서 [규칙 빌더](/help/components/classifications/sets/manage/rules.md) 기능을 사용할 수 있습니다. 분류 세트의 컨텍스트 내에서 규칙을 정의합니다. 분류 세트를 구독하는 모든 보고서 세트 및 키 차원 조합에 규칙이 적용됩니다(활성화된 경우).</p> |  | 2026년 1월 23일 토요일 |
| **개선된 데이터 피드** | 이제 데이터 피드에 다음과 같은 개선 사항을 사용할 수 있습니다.<ul><li>사용자 경험이 개선되었습니다.</li><li>열 템플릿을 만들고 관리할 수 있는 새로운 환경.</li><li>이제 향후 데이터 피드에서 다시 사용할 열 템플릿을 만들 시기를 선택할 수 있습니다. 템플릿을 삭제, 편집 및 복사할 수도 있습니다.<br/>이전에는 만들어진 각 데이터 피드에 새 열 템플릿이 추가되어 사용하지 않는 열 템플릿이 대량으로 나타나며 삭제하거나 관리할 방법이 없었습니다.</li><li>태그를 기준으로 추가 및 필터링합니다.</li><li>데이터 피드 작업 내역 보기 (요청 기간이 시작되고, 시작되고, 완료되는 등의 시간.)</li><li>데이터 피드를 다시 보내거나 다시 처리합니다. (작업 내역 페이지에서)</li><li>늦게 도착하는 히트를 허용합니다. 이제 데이터 피드 작업이 설정된 보고 빈도 내에서 데이터 처리를 완료한 후에 도착하는 데이터를 포함할 수 있습니다.</li><li>데이터 피드에 대한 종료 날짜를 선택할 때 선택한 종료 날짜가 데이터 피드의 마지막 날로 포함됩니다.<br/>이전에는 데이터 피드에서 종료 날짜가 제외되었습니다.</li><li>이제 15분 내보내기 빈도가 가능하지만 기본적으로 사용할 수 없습니다. 이 옵션을 사용자 환경에서 사용하려면 먼저 Adobe 고객 지원 센터에 문의하여 보고서 세트가 15분 내보내기를 지원하도록 구성되었는지 요청해야 합니다.</li></ul><p>**참고:** 이러한 개선 사항으로 Adobe Analytics의 데이터 피드 페이지에 대한 URL도 업데이트됩니다. 2026년 4월 30일까지 새 데이터 피드 페이지를 가리키도록 기존 책갈피를 업데이트하십시오.</p>(참조할 설명서 링크입니다.)</p> | 2026년 1월 20일 수요일 | 2026년 2월 10일 수요일 |
| **여러 열로 표 정렬** | 이제 Analysis Workspace에서 차원 또는 지표에 관계없이 자유 형식 테이블의 데이터를 여러 열로 정렬할 수 있습니다.<p>여러 열에 대한 데이터를 정렬할 때 데이터는 각 열에 할당하는 우선 순위에 따라 정렬됩니다. 정렬 아이콘 옆에 우선 순위 번호가 표시됩니다.</p><p>(참조할 설명서 링크입니다.)<!-- For more information, see "Filter and sort freeform tables". (need to move info to this article from "Include multiple dimension columns in a freeform table") --></p> | 2026년 1월 28일 목요일 | 2026년 2월 18일 목요일 |
| **스트리밍 미디어 서비스: 일정 데이터 지원** | 이제 과거 라이브 스트리밍 미디어 콘텐츠의 예약된 데이터를 업로드하여 시청자 수를 보다 쉽고 정확하게 추적할 수 있습니다.<p>다음은 일정 데이터 업로드가 지원되는 라이브 콘텐츠의 예입니다.</p><ul><li>FAST(무료 광고 지원 TV) 플랫폼</li><li>로컬 스트림</li><li>라이브 스포츠</li></ul><p>일정 데이터를 업로드하면 업로드 파일에서 지정한 시간 동안 실행된 개별 프로그램의 시청자 수 데이터를 추적할 수 있습니다. 특정 주제나 프로그램 세그먼트에 대한 시청자 수 데이터를 수집할 수도 있습니다.</p><p>이러한 기능은 스트리밍 미디어 컬렉션을 어떻게 구현하든 관계없이 사용할 수 있습니다.</p><p>이전에는 라이브 콘텐츠를 분석할 때 주어진 세션을 특정 프로그램에 정확하게 연결하는 것이 어려웠고, 주어진 세션을 개별 주제나 프로그램 세그먼트에 연결하는 것도 불가능했습니다.</p><p>자세한 내용은 [라이브 콘텐츠를 추적할 일정 데이터 업로드](https://experienceleague.adobe.com/ko/docs/media-analytics/using/media-use-cases/track-schedule-data)를 참조하십시오.</p> | 2025년 10월 29일 | 2026년 상반기<p>(원래 2025년 10월 29일 릴리스로 계획됨)</p> |

## Adobe Analytics의 수정 사항

**Activity Map**:
**Analysis Workspace**: AN-423389, AN-422636, AN-422482, AN-422027, AN-421134, AN-420187, AN-406271, AN-406188, AN-405997, AN-405983, AN-405796, AN-405033, AN-404893, AN-404871, AN-404842, AN-404713, AN-404502, AN-404353, AN-404352, AN-404048, AN-402523, AN-396149, AN-390990, AN-390728 390646 383484 376980 371729 347570
**분류**: AN-423985, AN-423092, AN-423067, AN-422913, AN-422908, AN-422793, AN-422785, AN-422745, AN-422705, AN-422422, AN-422126, AN-422098, AN-422077, AN-422058, AN-421999, AN-421698, AN-421351, AN-406583, AN-406295, AN-406123, AN-406052 404743 404372
**데이터 수집**: AN-422488
**데이터 피드 및 Data Warehouse**: AN-423186, AN-422789, AN-422239, AN-421552, AN-421393, AN-421339, AN-421231, AN-420149, AN-406345, AN-406217, AN-405073, AN-404822, AN-404774 389691
**개인 정보**:
**Report Builder**: AN-422120, AN-421937, AN-406296, AN-402951, AN-399748
**보고**:
**예약된 보고서**: AN-423087, AN-422686
**세그먼트 비교**:
**기타**: AN-423401, AN-422819, AN-422775, AN-422626, AN-422238, AN-422160, AN-422071, AN-421687, AN-420045, AN-404891, AN-404608, AN-390912


## 서비스 종료(EOL) 알림 {#eol}

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **실시간 스트리밍 처리 개선 사항** | 2026년 1월 14일 목요일 | Adobe은 라이브 스트림 페이로드의 형식을 개선하고 변경할 계획입니다. 이러한 업데이트는 LiveStream과 Analysis Workspace과 같은 다른 Adobe Analytics 기능 간의 패리티를 향상합니다. 계획된 변경 사항을 테스트할 수 있는 미리보기 엔드포인트를 사용할 수 있습니다. 변경 사항의 전체 목록 및 미리 보기 끝점 세부 정보는 [LiveStream 릴리스 정보]를 참조하십시오. Adobe은 2026년 4월 13일에 업데이트된 페이로드 포맷으로 하드 컷오버를 계획합니다. |
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
