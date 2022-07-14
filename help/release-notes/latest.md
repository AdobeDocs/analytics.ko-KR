---
title: 최신 Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: c14fc5f07d74ed3ab85e68e567f37712e4a92883
workflow-type: tm+mt
source-wordcount: '1104'
ht-degree: 96%

---

# 현재 Adobe Analytics 릴리스 정보 (2022년 6월)

**마지막 업데이트**: 2022년 7월 13일

## 관련 리소스

* [2022년 이전 릴리스 정보](/help/release-notes/2022.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=ko-KR)
* [Media Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=ko-KR)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트

## Adobe Analytics의 새로운 기능

| 기능 | 설명 | [목표 날짜](releases.md) |
| ----------- | ---------- | ------- |
| **새로운 플로우 시각화 UI** | 플로우 시각화를 보다 강력하고 유능하게 만드는 추가 기능을 제공합니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/flow/create-flow.html?lang=kr) | 롤아웃은 2022년 6월 15일 시작, GA는 2022년 6월 27일 또는 28일까지 |
| **모바일 스코어카드에서 주석 공유** | 모바일 스코어카드에서 작업 영역에 생성된 주석을 표시할 수 있습니다. 이를 통해 Analytics 대시보드 모바일 앱에서 볼 수 있는 모바일 스코어카드 프로젝트 내에서 조직 및 캠페인에 대한 상황별 데이터 뉘앙스와 통찰력을 직접 공유할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/components/annotations/mobile-annotations.html?lang=kr) | 2022년 6월 15일 |
| **Edge Collection이 있는 머천다이징 변수의 제품 구문 버전 지원** | 이제 관련 XDM 필드를 설정하여 제품 구문과 동일한 기능을 사용한 머천다이징 변수를 설정할 수 있습니다. `products` 변수가 포함된 웹 SDK 구문은 [제품 변수](../implement/vars/page-vars/products.md)를 참조하고, 사용 가능한 변수의 전체 목록은 [Adobe Experience Edge의 Analytics 변수 매핑](../implement/aep-edge/variable-mapping.md)을 참조하십시오. | 2022년 6월 15일 |
| **Experience Edge를 통해 라이프사이클 차원 및 지표 채우기** | Experience Edge를 통해 전송되는 모바일 라이프사이클 데이터가 이제 Analytics 보고에 표시됩니다. 기존 모바일 라이프사이클 보고에 매핑되는 XDM 필드에 대한 자세한 내용은 설명서를 참조하십시오. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) | 2022년 5월 27일 |
| **Analytics 처리 규칙에서 사용할 수 있는 모바일 서비스 처리 규칙** | Adobe Mobile Services 종료일은 2022년 12월 31일입니다. Adobe Mobile Services에서 만들거나 생성한 기존 처리 규칙은 Adobe Analytics 처리 규칙으로 자동으로 마이그레이션되며, 여기서 규칙을 편집하고 관리할 수 있습니다. 이러한 파일은 볼 수 있지만 제품이 만료될 때까지 모바일 서비스에서 더 이상 편집할 수 없습니다. 추가 질문이 있거나 지원이 필요한 경우 Adobe 고객 지원 센터에 문의하십시오. [자세히 알아보기](https://experienceleague.adobe.com/docs/mobile-services/using/eol.html?lang=kr) | 2022년 6월 15일 |
| **분류 세트 - 단계 1** | 새로운 분류 사용자 경험에 대한 이 단계적 릴리스는 고객 소유 분류 데이터에 대한 가시성을 크게 향상시킵니다. 자세한 내용은 [분류 세트](../components/classifications/sets/overview.md)를 참조하십시오. | 제한적인 테스트가 2022년 6월 15일에 시작됨, 일반 가용성은 2023년 초로 예상됨 |

{style=&quot;table-layout:auto&quot;}

### Adobe Analytics의 수정 사항

AN-251686; AN-283542; AN-286572; AN-286945; AN-286784; AN-286944; AN-287012; AN-287319; AN-287333; AN-287348; AN-287429; AN-288238; AN-288281; AN-288660; AN-288769; AN-288798; AN-288871; AN-288872; AN-288941; AN-288951; AN-288952; AN-288956; AN-289062; AN-289340; AN-289346; AN-289488; AN-289562; AN-289580; AN-289861; AN-289892;

### Adobe Analytics 관리자에 대한 중요 공지

| 공지 | 추가 또는 업데이트 날짜 | 설명 |
| ----------- | ---------- | ---------- |
| **시스템 생성 전자 메일의 새 도메인** | 2022년 7월 13일 | 설정 **2022년 5월 18일**, Adobe이 Workspace 프로젝트, 경고 및 초과 경고에서 보낸 사람의 도메인을 변경했습니다. `noreply@omniture.com` to `noreply@adobe.com`. 조직에서 특정 보낸 사람만 허용하는 경우 이 새 이메일을 허용 목록에 추가합니다. |
| **Reports &amp; Analytics에서 예약된 보고서 일시 중지** | 2022년 6월 8일 | 2022년 4월 21일에 이전에 발표된 Reports &amp; Analytics의 서비스 종료에 대비하여 예약된 보고서와 관련된 몇 가지 기능의 사용 중단을 발표했습니다. 이들 기능에는 새 보고서와 새 데이터 추출을 예약하는 기능이 포함되었습니다.<p>확장을 원하는 고객의 요청에 따라 Reports and Analytics에서 쉽게 전환할 수 있도록 이들 기능에 대한 액세스를 **2023년 1월 31일**&#x200B;까지 연장하기로 결정했습니다. 보고서와 데이터 추출의 만료 기간은 계속 9개월로 제한됩니다. 보고서 및 데이터 추출 전달은 일정이 다시 활성화되지 않는 한 이 기간이 끝나면 일시 중지됩니다.<p>반복해서 말씀드리지만, 이들 기능은 2023년 1월 31일에 사용이 중단됩니다. 해당 날짜 이전에 예약된 보고를 Adobe Analytics에서 사용할 수 있는 다른 메커니즘 중 하나로 마이그레이션해야 합니다. 추가 질문이 있거나 지원이 필요한 경우 Adobe 고객 지원 센터에 문의하십시오. [자세히 알아보기](/help/analyze/reports-analytics/scheduled-reports-eol.md) |
| **Report Builder에서 예약된 작업 일시 중지** | 2022년 6월 8일 | 2022년 4월 21일에 최적의 성능과 제공을 위한 노력의 일환으로 Report Builder의 예약된 작업에 대한 변경 사항이 배포되었습니다. 이러한 변경 사항에는 예약된 배달이 “x회 발생 후 종료”되도록 하는 기능의 제거가 포함되었습니다. 대안을 탐색하고 구현하기 위해 더 많은 시간을 요구하는 여러 고객 요청에 따라 **2023년 1월 31일**&#x200B;까지 제한된 방식으로 이 옵션을 복원하기로 결정했습니다.<p>계속해서 시간별 Report Builder 작업을 예약하고 최대 99회 발생 후 종료되도록 할 수 있습니다. 롤백은 시간별 작업에만 적용됩니다. “x회 발생 후 종료”는 다른 모든 제공 간격(일별, 주별, 월별 및 연간)에 대해 계속 사용할 수 없습니다. 이 옵션은 2023년 1월 31일에 사용이 중단됩니다. 추가 질문이 있거나 지원이 필요한 경우 Adobe 고객 지원 센터에 문의하십시오. [자세히 알아보기](/help/analyze/report-builder/r-arb-scheduled-reports.md) |
| **SFTP 업그레이드** | 2022년 5월 9일 | 이전에 Adobe는 파일 전송에 대한 보안을 개선하기 위해 2022년 5월에 SFTP(Secure File Transfer Protocol) 서비스를 업그레이드할 예정임을 공지했습니다. 이 업그레이드 일정이 **2022년 여름**&#x200B;으로 연기되었습니다. 이 변경 사항이 적용되면 일부 SFTP 클라이언트 구성은 더 이상 지원되지 않습니다. 이는 SFTP를 사용하여 Adobe Analytics로 전송되거나 Adobe Analytics에서 검색된 데이터에만 영향을 미칩니다. FTP 프로토콜은 영향을 받지 않습니다. 서비스 중단을 방지하려면 SFTP 클라이언트(코드, 도구, 서비스)가 [여기](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html?lang=ko-KR)에 설명된 변경 사항을 준수하는지 확인하십시오. |
| **특정 고객에 대해 지원되는 브라우저 암호화 방법에 대한 업데이트** | 2022년 3월 28일 | Adobe는 자사 데이터 수집에서의 보안에 대한 다양한 고객 요구 사항에 부합하는 두 가지의 암호 보안 수준을 제공합니다. **2022년 6월 23일**&#x200B;부터 보안 수준이 “높음”으로 설정되어 있는 고객에 대해 특정 HTTPS 암호화 알고리즘(암호라고도 함)에 대한 지원이 중단될 예정입니다. 이 작업은 일부 이전 운영 체제는 최신 암호화 방법을 지원하지 않으므로 더 이상 Analytics로 데이터를 전송하지 않게 됩니다. 기본 “표준” 암호 보안 설정을 사용 중인 고객은 영향을 받지 않습니다. 현재 “높음” 설정을 사용 중인 모든 고객에게는 이미 해당 공지가 직접 전송되었습니다. 이 변경의 영향을 받는 자세한 암호 목록은 다음과 같습니다. |
| **2022 ISO 지역 업데이트** | 2021년 3월 11일 | Adobe는 **2022년 6월 10일**&#x200B;에 2022 ISO 지역 업데이트를 수행했습니다. 이 릴리스 이후에 부분적인 지역 정보 업데이트가 있을 것으로 예상됩니다. |
| **[!DNL Reports & Analytics]**&#x200B;에 대한 EOL | 2022년 1월 4일 | **2023년 12월 31일**&#x200B;부로 Adobe는 [!DNL Reports & Analytics] 및 관련 보고서와 기능에 대한 서비스를 중단할 예정입니다. [!DNL Reports & Analytics]가 제공하는 보고서, 시각화 및 기반 기술은 더 이상 Adobe의 기술 표준을 충족하지 않습니다. 대부분의 [!DNL Reports & Analytics] 기능은 [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=ko-KR)에서 사용할 수 있습니다. 2015년 Analysis Workspace가 출시된 이후 [!DNL Reports & Analytics] 기능이 Analysis Workspace로 이전되면서 워크플로 패리티의 한계점에 도달했습니다. [이 공지 사항](https://spark.adobe.com/page/6WnF8JK6IRDhf/)은 서비스 종료 프로세스에 대해 설명합니다. |

{style=&quot;table-layout:auto&quot;}

### AppMeasurement

AppMeasurement 릴리스(버전 2.22.4)에 대한 최신 업데이트는 [JavaScript용 AppMeasurement 릴리스 정보](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=ko-KR)를 참조하십시오.

