---
title: 현재 Adobe Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: f7d36ac8de37633ccbe725865dbaeecee532f47e
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 72%

---

# 최신 Adobe Analytics 릴리스 정보 (2024년 8월)

**마지막 업데이트**: 2024년 8월 14일 목요일

이 릴리스 노트는 2024년 8월 14일부터 2024년 9월까지의 릴리스 기간을 다룹니다. Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 새로운 기능 또는 개선 사항 {#features}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **링크 추적을 위한 Web SDK 개선 사항** | Web SDK 최신 버전에서는 링크 추적을 중심으로 여러 가지 주목할 만한 개선 사항이 적용되었으며 이는 Activity Map 활용에 직접적인 이점을 제공합니다. 이 새로운 기능들은 Web SDK JavaScript 라이브러리와 Web SDK 태그 확장 기능 모두에서 사용할 수 있습니다.<ul><li>이벤트 그룹화: 방문자가 내부 링크를 클릭하면 링크 추적을 위한 별도 이벤트 호출을 트리거하는 대신 다음 페이지에서 이벤트 데이터를 그룹화하도록 선택할 수 있습니다. 이 개선 사항은 Web SDK가 계약상 한계 대비 적은 이벤트 수를 사용하도록 해 줍니다.</li><li>필터 클릭 속성: `OnBeforeLinkClickSend`를 대체하는 새로운 콜백입니다. 이 콜백을 사용하면 링크 관련 데이터를 Adobe로 전송하기 전에 필터링하거나 난독화할 수 있습니다.</li></ul><p>자세한 내용은 Web SDK 사용 안내서에서 [clickCollection](https://experienceleague.adobe.com/ko/docs/experience-platform/web-sdk/commands/configure/clickcollection)을 참조하십시오.</p> | 2024년 7월 10일 오픈 베타 시작 | 2024년 7월 18일 금요일 |

{style="table-layout:auto"}

## Adobe Analytics의 수정 사항

* Workspace에 알 수 없는 값이 여러 개 표시되던 문제가 해결되었습니다(AN-353632).
* Admin Console에서 새 고객 또는 새 Analytics 제품 프로필을 추가한 후 알림 이메일이 전송되지 않는 문제를 해결했습니다(AN-350930)

### 기타 Analytics 수정 사항

AN-354361, AN-354248, AN-354211, AN-354324, AN-351532, AN-349808, AN-347831, AN-353777, AN-354092, AN-354064, AN-354202, AN-354006, 354097, AN-352548, AN-353819, AN-353818, AN-353628, AN-353747, AN-353527, AN-353490, AN-352647, AN-352656, AN-351274, AN-352135, AN-351519, AN-344906, 353697, AN-354499, AN-354402, AN-354062, AN-353905, AN-353932, AN-354142, AN-354194, AN-354182, AN-353758, AN-353039, AN-353612, AN-350799, AN-354414, AN-354636, AN-354249, AN-353637, AN-350949, AN-349402, AN-355103, AN-354174, AN-353823, AN-354819, AN-354215, AN-354219, AN-354040, AN-354763, AN-354597, AN-354478, AN-354528, AN-354335, AN-

## Adobe Analytics 관리자에 대한 중요 공지 {#admin}

| 공지 | 추가 또는 업데이트 일자 | 설명 |
| ----------- | ---------- | ---------- |
| **저장된 기간이 13개월 만료됨:`cust_visids`** | 2024년 8월 20일 수요일 | Analytics 히트 처리 엔진 릴리스의 **2024년 8월 20일**&#x200B;은(는) 저장된 `cust_visids`의 13개월 만료 기간을 적용합니다. 보고서 세트에 “방문자 결합 활성화”가 활성화된 경우 이 설정은 히트에 `cust_visid`가 없는 `visid_high/visid_low value`에 대해 `cust_visid`를 찾는 데 사용됩니다. 이전에는 `visid_high/visid_low`에 대한 `cust_visid`의 매핑이 만료되지 않았습니다. 이 릴리스에서는 `visid_high/visid_low`가 `cust_visid`를 히트시킨 후 13개월 이상 경과한 경우 매핑이 만료됩니다. |

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
