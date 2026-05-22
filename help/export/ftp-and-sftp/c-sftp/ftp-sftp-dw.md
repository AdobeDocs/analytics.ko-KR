---
description: Adobe는 SFTP 서버로 Data Warehouse 요청 내보내기를 지원합니다.
keywords: ftp, sftp
title: SFTP 서버로 Data Warehouse 요청 보내기
feature: FTP Export
exl-id: 45694647-69ec-45e3-b614-4a936909a338
TQID: 'https://experienceleague.adobe.com/gZvqhVFN2WKnk0hs2t8R5fcg5g8Tts1jKZPvMqeGcy4'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
subfeature_v2: id: a8bf2e97-0add-4437-b976-1fc5154911a8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 258
ht-degree: 39%

---

# SFTP 서버로 Data Warehouse 요청 보내기

Adobe은 문서 [Data Warehouse 요청에 대한 보고서 대상 구성](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)의 [SFTP](/help/export/data-warehouse/create-request/dw-request-report-destinations.md#sftp)에 설명된 대로 Data Warehouse 요청을 SFTP 서버로 내보낼 수 있습니다.

다음 작업이 완료되었는지 확인합니다.

* Data Warehouse 보고서를 요청할 때 포트 22만 사용됩니다.
* Adobe의 `authorized_keys` 파일이 사용자가 로그인한 루트 디렉터리의 `.ssh` 디렉터리에 있습니다.
* 대상이 `ftp.omniture.com`이 아닙니다. Adobe 내부 서버 간의 SFTP 프로토콜은 지원되지 않습니다.
* 대상이 단일 (PKI) 인증을 지원합니다. 두 가지 요인으로 인한 문제가 있는 경우 보고서 배달이 실패합니다. 서버가 이중 인증을 시도하도록 구성되지 않았는지 확인합니다. Adobe Analytics은 로그인하는 데 키만 사용하고 다른 항목은 사용하지 않아야 합니다.
* Adobe는 SSHv2 암호화를 지원하며, SSHv1 (RSA 키만)로 돌아갑니다.

SFTP를 통해 Data Warehouse 요청을 성공적으로 전송하려면:

1. 문서 [Data Warehouse 요청에 대한 보고서 대상 구성](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)의 [SFTP](/help/export/data-warehouse/create-request/dw-request-report-destinations.md#sftp)에 설명된 단계를 완료하고 공개 키 다운로드를 포함합니다.
1. Data Warehouse 요청에 사용된 자격 증명으로 SFTP 사이트에 로그인합니다.
1. 루트 디렉터리에서 `.ssh` 폴더 (이 폴더가 없는 경우 만들기)로 이동하여 이 폴더에 `authorized_keys` 파일을 저장합니다.

1. [Data Warehouse 요청에 대한 보고서 대상 구성](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)에 설명된 대로 아직 완료하지 않았다면 Data Warehouse 요청을 완료하십시오.
