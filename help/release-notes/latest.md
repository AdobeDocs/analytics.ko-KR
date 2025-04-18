---
title: 현재 Adobe Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: e2e387f20d5e5732ec1d7eb67a0c81df95e07a55
workflow-type: tm+mt
source-wordcount: '663'
ht-degree: 60%

---

# 최신 Adobe Analytics 릴리스 정보 (2025년 4월 릴리스)

**마지막 업데이트**: 2025년 4월 16일 목요일

이 릴리스 정보는 2025년 3월 26일부터 5월까지의 릴리스 기간을 다룹니다. Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 새로운 기능 또는 개선 사항 {#features}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Analytics 인벤토리** | Analytics 인벤토리에서는 프로젝트 및 구성 요소 수, 보고서 세트, 사용자 등을 포함하여 Adobe Analytics 환경에 대한 포괄적인 개요를 제공합니다. 인벤토리 프로세스를 자동화하면 Adobe Analytics에서 Customer Journey Analytics로 전환하는 데 필요한 작업을 빠르게 파악할 수 있습니다. 이렇게 하면 전환이 더 쉽고 빨라집니다. [자세히 알아보기](https://experienceleague.adobe.com/ko/docs/analytics/admin/admin-tools/analytics-inventory) |  | 2025년 3월 26일 |
| **Data Warehouse 전용 차원** | 고객의 피드백을 바탕으로 재평가를 하기로 결정했습니다. 이전에 발표된 대로 자동 Data Warehouse 전용 차원 기능을 릴리스하지 않습니다. | | TBD |

## Adobe Analytics의 수정 사항

**A4T**: AN-370625; AN-371279; AN-371351
**관리 도구**: AN-365072; AN-371303
**Analysis Workspace**: AN-363831; AN-369554
**분류**: AN-370519; AN-370727; AN-370827; AN-370941; AN-370995; AN-371377; AN-371597; AN-371868; AN-371869; AN-372510; AN-372650; AN-373164; AN-373300; AN-373308 373592
**데이터 수집**: AN-371877
**데이터 피드**: AN-368676; AN-370225; AN-370514; AN-370521; AN-370687; AN-370761; AN-370911; AN-371047; AN-371542; AN-371627; AN-371746; AN-372708; AN-373068 373179
**Data Warehouse**: AN-366649; AN-369817; AN-370705; AN-371127; AN-371995; AN-372596; AN-372940
**마케팅 채널**: AN-372308
**모바일 앱**: AN-370287; AN-371335; AN-371374
**플랫폼**: AN-369510; AN-370435; AN-372150
**Report Builder**: AN-369830; AN-371395; AN-372983

## Adobe Analytics 관리자에 대한 중요 공지 {#admin}

| 공지 | 추가 또는 업데이트 일자 | 설명 |
| ----------- | ---------- | ---------- |
| 해당 사항 없음 |  |  |

## 서비스 종료(EOL) 알림 {#eol}

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **기존 도메인 또는 기존 SSO를 통해 액세스** | 2025년 4월 10일 금요일 | Adobe은 사용자가 Adobe Analytics에 액세스하는 방법을 업데이트하여 보안을 강화하고 로그인 환경을 간소화합니다. 이러한 노력의 일환으로, `my.omniture.com`을(를) 포함하여 레거시 도메인 또는 레거시 SSO를 통한 액세스는 **2026년 1월 2일**&#x200B;에 영구적으로 중단됩니다. 이 날짜 이후, 기존 로그인 자격 증명과 기존 SSO는 더 이상 작동하지 않습니다. 모든 사용자는 자신의 Adobe Experience Cloud ID를 사용하여 `experience.adobe.com`을(를) 통해 로그인해야 합니다. Experience Cloud ID에 대한 지원이 필요한 경우 조직의 Adobe Analytics 관리자 또는 [Adobe 고객 지원 센터](https://helpx.adobe.com/contact.html)에 문의하십시오. |
| **Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션** | 2025년 1월 17일 | Adobe I/O JWT 자격 증명을 사용하는 Adobe Analytics API 및 Livestream 고객은 **2025년 6월 30일**&#x200B;까지 Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 2024년 5월 1일부터는 Adobe I/O를 사용하여 새 JWT 자격 증명을 만들 수 없습니다. JWT를 사용하는 고객은 OAuth 서버 간 자격 증명을 새로 만들거나 기존 JWT 자격 증명을 OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 또한 고객은 새 OAuth 서버 간 자격 증명을 사용하려면 클라이언트 애플리케이션을 업데이트해야 합니다. <ul><li>[서비스 계정(JWT) 자격 증명에서 마이그레이션](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[OAuth를 사용한 신규 및 기존 애플리케이션 구현 안내서](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[새 OAuth 서버 간 자격 증명 사용](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[FAQ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |
| **Adobe Analytics API(버전 1.4)에 대한 EOL** | 2024년 7월 17일 | **2026년 8월 12일**&#x200B;에 다음과 같은 Analytics Legacy API 서비스가 종료되며 해당 서비스를 사용하여 빌드한 현재 모든 통합 기능은 더 이상 작동하지 않습니다.<ul><li>Adobe Analytics API (버전 1.4)</li><li>Adobe Analytics WSSE 인증</li></ul><p>Adobe Analytics API(버전 1.4)를 사용하는 통합은 [Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)로 마이그레이션되어야 하며 WSSE 통합은 [Adobe Developer Console](https://developer.adobe.com/console)의 OAuth 기반 인증 프로토콜로 마이그레이션되어야 합니다.</p><p>자주 묻는 질문에 대한 답변과 자세한 안내는 [Adobe Analytics 1.4 API EOL FAQ](/help/admin/c-admin-api/c-admin-14-api-eol.md)를 참조하시기 바랍니다.</p> |


## AppMeasurement

AppMeasurement 릴리스에 대한 최신 업데이트는 [AppMeasurement 릴리스 정보](https://github.com/adobe/appmeasurement/releases)를 참조하십시오.


## 관련 리소스

* [2025년 이전 릴리스 정보](/help/release-notes/2025.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [스트리밍 미디어 컬렉션 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트
