---
title: 최신 Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 14881de9527796430f13199a6fc5d06452a94a60
workflow-type: tm+mt
source-wordcount: '1141'
ht-degree: 88%

---

# 최신 Adobe Analytics 릴리스 정보 (2022년 3월)

**마지막 업데이트: 2022년 4월 6일**

* 2022년 2월 릴리스 정보는 [여기](/help/release-notes/2022.md)를 참조하십시오.
* Customer Journey Analytics 릴리스 노트의 경우 [여기](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=ko-KR)
* Media Analytics 릴리스 노트의 경우 [여기](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=en)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트에 대해 알아봅니다. Experience League에서 최신 자가 진단 설명서 튜토리얼 및 과정을 살펴보십시오.

## Adobe Analytics의 새로운 기능 {#aa-features}

**마지막 업데이트: 2022년 4월 6일**

| 기능 | 설명 | [목표 날짜](releases.md) |
| ----------- | ---------- | ------- |
| 작업 영역의 주석 | 작업 영역의 주석을 사용하면 상황별 데이터 뉘앙스와 통찰력을 조직에 효과적으로 전달할 수 있습니다. [자세히 알아보기](/help/analyze/analysis-workspace/components/annotations/overview.md) | 2022년 3월 23일부터 점진적 롤아웃이 시작됩니다. 일반 가용성: 2022년 4월 11일 |
| Adobe Analytics 랜딩 페이지 업데이트 | 작업 영역과 Reports &amp; Analytics의 공동 랜딩 페이지 업데이트로 유용성이 향상되고 탐색이 간편해졌습니다. [자세히 알아보기](/help/analyze/landing.md) | 2022년 4월 1일 |
| [!UICONTROL 다음 항목] 또는 [!UICONTROL 이전 항목] 작업 영역 패널 | [!UICONTROL 다음 또는 이전 항목] 패널을 통해 선택한 차원 항목의 다음 또는 이전 항목을 탐색할 수 있습니다. 예를 들어 특정 제품 페이지, 마케팅 채널 또는 디바이스 유형에 대해 다음 또는 이전 페이지를 살펴보려면 이 패널을 사용하십시오. 이 패널은 기존의 다음/이전 보고 수준을 넘어 모든 차원을 볼 수 있도록 해 주며 통찰력을 얻기 위한 새로운 구현이 필요하지 않습니다. | 2022년 4월 20일 |
| [!UICONTROL 페이지 요약] 작업 영역 패널 | [!UICONTROL 페이지 요약] 패널은 선택한 페이지에 대한 심도 있는 분석을 제공합니다. 이 패널은 기존 Reports &amp; Analytics [!UICONTROL 페이지 요약] 보고서에서 확인할 수 있었던 모든 세부 정보와 더불어 훨씬 더 많은 정보를 제공합니다. | 2022년 4월 20일 |

{style=&quot;table-layout:auto&quot;}

## Adobe Analytics의 수정 사항

* Activity Map에 액세스하려고 할 때 오류가 발생하는 문제가 해결되었습니다. (AN-267177)
* 사용자 에셋 전송에 실패하는 문제가 해결되었습니다. (AN-279813)
* [A4T 작업 영역] 패널 관련 문제가 해결되었습니다. (AN-281594; AN-282418)
* 일부 사용자가 Adobe Analytics에 액세스할 수 없는 문제가 해결되었습니다. (AN-282776)
* 새로 생성된 일부 보고서 세트가 데이터를 수집하지 못하는 문제가 해결되었습니다. (AN-283114, AN-283311)
* 데이터 피드 이메일이 제대로 전송되지 않는 문제가 해결되었습니다. (AN-280255; AN-282051)

### Adobe Analytics의 추가 수정 사항

AN-256929; AN-270937; AN-272158; AN-275130; AN-277830; AN-278635; AN-279066; AN-279683; AN-279899; AN-280504; AN-280617; AN-280663; AN-281423; AN-281523; AN-281608; AN-281671; AN-281963; AN-282027; AN-282218; AN-282593; AN-282605; AN-282632; AN-282654; AN-282694; AN-282744; AN-282756; AN-282804; AN-282838; AN-282862; AN-282903; AN-282937; AN-282892; AN-283315; AN-283338; AN-283388; AN-283417; AN-283474; AN-283511; AN-283691, AN-283895; AN-283943; AN-283957; AN-284030; AN-284100; AN-284142; AN-284162

## Adobe Analytics 관리자에 대한 중요 공지

**마지막 업데이트: 2022년 3월 31일**

| 공지 | 추가 또는 업데이트 날짜 | 설명 |
| ----------- | ---------- | ---------- |
| Analytics에서 Experience Edge를 통해 수집된 A4T 데이터를 처리하는 방법 변경 | 2022년 3월 31일 | 설정 **2022년 3월 7일**, A4T(Analytics for Target) 보고를 위한 Target 컨텐츠가 포함된 Experience Edge에서 오는 일부 호출을 처리하는 방식이 변경되었습니다. 3월 7일부터 A4T 보고 컨텐츠가 있는 모든 히트가 수정되었으므로 페이지 보기 또는 링크 이벤트로 처리되지 않습니다. **2022년 3월 31일부터**, 표준 페이지 보기 및 클릭 이벤트가 수정되지 않도록 논리가 더 선택되도록 변경했습니다. 앞으로는 A4T 콘텐츠만 있는 개인화 전용 호출만 수정됩니다. |
| 특정 고객에 대해 지원되는 브라우저 암호화 방법에 대한 업데이트 | 2022년 3월 28일 | Adobe는 자사 데이터 수집에서의 보안에 대한 다양한 고객 요구 사항에 부합하는 두 가지의 암호 보안 수준을 제공합니다. **2022년 6월 23일**&#x200B;부터 보안 수준이 “높음”으로 설정되어 있는 고객에 대해 특정 HTTPS 암호화 알고리즘(암호라고도 함)에 대한 지원이 중단될 예정입니다. 즉, 일부 이전 운영 체제는 최신 암호화 방법을 지원하지 않으므로 더 이상 Analytics로 데이터를 전송하지 않게 됩니다. 기본 “표준” 암호 보안 설정을 사용 중인 고객은 영향을 받지 않습니다. 현재 “높음” 설정을 사용 중인 모든 고객에게는 이미 해당 공지가 직접 전송되었습니다. 이 변경의 영향을 받는 암호 목록은 [여기](/help/technotes/rdc/encryption-algos.md)를 참조하십시오. |
| 이전 예약된 보고서 일시 중지 | 2022년 3월 11일 | **2022년 4월 15일**&#x200B;부터 Adobe는 2년 이상 전에 생성된 모든 예약된 예정된 보고서(2020년 1월 31일 전에 생성된 작업)를 일시 중지합니다. 보고서나 데이터는 삭제되지 않습니다. 중지 대상은 생성일이 2년 이상 지난 보고서로 식별되는 보고서만 해당하며, 예약된 보고서는 추가적으로 전송되지 않습니다. [자세히 알아보기](/help/analyze/reports-analytics/scheduled-reports-eol.md) |
| 2022 ISO 지역 업데이트 | 2021년 3월 11일 | Adobe는 **2022년 6월 10일**&#x200B;에 2022 ISO 지역 업데이트를 수행합니다. 이 릴리스 이후에 부분적인 지역 정보 업데이트가 있을 것으로 예상됩니다. |
| 이전 예약된 Report Builder 작업 일시 중지 | 2022년 2월 24일 | **2022년 4월 15일**&#x200B;부터 Adobe는 2년 이상 전에 생성된 모든 예약된 Report Builder 작업을 일시 중지합니다. 특히 2020년 1월 31일 전에 생성된 모든 작업이 일시 중지 대상에 해당합니다. 작업, 통합 문서나 데이터는 삭제되지 않습니다. 하지만 생성일이 2년 이상 지난 작업으로 식별되는 작업은 중지되며, 예약된 작업은 추가적으로 전송되지 않습니다. [자세히 알아보기](/help/analyze/report-builder/r-arb-scheduled-reports.md) |
| 기존 Analytics OAuth/JWT 통합에 대한 허용 목록 EOL 확장 기능 만료 | 2022년 1월 14일 | **2022년 5월 25일**&#x200B;에 [Analytics 1.3 API, 1.4 SOAP API 및 레거시 Analytics OAuth/JWT EOL](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/APIEOL.md) 허용 목록 확장 기능이 만료될 예정입니다. 이는 레거시 [!DNL Adobe Analytics] OAuth/JWT 자격 증명 추가 시간을 사용하여 클라이언트 통합을 [Adobe IMS 자격 증명](https://developer.adobe.com/console)으로 마이그레이션할 수 있도록 고객에게 제공되었던 기능입니다. 해당 만료는 필요한 IMS 마이그레이션을 완료하지 않은 [!DNL Adobe Analytics Livestream] 및 [!DNL Adobe Campaign] 고객에 영향을 주지만 이에 국한되지는 않습니다. 현재 허용 목록 확장 기능을 통해 기존 [!DNL Analytics] OAuth/JWT 자격 증명을 사용 중인 고객 및 2022년 5월 25일까지 IMS 자격 증명으로 마이그레이션을 완료하지 않은 고객은 Adobe 서비스에 액세스할 수 없게 됩니다. 라이브스트림 고객은 클라이언트 애플리케이션을 IMS 자격 증명으로 마이그레이션하는 방법에 대한 이 [지침](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/getting_started.md)을 참조할 수 있습니다. [!DNL Campaign] 고객은 Adobe 계정 팀에 최신 버전의 [!DNL Campaign]으로의 업그레이드에 대해 문의할 수 있습니다. |
| Secure File Transfer Protocol(SFTP) 서비스 업그레이드 | 2022년 3월 3일 | **2022년 5월 15일**, [!DNL Adobe Analytics]는 파일 전송 보안을 개선하기 위해 Secure File Transfer Protocol(SFTP) 서비스를 업그레이드할 예정입니다. 이 변경 사항으로 일부 SFTP 클라이언트 구성은 더 이상 지원되지 않습니다. 또한 **2022년 3월 1일**&#x200B;까지 사용할 수 있는 몇 가지 연결 옵션을 추가할 예정입니다. 이는 SFTP를 사용하여 Adobe Analytics로 전송되거나 Adobe Analytics에서 검색된 데이터에만 영향을 미칩니다. FTP 프로토콜은 영향을 받지 않습니다. 서비스 중단을 방지하려면 SFTP 클라이언트(코드, 도구, 서비스)가 [여기](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html?lang=ko-KR)에 설명된 변경 사항을 준수하는지 확인하십시오. |
| [!DNL Reports & Analytics]에 대한 EOL | 2022년 1월 4일 | **2023년 12월 31일**&#x200B;부로 Adobe는 [!DNL Reports & Analytics] 및 관련 보고서와 기능에 대한 서비스를 중단할 예정입니다. [!DNL Reports & Analytics]가 제공하는 보고서, 시각화 및 기반 기술은 더 이상 Adobe의 기술 표준을 충족하지 않습니다. 대부분의 [!DNL Reports & Analytics] 기능은 [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=ko-KR)에서 사용할 수 있습니다. 2015년 Analysis Workspace가 출시된 이후 [!DNL Reports & Analytics] 기능이 Analysis Workspace로 이전되면서 워크플로 패리티의 한계점에 도달했습니다. [이 공지 사항](https://spark.adobe.com/page/6WnF8JK6IRDhf/)은 서비스 종료 프로세스에 대해 설명합니다. |

{style=&quot;table-layout:auto&quot;}

## AppMeasurement {#appm}

AppMeasurement 릴리스(버전 2.22.4)에 대한 최신 업데이트는 [JavaScript용 AppMeasurement 릴리스 정보](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=ko-KR)를 참조하십시오.

>[!MORELIKETHIS]
>[[!DNL Customer Journey Analytics] 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=en)
