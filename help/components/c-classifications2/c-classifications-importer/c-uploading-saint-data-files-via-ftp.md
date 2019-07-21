---
description: FTP를 통해 데이터 파일을 업로드하는 방법을 설명하는 단계입니다.
seo-description: FTP를 통해 데이터 파일을 업로드하는 방법을 설명하는 단계입니다.
seo-title: FTP 가져오기
solution: Analytics
subtopic: 분류
title: FTP 가져오기
topic: 관리 도구
uuid: a 914970 d-ba 02-4111-9 dcf -06448 f 71 b 9 f 3
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# FTP 가져오기

FTP를 통해 데이터 파일을 업로드하는 방법을 설명하는 단계입니다.

## FTP import {#concept_2F965BE873254546A61FB755F25299FD}

FTP를 통해 데이터 파일을 업로드하는 방법을 설명하는 단계입니다.

**[!UICONTROL 관리]** &gt; **[!UICONTROL 분류 가져오기를]**&#x200B;참조하십시오.

다음 권장 한계를 고려해야 합니다.

* 작은 파일이 많으면 적은 수의 큰 파일이 있을 때보다 처리 속도가 느립니다. 이것은 작은 작업에 필요한 큐 및 우선순위의 양 때문입니다.
* 큰 파일은 50MB씩 자르십시오. 이 작업은 필수는 아니지만, 백엔드에서의 진행 상태를 더 잘 보여주므로 권장됩니다. 또한 Adobe에서 사용자의 작업을 처리하는 동안 오류가 발생하면 작업이 다시 시작됩니다. 이와 같은 상황에서 큰 파일을 사용하면 다시 수행하는 작업의 크기도 커집니다.

초기 설정은 몇 개의 행을 재분류하거나 행을 추가하는 것이 아니라 분류 데이터베이스를 큰 원본 데이터 세트로 채우거나 분류를 재구성합니다.

Adobe에서는 보고서 세트에서 특정 변수나 보고서에 대해 초기 업로드를 수행한 이후 가져오기에서는 새 행과 업데이트된 행만 업로드하도록 권장합니다. 변경되지 않는 행은 향후 업로드에서 생략되어야 합니다.

업로드한 새로운 키 값은 월 해당 변수의 고유 수에 대해 카운트합니다.

월 고유 수를 초과하는 경우, 초과한 고유 값에 해당하는 분류 데이터는 보고에 표시되지 않습니다. Data Warehouse 또는 Ad Hoc Analysis에서 해당 분류를 확인할 수 있습니다.

>[!NOTE]
>
>분류 데이터 파일을 처리하는 데 필요한 시간은 파일 크기와 Adobe 서버에서 이미 처리되는 파일의 현재 수에 따라 다릅니다. 데이터 파일 처리에 걸리는 시간은 보통 72시간 이내입니다.

FTP를 통해 데이터를 업로드하기 전에 FTP 계정을 만듭니다. 자세한 내용은 [FTP 계정 만들기](../../../components/c-classifications2/c-classifications-importer/c-uploading-saint-data-files-via-ftp.md#task_C019268E6C934C7C95F4326F42A22CCF).

## FTP를 통해 분류 가져오기 {#task_132C36830B69418B8C929E39838EF01D}

<!-- 

t_upload_a_saint_data_file_via_ftp.xml

 -->

 FTP 계정을 사용하여 Adobe Analytics로 분류를 가져오는 방법을 설명하는 단계입니다.

FTP 계정 만들기에 대한 자세한 내용은 [FTP 계정 만들기](../../../components/c-classifications2/c-classifications-importer/c-uploading-saint-data-files-via-ftp.md#task_C019268E6C934C7C95F4326F42A22CCF).

1. **[!UICONTROL 관리]** &gt; **[!UICONTROL 분류 가져오기를 클릭합니다]**.
1. Click **[!UICONTROL Import File]**, then click **[!UICONTROL FTP Import]**.
1. Next to the FTP account that you want to use, click **[!UICONTROL View]**.
1. FTP 액세스 정보(호스트, 로그인, 암호)를 사용하여 선택하려는 FTP 클라이언트를 사용하는 FTP 서버에 액세스합니다.
1. Upload the data file ( [!DNL .tab] or [!DNL .txt]) to the FTP server.
1. 데이터 파일을 업로드한 후 파일이 처리할 준비가 되었음을 나타내는 FIN 파일을 업로드합니다.

   The FIN file is an empty file that has the same name as your data file, with a [!DNL .fin] filename extension. For example, if your data file is [!DNL classdata1.tab], the FIN filename is [!DNL classdata1.fin].

Adobe는 FIN 파일과 연관된 업로드한 데이터 파일을 정기적으로 검색합니다. Adobe는 검색한 파일을 FTP 계정 구성에 지정된 보고서 세트와 데이터 세트로 내보냅니다.

## FTP 계정 만들기{#task_C019268E6C934C7C95F4326F42A22CCF}를 참조하십시오 

FTP를 통해 데이터를 업로드하기 전에 FTP 계정을 만듭니다. &gt;

<!-- 

t_create_an_ftp_account.xml

 -->

Adobe FTP 서버에 대한 추가 내용은 [FTP 및 sFTP](https://marketing.adobe.com/resources/help/en_US/whitepapers/ftp/)를 참조하십시오.

1. **[!UICONTROL 관리]** &gt; **[!UICONTROL 분류 가져오기를 클릭합니다]**.
1. Click **[!UICONTROL Import File]**, then click **[!UICONTROL FTP Import]**.
1. **파일 가져오기** 탭에서 **[!UICONTROL 새로 추가를 클릭합니다]**.
1.  FTP 계정 세부 사항을 지정합니다. 

   | 요소 | 설명 |
   |---|---|
   | 이름 | FTP 계정 이름입니다. |
   | 분류할 데이터 세트 | 드롭다운 목록에서 분류할 데이터 세트(마케팅 보고서 변수)를 선택합니다. |
   | 보고서 세트 선택 | 선택한 데이터 세트를 분류하려는 보고서 세트를 선택합니다. 여러 개의 보고서 세트를 선택하려면, 선택한 보고서 세트의 각 분류가 일치해야 합니다. |
   | 충돌 시 데이터 덮어쓰기 | 이 옵션을 선택하여 중복 데이터를 덮어씁니다. 이 옵션은 기존의 분류를 업로드하려는 경우에 유용합니다. 다른 분류를 추가하는 경우에는 이 옵션을 사용하지 않는 것이 좋습니다. |
   | 가져오기가 완료된 이후 | 가져오기가 완료된 이후 이 FTP 계정에 관한 알림을 받을 수 있도록 이메일 주소를 지정한 경우 이 옵션을 선택하면 업데이트된 데이터 세트를 동일한 FTP 계정으로 자동으로 내보냅니다. |
   | 알림 수신자 | 이 FTP 계정에 대한 알림을 수신할 이메일 주소를 지정합니다. |
   | 승인 | (필수) Adobe에서 새로운 FTP 계정에 보낸 모든 데이터 파일을 자동으로 가져오도록 허가합니다. |

1. **[!UICONTROL 저장을 클릭합니다]**.

만든 후에, 원하는 FTP 계정 옆의 해당하는 링크를 클릭하여 FTP 계정을 편집하거나 삭제합니다.
