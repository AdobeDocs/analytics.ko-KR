---
description: 'null'
title: 현재 서버 호출 사용량 보기
uuid: 1a42a45f-4bbc-4b5a-9706-c8937265de2b
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 현재 서버 호출 사용량 보기

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Server Call Usage]** > **[!UICONTROL Current Usage]**

>[!IMPORTANT] 표시되는 모든 사용량 및 약정 번호는 모든 로그인 회사 및 보고서 세트에 누적됩니다.

현재 사용 대시보드

* 각 서버 호출 유형에 대한 서버 호출 소비 및 약정 분류를 표시합니다. 이 견해는 고객마다 다를 수 있으며 계약에 포함된 내용과 일치합니다. 예를 들어, 4가지 유형의 서버 호출, 웹용 기본 및 보조, 모바일용 기본 및 보조 서버 호출을 각각 등록했을 수 있습니다. 이 경우 이 보기는 각 유형에 대해 하나씩 4개의 탭으로 구성됩니다. 각 탭에서 현재 사용 기간에 대한 소비를 볼 수 있습니다.
* 현재 사용량(녹색 라인)을 계약 사용량 제한(빨간색 라인)과 비교합니다.

   ![](assets/current_period.png)

* 현재 기간의 사용량을 작년 사용과 비교합니다(파란색 선). 분명히 파란색은 회사가 전년도의 서버 호출 사용 데이터를 가지고 있는 경우에만 나타납니다.

   > [!NOTE] 이전 기간에 대한 사용량을 보려면 [보고서 세트 사용량](/help/admin/c-server-call-usage/report-suite-usage.md) 탭으로 이동하여 이전 기간에 대한 사용 데이터를 다운로드해야 합니다.

* 사용된 호출 비율(백분율 및 원시 데이터)과 체류 기간 백분율(백분율 및 원시 데이터)을 나열합니다.
* 기본적으로 은 매일 업데이트되며 5일 처리 지연이 발생합니다.
* 모든 reportlet을 축소하고 확장할 수 있습니다.

![](assets/server_call_dashboard.png)

| UI 용어 | 정의 |
|---|---|
| 현재 기간 사용량(녹색) | 현재 기간은 [사용 기간을](/help/admin/c-server-call-usage/overage-overview.md)기반으로 합니다. |
| 이전 기간 사용량(파란색) | 이전 기간은 현재 사용 기간 빼기 1년으로 정의됩니다. |
| 사용량 제한(빨간색) | 이 사용 기간에 대한 계약 사용 제한. |
