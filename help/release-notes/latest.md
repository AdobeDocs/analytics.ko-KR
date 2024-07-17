---
title: 현재 Adobe Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: cb0eab15dac6d679e9f912010045e6be2e47df4a
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 45%

---

# 최신 Adobe Analytics 릴리스 정보 (2024년 7월)

**마지막 업데이트**: 2024년 7월 17일 목요일

이 릴리스 정보는 2024년 7월 17일부터 2024년 8월의 릴리스 기간을 다룹니다. Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 새로운 기능 또는 개선 사항 {#features}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **링크 추적을 위한 Web SDK 개선** | 링크 추적에 대한 최신 버전의 웹 SDK에서는 몇 가지 주목할 만한 개선 사항을 사용할 수 있으며, 이는 Activity Map에 직접적인 도움이 됩니다. 이러한 새로운 기능은 Web SDK JavaScript 라이브러리와 Web SDK 태그 확장 모두에서 사용할 수 있습니다.<ul><li>이벤트 그룹화: 방문자가 내부 링크를 클릭할 때 링크 추적을 위해 별도의 이벤트 호출을 트리거하는 대신 다음 페이지에서 이벤트 데이터를 그룹화하도록 선택할 수 있습니다. 이 개선 사항은 웹 SDK가 계약 제한에 대해 사용하는 이벤트 수를 줄입니다.</li><li>필터 클릭 속성: `OnBeforeLinkClickSend`을(를) 대체하는 새 콜백입니다. 이 콜백을 사용하여 링크 관련 데이터를 Adobe으로 보내기 전에 필터링하거나 난독화할 수 있습니다.</li></ul><p>자세한 내용은 Web SDK 사용 안내서의 [clickCollection](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/clickcollection)을 참조하십시오.</p> | Beta 열기 (2024년 7월 10일 시작) | TBD |

{style="table-layout:auto"}

## Adobe Analytics의 수정 사항

* 사용자가 Analytics UI에 로그인할 수 없는 문제가 해결되었습니다(AN-352953).
* 사용자가 Analytics 모바일 앱에 로그인할 수 없는 문제가 해결되었습니다(AN-352463).
* 프로젝트를 PDF으로 다운로드할 수 없는 문제를 해결했습니다(AN-352680).
* 분류를 가져오지 않는 문제가 해결되었습니다(AN-352178).

### 기타 Analytics 수정 사항

AN-352905; AN-352902; AN-352693; AN-352659; AN-352619;
AN-352577, AN-352575, AN-352572, AN-352571, AN-352549, AN-352501, AN-352499, AN-352478, AN-352466, AN-352437, AN-352378, AN-352355, 352341, AN-352318, AN-352297, AN-352272, AN-352267, AN-352263, AN-352088, AN-352019, AN-352018, AN-351978, AN-351908, AN-351809, AN-351750, AN-351689, 351624, AN-351564, AN-351524, AN-351507, AN-351416, AN-351414, AN-351405, AN-351299, AN-351283, AN-351231, AN-350710, AN-349912, AN-349786, AN-348300, AN-348061, AN-347865, AN-347676, AN-347478, AN-343611, AN-343114, AN-334124, AN-, AN-, AN-

## Adobe Analytics 관리자에 대한 중요 공지 {#admin}

| 공지 | 추가 또는 업데이트 일자 | 설명 |
| ----------- | ---------- | ---------- |
| **저장된 기간이 13개월 만료됨:`cust_visids`** | 2024년 5월 22일 | **2024년 7월로 예정**&#x200B;된 Analytics Hit 처리 엔진의 향후 릴리스에서는 저장된 `cust_visids`의 만료 기간을 13개월로 적용할 예정입니다. 보고서 세트에 “방문자 결합 활성화”가 활성화된 경우 이 설정은 히트에 `cust_visid`가 없는 `visid_high/visid_low value`에 대해 `cust_visid`를 찾는 데 사용됩니다. 현재는 `visid_high/visid_low`에 대한 `cust_visid`의 매핑 만료가 없습니다. 이 릴리스에서는 `visid_high/visid_low`가 `cust_visid`를 히트시킨 후 13개월 이상 경과한 경우 매핑이 만료됩니다. |

{style="table-layout:auto"}

## 서비스 종료(EOL) 알림 {#eol}

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **Adobe Analytics API용 EOL(버전 1.4)** | 2024년 7월 17일 목요일 | **2026년 8월 12일**&#x200B;에 다음 Analytics Legacy API 서비스가 사용 수명 종료에 도달하여 중단되며, 이러한 서비스를 사용하여 빌드된 현재 통합은 작동하지 않습니다.<ul><li>Adobe Analytics API(버전 1.4)</li><li>Adobe Analytics WSSE 인증</li></ul><p>Adobe Analytics API(버전 1.4)를 사용하는 통합은 [Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)(으)로 마이그레이션해야 하지만 WSSE 통합은 [Adobe Developer Console](https://developer.adobe.com/console)의 OAuth 기반 인증 프로토콜로 마이그레이션해야 합니다.</p><p>일반적인 질문 및 추가 지침에 대한 답변은 [Adobe Analytics 1.4 API EOL FAQ](/help/admin/c-admin-api/c-admin-14-api-eol.md)를 참조하십시오.</p> |
| **Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션** | 2023년 5월 11일 | Adobe I/O JWT 자격 증명을 사용하는 Adobe Analytics API 및 Livestream 고객은 **2025년 1월 1일**&#x200B;까지 Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 2024년 5월 1일부터는 Adobe I/O를 사용하여 새 JWT 자격 증명을 만들 수 없습니다. JWT를 사용하는 고객은 OAuth 서버 간 자격 증명을 새로 만들거나 기존 JWT 자격 증명을 OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 또한 고객은 새 OAuth 서버 간 자격 증명을 사용하려면 클라이언트 애플리케이션을 업데이트해야 합니다. <ul><li>[서비스 계정(JWT) 자격 증명에서 마이그레이션](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[OAuth를 사용한 신규 및 기존 애플리케이션 구현 안내서](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[새 OAuth 서버 간 자격 증명 사용](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[FAQ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |

{style="table-layout:auto"}

## AppMeasurement

AppMeasurement 릴리스(버전 2.26.0)에 대한 최신 업데이트는 [JavaScript용 AppMeasurement 릴리스 정보](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=ko-KR)를 참조하십시오.


## 관련 리소스

* [2024년 이전 릴리스 정보](/help/release-notes/2024.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=ko-KR)
* [스트리밍 미디어 컬렉션 추가 기능 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=ko-KR)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트
