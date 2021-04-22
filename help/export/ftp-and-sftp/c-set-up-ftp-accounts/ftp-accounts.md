---
description: Adobe에서 호스팅하는 FTP 계정을 설정하고 사용합니다.
keywords: ftp, sftp
title: FTP 계정 설정 - 개요
uuid: e5524619-248a-4aae-9f64-cd7d33f3c407
exl-id: 55f942fe-cb06-43e1-bd3c-57d6786278b7
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '290'
ht-degree: 100%

---

# FTP 계정 설정 - 개요

Adobe에서 호스팅하는 FTP 계정을 설정하고 사용합니다.

Adobe는 파일 전송 안정성을 향상하면서 고성능을 보장하도록 설계된 가용성 높은 고성능 FTP 클러스터를 유지 관리합니다.

Adobe 고객은 유지 관리 이벤트가 예약된 대로 표준 프로세스를 통해 유지 관리 알림을 받습니다. Adobe FTP 시스템이 설계된 대로 작동하고 계속해서 안전하고 안정적인 고성능 데이터 전송을 제공하는지 확인하기 위해 Adobe에서는 다음 지침을 준수할 것을 요청합니다.

* 대부분의 Adobe FTP 계정 (분류, Data Sources 및 기타)은 제공된 기능이 설정된 경우 자동으로 활성화됩니다. 데이터 피드 및 일반 파일 배달 계정에 대해 Adobe 고객 지원 팀에서 새 FTP 계정을 설정할 수 있습니다. 이 프로세스는 FTP 계정에 보안과 공간을 모두 사용할 수 있는지 확인하기 위해 적용됩니다.
* 데이터가 해당 시스템으로 성공적으로 전송되면 사용자는 Adobe에서 FTP 계정에 제공한 데이터를 제거해야 합니다.
* FTP 계정이 더 이상 필요하지 않으므로 비활성화할 수 있는 경우 Adobe에 알립니다.

Adobe FTP 호스트 이름은 [!DNL ftp.omniture.com] 또는 [!DNL ftp2.omniture.com]입니다.

이 정보는 사용자 이름 및 암호와 함께 [!UICONTROL Experience Cloud]  (분류 및 데이터 소스)에 제공해야 하거나, 요청 시 계정 설정을 담당하는 Adobe 담당자가 제공해야 합니다. 사용할 FTP 주소를 모를 경우 올바른 주소를 제공할 수 있는 Adobe 계정 관리자에게 문의하십시오. 또한, 분류 및 Data Sources 계정에 대해 Adobe는 FTP 파일이 처리되는 특정 시간이 없습니다. 대신 Adobe는 새 파일 프로세스에 대해 FTP 계정을 지속적으로 폴링하는 스크립트를 사용합니다. 이러한 계정에 업로드된 파일은 가능한 한 빨리 처리됩니다.
