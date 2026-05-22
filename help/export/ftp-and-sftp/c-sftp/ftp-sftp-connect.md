---
description: Adobe FTP Server로 보안 전송을 설정하는 지침입니다.
keywords: ftp, sftp
title: SFTP를 통해 Adobe FTP 계정에 연결
feature: FTP Export
exl-id: 727d4f7a-d7d1-40cf-bdcd-c783ca47f51c
TQID: 'https://experienceleague.adobe.com/5X1Nx0V0hievpCe9G1Q6gJS1c55T3xl5FuneZxPx4TI'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
subfeature_v2:
  - id: a8bf2e97-0add-4437-b976-1fc5154911a8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 214
ht-degree: 38%

---

# SFTP를 통해 FTP 계정에 연결

FTP를 사용하여 보안 전송을 설정하려면:

1. (조건부) Adobe FTP 서버를 사용하여 보안 전송을 설정하려면 다음을 수행합니다.

   1. Adobe에서 호스팅하는 FTP 계정을 요청합니다 (50MB 할당량).

   1. 공개/비공개 키를 만듭니다.

      * Linux 환경에서 다음을 실행합니다.

        ```
        ssh-keygen -t ed25519 -C "your-comment-or-email"
        ```

        정책에서 ed25519 사용을 허용하지 않는 경우 다음을 실행합니다.

        ```
        ssh-keygen -t rsa -b 4096 -C "your-comment-or-email"
        ```

        **참고:** 이는 일반적으로 최신 FIPS 186-5에서 먼저 지원되므로 FIPS 186-4에서 작동하25519 고객에게 적용됩니다.

      * Windows 환경에서 puttyGen을 사용합니다.

1. (조건부) 고유한 FTP 위치를 사용하여 보안 전송을 설정하려면 유효한 RSA 또는 ed25519 공개 키가 포함된 SFTP 호스트, 사용자 이름 및 대상 사이트가 있어야 합니다. 피드를 만들 때 적절한 공개 키를 다운로드할 수 있습니다.

1. [!DNL `authorized_keys`]라는 파일 (확장명 없음)을 만듭니다.

1. 공개 키의 콘텐츠를 [!DNL `authorized_keys`]에 복사합니다.

1. [!DNL `authorized_keys`]를 FTP 계정에 업로드합니다.

   * Adobe FTP 계정에 연결합니다.
   * [!DNL .ssh] 디렉토리가 없는 경우 디렉토리를 만듭니다.
   * [!DNL `authorized_keys`] 파일을 [!DNL .ssh] 디렉토리에 업로드합니다.

1. SFTP를 사용하여 FTP 계정에 로그인하여 연결을 테스트합니다.

자세한 내용은 [암호 없이 SFTP를 통해 Adobe에 연결](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md)을 참조하세요.

