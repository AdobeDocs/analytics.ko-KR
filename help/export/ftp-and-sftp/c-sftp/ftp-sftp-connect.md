---
description: Adobe FTP Server로 보안 전송을 설정하는 지침입니다.
keywords: ftp;sftp
seo-description: Adobe FTP Server로 보안 전송을 설정하는 지침입니다.
seo-title: SFTP를 통해 Adobe FTP 계정에 연결
solution: Analytics
title: SFTP를 통해 Adobe FTP 계정에 연결
uuid: 4faf27b8-7276-4c68-87cb-35802b809e27
translation-type: tm+mt
source-git-commit: 8c4c368a84ba5499d85f0b7512c99de47ddb14c2

---


# SFTP를 통해 Adobe FTP 계정에 연결

Adobe FTP Server로 보안 전송을 설정하는 지침입니다.

1. Adobe에서 호스팅하는 FTP 계정을 요청합니다(50MB 할당량).
1. 공개/개인 RSA 키를 만듭니다. Linux에서 다음을 실행합니다.

   ```
   ssh-keygen -t rsa
   ```

   Windows 환경에서는 puttyGen을 사용하여 키를 만듭니다.

1. Create a file named [!DNL authorized_keys] (no extension).
1. Copy the contents of the Public key into [!DNL authorized_keys].
1. Upload [!DNL authorized_keys] to an FTP account:

   * Adobe FTP 계정에 연결합니다.
   * Create a [!DNL .ssh] directory (if it does not already exist).
   * Upload the [!DNL authorized_keys] file to the [!DNL .ssh] directory.

1. SFTP를 사용하여 FTP 계정에 로그인하여 연결을 테스트합니다.

[자세한 내용은 sFTP ](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md)를 통해 암호 없이 Adobe에 연결하는 방법_...을 참조하십시오..
