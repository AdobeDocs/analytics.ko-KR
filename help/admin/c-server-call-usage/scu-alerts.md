---
description: 서버에 모든 사용량 경고를 추가하거나 관리합니다. 경고를 설정하면 청구 회사의 모든 로그인 회사에 있는 모든 보고서 세트에 적용됩니다.
title: 서버 호출 사용량 경고
uuid: 701fd542-5b24-42df-97a0-08e10929fa48
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8

---


# 서버 호출 사용량 경고

경고를 설정하면 청구 회사의 모든 로그인 회사에 있는 모든 보고서 세트에 적용됩니다.

## 개요

A new alert category called **[!UICONTROL Server Calls Usage Alert]** is part of the existing [Alert Management](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/virtual-analyst/intelligent-alerts/intellligent-alerts.html) user interface.

이 경고는 서버 호출 사용량 기능에 액세스할 수 있는 모든 로그인 회사 내에 표시되는 **1개의 기본 경고**&#x200B;로 미리 채워져 있습니다. 이 경고는 다음 기준 중 하나가 충족되는 경우 모든 로그인 회사 관리자에게 지정된 알림을 트리거합니다.

* 귀사에 부여된 서버 호출 유형에 대해 100%&quot;보다 크거나 같은&quot; &quot;모든&quot; 서버 호출 사용량 또는
* 귀사에 부여된 서버 호출 유형에 대해 90%&quot;보다 크거나 같은&quot; &quot;모든&quot; 서버 호출 사용량 또는
* 귀사에 부여된 서버 호출 유형에 대해 75%&quot;보다 크거나 같은&quot; &quot;모든&quot; 서버 호출 사용량 및 &quot;소비된 사용 기간&quot;이 사용 기간의 75%&quot;보다 작거나 같음&quot;

![](assets/alerts.png)

다음 두 가지 방법으로 서버 호출 사용량 경고에 액세스할 수 있습니다.

* Click **[!UICONTROL Manage Alerts]** in the upper right corner on the Current Usage tab or the Report Suite usage tab, or
* Adobe **[!UICONTROL Components]** Analytics **[!UICONTROL Alerts]** 에서 > 로 이동합니다.

## 서버 호출 사용량 경고 작성 {#section_2A2882C6D48D47C1944D52FB7C766BEC}

추가 경고를 작성하려면 다음을 수행하십시오.

1. 을 **[!UICONTROL + Add]** 클릭하고 **[!UICONTROL Server Call Usage Alert]**&#x200B;선택합니다.

   ![](assets/server_call_alert.png)

1. 경고를 정의합니다.

   ![](assets/sc_alert.png)

   * **제목**: 설명하는 이름을 지정합니다. 이름 없이 경고를 저장할 수 없습니다.
   * **시간 세부기간**: 경고를 확인하는 빈도를 말합니다. *현재 주별 세분기간만 지원합니다.* 즉, 경고가 주별로 확인되며, 현재 사용 기간에서 데이터를 다시 확인함을 의미합니다.
   * **수신자**: 경고가 지정된 임계 값을 트리거할 때 이메일을 받을 조직의 사용자를 지정합니다.
   * **만료 날짜**: 기본적으로 만료일은 경고 생성일로부터 1년입니다.
   * **다음의 경우에 경고 보내기**:

      * 다음 지표 중 하나 이상의 트리거
서버 호출 수/초 유형을 지표로 추가하고, 수정자 및 임계값을 선택하여 경고 임계값을 지정합니다.
         * 위 또는 같음
         * 아래 또는 같음
      * 포함
소비된 사용 기간에 대한 임계값 및 조건(다음 이상 또는 다음 이하)을 지정합니다.

1. 클릭 **[!UICONTROL Save]**.

## 서버 호출 사용량 경고 관리 {#section_8FF98170763C4B5CBEC6DD43F893177A}

![](assets/alert_mgmt.png)

경고를 관리하려면 다음을 수행하십시오.

1. 한 개 이상의 경고 옆에 있는 확인란을 선택합니다. 경고 관리 작업 맨 위에 표시됩니다.
1. 다음 작업을 한 개 이상 완료합니다.

   | 작업 | 정의 |
   |--- |--- |
   | + 추가 | Access the [Alert Builder](/help/admin/c-server-call-usage/scu-alerts.md) by clicking  [!UICONTROL + Add]. |
   | 태그 | 경고를 쉽게 사용할 수 있도록 구성하기 위해 태그를 지정합니다. |
   | 삭제 | 기본 경고를 제외한 모든 경고를 삭제할 수 있습니다. |
   | 이름 변경 | 기본 경고를 제외한 모든 경고의 이름을 바꿀 수 있습니다. |
   | 승인 | 경고를 승인하여 &quot;공식적&quot;으로 만듭니다. |
   | 활성화/비활성화 | 기본 경고를 포함하여 모든 경고를 활성화하거나 비활성화할 수 있습니다. |
   | 갱신 | 한 개 이상의 경고를 선택한 경우 갱신할 수 있습니다. This extends their expiration dates to be 1 year from the day [!UICONTROL Renew] was clicked, regardless of their original expiration date. |
   | CSV로 내보내기 | [사용량 보고서 다운로드](/help/admin/c-server-call-usage/report-suite-usage.md)를 참조하십시오. |

