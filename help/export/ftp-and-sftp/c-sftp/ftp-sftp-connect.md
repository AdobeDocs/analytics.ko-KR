---
description: Adobe FTP Server로 보안 전송을 설정하는 지침입니다.
keywords: ftp;sftp
title: SFTP를 통해 Adobe FTP 계정에 연결
uuid: 4faf27b8-7276-4c68-87cb-35802b809e27
translation-type: ht
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# SFTP를 통해 Adobe FTP 계정에 연결

Adobe FTP Server로 보안 전송을 설정하는 지침입니다.

1. Adobe에서 호스팅하는 FTP 계정을 요청합니다(50MB 할당량).
1. 공개/개인 RSA 키를 만듭니다. Linux에서 다음을 실행합니다.

   ```
   ssh-keygen -t rsa
   ```

   Windows 환경에서는 puttyGen을 사용하여 키를 만듭니다.

1. [!DNL authorized_keys]라는 파일(확장명 없음)을 만듭니다.
1. 공개 키의 콘텐츠를 [!DNL authorized_keys]에 복사합니다.
1. [!DNL authorized_keys]를 FTP 계정에 업로드합니다.

   * Adobe FTP 계정에 연결합니다.
   * [!DNL .ssh] 디렉토리가 없는 경우 디렉토리를 만듭니다.
   * [!DNL authorized_keys] 파일을 [!DNL .ssh] 디렉토리에 업로드합니다.

1. SFTP를 사용하여 FTP 계정에 로그인하여 연결을 테스트합니다.

자세한 내용은 [SFTP를 통해 암호 없이 Adobe에 연결하는·방법](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md)을·참조하십시오.
