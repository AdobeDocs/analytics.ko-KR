---
description: 분류(SAINT) FTP 선택 사항은 여러 보고서 세트로 데이터를 업로드하고 50,000개 이상의 행이 있는 데이터 세트를 업로드하는 기능을 포함하여 큰 분류 데이터 세트를 융통성 있게 업로드하도록 해 줍니다.
keywords: ftp; Sftp
seo-description: 분류(SAINT) FTP 선택 사항은 여러 보고서 세트로 데이터를 업로드하고 50,000개 이상의 행이 있는 데이터 세트를 업로드하는 기능을 포함하여 큰 분류 데이터 세트를 융통성 있게 업로드하도록 해 줍니다.
seo-title: 분류
solution: Analytics
title: 분류
uuid: 35936 c 98-b 785-43 eb -89 f 4-ab 42 a 10 db 256
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 분류

분류 FTP 옵션은 데이터를 여러 보고서 세트로 업로드하고 50,000 개 이상의 행이 있는 데이터 세트를 업로드할 수 있는 기능을 포함하여 큰 분류 데이터 세트를 업로드하는 데 더 많은 유연성을 제공합니다.

FTP를 통해 분류 데이터를 다운로드하는 방법 및 FTP를 통해 데이터 파일을 업로드하는 방법에 대한 단계(FTP 계정을 만드는 단계 포함)에 대해서는 [분류](https://marketing.adobe.com/resources/help/en_US/reference/c_working_with_saint.html)를 참조하십시오.

시스템에서 이러한 파일을 가져오는 데 필요한 시간은 여러 가지 요인에 따라 다릅니다. 업로드한 파일이 6시간이 지난 후에도 여전히 FTP 서버에 있는 경우 조직의 지원 사용자와 함께 Adobe 고객 지원 팀에 문의하십시오.

가져오기가 성공하면 내보내기에 적절한 변경 사항이 바로 표시되지만 Analytics의 데이터 변경 사항은 브라우저 가져오기에 최대 4시간, FTP 가져오기에 최대 24시간이 걸릴 수 있습니다.

FTP 제한 및 데이터 유지에 대한 자세한 내용은 [FTP 제한 및 데이터 유지](../../../export/ftp-and-sftp/ftp-limits.md#concept_8CAA1D8F27B3411AB902520AD6C9A70E)를 참조하십시오.

## 분류 및 Data Sources에 대한 .fin 파일 업로드 정보 {#section_1484719F8A134EAE91212DBD8F15174F}

When you upload a classification or [!UICONTROL Data Source] file ( [!DNL .tab]or [!DNL .txt]) the upload also requires that you upload an empty file with the exact same name as the data file being imported, but with a [!DNL .fin] extension. This [!DNL .fin] file is a finish file. 이 파일의 목적은 시스템에 데이터 파일이 FTP 계정에 완전히 업로드되었다는 것을 알리는 것입니다. The [!DNL .fin] file lets Adobe recognize that you are done with your import. 이 파일을 제출하면 Adobe가 두 파일을 FTP에서 제거하고 가져오기를 시작합니다.
파일 가져오기: [!DNL Classifications.tab]

Finish File: [!DNL Classifications.fin]

If you upload your Data Sources or classification file without an accompanying [!DNL .fin] file, Adobe does not add it to the queue for processing. The file remains on the FTP, and is not applied to your data in the [!UICONTROL Experience Cloud]. 이에 대한 알림은 이메일 주소를 Analytics의 [!UICONTROL FTP 계정 만들기] 창에서 [!UICONTROL 알림 수신자]로 입력한 경우에만 받습니다. 이 필드에 이메일 주소를 입력하지 않은 경우 알림이 전송되지 않습니다.

If you do upload your file with a [!DNL .fin] file, but there is an error in the file, it is submitted for processing, but the error causes the processing to cease and the file to be sent to an error folder. 이 경우 알림이 [!UICONTROL FTP 계정 만들기] 창의 [!UICONTROL 알림 수신자] 필드에 나열된 이메일 주소로 전송됩니다. 이메일 주소를 입력하지 않은 경우 알림이 전송되지 않습니다.
