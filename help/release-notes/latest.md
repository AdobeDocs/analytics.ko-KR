---
title: 현재 Adobe Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: ebe6716a3dde89d7212385c25044fb533d7737c2
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 84%

---

# 최신 Adobe Analytics 릴리스 정보 (2025년 7월 릴리스)

**마지막 업데이트**: 2025년 7월 16일 목요일

이 릴리스 정보는 2025년 7월 7일부터 8월 15일까지의 릴리스 기간을 다룹니다. Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 새로운 기능 또는 개선 사항 {#features}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **알고리즘을 활용한 라이브 스트리밍 TNT 필드** | 라이브스트림은 기술이 계속 현대적이고 안정적으로 유지되도록 개선 작업을 진행하고 있습니다. 새로 고침의 일환으로 TNT 필드에 알고리즘이 있는 경우 TNT 필드를 Livestream 출력에 통합하기 시작합니다. 단, 여기에는 이전에 지원되었던 다음과 같은 요소만 포함됩니다. `campaignId`, `recipeId`, `trafficType`, `actionId` 및 `actionName`. 라이브 스트리밍의 전반적인 TNT 스키마는 변경되지 않습니다. |   | 2025년 7월 7일 |
| **고객 속성 UI에 대한 탐색이 업데이트되었습니다.** | 이제 Adobe Experience Cloud의 앱 선택기에서 고객 속성 사용자 인터페이스에 바로 액세스할 수 있습니다. | 2025년 7월 1일 수요일 | TBD |

## Adobe Analytics의 수정 사항

**Activity Map**: AN-360987
**Analysis Workspace**: AN-378094; AN-380979; AN-382908; AN-387652;
**분류**: AN-382412; AN-383157; AN-384616; AN-384803; AN-385933; AN-387320; AN-387351; AN-387832; AN-387833; AN-387839; AN-387915;
**데이터 수집**: AN-387661
**데이터 피드**: AN-375172; AN-384369; AN-387859; AN-387952; AN-388155;
**플랫폼**: AN-382813; AN-386627; AN-386815
**개인 정보**: AN-384390
**Report Builder**: AN-388035
**보고**: AN-380441
**예약된 보고서**: AN-378280; AN-378331
**세그먼트 비교**: AN-368766


## 서비스 종료(EOL) 알림 {#eol}

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **레거시 Report Builder** | 2025년 6월 18일 | 기존 Report Builder 추가 기능은 2026년 6월에 지원이 중단됩니다. 모든 사용자는 기존 통합 문서를 새로운 [Report Builder](https://experienceleague.adobe.com/ko/docs/analytics/analyze/report-builder/rb-overview)로 업그레이드해야 합니다. 새로운 Report Builder는 Adobe Analytics와 Customer Journey Analytics 고객 모두에게 제공됩니다. 이는 [거의 동일한 기능](https://experienceleague.adobe.com/ko/docs/analytics/analyze/report-builder/convert-workbooks#unsupported)과 더불어 여러 가지 편리하고 새로운 기능과 개선된 UI를 제공합니다. 업그레이드 프로세스를 용이하게 하기 위해 새로운 Report Builder에는 간편한 통합 문서 변환 기능이 포함되어 있습니다. 새로운 Report Builder는 Microsoft Store를 통해 다운로드할 수 있는 추가 기능으로만 제공됩니다. 대부분의 조직에서는 사용자에게 추가 기능을 제공하기 전에 내부 승인 절차를 거쳐야 합니다. 이 프로세스에 시간을 할애하고 지금부터 조직과 협력하여 EOL 날짜 전에 통합 문서를 업그레이드할 충분한 시간을 확보하십시오. |
| **레거시 도메인 또는 레거시 SSO를 통한 액세스** | 2025년 4월 10일 | Adobe는 보안을 강화하고 로그인 환경을 간소화하기 위해 사용자가 Adobe Analytics에 액세스하는 방식을 업데이트할 계획입니다. 이러한 업데이트의 일환으로 `my.omniture.com`을 비롯한 기존 도메인 또는 기존 SSO를 통한 액세스는 **2026년 1월 2일**&#x200B;부터 영구 중단됩니다. 이 날짜 이후에는 기존 로그인 자격 증명과 기존 SSO가 더 이상 작동하지 않습니다. 모든 사용자는 Adobe Experience Cloud ID를 사용하여 `experience.adobe.com`을 통해 로그인해야 합니다. Experience Cloud ID와 관련하여 도움이 필요한 경우, 조직의 Adobe Analytics 관리자 또는 [Adobe 고객 지원 센터](https://helpx.adobe.com/kr/contact.html)에 문의하십시오. |
| **Adobe Analytics API (버전 1.4)** | 2024년 7월 17일 | **2026년 8월 12일**&#x200B;에 다음과 같은 Analytics Legacy API 서비스가 종료되며 해당 서비스를 사용하여 빌드한 현재 모든 통합 기능은 더 이상 작동하지 않습니다.<ul><li>Adobe Analytics API (버전 1.4)</li><li>Adobe Analytics WSSE 인증</li></ul><p>Adobe Analytics API(버전 1.4)를 사용하는 통합은 [Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)로 마이그레이션되어야 하며 WSSE 통합은 [Adobe Developer Console](https://developer.adobe.com/console)의 OAuth 기반 인증 프로토콜로 마이그레이션되어야 합니다.</p><p>자주 묻는 질문에 대한 답변과 자세한 안내는 [Adobe Analytics 1.4 API EOL FAQ](/help/admin/c-admin-api/c-admin-14-api-eol.md)를 참조하십시오.</p> |


## AppMeasurement

AppMeasurement 릴리스에 대한 최신 업데이트는 [AppMeasurement 릴리스 정보](https://github.com/adobe/appmeasurement/releases)를 참조하십시오.


## 관련 리소스

* [2025년 이전 릴리스 정보](/help/release-notes/2025.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=ko)
* [스트리밍 미디어 컬렉션 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=ko)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트
