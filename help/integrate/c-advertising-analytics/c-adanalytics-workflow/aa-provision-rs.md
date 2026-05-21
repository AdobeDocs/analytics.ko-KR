---
description: Advertising Analytics에서 사용할 CX 엔터프라이즈 매핑 보고서 세트를 구성합니다.
title: Advertising Analytics용 보고서 세트 활성화
feature: Advertising Analytics
exl-id: 3a467e41-2755-46c1-b077-b42946562e6b
TQID: https://experienceleague.adobe.com/sGEXiz2RiDhf9p-2df76o-XxBERTKPB-O-rZeIb4BBI
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: eb9732ab-8232-4b21-bc4c-89de86dbe4d7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: f570a4d2e66c2af8ad85ab097078dd95c574fc83
workflow-type: tm+mt
source-wordcount: 268
ht-degree: 33%

---

# Advertising Analytics용 보고서 세트 활성화

Analytics에서 Advertising Analytics 검색 데이터를 보려면 Advertising Analytics 보고를 위해 각 CX 엔터프라이즈 매핑 보고서 세트를 구성해야 합니다.

1. **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]**&#x200B;로 이동합니다.

1. CX 엔터프라이즈 조직에 매핑된 보고서 세트를 선택합니다.
1. **[!UICONTROL 설정 편집]** > **[!UICONTROL Advertising Analytics 구성]**&#x200B;을 클릭합니다.

   ![보고](assets/aa-reporting.png)

1. Advertising Analytics에 익숙하지 않은 **[!UICONTROL 을(를) 선택하십시오. Advertising Analytics에 대한 자세한 내용을 보려면 여기를 클릭]**&#x200B;하십시오.

1. AMO ID 변수에서 사용할 변수 할당 및 만료를 설정합니다. Adobe Analytics에서 전환 변수 (eVar)를 사용하면 성공 이벤트를 특정 변수 값에 의한 것으로 처리할 수 있습니다. 때때로 변수에서 성공 이벤트를 생성하기 전에 두 개 이상의 값을 받을 수 있습니다. 이러한 경우 할당은 이벤트에 대한 크레딧을 받는 변수 값을 결정합니다.

   | 설정 | 정의 |
   |--- |--- |
   | **[!UICONTROL 할당]** | 다음 중 선택:<br/> **[!UICONTROL 원래 값(첫 번째)]**: 해당 변수에 대한 후속 값이 무엇이든 맨 처음 표시되는 값이 전체 할당 크레딧을 받습니다. <br/>**[!UICONTROL 가장 최근(마지막)]**: 표시되는 마지막 값은 이전에 실행된 변수에 상관없이 성공 이벤트에 대한 전체 할당 크레딧을 받습니다. |
   | **[!UICONTROL 다음 시기 이후에 만료]** | eVar 값이 만료된 후 기간 또는 이벤트를 지정할 수 있습니다(즉, 더 이상 성공 이벤트에 대한 크레딧을 받지 않음).  성공 이벤트가 eVar 만료 후 발생하는 경우 값이 해당 이벤트에 대한 크레딧을 받지 않습니다 (eVar가 활성화되지 않았음). |

1. **[!UICONTROL Advertising Analytics 보고 활성화]** (맨 처음) 또는 **[!UICONTROL Advertising Analytics 보고 업데이트]** (이후)를 클릭합니다. 이제 보고서 세트가 Advertising Analytics 검색 데이터를 받을 준비가 되었습니다. 이제 [Advertising 계정을 만들](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-create-ad-account.md)준비가 되었습니다.
