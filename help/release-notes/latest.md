---
title: 최신 Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: b724ef95771b49a81563587a5d8bbfe26c99c134
workflow-type: tm+mt
source-wordcount: '891'
ht-degree: 72%

---

# 현재 Adobe Analytics 릴리스 정보 (2023년 7월)

**마지막 업데이트**: 2023년 7월 10일

Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 새로운 기능 또는 향상된 기능 {#features}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **분류 데이터를 수집하기 위한 클라우드 계정 저장소 위치 구성** | 이제 분류 세트 자동화에 사용되는 클라우드 계정 저장소 위치를 관리할 수 있습니다. [자세히 알아보기](/help/components/locations/configure-import-accounts.md)<p> | 해당 사항 없음 | 2023년 7월 10일 |
| **데이터 복구 필터 개선 사항** | 데이터 복구에 세 가지 필터링 개선 사항이 추가되었습니다.<ul><li>한 개의 변수로 필터링하여 두 번째 변수를 수정합니다. 예를 들어 다음과 같습니다. `eVar2` &quot;@&quot;을(를) 포함한 다음 삭제 `eVar3`.</li><li>숫자 또는 숫자가 아닌 값 필터링</li><li>AND로 여러 필터를 적용합니다. 예를 들어, `eVar2="a"` 및 `eVar3="b"`</li></ul>[자세히 알아보기](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/data-repair/) | 2023년 6월 21일 | 2023년 7월 12일 |
| **데이터 피드 내보내기를 위한 보안 대상** | 이제 데이터 피드를 다음 클라우드 스토리지 대상으로 보낼 수 있습니다.<ul><li>Amazon S3</li><li>Azure RBAC</li><li>Azure SAS</li><li>Google Cloud 플랫폼</li></ul>이전에 사용할 수 있었던 대상(FTP, SFTP, S3 및 Azure Blob)은 더 이상 권장되지 않습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/create-feed.html) | 2023년 6월 12일 | 2023년 7월 15일 |

{style="table-layout:auto"}

## Adobe Analytics의 수정 사항

AN-307816, AN-318111, AN-318584, AN-318828, AN-320440, AN-320568, AN-320616, AN-321013, AN-321513, AN-321520, AN-321757, AN-321820, 321917, AN-322034, AN-322135, AN-322140, AN-322142, AN-322251, AN-322353, AN-322378, AN-322383, AN-322427, AN-322458, AN-322543, AN-322630, AN-322637, 322638, AN-322647, AN-322728, AN-322732, AN-322777, AN-322817, AN-322957, AN-322958, AN-323035, AN-323074, AN-323150, AN-323196, AN-323197, AN-323205, AN-323206, AN-323217, AN-323224, AN-323225, AN-323244, AN-323257, AN-323277, AN-323280, AN-323293, AN-323309, AN-323318, AN-323468, AN-323476, AN-323514, AN-323572, AN-323592, AN-323782, AN-323835

## Adobe Analytics 관리자에 대한 중요 공지 {#admin}

| 공지 | 추가 또는 업데이트 일자 | 설명 |
| ----------- | ---------- | ---------- |
| **구매 ID 및 이벤트 ID의 37개월 만료(이벤트 일련화)** | 10,2023년 7월 | 다음에 릴리스가 타깃팅된 Analytics 히트 처리 엔진의 향후 릴리스 **2023년 7월 13일**&#x200B;는 구매 ID 및 이벤트 ID(이벤트 일련화)의 37개월 만료를 적용합니다. 현재 구매 ID 및 이벤트 ID는 Adobe Analytics에서 만료되지 않습니다. 구매 ID 또는 이벤트 ID가 표시/사용되면 이후 히트는 언제라도 해당 구매 또는 이벤트가 중복으로 표시됩니다. 새로운 처리 엔진 릴리스:<ul><li>구매 ID 및 이벤트 ID는 항상 37개월 후에 만료됩니다.</li><li>구매 ID 또는 이벤트 ID를 조회한 후 37개월이 경과한 경우에는 더 이상 중복 구매 또는 이벤트로 간주되지 않습니다.</li><li> 37개월 이전의 구매 ID 또는 이벤트 ID를 “재사용”하는 경우, 더 이상 중복으로 간주되지 않습니다.</li></ul> |
| **Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션** | 2023년 5월 11일 | Adobe I/O JWT 자격 증명을 사용하는 Adobe Analytics API 및 라이브스트림 고객은 다음 작업을 수행하여 Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. **2025년 1월 1일**. 자세한 내용과 타임라인은 아래 표의 수명 종료 알림을 참조하십시오. |

{style="table-layout:auto"}

## 서비스 종료(EOL) 알림 {#eol}

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션** | 2023년 5월 11일 | Adobe I/O JWT 자격 증명을 사용하는 Adobe Analytics API 및 라이브스트림 고객은 다음 작업을 수행하여 Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. **2025년 1월 1일**. 2024년 5월 1일부터 Adobe I/O에서 새 JWT 자격 증명을 만들 수 없습니다. JWT를 사용하는 고객은 OAuth 서버 간 자격 증명을 새로 만들거나 기존 JWT 자격 증명을 OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 또한 고객은 새 OAuth 서버 간 자격 증명을 사용하려면 클라이언트 애플리케이션을 업데이트해야 합니다. <ul><li>[서비스 계정(JWT) 자격 증명에서 마이그레이션](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[OAuth를 사용하는 신규 및 기존 애플리케이션에 대한 구현 안내서](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[새 OAuth 서버 간 자격 증명 사용](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[FAQ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |
| **[!DNL Reports & Analytics]**&#x200B;에 대한 EOL | 2023년 3월 7일 | **2023년 12월 31일**&#x200B;부로 Adobe는 [!DNL Reports & Analytics] 및 관련 보고서와 기능에 대한 서비스를 중단할 예정입니다. [!DNL Reports & Analytics]가 제공하는 보고서, 시각화 및 기반 기술은 더 이상 Adobe의 기술 표준을 충족하지 않습니다. 대부분의 [!DNL Reports & Analytics] 기능은 [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html)에서 사용할 수 있습니다. 2015년 Analysis Workspace가 출시된 이후 [!DNL Reports & Analytics] 기능이 Analysis Workspace로 이전되면서 워크플로 패리티의 한계점에 도달했습니다. [이 공지 사항](https://spark.adobe.com/page/6WnF8JK6IRDhf/)은 서비스 종료 프로세스에 대해 설명합니다.<p>2023년 12월 31일에 예약된 보고서, 데이터 추출, DL 보고서를 포함하되 이에 국한되지 않는 많은 관련 Reports &amp; Analytics 기능이 종료됩니다. 2023년 12월 31일 이후에는 예약된 보고서가 더 이상 전송되지 않습니다. **2023년 4월**, 2023년 12월 31일 이후에 만료되도록 예정된 모든 보고서가 자동으로 업데이트되고 2023년 12월 31일에 만료되도록 되돌려집니다. 또한 2023년 12월 31일 이후에는 더 이상 향후 보고서를 예약할 수 없습니다. |
| **[!UICONTROL 게시 목록] 기능의 EOL** | 2022년 9월 29일 | Reports &amp; Analytics EOL의 일환으로 [!UICONTROL 게시 목록]은 **2023년 12월**&#x200B;에 사용 수명이 종료됩니다. [!UICONTROL Analysis Workspace] 프로젝트를 보내거나 예약하기 위해 새 게시 목록을 만들거나 기존 [!UICONTROL 게시 목록]에 액세스할 수 없습니다. |
| **Data Workbench용 EOL** | 2022년 9월 14일 | Adobe는 **2023년 12월 31일**&#x200B;부로 Data Workbench의 서비스를 종료할 예정입니다. 자세한 내용은 [Data Workbench 서비스 종료 공지](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html)를 참조하십시오. 문의 사항이 있으면 조직의 Adobe 계정 관리자에게 문의하십시오. |

{style="table-layout:auto"}

## AppMeasurement

AppMeasurement 릴리스(버전 2.23.0)에 대한 최신 업데이트는 [JavaScript용 AppMeasurement 릴리스 정보](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html)를 참조하십시오.


## 관련 리소스

* [2022년 이전 릴리스 정보](/help/release-notes/2022.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [Media Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트
