---
title: 최신 Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: ccb40e45ea559db815f4252d85baa61b9e109024
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 58%

---

# 현재 Adobe Analytics 릴리스 정보 (2023년 3월)

**마지막 업데이트**: 2023년 3월 7일

Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## Adobe Analytics의 새로운 기능 또는 업데이트 {#features}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Analysis Workspace의 데이터 사전** | 데이터 사전은 사용자와 관리자 모두가 Analytics 환경의 구성 요소(차원, 지표)를 추적하고, 관리하고, 더 잘 이해할 수 있도록 도와줍니다. [자세히 알아보기](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) | 2023년 3월 15일 | 2023년 3월 22일 |
| **모바일 대시보드의 데이터 스토리** | 데이터 스토리를 사용하면 모바일 스코어카드 프로젝트의 타일에 사용자 지정 가능한 여러 세부 정보 보기를 추가할 수 있습니다. 데이터 스토리를 사용하여 주요 동인, 관련 지표 및 고객 여정의 다양한 단계를 자세히 알아보십시오. 이러한 보기를 쉽게 스와이프하여 주요 지표에 숨겨진 전체 스토리를 이해할 수 있습니다. 자세히 알아보기 (따라가기) | 해당 사항 없음 | 2023년 3월 8일 |
| **예약된 프로젝트에 대한 만료일** | 예약 빈도에 상관없이 예약된 프로젝트에 대한 최대 만료 날짜를 최대 1년으로 설정할 수 있습니다. | 해당 사항 없음 | 2023년 3월 8일 |
| **프로젝트에 대한 링크 공유(로그인 필요 없음)** - 비공개 Beta 액세스만 | <p>이제 Analysis Workspace 프로젝트에 대한 읽기 전용 링크를 Adobe Analytics 액세스 권한이 없는 사용자와 공유할 수 있습니다. 조직 외부 또는 Adobe Analytics에 대해 프로비저닝되지 않은 조직 내 사용자와 프로젝트 링크를 공유할 수 있습니다. [자세히 알아보기](/help/analyze/analysis-workspace/curate-share/share-projects.md)</p> <p>개인 Beta에 참여하려면 Adobe 계정 팀에 문의하십시오.</p> | 2023년 3월 15일(비공개 베타) | 2023년 4월 |

## Adobe Analytics의 수정 사항

AN-308177, AN-308727, AN-308846, AN-309591, AN-310614, AN-311544, AN-311570, AN-311665, AN-311948, AN-312108, AN-312114, AN-312142, 312143, AN-312389, AN-312391, AN-312431, AN-312453, AN-312454, AN-312458, AN-312503, AN-312533, AN-312682, AN-312698, AN-312714, AN-312738, AN-312807, 312829, AN-312849, AN-312875, AN-312980, AN-312997, AN-313059, AN-313077, AN-313110, AN-313195, AN-313196, AN-313258, AN-313554, AN-313580, AN-313702, AN-313820, AN-313844, AN-313859, AN-313879, AN-314273, AN-, AN-

## Adobe Analytics 관리자에 대한 중요 공지 {#admin}

| 공지 | 추가 또는 업데이트 일자 | 설명 |
| ----------- | ---------- | ---------- |
| **Google 클라이언트 힌트로 인한 디바이스 조회 업데이트** | 2023년 2월 27일 | 2023년 2월 16일로 예정되었던 클라이언트 힌트 사용은 힌트를 사용한 디바이스 조회 품질을 더 잘 보장하기 위해 연기되었습니다. 2023년 2월 27일에 클라이언트 힌트 지원을 위한 릴리스 첫 단계를 진행했습니다. 2023년 3월 2일(목) 릴리스의 2단계 및 최종 단계가 완료되었습니다. [자세히 알아보기](/help/technotes/client-hints.md) |
| **Analytics 소스 커넥터 가용성** | 2023년 2월 15일 | 2023년 2월 28일에 Analytics Source Connector를 캐나다에 있는 새 Adobe Experience Platform 데이터 센터에서 사용할 수 있게 되었습니다. |
| **분류 세트 아키텍처로 자동 마이그레이션** | 2023년 2월 8일 | Adobe는 앞으로 몇 달 동안 전 조직의 모든 분류를 최신 분류 아키텍처로 마이그레이션할 계획입니다. 마이그레이션할 마지막 고객은 2023년 5월에 발생할 것으로 예상됩니다. 고객 조치가 필요하지 않으며 중단 시간은 예상되지 않습니다. 이러한 새로운 아키텍처에는 다음과 같은 많은 이점이 있습니다.<ul><li>처리 시간 대폭 단축(72시간 → 24시간)</li><li>[분류 세트](/help/components/classifications/sets/overview.md) UI를 사용하는 기능</li><li>[분류 데이터용 Adobe Analytics 소스 커넥터](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/classifications.html?lang=ko-KR)를 통해 향후 Adobe Experience Platform에서 분류 데이터를 사용하는 옵션</li></ul>조직 워크플로에 잠재적으로 영향을 줄 수 있는 다음 변경 사항에 유의하십시오.<ul><li>브라우저 또는 FTP 가져오기를 사용하는 경우, &#39;[!UICONTROL 충돌 시 덮어쓰기]&#39;가 항상 활성화됩니다.</li><li>브라우저 또는 FTP 가져오기를 사용할 때 가져오기 직후 내보내기 옵션은 더 이상 지원되지 않습니다.</li><li>Analytics 2.0 API `GetDimensions` 엔드포인트는 이제 숫자 식별자 대신 분류에 대한 문자열 식별자를 반환합니다. 숫자 식별자를 계속 사용할 수 있지만 가능한 경우 새 문자열 식별자를 사용하는 것이 좋습니다. 숫자 식별자는 `?expansion=hidden` 쿼리 문자열 매개변수를 사용하여 검색할 수 있습니다.</li></ul>조직에 대한 보다 구체적인 마이그레이션 일정을 원하거나 이 마이그레이션에 대한 질문/우려 사항이 있는 경우 Adobe 고객 지원 센터에 문의하십시오. [자세히 알아보기](/help/components/classifications/sets/overview.md) |

{style="table-layout:auto"}

## 서비스 종료(EOL) 알림 {#eol}

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **[!DNL Reports & Analytics]**&#x200B;에 대한 EOL | 2023년 3월 7일 | **2023년 12월 31일**&#x200B;부로 Adobe는 [!DNL Reports & Analytics] 및 관련 보고서와 기능에 대한 서비스를 중단할 예정입니다. [!DNL Reports & Analytics]가 제공하는 보고서, 시각화 및 기반 기술은 더 이상 Adobe의 기술 표준을 충족하지 않습니다. 대부분의 [!DNL Reports & Analytics] 기능은 [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=ko-KR)에서 사용할 수 있습니다. 2015년 Analysis Workspace가 출시된 이후 [!DNL Reports & Analytics] 기능이 Analysis Workspace로 이전되면서 워크플로 패리티의 한계점에 도달했습니다. [이 공지 사항](https://spark.adobe.com/page/6WnF8JK6IRDhf/)은 서비스 종료 프로세스에 대해 설명합니다.<p>2023년 12월 31일에 예약된 보고서, 데이터 추출 및 DL 보고서를 포함하되 이에 국한되지 않는 많은 관련 Reports &amp; Analytics 기능이 종료됩니다. 2023년 12월 31일 이후에는 예약된 보고서가 더 이상 전송되지 않습니다. 위치 **2023년 4월**, 2023년 12월 31일 이후에 만료되도록 예약된 모든 보고서는 자동으로 업데이트되고 2023년 12월 31일에 만료되도록 되돌려집니다. 또한 2023년 12월 31일 이후에는 더 이상 향후 보고서를 예약할 수 없습니다. |
| **의 EOL [!UICONTROL 사람] 지표** | 2023년 2월 28일 | 의 사용 중단 시 [[!DNL Device Co-op]](https://experienceleague.adobe.com/docs/discontinued/using/device-co-op.html), Device Co-op 관련 사용자 지표는 더 이상 관련이 없습니다. 가까운 미래(날짜 TBD)에 이 항목을 제거합니다 [!UICONTROL 사람] 지표. 이 시점에서 해당 데이터를 [!UICONTROL 고유 방문자] 지표 를 사용하십시오.<p>**참고**: [[!UICONTROL 사람] 크로스 디바이스 분석에 연결된 지표](/help/components/metrics/people.md) 은(는) 이 발표의 영향을 받지 않습니다. |
| **[!UICONTROL 게시 목록] 기능의 EOL** | 2022년 9월 29일 | Reports &amp; Analytics 서비스 중단의 일환으로 [!UICONTROL 게시 목록] 다음 주에 수명이 종료될 예정입니다. **2023년 12월**. 새 항목을 만들거나 기존 항목에 액세스할 수 없습니다. [!UICONTROL 게시 목록] 전송 또는 예약하기 [!UICONTROL Analysis Workspace] 프로젝트. |
| **Data Workbench용 EOL** | 2022년 9월 14일 | Adobe는 **2023년 12월 31일**&#x200B;부로 Data Workbench의 서비스를 종료할 예정입니다. 자세한 내용은 [Data Workbench 서비스 종료 공지](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html?lang=ko-KR)를 참조하십시오. 문의 사항이 있으면 조직의 Adobe 계정 관리자에게 문의하십시오. |
| **[!DNL Reports & Analytics]**&#x200B;에 대한 EOL | 2022년 1월 4일 | **2023년 12월 31일**&#x200B;부로 Adobe는 [!DNL Reports & Analytics] 및 관련 보고서와 기능에 대한 서비스를 중단할 예정입니다. [!DNL Reports & Analytics]가 제공하는 보고서, 시각화 및 기반 기술은 더 이상 Adobe의 기술 표준을 충족하지 않습니다. 대부분의 [!DNL Reports & Analytics] 기능은 [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=ko-KR)에서 사용할 수 있습니다. 2015년 Analysis Workspace가 출시된 이후 [!DNL Reports & Analytics] 기능이 Analysis Workspace로 이전되면서 워크플로 패리티의 한계점에 도달했습니다. [이 공지 사항](https://spark.adobe.com/page/6WnF8JK6IRDhf/)은 서비스 종료 프로세스에 대해 설명합니다. |

{style="table-layout:auto"}

## AppMeasurement

AppMeasurement 릴리스(버전 2.23.0)에 대한 최신 업데이트는 [JavaScript용 AppMeasurement 릴리스 정보](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=ko-KR)를 참조하십시오.


## 관련 리소스

* [2022년 이전 릴리스 정보](/help/release-notes/2022.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=ko-KR)
* [Media Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=ko-KR)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트
