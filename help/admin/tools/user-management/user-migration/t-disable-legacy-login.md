---
description: Analytics 사용자의 기존 로그인을 비활성화하는 방법에 대해 알아봅니다.
title: 기존 로그인 비활성화
feature: Admin Tools
exl-id: 3e619700-722d-429b-94dc-7aa162e114c0
role: Admin
TQID: https://experienceleague.adobe.com/xwLXKuaeoKB5-TSVC7FLQXdUsBEeOg-zuITMa8Z3OIo
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 7d733a6375f6c6009563bc53f5a3ff090dbc48ed
workflow-type: tm+mt
source-wordcount: 185
ht-degree: 52%

---

# 기존 로그인 비활성화

Analytics 사용자의 기존 로그인을 비활성화하는 방법에 대해 알아봅니다.

사용자가 기존 Analytics 사용자 관리 시스템에서 Adobe Admin Console으로 마이그레이션한 후 기존 로그인을 비활성화할 수 있습니다. 기존 로그인을 비활성화하면 사용자가 기존 로그인을 사용하려는 경우 CX 엔터프라이즈 로그인으로 리디렉션됩니다.

1. **[!UICONTROL Analytics]** > **[!UICONTROL 관리]** > **[!UICONTROL 사용자 ID 마이그레이션]**&#x200B;에서 마이그레이션 도구를 엽니다.
1. [!DNL User Information] 섹션에서 함께 작업할 사용자가 포함된 도메인을 찾은 다음 **[!UICONTROL 사용자 선택]**&#x200B;을 클릭합니다.
1. 비활성화할 기존 로그인을 사용하는 사용자를 선택합니다.

   ![](/help/admin/tools/user-management/user-migration/assets/user-info.png)

   자격이 있는 사용자는 마이그레이션 상태 열 아래에 *`Migrated`* 상태가 표시됩니다. 마이그레이션되기 전까지는 사용자의 기존 로그인을 비활성화할 수 없습니다.
1. **[!UICONTROL 기존 로그인 비활성화]**&#x200B;를 클릭한 다음 **[!UICONTROL 완료]**&#x200B;를 클릭합니다.

   기존 로그인을 비활성화하는 것은 사용자가 기존의 [!DNL my.omniture.com] 사용자 이름 및 암호를 계속 사용할 수 있음을 나타냅니다.

   아직 마이그레이션되지 않은 사용자의 기존 로그인을 비활성화할 수 없습니다. 비활성화되면 사용자는 Experience Cloud ID를 사용하여 Analytics에 로그인하고 액세스해야 합니다.
