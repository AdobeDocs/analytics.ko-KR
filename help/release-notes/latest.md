---
title: 현재 Adobe Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 7468463e2fe1de16221b4528919b6abd6c8aedcb
workflow-type: ht
source-wordcount: '1445'
ht-degree: 100%

---

# 최신 Adobe Analytics 릴리스 정보 (2024년 4월)

**마지막 업데이트**: 2024년 4월 17일

이번 릴리스 정보에는 2024년 4월 17일부터 5월까지의 릴리스 기간이 포함됩니다. Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 새로운 기능 또는 개선 사항 {#features}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **스트리밍 미디어: Roku 데이터를 Adobe Experience Platform Edge Network로 보내기** | 이제 [Experience Platform Edge를 사용하여 Media Analytics를 설치](https://experienceleague.adobe.com/ko/ko/docs/media-analytics/using/implementation/edge-recommended/media-edge-sdk/implementation-edge)할 때 Adobe Experience Platform Roku SDK를 사용하여 스트리밍 미디어 데이터를 Adobe Experience Platform으로 보낼 수 있습니다. |  | 2024년 4월 12일 |
| **Web SDK 마이그레이션을 위한 향상된 워크플로** | 이제 데이터스트림은 Web SDK 데이터 오브젝트의 필드를 Adobe Analytics에 직접 자동으로 매핑합니다. [데이터 오브젝트 매핑](/help/implement/aep-edge/data-var-mapping.md)은 [XDM 오브젝트 매핑](/help/implement/aep-edge/xdm-var-mapping.md)과 유사하지만 XDM 스키마가 필요하지 않습니다. 향상된 이 워크플로에는 다음과 같은 이점이 있습니다.<ul><li>Adobe Experience Platform에 데이터를 보낼 준비가 될 때까지 스키마 사용 요구 사항이 지연됩니다. 구현 마이그레이션 단계에서 스키마가 필요한 경우, Adobe Analytics 필드를 기반으로 하는 스키마를 사용해야 합니다. Customer Journey Analytics와 같은 Adobe Experience Platform 서비스에는 prop 또는 eVar 개념이 없습니다. Analytics 중점 스키마는 조직에서 향후 자체 스키마를 사용하려는 경우 어려움을 초래할 수 있습니다.</li><li>Web SDK에 대한 구현을 변경한 후 조직은 Adobe Analytics에서 Customer Journey Analytics로 마이그레이션하기 더 수월해집니다. Web SDK를 사용하여 Adobe Analytics로 데이터를 보내는 경우, Adobe Experience Platform으로 데이터를 보내기 위해 구현 변경을 추가로 수행할 필요가 없습니다. 대신 데이터 준비를 사용하여 데이터 오브젝트 필드를 XDM 스키마에 매핑할 수 있습니다.</li></ul>자세한 내용은 [Adobe Analytics 태그 확장 기능에서 Web SDK 태그 확장 기능으로 마이그레이션](/help/implement/aep-edge/web-sdk/analytics-extension-to-web-sdk.md) 및 [AppMeasurement에서 Web SDK로 마이그레이션](../implement/aep-edge/web-sdk/appmeasurement-to-web-sdk.md)을 참조하십시오. |  | 2024년 4월 |
| **프로젝트 전용 [!UICONTROL Workspace] 구성 요소의 권한 강화** | 이전에는 사용자(사용자 A)가 다른 사용자(사용자 B)와 프로젝트를 공유하는데 사용자 B에게 프로젝트에 대한 편집 액세스 권한을 부여한 경우, 사용자 B가 프로젝트를 편집할 수 있었습니다. 그러나 사용자 B는 프로젝트에 임베드된 [!UICONTROL 빠른 세그먼트]를 편집할 수 없었습니다. 이제 이러한 제한이 제거되었습니다. 사용자 B는 [!UICONTROL 빠른 세그먼트] 및 공유 프로젝트에 임베드된 기타 프로젝트 전용 구성 요소를 편집할 수 있습니다. |  | 2024년 4월 17일 |
| **[!UICONTROL 데이터 피드], [!UICONTROL Data Warehouse] 및 [!UICONTROL 분류 세트]**&#x200B;에 대해 동일한 클라우드 계정 사용 | 이제 사용자가 만든 클라우드 계정 및 위치를 데이터 내보내기([!UICONTROL 데이터 피드] 및 [!UICONTROL Data Warehouse] 사용) 및 데이터 가져오기([!UICONTROL 분류 세트] 사용)에 사용할 수 있습니다.<p> **계정 구성 시 변경 사항:** 사용자는 다음 목적으로 사용 가능한 [클라우드 가져오기 및 내보내기 계정을 구성](https://experienceleague.adobe.com/ko/ko/docs/analytics/components/locations/configure-import-accounts)하고 [클라우드 가져오기 및 내보내기 위치를 구성](https://experienceleague.adobe.com/ko/ko/docs/analytics/components/locations/configure-import-locations)할 수 있습니다.<ul><li>[!UICONTROL 분류 세트]를 사용하여 데이터 가져오기</li><li>[!UICONTROL 데이터 피드]를 사용하여 데이터 내보내기</li><li>[!UICONTROL Data Warehouse]를 사용하여 데이터를 내보냅니다.</li></ul><p>**[!UICONTROL 위치] 페이지에서 계정 및 위치 관리 시 변경 사항**: 사용자는 [위치](https://experienceleague.adobe.com/ko/ko/docs/analytics/components/locations/locations-manager) 페이지([!UICONTROL 구성 요소] > 위치)를 사용하여 만든 위치에 관계없이 자신이 만든 모든 계정과 위치를 보고 관리할 수 있습니다. <p>이전에는 [!UICONTROL 분류 세트]를 사용하여 데이터를 가져오기 위해 만든 계정에만 [!UICONTROL 위치] 페이지가 적용되었습니다.</p>**[!UICONTROL Data Warehouse] 또는 [!UICONTROL 분류 설정]**&#x200B;에서 위치 관리 시 변경 사항<p>특정 애플리케이션 영역([!UICONTROL Data Warehouse] 또는 [!UICONTROL 분류 설정]) 내에서 위치를 관리할 때 특정 애플리케이션에서 생성된 위치만 사용할 수 있습니다. 예를 들어 [!UICONTROL Data Warehouse] 애플리케이션 영역을 보면 [!UICONTROL Data Warehouse] 위치만 표시됩니다. 모든 계정은 생성된 애플리케이션 영역에 관계없이 각 애플리케이션 영역에서 계속 사용할 수 있습니다. 이전에는 생성된 애플리케이션 영역에 관계없이 각 애플리케이션 영역에서 모든 계정과 위치를 사용할 수 있었습니다. [!UICONTROL 데이터 피드] 애플리케이션 영역을 볼 때도 마찬가지입니다. | | 2024년 4월 17일 |
| **관리자가 조직의 모든 위치 및 계정 관리 가능** | 위치 탭(구성 요소 > 위치 페이지)의 새로운 옵션을 통해 관리자가 조직의 모든 위치를 보고 관리할 수 있습니다.<p>[위치](https://experienceleague.adobe.com/ko/ko/docs/analytics/components/locations/locations-manager) 계정 탭(구성 요소 > 위치 페이지)의 새로운 옵션을 통해 관리자가 조직의 모든 계정을 보고 관리할 수 있습니다.</p> <p>이전에는 관리자가 자신이 만든 위치 및 계정만 보고 관리할 수 있었습니다.</p> |  | 2024년 4월 17일 |
| **기본적으로 낮은 트래픽 임계값 증가** | **2024년 4월 중반**&#x200B;에 Adobe는 기본 보고서 세트 ![낮은 트래픽 임계값](assets/thresholds.png)을 높일 예정입니다. 이는 현재 새 임계값 아래로 설정된 변수에만 영향을 줍니다. 해당 변경 사항은 점진적으로 적용되고, 작업은 **5월 말**&#x200B;에 완료될 예정입니다. 이 증가분이 롤아웃되면 카디널리티가 높은 변수에 대해 변경 사항이 발생할 수 있습니다.<ul><li>추가 차원 값이 보고에 사용할 수 있습니다.</li><li>세그먼트와 계산된 지표에는 추가 데이터가 포함될 수 있습니다.</li><li>세그먼트 기반 가상 보고서 세트에는 추가 데이터가 포함될 수 있습니다.</li><li>분류 내보내기에는 추가 데이터가 포함될 수 있습니다.</li></ul> | 2024년 4월 중반 | 2024년 5월 31일 |
| **Activity Map에서 Web SDK에 대해 더 적은 서버 호출 사용** | 현재 Activity Map 링크 이벤트는 자체 이벤트로 계산되어 추가 비용이 발생합니다. <p>이 향상된 기능을 통해 일부 링크 이벤트를 가져와 다음 히트로 패키지화합니다. 이는 AppMeasurement에서 이벤트를 처리하는 방법과 유사합니다.</p> |  | 2024년 5월 31일 |

{style="table-layout:auto"}

## Adobe Analytics의 수정 사항

* 다음 분류 문제가 수정되었습니다. AN-343439, AN-343503, AN-343504, AN-343986, AN-344262, AN-344564, AN-345204, AN-345234
* 다음 분류 규칙 빌더 문제가 수정되었습니다. AN-341488, AN-342501, AN-345751
* 다음 지능형 경고 문제가 수정되었습니다. AN-343466,
* 다음 세분화 문제가 해결되었습니다. AN-342313
* 다음 Data Warehouse 문제가 수정되었습니다. AN-344292
* 다음 데이터 피드 문제를 수정되었습니다. AN-339545, AN-340092, AN-342124, AN-342862, AN-343737, AN-344035, AN-344329, AN-344703, AN-344721, AN-344940, AN-345180, AN-345196, AN-345225, AN-345236, AN-345326, AN-345631, AN-345659
* 다음 데이터 소스 문제가 수정되었습니다. AN-343541
* 다음 Analysis Workspace 문제가 수정되었습니다. AN-336303, AN-336472, AN-338422, AN-338556, AN-339718, AN-340147, AN-340301, AN-340421, AN-340951, AN-341172, AN-342905, AN-342909, AN-343448, AN-343570, AN-344050, AN-344182, AN-344763, AN-344768,
* 다음 Analytics 관리 문제가 수정되었습니다. AN-342519, AN-342523, AN-343623, AN-343882, AN-344237, AN-344829, AN-345235
* 다음 A4T 문제가 수정되었습니다. AN-341619, AN-344402
* 다음 모바일 애플리케이션 문제가 해결되었습니다. AN-342010

### 기타 Analytics 수정 사항

AN-336099, AN-337474, AN-337993, AN-339718, AN-339901, AN-340014, AN-341356, AN-343021, AN-343102, AN-343353, AN-343416, AN-340014, AN-344037, AN-344525, AN-345737

## Adobe Analytics 관리자에 대한 중요 공지 {#admin}

| 공지 | 추가 또는 업데이트 일자 | 설명 |
| ----------- | ---------- | ---------- |
| **저장된 기간이 13개월 만료됨:`cust_visids`** | 2024년 3월 20일 | 4월 또는 5월을 목표로 하는 Analytics Hit 처리 엔진의 향후 릴리스에서는 저장된 `cust_visids`의 만료 기간을 13개월로 적용할 예정입니다. 보고서 세트에 “방문자 결합 활성화”가 활성화된 경우 이 설정은 히트에 `cust_visid`가 없는 `visid_high/visid_low value`에 대해 `cust_visid`를 찾는 데 사용됩니다. 현재는 `visid_high/visid_low`에 대한 `cust_visid`의 매핑 만료가 없습니다. 이 릴리스에서는 `visid_high/visid_low`가 `cust_visid`를 히트시킨 후 13개월 이상 경과한 경우 매핑이 만료됩니다. |
| **Adobe API 오브젝트 멤버 추가** | 2024년 1월 17일 | 언제든지 Adobe는 버전 관리에 대한 공지나 변경 없이 기존 API 오브젝트에 선택적 요청 및 응답 멤버(이름/값 쌍)를 추가할 수 있습니다. Adobe에서는 이들 추가 사항이 이해되지 않는 경우 처리 시 무시되도록 Adobe API와 통합하는 서드파티 도구의 API 설명서를 참조할 것을 권장합니다. 제대로 구현된 경우 이들 추가 사항은 구현을 위해 중단하는 변경 사항입니다. Adobe는 릴리스 정보를 통한 표준 알림 없이 매개변수를 제거하거나 필수 매개변수를 추가하지 않습니다. |

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
