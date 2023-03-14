---
description: Adobe는 SFTP 서버로 Data Warehouse 요청 내보내기를 지원합니다.
keywords: ftp, sftp
title: SFTP 서버로 Data Warehouse 요청 보내기
feature: FTP Export
exl-id: 45694647-69ec-45e3-b614-4a936909a338
source-git-commit: 25eccb2b9fe3827e62b0ae98d9bebf7a97b239f5
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 100%

---

# SFTP 서버로 Data Warehouse 요청 보내기

Adobe는 SFTP 서버로 Data Warehouse 요청 내보내기를 지원합니다.

다음 작업이 완료되었는지 확인합니다.

Adobe는 다음을 충족하는 경우 SFTP 서버로 Data Warehouse 요청 내보내기를 지원합니다.

* Data Warehouse 보고서를 요청할 때 `sftp://`프로토콜을 호스트 필드 (예: `sftp://ftp.example.com`)에 지정하고 포트 22만 사용합니다. 아래 설명된 대로 이 `sftp+norename://` 옵션을 사용할 수도 있습니다.
* Adobe의 `authorized_keys` 파일이 사용자가 로그인한 루트 디렉터리의 `.ssh` 디렉터리에 있습니다.
* 대상이 `ftp.omniture.com`이 아닙니다. Adobe의 내부 서버 사이의 SFTP 프로토콜이 지원되지 않습니다.
* 대상이 단일 (PKI) 인증을 지원합니다. 이중 인증 문제가 있는 경우 보고서 배달이 실패합니다. 서버가 이중 인증을 시도하도록 구성되지 않았는지 확인합니다. Adobe Analytics를 사용하려면 로그인하는 데 키만 사용되며 다른 것은 사용되지 않습니다.
* Adobe는 SSHv2 암호화를 지원하며, SSHv1 (RSA 키만)로 돌아갑니다.

SFTP를 통해 Data Warehouse 요청을 성공적으로 전송하려면:

1. 조직에서 지원하는 사용자 중 한 명이 고객 지원 센터에 문의하여 `authorized_keys` 파일을 얻습니다.
1. 이 파일을 얻었으면 Data Warehouse 요청에 사용한 자격 증명으로 FTP 사이트에 로그인합니다.
1. 루트 디렉터리에서 `.ssh` 폴더 (이 폴더가 없는 경우 만들기)로 이동하여 이 폴더에 `authorized_keys` 파일을 저장합니다.

1. Data Warehouse 요청 관리자로 이동합니다. 원하는 대로 요청을 구성하고 **[!UICONTROL 고급 배달 선택 사항]**&#x200B;을 클릭합니다.

1. 팝업 창에서 **[!UICONTROL FTP]**&#x200B;를 클릭하고 포트 22를 통해 ftp 사이트 (`sftp://` 프로토콜 포함, 예: `sftp://ftp.omniture.com`)를 지정합니다.

   SFTP를 사용하는 경우 `sftp://` 프로토콜만 포함할 수 있습니다. 일반 FTP 요청에는 프로토콜 접두사를 생략해야 합니다 (예: `ftp://ftp.omniture.com` 대신 `ftp.omniture.com`).

1. [폴더] 필드에 파일을 저장할 폴더 이름을 입력합니다. 폴더는 필수입니다.
1. 2단계에서 사용한 사용자 이름과 암호를 입력합니다.
1. **[!UICONTROL 보내기]**&#x200B;를 클릭합니다.

sftp PUT 명령은 .part 확장명이 있는 임시 파일을 지정된 디렉터리에 저장합니다. 업로드가 완료되면 파일 확장명이 최종 확장명으로 이름이 바뀝니다. 이 시점에서 파일을 사용할 수 있습니다.

또는 `sftp+norename://`을 `sftp://` 대신 지정하여 업로드 중에 임시 `.part` 파일 이름 없이 최종 이름으로 직접 파일을 업로드할 수 있습니다. 이 방법은 SFTP 서버가 업로드 중에 파일 이름 변경을 자동으로 처리할 때 적절하며, 업로드가 완료되기 전에 파일을 처리할 기회가 없습니다.
