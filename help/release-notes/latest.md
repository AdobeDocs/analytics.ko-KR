---
title: 최신 Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 09a4f0865c0297681a05da4eae98412632931626
workflow-type: tm+mt
source-wordcount: '1514'
ht-degree: 87%

---

# 현재 Adobe Analytics 릴리스 정보 (2023년 6월)

**마지막 업데이트**: 2023년 6월 21일

Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 릴리스 하이라이트 {#highlights}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **데이터 복구 필터 개선 사항** | 데이터 복구에 세 가지 필터링 개선 사항이 추가되었습니다.<ul><li>한 개의 변수로 필터링하여 두 번째 변수를 수정합니다. 예를 들어 다음과 같습니다. `eVar2` &quot;@&quot;을(를) 포함한 다음 삭제 `eVar3`.</li><li>숫자 또는 숫자가 아닌 값 필터링</li><li>AND로 여러 필터를 적용합니다. 예를 들어, `eVar2="a"` 및 `eVar3="b"`</li></ul>[자세히 알아보기](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/data-repair/) | 2023년 6월 21일 | 2023년 7월 12일 |
| **프로젝트 링크 공유 (로그인 불필요)** | 이제 Adobe Analytics에 액세스할 수 없는 사용자에게 Analysis Workspace 프로젝트에 대한 읽기 전용 링크를 공유할 수 있습니다. 여기에는 조직 외부의 사용자 또는 Adobe Analytics용으로 프로비저닝되지 않은 조직 내의 사용자와의 공유가 포함됩니다. [자세히 알아보기](../analyze/analysis-workspace/curate-share/share-projects.md#share-a-project-with-anyone-no-login-required)<p>이 기능은 기본적으로 활성화되어 있으며 시스템 관리자가 비활성화할 수 있습니다. [자세히 알아보기](../analyze/analysis-workspace/user-preferences.md#company-preferences)</p> | 2023년 5월 3일 | 2023년 6월 7일 |
| **분류 세트를 위한 새로운 기능** | [분류 세트](/help/components/classifications/sets/overview.md) 다음과 같은 몇 가지 새로운 기능이 업데이트되었습니다.<ul><li>**통합**: 분류 세트를 하나의 통합된 분류 세트로 결합합니다. 통합 분류 세트는 다른 분류 세트처럼 또는 Customer Journey Analytics에서 조회 데이터 세트로 사용할 수 있습니다. [자세히 알아보기](../components/classifications/sets/consolidations/manage.md)</li><li>**규칙**: 분류 세트의 규칙을 기반으로 값을 자동으로 분류합니다. [자세히 알아보기](../components/classifications/sets/manage/rules.md)</li><li>**자동 가져오기**: 클라우드 스토리지 대상에서 분류 데이터를 자동으로 가져옵니다. [자세히 알아보기](../components/classifications/sets/manage/schema.md)</li></ul> | | 2023년 6월 7일 |
| **새로운 AppMeasurement 변수** | `doubleEncodeLinkParameters` 변수는 구현으로 링크 추적 변수에서 멀티바이트 문자를 인코딩하는 극단적 사례를 포함합니다. 대부분의 구현에서는 이 변수를 정의하지 않아도 됩니다. [자세히 알아보기](../implement/vars/config-vars/doubleencodelinkparameters.md) |  | 2023년 6월 7일 |
| **데이터 피드 내보내기를 위한 보안 대상** | 이제 데이터 피드를 다음 클라우드 스토리지 대상으로 보낼 수 있습니다.<ul><li>Amazon S3</li><li>Azure RBAC</li><li>Azure SAS</li><li>Google Cloud 플랫폼</li></ul>이전에 사용할 수 있었던 대상(FTP, SFTP, S3 및 Azure Blob)은 더 이상 권장되지 않습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/create-feed.html) | 2023년 6월 12일 | 2023년 7월 15일 |
| **작업 영역의 봇 보고** | 이제 Analysis Workspace에서 봇 보고를 사용할 수 있습니다. 이 기능에는 다음과 같은 몇 가지 추가 기능이 있습니다.<ul><li>새 차원: [봇 이름](/help/components/dimensions/bot-name.md)</li><li>두 개의 새로운 지표: [봇 페이지 조회수](/help/components/metrics/bot-page-views.md) 및 [봇 발생 횟수](/help/components/metrics/bot-occurrences.md).</li><li>새로 계산된 지표 템플릿: [봇 페이지 조회수 비율](/help/components/c-calcmetrics/cm-reference/default-calcmetrics.md)</li><li>새로운 Workspace 보고서: 봇 보고</li></ul>새 차원 및 지표에는 2023년 3월부터 채워지는 데이터가 포함됩니다. |  | 2023년 6월 7일 |

{style="table-layout:auto"}

## 기타 새로운 기능 또는 업데이트된 기능 {#other}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **자유 형식 테이블에서 동적 차원이 포함된 행 삭제** | 이제 Analysis Workspace의 자유 형식 테이블에서 x 아이콘을 사용하여 동적 차원이 포함된 특정 행을 신속하게 삭제할 수 있습니다. 이렇게 하면 “항상 항목 제외” 필터 규칙이 자동으로 적용됩니다.<p>이전에는 동적 차원이 포함된 행을 삭제하는 유일한 방법은 필터 대화 상자에서 수동으로 규칙을 만드는 것이었습니다. [자세히 알아보기](/help/analyze/analysis-workspace/visualizations/freeform-table/filter-and-sort.md)</p> | 해당 사항 없음 | 2023년 5월 17일 |
| **패널 내에 시각화를 추가하는 새 버튼** | 이제 Analysis Workspace의 각 패널 하단에 새로운 버튼이 추가되어 시각화를 빠르게 추가할 수 있습니다. <p>이전에는 패널에 시각화를 추가하는 유일한 방법은 왼쪽 레일에서 시각화를 드래그하거나, 기존 시각화를 복제 또는 복사하거나, 빈 패널을 만드는 것이었습니다. [자세히 알아보기](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md)</p> | 해당 사항 없음 | 2023년 5월 17일 |
| **딥 링크 (모바일 앱)** | 사용자가 앱의 스코어카드 프로젝트로 바로 연결되는 스코어카드 링크를 보낼 수 있습니다. 이를 통해 프로젝트를 보다 쉽게 공유하고 기술 수준이 낮은 대상자의 참여를 높일 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/analyze/mobapp/create-scorecard.html#share-scorecards-using-a-shareable-link) | 해당 사항 없음 | 2023년 5월 17일 |
| **동적 드롭다운 필터** | 패널의 보고 범위 내의 데이터 및 기타 드롭다운 필터의 값을 기반으로 사용 가능한 값을 결정하는 새로운 유형의 드롭다운 필터를 도입하고 있습니다. [!UICONTROL Shift] 키를 누른 상태에서 차원을 패널 드롭 영역으로 드래그하면 동적 드롭다운 필터를 사용할 수 있습니다. [!UICONTROL Shift] 키를 누른 상태에서 차원 항목 그룹을 패널 드롭 영역으로 드래그하면 정적 드롭다운 필터가 변경되지 않은 상태로 유지됩니다. [자세히 알아보기](/help/analyze/analysis-workspace/c-panels/panels.md) |  | 2023년 6월 14일 |
| **업데이트된 분석 학습 페이지** | 이제 Adobe Analytics 랜딩 페이지의 학습 탭에 다음과 같은 개선 사항이 포함됩니다.<ul><li>개선된 탐색 기능으로 단일 페이지에 더 많은 학습 콘텐츠를 표시하는 개선된 디자인</li><li>경험 수준(초급, 중급, 고급)에 따라 학습 콘텐츠를 맞춤 설정하는 기능</li></ul>[자세히 알아보기](/help/analyze/landing.md) |  | 2023년 6월 30일 |
| **Analysis Workspace의 구성 요소 정렬** | 이제 왼쪽 레일 또는 Analysis Workspace의 데이터 사전에서 구성 요소를 볼 때 새로운 정렬 옵션을 사용할 수 있습니다. 권장(가장 일반적으로 사용되는 구성 요소), 알파벳순 또는 범주(유형)별로 구성 요소를 정렬할 수 있습니다.<p>이전에는 구성 요소만 검색하거나 필터링만 할 수 있었습니다. [자세히 알아보기](/help/analyze/analysis-workspace/components/analysis-workspace-components.md)</p> | 해당 사항 없음 | TBD |

{style="table-layout:auto"}

## Adobe Analytics의 수정 사항

-311878; -313968; AN-314130; AN-315701; AN-315761; AN-316613; AN-317563; AN-318829; AN-319009; AN-319043; AN-319066; AN-; AN-; AN-319166; AN-319245; AN-319271; AN-319381; AN-319391; AN-319482; AN-319621; AN-319637; AN-319676; AN-320176; AN-320221; AN-320225; AN-320286; AN-320312; AN-320316; AN-320449; AN-320477; AN-320492; AN-320538; AN-320556; AN-320569; AN-320679; AN-320684; AN-320786; AN-320802; AN-320811; AN-320812; AN-320815; AN-321032; AN-321033; AN-321070; AN-321096; AN-321105; AN-321122; AN-321337;

## Adobe Analytics 관리자에 대한 중요 공지 {#admin}

| 공지 | 추가 또는 업데이트 일자 | 설명 |
| ----------- | ---------- | ---------- |
| **구매 ID 및 이벤트 ID의 37개월 만료(이벤트 일련화)** | 2023년 5월 25일 | **2023년 6월 말 또는 2023년 7월 초**&#x200B;에 출시되는 Analytics Hit 처리 엔진의 다음 릴리스에서는 구매 ID 및 이벤트 ID의 37개월 만료(이벤트 일련화)가 적용될 예정입니다. 현재 구매 ID 및 이벤트 ID는 Adobe Analytics에서 만료되지 않습니다. 구매 ID 또는 이벤트 ID가 표시/사용되면 이후 히트는 언제라도 해당 구매 또는 이벤트가 중복으로 표시됩니다. 새로운 처리 엔진 릴리스:<ul><li>구매 ID 및 이벤트 ID는 항상 37개월 후에 만료됩니다.</li><li>구매 ID 또는 이벤트 ID를 조회한 후 37개월이 경과한 경우에는 더 이상 중복 구매 또는 이벤트로 간주되지 않습니다.</li><li> 37개월 이전의 구매 ID 또는 이벤트 ID를 “재사용”하는 경우, 더 이상 중복으로 간주되지 않습니다.</li></ul> |
| **Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션** | 2023년 5월 11일 | Adobe I/O JWT 자격 증명을 사용하는 Adobe Analytics API 및 라이브스트림 고객은 다음 작업을 수행하여 Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. **2025년 1월 1일**. 자세한 내용과 타임라인은 아래 표의 수명 종료 알림을 참조하십시오. |
| **런던 데이터 센터의 Adobe Analytics 데이터 피드 및 Data Warehouse 이그레스에 사용되는 새로운 IP** | 2023년 4월 27일 | 이는 데이터 피드 요청 및/또는 Data Warehouse 보고서가 FTP/SFTP 서비스로 전달되는 런던 데이터 센터의 고객과 관련이 있습니다. 액세스를 허용하려면 다음 IP 주소 범위를 방화벽 구성에 추가해야 합니다. <ul><li>130.248.244.32/29</li><li>130.248.244.40/29</li></ul> |

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
