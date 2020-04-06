---
description: FTP를 통해 데이터 파일을 업로드하는 방법을 설명하는 단계입니다.
subtopic: Classifications
title: FTP 가져오기
topic: Admin tools
uuid: a914970d-ba02-4111-9dcf-06448f71b9f3
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# FTP 가져오기

FTP를 통해 데이터 파일을 업로드하는 방법을 설명하는 단계입니다.

## FTP 가져오기 {#concept_2F965BE873254546A61FB755F25299FD}

FTP를 통해 데이터 파일을 업로드하는 방법을 설명하는 단계입니다.

**[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.

다음 권장 제한은 중요합니다.

* 작은 파일이 많으면 적은 수의 큰 파일보다 처리 속도가 느립니다. 이는 더 작은 작업에 필요한 큐 및 우선 순위의 크기 때문입니다.
* 큰 파일을 50MB의 청크로 나누십시오. 이는 필수는 아니지만, 백엔드에서 진행 중인 상태를 더 잘 볼 수 있도록 하기 때문에 권장됩니다. 또한 작업을 처리하는 동안 오류가 발생하는 경우 작업이 다시 시작됩니다.이 시나리오에서는 큰 파일이 있으면 많은 양의 작업이 다시 수행됩니다.

초기 설정은 몇 개의 행을 재분류하거나 행을 추가하는 대신 분류 데이터베이스를 큰 원본 데이터 세트로 채우거나 분류를 다시 구성합니다.

보고서 세트의 초기 업로드(지정된 변수 또는 보고서의 경우)에 따라 후속 가져오기에서 새 행과 업데이트된 행만 업로드하는 것이 좋습니다. 변경되지 않는 행은 향후 업로드에서 생략되어야 합니다.

업로드하는 새로운 각 키 값이 해당 월의 고유 수에 대해 카운트됩니다.

월 고유 수를 초과한 경우, 보고에서 고유 수가 초과된 값에 대한 해당 분류 데이터가 표시되지 않습니다. 데이터 웨어하우스 또는 애드혹 분석에서 이러한 분류를 볼 수 있습니다.

>[!NOTE] 분류 데이터 파일을 처리하는 데 필요한 시간은 파일 크기와 Adobe 서버에서 미리 처리되는 파일의 현재 수에 따라 다릅니다. 일반적으로 데이터 파일을 처리하는 데 72시간이 걸립니다.

FTP를 통해 데이터를 업로드하기 전에 FTP 계정을 만듭니다. 자세한 내용은 [FTP 계정 만들기](/help/components/c-classifications2/c-classifications-importer/c-uploading-saint-data-files-via-ftp.md#task_C019268E6C934C7C95F4326F42A22CCF)를 참조하십시오.

## FTP를 통해 분류 가져오기 {#task_132C36830B69418B8C929E39838EF01D}

<!-- 

t_upload_a_saint_data_file_via_ftp.xml

 -->

FTP 계정을 사용하여 분류를 Adobe Analytics로 가져오는 방법을 설명하는 단계입니다.

FTP 계정 만들기에 대한 자세한 내용은 FTP [계정](/help/components/c-classifications2/c-classifications-importer/c-uploading-saint-data-files-via-ftp.md#task_C019268E6C934C7C95F4326F42A22CCF)만들기를 참조하십시오.

1. 클릭 **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. 을 **[!UICONTROL Import File]**&#x200B;클릭한 다음 을 클릭합니다 **[!UICONTROL FTP Import]**.
1. Next to the FTP account that you want to use, click **[!UICONTROL View]**.
1. FTP 액세스 정보(호스트, 로그인, 암호)를 사용하여 선택하려는 FTP 클라이언트를 사용하는 FTP 서버에 액세스합니다.
1. 데이터 파일([!DNL .tab] 또는 [!DNL .txt])을 FTP 서버에 업로드합니다.
1. 데이터 파일을 업로드한 후 파일이 처리할 준비가 되었음을 나타내는 FIN 파일을 업로드합니다.

   FIN 파일은 데이터 파일과 같은 이름을 가지는 비어 있는 파일이며 파일 확장명은 [!DNL .fin]입니다. 예를 들어 데이터 파일이 [!DNL classdata1.tab]인 경우 FIN 파일 이름은 [!DNL classdata1.fin]입니다.

Adobe는 FIN 파일과 연관된 업로드된 데이터 파일을 정기적으로 검색합니다. Adobe는 FTP 계정 구성에 지정된 보고서 세트와 데이터 세트로 가져옵니다.

## FTP 계정 만들기를 참조하십시오.{#task_C019268E6C934C7C95F4326F42A22CCF}

FTP를 통해 데이터를 업로드하기 전에 FTP 계정을 만듭니다. >

<!-- 

t_create_an_ftp_account.xml

 -->

Adobe FTP 서버에 대한 추가 내용은 [FTP 및 sFTP](https://marketing.adobe.com/resources/help/ko_KR/whitepapers/ftp/)를 참조하십시오.

1. 클릭 **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. 을 **[!UICONTROL Import File]**&#x200B;클릭한 다음 을 클릭합니다 **[!UICONTROL FTP Import]**.
1. 탭에서 을 **[!UICONTROL Import File]** 클릭합니다 **[!UICONTROL Add New]**.
1.  FTP 계정 세부 사항을 지정합니다. 

   | 요소 | 설명 |
   |---|---|
   |  이름  | FTP 계정 이름입니다. |
   | 분류할 데이터 세트 | 드롭다운 목록에서 분류할 데이터 세트(마케팅 보고서 변수)를 선택합니다. |
   | 보고서 세트 선택 | 선택한 데이터 세트를 분류할 보고서 세트를 선택합니다. 여러 보고서 세트를 선택하려면 선택한 각 보고서 세트에 대한 분류가 동일해야 합니다. |
   | 충돌 시 데이터 덮어쓰기 | 중복 데이터를 덮어쓰려면 이 옵션을 선택합니다. 이 옵션은 기존 분류를 업데이트하는 경우에 유용합니다. 분류를 추가하는 경우에는 이 옵션을 사용하지 않는 것이 좋습니다. |
   | 가져오기 완료 후 | 가져오기가 완료된 후 이 FTP 계정에 대한 알림을 수신할 이메일 주소를 지정한 후 업데이트된 데이터 세트를 동일한 FTP 계정으로 자동으로 내보내려면 이 옵션을 선택합니다. |
   | 알림 수신자 | 이 FTP 계정에 대한 알림을 수신할 이메일 주소를 지정합니다. |
   | 승인 | (필수) Adobe가 새 FTP 계정으로 보낸 모든 데이터 파일을 자동으로 가져오도록 승인합니다. |

1. 클릭 **[!UICONTROL Save]**.

만든 후에, 원하는 FTP 계정 옆의 해당하는 링크를 클릭하여 FTP 계정을 편집하거나 삭제합니다.
