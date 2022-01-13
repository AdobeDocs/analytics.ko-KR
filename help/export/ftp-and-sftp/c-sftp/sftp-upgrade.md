---
title: SFTP 서비스 업그레이드 - FAQ
description: 2022년 5월에 예정된 SFTP 서비스 업그레이드에 대한 FAQ입니다.
source-git-commit: eb9bdcbd99d45afc913c5ade37e8fb5c62a3a456
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 2%

---


# SFTP 서비스 업그레이드 - FAQ

설정 **2022년 5월 2일**, Adobe Analytics은 보안 파일 전송 프로토콜을 업그레이드합니다 [SFTP] 파일 전송을 위한 향상된 보안을 제공하기 위한 서비스입니다. 이 변경 사항으로 인해 일부 SFTP 클라이언트 구성이 더 이상 지원되지 않습니다. 다음 방법으로 사용 가능한 일부 연결 옵션도 추가하겠습니다. **2022년 3월 1일**. 이 작업은 SFTP를 사용하여 Adobe Analytics으로 전송되거나에서 검색된 데이터에만 영향을 줍니다. FTP 프로토콜은 영향을 받지 않습니다. 서비스 중단을 방지하려면 SFTP 클라이언트(코드, 도구, 서비스)가 아래에 자세히 설명된 변경 사항에 부합하는지 확인하십시오.

## 조직에서 현재 사용하는 알고리즘, 연결 유형 및 프로토콜을 어떻게 확인할 수 있습니까?

사용 중인 FTP/SFTP 소프트웨어는 Adobe Analytics과의 데이터 교환을 위해 구성한 연결에 어떤 특정 설정을 사용하고 있는지를 나타내야 합니다. 이 소프트웨어에는 연결에 사용할 수 있는 다양한 옵션에 대한 설명서도 포함되어야 합니다. 이 업데이트 후에 지원되는 옵션은 업계에서 널리 지원되고 수락됩니다.

## 데이터 처리에 SFTP를 사용하는 Adobe Analytics 기능은 무엇입니까?

다음 기능은 SFTP를 사용하여 Adobe Analytics에 데이터를 업로드할 수 있는 옵션을 제공합니다.

* [분류](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-saint.html)

* [데이터 피드](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-datafeeds.html)

* [데이터 소스](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-datasources.html)

* [Data Warehouse 게재된 보고서](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-dw-reports.html)

* 또한 다음을 통해 생성된 일부 사용자 지정 구현 [엔지니어링 서비스](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-eng-services.html) 는 SFTP를 사용하여 Adobe과 데이터를 교환할 수 있습니다.

## 이 업데이트에는 어떤 특정 변경 사항이 포함됩니까?

다음은 제거되고 지원될 연결 및 알고리즘에 대한 세부 목록입니다.

* SFTP 프로토콜 mac 알고리즘:

   * 더 이상 지원하지 않습니다. hmac-md5, hmac-md5-96, hmac-ripemd160, hmacripemd160@openssh.com, hmac-sha1, hmac-sha1-96, hmac-sha1-etm@openssh.com, umac-64@openssh.com

   * Adobe는 다음과 같은 경우에만 지원합니다. hmac-sha2-512-etm@openssh.com, hmac-sha2-256-etm@openssh.com, umac-128-etm@openssh.com, hmac-sha2-512, hmacsha2-256, umac-128@openssh.com

* SFTP 프로토콜 암호 알고리즘:

   * 더 이상 지원하지 않습니다. 3des-cbc, aes128-cbc, aes128-gcm@openssh.com, aes192-cbc, aes256-cbc, aes256-gcm@openssh.com, arcfour, arcfour128, arcfour256, blowfish-cbc, cast128-cbc, rijndael-cbc@lysator.liu.se

   * Adobe는 다음과 같은 경우에만 지원합니다. aes128-ctr, aes192-ctr, aes256-ctr

* SFTP 프로토콜 지원 연결:

   * SFTP 프로토콜을 통해 scp 및 rsync 명령 또는 연결을 더 이상 지원하지 않습니다

   * 순수 SFTP 프로토콜 연결만 지원합니다

* 지원되는 FTP/SFTP 클라이언트/프로토콜:

   * FTP: vsftpd 버전 3.0.2-25 이상

   * SFTP: opensh 버전 7.4p1-21 이상