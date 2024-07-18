---
description: Adobe FTP Server로 보안 전송을 설정하는 지침입니다.
keywords: ftp, sftp
title: SFTP를 통해 Adobe FTP 계정에 연결
feature: FTP Export
exl-id: 727d4f7a-d7d1-40cf-bdcd-c783ca47f51c
source-git-commit: 62132284ca70f3bdb1a8896e4548b8b63a5c03c8
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 58%

---

# SFTP를 통해 FTP 계정에 연결

FTP를 사용하여 보안 전송을 설정하려면:

1. (조건부) Adobe FTP 서버를 사용하여 보안 전송을 설정하려면 다음을 수행합니다.

   1. Adobe에서 호스팅하는 FTP 계정을 요청합니다 (50MB 할당량).

   1. 공개/비공개 RSA 키를 만듭니다.

      * Linux 환경에서 다음을 실행합니다.

        ```
        ssh-keygen -t rsa
        ```

      * Windows 환경에서 puttyGen을 사용합니다.

1. (조건부) 고유한 FTP 위치를 사용하여 보안 전송을 설정하려면 유효한 RSA 또는 DSA 공개 키가 포함된 SFTP 호스트, 사용자 이름 및 대상 사이트가 있어야 합니다. 피드를 만들 때 적절한 공개 키를 다운로드할 수 있습니다.

1. [!DNL authorized_keys]라는 파일 (확장명 없음)을 만듭니다.

1. 공개 키의 콘텐츠를 [!DNL authorized_keys]에 복사합니다.

1. [!DNL authorized_keys]를 FTP 계정에 업로드합니다.

   * Adobe FTP 계정에 연결합니다.
   * [!DNL .ssh] 디렉토리가 없는 경우 디렉토리를 만듭니다.
   * [!DNL authorized_keys] 파일을 [!DNL .ssh] 디렉토리에 업로드합니다.

1. SFTP를 사용하여 FTP 계정에 로그인하여 연결을 테스트합니다.

자세한 내용은 [SFTP를 통해 암호 없이 Adobe에 연결하는·방법](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md)을·참조하십시오.
