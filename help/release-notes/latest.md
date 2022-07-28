---
title: 최신 Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: a71db2fac9333b70a55da91fe9a94b0cc8434b42
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 56%

---

# 현재 Adobe Analytics 릴리스 노트(2022년 7월)

**마지막 업데이트**: 2022년 7월 13일

## 관련 리소스

* [2022년 이전 릴리스 정보](/help/release-notes/2022.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html?lang=ko-KR)
* [Media Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=ko-KR)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트

## Adobe Analytics의 새로운 기능

| 기능 | 설명 | [목표 날짜](releases.md) |
| ----------- | ---------- | ------- |
| Edge Collection용 XDM에서 머천다이징 변수 지원 | Experience Edge/Web SDK를 통해 데이터를 수집하는 고객이 XDM을 사용하여 머천다이징 변수(eVars)에 대한 다양한 값을 지정할 수 있도록 합니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/evar-merchandising.html?lang=en) | 2022년 6월 29일 |

{style=&quot;table-layout:auto&quot;}

## Adobe Analytics의 수정 사항

* 일부 세그먼트 전환 오류를 수정했습니다. (AN-291262, AN-294092)

**개인 사용자 고객에 대한 수정 사항**:

AN-280192; AN-281628; AN-287022; AN-287104; AN-287876; AN-288802; AN-288457; AN-288779; AN-288799; AN-289198; AN-289852; AN-289931; AN-290162; AN-290213; AN-291059; AN-291090; AN-291270; AN-294091; AN-294135; AN-294152; AN-294158; AN-294285; AN-294317; AN-294404; AN-294531; AN-294769; AN-294984; AN-295172; AN-295211; AN-295224; AN-295413; AN-295440; AN-295465; AN-295499; AN-295516;

## Adobe Analytics 관리자에 대한 중요 공지

| 공지 | 추가 또는 업데이트 날짜 | 설명 |
| ----------- | ---------- | ---------- |
| **시스템 생성 이메일용 새 도메인** | 2022년 7월 13일 | 설정 **2022년 5월 18일**, Adobe이 Workspace 프로젝트, 경고 및 초과 경고에서 보낸 사람의 도메인을 변경했습니다. `noreply@omniture.com` to `noreply@adobe.com`. 귀사에서 특정 발신자만 허용하는 경우 이 새 이메일을 허용 목록에 추가하십시오. |
| **새 NetAcity Carrier 데이터베이스로 업데이트** | 2022년 7월 11일 | **2022년 10월부터**&#x200B;에 저장된 캐리어 관련 정보 `carrier` Adobe Analytics Data Warehouse 및 Analytics 데이터 피드의 필드가 변경됩니다. 이전에는 해당 열의 데이터 형식이 `<domain>:<ISP>`. Adobe은 이러한 테이블을 매핑하기 위해 내부 조회 테이블을 유지 관리했습니다 `<domain>:<ISP>` Adobe Analytics 보고 도구(Analysis Workspace, Reports &amp; Analytics, 보고 API, Data Warehouse, LiveStream 등)에서 보고를 위해 통신사 이름에 값을 포함함 조회 파일(carrier.tsv)도 데이터 피드와 함께 제공되므로 데이터 피드는 고객이 동일한 매핑을 사용할 수 있습니다.<p>이 업데이트는 NetAcity에서 보다 정확한 캐리어 데이터베이스를 사용하여 캐리어 매핑을 향상시킵니다. 데이터 피드의 통신사 열에 있는 데이터 형식은 앞으로 변경됩니다. 대신 `<domain>:<ISP>`에 캐리어 이름이 포함됩니다. Adobe은 이전 보고와 가능한 한 많은 연속성을 유지하기 위해 조회 테이블을 계속 사용합니다. Adobe(Analysis Workspace, Reports &amp; Analytics, 보고 API, Data Warehouse, LiveStream 등)에서 조회가 적용되는 보고 도구 은 보다 정확한 매핑의 이점을 제공합니다. 일부 매핑(특히 국제 도메인 및 ISP의 경우)은 새 데이터베이스를 채택할 때 다른 매핑보다 많이 변경됩니다. 데이터 피드 통신사 조회 파일(carrier.tsv)은 이전 매핑을 유지하고 새 매핑을 추가합니다.<p>Analytics 소스 커넥터는 현재 캐리어 필드를 매핑하지 않으므로 현재 AEP, CJA 등에서 캐리어 보고를 사용할 수 없습니다. 따라서 새 통신사 데이터베이스의 사용은 Analytics 소스 커넥터에서 제공한 데이터를 기반으로 하는 AEP의 어떤 데이터에도 영향을 주지 않습니다. |
| **향상된 IP-지리적 위치 매핑** | 2022년 7월 11일 | IP 조회 공급업체인 Digital Element 는 IP-to-geolocation 매핑을 위해 향상된 데이터 세트(NetAcity Pulse)로 업그레이드하고 있습니다. Adobe Analytics은 이 새 데이터 세트를 **2022년 10월** 일정. 새 데이터베이스가 이전 버전보다 더 정확할 것입니다. 일부 IP-지역 매핑은 새 데이터베이스가 채택되면 변경/개선됩니다.<p>모든 Adobe Analytics 도구(Analysis Workspace, Reports &amp; Analytics, 보고 API, Data Warehouse, LiveStream, 데이터 피드 등)는 은 새롭게 향상된 매핑을 자동으로 이용합니다. 데이터 피드의 데이터 형식은 변경되지 않습니다. Analytics 소스 커넥터를 통해 제공된 CJA 데이터도 새로운 매핑을 자동으로 활용할 수 있습니다. |
| **Reports &amp; Analytics에서 예약된 보고서 일시 중지** | 2022년 6월 8일 | 2022년 4월 21일에 이전에 발표된 Reports &amp; Analytics의 서비스 종료에 대비하여 예약된 보고서와 관련된 몇 가지 기능의 사용 중단을 발표했습니다. 이들 기능에는 새 보고서와 새 데이터 추출을 예약하는 기능이 포함되었습니다.<p>확장을 원하는 고객의 요청에 따라 Reports and Analytics에서 쉽게 전환할 수 있도록 이들 기능에 대한 액세스를 **2023년 1월 31일**&#x200B;까지 연장하기로 결정했습니다. 보고서와 데이터 추출의 만료 기간은 계속 9개월로 제한됩니다. 보고서 및 데이터 추출 전달은 일정이 다시 활성화되지 않는 한 이 기간이 끝나면 일시 중지됩니다.<p>반복해서 말씀드리지만, 이들 기능은 2023년 1월 31일에 사용이 중단됩니다. 해당 날짜 이전에 예약된 보고를 Adobe Analytics에서 사용할 수 있는 다른 메커니즘 중 하나로 마이그레이션해야 합니다. 추가 질문이 있거나 지원이 필요한 경우 Adobe 고객 지원 센터에 문의하십시오. [자세히 알아보기](/help/analyze/reports-analytics/scheduled-reports-eol.md) |
| **Report Builder에서 예약된 작업 일시 중지** | 2022년 6월 8일 | 2022년 4월 21일에 최적의 성능과 제공을 위한 노력의 일환으로 Report Builder의 예약된 작업에 대한 변경 사항이 배포되었습니다. 이러한 변경 사항에는 예약된 배달이 “x회 발생 후 종료”되도록 하는 기능의 제거가 포함되었습니다. 대안을 탐색하고 구현하기 위해 더 많은 시간을 요구하는 여러 고객 요청에 따라 **2023년 1월 31일**&#x200B;까지 제한된 방식으로 이 옵션을 복원하기로 결정했습니다.<p>계속해서 시간별 Report Builder 작업을 예약하고 최대 99회 발생 후 종료되도록 할 수 있습니다. 롤백은 시간별 작업에만 적용됩니다. “x회 발생 후 종료”는 다른 모든 제공 간격(일별, 주별, 월별 및 연간)에 대해 계속 사용할 수 없습니다. 이 옵션은 2023년 1월 31일에 사용이 중단됩니다. 추가 질문이 있거나 지원이 필요한 경우 Adobe 고객 지원 센터에 문의하십시오. [자세히 알아보기](/help/analyze/report-builder/r-arb-scheduled-reports.md) |
| **SFTP 업그레이드** | 2022년 5월 9일 | 이전에 Adobe는 파일 전송에 대한 보안을 개선하기 위해 2022년 5월에 SFTP(Secure File Transfer Protocol) 서비스를 업그레이드할 예정임을 공지했습니다. 이 업그레이드 일정이 **2022년 여름**&#x200B;으로 연기되었습니다. 이 변경 사항이 적용되면 일부 SFTP 클라이언트 구성은 더 이상 지원되지 않습니다. 이는 SFTP를 사용하여 Adobe Analytics로 전송되거나 Adobe Analytics에서 검색된 데이터에만 영향을 미칩니다. FTP 프로토콜은 영향을 받지 않습니다. 서비스 중단을 방지하려면 SFTP 클라이언트(코드, 도구, 서비스)가 [여기](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html?lang=ko-KR)에 설명된 변경 사항을 준수하는지 확인하십시오. |
| **[!DNL Reports & Analytics]**&#x200B;에 대한 EOL | 2022년 1월 4일 | **2023년 12월 31일**&#x200B;부로 Adobe는 [!DNL Reports & Analytics] 및 관련 보고서와 기능에 대한 서비스를 중단할 예정입니다. [!DNL Reports & Analytics]가 제공하는 보고서, 시각화 및 기반 기술은 더 이상 Adobe의 기술 표준을 충족하지 않습니다. 대부분의 [!DNL Reports & Analytics] 기능은 [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=ko-KR)에서 사용할 수 있습니다. 2015년 Analysis Workspace가 출시된 이후 [!DNL Reports & Analytics] 기능이 Analysis Workspace로 이전되면서 워크플로 패리티의 한계점에 도달했습니다. [이 공지 사항](https://spark.adobe.com/page/6WnF8JK6IRDhf/)은 서비스 종료 프로세스에 대해 설명합니다. |

{style=&quot;table-layout:auto&quot;}

## AppMeasurement

AppMeasurement 릴리스(버전 2.22.4)에 대한 최신 업데이트는 [JavaScript용 AppMeasurement 릴리스 정보](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=ko-KR)를 참조하십시오.

