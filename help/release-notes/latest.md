---
title: 최신 Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 945a495dfea2f4564d39457528a185b6b75c7d17
workflow-type: tm+mt
source-wordcount: '839'
ht-degree: 76%

---

# 현재 Adobe Analytics 릴리스 정보 (2022년 2월)

**마지막 업데이트**: 2022년 3월 3일

[Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트에 대해 알아봅니다. Experience League에서 최신 자가 진단 설명서 튜토리얼 및 과정을 살펴보십시오.

## Adobe Analytics의 새로운 기능 {#aa-features}

| 기능 | 설명 | [목표 날짜](releases.md) |
| ----------- | ---------- | ------- |
| 모바일 스코어카드 프로젝트 미리보기 모드 | 스코어카드 빌더에서 직접 모바일 스코어카드가 Analytics 대시보드 앱에 어떻게 표시되는지 미리보기를 시작해 보십시오. 미리보기 모드를 통해 사용자는 앱에서와 동일한 방식으로 필터 및 차트 및 상호 작용할 수 있으므로 스코어카드를 저장하고 공유하기 전에 환경을 미리 확인할 수 있습니다. 사용자는 미리보기 모드에서 디바이스 선택기를 사용하여 다른 디바이스에서 스코어카드가 어떻게 보이는지 확인할 수도 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/analyze/mobapp/create-scorecard.html?lang=en#preview) | 2022년 2월 16일 |
| API 프로젝트 끝점 | API를 사용하여 Analysis Workspace 프로젝트를 추가, 편집 또는 삭제합니다. [자세히 알아보기](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/projects/) | 2022년 2월 1일 |

{style=&quot;table-layout:auto&quot;}

## Adobe Analytics의 수정 사항

* [!UICONTROL 서버 호출 사용]과 관련된 여러 문제가 해결되었습니다. (AN-279134, AN-279878, AN-280802, AN-279097, AN-191284, AN-269720)
* Data Warehouse가 빈 .csv 파일을 내보내는 문제가 해결되었습니다. (AN-280291)
* 최근 세그먼트에 대해 대상 이름이 채워지지 않는 문제가 해결되었습니다. (AN-279715)
* 보고 시간이 지연되는 문제가 수정되었습니다. (AN-280055)
* 모든 치수 항목을 분류하지 않는 분류와 관련된 문제를 해결했습니다. (AN-280031)

### Adobe Analytics의 추가 수정 사항

AN-268093, AN-273820, AN-274435, AN-274904, AN-275356, AN-275947, AN-276160, AN-276258, AN-276705, AN-277051, AN-277957, AN-278693, AN-278882, AN-279000, AN-279046, AN-279362, AN-279460, AN-279488, AN-279554, AN-279572, AN-279663, AN-279755, AN-279825, AN-280002, AN-280013, AN-280019, AN-280033, AN-280086, AN-280232, AN-280264, AN-280288, AN-280342, AN-280347, AN-280360, AN-280370, AN-280724, AN-280830, AN-280941, AN-281353, AN-281424, AN-281533

## [!DNL Analytics] 관리자에 대한 중요 공지

**업데이트 날짜: 2022년 3월 3일**

| 공지 | 추가 또는 업데이트 날짜 | 설명 |
| ----------- | ---------- | ---------- |
| Analytics에서 Experience Edge를 통해 수집된 A4T 데이터를 처리하는 방법 변경 | 2022년 2월 25일 | 설정 **2022년 3월 7일**, Adobe에서는 Experience Edge를 통해 Adobe Analytics으로 전송된 일부 Target 관련 데이터를 처리하는 방법을 변경합니다. Analytics 및 Target에서 Adobe Experience Platform Web SDK를 사용할 때 일부 개인화 이벤트가에서 계산되었습니다. [!DNL Adobe Analytics] 로서의 [!UICONTROL 페이지 보기 수]. 이로 인해 페이지 보기 카운트와 추가 서버 호출이 부풀려졌습니다. 이러한 변경 사항으로 Analytics 콘텐츠가 없는 개인화 호출은 무시됩니다. A4T 데이터를 사용하는 개인화 호출은 A4T 데이터를 기록하지만 과금 가능한 서버 호출로 기록되지 않으며 페이지 보기 수 또는 링크 이벤트 지표에 영향을 주지 않습니다. |
| 이전에 예약된 Report Builder 작업 일시 중지 | 2022년 2월 24일 | **2022년 4월 15일 시행**, Adobe은 2년 이상 전에 만들어진 예약된 모든 Report Builder 작업을 일시 중지하려고 합니다. 특히, 이 일시 중지는 2020년 1월 31일 이전에 만들어진 모든 작업에 적용됩니다. 작업, 통합 문서 또는 데이터는 삭제되지 않습니다. 그러나 2년 이상으로 식별된 작업은 일시 중지되며 추가 예약된 작업은 전송되지 않습니다. [자세히 알아보기](/help/analyze/report-builder/r-arb-scheduled-reports.md) |
| 기존 Analytics OAuth/JWT 통합에 대한 허용 목록 EOL 확장 기능 만료 | 2022년 1월 14일 | **2022년 5월 25일**&#x200B;에 [Analytics 1.3 API, 1.4 SOAP API 및 레거시 Analytics OAuth/JWT EOL](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/APIEOL.md) 허용 목록 확장 기능이 만료될 예정입니다. 이는 레거시 [!DNL Adobe Analytics] OAuth/JWT 자격 증명 추가 시간을 사용하여 클라이언트 통합을 [Adobe IMS 자격 증명](https://developer.adobe.com/console)으로 마이그레이션할 수 있도록 고객에게 제공되었던 기능입니다. 해당 만료는 필요한 IMS 마이그레이션을 완료하지 않은 [!DNL Adobe Analytics Livestream] 및 [!DNL Adobe Campaign] 고객에 영향을 주지만 이에 국한되지는 않습니다. 현재 허용 목록 확장 기능을 통해 기존 [!DNL Analytics] OAuth/JWT 자격 증명을 사용 중인 고객 및 2022년 5월 25일까지 IMS 자격 증명으로 마이그레이션을 완료하지 않은 고객은 Adobe 서비스에 액세스할 수 없게 됩니다. 라이브스트림 고객은 클라이언트 애플리케이션을 IMS 자격 증명으로 마이그레이션하는 방법에 대한 이 [지침](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/getting_started.md)을 참조할 수 있습니다. [!DNL Campaign] 고객은 Adobe 계정 팀에 최신 버전의 [!DNL Campaign]으로의 업그레이드에 대해 문의할 수 있습니다. |
| [!DNL Reports & Analytics]에 대한 EOL | 2022년 1월 4일 | **2023년 12월 31일**&#x200B;부로 Adobe는 [!DNL Reports & Analytics] 및 관련 보고서와 기능에 대한 서비스를 중단할 예정입니다. [!DNL Reports & Analytics]가 제공하는 보고서, 시각화 및 기반 기술은 더 이상 Adobe의 기술 표준을 충족하지 않습니다. 대부분의 [!DNL Reports & Analytics] 기능은 [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html)에서 사용할 수 있습니다. 2015년 Analysis Workspace가 출시된 이후 [!DNL Reports & Analytics] 기능이 Analysis Workspace로 이전되면서 워크플로 패리티의 한계점에 도달했습니다. [이 공지 사항](https://spark.adobe.com/page/6WnF8JK6IRDhf/)은 서비스 종료 프로세스에 대해 설명합니다. |
| Secure File Transfer Protocol(SFTP) 서비스 업그레이드 | 2022년 3월 3일 | **2022년 5월 15일**, [!DNL Adobe Analytics]는 파일 전송 보안을 개선하기 위해 Secure File Transfer Protocol(SFTP) 서비스를 업그레이드할 예정입니다. 이 변경 사항으로 일부 SFTP 클라이언트 구성은 더 이상 지원되지 않습니다. 또한 **2022년 3월 1일**&#x200B;까지 사용할 수 있는 몇 가지 연결 옵션을 추가할 예정입니다. 이는 SFTP를 사용하여 Adobe Analytics로 전송되거나 Adobe Analytics에서 검색된 데이터에만 영향을 미칩니다. FTP 프로토콜은 영향을 받지 않습니다. 서비스 중단을 방지하려면 SFTP 클라이언트(코드, 도구, 서비스)가 [여기](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html)에 설명된 변경 사항을 준수하는지 확인하십시오. |

## AppMeasurement {#appm}

AppMeasurement 릴리스(버전 2.22.4)에 대한 최신 업데이트는 [JavaScript용 AppMeasurement 릴리스 정보](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=en)를 참조하십시오.

>[!MORELIKETHIS]
>[[!DNL Customer Journey Analytics] 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=en)
