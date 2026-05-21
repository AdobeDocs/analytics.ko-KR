---
description: 차원 간 흐름을 통해 다양한 차원에서 사용자 경로를 검사하는 방법을 이해합니다.
title: 차원 간 플로우
uuid: 51d08531-1c56-46c7-b505-bd8d5e6aa6c1
feature: Visualizations
role: User, Admin
exl-id: f84917a4-2c07-48fb-9af3-d96c537da65c
TQID: https://experienceleague.adobe.com/9OjAFYHo5uhcfbQQOB46jfG1R2wIQCBHXEr842EcZQ0
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2: id: dcae653e-62c6-4cc8-84e6-ee110b848296
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 338
ht-degree: 95%

---

# 차원 간 흐름

차원 간 흐름을 이용하면 다양한 차원에 걸친 사용자 경로를 검사할 수 있습니다.

<!-- 

>[!BEGINSHADEBOX]

See ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Inter-dimensional flows](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/analysis-workspace/analyzing-customer-journeys/text-wrapping-and-multi-dimensional-flow){target="_blank"} for a demo video.

>[!ENDSHADEBOX]

-->

이 문서에서는 모바일 앱 상호작용 및 이벤트 사용 사례에서 이 흐름을 사용하는 방법과 캠페인이 웹 방문을 유도하는 방법을 보여 줍니다.

## 모바일 앱 상호작용 및 이벤트

이 예제 흐름에서는 사용자가 앱의 다양한 화면(장면)을 어떻게 사용하는지 확인하기 위해 [!UICONTROL 화면 이름] 차원을 사용합니다. 반환된 상단 화면은 **[!UICONTROL luma: content: ios: en: home]**&#x200B;로, 앱의 홈 페이지입니다.

![추가된 항목을 보여 주는 플로우.](assets/flowapp.png)

이 앱에서 화면과 이벤트 유형(예: 장바구니에 추가, 구매 등) 간의 상호 작용을 탐색하려면 **[!UICONTROL 이벤트 유형]** 차원을 끌어다 놓습니다.

* 흐름에서 사용 가능한 단계 위에 해당 차원을 대체하려면 다음을 수행합니다.

  ![페이지 차원이 여러 영역으로 드래그되었음을 보여 주는 플로우.](assets/flowapp-replace.png)

* 현재 흐름 시각화 외부에서 차원을 추가하려면 다음을 수행합니다.

  ![페이지 차원이 끝에 있는 빈 공간으로 드래그된 플로우.](assets/flowapp-add.png)

아래의 흐름 시각화는 **[!UICONTROL 이벤트 유형]** 차원을 추가한 결과를 보여 줍니다. 시각화는 모바일 앱 사용자가 장바구니에 제품을 추가하거나 애플리케이션을 종료하고 오퍼를 제시받기 전에 앱의 다양한 화면을 어떻게 이동하는지에 대한 인사이트를 제공합니다.

![목록 상단에 페이지 차원 결과를 보여 주는 플로우.](assets/flowapp-result.png)

## 캠페인이 웹 방문을 유도하는 방법

어떤 캠페인이 웹 사이트 방문을 유도하는지 분석하려고 합니다. **[!UICONTROL 캠페인 이름]**&#x200B;을 차원으로 사용하여 플로우 시각화를 만듭니다.

![플로우 웹 캠페인 이름 차원](assets/flowweb.png)

마지막 **[!UICONTROL 캠페인 이름]** 차원을 **[!UICONTROL 서식이 지정된 페이지 이름]** 차원으로 교체하고 플로우 시각화의 마지막에 다른 **[!UICONTROL 서식이 지정된 페이지 이름]** 차원을 추가합니다.

![Flow web campaign name and web page dimension](assets/flowweb-replace.png)

자세한 내용을 보려면 흐름 위에 마우스를 가져다 댑니다. 예를 들어 어떤 캠페인이 장바구니 결제로 이어졌는지 확인합니다.

![웹 캠페인 이름 및 웹 페이지 차원 호버 플로우](assets/flowweb-hover.png)
