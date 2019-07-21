---
description: Sftp는 아무도 데이터를 볼 수 없도록 보장하는 데이터를 전송하기 위한 안전한 프로토콜입니다. Adobe 엔지니어링 서비스는 데이터를 안전하게 유지하기 위해 Sftp 계정을 설정할 수 있습니다.
keywords: ftp; Sftp
seo-description: Sftp는 아무도 데이터를 볼 수 없도록 보장하는 데이터를 전송하기 위한 안전한 프로토콜입니다. Adobe 엔지니어링 서비스는 데이터를 안전하게 유지하기 위해 Sftp 계정을 설정할 수 있습니다.
seo-title: 보안 파일 전송 프로토콜 - 개요
solution: Analytics
title: 보안 파일 전송 프로토콜 - 개요
uuid: 7 DD 1 A 867-E 828-4 C 7 B-BF 11-75 A 81 D 4 C 149 C
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 보안 파일 전송 프로토콜 - 개요

Sftp는 아무도 데이터를 볼 수 없도록 보장하는 데이터를 전송하기 위한 안전한 프로토콜입니다. Adobe 엔지니어링 서비스는 데이터를 안전하게 유지하기 위해 Sftp 계정을 설정할 수 있습니다.

## 배달 푸시 {#section_A47831BB1DCA490BB57F0940617AA506}

이는 Adobe 서버에서 사용자 서버로 파일을 "푸시"하는 것을 의미합니다. 기본적으로 Adobe에서 사용자의 끝 포인트에 배달합니다.

[데이터 웨어하우스](../../../export/ftp-and-sftp/c-sftp/ftp-sftp-dw.md#concept_904ADB7B4FE04DCCB90EFDB6D0DB1076) 및 [Analytics 데이터 피드는](https://marketing.adobe.com/resources/help/en_US/reference/analytics-data-feed.html) Sftp를 통해 데이터를 푸시할 수 있습니다.

The following Analytics tools **cannot** push data via SFTP:

* Reports &amp; Analytics
* Ad Hoc Analysis
* Report Builder

## 배달 가져오기 {#section_FA29FAEF02FE40B8B32452146A036F48}

이는 일반 FTP를 사용하는 Adobe 서버 중 하나로 파일을 보내는 것을 의미합니다. 서버에 있는 파일을 사용하려면 서버에서 Sftp를 사용하여 Adobe의 FTP 서버로 파일을 가져와야 합니다. 다음 세 가지 방법 중 하나를 사용하여 이 작업을 수행할 수 있습니다.

* [Sftp를 통해 암호 없이 Adobe에 연결할 수 있습니다.](../../../export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md#concept_962A381F42A4472AA366A08CCC962846)
* [Sftp를 사용하여 Adobe FTP 계정에 연결합니다.](../../../export/ftp-and-sftp/c-sftp/ftp-sftp-connect.md#concept_01176600188441C6AFB28F5E264D89F8)
* 원하는 보고서를 Adobe의 FTP와 유사한 데이터 피드/R&amp;A/애드혹 등에 푸시한 다음 가져옵니다. Adobe는 사용자가 설정한 Sftp 서버에 이러한 보고서를 제공할 수 없습니다.

