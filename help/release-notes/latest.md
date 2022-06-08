---
title: 최신 Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 8666c32ffe907ad486778fa382404807459be03c
workflow-type: tm+mt
source-wordcount: '826'
ht-degree: 62%

---

# 현재 Adobe Analytics 릴리스 정보 (2022년 5월)

**마지막 업데이트**: 2022년 6월 8일

## 관련 리소스

* [2022년 이전 릴리스 정보](/help/release-notes/2022.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=ko-KR)
* [Media Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=ko-KR)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트

## Adobe Analytics의 새로운 기능

| 기능 | 설명 | [목표 날짜](releases.md) |
| ----------- | ---------- | ------- |
| Experience Edge를 통해 라이프사이클 차원 및 지표 채우기 | Experience Edge를 통해 전송되는 모바일 라이프사이클 데이터가 이제 Analytics 보고에 표시됩니다. Experience Edge를 통해 수집되는 라이프사이클 데이터와 기존 라이프사이클 보고에 대한 자세한 내용은 설명서를 참조하십시오. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) | 2022년 5월 27일 |

{style=&quot;table-layout:auto&quot;}

### Adobe Analytics의 수정 사항

(여러 고객에 대한 수정 사항)

해당 사항 없음

### Adobe Analytics의 추가 수정 사항

(개인 사용자 고객에 대한 수정 사항)

AN-274429; AN-279640; AN-280918; AN-280945; AN-282884; AN-283565; AN-284785; AN-284814; AN-284854; AN-284989; AN-285244; AN-285253; AN-285432; AN-285528; AN-285535; AN-285710; AN-286255; AN-286340; AN-286434; AN-286454; AN-286630; AN-286716; AN-286854; AN-286911

### Adobe Analytics 관리자에 대한 중요 공지

| 공지 | 추가 또는 업데이트 날짜 | 설명 |
| ----------- | ---------- | ---------- |
| Reports &amp; Analytics에서 예약된 보고서 일시 중지 | 2022년 6월 8일 | 2022년 4월 21일, 이전에 발표된 보고서를 준비하기 위해 예약된 보고서에 특정 기능의 사용 중단을 발표했습니다 [Reports &amp; Analytics 수명 종료](https://express.adobe.com/page/6WnF8JK6IRDhf/). 이러한 기능에는 새 보고서 및 새 데이터 추출을 예약하는 기능이 포함되었습니다.<p>확장을 찾고 Reports and Analytics에서 간편하게 전환하기 위해 고객 요청에 대한 응답으로 다음 시점까지 이러한 기능에 대한 액세스를 연장하기로 결정했습니다 **2023년 1월 31일**. 보고서 및 데이터 추출 모두에 대한 만료 기간은 9개월로 제한됩니다. 일정을 다시 활성화하지 않으면 이 기간이 끝날 때 보고서 및 데이터 추출 게재가 일시 중지됩니다. <p>다시 말하면 이러한 기능은 2023년 1월 31일에 더 이상 사용되지 않으며, 그 전에 Adobe Analytics에서 사용할 수 있는 다른 메커니즘 중 하나로 예약된 보고를 마이그레이션해야 합니다. 추가 질문이 있거나 지원이 필요한 경우 Adobe 고객 지원 센터에 문의하십시오. |
| Report Builder에서 예약된 작업 일시 중지 | 2022년 6월 8일 | 2022년 4월 21일에 성능 및 게재 최적화 노력의 일환으로 Report Builder의 예약된 작업에 대한 변경 사항을 발표했습니다. 이러한 변경 사항에는 예약된 게재를 &quot;x 회 후 종료&quot;하는 기능을 제거하는 기능이 포함되었습니다. 대안을 탐색하고 구현하는 데 더 많은 시간을 원하는 여러 고객 요청에 대해 Adobe는 이 옵션을 **2023년 1월 31일**.<p>시간별 Report Builder 작업을 계속 예약하고 최대 99회 발생 후 완료할 수 있습니다. 롤백은 시간별 작업에만 적용됩니다. 다른 모든 배달 간격(일별, 주별, 월별 및 연간)에는 &quot;x 발생 후 종료&quot;를 사용할 수 없습니다. 이 옵션은 2023년 1월 31일부터 사용되지 않습니다. 추가 질문 또는 지원이 필요한 경우 Adobe 고객 지원 센터에 문의하십시오. |
| **SFTP 업그레이드** | 2022년 5월 9일 | 이전에 Adobe는 파일 전송에 대한 보안을 개선하기 위해 2022년 5월에 SFTP(Secure File Transfer Protocol) 서비스를 업그레이드할 예정임을 공지했습니다. 이 업그레이드를으로 연기했습니다. **2022년 여름**. 이 변경 사항이 적용되면 일부 SFTP 클라이언트 구성은 더 이상 지원되지 않습니다. 이는 SFTP를 사용하여 Adobe Analytics로 전송되거나 Adobe Analytics에서 검색된 데이터에만 영향을 미칩니다. FTP 프로토콜은 영향을 받지 않습니다. 서비스 중단을 방지하려면 SFTP 클라이언트(코드, 도구, 서비스)가 [여기](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html?lang=ko-KR)에 설명된 변경 사항을 준수하는지 확인하십시오. |
| **특정 고객에 대해 지원되는 브라우저 암호화 방법에 대한 업데이트** | 2022년 3월 28일 | Adobe는 자사 데이터 수집에서의 보안에 대한 다양한 고객 요구 사항에 부합하는 두 가지의 암호 보안 수준을 제공합니다. **2022년 6월 23일**&#x200B;부터 보안 수준이 “높음”으로 설정되어 있는 고객에 대해 특정 HTTPS 암호화 알고리즘(암호라고도 함)에 대한 지원이 중단될 예정입니다. 이 작업은 일부 이전 운영 체제는 최신 암호화 방법을 지원하지 않으므로 더 이상 Analytics로 데이터를 전송하지 않게 됩니다. 기본 “표준” 암호 보안 설정을 사용 중인 고객은 영향을 받지 않습니다. 현재 “높음” 설정을 사용 중인 모든 고객에게는 이미 해당 공지가 직접 전송되었습니다. 이 변경의 영향을 받는 암호 목록은 여기에서 찾아볼 수 있습니다. |
| **2022 ISO 지역 업데이트** | 2021년 3월 11일 | Adobe는 **2022년 6월 10일**&#x200B;에 2022 ISO 지역 업데이트를 수행할 계획입니다. 이 릴리스 이후에 부분적인 지역 정보 업데이트가 있을 것으로 예상됩니다. |
| **[!DNL Reports & Analytics]**&#x200B;에 대한 EOL | 2022년 1월 4일 | **2023년 12월 31일**&#x200B;부로 Adobe는 [!DNL Reports & Analytics] 및 관련 보고서와 기능에 대한 서비스를 중단할 예정입니다. [!DNL Reports & Analytics]가 제공하는 보고서, 시각화 및 기반 기술은 더 이상 Adobe의 기술 표준을 충족하지 않습니다. 대부분의 [!DNL Reports & Analytics] 기능은 [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=ko-KR)에서 사용할 수 있습니다. 2015년 Analysis Workspace가 출시된 이후 [!DNL Reports & Analytics] 기능이 Analysis Workspace로 이전되면서 워크플로 패리티의 한계점에 도달했습니다. [이 공지 사항](https://spark.adobe.com/page/6WnF8JK6IRDhf/)은 서비스 종료 프로세스에 대해 설명합니다. |

{style=&quot;table-layout:auto&quot;}

### AppMeasurement

AppMeasurement 릴리스(버전 2.22.4)에 대한 최신 업데이트는 [JavaScript용 AppMeasurement 릴리스 정보](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=ko-KR)를 참조하십시오.

