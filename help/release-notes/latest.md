---
title: 현재 Adobe Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 7cb7953e3321f2e8fa814ef6f1607cbe8d0f44de
workflow-type: tm+mt
source-wordcount: '1085'
ht-degree: 43%

---

# 최신 Adobe Analytics 릴리스 정보 (2024년 3월)

**마지막 업데이트**: 2024년 3월 13일 목요일

이 릴리스 정보는 2024년 3월 12일부터 2024년 4월까지의 릴리스 기간을 다룹니다. Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 새로운 기능 또는 개선 사항 {#features}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **AppMeasurement 업데이트** | [AppMeasurement 릴리스 v2.26.0](/help/implement/appmeasurement-updates.md) 사용이 가능합니다. | | 2024년 3월 4일 |
| **프로젝트 랜딩 페이지에서 사용할 수 있는 새 열** | 다음 **[!UICONTROL 마지막으로 사용한 날짜]** 이제 의 프로젝트 탭을 볼 때 열을 사용할 수 있습니다. [Adobe Analytics 랜딩 페이지](https://experienceleague.adobe.com/docs/analytics/analyze/landing.html). <p>이 정보는 프로젝트를 마지막으로 연 날짜와 시간을 표시하여 프로젝트가 조직의 사용자에게 중요한지 여부를 확인하는 데 도움이 될 수 있습니다.</p> <p>이전에는 **[!UICONTROL 마지막으로 사용한 날짜]** 열은 계산된 지표 관리자, 세그먼트 관리자 및 경고 관리자에서만 사용할 수 있습니다.</p> |  | 2024년 3월 13일 |
| **DMA용 Google에 필요한 동의 플래그에 대한 분석 지원** | 새로운 유럽 개인 정보 보호 규정으로 인해 Google은 유럽에서 수집된 데이터가 전송되면 두 가지 특정 유형의 동의 여부를 표시해야 합니다. **3월 6일 시작**, Google은 관련 동의가 부여되었음을 표시하지 않는 이벤트 데이터를 더 이상 수락하지 않습니다. Adobe Analytics은 새 adConsent 변수를 통해 이 데이터를 캡처할 수 있도록 지원을 발표했습니다. 새 변수가에 나열되어 있습니다. [개인 정보 보고 UI](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/privacy-reporting.md). 이 기능을 활성화하고 이전 동의 변수에 대해 이미 개인 정보를 활성화한 경우 개인 정보를 다시 활성화해야 합니다. |  | 2024년 3월 13일 |
| **데이터 피드, Data Warehouse 및 분류 세트에 대해 동일한 클라우드 계정 사용** | 이제 생성하는 클라우드 계정 및 위치를 데이터 피드 및 Data Warehouse을 사용하여 데이터를 내보내고 분류 세트를 사용하여 데이터를 가져오는 데 사용할 수 있습니다.<p> **계정 구성 시 변경 사항:** 사용자는 클라우드 가져오기 및 내보내기 계정을 구성하고 다음 목적에 사용할 수 있는 클라우드 가져오기 및 내보내기 위치를 구성할 수 있습니다.<ul><li>분류 세트로 데이터 가져오기</li><li>데이터 피드를 사용하여 데이터 내보내기</li><li>Data Warehouse으로 데이터 내보내기.</li></ul><p>**계정 관리 시 변경 사항**: 사용자는 위치 페이지( 구성 요소 > 위치 아래)를 사용하여 계정 및 위치가 생성된 위치에 관계없이 생성된 모든 계정 및 위치를 보고 관리할 수 있습니다. <p>이전에는 위치 페이지가 분류 세트가 있는 데이터를 가져오기 위해 만든 계정에만 적용되었습니다.</p> | | 2024년 4월 |
| **관리자는 조직의 모든 위치를 관리할 수 있습니다.** | 위치 페이지의 새 옵션을 사용하여 관리자는 조직의 모든 위치를 보고 관리할 수 있습니다. <p>이전에는 관리자가 생성한 위치만 보고 관리할 수 있었습니다.</p> |  | 2024년 4월 |
| **Activity Map은 웹 SDK에 대해 더 적은 서버 호출을 사용합니다** | 현재 Activity Map 링크 이벤트는 자체 이벤트로 계산되며 추가 비용이 발생합니다. <p>이 향상된 기능을 통해 일부 링크 이벤트를 가져와 다음 히트로 패키지화합니다. 이는 AppMeasurement에서 이벤트를 처리하는 방법과 유사합니다.</p> |  | 2024년 4월 3일 |
| **기본적으로 낮은 트래픽 임계값 증가** | **2024년 4월 중반**&#x200B;에 Adobe는 기본 보고서 세트 ![낮은 트래픽 임계값](assets/thresholds.png)을 높일 예정입니다. 이는 현재 새 임계값 아래로 설정된 변수에만 영향을 줍니다. 해당 변경 사항은 점진적으로 적용되고, 작업은 **5월 말**&#x200B;에 완료될 예정입니다. 이 증가분이 롤아웃되면 카디널리티가 높은 변수에 대해 변경 사항이 발생할 수 있습니다.<ul><li>추가 차원 값이 보고에 사용할 수 있습니다.</li><li>세그먼트와 계산된 지표에는 추가 데이터가 포함될 수 있습니다.</li><li>세그먼트 기반 가상 보고서 세트에는 추가 데이터가 포함될 수 있습니다.</li><li>분류 내보내기에는 추가 데이터가 포함될 수 있습니다.</li></ul> | | 2024년 4월 중반 |

{style="table-layout:auto"}

## Adobe Analytics의 수정 사항

* AN-335632, AN-337559, AN-340164, AN-340370, AN-341089, AN-341211, AN-341284, AN-341469, AN-341481, AN-341760, AN-341778, AN-342144, AN-342258, AN-342338, AN-342400의 분류 문제를 해결했습니다
* AN-340921; AN-341269; AN-341292; AN-341467; AN-341666; AN-342145; AN-342329 분류 규칙 빌더 문제가 수정되었습니다.
* 다음 지능형 경고 문제를 해결했습니다. AN-340736
* 다음 세분화 문제를 해결했습니다. AN-336242
* AN-335354; AN-339446; AN-339774; AN-340221; AN-340599; AN-341277; AN-342009; AN-342088; AN-342592 Data Warehouse 문제가 수정되었습니다.
* An-335508, AN-340887, AN-341050, AN-341208, AN-341403, AN-341479, AN-341524, AN-341661, AN-342000, AN-342125, AN-342256, AN-342301, AN-342410, AN-342502342525 과 같은 데이터 피드 문제를 수정했습니다
* 다음 Report Builder 문제를 해결했습니다. AN-340540
* Analysis Workspace 문제: AN-295889; AN-330981; AN-338818; AN-339730; AN-341114; AN-341520;

### 기타 Analytics 수정 사항

AN-312198, AN-338009, AN-339549, AN-333970, AN-334790, AN-336461, AN-336572, AN-339549, AN-341119, AN-341246, AN-341268, AN-341272, AN-341475, AN-341547, AN-341558, AN-341680, AN-342017, AN-,

## Adobe Analytics 관리자에 대한 중요 공지 {#admin}

| 공지 | 추가 또는 업데이트 일자 | 설명 |
| ----------- | ---------- | ---------- |
| **Adobe API 개체 멤버 추가** | 2024년 1월 17일 | 언제든지 Adobe는 버전 관리에 대한 공지나 변경 없이 기존 API 오브젝트에 선택적 요청 및 응답 멤버(이름/값 쌍)를 추가할 수 있습니다. Adobe에서는 이들 추가 사항이 이해되지 않는 경우 처리 시 무시되도록 Adobe API와 통합하는 서드파티 도구의 API 설명서를 참조할 것을 권장합니다. 제대로 구현된 경우 이들 추가 사항은 구현을 위해 중단하는 변경 사항입니다. Adobe는 릴리스 정보를 통한 표준 알림 없이 매개변수를 제거하거나 필수 매개변수를 추가하지 않습니다. |
| **`getPageLoadTime`더 이상 사용되지 않는 플러그인** | 2024년 1월 10일 | 이 플러그인은 더 이상 지원되지 않습니다. 해당 코드는 MDN에 따라 [더 이상 사용되지 않는](https://developer.mozilla.org/en-US/docs/Web/API/PerformanceTiming) performance.timing 메서드를 활용합니다. 업데이트된 플러그인 작업이 시작되었습니다. |

{style="table-layout:auto"}

## 서비스 종료(EOL) 알림 {#eol}

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션** | 2023년 5월 11일 | Adobe I/O JWT 자격 증명을 사용하는 Adobe Analytics API 및 Livestream 고객은 **2025년 1월 1일**&#x200B;까지 Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 2024년 5월 1일부터는 Adobe I/O를 사용하여 새 JWT 자격 증명을 만들 수 없습니다. JWT를 사용하는 고객은 OAuth 서버 간 자격 증명을 새로 만들거나 기존 JWT 자격 증명을 OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 또한 고객은 새 OAuth 서버 간 자격 증명을 사용하려면 클라이언트 애플리케이션을 업데이트해야 합니다. <ul><li>[서비스 계정(JWT) 자격 증명에서 마이그레이션](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[OAuth를 사용한 신규 및 기존 애플리케이션 구현 안내서](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[새 OAuth 서버 간 자격 증명 사용](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[FAQ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |

{style="table-layout:auto"}

## AppMeasurement

AppMeasurement 릴리스(버전 2.26.0)에 대한 최신 업데이트는 다음을 참조하십시오. [JavaScript 릴리스 노트 AppMeasurement](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html).


## 관련 리소스

* [2023년 이전 릴리스 정보](/help/release-notes/2023.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [Media Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트
