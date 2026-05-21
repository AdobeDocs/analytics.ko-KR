---
description: 포함된 요청과 함께 보고서를 저장하는 방법에 대해 알아봅니다.
title: 요청이 있는 통합 문서 저장 기본 정보
uuid: 31611031-0982-4124-9fc7-7888124aa603
feature: Report Builder
role: User, Admin
exl-id: 192ac2f6-cfb8-447b-8fc1-19ad786ef924
TQID: https://experienceleague.adobe.com/0UMDDWbeilsUp-yB-tzMVcWkGfUXtf4lh2ciaAg4AEk
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2: id: ac8a38fa-dec3-4581-8f64-178fde9f64e8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 276
ht-degree: 31%

---

# 요청이 있는 통합 문서 저장

{{legacy-arb}}

포함된 요청이 있는 보고서를 만들 때 Excel에서 **파일** > **저장** 또는 **파일** > **다른 이름으로 저장**&#x200B;을 사용하여 저장할 수 있습니다. Report Builder은 보고서에 요청이 포함되어 있는지 여부를 감지합니다. 저장 옵션 중 하나를 선택하면 **다른 이름으로 통합 문서 저장** 양식을 작성합니다.

* Windows 응용 프로그램을 사용하는 광범위한 작업을 위한 우수 사례로서, Adobe에서는 워크시트에서 예기치 않은 요청 손실을 방지하기 위해 요청을 스프레드시트에 자주 정기적으로 저장하는 것이 좋습니다.
* 통합 문서의 이름을 지정할 때 작업 기록을 유지할 수 있도록 파일 이름에 버전 번호를 사용하는 것이 좋습니다. 예를 들어, 첫 번째 통합 문서의 이름은 [!DNL web_forecast_01_01.xlsx]로 지정할 수 있습니다.
* 보고서를 이미 저장한 경우 보고서를 다시 저장할 때 [!UICONTROL 템플릿 저장] 양식이 표시되지 않습니다. 보고서에 요청이 들어 있지 않으면 이 대화 상자가 표시되지 않습니다. 대신 표준 Excel [!UICONTROL 다른 이름으로 저장] 양식이 표시됩니다.

## 파일 이름 및 위치 {#section_2406629E9B644CE08430826948977D5D}

[!UICONTROL 템플릿 저장] 양식에는 기존의 [!DNL .xls] 파일 확장명을 사용하여 스프레드시트의 파일 이름을 입력하도록 하는 텍스트 상자와 같이, Excel의 [!UICONTROL 파일] > [!UICONTROL 다른 이름으로 저장] 대화 상자와 동일한 기능이 일부 있습니다.

사용하는 모든 파일 이름은 255자 이하여야 합니다. 또한 파일 이름에는 다음 문자가 포함되지 않을 수 있습니다.

\ ? | > &lt; : / &#42; &#39; &quot;

마지막으로, 확장 ASCII 문자 집합 외의 유니코드 문자는 사용할 수 없습니다.

파일을 로컬 드라이브나 네트워크 드라이브에 저장할 때 텍스트 상자에 전체 경로를 입력하거나 [!UICONTROL 다른 이름으로 저장] 텍스트 상자 근처에 있는 찾아보기 단추 ![browse_button.gif](assets/browse_button.gif)를 클릭합니다.
