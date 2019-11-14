---
description: SFTP는 사용자 이외의 사용자가 데이터를 볼 수 없도록 데이터를 전송하기 위한 보안 프로토콜입니다. Adobe 엔지니어링 서비스는 데이터를 안전하게 유지하도록 SFTP 계정을 설정할 수 있습니다.
keywords: ftp;sftp
solution: Analytics
title: Secure File Transfer Protocol - 개요
uuid: 7dd1a867-e828-4c7b-bf11-75a81d4c149c
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Secure File Transfer Protocol - 개요

SFTP는 사용자 이외의 사용자가 데이터를 볼 수 없도록 데이터를 전송하기 위한 보안 프로토콜입니다. Adobe 엔지니어링 서비스는 데이터를 안전하게 유지하도록 SFTP 계정을 설정할 수 있습니다.

## 배달 푸시 {#section_A47831BB1DCA490BB57F0940617AA506}

이는 Adobe 서버에서 사용자 서버로 파일을 "푸시"하는 것을 의미합니다. 기본적으로 Adobe에서 사용자의 끝 포인트에 배달합니다.

[데이터 웨어하우스](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-dw.md) 및 [분석 데이터 피드는 SFTP를](https://marketing.adobe.com/resources/help/en_US/reference/analytics-data-feed.html) 통해 데이터를 푸시할 수 있습니다.

The following Analytics tools **cannot** push data via SFTP:

* Reports &amp; Analytics
* Ad Hoc Analysis
* Report Builder

## 배달 가져오기 {#section_FA29FAEF02FE40B8B32452146A036F48}

이는 일반 FTP를 사용하는 Adobe 서버 중 하나로 파일을 보내는 것을 의미합니다. 서버에서 파일을 가져오려면 서버에서 SFTP를 사용하여 Adobe의 FTP 서버로 파일을 가져와야 합니다. 다음 세 가지 방법 중 하나를 사용하여 이 작업을 수행할 수 있습니다.

* [SFTP를 통해 암호 없이 Adobe에 연결.](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md)
* [SFTP 파섹](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-connect.md)
* 원하는 보고서를 Adobe의 FTP와 유사한 데이터 피드/R&amp;A/애드혹 등에 푸시한 다음 가져옵니다. Adobe는 설정한 SFTP 서버에 이러한 보고서를 제공할 수 없습니다.

