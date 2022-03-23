---
title: SFTP 서비스 업그레이드 - FAQ
description: 2022년 5월에 예정된 SFTP 서비스 업그레이드에 대해 자주 묻는 질문
feature: FTP Export
exl-id: e271b545-0769-4a69-9d7f-dc46bc654737
source-git-commit: dd1b2d358e6074fc393e6e5999c4286549a1b82d
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 100%

---

# SFTP 서비스 업그레이드 - FAQ

**2022년 5월 15일**, Adobe Analytics는 파일 전송 보안을 개선하기 위해 Secure File Transfer Protocol([SFTP]) 서비스를 업그레이드할 예정입니다. 이 변경 사항으로 일부 SFTP 클라이언트 구성은 더 이상 지원되지 않습니다. 또한 **2022년 3월 1일**&#x200B;까지 사용할 수 있는 몇 가지 연결 옵션을 추가할 예정입니다. 이는 SFTP를 사용하여 Adobe Analytics로 전송되거나 Adobe Analytics에서 검색된 데이터에만 영향을 미칩니다. FTP 프로토콜은 영향을 받지 않습니다. 서비스 중단을 방지하려면 SFTP 클라이언트(코드, 도구, 서비스)가 아래에 설명된 변경 사항을 준수하는지 확인하십시오.

## 현재 조직에서 사용 중인 알고리즘, 연결 유형 및 프로토콜을 확인하려면 어떻게 해야 합니까?

사용 중인 FTP/SFTP 소프트웨어는 Adobe Analytics와 데이터를 교환하기 위해 구성한 연결에서 어떤 특정 설정이 사용되고 있는지 표시해야 합니다. 이 소프트웨어에는 연결에 사용할 수 있는 다양한 옵션에 대한 설명서도 포함되어야 합니다. 이 업데이트 이후에 지원되는 옵션은 업계에서 널리 지원되고 수용됩니다.

제거될 연결 옵션은 일반적으로 더 이상 사용하지 않는 것으로 간주되며 현재 소프트웨어에서 사용되지 않습니다. 지난 3년 이내에 FTP/SFTP 소프트웨어를 업그레이드했다면 이미 호환되는 연결이 있을 수 있습니다.

## 데이터 수집에 SFTP를 사용하는 Adobe Analytics 기능은 무엇입니까?

다음 기능은 SFTP를 사용하여 Adobe Analytics에 데이터를 업로드하는 옵션을 제공합니다.

* [분류](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-saint.html?lang=ko-KR)

* [데이터 피드](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-datafeeds.html?lang=ko-KR)

* [데이터 소스](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-datasources.html?lang=ko-KR)

* [Data Warehouse 게재된 보고서](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-dw-reports.html?lang=ko-KR)

* 또한 [엔지니어링 서비스](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-eng-services.html?lang=ko-KR)를 통해 생성된 맞춤형 구현은 SFTP를 사용하여 Adobe와 데이터를 교환할 수 있습니다.

## 이 업데이트에 포함된 특정 변경 사항은 무엇입니까?

다음은 제거되고 지원되는 연결 및 알고리즘에 대한 상세 목록입니다.

* SFTP 프로토콜 mac 알고리즘:

   * 더 이상 지원되지 않음: hmac-md5, hmac-md5-96, hmac-ripemd160, hmacripemd160@openssh.com, hmac-sha1, hmac-sha1-96, hmac-sha1-etm@openssh.com, umac-64-etm@openssh.com, umac-64@openssh.com

   * 다음만 지원됨: hmac-sha2-512-etm@openssh.com, hmac-sha2-256-etm@openssh.com, umac-128-etm@openssh.com, hmac-sha2-512, hmacsha2-256, umac-128@openssh.com

* SFTP 프로토콜 암호 알고리즘:

   * 더 이상 지원되지 않음: 3des-cbc, aes128-cbc, aes128-gcm@openssh.com, aes192-cbc, aes256-cbc, aes256-gcm@openssh.com, arcfour, arcfour128, arcfour256, blowfish-cbc, cast128-cbc, rijndael-cbc@lysator.liu.se

   * 다음만 지원됨: aes128-ctr, aes192-ctr, aes256-ctr

* SFTP 프로토콜 지원 연결:

   * 더 이상 scp 및 rsync 명령의 사용이나 SFTP 프로토콜을 통한 연결을 지원하지 않습니다.

   * 순수 SFTP 프로토콜 연결만 지원합니다.

* FTP/SFTP 클라이언트/프로토콜 지원:

   * FTP: vsftpd 버전 3.0.2-25 이상

   * SFTP: openssh 버전 7.4p1-21 이상
