---
title: 현재 Adobe Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 66c846dd64ee3ed8f421c834ab82b53b1f0f00a5
workflow-type: tm+mt
source-wordcount: '1139'
ht-degree: 84%

---

# 최신 Adobe Analytics 릴리스 정보(2024년 5월)

**마지막 업데이트**: 2024년 5월 21일 수요일

이번 릴리스 정보에는 2024년 5월 15일부터 6월까지의 릴리스 기간이 포함됩니다. Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 새로운 기능 또는 개선 사항 {#features}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Adobe Analytics에서 Customer Journey Analytics로 업그레이드에 대한 새로운 설명서** | Adobe Analytics에서 Customer Journey Analytics로 업그레이드하는 조직의 경우 조직의 현재 Adobe Analytics 구현 및 장기 목표를 기반으로 염두에 두어야 할 다양한 업그레이드 옵션 등 고려 사항이 많습니다. 이제 새로운 문서 리소스를 통해 다음 내용을 더 효과적으로 이해할 수 있습니다.<ul><li>존재하는 다양한 업그레이드 경로</li><li>조직의 현재 Adobe Analytics 구현에 따라 사용 가능한 업그레이드 경로</li><li>각 업그레이드 경로의 장점과 단점</li><li>각 업그레이드 경로에 대한 단계별 지침</li><li>내역 데이터 처리 시 고려 사항</li></ul>[Customer Journey Analytics로 업그레이드 시작하기](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/upgrade-to-cja/cja-upgrade-getstarted) | | 지금 사용 가능 |
| **XDM을 통해 `contextData` 필드 설정** | Experience Edge Network를 통해 Adobe Analytics로 데이터를 보내는 고객은 XDM 또는 페이로드의 “데이터” 부분에서 직접 [컨텍스트 데이터 값을 설정](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/page-vars/contextdata)할 수 있습니다. |  | 지금 사용 가능 |
| **Analytics 실시간 보고 2.0 API** | Adobe Analytics의 새로운 실시간 보고 API 2.0은 고객 통합을 개선하고 신속한 보고 결과를 제공합니다. 기본 보고서, 추세 보고서, 분류 보고서 작업에 이러한 결과를 프로그래밍 방식으로 사용할 수 있습니다. [자세히 알아보기](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/reports/real-time/) | | 2024년 5월 30일 |
| **스트리밍 미디어: Web SDK를 통해 웹 데이터를 Adobe Experience Platform Edge Network로 보내기** | 이제 Adobe Experience Platform Web SDK를 사용하여 스트리밍 미디어 웹 데이터를 Adobe Experience Platform Edge Network로 보낼 수 있습니다. 이 개선 사항을 통해 보다 개인화된 캠페인을 빌드하고 더욱 개인화된 콘텐츠를 제공할 수 있으므로 더 많은 추적 데이터를 보고할 수 있게 됩니다.<p>이러한 변경은 Customer Journey Analytics, Adobe Real-time CDP, Adobe Journey Optimizer 및 이벤트 전달과 같은 모든 Platform 솔루션 전반에 걸쳐 웹 구현을 위한 통합 수집 방법을 제공합니다. 이전까지 스트리밍 미디어 웹 데이터를 Edge Network로 보내는 유일한 방법은 Media Edge API를 사용하는 것이었습니다. [자세히 알아보기] | | 2024년 5월 31일 |
| **기본적으로 낮은 트래픽 임계값 증가** | **2024년 4월 중반**&#x200B;에 Adobe는 기본 보고서 세트 ![낮은 트래픽 임계값](assets/thresholds.png)을 높일 예정입니다. 이는 현재 새 임계값 아래로 설정된 변수에만 영향을 줍니다. 해당 변경 사항은 점진적으로 적용되고, 작업은 **5월 말**&#x200B;에 완료될 예정입니다. 이 증가분이 롤아웃되면 카디널리티가 높은 변수에 대해 변경 사항이 발생할 수 있습니다.<ul><li>추가 차원 값이 보고에 사용할 수 있습니다.</li><li>세그먼트와 계산된 지표에는 추가 데이터가 포함될 수 있습니다.</li><li>세그먼트 기반 가상 보고서 세트에는 추가 데이터가 포함될 수 있습니다.</li><li>분류 내보내기에는 추가 데이터가 포함될 수 있습니다.</li></ul> | 2024년 4월 중반 | 2024년 5월 31일 |
| **내보내기 및 가져오기에 사용되는 계정 및 위치를 제어하는 관리자 설정** | 위치 관리자의 새로운 &quot;관리자 설정&quot; 탭은 사용자가 계정 및 위치를 만들고 편집할 수 있는지 여부를 관리자가 제어할 수 있도록 해줍니다. 이러한 설정은 사용자가 클라우드 가져오기 및 내보내기 계정을 구성하고 클라우드 가져오기 및 내보내기 위치를 구성할 때 적용됩니다. <p>관리자는 사용자가 만들고 사용할 수 있는 계정 유형(Google Cloud Platform, Azure RBAC, Amazon S3 등)을 제한할 수도 있습니다.</p><p>이전에는 모든 사용자가 모든 유형의 계정에 대해 계정과 위치를 만들고, 편집하고, 사용할 수 있었습니다.</p> | 2024년 6월 | 2024년 6월 |
| **내보내기 및 가져오기에 사용되는 계정 및 위치 공유** | 이제 사용자는 자신이 만든 계정과 위치를 조직의 모든 사용자가 사용할 수 있도록 할 수 있습니다. 계정 및 위치 소유자와 시스템 관리자만 계정 및 위치를 편집하고 삭제할 수 있습니다.<p>이전에는 계정 및 위치를 만든 사용자만 사용할 수 있었습니다.</p><p>이러한 설정은 사용자가 사용할 수 있습니다 [클라우드 가져오기 및 내보내기 계정 구성](/help/components/locations/configure-import-accounts.md) 및 [클라우드 가져오기 및 내보내기 위치 구성](/help/components/locations/configure-import-locations.md). </p> | 2024년 6월 | 2024년 6월 |
| **Activity Map에서 Web SDK에 대해 더 적은 서버 호출 사용** | 현재 Activity Map 링크 이벤트는 자체 이벤트로 계산되어 추가 비용이 발생합니다. 이 향상된 기능을 통해 일부 링크 이벤트를 가져와 다음 히트로 패키지화합니다. 이는 AppMeasurement에서 이벤트를 처리하는 방법과 유사합니다. (참조할 설명서) | Beta 시작일: 2024년 5월 31일 | TBD |

{style="table-layout:auto"}

## Adobe Analytics의 수정 사항

* 다음 분류 문제가 수정되었습니다. AN-343186; AN-344711; AN-344856; AN-345094; AN-345179; AN-346265; AN-345288; AN-346339; AN-346560; AN-347572; AN-347681; AN-347768; AN-348024
* 다음 Data Warehouse 문제가 수정되었습니다. AN-346789; AN-347031; AN-347568;
* 다음 데이터 피드 문제가 수정되었습니다. AN-343616, AN-345831, AN-345988, AN-346124, AN-346232, AN-346972, AN-347680, AN-347755, AN-347954
* 다음 데이터 소스 문제가 수정되었습니다. AN-347890,
* 다음 Analysis Workspace 문제가 수정되었습니다. AN-321503, AN-343103, AN-343471, AN-345171, AN-345223, AN-345912, AN-346026, AN-346330, AN-346839, AN-347679
* 다음 A4T 문제가 해결되었습니다. AN-345118,

### 기타 Analytics 수정 사항

AN-327749, AN-332949, AN-342881, AN-343171, AN-343708, AN-344034, AN-345559, AN-346023, AN-346230, AN-346330, AN-346469, AN-346606, AN-346750, AN-346973, AN-347026, AN-347110, AN-347439

## Adobe Analytics 관리자에 대한 중요 공지 {#admin}

| 공지 | 추가 또는 업데이트 일자 | 설명 |
| ----------- | ---------- | ---------- |
| **ISO 지역 업데이트** | 2024년 5월 10일 | Adobe는 2024년 6월 7일에 2024 ISO 지역 업데이트를 수행합니다. 이 릴리스 이후에 부분적인 지역 정보(지역) 업데이트가 있을 것으로 예상됩니다. |
| **저장된 기간이 13개월 만료됨:`cust_visids`** | 2024년 3월 20일 | 4월 또는 5월을 목표로 하는 Analytics Hit 처리 엔진의 향후 릴리스에서는 저장된 `cust_visids`의 만료 기간을 13개월로 적용할 예정입니다. 보고서 세트에 “방문자 결합 활성화”가 활성화된 경우 이 설정은 히트에 `cust_visid`가 없는 `visid_high/visid_low value`에 대해 `cust_visid`를 찾는 데 사용됩니다. 현재는 `visid_high/visid_low`에 대한 `cust_visid`의 매핑 만료가 없습니다. 이 릴리스에서는 `visid_high/visid_low`가 `cust_visid`를 히트시킨 후 13개월 이상 경과한 경우 매핑이 만료됩니다. |

{style="table-layout:auto"}

## 서비스 종료(EOL) 알림 {#eol}

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션** | 2023년 5월 11일 | Adobe I/O JWT 자격 증명을 사용하는 Adobe Analytics API 및 Livestream 고객은 **2025년 1월 1일**&#x200B;까지 Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 2024년 5월 1일부터는 Adobe I/O를 사용하여 새 JWT 자격 증명을 만들 수 없습니다. JWT를 사용하는 고객은 OAuth 서버 간 자격 증명을 새로 만들거나 기존 JWT 자격 증명을 OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 또한 고객은 새 OAuth 서버 간 자격 증명을 사용하려면 클라이언트 애플리케이션을 업데이트해야 합니다. <ul><li>[서비스 계정(JWT) 자격 증명에서 마이그레이션](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[OAuth를 사용한 신규 및 기존 애플리케이션 구현 안내서](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[새 OAuth 서버 간 자격 증명 사용](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[FAQ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |

{style="table-layout:auto"}

## AppMeasurement

AppMeasurement 릴리스(버전 2.26.0)에 대한 최신 업데이트는 [JavaScript용 AppMeasurement 릴리스 정보](https://experienceleague.adobe.com/ko/docs/analytics/implementation/appmeasurement-updates.html?lang=ko-KR)를 참조하십시오.


## 관련 리소스

* [2023년 이전 릴리스 정보](/help/release-notes/2023.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/releases/latest.html?lang=ko-KR)
* [Media Analytics 릴리스 정보](https://experienceleague.adobe.com/ko/docs/media-analytics/using/additional-resources/release-notes.html?lang=ko-KR)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트
