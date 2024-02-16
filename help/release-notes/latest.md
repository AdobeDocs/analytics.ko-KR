---
title: 현재 Adobe Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: e9abbc03cf01abecab4ea0627624b5272b503d5c
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 41%

---

# 현재 Adobe Analytics 릴리스 정보 (2024년 2월)

**마지막 업데이트**: 2024년 2월 16일 토요일

이 릴리스 정보는 2024년 2월 14일부터 2024년 3월 11일까지의 릴리스 기간을 다룹니다. Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 새로운 기능 또는 개선 사항 {#features}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **추가 비용 없이 웹 SDK용 Activity Map** | 현재 Activity Map 링크 이벤트는 자체 이벤트로 계산되며 추가 비용이 발생합니다. 이 개선 사항은 AppMeasurement에서 이벤트를 처리하는 방법과 유사하게 일부 링크 이벤트를 가져와서 다음 히트로 패키지화합니다. |  | 2024년 3월 6일 목요일 |
| **기본 낮은 트래픽 임계값 증가** | 위치 **2024년 4월 중순**, Adobe은 다음과 같이 기본 보고서 세트의 낮은 트래픽 임계값 증가를 시작합니다. ![낮은 트래픽 임계값](assets/thresholds.png) 이 경우 현재 새 임계값 이하로 설정된 변수에만 영향을 줍니다. 이러한 변경은 점진적으로 이루어질 것이며, 우리는 작업에 의해 완성될 것으로 기대한다. **5월 말**. 이러한 증가분이 롤아웃되면 카디널리티가 높은 변수에 대한 변경 사항이 표시될 수 있습니다.<ul><li>보고에 더 많은 차원 값을 사용할 수 있습니다.</li><li>세그먼트 및 계산된 지표에 더 많은 데이터가 포함될 수 있습니다.</li><li>세그먼트를 기반으로 하는 가상 보고서 세트는 더 많은 데이터를 포함할 수 있습니다.</li><li>분류 내보내기에 더 많은 데이터가 포함될 수 있습니다.</li></ul> | 2024년 4월 중순 | 2024년 5월 말 |

{style="table-layout:auto"}

## Adobe Analytics의 수정 사항

* AN-319515, AN-337559, AN-338149, AN-338702, AN-338769, AN-338891, AN-339327, AN-339649, AN-339668, AN-339669, AN-339776, AN-339822, AN-340017, AN-340202, AN-340476,
* AN-338385; AN-338399; AN-338592; AN-338810; AN-338893; AN-339431; AN-339894; AN-339933; AN-340201; AN-340309; 분류 규칙 빌더 문제를 수정했습니다.
* A4T 문제인 AN-334830; AN-336194; AN-338309; AN-338650;
* 다음 데이터 수집 문제를 해결했습니다. AN-339323
* AN-335542; AN-331425; AN-337215; AN-338445; AN-338643; AN-338651; AN-339461; AN-340066; AN-340207; AN-340460 Data Warehouse 문제가 수정되었습니다.
* AN-335952; AN-338653; AN-339508; AN-339681; AN-340418 데이터 피드 문제가 해결되었습니다.
* 다음 데이터 소스 문제가 해결되었습니다. AN-338648
* Analysis Workspace 문제: AN-326509; AN-336186; AN-336190; AN-336309; AN-337922; AN-338094; AN-338323; AN-338556; AN-339600; AN-340445이 수정되었습니다.

### 기타 Analytics 수정 사항

AN-328239, AN-332908, AN-335449, AN-335517, AN-336075, AN-336100, AN-336128, AN-338088, AN-338270, AN-338393, AN-338494, AN-339326, AN-339742, AN-339883, AN-340419,

## Adobe Analytics 관리자에 대한 중요 공지 {#admin}

| 공지 | 추가 또는 업데이트 일자 | 설명 |
| ----------- | ---------- | ---------- |
| Adobe API 오브젝트 멤버 추가 | 2024년 1월 17일 | Adobe은 언제든지 버전 관리에 대한 통지 또는 변경 없이 선택적 요청 및 응답 멤버(이름/값 쌍)를 기존 API 객체에 추가할 수 있습니다. Adobe은 API와 통합하는 모든 서드파티 도구의 API 설명서 를 참조하도록 권장하므로 이해되지 않는 경우 처리에서 이러한 추가 사항이 무시됩니다. 제대로 구현된 경우 이러한 추가 사항은 구현에 대한 끊김 없는 변경 사항입니다. Adobe는 릴리스 정보를 통해 표준 알림을 제공하지 않고 매개변수를 제거하거나 필수 매개변수를 추가하지 않습니다. |
| `getPageLoadTime` 플러그인 사용 안 함 | 2024년 1월 10일 | 이 플러그인은 더 이상 지원되지 않습니다. 해당 코드는 MDN에 따라 [더 이상 사용되지 않는](https://developer.mozilla.org/en-US/docs/Web/API/PerformanceTiming) performance.timing 메서드를 활용합니다. 업데이트된 플러그인 작업이 시작되었습니다. |

{style="table-layout:auto"}

## 서비스 종료(EOL) 알림 {#eol}

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션** | 2023년 5월 11일 | Adobe I/O JWT 자격 증명을 사용하는 Adobe Analytics API 및 Livestream 고객은 **2025년 1월 1일**&#x200B;까지 Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 2024년 5월 1일부터는 Adobe I/O를 사용하여 새 JWT 자격 증명을 만들 수 없습니다. JWT를 사용하는 고객은 OAuth 서버 간 자격 증명을 새로 만들거나 기존 JWT 자격 증명을 OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 또한 고객은 새 OAuth 서버 간 자격 증명을 사용하려면 클라이언트 애플리케이션을 업데이트해야 합니다. <ul><li>[서비스 계정(JWT) 자격 증명에서 마이그레이션](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[OAuth를 사용한 신규 및 기존 애플리케이션 구현 안내서](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[새 OAuth 서버 간 자격 증명 사용](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[FAQ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |

{style="table-layout:auto"}

## AppMeasurement

AppMeasurement 릴리스(버전 2.25.0)에 대한 최신 업데이트는 [JavaScript용 AppMeasurement 릴리스 정보](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html)를 참조하십시오.


## 관련 리소스

* [2023년 이전 릴리스 정보](/help/release-notes/2023.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [Media Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트
