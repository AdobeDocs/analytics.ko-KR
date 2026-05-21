---
description: 데이터 피드는 표준 및 사용자 지정 데이터 피드를 모두 제공하는 Adobe로부터 받은 클릭스트림 데이터의 내보내기입니다.
keywords: ftp, sftp
title: 데이터 피드
feature: FTP Export
exl-id: 286050fa-e197-4b70-b167-da6921615c1b
TQID: https://experienceleague.adobe.com/SWXC-g3KTGuKiT0CBFfptUSBigs8pgkPVdRLzWhl6z4
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 331
ht-degree: 31%

---

# 데이터 피드

>[!NOTE]
>
>다음 정보는 FTP 및 SFTP 대상 유형과 관련되어 있습니다. FTP 및 SFTP는 기존 대상 유형입니다. 데이터 피드를 구성할 때는 보다 안전한 클라우드 대상 유형을 사용해야 합니다. 데이터 피드에 대한 클라우드 대상 형식을 구성하는 방법에 대한 자세한 내용은 [데이터 피드 만들기](/help/export/analytics-data-feed/create-feed.md)를 참조하십시오.

데이터 피드는 표준 및 사용자 지정 [데이터 피드](/help/export/analytics-data-feed/data-feed-overview.md)를 모두 제공하는 Adobe로부터 받은 클릭스트림 데이터의 내보내기입니다.

Adobe Data Warehouse를 구매한 경우 [!UICONTROL 표준 데이터 피드]는 고유한 Analytics 데이터 피드를 설정할 수 있습니다. 이러한 데이터 피드는 FTP 계정 (Adobe에서 설정한 계정 또는 외부 FTP에서 설정한 계정)으로 보낼 수 있습니다. Adobe 엔지니어링 서비스에서는 거의 모든 방법으로 전송할 수 있는 사용자 지정 [!UICONTROL 데이터 피드]를 제공합니다.

[!UICONTROL 데이터 피드] FTP 계정은 10GB(기본값)를 허용합니다. 다른 모든 표준 FTP 계정은 기본적으로 50MB입니다. 클라이언트가 적절한 목적 사용을 위해 FTP 계정을 사용하는 경우 트래픽 양이 많은 일부 사용자가 이러한 계정을 빠르게 채울 수 있습니다. FTP 계정이 꽉 차면 추가 파일을 푸시할 수 없습니다. 따라서 이 FTP 계정으로 배달되는 파일 ([!UICONTROL 데이터 피드], Data Warehouse 요청 등)은 배달되지 않습니다. 이 때문에 받아서 다운로드한 파일을 제거하여 Adobe FTP 계정을 관리하는 것이 중요합니다.

FTP 계정이 꽉 차면 현재 파일을 다운로드하여 제거하고 Adobe에 공간이 지워졌음을 알려야 합니다. 그런 다음 Adobe에서 배달되지 않은 파일을 다시 보낼 수 있습니다. Data Warehouse와 같은 일부 도구를 사용하여 사용자가 이러한 파일을 다시 보낼 수 있습니다. 다시 보내기는 Adobe의 관여가 필요하지 않을 수 있습니다. FTP 계정이 자주 추가되는 것으로 표시되면 Adobe 고객 지원 센터에 문의하여 계정의 FTP 공간 및 파일 번호 할당량을 늘릴 수 있는 게재 대안을 제안할 수 있습니다.
