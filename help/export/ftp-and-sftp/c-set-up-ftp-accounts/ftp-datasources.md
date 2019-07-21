---
description: Analytics를 사용하면 FTP 파일 전송을 이용하여 오프라인 데이터나 기록 데이터를 Experience Cloud로 가져오는 FTP 기반 Data Sources를 만들고 관리할 수 있습니다.
keywords: ftp; Sftp
seo-description: Analytics를 사용하면 FTP 파일 전송을 이용하여 오프라인 데이터나 기록 데이터를 Experience Cloud로 가져오는 FTP 기반 Data Sources를 만들고 관리할 수 있습니다.
seo-title: 데이터 소스
solution: Analytics
title: 데이터 소스
uuid: 41 BA 2 DE 7-D 33 D -4394-B 7 D 8-04 A 116 F 45419
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 데이터 소스

Analytics를 사용하면 FTP 파일 전송을 이용하여 오프라인 데이터나 기록 데이터를 Experience Cloud로 가져오는 FTP 기반 Data Sources를 만들고 관리할 수 있습니다.

Data Sources 인스턴스가 생성되면 도구에서는 Data Sources 파일 업로드에 사용할 수 있는 FTP 위치를 제공합니다. 업로드되면 Data Sources는 자동으로 이를 찾아서 처리합니다. 파일이 처리되면, Analytics 보고에 데이터를 사용할 수 있게 됩니다.

Data Sources 관리자의 [!UICONTROL 만들기] 탭을 사용하여 선택한 보고서 세트에 대한 새 Data Sources 인스턴스를 구성할 수 있습니다. [!UICONTROL Data Sources 마법사]에서 안내하는 Data Sources 템플릿 생성 프로세스에 따라 데이터를 업로드할 FTP 위치를 만듭니다.

[!UICONTROL Data Sources 관리] 창에서 데이터 소스를 찾고 FTP 정보 링크를 선택합니다. FTP 로그인 정보가 [!UICONTROL 업로드/FTP 정보] 섹션의 [!UICONTROL 데이터 소스 활성화] 창에 표시됩니다.

FTP 제한 및 데이터 유지에 대한 자세한 내용은 [FTP 제한 및 데이터 유지](../../../export/ftp-and-sftp/ftp-limits.md#concept_8CAA1D8F27B3411AB902520AD6C9A70E)를 참조하십시오.

## 분류 및 Data Sources에 대한 .fin 파일 업로드 정보 {#section_1484719F8A134EAE91212DBD8F15174F}

When you upload a classifications or [!UICONTROL Data Source] file ( [!DNL .tab] or [!DNL .txt]) the upload also requires that you upload an empty file with the exact same name as the data file being imported, but with a [!DNL .fin] extension. This [!DNL .fin] file is a finish file. 이 파일의 목적은 시스템에 데이터 파일이 FTP 계정에 완전히 업로드되었다는 것을 알리는 것입니다. The [!DNL .fin] file lets Adobe recognize that you are done with your import. 이 파일을 제출하면 Adobe가 두 파일을 FTP에서 제거하고 가져오기를 시작합니다.
파일 가져오기: [!DNL Classifications.tab]

Finish File: [!DNL Classifications.fin]

If you upload your Data Sources or SAINT file without an accompanying [!DNL .fin] file, Adobe does not add it to the queue for processing. The file remains on the FTP, and is not applied to your data in the [!UICONTROL Experience Cloud]. 이에 대한 알림은 이메일 주소를 보고하는 [!UICONTROL FTP 계정 만들기] 창에서 [!UICONTROL 알림 수신자]로 입력한 경우에만 받습니다. 이 필드에 이메일 주소를 입력하지 않은 경우 알림이 전송되지 않습니다.

If you do upload your file with a [!DNL .fin] file, but there is an error in the file, it is submitted for processing, but the error causes the processing to cease and the file to be sent to an error folder. 이 경우 알림이 [!UICONTROL FTP 계정 만들기] 창의 [!UICONTROL 알림 수신자] 필드에 나열된 이메일 주소로 전송됩니다. 이메일 주소를 입력하지 않은 경우 알림이 전송되지 않습니다.
