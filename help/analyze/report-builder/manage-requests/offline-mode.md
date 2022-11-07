---
description: 오프라인 모드는 요청을 만들고 편집하는 과정을 가속하는 자리 표시자 데이터를 반환합니다.
title: 요청을 만들고 편집하기 위한 오프라인 모드
uuid: 4eb1f754-b6da-4896-a64f-b737563925b8
feature: Report Builder
role: User, Admin
exl-id: f18859e3-19e4-48af-963f-0bb4d1b46380
source-git-commit: 25eccb2b9fe3827e62b0ae98d9bebf7a97b239f5
workflow-type: ht
source-wordcount: '201'
ht-degree: 100%

---

# 요청을 만들고 편집하기 위한 오프라인 모드

오프라인 모드는 요청을 만들고 편집하는 과정을 가속하는 자리 표시자 데이터를 반환합니다.

새 요청을 만들거나 편집할 때 응답을 가져오기 위한 보고서 API 호출이 수행됩니다. 이 경우 다음 단계로 이동하기 전에 데이터가 반환되기 기다려야 하므로 요청 생성 프로세스가 느려집니다. 오프라인 모드는 자리 표시자 데이터만 반환하므로 API 호출이 수행될 필요가 없습니다.

오프라인 모드를 활성화하려면

1. Report Builder 메뉴에서 **[!UICONTROL 옵션]**&#x200B;을 클릭합니다.

   ![오프라인 모드](assets/offline_mode.png)

1. **[!UICONTROL 요청 생성 및 편집을 위한 오프라인 모드를 켭니다.]** 옆의 확인란을 선택합니다.
1. **[!UICONTROL 지표 데이터를 다음으로 표시]** 필드에 요청에서 반환하려는 자리 표시자 데이터를 입력합니다. 예를 들어 &quot;1&quot;을 입력합니다.
1. **[!UICONTROL 확인]**&#x200B;을 클릭합니다.
1. 이제 요청 마법사를 사용하여 오프라인 모드에서 요청을 만들고 실행합니다.
1. 자리 표시자로 &quot;1&quot;을 지정하면 요청이 다음과 같이 표시됩니다.

   ![오프라인 모드 예](assets/offline_mode_example.png)

   >[!IMPORTANT]
   >
   >실제 데이터로 요청을 실행하려면 먼저 오프라인 모드를 비활성화해야 합니다. 이렇게 하려면 **[!UICONTROL 옵션]**&#x200B;으로 가서 확인 표시를 제거합니다.
