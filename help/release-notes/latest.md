---
title: 최신 Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 29f152bf1724c566da69598f35929ee3b502b7f9
workflow-type: tm+mt
source-wordcount: '1077'
ht-degree: 70%

---

# 현재 Adobe Analytics 릴리스 노트(2022년 6월)

>[!NOTE]
>
>이 페이지에는 프리릴리스 정보가 포함되어 있으며 향후 변경될 수 있습니다.

**최종 업데이트**: 2022년 6월 15일

## 관련 리소스

* [2022년 이전 릴리스 정보](/help/release-notes/2022.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=ko-KR)
* [Media Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=ko-KR)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트

## Adobe Analytics의 새로운 기능

| 기능 | 설명 | [목표 날짜](releases.md) |
| ----------- | ---------- | ------- |
| **새 흐름 시각화 UI** | 플로우 시각화에 추가 기능을 제공하여 보다 강력하고 기능을 제공합니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/flow/create-flow.html?lang=en) | 2022년 6월 15일 |
| **모바일 스코어카드에서 주석 공유** | Workspace에서 생성된 주석을 모바일 스코어카드에 표시할 수 있습니다. 이를 통해 Mobile Scorecard 프로젝트에서 바로 조직 및 캠페인에 대한 통찰력과 컨텍스트 데이터 뉘앙스를 공유할 수 있으며 Analytics 대시보드 모바일 앱에서 볼 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/annotations/mobile-annotations.html?lang=en) | 2022년 6월 15일 |
| **Edge Collection에서 머천다이징 변수의 제품 구문 버전 지원** | 이제 관련 XDM 필드를 설정하여 제품 구문과 동등한 기능을 사용하여 머천다이징 변수를 설정할 수 있습니다. 머천다이징 변수의 제품 구문에 대한 자세한 내용을 살펴보십시오 [여기](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/merchandising-evars.html?lang=ko). 제품 구문에 대한 매핑 을 참조하십시오 [여기](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html?lang=en#aep-edge). | 2022년 6월 15일 |
| **Experience Edge를 통해 라이프사이클 차원 및 지표 채우기** | Experience Edge를 통해 전송되는 모바일 라이프사이클 데이터가 이제 Analytics 보고에 표시됩니다. 기존 모바일 라이프사이클 보고에 매핑되는 XDM 필드에 대한 자세한 내용은 설명서를 참조하십시오. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) | 2022년 5월 27일 |
| **Analytics 처리 규칙에서 사용할 수 있는 모바일 서비스 처리 규칙** | Adobe Mobile Services 수명 종료 날짜는 2022년 12월 31일입니다. Adobe Mobile Services에서 만들거나 생성한 기존 처리 규칙은 자동으로 Adobe Analytics 처리 규칙으로 마이그레이션되어 편집하고 관리할 수 있습니다. 관리할 수 있지만, 제품이 종료될 때까지 Mobile Services에서 더 이상 편집할 수 없습니다. 추가 질문이 있거나 지원이 필요한 경우 Adobe 고객 지원 센터에 문의하십시오. [자세히 알아보기](https://experienceleague.adobe.com/docs/mobile-services/using/eol.html?lang=en) | 2022년 6월 15일 |
| **새로운 분류 경험 - 1단계** | 새로운 분류 세트 사용자 경험의 단계적 릴리스는 고객이 소유한 분류 데이터에 대한 가시성을 크게 향상시킵니다. [일반 공급](/help/release-notes/releases.md) 이 지역은 2023년 초와 비슷한 것으로 추정된다. | 제한된 테스트 시작: 2022년 6월 15일 |

{style=&quot;table-layout:auto&quot;}

### Adobe Analytics의 수정 사항

AN-251686; AN-283542; AN-286572; AN-286945; AN-286784; AN-286944; AN-287012; AN-287319; AN-287333; AN-287348; AN-287429; AN-288238; AN-288281; AN-288660; AN-288769; AN-288798; AN-288871; AN-288872; AN-288941; AN-288951; AN-288952; AN-288956; AN-289062; AN-289340; AN-289346; AN-289488; AN-289562; AN-289580; AN-289861; AN-289892;

### Adobe Analytics 관리자에 대한 중요 공지

| 공지 | 추가 또는 업데이트 날짜 | 설명 |
| ----------- | ---------- | ---------- |
| **Reports &amp; Analytics에서 예약된 보고서 일시 중지** | 2022년 6월 8일 | 2022년 4월 21일에 이전에 발표된 Reports &amp; Analytics의 서비스 종료에 대비하여 예약된 보고서와 관련된 몇 가지 기능의 사용 중단을 발표했습니다. 이러한 기능에는 새 보고서와 새 데이터 추출을 예약하는 기능이 포함되었습니다.<p>확장을 원하는 고객의 요청에 따라 Reports and Analytics에서 쉽게 전환할 수 있도록 이러한 기능에 대한 액세스를 **2023년 1월 31일**&#x200B;까지 연장하기로 결정했습니다. 보고서와 데이터 추출의 만료 기간은 계속 9개월로 제한됩니다. 보고서 및 데이터 추출 전달은 일정이 다시 활성화되지 않는 한 이 기간이 끝나면 일시 중지됩니다.<p>다시 말하면 이러한 기능은 2023년 1월 31일에 더 이상 사용되지 않습니다. 이 날짜 전에, 예약된 보고를 Adobe Analytics에서 사용할 수 있는 다른 메커니즘 중 하나로 마이그레이션해야 합니다. 추가 질문이 있거나 지원이 필요한 경우 Adobe 고객 지원 센터에 문의하십시오. [자세히 알아보기](/help/analyze/reports-analytics/scheduled-reports-eol.md) |
| **Report Builder에서 예약된 작업 일시 중지** | 2022년 6월 8일 | 2022년 4월 21일에 최적의 성능과 제공을 위한 노력의 일환으로 Report Builder의 예약된 작업에 대한 변경 사항이 배포되었습니다. 이러한 변경 사항에는 예약된 배달이 “x회 발생 후 종료”되도록 하는 기능의 제거가 포함되었습니다. 대안을 탐색하고 구현하기 위해 더 많은 시간을 요구하는 여러 고객 요청에 따라 **2023년 1월 31일**&#x200B;까지 제한된 방식으로 이 옵션을 복원하기로 결정했습니다.<p>시간별 Report Builder 작업을 계속 예약하고 최대 99회 발생 후 종료하도록 할 수 있습니다. 롤백은 시간별 작업에만 적용됩니다. “x회 발생 후 종료”는 다른 모든 제공 간격(일별, 주별, 월별 및 연간)에 대해 계속 사용할 수 없습니다. 이 옵션은 2023년 1월 31일에 사용이 중단됩니다. 추가 질문이 있거나 지원이 필요한 경우 Adobe 고객 지원 센터에 문의하십시오. [자세히 알아보기](/help/analyze/report-builder/r-arb-scheduled-reports.md) |
| **SFTP 업그레이드** | 2022년 5월 9일 | 이전에 Adobe는 파일 전송에 대한 보안을 개선하기 위해 2022년 5월에 SFTP(Secure File Transfer Protocol) 서비스를 업그레이드할 예정임을 공지했습니다. 이 업그레이드 일정이 **2022년 여름**&#x200B;으로 연기되었습니다. 이 변경 사항이 적용되면 일부 SFTP 클라이언트 구성은 더 이상 지원되지 않습니다. 이는 SFTP를 사용하여 Adobe Analytics로 전송되거나 Adobe Analytics에서 검색된 데이터에만 영향을 미칩니다. FTP 프로토콜은 영향을 받지 않습니다. 서비스 중단을 방지하려면 SFTP 클라이언트(코드, 도구, 서비스)가 [여기](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html?lang=ko-KR)에 설명된 변경 사항을 준수하는지 확인하십시오. |
| **특정 고객에 대해 지원되는 브라우저 암호화 방법에 대한 업데이트** | 2022년 3월 28일 | Adobe는 자사 데이터 수집에서의 보안에 대한 다양한 고객 요구 사항에 부합하는 두 가지의 암호 보안 수준을 제공합니다. **2022년 6월 23일**&#x200B;부터 보안 수준이 “높음”으로 설정되어 있는 고객에 대해 특정 HTTPS 암호화 알고리즘(암호라고도 함)에 대한 지원이 중단될 예정입니다. 이 작업은 일부 이전 운영 체제는 최신 암호화 방법을 지원하지 않으므로 더 이상 Analytics로 데이터를 전송하지 않게 됩니다. 기본 “표준” 암호 보안 설정을 사용 중인 고객은 영향을 받지 않습니다. 현재 “높음” 설정을 사용 중인 모든 고객에게는 이미 해당 공지가 직접 전송되었습니다. 영향을 받는 세부 암호 목록 |
| **2022 ISO 지역 업데이트** | 2021년 3월 11일 | Adobe에 대해 2022 ISO 지역 업데이트 수행 **2022년 6월 10일**. 이 릴리스 이후에 부분적인 지역 정보 업데이트가 있을 것으로 예상됩니다. |
| **[!DNL Reports & Analytics]**&#x200B;에 대한 EOL | 2022년 1월 4일 | **2023년 12월 31일**&#x200B;부로 Adobe는 [!DNL Reports & Analytics] 및 관련 보고서와 기능에 대한 서비스를 중단할 예정입니다. [!DNL Reports & Analytics]가 제공하는 보고서, 시각화 및 기반 기술은 더 이상 Adobe의 기술 표준을 충족하지 않습니다. 대부분의 [!DNL Reports & Analytics] 기능은 [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=ko-KR)에서 사용할 수 있습니다. 2015년 Analysis Workspace가 출시된 이후 [!DNL Reports & Analytics] 기능이 Analysis Workspace로 이전되면서 워크플로 패리티의 한계점에 도달했습니다. [이 공지 사항](https://spark.adobe.com/page/6WnF8JK6IRDhf/)은 서비스 종료 프로세스에 대해 설명합니다. |

{style=&quot;table-layout:auto&quot;}

### AppMeasurement

AppMeasurement 릴리스(버전 2.22.4)에 대한 최신 업데이트는 [JavaScript용 AppMeasurement 릴리스 정보](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=ko-KR)를 참조하십시오.

