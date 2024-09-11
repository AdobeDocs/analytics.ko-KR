---
title: 현재 Adobe Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: a74d47cf99545305c9b7d99d934dfedafdd9233b
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 56%

---

# 최신 Adobe Analytics 릴리스 정보 (2024년 9월)


**마지막 업데이트**: 2024년 9월 11일 목요일

이 릴리스 노트는 2024년 9월 11일부터 10월 초까지의 릴리스 기간을 다룹니다. Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 새로운 기능 또는 개선 사항 {#features}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
|--- | --- | --- | --- |
| **계산된 지표 관리자 및 세그먼트 관리자의 &quot;사용 위치&quot; 열에 있는 추가 정보** | 계산된 지표 관리자 및 세그먼트 관리자의 &quot;사용 위치&quot; 열에는 다음과 같은 새 보고 영역이 포함됩니다.<ul><li>**Report Builder**: Report Builder에서 사용 중인 계산된 지표 또는 세그먼트의 수를 표시합니다.</li><li>**Ad Hoc 구성 요소**: 프로젝트에서 사용 중인 Ad Hoc 계산된 지표 또는 Ad Hoc 세그먼트의 수를 표시합니다. 이러한 애드혹 계산된 지표 및 세그먼트(또는 &quot;빠른 계산된 지표&quot; 및 &quot;빠른 세그먼트&quot;라고도 함)는 해당 지표가 생성된 프로젝트에서만 사용할 수 있으므로 &quot;사용됨&quot; 열의 &quot;프로젝트&quot; 보고 영역과 별도로 보고됩니다.</li></ul> |  | 2024년 9월 11일 |
| **Activity Map v3 확장** | 이제 Activity Map v3 확장을 사용할 수 있습니다. v2 확장이 설치되어 있는 경우 v3 확장을 설치하기 전에 제거합니다. 최신 버전의 확장을 얻으려면 **[!UICONTROL 도구]** > **[!UICONTROL Activity Map]**(으)로 이동합니다. |  | 2024년 9월 3일 |


## Adobe Analytics의 수정 사항

A4T: AN-355736
Activity Map: AN-353779
Analysis Workspace: AN-348485; AN-349693; AN-357247
Analytics 모바일 앱: AN-352645
분류: AN-355636; AN-355651; AN-355753; AN-356005; AN-356439; AN-356540; AN-356577; AN-356622
크로스 디바이스 분석: AN-355138
데이터 피드: AN-356258; AN-357133
Data Warehouse: AN-339292; AN-353807
내보내기 위치: AN-356912
개인 정보 API: AN-352420
Report Builder: AN-352555; AN-354316
예약된 프로젝트: AN-355971
세그멘테이션: AN-352095;
Target 보고: AN-355748

기타 수정 사항: AN-349698; AN-349880; AN-354860; AN-355355; AN-356289;

## Adobe Analytics 관리자에 대한 중요 공지 {#admin}

| 공지 | 추가 또는 업데이트 일자 | 설명 |
| ----------- | ---------- | ---------- |
| **저장된 기간이 13개월 만료됨:`cust_visids`** | 2024년 8월 20일 | **2024년 8월 20일** Analytics Hit 처리 엔진의 릴리스에서는 저장된 `cust_visids`의 만료 기간을 13개월로 적용할 예정입니다. 보고서 세트에 “방문자 결합 활성화”가 활성화된 경우 이 설정은 히트에 `cust_visid`가 없는 `visid_high/visid_low value`에 대해 `cust_visid`를 찾는 데 사용됩니다. 이전에는 `visid_high/visid_low`에 대한 `cust_visid`의 매핑 만료가 없었습니다. 이 릴리스에서는 `visid_high/visid_low`가 `cust_visid`를 히트시킨 후 13개월 이상 경과한 경우 매핑이 만료됩니다. |
| **추가 구현 세부 XDM 필드가 자동으로 매핑됨** | 2024년 9월 11일 목요일 | Adobe Experience Platform Edge Network을 사용하여 데이터를 Adobe Analytics으로 보낼 때 XDM 필드 `xdm.implementationdetails.name` 및 `xdm.implementationdetails.environment`은(는) 이제 항상 컨텍스트 데이터 변수 `c.a.x.implementationdetails.name` 및 `c.a.x.implementationdetails.environment`에 매핑됩니다. 이전에는 일부 시나리오에서 이러한 값을 채우지 못했습니다. 이러한 값의 가용성을 수용하도록 관련 처리 규칙을 조정하십시오. |

{style="table-layout:auto"}

## 서비스 종료(EOL) 알림 {#eol}

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **Adobe Analytics API(버전 1.4)에 대한 EOL** | 2024년 7월 17일 | **2026년 8월 12일**&#x200B;에 다음과 같은 Analytics Legacy API 서비스가 종료되며 해당 서비스를 사용하여 구축한 현재 모든 통합은 더 이상 작동하지 않습니다.<ul><li>Adobe Analytics API(버전 1.4)</li><li>Adobe Analytics WSSE 인증</li></ul><p>Adobe Analytics API(버전 1.4)를 사용하는 통합은 [Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)로 마이그레이션되어야 하며 WSSE 통합은 [Adobe Developer Console](https://developer.adobe.com/console)의 OAuth 기반 인증 프로토콜로 마이그레이션되어야 합니다.</p><p>자주 묻는 질문에 대한 답변과 자세한 안내는 [Adobe Analytics 1.4 API EOL FAQ](/help/admin/c-admin-api/c-admin-14-api-eol.md)를 참조하시기 바랍니다.</p> |
| **Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션** | 2023년 5월 11일 | Adobe I/O JWT 자격 증명을 사용하는 Adobe Analytics API 및 Livestream 고객은 **2025년 1월 1일**&#x200B;까지 Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 2024년 5월 1일부터는 Adobe I/O를 사용하여 새 JWT 자격 증명을 만들 수 없습니다. JWT를 사용하는 고객은 OAuth 서버 간 자격 증명을 새로 만들거나 기존 JWT 자격 증명을 OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 또한 고객은 새 OAuth 서버 간 자격 증명을 사용하려면 클라이언트 애플리케이션을 업데이트해야 합니다. <ul><li>[서비스 계정(JWT) 자격 증명에서 마이그레이션](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[OAuth를 사용한 신규 및 기존 애플리케이션 구현 안내서](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[새 OAuth 서버 간 자격 증명 사용](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[FAQ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |

{style="table-layout:auto"}

## AppMeasurement

AppMeasurement 릴리스(버전 2.26.0)에 대한 최신 업데이트는 [JavaScript용 AppMeasurement 릴리스 정보](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=ko-KR)를 참조하십시오.


## 관련 리소스

* [2024년 이전 릴리스 정보](/help/release-notes/2024.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=ko-KR)
* [스트리밍 미디어 컬렉션 추가 기능 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=ko-KR)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트
