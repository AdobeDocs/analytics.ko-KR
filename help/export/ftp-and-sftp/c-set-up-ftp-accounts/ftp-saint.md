---
description: 분류(SAINT) FTP 선택 사항은 여러 보고서 세트로 데이터를 업로드하고 50,000개 이상의 행이 있는 데이터 세트를 업로드하는 기능을 포함하여 큰 분류 데이터 세트를 융통성 있게 업로드하도록 해 줍니다.
keywords: ftp;sftp
title: 분류
uuid: 35936c98-b785-43eb-89f4-ab42a10db256
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8

---


# 분류

분류 FTP 옵션은 여러 보고서 세트로 데이터를 업로드하고 50,000개 이상의 행이 있는 데이터 세트를 업로드하는 기능을 포함하여 큰 분류 데이터 세트를 융통성 있게 업로드하도록 해 줍니다.

FTP를 통해 분류 데이터를 다운로드하는 방법 및 FTP를 통해 데이터 파일을 업로드하는 방법에 대한 단계(FTP 계정을 만드는 단계 포함)에 대해서는 [분류](https://docs.adobe.com/content/help/en/analytics/components/classifications/classifications-importer/c-working-with-saint.html)를 참조하십시오.

시스템에서 이러한 파일을 가져오는 데 필요한 시간은 여러 가지 요인에 따라 다릅니다. 업로드한 파일이 6시간이 지난 후에도 여전히 FTP 서버에 있는 경우 조직의 지원 사용자와 함께 Adobe 고객 지원 팀에 문의하십시오.

가져오기가 성공하면 내보내기에 적절한 변경 사항이 바로 표시되지만 Analytics의 데이터 변경 사항은 브라우저 가져오기에 최대 4시간, FTP 가져오기에 최대 24시간이 걸릴 수 있습니다.

FTP 제한 및 데이터 유지에 대한 자세한 내용은 [FTP 제한 및 데이터 유지](/help/export/ftp-and-sftp/ftp-limits.md)를 참조하십시오.

## 분류 및 데이터 소스에 대한 .fin 파일 업로드 정보 {#section_1484719F8A134EAE91212DBD8F15174F}

When you upload a classification or [!UICONTROL Data Source] file ( [!DNL .tab]or [!DNL .txt]) the upload also requires that you upload an empty file with the exact same name as the data file being imported, but with a [!DNL .fin] extension. 이 [!DNL .fin] 파일은 완료한 파일입니다. 이 파일의 목적은 시스템에 데이터 파일이 FTP 계정에 완전히 업로드되었음을 알리는 것입니다. [!DNL .fin] 파일을 사용하면 사용자가 가져오기를 완료했음을 Adobe에서 인식할 수 있습니다. 이 파일을 제출하면 Adobe가 두 파일을 FTP에서 제거하고 가져오기를 시작합니다.
파일 가져오기: [!DNL Classifications.tab]

완료 파일: [!DNL Classifications.fin]

[!DNL .fin] 파일 없이 데이터 소스 또는 분류 파일을 업로드하면 Adobe가 처리를 위해 해당 파일을 큐에 추가하지 않습니다. 이 파일은 FTP에 남아 있으며 [!UICONTROL Experience Cloud]의 데이터에 적용되지 않습니다. You are notified of this only if you have entered your email address as the [!UICONTROL Notification Recipient] in the [!UICONTROL Create FTP Account] window of Analytics. 이 필드에 이메일 주소를 입력하지 않은 경우 알림이 전송되지 않습니다.

이 파일을 [!DNL .fin] 파일과 함께 업로드하면 파일에 오류가 있는 경우 처리를 위해 제출되지만 오류로 인해 처리가 중지되고 파일이 오류 폴더로 전송됩니다. If this occurs, a notification is sent to the email address listed in the [!UICONTROL Notification Recipient] field in the [!UICONTROL Create FTP Account] window. 이메일 주소를 입력하지 않은 경우 알림이 전송되지 않습니다.
