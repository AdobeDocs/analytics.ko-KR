---
description: 데이터 소스 파일을 업로드하는 방법을 설명하는 절차입니다.
seo-description: 데이터 소스 파일을 업로드하는 방법을 설명하는 절차입니다.
seo-title: Data Sources 파일 업로드
solution: Analytics
subtopic: 데이터 소스
title: Data Sources 파일 업로드
topic: 개발자 및 구현
uuid: 5a9dde91-1297-47e5-9393-611b40413c17
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Data Sources 파일 업로드

데이터 소스 파일을 업로드하는 방법을 설명하는 절차입니다.

데이터 소스 데이터 파일을 준비한 후에는 처리를 위해 데이터 소스로 전송합니다. Adobe는 데이터 소스 파일을 업로드할 수 있도록 다수의 데이터 소스 FTP 서버를 운영합니다. 데이터 소스 FTP 서버에 관해 다음에 유의하십시오.

* Select FTP Info next to the Data Source entry in the [!UICONTROL Data Sources Manage] tab to see the FTP Host, Login, and Password information for the data source's FTP account. 이 정보에 액세스할 수 있는 사람이라면 누구나 데이터를 보고서 세트에 업로드할 수 있습니다.
* 보안상의 이유로 FTP 계정은 30일간 활동이 없는 경우 폐쇄됩니다.
* FTP 계정은 데이터 소스별로 특정합니다. FTP 계정 하나로 여러 데이터 소스에 데이터 소스 파일을 업로드할 수 없습니다.

**데이터 소스 파일을 업로드하려면**

1. FTP 클라이언트를 사용하여 데이터를 데이터 소스 FTP 사이트에 보냅니다.

   (데이터 소스 관리자의 FTP 정보 링크를 사용할 수 있습니다.)

1. Upload a [!DNL .fin] file to notify Adobe that the Data Sources file upload is complete.

   The [!DNL .fin] file must have the exact same name as the Data Sources file, except for the file extension. Adobe does not queue the Data Sources file for processing until you upload the [!DNL .fin] file.

   데이터 소스 파일이 업로드를 마치기 전까지는 파일을 업로드하지 마십시오. 그렇지 않으면, 데이터 소스가 불완전한 파일을 처리할 수 있습니다.
1. 데이터 소스 파일이 처리되는 동안 나타나는 메시지를 확인하십시오.

   데이터 소스 관리자는 파일 처리 중에 발생하는 모든 오류를 표시합니다.

