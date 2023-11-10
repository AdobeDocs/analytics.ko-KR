---
title: 현재 Adobe Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: dfb3750edabed3fd9aef758d2ea1625fc3fb6a96
workflow-type: tm+mt
source-wordcount: '1131'
ht-degree: 100%

---

# 현재 Adobe Analytics 릴리스 정보 (2023년 10월/11월)

**마지막 업데이트**: 2023년 10월 25일

이번 릴리스 정보에는 2023년 10월 23일부터 2023년 11월 말일까지의 릴리스 기간이 포함됩니다. Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 새로운 기능 또는 개선 사항 {#features}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **보고 활동 관리자 개선 사항** | 보고 활동 관리자를 사용하면 조직의 각 보고서 세트에 대한 보고 용량을 확인할 수 있습니다.  이는 관리자에게 보고 사용량에 대해 상세한 가시성을 제공하며 최대 보고 시간 동안 발생할 수 있는 용량 문제를 쉽게 진단하고 해결할 수 있도록 해 줍니다. 이제 보고 활동 관리자에서 사용할 수 있는 몇 가지 개선 사항은 다음과 같습니다. <ul><li>후속 요청 제한: 현재 요청을 취소하는 것 외에도 관리자는 이제 정의된 기간 동안 요청을 제한할 수 있습니다. 관리자는 요청, 프로젝트 및 사용자별로 요청을 제한할 수 있습니다.</li><li>활용성 및 용량 지표 외에도 이제 보고 활동 관리자에는 보고 활동에 대한 추가 데이터(복잡성 열, 사용자 열, 연결 열)가 포함됩니다.</li><li>이제 보고 활동 관리자에서 이루어진 모든 취소 및 제한 사항이 감사 로그에 표시됩니다. 관리자는 감사 로그를 사용하여 현재 취소된 내용을 확인할 수 있습니다. 취소는 보고 활동 관리자 또는 감사 로그에서 되돌릴 수 없습니다.</li></ul><p>자세한 내용은 [보고 활동 관리자 개요](/help/admin/admin/reporting-activity-manager/reporting-activity-overview.md)를 참조하십시오.</p> | 2023년 10월 17일 | 2023년 10월 24일 |
| **Data Warehouse 개선 사항** | Data Warehouse 요청을 만들 때 이제 보고서 대상으로 사용할 클라우드 계정을 구성할 수 있습니다. 다음 클라우드 계정 유형을 데이터 전송에 사용할 수 있습니다.<ul><li>Amazon S3</li><li>Google Cloud 플랫폼</li><li>Azure SAS</li><li>Azure RBAC</li><li>이메일(이 옵션은 이전에 사용 가능했음)</li></ul>FTP, SFTP, Azure Blob 및 S3는 여전히 보고서 대상으로 사용할 수 있지만 더 이상 권장되지 않습니다.<p>Data Warehouse 요청을 생성하고 관리할 때의 사용자 경험도 개선되었습니다. 자세한 내용은 [Data Warehouse 요청 만들기](/help/export/data-warehouse/create-request/t-dw-create-request.md) 및 [Data Warehouse 요청 관리](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse-requests-manage.html)를 참조하십시오. | 2023년 9월 12일 | TBD |

{style="table-layout:auto"}

## Adobe Analytics의 수정 사항

* 이들 Analytics 처리 및 보고 엔진 변경 사항은 10월 마지막 주에 배포될 예정이며, 페이지 또는 링크 차원의 레이블이 `Unknown`과 같이 잘못 표시되는 문제를 해결할 예정입니다. 수정 작업이 완료되기 전까지는 히트 시 페이지 이름 또는 링크 이름이 전달되지 않았을 때 `Unknown` 레이블이 잘못 표시될 수 있으며, 기본값은 각각 [!UICONTROL 페이지 URL]과 [!UICONTROL 링크 URL]이 됩니다. 이들 차원은 대소문자를 구분하지 않도록 구성되었습니다. 이번 수정을 통해 향후 보고서는 정확해질 것입니다. 단, 내역 데이터에 대한 보고서의 경우 일부 보고서 결과는 여전히 `Unknown`으로 잘못 표시될 수 있습니다. (AN-328030)

### 기타 수정 사항

-315676; AN-; AN-323398; AN-326209; AN-328178; AN-328261; AN-328395; AN-328671; AN-329282; AN-329330; AN-329355; AN-329506; AN-329516; AN-329738; AN-329769; AN-329771; AN-329816; AN-329877; AN-329928; AN-329957; AN-329962; AN-329966; AN-330023; AN-330081; AN-330083; AN-330105; AN-330138; AN-330140; AN-330165; AN-330241; AN-330359; AN-330366; AN-330427; AN-330438; AN-330442; AN-330534; AN-330616; AN-330654; AN-330783; AN-330879; AN-330881; AN-330883; AN-330887; AN-330888; AN-330955; AN-330979; AN-331031; AN-331053; AN-331068; AN-331071; AN-331074; AN-331075; AN-331076; AN-331078; AN-331085; AN-331093; AN-331167; AN-331171; AN-331181; AN-331196; AN-331226; AN-331258; AN-331260; AN-331279; AN-331286; AN-331290; AN-331365; AN-331375; AN-331376; AN-331454; AN-331519; AN-331570; AN-331590; AN-331593; AN-331603; AN-331751; AN-331816; AN-331897; AN-331900; AN-331906; AN-331926; AN-331929; AN-332031; AN-332067; AN-332101; AN-332114; AN-332156; AN-332201; AN-332225; AN-332253; AN-332277; AN-332361; AN-332370; AN-332386

## Adobe Analytics 관리자에 대한 중요 공지 {#admin}

| 공지 | 추가 또는 업데이트 일자 | 설명 |
| ----------- | ---------- | ---------- |
| **Adobe Experience Edge 히트에 대한 전체 IP 난독화** | 2023년 9월 27일 | Experience Edge에서 발생한 히트에 대한 IP 난독화는 2023년 10월 말경에 업데이트될 예정입니다. Experience Edge에는 IP 주소를 난독화할 수 있는 기능이 2023년 4월에 추가되었습니다. 해당 시점에 Analytics가 Experience Edge의 히트를 처리하는 방식으로 인해 Adobe Analytics에서는 IP의 부분적인 난독화만 지원되었습니다. 고객이 Experience Edge에 대해 전체 난독화를 선택한 경우 Analytics는 부분적으로 난독화된 IP만 수신했습니다. 이 변경 사항이 구현되면 Analytics는 전체 난독화된 IP를 수신하게 됩니다. |
| **Adobe Analytics 라이브스트림 - Analytics 2.0 API** | 2023년 9월 27일 | 이제 고객은 1.4 API를 사용하는 이전 위치 대신 Adobe Analytics 2.0 API에서 [Adobe Analytics 라이브스트림용 엔드포인트 안내서](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/livestream/)에 액세스할 수 있습니다. Adobe I/O JWT 자격 증명을 사용하는 고객은 2025년 1월 1일까지 Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. (아래 EOL 공지의 세부 사항을 확인하십시오.) |

{style="table-layout:auto"}

## 서비스 종료(EOL) 알림 {#eol}

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션** | 2023년 5월 11일 | Adobe I/O JWT 자격 증명을 사용하는 Adobe Analytics API 및 Livestream 고객은 **2025년 1월 1일**&#x200B;까지 Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 2024년 5월 1일부터는 Adobe I/O를 사용하여 새 JWT 자격 증명을 만들 수 없습니다. JWT를 사용하는 고객은 OAuth 서버 간 자격 증명을 새로 만들거나 기존 JWT 자격 증명을 OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 또한 고객은 새 OAuth 서버 간 자격 증명을 사용하려면 클라이언트 애플리케이션을 업데이트해야 합니다. <ul><li>[서비스 계정(JWT) 자격 증명에서 마이그레이션](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[OAuth를 사용한 신규 및 기존 애플리케이션 구현 안내서](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)<li>[새 OAuth 서버 간 자격 증명 사용](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[FAQ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |
| **[!DNL Reports & Analytics]**&#x200B;에 대한 EOL | 2023년 3월 7일 | **2023년 12월 31일**&#x200B;부로 Adobe는 [!DNL Reports & Analytics] 및 관련 보고서와 기능에 대한 서비스를 중단할 예정입니다. [!DNL Reports & Analytics]가 제공하는 보고서, 시각화 및 기반 기술은 더 이상 Adobe의 기술 표준을 충족하지 않습니다. 대부분의 [!DNL Reports & Analytics] 기능은 [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html)에서 사용할 수 있습니다. 2015년 Analysis Workspace가 출시된 이후 [!DNL Reports & Analytics] 기능이 Analysis Workspace로 이전되면서 워크플로 패리티의 한계점에 도달했습니다. [이 공지 사항](https://spark.adobe.com/page/6WnF8JK6IRDhf/)은 서비스 종료 프로세스에 대해 설명합니다.<p>2023년 12월 31일에 예약된 보고서, 데이터 추출, DL 보고서를 포함하되 이에 국한되지 않는 많은 관련 Reports &amp; Analytics 기능이 종료됩니다. 2023년 12월 31일 이후에는 예약된 보고서가 더 이상 전송되지 않습니다. **2023년 4월**, 2023년 12월 31일 이후에 만료되도록 예정된 모든 보고서가 자동으로 업데이트되고 2023년 12월 31일에 만료되도록 되돌려집니다. 또한 2023년 12월 31일 이후에는 더 이상 향후 보고서를 예약할 수 없습니다. |
| **[!UICONTROL 게시 목록] 기능의 EOL** | 2022년 9월 29일 | Reports &amp; Analytics EOL의 일환으로 [!UICONTROL 게시 목록]은 **2023년 12월**&#x200B;에 서비스가 종료됩니다. [!UICONTROL Analysis Workspace] 프로젝트를 보내거나 예약하기 위해 새 게시 목록을 만들거나 기존 [!UICONTROL 게시 목록]에 액세스할 수 없습니다. |
| **Data Workbench용 EOL** | 2022년 9월 14일 | Adobe는 **2023년 12월 31일**&#x200B;부로 Data Workbench의 서비스를 종료할 예정입니다. 자세한 내용은 [Data Workbench 서비스 종료 공지](https://experienceleague.adobe.com/docs/data-workbench/using/eol.html)를 참조하십시오. 문의 사항이 있으면 조직의 Adobe 계정 관리자에게 문의하십시오. |

{style="table-layout:auto"}

## AppMeasurement

AppMeasurement 릴리스(버전 2.25.0)에 대한 최신 업데이트는 [JavaScript용 AppMeasurement 릴리스 정보](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html)를 참조하십시오.


## 관련 리소스

* [2022년 이전 릴리스 정보](/help/release-notes/2022.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [Media Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트
