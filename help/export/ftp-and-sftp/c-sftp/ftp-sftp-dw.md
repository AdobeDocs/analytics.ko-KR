---
description: Adobe는 Sftp 서버로 데이터 웨어하우스 요청 내보내기를 지원합니다.
keywords: ftp; Sftp
seo-description: Adobe는 Sftp 서버로 데이터 웨어하우스 요청 내보내기를 지원합니다.
seo-title: SFTP 서버로 데이터 웨어하우스 요청 보내기
solution: Analytics
title: SFTP 서버로 데이터 웨어하우스 요청 보내기
uuid: 393634 A 1-0643-4 D 63-BB 6 E-FB 80 F 1 BA 76 C 1
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# SFTP 서버로 데이터 웨어하우스 요청 보내기

Adobe는 Sftp 서버로 데이터 웨어하우스 요청 내보내기를 지원합니다.

다음 작업이 완료되었는지 확인합니다.

Adobe는 다음을 충족하는 경우 Sftp 서버로 데이터 웨어하우스 요청 내보내기를 지원합니다.

* [!DNL sftp://] 프로토콜은 호스트 필드에 지정되며 (예: [!DNL sftp://ftp.example.com]) 데이터 웨어하우스 보고서를 요청할 때 포트 22만 사용됩니다.

   You can also use the [!DNL sftp+norename://] option, as described below.

* Adobe's [!DNL authorized_keys] file is in the [!DNL .ssh] directory within the root directory of the user you log in with

* 대상이 [!DNL ftp.omniture.com]이 아닙니다. Adobe의 내부 서버 사이의 SFTP 프로토콜이 지원되지 않습니다.
* 대상이 단일(PKI) 인증을 지원합니다. 이중 인증 문제가 있는 경우 보고서 배달이 실패합니다. 서버가 이중 인증을 시도하도록 구성되지 않았는지 확인합니다. Adobe Analytics를 사용하려면 로그인하는 데 키만 사용되며 다른 것은 사용되지 않습니다.
* Adobe는 SSHv2 암호화를 지원하며, SSHv1(RSA 키만)로 돌아갑니다.

To successfully send a [!DNL Data Warehouse] request via SFTP:

1. 조직에서 지원하는 사용자 중 한 명이 고객 지원 센터에 문의하여 [!DNL authorized_keys] 파일을 얻습니다.
1. After this file is obtained, log in to the FTP site under the same credentials that are used for the [!DNL Data Warehouse] request.
1. In the root directory, navigate to the folder named [!DNL .ssh] (if one does not exist, create one) and place the [!DNL authorized_keys] file there.

1. [!DNL Data Warehouse] 요청 관리자로 이동합니다. 원하는 대로 요청을 구성하고 **[!UICONTROL 고급 배달 선택 사항을 클릭합니다]**.

1. In the pop-up window, click **[!UICONTROL FTP]**, then specify the ftp site (including the [!DNL sftp://] protocol, such as [!DNL sftp://ftp.omniture.com]) via port 22.

   Including the [!DNL sftp://] protocol is only permitted when using SFTP. Regular FTP requests should omit the protocol prefix (such as, [!DNL ftp.omniture.com] instead of [!DNL ftp://ftp.omniture.com]).

1. [폴더] 필드에 파일을 저장할 폴더 이름을 입력합니다. 폴더는 필수입니다.
1. 2단계에서 사용한 사용자 이름과 암호를 입력합니다.
1. **[!UICONTROL 보내기를 클릭합니다]**.

sftp PUT 명령은 .part 확장명이 있는 임시 파일을 지정된 디렉토리에 저장합니다. 업로드가 완료되면 파일 확장명이 최종 확장명으로 이름이 바뀝니다. 이 시점에서 파일을 사용할 수 있습니다.

Alternatively, [!DNL sftp+norename://] can be specified instead of [!DNL sftp://] to upload the file directly with the final name, without a temporary [!DNL .part] file name during upload. 이 방법은 Sftp 서버가 업로드 중에 파일 이름을 자동으로 처리하며 업로드가 완료되기 전에 파일이 처리될 가능성이 없을 때 적합합니다.
