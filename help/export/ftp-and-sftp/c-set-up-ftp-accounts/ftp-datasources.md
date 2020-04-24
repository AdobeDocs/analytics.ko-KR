---
description: Analytics를 사용하면 FTP 파일 전송을 이용하여 오프라인 데이터나 기록 데이터를 Experience Cloud로 가져오는 FTP 기반 데이터 소스를 만들고 관리할 수 있습니다.
keywords: ftp;sftp
title: 데이터 소스
uuid: 41ba2de7-d33d-4394-b7d8-04a116f45419
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# 데이터 소스

Analytics를 사용하면 FTP 파일 전송을 이용하여 오프라인 데이터나 기록 데이터를 Experience Cloud로 가져오는 FTP 기반 데이터 소스를 만들고 관리할 수 있습니다.

Data Sources 인스턴스가 생성되면 도구에서는 Data Sources 파일 업로드에 사용할 수 있는 FTP 위치를 제공합니다. 업로드되면 Data Sources는 자동으로 이를 찾아서 처리합니다. 파일이 처리되면, Analytics 보고에 데이터를 사용할 수 있게 됩니다.

The [!UICONTROL Create] tab in the Data Sources Manager lets you configure a new Data Sources instance for the selected report suite. The [!UICONTROL Data Sources Wizard] guides you through the process of creating a Data Sources template, and creates an FTP location for uploading data.

In the [!UICONTROL Manage Data Sources] window, find your data source and select the FTP Info link. FTP 로그인 정보는 [!UICONTROL Activate a Data Source] 섹션의 [!UICONTROL Upload/FTP Information] 창에 표시됩니다.

FTP 제한 및 데이터 보존에 대한 자세한 내용은 FTP 제한 [및 데이터 유지를 참조하십시오](/help/export/ftp-and-sftp/ftp-limits.md).

## 분류 및 데이터 소스에 대한 .fin 파일 업로드 정보 {#section_1484719F8A134EAE91212DBD8F15174F}

When you upload a classifications or [!UICONTROL Data Source] file ( [!DNL .tab] or [!DNL .txt]) the upload also requires that you upload an empty file with the exact same name as the data file being imported, but with a [!DNL .fin] extension. 이 [!DNL .fin] 파일은 완료한 파일입니다. 이 파일의 목적은 시스템에 데이터 파일이 FTP 계정에 완전히 업로드되었음을 알리는 것입니다. [!DNL .fin] 파일을 사용하면 사용자가 가져오기를 완료했음을 Adobe에서 인식할 수 있습니다. 이 파일을 제출하면 Adobe가 두 파일을 FTP에서 제거하고 가져오기를 시작합니다.
파일 가져오기: [!DNL Classifications.tab]

완료 파일: [!DNL Classifications.fin]

[!DNL .fin] 파일 없이 데이터 소스 또는 SAINT 파일을 업로드하면 Adobe가 처리를 위해 해당 파일을 큐에 추가하지 않습니다. 이 파일은 FTP에 남아 있으며 [!UICONTROL Experience Cloud]의 데이터에 적용되지 않습니다. You are notified of this only if you have entered your email address as the [!UICONTROL Notification Recipient] in the [!UICONTROL Create FTP Account] window of reporting. 이 필드에 이메일 주소를 입력하지 않은 경우 알림이 전송되지 않습니다.

이 파일을 [!DNL .fin] 파일과 함께 업로드하면 파일에 오류가 있는 경우 처리를 위해 제출되지만 오류로 인해 처리가 중지되고 파일이 오류 폴더로 전송됩니다. If this occurs, a notification is sent to the email address listed in the [!UICONTROL Notification Recipient] field in the [!UICONTROL Create FTP Account] window. 이메일 주소를 입력하지 않은 경우 알림이 전송되지 않습니다.
