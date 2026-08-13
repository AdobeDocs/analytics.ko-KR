---
description: 요청이 들어 있는 워크시트에서 셀을 선택하여 날짜 범위를 지정할 수 있습니다. Report Builder는 해당 요청에서 특정 날짜 범위 정보를 사용합니다. 오늘 날짜를 선택하면 요청이 실행되는 시간을 기반으로 한 부분 데이터가 표시됩니다.
title: 셀의 날짜
uuid: 0d9bf08d-d39d-4f37-94f1-232da0813245
feature: Report Builder
role: User, Admin
exl-id: e10573cc-984e-4202-a797-c2c9bec2af96
TQID: https://experienceleague.adobe.com/9-U5bdrNbEahhtBuJA4ylaXzGEgH01q1z7FBR2w5sPs
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 179
ht-degree: 24%

---

# 셀의 날짜

{{legacy-arb}}

요청이 들어 있는 워크시트에서 셀을 선택하여 날짜 범위를 지정할 수 있습니다. Report Builder는 해당 요청에서 특정 날짜 범위 정보를 사용합니다. 오늘 날짜를 선택하면 요청이 실행되는 시간을 기반으로 한 부분 데이터가 표시됩니다.

**셀에서 날짜를 구성하려면**

1. [!UICONTROL 요청 마법사: 1단계]에서, **[!UICONTROL 셀의 날짜]**&#x200B;를 선택합니다.
1. **[!UICONTROL 시작]** 및 **[!UICONTROL 종료]** 필드에 셀 참조를 입력하거나, 선택기를 클릭하고 시작 및 종료 날짜가 있는 요청이 들어 있는 셀을 선택합니다.

   예를 들어 날짜 범위가 &quot;어제&quot;로 설정된 Report Builder 요청을 만들고 동일한 셀의 요청 날짜를 &quot;today()-1&quot;로 출력합니다.

다음은 지원되는 날짜 형식 목록입니다.

![지원되는 날짜 형식을 보여 주는 스크린샷입니다.](assets/date-formats.png)

