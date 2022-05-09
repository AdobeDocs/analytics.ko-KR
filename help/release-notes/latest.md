---
title: 최신 Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 43869c683ca30c94157c6822b53f02a917f6e3ff
workflow-type: tm+mt
source-wordcount: '1170'
ht-degree: 95%

---

# 최신 Adobe Analytics 릴리스 정보 (2022년 4월)

**마지막 업데이트**: 2022년 5월 9일

## 관련 리소스

* [2022년 이전 릴리스 정보](/help/release-notes/2022.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [Media Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트

## Adobe Analytics의 새로운 기능

| 기능 | 설명 | [목표 날짜](releases.md) |
| ----------- | ---------- | ------- |
| Adobe Analytics 랜딩 페이지 업데이트 | 작업 영역과 Reports &amp; Analytics의 공동 랜딩 페이지 업데이트로 유용성이 향상되고 탐색이 간편해졌습니다. [자세히 알아보기](/help/analyze/landing.md) | 2022년 4월 20일 |
| [!UICONTROL 다음 항목] 또는 [!UICONTROL 이전 항목] 작업 영역 패널 | [!UICONTROL 다음 또는 이전 항목] 패널을 통해 선택한 차원 항목의 다음 또는 이전 항목을 탐색할 수 있습니다. 예를 들어 특정 제품 페이지, 마케팅 채널 또는 디바이스 유형에 대해 다음 또는 이전 페이지를 살펴보려면 이 패널을 사용하십시오. 이 패널은 기존의 다음/이전 보고 수준을 넘어 모든 차원을 볼 수 있도록 해 주며 통찰력을 얻기 위한 새로운 구현이 필요하지 않습니다. [자세히 알아보기](/help/analyze/analysis-workspace/c-panels/next-previous.md) | 2022년 4월 20일 |
| [!UICONTROL 페이지 요약] 작업 영역 패널 | [!UICONTROL 페이지 요약] 패널은 선택한 페이지에 대한 심도 있는 분석을 제공합니다. 이 패널은 기존 Reports &amp; Analytics [!UICONTROL 페이지 요약] 보고서에서 확인할 수 있었던 모든 세부 정보와 더불어 훨씬 더 많은 정보를 제공합니다. [자세히 알아보기](/help/analyze/analysis-workspace/c-panels/page-summary.md) | 2022년 4월 20일 |
| 2.0 API 호출에 대한 `x-proxy-global-company-id` 헤더 요구 사항 제거 | 이 정보는 끝점 URL의 일부이므로 Adobe Analytics 2.0 API에는 더 이상 `x-proxy-global-company-id` 헤더가 필요하지 않습니다. 이 헤더를 계속 포함할 수 있지만 누락된 경우 더 이상 오류가 발생하지 않습니다. | 2022년 4월 20일 |

{style=&quot;table-layout:auto&quot;}

## Adobe Analytics의 수정 사항

* 데이터 피드 UI에서 생성할 때 데이터 피드를 저장한 후 시작 및 종료 날짜가 자동으로 변경되는 데이터 피드 문제를 수정했습니다. 날짜가 저절로 1일씩 업데이트되었습니다. (AN-281262)
* 이메일 링크를 통해 예약된 프로젝트를 업데이트할 수 없는 문제가 해결되었습니다. (AN-283622)
* Adobe 브라우저 유형 조회 테이블에서 Apple Safari 및 Microsoft Edge의 최신 릴리스가 제대로 식별되지 않는 문제를 해결했습니다. [브라우저 버전이 업데이트](/help/components/dimensions/browser.md)되는 경우와 마찬가지로 브라우저 유형 조회 테이블에 대한 업데이트는 향후 데이터만 수정합니다. 브라우저 버전의 조회 테이블은 4월 20일에 업데이트되었으며 브라우저 유형의 조회 테이블은 4월 28일에 업데이트되었습니다. (AN-284872; AN-285753; AN-286257)

### Adobe Analytics의 추가 수정 사항

AN-274486; AN-279258; AN-279995; AN-280918; AN-281423; AN-282084; AN-282435; AN-283508; AN-283517; AN-283706; AN-283762; AN-283921; AN-284195; AN-284663; AN-284573; AN-284721; AN-284790; AN-284867; AN-284870; AN-284872; AN-284884; AN-284914; AN-284930; AN-284933; AN-284967; AN-284970; AN-285187; AN-285328; AN-285337; AN-285375; AN-285447; AN-285724; AN-285753; AN-285761

## Adobe Analytics 관리자에 대한 중요 공지

| 공지 | 추가 또는 업데이트 날짜 | 설명 |
| ----------- | ---------- | ---------- |
| **SFTP 업그레이드** | 2022년 5월 9일 | 이전에 Adobe는 Adobe이 파일 전송을 위한 향상된 보안을 제공하기 위해 2022년 5월에 SFTP(Secure File Transfer Protocol) 서비스를 업그레이드할 것을 알렸습니다. 2022년 여름으로의 업그레이드를 연기했습니다. 이 변경 사항이 발생하면 특정 SFTP 클라이언트 구성이 더 이상 지원되지 않습니다. 이는 SFTP를 사용하여 Adobe Analytics로 전송되거나 Adobe Analytics에서 검색된 데이터에만 영향을 미칩니다. FTP 프로토콜은 영향을 받지 않습니다. 서비스 중단을 방지하려면 SFTP 클라이언트(코드, 도구, 서비스)가 [여기](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html?lang=kr)에 설명된 변경 사항을 준수하는지 확인하십시오. |
| **크로스 디바이스 분석(CDA) 권한** | 2022년 4월 13일 | **2022년 5월 1일**&#x200B;부터 [CDA](/help/components/cda/overview.md)의 새로운 구현은 고객당 최대 3개의 RSID(보고서 세트 ID)로 제한됩니다. |
| **Adobe Analytics가 Experience Edge를 통해 수집된 A4T 데이터를 처리하는 방법 변경** | 2022년 3월 31일 | 2022년 3월 7일부터 Analytics는 A4T(Analytics for Target) 보고용 Target 콘텐츠가 포함된 Experience Edge에서 오는 일부 호출을 처리하는 방법을 변경했습니다. 3월 7일부터 A4T 보고 콘텐츠가 포함된 모든 히트가 페이지 보기 또는 링크 이벤트로 처리되지 않도록 수정됩니다. **2022년 3월 31일**&#x200B;부터 로직이 보다 선택적으로 변경되어 표준 페이지 보기 및 클릭 이벤트가 수정되지 않았습니다. 향후 수정되는 유일한 이벤트는 A4T 콘텐츠만 있는 개인화 전용 호출입니다. |
| **특정 고객에 대해 지원되는 브라우저 암호화 방법에 대한 업데이트** | 2022년 3월 28일 | Adobe는 자사 데이터 수집에서의 보안에 대한 다양한 고객 요구 사항에 부합하는 두 가지의 암호 보안 수준을 제공합니다. **2022년 6월 23일**&#x200B;부터 보안 수준이 “높음”으로 설정되어 있는 고객에 대해 특정 HTTPS 암호화 알고리즘(암호라고도 함)에 대한 지원이 중단될 예정입니다. 이 작업은 일부 이전 운영 체제는 최신 암호화 방법을 지원하지 않으므로 더 이상 Analytics로 데이터를 전송하지 않게 됩니다. 기본 “표준” 암호 보안 설정을 사용 중인 고객은 영향을 받지 않습니다. 현재 “높음” 설정을 사용 중인 모든 고객에게는 이미 해당 공지가 직접 전송되었습니다. 이 변경의 영향을 받는 암호 목록은 여기에서 찾아볼 수 있습니다. |
| **이전 예약된 보고서 일시 중지** | 2022년 4월 12일 | **2022년 4월 20일**&#x200B;부터 Adobe는 2년 이상 전에 생성된 모든 예약된 예정된 보고서(2020년 1월 31일 전에 생성된 작업)를 일시 중지할 예정입니다. 보고서나 데이터는 삭제되지 않습니다. 중지 대상은 생성일이 2년 이상 지난 보고서로 식별되는 보고서만 해당하며, 예약된 보고서는 추가적으로 전송되지 않습니다. 자세히 알아보기 |
| **2022 ISO 지역 업데이트** | 2021년 3월 11일 | Adobe는 **2022년 6월 10일**&#x200B;에 2022 ISO 지역 업데이트를 수행할 계획입니다. 이 릴리스 이후에 부분적인 지역 정보 업데이트가 있을 것으로 예상됩니다. |
| **이전 예약된 Report Builder 작업 일시 중지** | 2022년 4월 12일 | **2022년 4월 20일**&#x200B;부터 Adobe는 2년 이상 전에 생성된 모든 예약된 Report Builder 작업을 일시 중지할 예정입니다. 특히 2020년 1월 31일 전에 생성된 모든 작업이 일시 중지 대상에 해당합니다. 작업, 통합 문서나 데이터는 삭제되지 않습니다. 하지만 생성일이 2년 이상 지난 작업으로 식별되는 작업은 중지되며, 예약된 작업은 추가적으로 전송되지 않습니다. 자세히 알아보기 |
| **기존 Analytics OAuth/JWT 통합에 대한 허용 목록 EOL 확장 기능 만료** | 2022년 1월 14일 | **2022년 5월 25일**&#x200B;에 [Analytics 1.3 API, 1.4 SOAP API 및 레거시 Analytics OAuth/JWT EOL](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/APIEOL.md) 허용 목록 확장 기능이 만료됩니다. 이는 레거시 [!DNL Adobe Analytics] OAuth/JWT 자격 증명 추가 시간을 사용하여 클라이언트 통합을 [Adobe IMS 자격 증명](https://developer.adobe.com/console)으로 마이그레이션할 수 있도록 고객에게 제공되었던 기능입니다. 해당 만료는 필요한 IMS 마이그레이션을 완료하지 않은 [!DNL Adobe Analytics Livestream] 및 [!DNL Adobe Campaign] 고객에 영향을 주지만 이에 국한되지는 않습니다. 현재 허용 목록 확장 기능을 통해 기존 [!DNL Analytics] OAuth/JWT 자격 증명을 사용 중인 고객 및 2022년 5월 25일까지 IMS 자격 증명으로 마이그레이션을 완료하지 않은 고객은 Adobe 서비스에 액세스할 수 없습니다. 라이브스트림 고객은 클라이언트 애플리케이션을 IMS 자격 증명으로 마이그레이션하는 방법에 대한 이 [지침](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/getting_started.md)을 참조할 수 있습니다. [!DNL Campaign] 고객은 Adobe 계정 팀에 최신 버전의 [!DNL Campaign]으로의 업그레이드에 대해 문의할 수 있습니다. |
| **[!DNL Reports & Analytics]**&#x200B;에 대한 EOL | 2022년 1월 4일 | **2023년 12월 31일**&#x200B;부로 Adobe는 [!DNL Reports & Analytics] 및 관련 보고서와 기능에 대한 서비스를 중단할 예정입니다. [!DNL Reports & Analytics]가 제공하는 보고서, 시각화 및 기반 기술은 더 이상 Adobe의 기술 표준을 충족하지 않습니다. 대부분의 [!DNL Reports & Analytics] 기능은 [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=ko)에서 사용할 수 있습니다. 2015년 Analysis Workspace가 출시된 이후 [!DNL Reports & Analytics] 기능이 Analysis Workspace로 이전되면서 워크플로 패리티의 한계점에 도달했습니다. [이 공지 사항](https://spark.adobe.com/page/6WnF8JK6IRDhf/)은 서비스 종료 프로세스에 대해 설명합니다. |

{style=&quot;table-layout:auto&quot;}

## AppMeasurement {#appm}

AppMeasurement 릴리스(버전 2.22.4)에 대한 최신 업데이트는 [JavaScript용 AppMeasurement 릴리스 정보](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=ko)를 참조하십시오.

>[!MORELIKETHIS]
>[[!DNL Customer Journey Analytics] 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=ko)
