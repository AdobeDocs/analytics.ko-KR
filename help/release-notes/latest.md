---
title: 현재 Adobe Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: df9470f1870879ac91f00a021ed890bc6fb10cda
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 96%

---

# 현재 Adobe Analytics 릴리스 정보(2024년 6월)

**마지막 업데이트**: 2024년 6월 13일 금요일

이번 릴리스 정보에는 2024년 6월 12일부터 7월까지의 릴리스 기간이 포함됩니다. Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 새로운 기능 또는 개선 사항 {#features}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **드롭다운 필터에서 여러 필드 선택** | 드롭다운 필터에 여러 필드를 추가한 경우 이제 사용자가 한 번에 여러 개의 필드를 선택할 수 있습니다. 선택된 필드를 포함하도록 패널이 필터링됩니다. <p>이전에는 사용자가 드롭다운 필터에서 한 번에 하나의 필드만 선택할 수 있었습니다.</p><p>자세한 내용은 [정적 드롭다운 세그먼트](/help/analyze/analysis-workspace/c-panels/panels.md#static-drop-down-segments) 위치: [패널 개요](/help/analyze/analysis-workspace/c-panels/panels.md).</p> |  | 2024년 6월 19일 목요일 |
| **Workspace 프로젝트 목차** | 이제 프로젝트에 새로운 목차를 사용할 수 있습니다. 목차는 사용자가 프로젝트 내 패널 및 시각화로 빠르게 이동할 수 있는 링크를 제공합니다. 목차는 개별 프로젝트 또는 해당 사용자의 모든 프로젝트에 대해 활성화할 수 있습니다.<p>자세한 내용은 [프로젝트 목차](/help/analyze/analysis-workspace/build-workspace-project/project-table-of-contents.md).</p> |  | 2024년 6월 19일 목요일 |
| **자유 형식 테이블의 차원 항목에 대한 하이퍼링크 만들기** | 여러 차원 항목에 대한 하이퍼링크를 만들어 Analysis Workspace의 자유 형식 테이블 내에서 해당 항목을 클릭하도록 할 수 있습니다. <p>URL 값이 있는 차원 항목에 대해 하이퍼링크를 만들거나, URL이 아닌 값이 있는 차원 항목에 대해 사용자 정의 URL을 만들 수 있습니다.</p><p>변수를 사용하여 여러 차원 항목에 대한 동적 사용자 정의 URL을 만들 수 있습니다. 변수는 차원 항목의 값을 참조하거나 분류 차원을 참조할 수 있습니다.</p><p>자세한 내용은 [자유 형식 테이블에서 차원에 대한 하이퍼링크 만들기](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table-hyperlinks.md).</p> |  | 2024년 6월 19일 목요일 |
| **내보내기 및 가져오기에 사용되는 계정 및 위치를 제어하는 &#x200B;&#x200B;관리자 설정** | 관리자는 [위치 관리자의 새로운 “관리자 설정” 탭](/help/components/locations/locations-manager.md#configure-company-wide-settings-administrators-only)을 통해 사용자가 계정과 위치를 생성하고 편집할 수 있는지 여부를 제어할 수 있습니다. 이러한 설정은 [사용자가 클라우드 가져오기 및 내보내기 계정을 구성](/help/components/locations/configure-import-accounts.md)하고 [클라우드 가져오기 및 내보내기 위치를 구성](/help/components/locations/configure-import-locations.md)할 때 적용됩니다. <p>관리자는 사용자가 만들고 사용할 수 있는 계정 유형(Google Cloud Platform, Azure RBAC, Amazon S3 등)을 제한할 수도 있습니다.</p><p>이전에는 모든 사용자가 모든 유형의 계정에 대해 계정과 위치를 만들고, 편집하고, 사용할 수 있었습니다.</p> | 2024년 6월 12일 | 2024년 6월 20일 금요일 |
| **내보내기 및 가져오기에 사용되는 계정 및 위치 공유** | 이제 사용자는 자신이 만든 계정과 위치를 조직의 모든 사용자가 사용할 수 있도록 할 수 있습니다. 계정 및 위치 소유자와 시스템 관리자만 계정과 위치를 편집하고 삭제할 수 있습니다.<p>이전에는 계정과 위치를 생성한 사용자만 사용할 수 있었습니다.</p><p>이러한 설정은 사용자가 [클라우드 가져오기 및 내보내기 계정을 구성](https://experienceleague.adobe.com/ko/docs/analytics/components/locations/configure-import-accounts)하고 [클라우드 가져오기 및 내보내기 위치를 구성](https://experienceleague.adobe.com/ko/docs/analytics/components/locations/configure-import-locations)할 때 사용할 수 있습니다. </p> | 2024년 6월 12일 | 2024년 6월 20일 금요일 |
| **Activity Map에서 Web SDK에 대해 더 적은 서버 호출 사용** | 현재 Activity Map 링크 이벤트는 자체 이벤트로 계산되어 추가 비용이 발생합니다. 이 향상된 기능을 통해 일부 링크 이벤트를 가져와 다음 히트로 패키지화합니다. 이는 AppMeasurement에서 이벤트를 처리하는 방법과 유사합니다. <p>(업데이트된 설명서 링크)</p> | 2024년 6월 19일 오픈 베타 시작 | TBD |

{style="table-layout:auto"}

## Adobe Analytics의 수정 사항

* 다음 분류 문제가 수정되었습니다. AN-347682; AN-348396; AN-348625; AN-348668; AN-348926; AN-348936; AN-349040; AN-349191; AN-349195; AN-349443; AN-349697; AN-349758; AN-349862; AN-350051; AN-350054; AN-350208; AN-350497; AN-350525; AN-351067
* 다음 Data Warehouse 문제가 수정되었습니다. AN-346862, AN-349409, AN-349926, AN-350629, AN-350996
* 다음 데이터 피드 문제가 수정되었습니다. AN-346727; AN-348282; AN-348334; AN-348725; AN-348726; AN-348823; AN-349081; AN-349207; AN-349307; AN-349539; AN-349710; AN-349729; AN-349742; AN-349878; AN-349943; AN-350527;
* 다음 데이터 소스 문제가 수정되었습니다. AN-350038
* 다음 Analysis Workspace 문제가 수정되었습니다. AN-342953, AN-346346, AN-349590, AN-349717, AN-350057, AN-350697, AN-350904
* 다음 Report Builder 문제가 수정되었습니다. AN-348903; AN-350691
* 다음 A4T 문제가 수정되었습니다. AN-347690, AN-350853

### 기타 Analytics 수정 사항

AN-346470; AN-346850; AN-347227; AN-348145; AN-348564; AN-349001; AN-349008; AN-349211; AN-349719; AN-350523;

## Adobe Analytics 관리자에 대한 중요 공지 {#admin}

| 공지 | 추가 또는 업데이트 일자 | 설명 |
| ----------- | ---------- | ---------- |
| **저장된 기간이 13개월 만료됨:`cust_visids`** | 2024년 5월 22일 | **2024년 7월로 예정**&#x200B;된 Analytics Hit 처리 엔진의 향후 릴리스에서는 저장된 `cust_visids`의 만료 기간을 13개월로 적용할 예정입니다. 보고서 세트에 “방문자 결합 활성화”가 활성화된 경우 이 설정은 히트에 `cust_visid`가 없는 `visid_high/visid_low value`에 대해 `cust_visid`를 찾는 데 사용됩니다. 현재는 `visid_high/visid_low`에 대한 `cust_visid`의 매핑 만료가 없습니다. 이 릴리스에서는 `visid_high/visid_low`가 `cust_visid`를 히트시킨 후 13개월 이상 경과한 경우 매핑이 만료됩니다. |
| **ISO 지역 업데이트** | 2024년 5월 10일 | Adobe는 2024년 6월 7일에 2024 ISO 지역 업데이트를 수행합니다. 이 릴리스 이후에 부분적인 지역 정보(지역) 업데이트가 있을 것으로 예상됩니다. |

{style="table-layout:auto"}

## 서비스 종료(EOL) 알림 {#eol}

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션** | 2023년 5월 11일 | Adobe I/O JWT 자격 증명을 사용하는 Adobe Analytics API 및 Livestream 고객은 **2025년 1월 1일**&#x200B;까지 Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 2024년 5월 1일부터는 Adobe I/O를 사용하여 새 JWT 자격 증명을 만들 수 없습니다. JWT를 사용하는 고객은 OAuth 서버 간 자격 증명을 새로 만들거나 기존 JWT 자격 증명을 OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 또한 고객은 새 OAuth 서버 간 자격 증명을 사용하려면 클라이언트 애플리케이션을 업데이트해야 합니다. <ul><li>[서비스 계정(JWT) 자격 증명에서 마이그레이션](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[OAuth를 사용한 신규 및 기존 애플리케이션 구현 안내서](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[새 OAuth 서버 간 자격 증명 사용](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[FAQ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |

{style="table-layout:auto"}

## AppMeasurement

AppMeasurement 릴리스(버전 2.26.0)에 대한 최신 업데이트는 [JavaScript용 AppMeasurement 릴리스 정보](https://experienceleague.adobe.com/ko/docs/analytics/implementation/appmeasurement-updates.html?lang=ko-KR)를 참조하십시오.


## 관련 리소스

* [2024년 이전 릴리스 정보](/help/release-notes/2024.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/releases/latest.html?lang=ko-KR)
* [Media Analytics 릴리스 정보](https://experienceleague.adobe.com/ko/docs/media-analytics/using/additional-resources/release-notes.html?lang=ko-KR)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트
