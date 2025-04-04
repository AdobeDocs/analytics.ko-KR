---
title: 현재 Adobe Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: bf6a811aac7d881517944c8308fd97e719791cc0
workflow-type: tm+mt
source-wordcount: '980'
ht-degree: 61%

---

# 최신 Adobe Analytics 릴리스 정보 (2025년 3월 릴리스)

**마지막 업데이트**: 2025년 4월 4일 토요일

이번 릴리스 정보에는 2025년 3월 5일부터 5월까지의 릴리스 기간이 포함됩니다. Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 새로운 기능 또는 개선 사항 {#features}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Analytics 인벤토리** | Analytics 인벤토리는 프로젝트 및 구성 요소 수, 보고서 세트, 사용자 등을 포함하여 Adobe Analytics 환경에 대한 포괄적인 개요를 제공합니다. 인벤토리 프로세스를 자동화하면 Adobe Analytics에서 Customer Journey Analytics으로 전환하는 데 필요한 노력을 신속하게 이해할 수 있습니다. 이렇게 하면 전환이 더 쉽고 빨라집니다. [자세히 알아보기](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/analytics-inventory) |  | 2025년 3월 26일 |
| **Analytics 컨텍스트 데이터 필드 업데이트`a.locale`** | 해당 업데이트 이후 Experience Edge를 통해 데이터를 수집할 때 Analytics 컨텍스트 데이터 필드 `a.locale`이 설정되는 방식이 변경됩니다. Experience Edge를 사용하여 Adobe Analytics로 데이터를 전송하면 XDM 필드의 매핑을 기반으로 Analytics 필드가 채워집니다. `c.a.locale`에 대한 매핑은 비표준 XDM 필드인 `xdm.environment.language`를 참조합니다. 이 필드는 올바른 필드 `xdm.environment._dc.language`를 참조하도록 업데이트됩니다.<p>해당 매핑은 이전 버전과의 호환성을 유지하기 위해 `xdm.environment.language`를 계속 참조합니다. 연속성을 위해 두 필드가 모두 설정된 경우 `xdm.environment.language`가 우선 적용됩니다. XDM에서 표준 Analytics 필드로 매핑되는 전체 목록은 [여기](https://experienceleague.adobe.com/ko/docs/analytics/implementation/aep-edge/xdm-var-mapping)에서 확인할 수 있습니다. | | 2025년 3월 5일 |
| **Customer Journey Analytics 업그레이드 안내서** | Adobe Analytics에서 Customer Journey Analytics로 업그레이드하기 위한 단계별 안내서를 생성할 수 있습니다. 이 안내서는 귀하의 조직에 맞게 작성되었으며, 현재 Adobe Analytics 환경, Customer Journey Analytics에 대해 의도된 용도, 그리고 시간 절약을 위한 타협을 고려합니다.<p>사용자 정의 안내서 생성을 시작하려면 [!DNL Customer Journey Analytics]에 로그인한 다음 **[!UICONTROL 작업 영역]** 탭에서 **[!UICONTROL Customer Journey Analytics로 업그레이드]**&#x200B;를 선택합니다.<p>[자세히 알아보기](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/compare-aa-cja/upgrade-to-cja/cja-upgrade-recommendations#recommended-upgrade-steps-for-most-organizations) |  | 2025년 3월 11일 |
| **Data Warehouse 전용 차원** | 2025년 5월부터 Adobe은 특정 차원(eVar 및 prop과 같은 사용자 지정 변수)을 &#39;Data Warehouse 전용&#39;으로 설정할 예정입니다. 이는 다음 특성을 나타내는 차원에 적용됩니다.<ul><li> 여러 달의 기간 동안 변수는 그 달의 처음 며칠 내에 낮은 트래픽 제한에 도달합니다.</li><li>전달된 값의 90% 이상이 한 달 동안 한 번만 표시됩니다.</li></ul>예를 들면 카디널리티가 매우 높고 거의 모든 히트(또는 방문 또는 방문자)에 대해 한 달 동안 고유한 새 값이 전달되는 타임스탬프, UUID 또는 기타 데이터가 포함된 차원이 포함됩니다. 이러한 차원은 일반적으로 낮은 트래픽 제한을 매우 빨리 초과하며 Analysis Workspace에서 매우 작은 부분만 보고할 수 있습니다. 이렇게 하면 유용하거나 정확한 정보를 표시하지 않으므로 이러한 차원을 활용하는 보고서를 헷갈리게 합니다. 이러한 차원은 차원이 해당 달 동안 낮은 트래픽 제한을 초과한 후 &#39;자주&#39; 사용되는 값에 대한 보고를 수행하는 방법을 제공하기 위한 낮은 트래픽 기능의 목적이나 이점을 따르지 않습니다. [자세히 알아보기](https://experienceleague.adobe.com/en/docs/analytics/technotes/low-traffic.)<p>&quot;Data Warehouse 전용&quot;으로 표시된 차원은 Analysis Workspace에서 보고할 수 없습니다. 하지만 낮은 트래픽 제한은 여기에 적용되지 않으므로 Data Warehouse을 통해 보고할 수 있습니다.<p>이는 낮은 트래픽 제한에 도달한 모든 차원이 &quot;Data Warehouse 전용&quot;으로 표시될 후보임을 의미하지는 않습니다. 낮은 트래픽 제한에 도달한 대부분의 차원은 실제로 낮은 트래픽 기능의 의도를 충족합니다.<ul><li>전달된 대부분의 값이 고유하지 않습니다.</li><li>해당 달 동안 낮은 트래픽 제한에 도달한 후에도 일반 값이 계속 표시됩니다.</li><li>새 &#39;인기&#39; 값은 계속 발생할 수 있습니다.</li></ul>전달된 거의 모든 값이 &quot;Data Warehouse 전용&quot;으로 표시되는 새롭고 고유한 차원입니다. 낮은 트래픽 제한을 늘리는 것은 이러한 상황에서 수집되는 데이터의 고유성을 고려할 때 해결책이 아닙니다. | | 2025년 5월 |


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

AppMeasurement 릴리스에 대한 최신 업데이트는 [AppMeasurement 릴리스 노트](https://github.com/adobe/appmeasurement/releases)를 참조하십시오.


## 관련 리소스

* [2025년 이전 릴리스 정보](/help/release-notes/2025.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [스트리밍 미디어 컬렉션 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트
