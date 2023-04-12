---
title: 최신 Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기.
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: 611477ef794464de0b05b45e8445ed8fdd32b154
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 현재 Adobe Analytics 릴리스 정보 (2023년 4월)

**마지막 업데이트**: 2023년 4월 12일

Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## Adobe Analytics의 새로운 기능 또는 업데이트 {#features}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Analytics 소스 커넥터 스트리밍을 위한 행/열 필터링** | 이제 Adobe Experience Platform의 Analytics 소스 커넥터를 통해 [실시간 고객 프로필](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=ko)에 프로필을 채우는 데 사용되는 Analytics 데이터를 필터링할 수 있습니다. 행 수준 필터링은 프로필과 관련된 이벤트 수를 줄이는 데 도움이 됩니다. 열 수준 필터링은 이벤트 자체의 내용을 줄이는 데 도움이 되므로 프로필 자격 사용을 최적화할 수 있습니다. 이 필터링은 실시간 고객 프로필 및 [ID 서비스](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=ko)로 전송된 데이터에만 적용됩니다. **필터링은 Customer Journey Analytics와 같은 애플리케이션에서 사용하기 위해 데이터 레이크로 전송되는 데이터에 영향을 미치지 않습니다**. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=ko#filtering-for-profile) | 해당 사항 없음 | 2023년 3월 29일 |
| **Web SDK로 Activity Map 부분 지원** | Web SDK 버전 2.15.0부터는 링크 추적이 활성화되면 Activity Map 데이터를 채우게 됩니다. 이를 통해 Web SDK 사용자는 Analytics에서 구성된 Web SDK 및 Activity Map으로 링크 추적을 활성화한 경우 Activity Map 보고서를 받을 수 있습니다.<p>Web SDK로 링크 추적을 활성화하면 현재 고객이 하나의 페이지에서 다음 페이지로 이동할 때 링크 이벤트를 전송합니다. 이는 AppMeasurement가 작동하는 방식과 다르며 잠재적으로 Adobe로 전송되는 추가 청구 가능 히트를 초래할 수 있습니다. [여기](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/track-links.html) 및 [여기](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md)에서 자세히 알아보십시오. | 해당 사항 없음 | 2023년 3월 31일 |
| **Experience Edge용 IP 난독화** | Experience Edge는 Adobe Experience Platform으로 직접 전송된 데이터에 대해 IP 난독화를 지원합니다. CJA 또는 기타 플랫폼 솔루션에서 사용할 수 있도록 데이터를 플랫폼으로 직접 전송하는 고객이 이러한 혜택을 누릴 수 있습니다. IP 난독화는 데이터 스트림 수준에서 구성됩니다. 마지막 8진수나 전체 IP 주소 제거를 지원합니다.<p>**참고**: 난독화는 Adobe Analytics에 전송된 데이터에는 적용되지 않습니다. Analytics는 계속해서 전체 IP를 가져옵니다. IP 처리는 Analytics에서 별도로 계속 수행됩니다. 미래에는 Analytics 데이터가 Edge에서 난독화되도록 할 계획입니다. | 해당 사항 없음 | 2023년 4월 26일 AEP 릴리스 |
| **Analysis Workspace의 데이터 사전** | 데이터 사전을 통해 사용자와 관리자 모두가 Analytics 환경의 구성 요소(차원, 지표)를 추적하고 관리하고 더 잘 이해할 수 있습니다. [자세히 알아보기](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md) | 2023년 3월 15일 | 2023년 3월 29일 |
| **프로젝트 링크 공유(로그인 불필요)** - Private Beta 액세스 전용 | <p>이제 Adobe Analytics에 액세스할 수 없는 사용자에게 Analysis Workspace 프로젝트에 대한 읽기 전용 링크를 공유할 수 있습니다. 조직 외부의 사람들 또는 Adobe Analytics에 대해 프로비저닝되지 않은 조직 내의 사람들과 프로젝트 링크를 공유할 수 있습니다. [자세히 알아보기](/help/analyze/analysis-workspace/curate-share/share-projects.md)</p> <p>Private Beta에 참여하려면 Adobe 계정 팀에 문의하십시오.</p> | 2023년 4월 26일 | 2023년 6월 |

{style="table-layout:auto"}

## Adobe Analytics의 수정 사항

* 데이터 피드의 운영 체제.tsv 조회 파일 문제를 해결했습니다.
* Reports &amp; Analytics와 작업 공간 간에 지표 값이 다른 문제를 수정했습니다(AN-315965).
* 부분 분류를 가져올 수 없는 문제가 해결되었습니다. (AN-315854)
* Analytics API 1.4 문제를 수정했습니다. (AN-316475)
* 일부 고객이 Report Builder 및 Report &amp; Analytics를 통해 페이지 차원에 대한 분류를 받지 못하던 문제를 수정했습니다. (AN-314445)
* 경고를 전송할 수 없는 문제가 해결되었습니다. (AN-306457)

### 기타 수정 사항

AN-288373; AN-305144; AN-309023; AN-310466; AN-311686; AN-311705; AN-312018; AN-312105; AN-312116; AN-312191; AN-312502; AN-312737; AN-312854; AN-312991; AN-313253; AN-313275; AN-313278; AN-313282; AN-313365; AN-313390; AN-313547; AN-313549; AN-313818; AN-313986; AN-314080; AN-314248; AN-314251; AN-314262; AN-314300; AN-314309; AN-314448; AN-314643; AN-314564; AN-314645; AN-314705; AN-314761; AN-314831; AN-314919; AN-314948; AN-315032; AN-315115; AN-315154; AN-315158; AN-315321; AN-315375; AN-315379; AN-315392; AN-315407; AN-315427; AN-315582; AN-315591; AN-315699; AN-315700; AN-315704; AN-315705; AN-315777; AN-315923; AN-316237; AN-316243; AN-316324; AN-316415; AN-316474; AN-316493; AN-316596; AN-316864;

## Adobe Analytics 관리자에 대한 중요 공지 {#admin}

| 공지 | 추가 또는 업데이트 일자 | 설명 |
| ----------- | ---------- | ---------- |
| **디바이스 조회 프로세스는 이제 모든 디바이스 조회에 서드파티를 사용합니다** | 2023년 3월 3일 | 2023년 3월 2일 클라이언트 힌트 지원 롤아웃의 일환으로 모든 디바이스 조회에 서드파티를 사용하도록 디바이스 조회 프로세스를 업데이트했습니다. 이전에는 모바일 디바이스 조회에만 서드파티를 사용했습니다. 상기 롤아웃에서 일부 데스크탑 운영 체제에 “모바일”이라는 텍스트가 잘못 표시되어 있습니다(예: “OS X 10.15.7” 대신 “모바일 OS X 10.15.7”).<p>Adobe의 4월 릴리스에서 이들 이름을 수정할 예정입니다. Analytics 및 CJA 보고는 이벤트 데이터의 일부로 기록된 ID를 기반으로 운영 체제 이름을 조회하므로 소급하여 업데이트됩니다. ID에 해당하는 조회 값이 업데이트되면 내역 데이터를 포함하여 모든 보고가 수정됩니다. [!UICONTROL 데이터 피드] 고객의 경우 보고 시 유사한 조회 프로세스를 사용하면 변경이 소급 적용됩니다. 그러나 이벤트 데이터에 운영 체제 값을 저장하면 전향적으로만 보고가 업데이트됩니다. 자세한 내용은 [운영 체제](/help/components/dimensions/operating-systems.md)를 참조하십시오. |
| **Google 클라이언트 힌트로 인한 디바이스 조회 업데이트** | 2023년 2월 27일 | 2023년 2월 16일로 예정되었던 클라이언트 힌트 사용은 힌트를 사용한 디바이스 조회 품질을 더 잘 보장하기 위해 연기되었습니다. 2023년 2월 27일에 클라이언트 힌트 지원을 위한 첫 번째 릴리스 단계가 진행되었습니다. 릴리스의 두 번째이자 마지막 단계는 2023년 3월 2일 목요일에 완료되었습니다. [자세히 알아보기](/help/technotes/client-hints.md) |
| **분류 세트 아키텍처로 자동 마이그레이션** | 2023년 2월 8일 | Adobe는 앞으로 몇 달 동안 전 조직의 모든 분류를 최신 분류 아키텍처로 마이그레이션할 계획입니다. 마이그레이션할 마지막 고객은 2023년 5월에 발생할 것으로 예상됩니다. 고객 조치가 필요하지 않으며 중단 시간은 예상되지 않습니다. 이러한 새로운 아키텍처에는 다음과 같은 많은 이점이 있습니다.<ul><li>처리 시간 대폭 단축 (72시간 → 24시간)</li><li>[분류 세트](/help/components/classifications/sets/overview.md) UI를 사용하는 기능</li><li>[분류 데이터용 Adobe Analytics 소스 커넥터](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/classifications.html)를 통해 향후 Adobe Experience Platform에서 분류 데이터를 사용하는 옵션</li></ul>조직 워크플로에 잠재적으로 영향을 줄 수 있는 다음 변경 사항에 유의하십시오.<ul><li>브라우저 또는 FTP 가져오기를 사용하는 경우, &#39;[!UICONTROL 충돌 시 덮어쓰기]&#39;가 항상 활성화됩니다.</li><li>브라우저 또는 FTP 가져오기를 사용할 때 가져오기 직후 내보내기 옵션은 더 이상 지원되지 않습니다.</li><li>Analytics 2.0 API `GetDimensions` 엔드포인트는 이제 숫자 식별자 대신 분류에 대한 문자열 식별자를 반환합니다. 숫자 식별자를 계속 사용할 수 있지만 가능한 경우 새 문자열 식별자를 사용하는 것이 좋습니다. 숫자 식별자는 `?expansion=hidden` 쿼리 문자열 매개변수를 사용하여 검색할 수 있습니다.</li></ul>조직에 대한 보다 구체적인 마이그레이션 일정을 원하거나 이 마이그레이션에 대한 질문/우려 사항이 있는 경우 Adobe 고객 지원 센터에 문의하십시오. [자세히 알아보기](/help/components/classifications/sets/overview.md) |

{style="table-layout:auto"}

## 서비스 종료(EOL) 알림 {#eol}

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **일본 피처폰 추적 서비스 종료** | 2023년 3월 21일 | 일본 고객에게만 해당됩니다. 에서 **2023년 5월 말**&#x200B;로 설정되면 일본어 기능 전화 추적 서비스(mod_ktrack)가 중단됩니다. 불편을 드려 죄송합니다. Apache 서버에 설치된 모듈을 제거하거나 비활성화하시기 바랍니다. [이 문서](/help/release-notes/mod_ktrackforSiteCatalyst_ver1.40.pdf)의 27페이지와 28페이지를 참조하십시오. |
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
