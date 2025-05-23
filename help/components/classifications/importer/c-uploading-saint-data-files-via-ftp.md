---
description: FTP를 통해 데이터 파일을 업로드하는 방법.
title: FTP 가져오기
feature: Classifications
exl-id: 3e93b35c-6f65-4a93-887d-d94e4d359bdc
source-git-commit: a40f30bbe8fdbf98862c4c9a05341fb63962cdd1
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 90%

---

# FTP 가져오기(이전)

>[!IMPORTANT]
>
>Adobe에서는 이 페이지에 설명된 대로 FTP를 사용하여 가져오기를 더 이상 권장하지 않습니다.
>
>FTP는 파일을 공유하는 암호화되지 않은 방법이므로 권장하지 않습니다. 즉, 계정에 사용되는 사용자 이름과 암호뿐만 아니라 파일 내용을 누구든지 가로챌 수 있습니다.
>
>대신 [클라우드 가져오기 및 내보내기 계정 구성](/help/components/locations/configure-import-accounts.md)에 설명된 대로 클라우드 계정을 구성하십시오.

FTP를 통해 데이터 파일을 업로드하는 방법을 설명하는 단계입니다.

## FTP 가져오기 {#concept_2F965BE873254546A61FB755F25299FD}

FTP를 통해 데이터 파일을 업로드하려면 다음 작업을 수행합니다.

1. **[!UICONTROL 관리]** > **[!UICONTROL 분류 가져오기]**

다음과 같은 권장 제한이 중요합니다.

>[!IMPORTANT]
>
>작은 파일이 너무 많거나 하나의 큰 파일이 있으면 처리 서버에 불필요한 처리 부하가 발생할 수 있습니다. 큰 파일을 50개의 MB 단위 청크로 분할하고 작은 파일은 함께 결합하는 것이 좋습니다.

초기 설정은 몇 개의 행을 재분류하거나 행을 추가하는 것이 아니라 분류 데이터베이스를 큰 원본 데이터 세트로 채우거나 분류를 재구성합니다.

Adobe에서는 보고서 세트에서 특정 변수나 보고서에 대해 초기 업로드를 수행한 이후 가져오기에서는 새 행과 업데이트된 행만 업로드하도록 권장합니다. 변경되지 않는 행은 향후 업로드에서 생략되어야 합니다.

업로드한 새로운 키 값은 월 해당 변수의 고유 수에 대해 카운트합니다.

월 고유 수를 초과하는 경우, 초과한 고유 값에 해당하는 분류 데이터는 보고에 표시되지 않습니다. Data Warehouse에서 이러한 분류를 확인할 수 있습니다.

>[!NOTE]
>
>분류 데이터 파일을 처리하는 데 필요한 시간은 파일 크기와 Adobe 서버에서 미리 처리되는 파일의 현재 수에 따라 다릅니다. 데이터 파일 처리에 걸리는 시간은 보통 72시간 이내입니다.

## FTP 계정 만들기를 참조하십시오.

FTP를 통해 데이터를 업로드하기 전에 FTP 계정을 만듭니다. >

Adobe FTP 서버에 대한 추가 내용은 [FTP 및 sFTP](/help/export/ftp-and-sftp/ftp-overview.md)를 참조하십시오.

1. **[!UICONTROL 관리자]** > **[!UICONTROL 분류 가져오기]**&#x200B;를 클릭합니다.
1. **[!UICONTROL 파일 가져오기]**&#x200B;를 클릭한 다음 **[!UICONTROL FTP 가져오기]**&#x200B;를 클릭합니다.
1. **[!UICONTROL 파일 가져오기]** 탭에서 **[!UICONTROL 새로 추가]**&#x200B;를 클릭합니다.
1. FTP 계정 세부 사항을 지정합니다.

   | 요소 | 설명 |
   |---|---|
   | **이름** | FTP 계정 이름입니다. |
   | **분류할 데이터 세트** | 드롭다운 목록에서 분류할 데이터 세트(마케팅 보고서 변수)를 선택합니다. |
   | **보고서 세트 선택** | 선택한 데이터 세트를 분류하려는 보고서 세트를 선택합니다. 여러 개의 보고서 세트를 선택하려면 선택한 보고서 세트의 각 분류가 일치해야 합니다. |
   | **충돌 시 데이터 덮어쓰기** | 이 옵션을 선택하여 중복 데이터를 덮어씁니다. 이 옵션은 기존의 분류를 업로드하려는 경우에 유용합니다. [최신 분류 아키텍처](../sets/overview.md)를 사용하는 경우 이 설정은 항상 활성화되어 있습니다. |
   | **가져오기가 완료된 이후** | 가져오기가 완료된 이후 이 FTP 계정에 관한 알림을 받을 수 있도록 이메일 주소를 지정한 경우 이 옵션을 선택하면 업데이트된 데이터 세트를 동일한 FTP 계정으로 자동으로 내보냅니다. [최신 분류 아키텍처](../sets/overview.md)를 사용하는 경우에는 이 옵션을 사용할 수 없습니다. |
   | **알림 수신자** | 이 FTP 계정에 대한 알림을 수신할 이메일 주소를 지정합니다. |
   | **승인** | (필수) Adobe에서 새로운 FTP 계정에 보낸 모든 데이터 파일을 자동으로 가져오도록 허가합니다. |

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

만든 후에, 원하는 FTP 계정 옆의 해당하는 링크를 클릭하여 FTP 계정을 편집하거나 삭제합니다.

>[!NOTE]
>
>가져오기로 인해 분류가 변경되지 않으면 알림이 전송되지 않습니다. 이메일은 성공한 경우와 분류가 변경된 경우에만 전송됩니다.

## FTP를 통해 분류 가져오기

FTP 계정을 사용하여 Adobe Analytics로 분류를 가져올 수 있습니다.

FTP를 통해 분류를 가져오려면 다음 작업을 수행합니다.

1. **[!UICONTROL 관리자]** > **[!UICONTROL 분류 가져오기]**&#x200B;를 클릭합니다.
1. **[!UICONTROL 파일 가져오기]**&#x200B;를 클릭한 다음 **[!UICONTROL FTP 가져오기]**&#x200B;를 클릭합니다.
1. 사용하려는 FTP 계정 옆의 **[!UICONTROL 보기]**&#x200B;를 클릭합니다.
1. FTP 액세스 정보 (호스트, 로그인, 암호)를 사용하여 선택하려는 FTP 클라이언트를 사용하는 FTP 서버에 액세스합니다.
1. 데이터 파일 (`.tab` 또는 `.txt`)을 FTP 서버에 업로드합니다.
1. 데이터 파일을 업로드한 후 파일이 처리할 준비가 되었음을 나타내는 FIN 파일을 업로드합니다.

   FIN 파일은 데이터 파일과 같은 이름을 가지는 비어 있는 파일이며 파일 확장명은 `.fin`입니다. 예를 들어 데이터 파일이 `classdata1.tab`인 경우 FIN 파일 이름은 `classdata1.fin`입니다.

Adobe는 FIN 파일과 연관된 업로드한 데이터 파일을 정기적으로 검색합니다. Adobe는 검색한 파일을 FTP 계정 구성에 지정된 보고서 세트와 데이터 세트로 내보냅니다.

Adobe Analytics가 FTP 폴더에 업로드된 파일을 읽고 처리하면 파일이 FTP 사이트에서 자동으로 제거됩니다.
