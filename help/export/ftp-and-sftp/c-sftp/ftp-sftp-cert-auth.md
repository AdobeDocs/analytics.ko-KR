---
description: 암호 없이 FTP 계정에 연결하려면 SFTP 연결과 대체 인증 방법을 모두 사용해야 합니다. 이 작업에는 공개 및 개인 키 조합이라고 하는 두 개 파일 (각각 FTP 계정과 사용자 컴퓨터 상주용)이 포함됩니다.
keywords: ftp, sftp
title: SFTP를 통해 암호 없이 Adobe에 연결
feature: FTP Export
exl-id: 7ff9511c-50a2-466f-b5af-6bbd59941ce5
TQID: 'https://experienceleague.adobe.com/5XpefTP6xLr007yTQjLDVoj-j-EcPLvBDda-NNIg6xA'
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
source-wordcount: 609
ht-degree: 46%

---

# SFTP를 통해 암호 없이 Adobe에 연결

암호 없이 FTP 계정에 연결하려면 SFTP 연결과 대체 인증 방법을 모두 사용해야 합니다. 이 작업에는 공개 및 개인 키 조합이라고 하는 두 개 파일 (각각 FTP 계정과 사용자 컴퓨터 상주용)이 포함됩니다.

이는 암호 인증보다 덜 안전하지 않습니다. 사용자가 매번 암호를 입력할 필요가 없는 또 다른 인증 방식입니다. 이 파일을 올바르게 사용하면 암호를 지정하지 않고도 특정 컴퓨터가 로그인할 수 있습니다. 컴퓨터 단위로 설정해야 합니다. 이러한 키 파일을 사용하지 않는 다른 모든 연결에서는 암호를 지정해야 합니다.

SFTP (Secure File Transfer Protocol)는 일부 클라이언트가 중요한 데이터를 전송하는 데 필요합니다. SFTP 연결은 암호화된 데이터 통신을 허용하므로 일반 FTP 연결보다 훨씬 안전합니다. 기본적으로 모든 Adobe FTP 계정은 SFTP가 준비되어 있습니다. SFTP 연결은 포트 22 (안전하지 않은 일반 FTP 연결은 포트 21 사용)에서 연결하는 SFTP 클라이언트를 사용하여 올바른 사용자 이름과 암호로 열 수 있습니다.

SFTP를 사용할 때 특정 조건에서 개인 키를 사용하여 암호 없이 계정에 연결할 수 있습니다. 이 방법을 사용하면 컴퓨터에서 일반적인 암호 인증 대신 인증에 키 파일을 사용할 수 있습니다. 개인 키를 보유하고 있는 컴퓨터만 비밀번호 없이 연결할 수 있다는 의미다. 다른 모든 컴퓨터/사용자는 여전히 암호 인증을 사용해야 합니다 (개인 키가 이러한 다른 컴퓨터에 설정되지 않은 경우).

**암호 없는 인증을 위해 개인 키를 설정하고 사용하려면**

1. FTP 계정 만들기 (Adobe).

   Adobe 담당자가 FTP 계정이 없는 경우 만들 수 있습니다. 계정을 만들려면 Adobe 계정 팀 또는 Adobe 고객 지원 센터에 문의하십시오.
1. 공개/개인 키 만들기 (고객).

   공개 키와 개인 키 조합을 만듭니다. 개인 키는 사용자 컴퓨터/서버에 대해 비공개이며 상주하는 파일입니다. 공개 키 파일을 Adobe 계정에 업로드해야 합니다. 이러한 방식으로 사용할 경우 암호 인증 없이 연결할 수 있습니다. Adobe의 공개 키 파일은 컴퓨터/서버의 개인 키 파일과 일치하며 이러한 방식으로 인증됩니다.

   이러한 파일을 만들려면 내부 네트워크 지원 그룹에 참여하여 환경에 적합한 키 세트를 만드십시오. 이러한 두 파일을 만드는 데 사용할 수 있는 많은 도구와 애플리케이션이 있습니다.

   다음은 UNIX 셸 환경에서 이 작업을 수행하는 방법의 예입니다. 이는 이 작업을 수행하는 방법의 한 가지 예일 뿐이며, 팀이나 내부 네트워크 그룹에 요구 사항을 전달할 때 유용한 참조 정보로 활용할 수 있습니다.

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

1. FTP 계정에 공개 키 업로드 (고객).

   공개 키를 업로드하고 테스트합니다. Adobe FTP 계정에 연결하고 [!DNL .ssh] 디렉토리가 없는 경우 만듭니다. [!DNL authorized_keys] 파일을 이 [!DNL .ssh] 디렉토리에 업로드합니다. 이 작업은 다른 여러 가지 방법 (명령줄, 그래픽 FTP 클라이언트 등)으로 수행할 수 있습니다. 디렉터리를 만들고 파일을 업로드하는 기능만 필요합니다.

   여기서도 UNIX 셸을 사용하여 이 작업을 수행하는 예입니다.

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
