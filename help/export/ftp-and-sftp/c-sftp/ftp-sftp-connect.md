---
description: Adobe FTP Server로 보안 전송을 설정하는 지침입니다.
keywords: ftp; Sftp
seo-description: Adobe FTP Server로 보안 전송을 설정하는 지침입니다.
seo-title: Sftp를 사용하여 Adobe FTP 계정에 연결
solution: Analytics
title: Sftp를 사용하여 Adobe FTP 계정에 연결
uuid: 4 FAF 27 B 8-7276-4 C 68-87 CB -35802 B 809 E 27
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Sftp를 사용하여 Adobe FTP 계정에 연결

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
   * [!DNL .ssh] 디렉토리를 만듭니다 (아직 없는 경우).
   * Upload the [!DNL authorized_keys] file to the [!DNL .ssh] directory.

1. Sftp를 사용하여 FTP 계정에 로그인하여 연결을 테스트합니다.

For more detailed information, see [How to Connect to Adobe via sFTP Without a Password_...](../../../export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md#concept_962A381F42A4472AA366A08CCC962846).
