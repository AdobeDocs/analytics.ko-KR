---
description: Analysis Workspace 프로젝트를 직접 또는 이메일 게재 일정에 따라 보내는 방법을 알아봅니다.
keywords: Analysis Workspace
title: 프로젝트 보내기 및 예약
feature: Curate and Share
role: User, Admin
exl-id: 2d6854f7-8954-4d55-b2be-25981cfb348b
source-git-commit: e478da9ae80e5534fcfd77ced3864d7f31ef748d
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 28%

---

# 프로젝트 보내기 및 예약

Adobe Analytics 프로젝트를 선택한 사용자에게 이메일로 파일로 보낼 수 있습니다. 파일을 애드혹으로 보낼 수도 있고, 일정에 따라 파일을 보내도록 구성할 수도 있습니다. 파일은 CSV 또는 PDF 형식으로 보낼 수 있습니다.

프로젝트에 적용된 모든 태그는 자동으로 내보내기에 적용됩니다.

[내보내기 개요](/help/export/home.md)에 설명된 대로 Adobe Analytics 데이터를 내보내는 다른 방법도 사용할 수 있습니다.

![파일 보내기](assets/send-file.png)

## 파일 보내기

파일을 임시로 수신자에게 전자 메일로 보내려면 다음을 수행합니다.

1. **[!UICONTROL 공유] > [!UICONTROL 파일 보내기]**&#x200B;를 선택합니다.
1. 파일 유형을 지정합니다.
   * [!UICONTROL **CSV**]: 일반 텍스트 데이터를 원하는 경우 이 옵션을 선택합니다.
   * [!UICONTROL **PDF**]: 다운로드한 파일에 프로젝트에 표시된(표시되는) 테이블과 시각화가 모두 포함되도록 하려면 이 옵션을 선택합니다.
1. (선택 사항) 전자 메일에 포함할 설명을 추가하려면 **[!UICONTROL 설명]**&#x200B;을 사용합니다.
1. 수신자 또는 그룹을 추가합니다. 이메일 주소를 입력할 수도 있습니다.
1. (선택 사항) **[!UICONTROL 예약 옵션 표시]**&#x200B;를 선택하여 [파일 내보내기 예약](#schedule-file-export)을 선택합니다.
1. **[!UICONTROL 지금 보내기]**&#x200B;를 클릭합니다. 취소하려면 **[!UICONTROL 취소]**&#x200B;를 선택합니다.


## 파일 내보내기 예약 {#schedule}

이메일로 수신자에게 일정에 따라 파일을 보내려면

1. **[!UICONTROL 공유] > [!UICONTROL 파일 내보내기 예약]**&#x200B;을 선택합니다.
1. 파일 유형을 지정합니다.
   * [!UICONTROL **CSV**]: 일반 텍스트 데이터를 원하는 경우 이 옵션을 선택합니다.
   * [!UICONTROL **PDF**]: 다운로드한 파일에 프로젝트에 표시된(표시되는) 테이블과 시각화가 모두 포함되도록 하려면 이 옵션을 선택합니다.
1. (선택 사항) 전자 메일에 포함할 설명을 추가하려면 **[!UICONTROL 설명]**&#x200B;을 사용합니다.
1. 수신자 또는 그룹을 추가합니다. 이메일 주소를 입력할 수도 있습니다.
1. (Healthcare Shield 고객만 해당) [예약된 보고서를 암호로 보호](#password-protect-a-new-scheduled-project)하려면 암호를 제공하세요.
1. **[!UICONTROL 예약 옵션 표시]**&#x200B;를 선택했는지 확인하십시오.
1. **[!UICONTROL 빈도]**&#x200B;를 선택하십시오. 다음 중 하나를 선택할 수 있습니다.

   | 빈도 | 옵션 |
   |---|---|
   | **[!UICONTROL 시간별 전송]** | **[!UICONTROL 시간 단위로 보내기]**&#x200B;에 대한 값을 입력하십시오. |
   | **[!UICONTROL 매일 보내기]** | **[!UICONTROL 일별 빈도]**&#x200B;를 선택하십시오. **[!UICONTROL 매일 보내기]**, **[!UICONTROL 평일마다 보내기]** 또는 **[!UICONTROL 사용자 지정 빈도]**.<br/>**[!UICONTROL 사용자 지정 빈도]**&#x200B;를 선택한 경우 **[!UICONTROL 일마다 보내기]**&#x200B;에 대한 값을 입력하십시오. |
   | **[!UICONTROL 주별 보내기]** | **[!UICONTROL 주마다 보내기]**&#x200B;에 대한 값을 입력하십시오. **[!UICONTROL 요일]**&#x200B;을 선택하세요. |
   | **[!UICONTROL 요일별로 월별 전송]** | **[!UICONTROL 요일]**&#x200B;과 **[!UICONTROL 월 주]**&#x200B;을(를) 선택하십시오. |
   | **[!UICONTROL 월별 전송(날짜 기준)]** | **[!UICONTROL 이 달의 날짜에 보내기]**&#x200B;에서 값을 선택하십시오. |
   | **[!UICONTROL 매년 해당 월의 날짜별로 보내기]** | **[!UICONTROL 요일]**&#x200B;을 선택하고 **[!UICONTROL 주]**&#x200B;을 선택한 다음 **[!UICONTROL 월별]**&#x200B;을(를) 선택합니다. |
   | **[!UICONTROL 특정 날짜까지 연간 전송]** | **[!UICONTROL 월(한 해 기준)]**&#x200B;을 선택하고 **[!UICONTROL 이 날짜에 보내기]**&#x200B;에서 값을 선택합니다. |

1. **[!UICONTROL 시작 날짜]**&#x200B;에 시작 날짜를 입력하십시오. 또는 ![달력](/help/assets/icons/Calendar.svg)을 선택하여 달력에서 시작 날짜를 선택하십시오.

1. 종료 날짜를 **[!UICONTROL 종료 날짜]**&#x200B;로 입력하십시오. 또는 ![캘린더](/help/assets/icons/Calendar.svg)를 선택하여 달력에서 종료 날짜를 선택하십시오.
1. **[!UICONTROL 일정에 따라 보내기]**&#x200B;를 선택합니다. 취소하려면 **[!UICONTROL 취소]**&#x200B;를 선택합니다.


## 예약된 프로젝트 관리자 {#manager}

예약된 Analysis Workspace 프로젝트는 **[!UICONTROL 구성 요소]** > **[!UICONTROL 예약된 프로젝트]**&#x200B;를 사용하여 기본 인터페이스에서 관리할 수 있습니다. 자세한 내용은 [예약된 프로젝트](/help/components/scheduled-projects-manager.md)를 참조하십시오.

<!--
# Schedule projects

From the Workspace **Share menu**, you can send Analysis Workspace projects using email to selected recipients. Files can be sent in CSV or PDF format. After you share scheduled projects, you can edit the schedule settings to modify the frequency, receipient list, or file type using the Scheduled Projects manager.

## Send file now

To send a file immediately to recipients via email:

1. Click **[!UICONTROL Share] > [!UICONTROL Export file]**.
1. Specify the file type:
   * [!UICONTROL **CSV**]: Choose this option if you want plain-text data.
   * [!UICONTROL **PDF**]: Choose this option if you want the downloaded file to contain all the displayed (visible) tables and visualizations in the project.
1. (Optional) Add a description to include in the email to explain the file being received. 
1. Add recipients or groups. Email addresses can also be entered. 
1. Click **[!UICONTROL Send Now]**.
1. (Optional) Click **[!UICONTROL Show scheduling options]** to specify a delivery schedule.

![Send file now](assets/send-file-now.png)

## Send file on schedule

To send a file on a recurring schedule to recipients via email:

1. Click **[!UICONTROL Share] > [!UICONTROL Schedule file export]**.
1. Specify the file type (CSV or PDF).
1. (Optional) Add a description that will be included in the email to explain the file being received. 
1. Add recipients or groups. Email addresses can also be entered. 
1. Specify the range the schedule should be delivered over by modifying Starting on and Ending on inputs. The end date must be within a year from the day the schedule is created or modified.
1. Specify the delivery frequency. Each frequency allows for different customizations. 
1. Click **[!UICONTROL Send on schedule]**.

![](assets/send-on-schedule.png)

## Manage scheduled projects

When you manage scheduled projects, you can edit and delete recurring project schedules:

*  Change the file type (.csv or PDF)
*  Update the project description
*  Add or remove recipients
*  Change the frequency


Scheduled Analysis Workspace projects can be managed under **Analytics > Components > Scheduled Projects**.

For more information, see [Scheduled projects](/help/components/scheduled-projects-manager.md)
-->
