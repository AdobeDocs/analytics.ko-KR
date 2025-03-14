---
title: 현재 Adobe Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 2b13f649d286e9eb707f2dd22c068b9742c51c70
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 53%

---

# 최신 Adobe Analytics 릴리스 정보 (2025년 3월 릴리스)

**마지막 업데이트**: 2025년 3월 12일 목요일

이 릴리스 정보는 2025년 3월 5일부터 5월까지의 릴리스 기간을 다룹니다. Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 새로운 기능 또는 개선 사항 {#features}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Analytics 컨텍스트 데이터 필드 업데이트`a.locale`** | 이 업데이트는 Experience Edge을 통해 데이터를 수집할 때 Analytics 컨텍스트 데이터 필드 `a.locale`을(를) 설정하는 방법을 변경합니다. Experience Edge를 사용하여 Adobe Analytics로 데이터를 전송하면 XDM 필드의 매핑을 기반으로 Analytics 필드가 채워집니다. `c.a.locale`에 대한 매핑은 비표준 XDM 필드인 `xdm.environment.language`를 참조합니다. 이 필드는 올바른 필드 `xdm.environment._dc.language`를 참조하도록 업데이트됩니다.<p>해당 매핑은 이전 버전과의 호환성을 유지하기 위해 `xdm.environment.language`를 계속 참조합니다. 연속성의 경우 두 필드가 모두 설정되면 `xdm.environment.language`이(가) 우선합니다. XDM에서 표준 Analytics 필드로 매핑되는 전체 목록은 [여기](https://experienceleague.adobe.com/ko/docs/analytics/implementation/aep-edge/xdm-var-mapping)에서 확인할 수 있습니다. | | 2025년 3월 5일 |
| **Customer Journey Analytics 업그레이드 안내서** | Adobe Analytics에서 Customer Journey Analytics으로 업그레이드하기 위한 단계별 안내서를 생성할 수 있습니다. 이 안내서는 조직에 맞게 구성되어 있으며 현재 Adobe Analytics 환경, Customer Journey Analytics의 사용 목적 및 조직에서 수행하려는 시간 절약 요약을 고려합니다.<p>사용자 지정 가이드를 생성하려면 [!DNL Customer Journey Analytics]에 로그인한 다음 **[!UICONTROL Customer Journey Analytics]** 탭에서 **[!UICONTROL Workspace으로 업그레이드]**&#x200B;를 선택합니다.<p>[자세히 알아보기](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/upgrade-to-cja/cja-upgrade-recommendations#recommended-upgrade-steps-for-most-organizations) |  | 2025년 3월 11일 수요일 |
| **Data Warehouse 전용 차원** | 2025년 5월부터 Adobe은 카디널리티가 매우 높은 차원(eVar 및 prop과 같은 사용자 지정 변수)을 &#39;Data Warehouse 전용&#39;으로 설정할 예정입니다. 높은 카디널리티 변수에는 많은 고유한 값이 있습니다. 예로는 타임스탬프 또는 UUID가 있습니다. Analysis Workspace에서는 이러한 차원을 더 이상 보고에 사용할 수 없습니다.<p>이 변경에 대한 후보는 해당 월의 매우 이른 시간에 낮은 트래픽 제한을 초과하는 차원입니다. 이러한 유형의 차원을 사용하면, 보고 가능한 데이터가 수집된 초기 값의 얇은 부분만 나타내므로 이 차원을 기반으로 하는 Analysis Workspace의 보고서가 유용하지 않습니다.<p>Data Warehouse에는 낮은 트래픽 제한이 적용되지 않으므로 이러한 유형의 차원을 기반으로 유용한 보고서나 세그먼트를 작성할 수 있습니다. | | 2025년 5월 |


## Adobe Analytics의 수정 사항

**Activity Map**: AN-361038
**관리 도구**: AN-362178; AN-369483
**Analytics API 1.4**: AN-369615
**Analysis Workspace**: AN-353491; AN-363403; AN-367230; AN-367313; AN-368582; AN-369821; AN-370227;
**분류**: AN-369848; AN-370196; AN-370226; AN-370437
**데이터 피드**: AN-366162; AN-368906; AN-369066; AN-369087; AN-369225; AN-369798
**데이터 거버넌스**: AN-365157
**데이터 소스**: AN-367550
**플랫폼**: AN-363931
**Report Builder**: AN-367460; AN-368975

## Adobe Analytics 관리자에 대한 중요 공지 {#admin}

| 공지 | 추가 또는 업데이트 일자 | 설명 |
| ----------- | ---------- | ---------- |
| 해당 사항 없음 |  |  |

## 서비스 종료(EOL) 알림 {#eol}

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션** | 2025년 1월 17일 | Adobe I/O JWT 자격 증명을 사용하는 Adobe Analytics API 및 Livestream 고객은 **2025년 6월 30일**&#x200B;까지 Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 2024년 5월 1일부터는 Adobe I/O를 사용하여 새 JWT 자격 증명을 만들 수 없습니다. JWT를 사용하는 고객은 OAuth 서버 간 자격 증명을 새로 만들거나 기존 JWT 자격 증명을 OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 또한 고객은 새 OAuth 서버 간 자격 증명을 사용하려면 클라이언트 애플리케이션을 업데이트해야 합니다. <ul><li>[서비스 계정(JWT) 자격 증명에서 마이그레이션](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[OAuth를 사용한 신규 및 기존 애플리케이션 구현 안내서](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[새 OAuth 서버 간 자격 증명 사용](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[FAQ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |
| **Adobe Analytics API(버전 1.4)에 대한 EOL** | 2024년 7월 17일 | **2026년 8월 12일**&#x200B;에 다음과 같은 Analytics Legacy API 서비스가 종료되며 해당 서비스를 사용하여 빌드한 현재 모든 통합 기능은 더 이상 작동하지 않습니다.<ul><li>Adobe Analytics API (버전 1.4)</li><li>Adobe Analytics WSSE 인증</li></ul><p>Adobe Analytics API(버전 1.4)를 사용하는 통합은 [Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)로 마이그레이션되어야 하며 WSSE 통합은 [Adobe Developer Console](https://developer.adobe.com/console)의 OAuth 기반 인증 프로토콜로 마이그레이션되어야 합니다.</p><p>자주 묻는 질문에 대한 답변과 자세한 안내는 [Adobe Analytics 1.4 API EOL FAQ](/help/admin/c-admin-api/c-admin-14-api-eol.md)를 참조하시기 바랍니다.</p> |


## AppMeasurement

AppMeasurement 릴리스(버전 2.27.0)에 대한 최신 업데이트는 [JavaScript용 AppMeasurement 릴리스 노트](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html)를 참조하십시오.


## 관련 리소스

* [2025년 이전 릴리스 정보](/help/release-notes/2025.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [스트리밍 미디어 컬렉션 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트
