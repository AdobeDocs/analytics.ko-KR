---
description: FTP 계정에 암호 없이 연결하는 것은 Sftp 연결과 대체 인증 방법을 모두 사용하여 가능합니다. 이 작업에는 공개 및 개인 키 조합이라고 하는 두 개 파일(각각 FTP 계정과 사용자 컴퓨터 상주용)이 포함됩니다.
keywords: ftp; Sftp
seo-description: FTP 계정에 암호 없이 연결하는 것은 Sftp 연결과 대체 인증 방법을 모두 사용하여 가능합니다. 이 작업에는 공개 및 개인 키 조합이라고 하는 두 개 파일(각각 FTP 계정과 사용자 컴퓨터 상주용)이 포함됩니다.
seo-title: Sftp를 통해 암호 없이 Adobe에 연결
solution: Analytics
title: Sftp를 통해 암호 없이 Adobe에 연결
uuid: 88728309-50 D 2-450 B-B 0 E 6-7 DCDF 61 B 5 DBC
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Sftp를 통해 암호 없이 Adobe에 연결

FTP 계정에 암호 없이 연결하는 것은 Sftp 연결과 대체 인증 방법을 모두 사용하여 가능합니다. 이 작업에는 공개 및 개인 키 조합이라고 하는 두 개 파일(각각 FTP 계정과 사용자 컴퓨터 상주용)이 포함됩니다.

이 방법은 암호 인증보다 안전합니다. 이 방법은 사용자가 매번 암호를 입력하지 않아도 되는 또 다른 인증 양식입니다. 올바르게 사용할 경우 이러한 파일은 특정 컴퓨터가 암호를 지정하지 않고도 로그인할 수 있도록 허용합니다. 이 작업은 컴퓨터마다 설정해야 합니다. 이러한 키 파일을 사용하지 않는 다른 연결에는 모두 암호를 지정해야 합니다.

Sftp (Secure File Transfer Protocol) 는 일부 클라이언트가 중요한 데이터를 전송하는 데 필요합니다. Sftp 연결은 암호화된 데이터 통신을 허용하므로 일반 FTP 연결보다 더 안전합니다. 기본적으로 모든 Adobe FTP 계정은 Sftp가 준비되어 있습니다. Sftp 연결은 포트 22 (비보안 포트 21 사용) 에서 연결하는 Sftp 클라이언트를 사용하여 유효한 사용자 이름과 암호로 열 수 있습니다.

Sftp를 사용할 때는 특정 조건에서 개인 키를 사용하여 암호 없이 계정에 연결할 수 있습니다. 이 방법을 사용하면 사용자 컴퓨터에서 일반 암호 인증 대신 인증에 키 파일을 사용할 수 있습니다. 즉, 개인 키가 있는 컴퓨터만 암호 없이 연결할 수 있습니다. 다른 모든 컴퓨터/사용자는 여전히 암호 인증을 사용해야 합니다(개인 키가 이러한 다른 컴퓨터에 설정되지 않은 경우).

**암호를 사용하지 않는 인증에 개인 키를 설정하고 사용하려면**

1. FTP 계정 만들기(Adobe).

   Adobe 담당자는 FTP 계정이 없는 경우 만들 수 있습니다. Adobe 계정 관리자 또는 Adobe 고객 지원 팀에 문의하여 계정을 만듭니다.
1. 공개/개인 키 만들기(고객).

   공개 및 개인 키 조합을 만듭니다. 개인 키는 컴퓨터/서버 전용 파일이며, 컴퓨터/서버에 있습니다. 공개 키 파일은 Adobe 계정으로 업로드해야 합니다. 이 방법으로 사용하는 경우 암호 인증 없이 연결할 수 있습니다. Adobe의 공개 키 파일은 컴퓨터/서버의 개인 키 파일에 일치하며 해당 방법으로 인증합니다.

   이러한 파일을 만들려면 내부 네트워크 지원 그룹에 참여하여 환경에 적합한 키를 만듭니다. 이러한 두 파일을 만드는 데 사용할 수 있는 도구와 애플리케이션이 여러 개 있습니다.

   이 작업을 UNIX 쉘 환경에서 수행하는 방법에 대한 예가 아래에 나와 있습니다. 이는 이 작업을 수행하는 방법의 한 가지 예에 불과하며, 사용자 팀이나 내부 네트워크 그룹의 통신 요구 사항에 대한 유용한 참조 포인트 역할을 합니다.

   ```
   // Linux/Unix (bash shell)
   
   // First make sure the ".ssh" directory exists
   
   $ mkdir ~/.ssh
   
   $ cd ~/.ssh
   
   // Now actually generate the key pair
   
   // Usually we will want to create an empty passphrase (just hit "Enter" for both password prompts)
   
   $ ssh-keygen -q -t dsa
   
   Enter file in which to save the key (/home/user/.ssh/id_dsa):
   
   Enter passphrase (empty for no passphrase): ...
   
   Enter same passphrase again: ...
   
   // Rename or copy the public key file to "authorized_keys"
   
   // This "authorized_keys" file is the one that we will upload to the Adobe FTP server in step 3
   
   $ cp id_dsa.pub authorized_keys 
   ```

1. FTP 계정에 공개 키 업로드(고객).

   공개 키를 업로드하고 테스트합니다. Connect to the Adobe FTP account and create a [!DNL .ssh] directory, if it does not already exist. Upload the [!DNL authorized_keys] file to this [!DNL .ssh] directory. 이 작업은 다른 여러 가지 방법(명령줄, 그래픽 FTP 클라이언트 등)으로 수행할 수 있습니다. 디렉토리를 만들고 파일을 업로드하는 기능만 있으면 됩니다.

   다음은 UNIX 쉘을 사용하여 이 작업을 수행하는 예입니다.

   ```
   $ ftp ftp.Adobe.com
   
   OR (depending on hostname provided by Adobe)
   
   $ ftp ftp2.Adobe.com
   
   // Enter username and password for account as prompted
   
   ftp> mkdir .ssh
   
   ftp> cd .ssh
   
   ftp> put authorized_keys
   
   ftp> exit
   
   // Now test the connection by logging in to the server using "sftp" command:
   
   $ sftp username@ftp.omniture.com
   
   OR (depending on hostname provided by Adobe)
   
   $ sftp username@ftp2.omniture.com
   
   // You should immediately receive an sftp prompt without having to enter the password:
   
   sftp>
   ```

