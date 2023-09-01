---
title: 현재 Adobe Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 5d0133495613c89deca4dc070d38389ef89853b3
workflow-type: ht
source-wordcount: '891'
ht-degree: 100%

---

# 현재 Adobe Analytics 릴리스 정보 (2023년 8월)

**마지막 업데이트**: 2023년 8월 24일

이 릴리스 정보는 2023년 8월 9일부터 9월 13일까지의 릴리스 기간을 다룹니다. Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 새로운 기능 또는 개선 사항 {#features}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **API 2.0의 분류 세트** | 분류 세트 데이터의 저장, 삭제, 검색, 가져오기 및 내보내기를 위한 Adobe Analytics API 2.0 메서드를 제공합니다. | 해당 사항 없음 | 2023년 8월 30일 |
| **보고 활동 관리자** | 보고 활동 관리자는 관리자에게 보고 사용량에 대해 상세한 가시성을 제공하며 최대 보고 시간 동안 발생할 수 있는 용량 문제를 쉽게 진단하고 해결할 수 있도록 해 줍니다. [자세히 알아보기](/help/admin/admin/reporting-activity.md) | 해당 사항 없음 | 2023년 9월 12일 |

{style="table-layout:auto"}

## Adobe Analytics의 수정 사항

* 사용자 정의 이벤트가 로드되지 않는 문제가 해결되었습니다. (AN-324163)
* 시각화에서 범례의 레이블을 편집할 수 없는 문제가 해결되었습니다. (AN-323246)

AN-315605; AN-316306; AN-317494; AN-317844; AN-320424; AN-320597; AN-320680; AN-320869; AN-321624; AN-321693; AN-322009; AN-322244; AN-322380; AN-322432; AN-322466; AN-322556; AN-322669; AN-322735; AN-323151; AN-323220; AN-323380; AN-323492; AN-323595; AN-323755; AN-323854; AN-323916; AN-324044; AN-324200; AN-324213; AN-324238; AN-324347; AN-323598; AN-323625; AN-323631; AN-323638; AN-323641; AN-323755; AN-323767; AN-323777; AN-323825; AN-323846; AN-323972; AN-324113; AN-324170; AN-324197; AN-324273; AN-324275; AN-324345; AN-324384; AN-324433; AN-324511; AN-324513; AN-324521; AN-324524; AN-324531; AN-324532; AN-324534; AN-324537; AN-324569; AN-324618; AN-324635; AN-324688; AN-324704; AN-324712; AN-324721; AN-324745; AN-324792; AN-324793; AN-324794; AN-324795; AN-324824; AN-324905; AN-324918; AN-324932; AN-324934; AN-324947; AN-325003; AN-325073; AN-325143; AN-325148; AN-325153; AN-325177; AN-325187; AN-325252; AN-325305; AN-325363; AN-325401; AN-325439; AN-325431; AN-325491; AN-325495; AN-325508; AN-325594; AN-325601; AN-325660; AN-325779; AN-325857; AN-325883; AN-325885; AN-325886


## Adobe Analytics 관리자에 대한 중요 공지 {#admin}

| 공지 | 추가 또는 업데이트 일자 | 설명 |
| ----------- | ---------- | ---------- |
| **구매 ID 및 이벤트 ID의 37개월 만료(이벤트 일련화)** | 2023년 7월 10일 | **2023년 7월 13일**&#x200B;에 출시되는 Analytics Hit 처리 엔진의 최신 릴리스에서는 구매 ID 및 이벤트 ID의 37개월 만료(이벤트 일련화)가 적용되었습니다. 이전에는 구매 ID 및 이벤트 ID가 Adobe Analytics에서 만료되지 않았습니다. 구매 ID 또는 이벤트 ID가 표시/사용되면 이후 히트는 언제라도 해당 구매 또는 이벤트가 중복으로 표시되었습니다. 새로운 처리 엔진 릴리스:<ul><li>구매 ID 및 이벤트 ID는 항상 37개월 후에 만료됩니다.</li><li>구매 ID 또는 이벤트 ID를 조회한 후 37개월이 경과한 경우에는 더 이상 중복 구매 또는 이벤트로 간주되지 않습니다.</li><li> 37개월 이전의 구매 ID 또는 이벤트 ID를 “재사용”하는 경우, 더 이상 중복으로 간주되지 않습니다.</li></ul> |
| **Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션** | 2023년 5월 11일 | Adobe I/O JWT 자격 증명을 사용하는 Adobe Analytics API 및 Livestream 고객은 **2025년 1월 1일**&#x200B;까지 Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 자세한 내용과 타임라인은 아래 표의 서비스 종료 알림을 참조하십시오. |

{style="table-layout:auto"}

## 서비스 종료(EOL) 알림 {#eol}

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션** | 2023년 5월 11일 | Adobe I/O JWT 자격 증명을 사용하는 Adobe Analytics API 및 Livestream 고객은 **2025년 1월 1일**&#x200B;까지 Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 2024년 5월 1일부터는 Adobe I/O를 사용하여 새 JWT 자격 증명을 만들 수 없습니다. JWT를 사용하는 고객은 OAuth 서버 간 자격 증명을 새로 만들거나 기존 JWT 자격 증명을 OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 또한 고객은 새 OAuth 서버 간 자격 증명을 사용하려면 클라이언트 애플리케이션을 업데이트해야 합니다. <ul><li>[서비스 계정(JWT) 자격 증명에서 마이그레이션](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[OAuth를 사용한 신규 및 기존 애플리케이션 구현 안내서](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[새 OAuth 서버 간 자격 증명 사용](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[FAQ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |
| **[!DNL Reports & Analytics]**&#x200B;에 대한 EOL | 2023년 3월 7일 | **2023년 12월 31일**&#x200B;부로 Adobe는 [!DNL Reports & Analytics] 및 관련 보고서와 기능에 대한 서비스를 중단할 예정입니다. [!DNL Reports & Analytics]가 제공하는 보고서, 시각화 및 기반 기술은 더 이상 Adobe의 기술 표준을 충족하지 않습니다. 대부분의 [!DNL Reports & Analytics] 기능은 [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html)에서 사용할 수 있습니다. 2015년 Analysis Workspace가 출시된 이후 [!DNL Reports & Analytics] 기능이 Analysis Workspace로 이전되면서 워크플로 패리티의 한계점에 도달했습니다. [이 공지 사항](https://spark.adobe.com/page/6WnF8JK6IRDhf/)은 서비스 종료 프로세스에 대해 설명합니다.<p>2023년 12월 31일에 예약된 보고서, 데이터 추출, DL 보고서를 포함하되 이에 국한되지 않는 많은 관련 Reports &amp; Analytics 기능이 종료됩니다. 2023년 12월 31일 이후에는 예약된 보고서가 더 이상 전송되지 않습니다. **2023년 4월**, 2023년 12월 31일 이후에 만료되도록 예정된 모든 보고서가 자동으로 업데이트되고 2023년 12월 31일에 만료되도록 되돌려집니다. 또한 2023년 12월 31일 이후에는 더 이상 향후 보고서를 예약할 수 없습니다. |
| **[!UICONTROL 게시 목록] 기능의 EOL** | 2022년 9월 29일 | Reports &amp; Analytics EOL의 일환으로 [!UICONTROL 게시 목록]은 **2023년 12월**&#x200B;에 서비스가 종료됩니다. [!UICONTROL Analysis Workspace] 프로젝트를 보내거나 예약하기 위해 새 게시 목록을 만들거나 기존 [!UICONTROL 게시 목록]에 액세스할 수 없습니다. |
| **Data Workbench용 EOL** | 2022년 9월 14일 | Adobe는 **2023년 12월 31일**&#x200B;부로 Data Workbench의 서비스를 종료할 예정입니다. 자세한 내용은 [Data Workbench 서비스 종료 공지](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html)를 참조하십시오. 문의 사항이 있으면 조직의 Adobe 계정 관리자에게 문의하십시오. |

{style="table-layout:auto"}

## AppMeasurement

AppMeasurement 릴리스(버전 2.24.0)에 대한 최신 업데이트는 [JavaScript용 AppMeasurement 릴리스 정보](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html)를 참조하십시오.


## 관련 리소스

* [2022년 이전 릴리스 정보](/help/release-notes/2022.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [Media Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트
