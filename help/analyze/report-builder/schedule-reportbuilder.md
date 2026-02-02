---
title: Report Builder을 사용하여 통합 문서 예약
description: Report Builder에서 예약 기능을 사용하는 방법을 알아봅니다.
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: 40e1feb0-64bc-40e6-83cb-4a1ea7e2d0cc
source-git-commit: 8b6d8a4efec59b693a69984880d8f374ae0cfabc
workflow-type: tm+mt
source-wordcount: '903'
ht-degree: 26%

---

# 이메일을 통해 공유하여 통합 문서 예약

>[!NOTE]
>
>[클라우드 대상으로 내보낼 통합 문서 예약](/help/analyze/report-builder/report-builder-export.md)에 설명된 대로 전자 메일을 통해 공유할 통합 문서를 예약하는 것 외에도 클라우드 대상으로 내보낼 통합 문서를 예약할 수 있습니다.

통합 문서를 저장하고 분석을 완료한 후에 예약 기능을 사용하여 팀의 다른 구성원들과 통합 문서를 쉽게 공유할 수 있습니다. 예약 기능을 사용하여 통합 문서의 데이터를 자동으로 새로 고치고 특정 날짜 및 시간에 Excel 통합 문서 .xlsx 파일을 지정된 대상자에게 이메일 첨부 파일로 보내는 일정을 만들 수 있습니다. 예약을 설정하면 정기 업데이트가 자동으로 수신자에게 제공됩니다. 예약 기능을 사용하여 자동 업데이트를 예약하지 않고도 통합 문서를 한 번에 전송할 수도 있습니다.

단일 통합 문서에 여러 일정을 만들 수 있습니다. 예를 들어 일별로 통합 문서를 팀에 전송하고 두 개의 다른 일정을 만들어 일주일에 한 번 통합 문서를 관리자에게 보낼 수 있습니다.

예약 기능을 사용하여 통합 문서에 대한 암호 보호를 설정하고 이전에 예약한 통합 문서를 편집할 수도 있습니다.


>[!BEGINSHADEBOX]

데모 비디오는 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [통합 문서 예약](https://video.tv.adobe.com/v/3413079?quality=12&learn=on){target="_blank"}을 참조하세요.

>[!ENDSHADEBOX]


## 통합 문서 예약

워크북을 예약하려면

1. 통합 문서 Excel 파일(.xlsx)을 개인 또는 그룹에 자동으로 배포할 수 있도록 일정을 만들려면 Report Builder 허브에서 **[!UICONTROL 일정]**&#x200B;을 선택하세요.

   ![일정을 만들려면 [일정] 단추를 선택하십시오.](./assets/schedule.png){zoomable="yes"}

1. 새 예약된 통합 문서를 만들려면 **[!UICONTROL 통합 문서 예약]** 또는 ![추가](/help/assets/icons/Add.svg)를 선택하십시오.

   ![통합 문서 예약 창](./assets/schedule-workbook.png){zoomable="yes"}

   예약 창에는 통합 문서 이름과 통합 문서를 마지막으로 수정한 날짜 등 통합 문서에 대한 사전 정의된 일부 정보가 표시됩니다.

### 파일

**[!UICONTROL 파일]** 섹션에서 파일 형식, 이름 및 암호를 자세히 입력하여 파일을 보호합니다.

![일정 창.](./assets/schedule-pane.png){zoomable="yes"}

1. 아직 선택하지 않은 경우 ![TableSelect](/help/assets/icons/TableSelect.svg)을(를) 사용하여 현재 통합 문서를 선택하십시오.

1. (선택 사항) **[!UICONTROL 파일 이름]**&#x200B;을 입력합니다.

   통합 문서 파일 이름은 기본적으로 통합 문서의 이름으로 설정되지만 원하는 경우 파일 이름을 변경할 수 있습니다.

1. **[!UICONTROL 파일 형식]**&#x200B;을(를) 선택하십시오.

   * **[!UICONTROL Excel]**
   * **[!UICONTROL PDF]**
   * **[!UICONTROL CSV]**

   **[!UICONTROL CSV]**&#x200B;을(를) 선택하면 예약된 통합 문서가 zip 첨부 파일로 전송됩니다. 일부 회사 이메일 관리자는 zip 첨부 파일이 있는 이메일을 차단할 수 있습니다. 그에 따라 경고가 표시됩니다.

1. (선택 사항) **[!UICONTROL 파일 이름에 타임스탬프 추가]**&#x200B;를 선택합니다.

   타임스탬프를 파일 이름에 추가하여 통합 문서가 업데이트된 날짜를 식별할 수 있습니다. 타임스탬프는 특정 날짜에 전송된 통합 문서의 버전을 확인하는 데 유용합니다. 선택하면 다음 중 하나를 선택할 수 있습니다.

   * **[!UICONTROL ISO 날짜 형식]**&#x200B;입니다. 이 경우 `YYYY-MM-DD`이(가) 파일 이름에 추가됩니다.
   * **[!UICONTROL ISO 날짜 형식 + 타임스탬프]**&#x200B;입니다. 그러면 `YYYY-MM-DD_HH-MM-SS`이(가) 파일 이름에 추가됩니다.

<!-- Does no longer seem to be an option? 
1. (Optional) Select **.zip compression** to compress the file and set up password protection on the file.

    When you make this selection, you're prompted to enter a password to open the file. This is helpful if you have concerns about data security and you want to password protect the workbook. Protecting the file with a password requires you to select **.zip compression**. The password must be at least 8 characters and contain a number and a special character.

    ![Enter a password in the Password protect the workbook field.](./assets/zip-compression.png){zoomable="yes"}{width="55%"}
-->

1. **[!UICONTROL 통합 문서 암호 보호]**&#x200B;에 암호를 입력하십시오. 유효한 암호에는 8자 이상, 숫자 및 특수 문자가 필요합니다. 암호를 표시하려면 ![VisibilityOff](/help/assets/icons/VisibilityOff.svg)를 선택하고 암호를 숨기려면 ![Visibility](/help/assets/icons/Visibility.svg)을 선택합니다(기본값).


### 이메일

**[!UICONTROL 전자 메일]** 섹션에서 전자 메일의 수신자, 제목 및 설명을 제공합니다.

![전자 메일 설정 예약](assets/schedule-email.png){zoomable="yes"}

1. **수신자**&#x200B;를 입력합니다. 조직에서 인식하는 사람의 이름을 입력할 수 있습니다. 또는 조직 외부에 있는 사람의 이메일 주소를 입력할 수 있습니다.

1. 이메일의 **제목** 및 수신자에 대한 설명을 입력합니다. 제목에 통합 문서 파일 이름이 기본적으로 표시되지만 필요한 경우 제목을 수정할 수 있습니다. 설명 섹션의 세부 정보를 추가할 수 있습니다.

1. **[!UICONTROL 설명]** 텍스트 영역에 설명을 선택적으로 입력할 수 있습니다.


### 예약

**[!UICONTROL 일정]** 섹션에서 통합 문서가 포함된 전자 메일을 받는 사람에게 보내는 일정을 정의할 수 있습니다.

![일정 정의](assets/schedule-enable.png){zoomable="yes"}

1. **[!UICONTROL 예약 옵션 표시]**&#x200B;를 선택하여 일정을 정의합니다.

1. **[!UICONTROL 시작 날짜]**&#x200B;에 시작 날짜를 입력하십시오. 또는 ![달력](/help/assets/icons/Calendar.svg)을 선택하여 달력에서 시작 날짜를 선택하십시오.

1. 종료 날짜를 **[!UICONTROL 종료 날짜]**&#x200B;로 입력하십시오. 또는 ![캘린더](/help/assets/icons/Calendar.svg)를 선택하여 달력에서 종료 날짜를 선택하십시오.

1. **[!UICONTROL 빈도]**&#x200B;를 선택하십시오. 선택한 빈도에 따라 추가 옵션이 있습니다. 아래 표를 참조하십시오.

   | 빈도 | 옵션 |
   |---|---|
   | **[!UICONTROL 시간별 전송]** | **[!UICONTROL 시간 단위로 보내기]**&#x200B;에 대한 값을 입력하십시오. |
   | **[!UICONTROL 매일 보내기]** | **[!UICONTROL 일별 빈도]**&#x200B;를 선택하십시오. **[!UICONTROL 매일 보내기]**, **[!UICONTROL 평일마다 보내기]** 또는 **[!UICONTROL 사용자 지정 빈도]**.<br/>**[!UICONTROL 사용자 지정 빈도]**&#x200B;를 선택한 경우 **[!UICONTROL 일마다 보내기]**&#x200B;에 대한 값을 입력하십시오. |
   | **[!UICONTROL 주별 보내기]** | **[!UICONTROL 주마다 보내기]**&#x200B;에 대한 값을 입력하십시오. **[!UICONTROL 요일]**&#x200B;을 선택하세요. |
   | **[!UICONTROL 요일별로 월별 전송]** | **[!UICONTROL 요일]**&#x200B;과 **[!UICONTROL 월 주]**&#x200B;을(를) 선택하십시오. |
   | **[!UICONTROL 월별 전송(날짜 기준)]** | **[!UICONTROL 이 달의 날짜에 보내기]**&#x200B;에서 값을 선택하십시오. |
   | **[!UICONTROL 매년 해당 월의 날짜별로 보내기]** | **[!UICONTROL 요일]**&#x200B;을 선택하고 **[!UICONTROL 주]**&#x200B;을 선택한 다음 **[!UICONTROL 월별]**&#x200B;을(를) 선택합니다. |
   | **[!UICONTROL 특정 날짜까지 연간 전송]** | **[!UICONTROL 월(한 해 기준)]**&#x200B;을 선택하고 **[!UICONTROL 이 날짜에 보내기]**&#x200B;에서 값을 선택합니다. |

### 보내기

통합 문서를 보내려면:

* **[!UICONTROL 예약 옵션 표시]**&#x200B;를 사용하여 일정을 정의하지 않은 경우 **[!UICONTROL 지금 보내기]**&#x200B;를 선택하여 전자 메일로 통합 문서를 즉시 보냅니다.
* **[!UICONTROL 예약 옵션 표시]**&#x200B;를 사용하여 일정을 정의한 경우 **[!UICONTROL 일정에 따라 보내기]**&#x200B;를 선택하여 정의한 일정을 사용하여 전자 메일로 통합 문서를 보냅니다.

두 경우 모두 Report Builder 허브 하단에 확인 알림이 표시됩니다.

통합 문서 전송을 취소하려면 **[!UICONTROL 취소]**&#x200B;를 선택하십시오.

## 예약된 통합 문서 관리

이미 예약된 통합 문서 관리에 대한 자세한 내용은 [예약된 통합 문서 관리](/help/analyze/report-builder/manage-reportbuilder.md)를 참조하십시오.




<!--

## Schedule a workbook

Use the Schedule button in the Report Builder hub to quickly create a schedule so that you can automatically distribute a workbook Excel file (.xlsx) to an individual or a group.

1. Click the Schedule button in the Report Builder hub.

    ![Click the Schedule button to create a schedule.](./assets/schedule-button.png){width="55%"}

1. Click Schedule Workbook or the plus button in the upper-left to create a new scheduled workbook.

    ![The Schedule workbooks window.](./assets/schedule-workbook.png){width="55%"}

    The scheduling pane displays some pre-defined information about the workbook such as the workbook name and the last date that the workbook was modified.

    ![The scheduling pane.](./assets/schedule-pane.png){width="55%"}

1. (Optional) Enter a file name.

    The workbook file name defaults to the name of the workbook but you can change this if you want. If you\'re sending the same workbook to multiple audiences and you want to name it something a little bit more friendly for a certain audience, you can change the name.

1. (Optional) Select **Append time-stamp to file name**.

    You can append a timestamp to the file name to identify the date the workbook was updated. This is helpful to quickly see which version of a workbook was sent on a specific date. The **Filename preview** shows how the workbook file name will appear in the email when the workbook is distributed. The time-stamp format is YYYY-MM-DD.

1. (Optional) Select **.zip compression** to compress the file and set up password protection on the file.

    When you make this selection, you're prompted to enter a password to open the file. This is helpful if you have concerns about data security and you want to password protect the workbook. Protecting the file with a password requires you to select **.zip compression**. The password must be at least 8 characters and contain a number and a special character.

    ![Enter a password in the Password protect the workbook field.](./assets/zip-compression.png){width="55%"}

1. Enter **Recipients**. You can enter the name of a person that is recognized in your organization, or you can enter an email address of a person inside or outside of your organization.

1. Enter the **Subject** of the email and a description for your recipients. The subject defaults to the workbook file name but you can modify the subject if needed. You can add details in the description section.

    ![Enter a subject in the Subject field.](./assets/recipients-subject.png){width="55%"}

1. Set up the scheduling options to set the date and time that you want the workbook emailed to your recipients.

    Choose the start and end date and time frames. This can be today's date or a date in the future.

    Choose the **Frequency** from the drop-down menu. You can set the frequency to be hourly, daily, weekly, monthly, or yearly on a specific day. For example, you can set up a schedule to send the workbook on the first Sunday night of the month so that your recipients will have the email in their inbox first thing on Monday morning.

    ![Select the frequency to schedule your report.](./assets/frequency.png){width="55%"}

1. After you set the schedule, click **Send on schedule**.

    ![Click Send on schedule.](./assets/send-on-schedule.png){width="55%"}

    You see a confirmation toast at the bottom of the Report Builder hub and the scheduled workbook is listed under the Workbooks tab.

    ![Confirmation toast](./assets/confirmation-toast.png){width="55%"}

## Schedule a converted workbook {#converted}

1. Schedule a [converted](/help/analyze/report-builder/convert-workbooks.md) legacy workbook.

   A pop up appears, asking if you want to use the scheduling metada from the legacy workbook to create a new scheduled task. 

1. If you select **[!UICONTROL Use]**, Report Builder automatically fills in the legacy scheduling information. 

1. Ensure that this information is correct and schedule. 

1. If you want to send the workbook on a different schedule, schedule a completely fresh scheduled task. 


## Send the workbook one-time only

You can also send out the workbook only once.

1. Un-check **Show scheduling options** 

    ![Click Un-check Show scheduling options to send out a workbook one time.](./assets/send-now.png){width="40%"}

1. Click **Send Now**.

## Manage scheduled workbooks

For information about managing workbooks that are already scheduled, see [Manage scheduled workbooks](/help/analyze/report-builder/manage-schedules-reportbuilder.md).

-->