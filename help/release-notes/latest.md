---
title: 현재 Adobe Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: e281d43204e1c5b10508661f04b880125fe8671c
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 45%

---

# 최신 Adobe Analytics 릴리스 정보 (2025년 1월 릴리스)

**마지막 업데이트**: 2024년 1월 22일 화요일

이 릴리스 정보는 2025년 1월 15일부터 2월 중순까지의 릴리스 기간을 다룹니다. Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 새로운 기능 또는 개선 사항 {#features}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **새 Report Builder에서 예약** | 예약을 사용하면 새 Report Builder 통합 문서를 예약할 수 있을 뿐만 아니라 또한 이전 통합 문서를 변환할 때 이전 예약된 작업에서 메타데이터를 검색할 수 있도록 해줍니다. 이렇게 하면 기존 통합 문서를 새 통합 문서로 변환하고 예약할 때 기존 통합 문서와 동일한 e-메일 및 동일한 케이던스로 통합 문서를 보냅니다. [자세히 알아보기](/help/analyze/report-builder/schedule-reportbuilder.md) |  | 2025년 1월 22일 |
| **Analysis Workspace의 보고서(템플릿이라고도 함)에 대한 개선 사항** | 이제 보고서(템플릿이라고도 함)에 대해 다양한 개선 사항을 사용할 수 있습니다.<ul><li>이제 [!UICONTROL 템플릿](더 이상 [!UICONTROL 보고서](이라고 하지 않음)이라고 합니다.</li><li>열 보기 또는 카드 보기에서 템플릿을 보는 옵션을 포함하여 템플릿을 보고 찾는 사용자 경험이 개선되었습니다.</li><li>보다 직관적인 새 회사 서식 파일 위치(**[!UICONTROL Workspace]** > **[!UICONTROL 서식 파일]**).</li><li>이전에는 프로젝트를 만들 때 대화 상자에서 회사 템플릿에 액세스했습니다.</li><li>사전 제작된 추가 템플릿을 사용할 수 있습니다.</li></ul>[자세히 알아보기](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/templates/use-templates).<p>관리자는 템플릿을 만들고 이를 저장하여 로그인 회사의 다른 사용자가 사용할 수 있도록 할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/templates/create-templates) | 2025년 1월 15일 목요일 | 2025년 1월 30일 금요일 |
| **거래 ID 보존 기간** | 거래 ID 보존 기간 90일이 2025년 2월에 25개월로 연장됩니다. `transactionID` 변수는 데이터 소스를 통해 업로드된 데이터에 히트가 연결될 수 있도록 거래를 고유하게 식별합니다. (다음 설명서 링크) |  | 2025년 2월 11일 수요일 |

## Adobe Analytics의 수정 사항

A4T: AN-355602; AN-365988
Activity Map: AN-365320
Admin Console: AN-363884
관리 도구: AN-356747; AN-358776
Advertising Analytics: AN-355488
Analysis Workspace: AN-345318; AN-354801; AN-357052; AN-358975; AN-362886; AN-363831; AN-364124; AN-365257; AN-365319; AN-365462
Analytics 1.4 API: AN-358059
분류 : AN-360049, AN-360424, AN-362208, AN-362345, AN-362560, AN-362576, AN-362633, AN-362653, AN-362762, AN-362815, AN-362881, AN-362885, 362973, AN-363343, AN-363558, AN-363860, AN-364239, AN-364480, AN-364451, AN-364528, AN-364548, AN-364552, AN-364585, AN-364598, AN-364715, AN-364912, AN-364997, AN-365189, 365197, AN-365203, AN-365431, AN-365647, 365794;
구성 요소 마이그레이션: AN-362236; AN-365429
기여도 분석: AN-360146
자료 제공: AN-356997, AN-362470, AN-362498, AN-362775, AN-363323, AN-363413, AN-363569, AN-364063, AN-364142, AN-364294, AN-364298, AN-364325, AN-364367, AN-364594, AN-364995, AN-365272, AN-365519, AN-365760, AN-366152, AN-, AN-,
데이터 복구 API: AN-362773; AN-362874
데이터 소스: AN-360745; AN-362202; AN-364566
Data Warehouse: AN-361447; AN-362616; AN-364524; AN-365108
모바일 앱: AN-362856; AN-365270
초과 경고: AN-355594; AN-364547
플랫폼: AN-358914; AN-360205; AN-362990; AN-364550; AN-365454; AN-365485
Report Builder: AN-363478; AN-364433; AN-365610
보고 활동 관리자: AN-362440
세그먼테이션: AN-359921
VISTA 규칙: AN-362927

## Adobe Analytics 관리자에 대한 중요 공지 {#admin}

| 공지 | 추가 또는 업데이트 일자 | 설명 |
| ----------- | ---------- | ---------- |
| **캠페인 고객이 아닌 사용자는 트리거에 대한 액세스 권한을 잃게 됩니다.** | 2023년 10월 16일 | 2025년 1월 30일에 Adobe Campaign 라이선스가 없는 Adobe Analytics 고객은 [트리거](https://experienceleague.adobe.com/en/docs/core-services/interface/services/triggers)를 구성하고 사용할 수 있는 기능에 액세스할 수 없게 됩니다. 고객은 Campaign을 구매하거나 트리거 사용을 중단하거나 트리거 기능을 제공하는 다른 Adobe 도구를 확인해야 합니다. |

## 서비스 종료(EOL) 알림 {#eol}

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션** | 2025년 1월 17일 토요일 | Adobe I/O JWT 자격 증명을 사용하는 Adobe Analytics API 및 Livestream 고객은 **2025년 6월 30일 화요일**&#x200B;까지 Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 2024년 5월 1일부터는 Adobe I/O를 사용하여 새 JWT 자격 증명을 만들 수 없습니다. JWT를 사용하는 고객은 OAuth 서버 간 자격 증명을 새로 만들거나 기존 JWT 자격 증명을 OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 또한 고객은 새 OAuth 서버 간 자격 증명을 사용하려면 클라이언트 애플리케이션을 업데이트해야 합니다. <ul><li>[서비스 계정(JWT) 자격 증명에서 마이그레이션](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[OAuth를 사용한 신규 및 기존 애플리케이션 구현 안내서](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[새 OAuth 서버 간 자격 증명 사용](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[FAQ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |
| **Adobe Analytics API(버전 1.4)에 대한 EOL** | 2024년 7월 17일 | **2026년 8월 12일**&#x200B;에 다음과 같은 Analytics Legacy API 서비스가 종료되며 해당 서비스를 사용하여 빌드한 현재 모든 통합 기능은 더 이상 작동하지 않습니다.<ul><li>Adobe Analytics API (버전 1.4)</li><li>Adobe Analytics WSSE 인증</li></ul><p>Adobe Analytics API(버전 1.4)를 사용하는 통합은 [Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)로 마이그레이션되어야 하며 WSSE 통합은 [Adobe Developer Console](https://developer.adobe.com/console)의 OAuth 기반 인증 프로토콜로 마이그레이션되어야 합니다.</p><p>자주 묻는 질문에 대한 답변과 자세한 안내는 [Adobe Analytics 1.4 API EOL FAQ](/help/admin/c-admin-api/c-admin-14-api-eol.md)를 참조하시기 바랍니다.</p> |


## AppMeasurement

AppMeasurement 릴리스(버전 2.26.0)에 대한 최신 업데이트는 [JavaScript용 AppMeasurement 릴리스 정보](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html)를 참조하십시오.


## 관련 리소스

* [2024년 이전 릴리스 정보](/help/release-notes/2024.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [스트리밍 미디어 컬렉션 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트
