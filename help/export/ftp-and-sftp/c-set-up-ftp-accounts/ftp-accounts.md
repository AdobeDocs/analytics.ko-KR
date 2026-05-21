---
description: Adobe에서 호스팅하는 FTP 계정을 설정하고 사용합니다.
keywords: ftp, sftp
title: FTP 계정 설정 - 개요
feature: FTP Export
exl-id: 55f942fe-cb06-43e1-bd3c-57d6786278b7
TQID: https://experienceleague.adobe.com/38oslnk-IS87YU9qpOJyEoqytnrMuK5lp3VtYnTyQOg
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 157cc2bde1047063014aff39319d5cfaa1de9b5c
workflow-type: tm+mt
source-wordcount: 316
ht-degree: 14%

---

# FTP 또는 SFTP 계정 설정 - 개요

Adobe에서 호스팅하는 FTP 또는 SFTP 계정을 설정하고 사용합니다.

Adobe은 파일 전송 안정성을 향상하면서 고성능을 보장하도록 설계된 가용성 높은 고성능 FTP 또는 SFTP 클러스터를 유지 관리합니다.

Adobe 고객은 유지 관리 이벤트가 예약된 대로 표준 프로세스를 통해 유지 관리 알림을 받습니다. Adobe FTP 또는 SFTP 시스템이 설계된 대로 작동하고 계속해서 안전하고 안정적인 고성능 데이터 전송을 제공하는지 확인하기 위해 Adobe에서 다음 지침을 준수할 것을 요청합니다.

* 대부분의 Adobe FTP 또는 SFTP 계정(분류, Data Sources 및 기타)은 제공된 기능이 설정된 경우 자동으로 활성화됩니다. 데이터 피드 및 일반 파일 배달 계정의 경우 Adobe 고객 지원 센터에서 새 FTP 또는 SFTP 계정을 설정할 수 있습니다. 이 프로세스는 FTP 또는 SFTP 계정에 보안과 공간을 모두 사용할 수 있는지 확인하기 위해 적용됩니다.
* 데이터가 시스템에 성공적으로 전송된 후 사용자는 Adobe에서 FTP 또는 SFTP 계정에 제공한 데이터를 제거해야 합니다.
* FTP 또는 SFTP 계정이 더 이상 필요하지 않아 비활성화할 수 있는 경우 Adobe에 알립니다.

Adobe FTP 호스트 이름은 `ftp://ftp.omniture.com` 또는 `ftp://ftp2.omniture.com`입니다.

이 정보는 사용자 이름 및 암호와 함께 CX Enterprise (분류 및 데이터 소스)에 제공해야 하거나, 요청 시 계정 설정을 담당하는 Adobe 담당자가 제공해야 합니다. 사용할 FTP 또는 SFTP 주소를 모를 경우 올바른 주소를 제공할 수 있는 Adobe 계정 팀에 문의하십시오. 또한 분류 및 Data Sources 계정의 경우, Adobe에는 FTP 또는 SFTP 파일이 처리되는 특정 시간이 없습니다. 대신 Adobe은 새 파일 프로세스에 대해 FTP 또는 SFTP 계정을 지속적으로 폴링하는 스크립트를 사용합니다. 이러한 계정에 업로드된 파일은 가능한 한 빨리 처리됩니다.
