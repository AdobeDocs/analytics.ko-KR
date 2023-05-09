---
title: 최신 Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: d1fd0aa0312b8fb6112cde22a53c58eb3be791a2
workflow-type: tm+mt
source-wordcount: '1239'
ht-degree: 62%

---

# 현재 Adobe Analytics 릴리스 정보 (2023년 5월)

**마지막 업데이트**: 2023년 5월 8일

Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## Adobe Analytics의 새로운 기능 또는 업데이트 {#features}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **비프로덕션 샌드박스용 채우기** | 비프로덕션 샌드박스에서 Analytics 소스 커넥터 데이터 흐름을 생성할 때 비프로덕션 샌드박스의 채우기는 3개월로 제한됩니다. 프로덕션 샌드박스의 경우 13개월로 유지됩니다. | 해당 사항 없음 | 2023년 4월 26일 |
| **프로젝트 링크 공유 (로그인 불필요)** | 이제 Adobe Analytics에 액세스할 수 없는 사용자에게 Analysis Workspace 프로젝트에 대한 읽기 전용 링크를 공유할 수 있습니다. 여기에는 조직 외부의 사람 또는 Adobe Analytics에 대해 프로비저닝되지 않은 조직 내의 사람과의 공유가 포함됩니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/share-projects.html?lang=en#share-public-link)<p>이 기능은 기본적으로 활성화되어 있으며 시스템 관리자가 비활성화할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/user-preferences.html?lang=en#company-preferences)</p> | 2023년 5월 3일 | 2023년 6월 |
| **Analytics 대시보드 앱(모바일 앱)에 대한 홈 화면이 업데이트되었습니다** | 새로 업데이트된 홈 화면에서 하나의 통합 스코어카드 목록에서 모든 스코어카드를 볼 수 있습니다.  한 번의 로그인으로 두 개 이상의 조직에 액세스할 수 있는 경우 조직의 모든 스코어카드를 단일 목록에서 사용할 수 있습니다. | 해당 사항 없음 | 2023년 5월 10일 |
| **Analysis Workspace에서 구성 요소 정렬** | 이제 왼쪽 레일이나 Analysis Workspace의 데이터 사전에서 구성 요소를 볼 때 새 정렬 옵션을 사용할 수 있습니다. 구성 요소를 권장(가장 일반적으로 사용되는 항목), 알파벳 또는 카테고리적(유형)별로 정렬할 수 있습니다.<p>이전에는 구성 요소를 검색하거나 필터링할 수만 있었습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/analysis-workspace-components.html?lang=en)</p> | 해당 사항 없음 | 2023년 5월 10일 |
| **자유 형식 테이블에서 동적 차원이 포함된 행 삭제** | 이제 Analysis Workspace의 자유 형식 테이블에서 x 아이콘을 사용하여 동적 차원이 포함된 특정 행을 빠르게 삭제할 수 있습니다. 이 경우 &quot;다음과 같지 않음&quot; 필터 규칙이 자동으로 적용됩니다.<p>이전에는 동적 차원이 포함된 행을 삭제하는 유일한 방법은 필터 대화 상자에서 규칙을 수동으로 만드는 것이었습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-table/filter-and-sort.html?lang=en)</p> | 해당 사항 없음 | 2023년 5월 10일 |
| **패널 내에 시각화를 추가하는 새 단추** | 이제 Analysis Workspace의 각 패널 하단에 새 단추를 사용할 수 있으므로 시각화를 빠르게 추가할 수 있습니다. <p>이전에는 시각화를 패널에 추가하는 유일한 방법은 왼쪽 레일에서 시각화를 드래그하거나 기존 시각화를 복제하거나 복사하거나 빈 패널을 만드는 것이었습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html?lang=en#quick-viz)</p> | 해당 사항 없음 | 2023년 5월 10일 |
| **딥 링크(모바일 앱)** | 사용자가 앱의 스코어카드 프로젝트로 바로 안내하는 스코어카드에 대한 링크를 전송할 수 있습니다. 따라서 프로젝트를 보다 쉽게 공유하고 기술적인 지식이 부족한 대상으로부터의 참여를 늘릴 수 있습니다. | TBD | TBD |

{style="table-layout:auto"}

## Adobe Analytics의 수정 사항

AN-312098; AN-318309; AN-316675; AN-318173; AN-310359; AN-317613; AN-318836; AN-315744; AN-311772; AN-318719; AN-314074; AN-316651<!--"Verified" status-->; AN-318602; AN-315961; AN-317534; AN-318607; AN-316498; AN-316648; AN-318244; AN-317747; AN-318432; AN-318231; AN-317590; AN-318415; AN-318154; AN-316647; N-314417; AN-317614; AN-317725; AN-318114; AN-317876; AN-318052; AN-317966; AN-316477; AN-318036; AN-317931; AN-318045; AN-316246; AN-317281; AN-317879; AN-308077; AN-317708; AN-316115; AN-315963

## Adobe Analytics 관리자에 대한 중요 공지 {#admin}

| 공지 | 추가 또는 업데이트 일자 | 설명 |
| ----------- | ---------- | ---------- |
| **알림: 런던 데이터 센터의 Adobe Analytics 데이터 피드 및 Data Warehouse 헤드에서 사용하는 새 IP** | 2023년 4월 27일 | 데이터 피드 요청 및/또는 Data Warehouse 보고서가 FTP/SFTP 서비스로 전달되는 런던 데이터 센터의 고객의 경우 액세스를 허용하려면 방화벽 구성에 다음 IP 주소 범위를 추가해야 합니다. <ul><li>130.248.244.32/29</li><li>130.248.244.40/29</li></ul> |
| **디바이스 조회 프로세스는 이제 모든 디바이스 조회에 서드파티를 사용합니다** | 2023년 3월 3일 | 2023년 3월 2일 클라이언트 힌트 지원 롤아웃의 일환으로 모든 디바이스 조회에 서드파티를 사용하도록 디바이스 조회 프로세스를 업데이트했습니다. 이전에는 모바일 디바이스 조회에만 서드파티를 사용했습니다. 상기 롤아웃에서 일부 데스크탑 운영 체제에 “모바일”이라는 텍스트가 잘못 표시되어 있습니다(예: “OS X 10.15.7” 대신 “모바일 OS X 10.15.7”).<p>Adobe의 4월 릴리스에서 이들 이름을 수정할 예정입니다. Analytics 및 CJA 보고는 이벤트 데이터의 일부로 기록된 ID를 기반으로 운영 체제 이름을 조회하므로 소급하여 업데이트됩니다. ID에 해당하는 조회 값이 업데이트되면 내역 데이터를 포함하여 모든 보고가 수정됩니다. [!UICONTROL 데이터 피드] 고객의 경우 보고 시 유사한 조회 프로세스를 사용하면 변경이 소급 적용됩니다. 그러나 이벤트 데이터에 운영 체제 값을 저장하면 전향적으로만 보고가 업데이트됩니다. 자세한 내용은 [운영 체제](/help/components/dimensions/operating-systems.md)를 참조하십시오. |

{style="table-layout:auto"}

## 서비스 종료(EOL) 알림 {#eol}

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **일본 피처폰 추적 서비스 종료** | 2023년 3월 21일 | 일본 고객만 해당: **2023년 5월 말**&#x200B;에 일본 피처폰 추적 서비스(mod_ktrack)가 종료됩니다. 불편을 드려 죄송합니다. Apache 서버에 설치된 모듈을 제거하거나 비활성화하시기 바랍니다. [이 문서](/help/release-notes/mod_ktrackforSiteCatalyst_ver1.40.pdf)의 27페이지와 28페이지를 참조하십시오. |
| **[!DNL Reports & Analytics]**&#x200B;에 대한 EOL | 2023년 3월 7일 | **2023년 12월 31일**&#x200B;부로 Adobe는 [!DNL Reports & Analytics] 및 관련 보고서와 기능에 대한 서비스를 중단할 예정입니다. [!DNL Reports & Analytics]가 제공하는 보고서, 시각화 및 기반 기술은 더 이상 Adobe의 기술 표준을 충족하지 않습니다. 대부분의 [!DNL Reports & Analytics] 기능은 [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html)에서 사용할 수 있습니다. 2015년 Analysis Workspace가 출시된 이후 [!DNL Reports & Analytics] 기능이 Analysis Workspace로 이전되면서 워크플로 패리티의 한계점에 도달했습니다. [이 공지 사항](https://spark.adobe.com/page/6WnF8JK6IRDhf/)은 서비스 종료 프로세스에 대해 설명합니다.<p>2023년 12월 31일에 예약된 보고서, 데이터 추출, DL 보고서를 포함하되 이에 국한되지 않는 많은 관련 Reports &amp; Analytics 기능이 종료됩니다. 2023년 12월 31일 이후에는 예약된 보고서가 더 이상 전송되지 않습니다. **2023년 4월**, 2023년 12월 31일 이후에 만료되도록 예정된 모든 보고서가 자동으로 업데이트되고 2023년 12월 31일에 만료되도록 되돌려집니다. 또한 2023년 12월 31일 이후에는 더 이상 향후 보고서를 예약할 수 없습니다. |
| **[!UICONTROL 사용자] 지표의 EOL** | 2023년 3월 9일 | [[!DNL Device Co-op]](https://experienceleague.adobe.com/docs/discontinued/using/device-co-op.html) 중단으로 인해 Device Co-op과 관련된 사용자 지표는 더 이상 관련이 없습니다. 2023년 5월 8일부로 [!UICONTROL 사용자] 지표가 제거될 예정입니다. 프로젝트, 세그먼트 및 계산된 지표가 손상되지 않도록 해당 시점에 관련 데이터가 [!UICONTROL 고유 방문자] 지표로 리디렉션될 예정입니다.<p>**참고**: [Cross-Device Analytics에 연결된 사용자 지표](/help/components/metrics/people.md)는 이 공지의 영향을 받지 않습니다. |
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
