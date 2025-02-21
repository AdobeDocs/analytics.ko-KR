---
title: 현재 Adobe Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 924f5f670d2f29269a5ba6623079e839f1fe8122
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 57%

---

# 현재 Adobe Analytics 릴리스 정보 (2025년 2월 릴리스)

**마지막 업데이트**: 2024년 2월 21일

이 릴리스 정보는 2025년 2월 11일부터 3월 중순까지의 릴리스 기간을 다룹니다. Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 새로운 기능 또는 개선 사항 {#features}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **거래 ID 보존 기간** | 거래 ID 보존 기간 90일이 25개월로 연장되었습니다. `transactionID` 변수는 데이터 소스를 통해 업로드된 데이터에 히트가 연결될 수 있도록 거래를 고유하게 식별합니다. [여기](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/page-vars/transactionid) 및 [여기](https://experienceleague.adobe.com/en/docs/analytics/import/data-sources/transactionid)에서 자세히 알아보세요. |  | 2025년 2월 20일 금요일 |
| **데이터 피드 API 참조** | 이제 데이터 피드 API에 대한 [참조](https://adobedocs.github.io/analytics-2.0-apis/?urls.primaryName=Data%20Feeds%20APIs)을(를) 사용할 수 있습니다. |  | 2025년 1월 30일 |
| **실시간 스트리밍 API - 클라이언트 구현** | Livestream 클라이언트 구현을 사용하여 Livestream 데이터를 사용합니다. [자세히 알아보기](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/livestream/clientcode/) |  | 2025년 2월 18일 수요일 |
| **분류 API 업데이트** | 이제 서버에서 개별 분류 필드 또는 키를 제거할 수 있습니다. 이렇게 하면 DELETE 메서드로 전체 분류 데이터 세트를 삭제할 수 있는 대체 방법이 제공됩니다. [자세히 알아보기](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/classifications/remove-values/) |  | 2025년 2월 18일 수요일 |


## Adobe Analytics의 수정 사항

**Analysis Workspace**: AN-359974; AN-366212; AN-368460
**분류**: AN-367186; AN-367328; AN-368548
**구성 요소 마이그레이션**: AN-364529; AN-366398; AN-367509;
**데이터 피드**: AN-365685; AN-366745; AN-367256; AN-367349; AN-368363
**Data Warehouse**: AN-368178; AN-368331;
**모바일 앱**: AN-367137
**플랫폼**: AN-351924; AN-365540; AN-365866; AN-366898; AN-367856; AN-367933
**Report Builder**: AN-366456; AN-366655;
**가상 보고서 세트**: AN-367411
**VISTA 규칙**: AN-365331

## Adobe Analytics 관리자에 대한 중요 공지 {#admin}

| 공지 | 추가 또는 업데이트 일자 | 설명 |
| ----------- | ---------- | ---------- |
| **Analytics 컨텍스트 데이터 필드`a.locale`**&#x200B;에 대해 예정된 업데이트 | 2025년 2월 21일 토요일 | 2025년 3월 5일에 Experience Edge을 통해 데이터를 수집할 때 Analytics 컨텍스트 데이터 필드 `a.locale`을(를) 설정하는 방법에 대한 업데이트가 있을 예정입니다. Experience Edge을 사용하여 데이터를 Adobe Analytics으로 보내면 Analytics 필드가 XDM 필드의 매핑을 기반으로 채워집니다. `c.a.locale`에 대한 매핑이 비표준 XDM 필드 `xdm.environment.language`을(를) 참조합니다. 이 필드는 올바른 필드 `xdm.environment._dc.language`을(를) 참조하도록 업데이트됩니다.  이전 버전과의 호환성을 위해 매핑에서 `xdm.environment.language`을(를) 계속 참조합니다. 연속성의 경우 두 필드가 모두 설정되면 `xdm.environment.language`이(가) 우선합니다. XDM에서 표준 Analytics 필드 [여기](https://experienceleague.adobe.com/en/docs/analytics/implementation/aep-edge/xdm-var-mapping)에 매핑의 전체 목록을 볼 수 있습니다. |
| **캠페인 고객이 아닌 사용자는 트리거에 대한 액세스 권한을 잃게 됩니다.** | 2023년 10월 16일 | 2025년 1월 30일에 Adobe Campaign 라이선스가 없는 Adobe Analytics 고객은 [트리거](https://experienceleague.adobe.com/ko/docs/core-services/interface/services/triggers)를 구성하고 사용할 수 있는 기능에 액세스할 수 없습니다. 고객은 Campaign을 구매하거나 트리거 사용을 중단하거나 트리거 기능을 제공하는 다른 Adobe 도구를 확인해야 합니다. |

## 서비스 종료(EOL) 알림 {#eol}

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션** | 2025년 1월 17일 | Adobe I/O JWT 자격 증명을 사용하는 Adobe Analytics API 및 Livestream 고객은 **2025년 6월 30일**&#x200B;까지 Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 2024년 5월 1일부터는 Adobe I/O를 사용하여 새 JWT 자격 증명을 만들 수 없습니다. JWT를 사용하는 고객은 OAuth 서버 간 자격 증명을 새로 만들거나 기존 JWT 자격 증명을 OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 또한 고객은 새 OAuth 서버 간 자격 증명을 사용하려면 클라이언트 애플리케이션을 업데이트해야 합니다. <ul><li>[서비스 계정(JWT) 자격 증명에서 마이그레이션](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[OAuth를 사용한 신규 및 기존 애플리케이션 구현 안내서](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[새 OAuth 서버 간 자격 증명 사용](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[FAQ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |
| **Adobe Analytics API(버전 1.4)에 대한 EOL** | 2024년 7월 17일 | **2026년 8월 12일**&#x200B;에 다음과 같은 Analytics Legacy API 서비스가 종료되며 해당 서비스를 사용하여 빌드한 현재 모든 통합 기능은 더 이상 작동하지 않습니다.<ul><li>Adobe Analytics API (버전 1.4)</li><li>Adobe Analytics WSSE 인증</li></ul><p>Adobe Analytics API(버전 1.4)를 사용하는 통합은 [Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)로 마이그레이션되어야 하며 WSSE 통합은 [Adobe Developer Console](https://developer.adobe.com/console)의 OAuth 기반 인증 프로토콜로 마이그레이션되어야 합니다.</p><p>자주 묻는 질문에 대한 답변과 자세한 안내는 [Adobe Analytics 1.4 API EOL FAQ](/help/admin/c-admin-api/c-admin-14-api-eol.md)를 참조하시기 바랍니다.</p> |


## AppMeasurement

AppMeasurement 릴리스(버전 2.26.0)에 대한 최신 업데이트는 [JavaScript용 AppMeasurement 릴리스 정보](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html)를 참조하십시오.


## 관련 리소스

* [2024년 이전 릴리스 정보](/help/release-notes/2024.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [스트리밍 미디어 컬렉션 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트
