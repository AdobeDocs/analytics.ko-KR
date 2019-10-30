---
description: Analytics 사용자의 기존 로그인을 비활성화하는 방법에 대해 알아봅니다.
seo-description: Analytics 사용자의 기존 로그인을 비활성화하는 방법에 대해 알아봅니다.
seo-title: 기존 로그인 비활성화
title: 기존 로그인 비활성화
uuid: 085874b2-1 파섹
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# 기존 로그인 비활성화{#disable-legacy-logins}

Analytics 사용자의 기존 로그인을 비활성화하는 방법에 대해 알아봅니다.

사용자가 기존 Analytics 사용자 관리 시스템에서 Adobe Admin Console로 마이그레이션하면 기존 로그인의 사용을 중지시킬 수 있습니다. 기존 로그인을 사용하지 않도록 설정하면 사용자가 기존 로그인을 사용하려고 시도하는 경우 Experience Cloud 로그인으로 리디렉션됩니다.

1. Open the Migration tool in **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL User ID Migration]**.
1. In the [!DNL User Information] section, locate the domain containing the users you want to work with, then click **[!UICONTROL Select Users]**.
1. 비활성화할 이전 로그인을 사용하는 사용자를 선택합니다.

   ![](assets/user-info.png)

   자격이 있는 사용자는 [마이그레이션 상태] 열 *`Migrated`* 아래에 상태가 됩니다. 마이그레이션되기 전까지는 사용자의 기존 로그인을 비활성화할 수 없습니다.
1. Click **[!UICONTROL Disable Legacy Login]**, then click **[!UICONTROL Done]**.

   기존 로그인을 비활성화하는 것은 사용자가 기존의 [!DNL my.omniture.com] 사용자 이름 및 암호를 계속 사용할 수 있음을 나타냅니다.

   아직 마이그레이션되지 않은 사용자의 기존 로그인은 비활성화할 수 없습니다. 비활성화하면 사용자가 Experience Cloud ID를 사용하여 Analytics에 로그인 및 액세스해야 합니다.

