---
description: Adobe Analytics에서 현재 서버 호출 사용을 보는 방법.
title: 현재 서버 호출 사용량 보기
feature: Server Call Usage
exl-id: 07eac732-b9d6-41ab-be34-5688eaa8166e
role: Admin
TQID: 'https://experienceleague.adobe.com/5DgWR4QWklOEMK1Ato17-lcpMdnRgaIrMfds9ATXUpE'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: f73667dc-d296-4875-8975-ac3fdc3adc42id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
subfeature_v2: id: c9d85838-8d05-4bc7-9f18-30ec779251bc
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 293
ht-degree: 58%

---

# 현재 서버 호출 사용량 보기

**[!UICONTROL Analytics]** > **[!UICONTROL 관리]** > **[!UICONTROL 서버 호출 사용량]** > **[!UICONTROL 현재 사용량]**

>[!IMPORTANT]
>
>표시되는 모든 사용량 및 약정 번호는 모든 로그인 회사 및 보고서 세트에 누적됩니다.

현재 사용량 대시보드

* 각 서버 호출 유형에서 서버 호출 사용량 및 약정에 대한 분류를 표시합니다. 이 보기는 고객마다 다를 수 있으며 계약에 포함된 내용과 일치합니다. 예를 들어 4개의 별도 서버 호출 유형 (웹 기본 및 보조와 모바일 기본 및 보조)에 등록했을 수 있습니다. 이 경우 이 보기는 4개의 탭 (각 유형에 대해 한 개 탭)으로 구성됩니다. 각 탭 내에서 현재 사용 기간에 대한 소비를 볼 수 있습니다.
* 현재 사용량 (녹색 선)과 계약상 사용량 한도 (빨간색 선)를 비교합니다.

  ![](/help/admin/tools/server-call-usage/assets/current_period.png)

* 현재 기간의 사용량과 작년의 사용량 (파란색 선)을 비교합니다. 분명히 파란색 선은 회사에 이전 연도의 서버 호출 사용량 데이터가 있는 경우에만 나타납니다.

  >[!NOTE]
  >
  >이전 기간에 대한 사용량을 보려면 [보고서 세트 사용량](/help/admin/tools/server-call-usage/report-suite-usage.md) 탭으로 이동하여 이전 기간에 대한 사용 데이터를 다운로드해야 합니다.

* 사용된 호출 수의 백분율 (백분율 및 원시 데이터)과 소비된 사용 기간의 백분율 (백분율 및 원시 데이터)을 나열합니다.
* 기본적으로 은 매일 업데이트되며, 5일 처리 지연이 있습니다.
* 모든 reportlet을 축소하고 확장할 수 있습니다.

![](/help/admin/tools/server-call-usage/assets/server_call_dashboard.png)

| UI 용어 | 정의 |
| --- | --- |
| 현재 기간 사용량 (녹색) | 현재 기간은 [사용 기간](/help/admin/tools/server-call-usage/overage-overview.md)을 기반으로 합니다. |
| 이전 기간 사용량 (파란색) | 이전 기간은 현재 사용기간에서 1년을 차감한 기간으로 정의된다. |
| 사용량 한도 (빨간색) | 이 사용 기간에 대한 계약상 사용 한도. |
