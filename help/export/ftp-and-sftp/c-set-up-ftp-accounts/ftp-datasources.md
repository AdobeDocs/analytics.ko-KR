---
description: Analytics를 사용하면 FTP 파일 전송을 이용하여 오프라인 데이터나 기록 데이터를 Experience Cloud로 가져오는 FTP 기반 데이터 소스를 만들고 관리할 수 있습니다.
keywords: ftp, sftp
title: 데이터 소스
uuid: 41ba2de7-d33d-4394-b7d8-04a116f45419
exl-id: 777917bd-bd11-4360-a149-e4fd0bb2f99e
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '450'
ht-degree: 100%

---

# 데이터 소스

Analytics를 사용하면 FTP 파일 전송을 이용하여 오프라인 데이터나 기록 데이터를 Experience Cloud로 가져오는 FTP 기반 데이터 소스를 만들고 관리할 수 있습니다.

Data Sources 인스턴스가 생성되면 도구에서는 Data Sources 파일 업로드에 사용할 수 있는 FTP 위치를 제공합니다. 업로드되면 Data Sources는 자동으로 이를 찾아서 처리합니다. 파일이 처리되면, Analytics 보고에 데이터를 사용할 수 있게 됩니다.

Data Sources 관리자의 [!UICONTROL 만들기] 탭을 사용하여 선택한 보고서 세트에 대한 새 Data Sources 인스턴스를 구성할 수 있습니다. [!UICONTROL Data Sources 마법사]에서 안내하는 Data Sources 템플릿 생성 프로세스에 따라 데이터를 업로드할 FTP 위치를 만듭니다.

[!UICONTROL Data Sources 관리] 창에서 데이터 소스를 찾고 FTP 정보 링크를 선택합니다. FTP 로그인 정보가 [!UICONTROL 업로드/FTP 정보] 섹션의 [!UICONTROL 데이터 소스 활성화] 창에 표시됩니다.

FTP 제한 및 데이터 유지에 대한 자세한 내용은 [FTP 제한 및 데이터 유지](/help/export/ftp-and-sftp/ftp-limits.md)를 참조하십시오.

## 분류 및 데이터 소스에 대한 .fin 파일 업로드 정보 {#section_1484719F8A134EAE91212DBD8F15174F}

분류 또는 [!UICONTROL 데이터 소스] 파일 ([!DNL .tab] 또는 [!DNL .txt])을 업로드할 때 가져오는 데이터 파일과 이름이 같지만 확장명이 [!DNL .fin]인 빈 파일도 업로드해야 합니다. 이 [!DNL .fin] 파일은 완료한 파일입니다. 이 파일의 목적은 시스템에 데이터 파일이 FTP 계정에 완전히 업로드되었음을 알리는 것입니다. [!DNL .fin] 파일을 사용하면 사용자가 가져오기를 완료했음을 Adobe에서 인식할 수 있습니다. 이 파일을 제출하면 Adobe가 두 파일을 FTP에서 제거하고 가져오기를 시작합니다.
파일 가져오기: [!DNL Classifications.tab]

완료 파일: [!DNL Classifications.fin]

[!DNL .fin] 파일 없이 데이터 소스 또는 SAINT 파일을 업로드하면 Adobe가 처리를 위해 해당 파일을 큐에 추가하지 않습니다. 이 파일은 FTP에 남아 있으며 [!UICONTROL Experience Cloud]의 데이터에 적용되지 않습니다. 이에 대한 알림은 이메일 주소를 보고하는 [!UICONTROL FTP 계정 만들기] 창에서 [!UICONTROL 알림 수신자]로 입력한 경우에만 받습니다. 이 필드에 이메일 주소를 입력하지 않은 경우 알림이 전송되지 않습니다.

이 파일을 [!DNL .fin] 파일과 함께 업로드하면 파일에 오류가 있는 경우 처리를 위해 제출되지만 오류로 인해 처리가 중지되고 파일이 오류 폴더로 전송됩니다. 이 경우 알림이 [!UICONTROL FTP 계정 만들기] 창의 [!UICONTROL 알림 수신자] 필드에 나열된 이메일 주소로 전송됩니다. 이메일 주소를 입력하지 않은 경우 알림이 전송되지 않습니다.
