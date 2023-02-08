---
title: 최신 Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: e7140b78b7b2c6c63cb93f1341581cc83af7b33b
workflow-type: tm+mt
source-wordcount: '954'
ht-degree: 70%

---

# 현재 Adobe Analytics 릴리스 정보 (2023년 2월)

**마지막 업데이트 날짜**: 2023년 2월 2일

Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## Adobe Analytics의 새로운 기능 또는 업데이트

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **데이터 개인 정보 보호 레이블에 대한 사용자 인터페이스가 업데이트되었습니다** | 업데이트된 인터페이스를 사용하면 보고서 세트 구성 요소에 대한 데이터 개인 정보 레이블 생성, 관리 및 편집 프로세스를 간소화할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/data-labels/gdpr-setup-reportsuite.html?lang=en) | 해당 사항 없음 | 2023년 2월 8일 |
| **모바일 스코어카드의 비교 날짜 범위** | 모바일 스코어카드를 사용하여 **[!UICONTROL 비교 날짜 포함]** 비교 날짜를 보거나 숨기도록 설정합니다. | 해당 없음 | 2023년 2월 8일 |
| **Workspace의 달력 업데이트** | <ul><li>앵커 패널 날짜: 패널 달력에 상대적인 날짜 범위 구성 요소를 만들 수 있습니다. [자세히 알아보기](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md#relative-panel-dates)</li><li>달력 스타일 업데이트: UI의 달력 스타일이 업그레이드되어 보다 일관되고 사용하기 쉬운 워크플로우를 제시했습니다.</li><li>달력 공식 업데이트: 상대적 날짜를 사용하는 경우 모든 달력 공식은 패널 날짜 범위의 시작을 반영합니다. [자세히 알아보기](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md#formula-relative-dates)</li></ul> | 해당 사항 없음 | 2023년 2월 8일 |
| **Adobe Analytics 소스 커넥터 스트리밍을 위한 행/열 필터링** | 이제 Adobe Experience Platform의 Analytics 소스 커넥터에서 프로필을 채우는 데 사용되는 Analytics 데이터를 필터링할 수 있습니다. [실시간 고객 프로필](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=ko). 행 수준 필터링은 프로필과 관련된 이벤트 수를 줄이는 데 도움이 됩니다. 열 수준 필터링은 이벤트 자체의 풍부함을 줄이는 데 도움이 되므로 프로필 권한 사용을 최적화할 수 있습니다. 이 필터링은 실시간 고객 프로필로 전송된 데이터에만 적용됩니다. [ID 서비스](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=ko). **필터링은 Customer Journey Analytics과 같은 애플리케이션에서 사용하기 위해 Data Lake로 전송되는 데이터에 영향을 주지 않습니다**. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=en#filtering-for-profile) | 해당 사항 없음 | 2023년 2월 22일 |

{style=&quot;table-layout:auto&quot;}

## Adobe Analytics의 수정 사항

-302282; AN-303127; AN-303541; AN-303550; AN-305282; AN-306504; AN-307351; AN-307496; AN-307530; AN-307947; AN-308497; AN-; AN-308610; AN-308777; AN-308994; AN-309143; AN-309404; AN-309414; AN-309445; AN-309575; AN-309630; AN-309658; AN-309690; AN-309742; AN-309861; AN-309967; AN-309973; AN-310059; AN-310132; AN-310168; AN-310238; AN-310241; AN-310301; AN-310318; AN-310324; AN-310335; AN-310338; AN-310460; AN-310500; AN-310684; AN-310690; AN-311010; AN-311022; AN-311043; AN-311125; AN-311250; AN-311370; AN-311458;

## Adobe Analytics 관리자에 대한 중요 공지

| 공지 | 추가 또는 업데이트 일자 | 설명 |
| ----------- | ---------- | ---------- |
| **Google 클라이언트 힌트로 인한 디바이스 조회 업데이트** | 2023년 1월 25일 | 디바이스 조회에서 클라이언트 힌트는 **2023년 2월 16일**&#x200B;부터 사용할 수 있습니다. <p> <p>2022년 10월부터 Web SDK 또는 AppMeasurement JavaScript 라이브러리를 사용하여 클라이언트 힌트를 수집할 수 있습니다. 그러나 클라이언트 힌트는 2023년 2월까지 디바이스 조회에 통합되지 않을 예정입니다. 해당 시기에 Adobe는 Google Chrome 및 Microsoft Edge와 같은 Chromium 브라우저에서 발생하는 히트에 대한 특정 디바이스 정보를 가져올 때 사용자 에이전트와 함께 클라이언트 힌트를 사용할 예정입니다. 이는 클라이언트 힌트를 통해 전달되는 데이터 대신 사용자 에이전트 문자열에서 제공되는 정보를 점차적으로 줄이려는 Google의 계획에 따른 것입니다. <p> <p>이 변경 내용의 일부로 Adobe는 사용자 에이전트와 관련된 모든 디바이스 조회에 Device Atlas를 사용하게 됩니다. [자세히 알아보기](/help/technotes/client-hints.md) |
| **Reports &amp; Analytics에서 예약된 보고서 일시 중지** | 2023년 1월 6일 | Adobe에서 이러한 기능은 더 이상 사용되지 않음 **2023년 1월 31일**. 보고서와 데이터 추출의 만료 기간은 계속 9개월로 제한됩니다. 보고서 및 데이터 추출 게재는 일정이 다시 활성화되지 않는 한 이 기간이 끝나면 일시 중지됩니다.<p>2023년 1월 31일 이전에 Adobe Analytics에서 사용할 수 있는 다른 메커니즘으로 예약된 보고를 마이그레이션해야 했습니다. 추가 질문이 있거나 지원이 필요한 경우 Adobe 고객 지원 센터에 문의하십시오. [자세히 알아보기](/help/analyze/reports-analytics/scheduled-reports-eol.md) |
| **Report Builder에서 예약된 작업 일시 중지** | 2023년 1월 6일 | 설정 **2023년 1월 31일**, Adobe은 성능 및 게재 최적화 노력의 일환으로 Report Builder에서 예약된 작업에 대한 변경 사항을 롤아웃했습니다. 이러한 변경 사항에는 예약된 게재가 “x회 발생 후 종료”되도록 하는 기능의 제거가 포함되었습니다. <p>계속해서 시간별 Report Builder 작업을 예약하고 최대 99회 발생 후 종료되도록 할 수 있습니다. 롤백은 시간별 작업에만 적용됩니다. “x회 발생 후 종료”는 다른 모든 게재 간격(일별, 주별, 월별 및 연간)에 대해 계속 사용할 수 없습니다. 추가 질문이 있거나 지원이 필요한 경우 Adobe 고객 지원 센터에 문의하십시오. [자세히 알아보기](/help/analyze/report-builder/r-arb-scheduled-reports.md) |

{style=&quot;table-layout:auto&quot;}

## 서비스 종료 알림

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **Data Workbench용 EOL** | 2022년 9월 14일 | Adobe는 **2023년 12월 31일**&#x200B;부로 Data Workbench의 서비스를 종료할 예정입니다. 자세한 내용은 [Data Workbench 서비스 종료 공지](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html)를 참조하십시오. 문의 사항이 있으면 조직의 Adobe 계정 관리자에게 문의하십시오. |
| **[!DNL Reports & Analytics]**&#x200B;에 대한 EOL | 2022년 1월 4일 | **2023년 12월 31일**&#x200B;부로 Adobe는 [!DNL Reports & Analytics] 및 관련 보고서와 기능에 대한 서비스를 중단할 예정입니다. [!DNL Reports & Analytics]가 제공하는 보고서, 시각화 및 기반 기술은 더 이상 Adobe의 기술 표준을 충족하지 않습니다. 대부분의 [!DNL Reports & Analytics] 기능은 [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=ko-KR)에서 사용할 수 있습니다. 2015년 Analysis Workspace가 출시된 이후 [!DNL Reports & Analytics] 기능이 Analysis Workspace로 이전되면서 워크플로 패리티의 한계점에 도달했습니다. [이 공지 사항](https://spark.adobe.com/page/6WnF8JK6IRDhf/)은 서비스 종료 프로세스에 대해 설명합니다. |
| **[!UICONTROL 게시 목록] 기능의 EOL** | 2022년 9월 29일 | Reports &amp; Analytics EOL의 일환으로 게시 목록은 **2023년 12월**&#x200B;에 사용 수명이 종료됩니다. Analysis Workspace 프로젝트를 보내거나 예약하기 위해 새 게시 목록을 만들거나 기존 게시 목록에 액세스할 수 없습니다. |

{style=&quot;table-layout:auto&quot;}

## AppMeasurement

AppMeasurement 릴리스(버전 2.23.0)에 대한 최신 업데이트는 [JavaScript용 AppMeasurement 릴리스 정보](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html)를 참조하십시오.


## 관련 리소스

* [2022년 이전 릴리스 정보](/help/release-notes/2022.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=ko-KR)
* [Media Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=ko-KR)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트
