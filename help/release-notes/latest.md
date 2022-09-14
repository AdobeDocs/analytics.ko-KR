---
title: 최신 Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 1622f69e4d2a19d72e5748d165567d0bf7c5f83c
workflow-type: tm+mt
source-wordcount: '1312'
ht-degree: 62%

---

# 현재 Adobe Analytics 릴리스 노트(2022년 9월)

**마지막 업데이트**: 2022년 9월 14일

## 관련 리소스

* [2022년 이전 릴리스 정보](/help/release-notes/2022.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=ko-KR)
* [Media Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=ko-KR)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트

## Adobe Analytics의 새로운 기능 또는 업데이트

| 기능 | 설명 | [목표 날짜](releases.md) |
| ----------- | ---------- | ------- |
| 작업 공간의 콤보 차트 시각화 | 콤보 차트를 사용하면 Workspace 내에서 지표를 보다 쉽고 직관적으로 비교할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/combo-charts.html) | 2022년 9월 14일 |

{style=&quot;table-layout:auto&quot;}

## Adobe Analytics의 수정 사항

* 분류 가져오기 및 내보내기와 관련된 문제가 해결되었습니다. (AN-299267)

**개인 사용자 고객에 대한 수정 사항**:

AN-288519; AN-289300; AN-297387; AN-297465; AN-297520; AN-297641; AN-298134; AN-298351; AN-298429; AN-298483; AN-298520; AN-298582; AN-298816; AN-298832; AN-298855; AN-298864; AN-299407; AN-299545; AN-299644; AN-299715

## Adobe Analytics 관리자에 대한 중요 공지

| 공지 | 추가 또는 업데이트 날짜 | 설명 |
| ----------- | ---------- | ---------- |
| **Analytics에서 Experience Edge를 통해 수집된 A4T 데이터를 처리하는 방법 변경** | 2022년 9월 14일 | 2022년 3월에 Analytics는 A4T 데이터를 포함하는 Experience Edge에서 시작된 일부 호출을 처리하는 방법을 변경했습니다. A4T 보고 컨텐츠가 있는 히트는 페이지 보기(`t()`) 또는 링크 추적(`tl()`) events에 할당하는 방법을 보여줍니다. 이제 이 논리가 다음 위치의 경우를 포함하도록 업데이트됩니다. `propositionDisplay` 이벤트가 의도한 대로 수정되지 않았습니다. |
| **웹 SDK의 목록 변수 및 목록 속성에 대한 자동 구분 기호** | 2022년 9월 14일 | 이제 목록 변수 및 목록 prop은 XDM에 구분 기호 무시를 지정하지 않는 한 보고서 세트 설정에 지정된 구분 기호를 사용합니다. 자세한 내용은 [list](/help/implement/vars/page-vars/list.md) 변수를 참조하십시오. |
| **SFTP 업그레이드** | 2022년 9월 14일 | 이전에는 Adobe이 파일 전송에 대한 개선된 보안을 제공하기 위해 Adobe이 2022년 9월에 SFTP(Secure File Transfer Protocol) 서비스를 업그레이드한다고 통신했습니다. Adobe이 이 업그레이드를 연기했습니다. **2022년 9월 중후반**. 이 변경 사항이 발생하면 특정 SFTP 클라이언트 구성이 더 이상 지원되지 않습니다. 이는 SFTP를 사용하여 Adobe Analytics로 전송되거나 Adobe Analytics에서 검색된 데이터에만 영향을 미칩니다. FTP 프로토콜은 영향을 받지 않습니다. 서비스가 중단되는 것을 방지하려면 SFTP 클라이언트(코드, 도구, 서비스)가 [여기](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html)에 설명된 변경 사항을 준수하는지 확인하십시오. |
| **Data Workbench용 EOL** | 2022년 9월 14일 | Adobe은 수명 종료 Data Workbench 유효 기간 종료 **2023년 12월 31일**. 질문이 있는 경우 Data Workbench에 대한 대체 해결 방법은 고객 지원 담당자에게 문의하십시오. |
| **Google 클라이언트 힌트로 인한 디바이스 조회 업데이트** | 2022년 9월 14일 | 시작 **2022년 9월 29일**, Adobe은 Google Chrome 및 Microsoft Edge와 같이 Chromium 브라우저에서 발생하는 히트에 대한 특정 장치 정보를 도출할 때 사용자 에이전트 외에도 클라이언트 힌트를 사용하기 시작합니다. 이는 클라이언트 힌트를 통해 전달되는 데이터 대신 사용자 에이전트 문자열에서 제공되는 정보를 점차적으로 줄이려는 Google의 계획에 따른 것입니다. 클라이언트 힌트에 대한 자세한 내용은 [여기](https://web.dev/user-agent-client-hints/)에서 확인하십시오.<p> AppMeasurement 및 Web SDK 수집 라이브러리는 모두 클라이언트 힌트 수집 및 높은 엔트로피 클라이언트 힌트 수집 여부 구성을 10월까지 지원합니다. 이 변경 사항의 일부로 Adobe는 사용자 에이전트와 관련된 모든 디바이스 조회에 Device Atlas를 사용하게 됩니다. 현재 Device Atlas는 모바일 조회에만 사용됩니다. 이러한 업데이트로 인해 사용자 에이전트(특히 브라우저, 브라우저 유형, 운영 체제, 운영 체제 유형 및 모바일 디바이스)에서 파생된 디바이스 정보가 약간 변경될 수 있습니다. |
| **새로운 NetAcuity 통신사 데이터베이스로 업데이트** | 2022년 9월 14일 | **2022년 10월 5일부터**&#x200B;에 저장된 캐리어 관련 정보 `carrier` Adobe Analytics Data Warehouse 및 Analytics 데이터 피드의 필드가 변경됩니다. 지금까지 해당 열의 데이터 형식은 `<domain>:<ISP>`이었습니다. Adobe은 이러한 테이블을 매핑하기 위해 내부 조회 테이블을 유지 관리했습니다 `<domain>:<ISP>` Adobe Analytics 보고 도구(Analysis Workspace, Reports &amp; Analytics, 보고 API, Data Warehouse, LiveStream 등)에서 보고를 위해 통신사 이름에 값을 포함하는 경우도 있습니다. 조회 파일(`carrier.tsv`)에는 데이터 피드가 제공되어 동일한 매핑을 사용할 수 있습니다.<p>이 업데이트는 NetAcuity의 보다 정확한 통신사 데이터베이스를 사용하여 통신사 매핑을 향상시킵니다. 데이터 피드의 통신사 열에 있는 데이터 형식은 향후 변경될 예정입니다. `<domain>:<ISP>` 대신 통신사 이름이 포함됩니다. Adobe는 계속해서 조회 테이블을 사용하여 가능한 한 과거 보고서와의 연속성을 유지할 것입니다. Adobe에서 조회를 적용하는 보고 도구 (Analysis Workspace, Reports &amp; Analytics, 보고 API, Data Warehouse, 라이브스트림 등) 보다 정확한 매핑의 이점을 얻을 수 있습니다. 일부 매핑(특히 국제 도메인 및 ISP의 경우)은 Adobe이 새 데이터베이스를 채택할 때 다른 것보다 더 많이 변경됩니다. 데이터 피드 통신사 조회 파일(`carrier.tsv`)은 이전 매핑을 유지하고 새 매핑을 추가합니다.<p>Analytics 소스 커넥터는 현재 캐리어 필드를 매핑하지 않으므로 현재 Experience Platform, CJA 등에서 캐리어 보고를 사용할 수 없습니다. 따라서 새 통신사 데이터베이스의 사용은 Analytics 소스 커넥터에서 제공한 데이터를 기반으로 하는 Experience Platform의 어떤 것도 영향을 주지 않습니다. |
| **개선된 IP-to-geolocation 매핑** | 2022년 9월 14일 | 당사의 IP 조회 공급업체인 Digital Element는 IP-to-geolocation 매핑을 위해 새롭게 개선된 데이터 세트(NetAcuity Pulse)로 업그레이드하고 있습니다. Adobe Analytics에서 이 새 데이터 세트를 채택합니다 **2022년 10월 5일**. 새 데이터베이스는 이전 버전보다 더 정확합니다. 새 데이터베이스가 채택되면 일부 IP-to-geo 매핑이 변경 및 개선됩니다.<p>모든 Adobe Analytics 도구 (Analysis Workspace, Reports &amp; Analytics, 보고 API, Data Warehouse, 라이브스트림 등) 새롭게 개선된 매핑을 자동으로 활용합니다. 데이터 피드의 데이터 형식은 변경되지 않습니다. Analytics Source Connector를 통해 제공되는 CJA 데이터도 자동으로 새 매핑을 활용합니다. |
| **Reports &amp; Analytics에서 예약된 보고서 일시 중지** | 2022년 6월 8일 | 2022년 4월 21일, Adobe은 이전에 Reports &amp; Analytics에 대해 발표된 사용 수명 종료를 준비하기 위해 예약된 보고서에 특정 기능 몇 가지를 더 이상 사용하지 않는다고 발표했습니다. 이들 기능에는 새 보고서와 새 데이터 추출을 예약하는 기능이 포함되었습니다.<p>확장을 찾고 Reports &amp; Analytics에서 쉽게 전환하기 위한 고객 요청에 대한 응답으로, Adobe은 다음까지 이러한 기능에 대한 액세스를 연장하기로 결정했습니다 **2023년 1월 31일**. 보고서와 데이터 추출의 만료 기간은 계속 9개월로 제한됩니다. 보고서 및 데이터 추출 전달은 일정이 다시 활성화되지 않는 한 이 기간이 끝나면 일시 중지됩니다.<p>반복해서 말씀드리지만, 이들 기능은 2023년 1월 31일에 사용이 중단됩니다. 해당 날짜 이전에 예약된 보고를 Adobe Analytics에서 사용할 수 있는 다른 메커니즘 중 하나로 마이그레이션해야 합니다. 추가 질문이 있거나 지원이 필요한 경우 Adobe 고객 지원 센터에 문의하십시오. [자세히 알아보기](/help/analyze/reports-analytics/scheduled-reports-eol.md) |
| **Report Builder에서 예약된 작업 일시 중지** | 2022년 6월 8일 | 2022년 4월 21일에 Adobe은 성능 및 게재 최적화 노력의 일환으로 Report Builder의 예약된 작업에 대한 변경 사항을 롤아웃했습니다. 이러한 변경 사항에는 예약된 배달이 “x회 발생 후 종료”되도록 하는 기능의 제거가 포함되었습니다. 대안을 탐색하고 구현할 시간을 더 찾고자 하는 여러 고객 요청에 대한 응답으로, Adobe은 이 옵션을 **2023년 1월 31일**.<p>계속해서 시간별 Report Builder 작업을 예약하고 최대 99회 발생 후 종료되도록 할 수 있습니다. 롤백은 시간별 작업에만 적용됩니다. “x회 발생 후 종료”는 다른 모든 제공 간격(일별, 주별, 월별 및 연간)에 대해 계속 사용할 수 없습니다. 이 옵션은 2023년 1월 31일에 사용이 중단됩니다. 추가 질문이 있거나 지원이 필요한 경우 Adobe 고객 지원 센터에 문의하십시오. [자세히 알아보기](/help/analyze/report-builder/r-arb-scheduled-reports.md) |
| **[!DNL Reports & Analytics]**&#x200B;에 대한 EOL | 2022년 1월 4일 | **2023년 12월 31일**&#x200B;부로 Adobe는 [!DNL Reports & Analytics] 및 관련 보고서와 기능에 대한 서비스를 중단할 예정입니다. [!DNL Reports & Analytics]가 제공하는 보고서, 시각화 및 기반 기술은 더 이상 Adobe의 기술 표준을 충족하지 않습니다. 대부분의 [!DNL Reports & Analytics] 기능은 [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=ko-KR)에서 사용할 수 있습니다. 2015년 Analysis Workspace가 출시된 이후 [!DNL Reports & Analytics] 기능이 Analysis Workspace로 이전되면서 워크플로 패리티의 한계점에 도달했습니다. [이 공지 사항](https://spark.adobe.com/page/6WnF8JK6IRDhf/)은 서비스 종료 프로세스에 대해 설명합니다. |

{style=&quot;table-layout:auto&quot;}

## AppMeasurement

AppMeasurement 릴리스(버전 2.22.4)에 대한 최신 업데이트는 [JavaScript용 AppMeasurement 릴리스 정보](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=ko-KR)를 참조하십시오.
