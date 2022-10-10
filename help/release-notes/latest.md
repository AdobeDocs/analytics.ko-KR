---
title: 최신 Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 1843989f77482152adeaee1f1c9e523d0c55dc21
workflow-type: ht
source-wordcount: '1511'
ht-degree: 100%

---

# 현재 Adobe Analytics 릴리스 정보 (2022년 10월)

**마지막 업데이트**: 2022년 10월 5일

Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 제공 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이러한 릴리스 정보를 정기적으로 확인하십시오.

## 관련 리소스

* [2022년 이전 릴리스 정보](/help/release-notes/2022.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=ko-KR)
* [Media Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=ko-KR)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트

## Adobe Analytics의 새로운 기능 또는 업데이트

| 기능 | 설명 | [목표 일자](releases.md) |
| ----------- | ---------- | ------- |
| **[!UICONTROL 주요 지표 요약]** 시각화 | [!UICONTROL 주요 지표 요약] 시각화를 통해 단일 기간 내에서 중요한 지표의 추세를 확인할 수 있습니다. 또한 두 기간에 걸쳐 지표의 성능을 비교할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/key-metric.html?lang=ko) | 2022년 10월 5일부터 단계적으로 롤아웃 |
| 새로운 **[!UICONTROL 분류 설정]** 사용자 경험 | 새 사용자 경험은 분류 및 규칙을 관리하고 고객 소유 분류 데이터의 가시성을 향상시키는 단일 인터페이스를 제공합니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/components/classifications/sets/overview.html?lang=ko) | 2022년 10월 5일 |
| 모바일 앱: **사용자 정의 상세 보기** | 사용자 정의 상세 보기를 사용하면 대상자가 가장 중요한 것에 집중할 수 있도록 함으로써 대상자와 공유하는 정보에 대해 훨씬 더 정확하게 지정할 수 있습니다. 각 스코어카드 타일과 관련된 상세 보기의 레이아웃을 변경하고 텍스트를 추가하여 최종 사용자가 데이터에서 볼 수 있는 내용을 더 잘 설명할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/analyze/mobapp/create-scorecard.html?lang=ko) | 2022년 10월 5일 |

{style=&quot;table-layout:auto&quot;}

## Adobe Analytics의 수정 사항

AN-298512; AN-300117; AN-301754; AN-301584; AN-301685; AN-301783; AN-301818; AN-301825; AN-301834; AN-301965; AN-302095; AN-302189; AN-302269; AN-302290; AN-302301; AN-302348; AN-302531; AN-302533;


## Adobe Analytics 관리자에 대한 중요 공지

| 공지 | 추가 또는 업데이트 일자 | 설명 |
| ----------- | ---------- | ---------- |
| **기본 랜딩 페이지** | 2022년 9월 29일 | 올해 초에 도입된 [새 랜딩 페이지](/help/analyze/landing.md)는 **2023년 1월**&#x200B;에 모든 사용자의 기본 환경이 됩니다. 현재 페이지는 더 이상 사용되지 않으며 모든 사용자는 새 환경을 사용해야 합니다. |
| **[!UICONTROL 게시 목록] 기능의 EOL** | 2022년 9월 29일 | Reports &amp; Analytics EOL의 일환으로 게시 목록은 **2023년 12월**&#x200B;에 사용 수명이 종료됩니다. Analysis Workspace 프로젝트를 보내거나 예약하기 위해 새 게시 목록을 만들거나 기존 게시 목록에 액세스할 수 없습니다. [자세히 알아보기](/help/admin/admin/publishing-list.md) |
| **[!UICONTROL 예외 항목 탐지] 자동 실행 조건** | 2022년 9월 29일 | 오늘, [!UICONTROL 예외 항목 탐지]가 시계열 자유 형식 테이블의 모든 열에서 자동 실행됩니다. 데이터를 분석에 사용할 수 있고 프로젝트를 더 빠르게 로드할 수 있도록 Adobe는 예외 항목 탐지 자동 실행 방식을 변경할 것입니다. **2022년 10월 26일**&#x200B;부터 [!UICONTROL 예외 항목 탐지]는 테이블의 첫 번째 지표 열에서만 자동 실행됩니다. 필요한 경우 다른 열에서 예외 항목 탐지를 실행하도록 열 설정을 구성할 수 있습니다. |
| **새로운 NetAcuity 통신사 데이터베이스로 업데이트** | 2022년 9월 26일 | 원래 2022년 10월 5일로 계획되었던 이 업데이트는 **2023년 1월**&#x200B;로 연기되었습니다. Adobe Analytics Data Warehouse 및 Analytics 데이터 피드의 `carrier` 필드에 저장된 통신사 관련 정보가 변경될 예정입니다. 지금까지 해당 열의 데이터 형식은 `<domain>:<ISP>`였습니다. Adobe는 Adobe Analytics 보고 도구(Analysis Workspace, Reports &amp; Analytics, 보고 API, Data Warehouse, 라이브스트림 등)에서 보고 목적으로 이러한 `<domain>:<ISP>` 값을 통신사 이름으로 매핑하기 위한 내부 조회 테이블을 유지 관리했습니다. 조회 파일(`carrier.tsv`)에는 데이터 피드가 제공되어 동일한 매핑을 사용할 수 있습니다.<p>이 업데이트는 NetAcuity의 보다 정확한 통신사 데이터베이스를 사용하여 통신사 매핑을 향상시킵니다. 데이터 피드의 통신사 열에 있는 데이터 형식은 향후 변경될 예정입니다. `<domain>:<ISP>` 대신 통신사 이름이 포함됩니다. Adobe는 계속해서 조회 테이블을 사용하여 가능한 한 과거 보고서와의 연속성을 유지할 것입니다. Adobe에서 조회를 적용하는 보고 도구 (Analysis Workspace, Reports &amp; Analytics, 보고 API, Data Warehouse, 라이브스트림 등) 보다 정확한 매핑의 이점을 얻을 수 있습니다. 일부 매핑(특히 국제 도메인 및 ISP의 경우)은 Adobe가 새 데이터베이스를 채택할 때 다른 매핑보다 더 많이 변경될 수 있습니다. 데이터 피드 통신사 조회 파일(`carrier.tsv`)은 이전 매핑을 유지하고 새 매핑을 추가합니다.<p>Analytics Source Connector는 현재 통신사 필드를 매핑하지 않으므로 현재 Experience Platform, CJA 등에서 통신사 보고를 사용할 수 없습니다. 따라서 새 통신사 데이터베이스를 사용하더라도 Analytics Source Connector에서 제공한 데이터를 기반으로 하는 Experience Platform의 어떤 것에도 영향을 미치지 않습니다. |
| **개선된 IP-to-geolocation 매핑** | 2022년 9월 26일 | 당사의 IP 조회 공급업체인 Digital Element는 IP-to-geolocation 매핑을 위해 새롭게 개선된 데이터 세트(NetAcuity Pulse)로 업그레이드하고 있습니다. 원래 2022년 10월로 계획되었던 일정이 변경되었으며 Adobe Analytics는 **2023년 1월**&#x200B;에 이 새로운 데이터 세트를 채택할 예정입니다. 새 데이터베이스는 이전 버전보다 더 정확합니다. 새 데이터베이스가 채택되면 일부 IP-to-geo 매핑이 변경 및 개선됩니다.<p>모든 Adobe Analytics 도구 (Analysis Workspace, Reports &amp; Analytics, 보고 API, Data Warehouse, 라이브스트림 등) 새롭게 개선된 매핑을 자동으로 활용합니다. 데이터 피드의 데이터 형식은 변경되지 않습니다. Analytics Source Connector를 통해 제공되는 CJA 데이터도 자동으로 새 매핑을 활용합니다. |
| **SFTP 업그레이드** | 2022년 9월 19일 | 이전에 Adobe는 파일 전송에 대한 보안을 개선하기 위해 2022년 9월에 SFTP(Secure File Transfer Protocol) 서비스를 업그레이드할 예정임을 공지했습니다. Adobe는 이 업그레이드를 **2022년 9월 20일**&#x200B;에 수행했습니다. 이 변경 사항이 적용되었으며 일부 SFTP 클라이언트 구성은 더 이상 지원되지 않습니다. 이는 SFTP를 사용하여 Adobe Analytics로 전송되거나 Adobe Analytics에서 검색된 데이터에만 영향을 미칩니다. FTP 프로토콜은 영향을 받지 않습니다. 서비스가 중단되는 것을 방지하려면 SFTP 클라이언트(코드, 도구, 서비스)가 [여기](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html)에 설명된 변경 사항을 준수하는지 확인하십시오. |
| **Data Workbench용 EOL** | 2022년 9월 14일 | Adobe는 **2023년 12월 31일**&#x200B;부로 Data Workbench의 서비스를 종료할 예정입니다. 질문이 있는 경우 고객 지원 센터 담당자에게 문의하여 Data Workbench에 대한 대체 솔루션을 확인하십시오. |
| **Google 클라이언트 힌트로 인한 디바이스 조회 업데이트** | 2022년 8월 19일 | **2022년 10월 26일**&#x200B;부터 Adobe는 Google Chrome 및 Microsoft Edge와 같은 Chromium 브라우저에서 발생한 히트에 대한 특정 디바이스 정보를 가져올 때 사용자 에이전트와 함께 클라이언트 힌트를 사용할 예정입니다. 이는 클라이언트 힌트를 통해 전달되는 데이터 대신 사용자 에이전트 문자열에서 제공되는 정보를 점차적으로 줄이려는 Google의 계획에 따른 것입니다. 클라이언트 힌트에 대한 자세한 내용은 [여기](https://web.dev/user-agent-client-hints/)에서 확인하십시오.<p> AppMeasurement 및 Web SDK 수집 라이브러리는 모두 클라이언트 힌트 수집 및 높은 엔트로피 클라이언트 힌트 수집 여부 구성을 10월까지 지원합니다. 이 변경 내용의 일부로 Adobe는 사용자 에이전트와 관련된 모든 디바이스 조회에 Device Atlas를 사용하게 됩니다. 현재 Device Atlas는 모바일 조회에만 사용됩니다. 이러한 업데이트로 인해 사용자 에이전트(특히 브라우저, 브라우저 유형, 운영 체제, 운영 체제 유형 및 모바일 디바이스)에서 파생된 디바이스 정보가 약간 변경될 수 있습니다. [자세히 알아보기](/help/technotes/client-hints.md) |
| **Reports &amp; Analytics에서 예약된 보고서 일시 중지** | 2022년 6월 8일 | 2022년 4월 21일에 Adobe는 이전에 발표된 Reports &amp; Analytics의 서비스 종료에 대비하여 예약된 보고서와 관련된 몇 가지 기능의 사용 중단을 발표했습니다. 이들 기능에는 새 보고서와 새 데이터 추출을 예약하는 기능이 포함되었습니다.<p>확장을 원하는 고객의 요청에 따라 Reports &amp; Analytics에서 쉽게 전환할 수 있도록 Adobe는 이러한 기능에 대한 액세스를 **2023년 1월 31일**&#x200B;까지 연장하기로 결정했습니다. 보고서와 데이터 추출의 만료 기간은 계속 9개월로 제한됩니다. 보고서 및 데이터 추출 전달은 일정이 다시 활성화되지 않는 한 이 기간이 끝나면 일시 중지됩니다.<p>반복해서 말씀드리지만 이들 기능은 2023년 1월 31일에 사용이 중단됩니다. 해당 날짜 이전에 예약된 보고를 Adobe Analytics에서 사용할 수 있는 다른 메커니즘 중 하나로 마이그레이션해야 합니다. 추가 질문이 있거나 지원이 필요한 경우 Adobe 고객 지원 센터에 문의하십시오. [자세히 알아보기](/help/analyze/reports-analytics/scheduled-reports-eol.md) |
| **Report Builder에서 예약된 작업 일시 중지** | 2022년 6월 8일 | 2022년 4월 21일에 Adobe는 최적의 성능과 제공을 위한 노력의 일환으로 Report Builder의 예약된 작업에 대한 변경 사항이 배포되었습니다. 이러한 변경 사항에는 예약된 배달이 “x회 발생 후 종료”되도록 하는 기능의 제거가 포함되었습니다. 대안을 탐색하고 구현하기 위해 더 많은 시간을 요구하는 여러 고객 요청에 따라 Adobe는 **2023년 1월 31일**&#x200B;까지 제한된 방식으로 이 옵션을 복원하기로 결정했습니다.<p>계속해서 시간별 Report Builder 작업을 예약하고 최대 99회 발생 후 종료되도록 할 수 있습니다. 롤백은 시간별 작업에만 적용됩니다. “x회 발생 후 종료”는 다른 모든 제공 간격(일별, 주별, 월별 및 연간)에 대해 계속 사용할 수 없습니다. 이 옵션은 2023년 1월 31일에 사용이 중단됩니다. 추가 질문이 있거나 지원이 필요한 경우 Adobe 고객 지원 센터에 문의하십시오. [자세히 알아보기](/help/analyze/report-builder/r-arb-scheduled-reports.md) |
| **[!DNL Reports & Analytics]**&#x200B;에 대한 EOL | 2022년 1월 4일 | **2023년 12월 31일**&#x200B;부로 Adobe는 [!DNL Reports & Analytics] 및 관련 보고서와 기능에 대한 서비스를 중단할 예정입니다. [!DNL Reports & Analytics]가 제공하는 보고서, 시각화 및 기반 기술은 더 이상 Adobe의 기술 표준을 충족하지 않습니다. 대부분의 [!DNL Reports & Analytics] 기능은 [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=ko-KR)에서 사용할 수 있습니다. 2015년 Analysis Workspace가 출시된 이후 [!DNL Reports & Analytics] 기능이 Analysis Workspace로 이전되면서 워크플로 패리티의 한계점에 도달했습니다. [이 공지 사항](https://spark.adobe.com/page/6WnF8JK6IRDhf/)은 서비스 종료 프로세스에 대해 설명합니다. |

{style=&quot;table-layout:auto&quot;}

## AppMeasurement

AppMeasurement 릴리스(버전 2.23.0)에 대한 최신 업데이트는 [JavaScript용 AppMeasurement 릴리스 정보](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=ko-KR)를 참조하십시오.
