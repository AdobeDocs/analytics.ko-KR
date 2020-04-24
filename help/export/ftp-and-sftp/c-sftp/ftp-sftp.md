---
description: SFTP는 본인을 제외한 누구도 본인의 데이터를 볼 수 없도록 전송 중인 데이터를 보호하는 프로토콜입니다. Adobe 엔지니어링 서비스에서 데이터를 안전하게 유지하도록 SFTP 계정을 설정할 수 있습니다.
keywords: ftp;sftp
title: Secure File Transfer Protocol - 개요
uuid: 7dd1a867-e828-4c7b-bf11-75a81d4c149c
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Secure File Transfer Protocol - 개요

SFTP는 본인을 제외한 누구도 본인의 데이터를 볼 수 없도록 전송 중인 데이터를 보호하는 프로토콜입니다. Adobe 엔지니어링 서비스에서 데이터를 안전하게 유지하도록 SFTP 계정을 설정할 수 있습니다.

## 배달 푸시 {#section_A47831BB1DCA490BB57F0940617AA506}

이는 Adobe 서버에서 사용자 서버로 파일을 &quot;푸시&quot;하는 것을 의미합니다. 기본적으로 Adobe에서 사용자의 끝 포인트에 배달합니다.

[Data Warehouse](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-dw.md) 및 [Analytics 데이터 피드](https://marketing.adobe.com/resources/help/en_US/reference/analytics-data-feed.html)는 SFTP를 통해 데이터를 푸시할 수 있습니다.

SFTP를 통해 데이터를 푸시할 수 **없는** Analytics 도구는 다음과 같습니다.

* Reports &amp; Analytics
* Ad Hoc Analysis
* Report Builder

## 배달 가져오기 {#section_FA29FAEF02FE40B8B32452146A036F48}

이는 일반 FTP를 사용하는 Adobe 서버 중 하나로 파일을 보내는 것을 의미합니다. 서버에 있는 파일이 필요한 경우 자신의 서버에서 SFTP를 사용하여 Adobe의 FTP 서버로 Adobe의 서버를 가져와야 합니다. 다음 세 가지 방법 중 하나를 사용하여 이 작업을 수행할 수 있습니다.

* [SFTP를 통해 암호 없이 Adobe에 연결합니다.](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md)
* [SFTP를 통해 Adobe FTP 계정에 연결합니다.](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-connect.md)
* 원하는 보고서를 Adobe의 FTP와 유사한 데이터 피드/R&amp;A/Ad Hoc 등에 푸시한 다음 가져옵니다. Adobe는 이러한 보고서를 사용자가 설정한 SFTP 서버에 전달할 수 없습니다.

