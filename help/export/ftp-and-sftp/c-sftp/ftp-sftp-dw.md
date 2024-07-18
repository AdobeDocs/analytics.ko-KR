---
description: Adobe는 SFTP 서버로 Data Warehouse 요청 내보내기를 지원합니다.
keywords: ftp, sftp
title: SFTP 서버로 Data Warehouse 요청 보내기
feature: FTP Export
exl-id: 45694647-69ec-45e3-b614-4a936909a338
source-git-commit: d8bfad5d388f906c7c7301a9126813f5c2a5dbaa
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 52%

---

# SFTP 서버로 Data Warehouse 요청 보내기

Adobe은 문서 [Data Warehouse 요청에 대한 보고서 대상 구성](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)의 [SFTP](/help/export/data-warehouse/create-request/dw-request-report-destinations.md#sftp)에 설명된 대로 SFTP 서버로 Data Warehouse 요청 내보내기를 지원합니다.

다음 작업이 완료되었는지 확인합니다.

* Data Warehouse 보고서를 요청할 때 포트 22만 사용됩니다.
* Adobe의 `authorized_keys` 파일이 사용자가 로그인한 루트 디렉터리의 `.ssh` 디렉터리에 있습니다.
* 대상이 `ftp.omniture.com`이 아닙니다. Adobe의 내부 서버 사이의 SFTP 프로토콜이 지원되지 않습니다.
* 대상이 단일 (PKI) 인증을 지원합니다. 이중 인증 문제가 있는 경우 보고서 배달이 실패합니다. 서버가 이중 인증을 시도하도록 구성되지 않았는지 확인합니다. Adobe Analytics를 사용하려면 로그인하는 데 키만 사용되며 다른 것은 사용되지 않습니다.
* Adobe는 SSHv2 암호화를 지원하며, SSHv1 (RSA 키만)로 돌아갑니다.

SFTP를 통해 Data Warehouse 요청을 성공적으로 전송하려면:

1. 문서의 [SFTP](/help/export/data-warehouse/create-request/dw-request-report-destinations.md#sftp)에 설명된 단계, [공개 키 다운로드를 포함하여 Data Warehouse 요청에 대한 보고서 대상 구성](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)을 완료합니다.
1. Data Warehouse 요청에 사용된 자격 증명으로 SFTP 사이트에 로그인합니다.
1. 루트 디렉터리에서 `.ssh` 폴더 (이 폴더가 없는 경우 만들기)로 이동하여 이 폴더에 `authorized_keys` 파일을 저장합니다.

1. [Data Warehouse 요청에 대한 보고서 대상 구성](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)에 설명된 대로 아직 완료하지 않았다면 Data Warehouse 요청을 완료하십시오.
