---
description: 데이터 피드는 표준 및 사용자 지정 데이터 피드를 모두 제공하는 Adobe로부터 받은 클릭스트림 데이터의 내보내기입니다.
keywords: ftp; Sftp
seo-description: 데이터 피드는 표준 및 사용자 지정 데이터 피드를 모두 제공하는 Adobe로부터 받은 클릭스트림 데이터의 내보내기입니다.
seo-title: 데이터 피드
solution: Analytics
title: 데이터 피드
uuid: 3 C 70 EEA 3-CA 59-4 AA 5-9 B 11-64 E 1 BB 677 BFA
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 데이터 피드

데이터 피드는 표준 및 사용자 지정 [데이터 피드](/help/export/analytics-data-feed/c-getstarted/data-feed-overview.md)를 모두 제공하는 Adobe로부터 받은 클릭스트림 데이터의 내보내기입니다.

If you have purchased Adobe Data Warehouse, [!UICONTROL Standard Data Feeds] you can set up your own Analytics data feeds. 이러한 데이터 피드는 FTP 계정(Adobe에서 설정한 계정 또는 외부 FTP에서 설정한 계정)으로 보낼 수 있습니다. Adobe 엔지니어링 서비스는 임의 방법을 통해 가상으로 보낼 수 있는 사용자 지정 [!UICONTROL 데이터 피드]를 제공합니다.

[!UICONTROL 데이터 피드 ]FTP 계정은 2GB 또는 63개 파일(기본값)을 허용합니다. 다른 모든 표준 FTP 계정은 기본적으로 50MB입니다. 클라이언트가 의도한 적절한 용도에 FTP 계정을 사용하는 경우 트래픽 양이 많은 일부 사용자가 이러한 계정을 빠르게 채울 수 있습니다. FTP 계정이 꽉 차면 추가 파일을 푸시할 수 없습니다. 따라서 이 FTP 계정으로 배달되는 파일([!UICONTROL 데이터 피드], 데이터 웨어하우스 요청 등)은 배달되지 않습니다. 받은 파일과 다운로드한 파일을 제거하여 Adobe FTP 계정을 관리하는 것이 중요한 한 가지 이유가 이 때문입니다.

FTP 계정이 꽉 차면 현재 파일을 다운로드하고 제거해야 하며 Adobe에 공간이 지워졌다는 것을 알려야 합니다. 그러면 Adobe가 배달되지 않은 파일을 다시 보낼 수 있습니다. 데이터 웨어하우스와 같은 일부 도구를 사용하여 사용자가 이러한 파일을 다시 보낼 수 있습니다. 다시 보내는 데 Adobe가 참여하지 않아도 됩니다. FTP 계정이 자주 채워지는 것처럼 보이면 늘린 FTP 공간 및 파일 개수 할당량을 계정에 포함할 수 있는 배달 대체 항목을 제안할 수 있는 Adobe 고객 지원 팀에 문의하십시오.

FTP 제한 및 데이터 유지에 대한 자세한 내용은 [FTP 제한 및 데이터 유지](../../../export/ftp-and-sftp/ftp-limits.md#concept_8CAA1D8F27B3411AB902520AD6C9A70E)를 참조하십시오.
