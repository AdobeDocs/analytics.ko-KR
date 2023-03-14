---
title: 데이터 레이어 오브젝트를 데이터 요소에 매핑
description: 데이터 레이어에서 읽을 태그를 구성합니다.
feature: Launch Implementation
exl-id: b7594084-cb5f-408e-8a76-0a0815cc7553
source-git-commit: ac9e4934cee0178fb00e4201cc3444d333a74052
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 100%

---

# 데이터 레이어 오브젝트를 데이터 요소에 매핑

조직이 사이트에서 데이터 레이어를 설정하고 구현하면 태그 내의 데이터 요소에 데이터 레이어 오브젝트를 매핑할 수 있습니다.

## 사전 요구 사항

[데이터 레이어 만들기](../prepare/data-layer.md): 사이트에 데이터 레이어가 있는지 확인합니다. 기술적으로 모든 JavaScript 오브젝트를 매핑하거나 페이지에서 직접 CSS 요소를 스크랩할 수 있지만 Adobe에서는 이 방법을 마지막 수단으로 권장합니다. 사이트 레이아웃이 변경되면 태그에 사용된 CSS 선택기의 작동이 중지되어 데이터가 손실됩니다.

## 태그를 사용하여 데이터 요소 만들기

[데이터 요소](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html)는 Adobe Experience Platform 데이터 수집의 구성 요소로서 도구 전반에서 사용할 수 있습니다. 데이터 요소를 사용하여 Adobe Analytics 확장 기능에서 변수 값을 할당할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 태그 속성을 클릭합니다.
1. **[!UICONTROL 데이터 요소]** 탭을 클릭한 다음 **[!UICONTROL 데이터 요소 추가]**&#x200B;를 클릭합니다.

   ![데이터 요소 만들기](assets/createelement.png)

1. 데이터 요소의 이름을 입력합니다. 추적하려는 데이터 레이어의 JavaScript 변수에 해당하는 간단한 레이블이 될 수 있습니다.
1. **[!UICONTROL 확장 프로그램]** 드롭다운 아래에서 **[!UICONTROL 코어]**&#x200B;를 선택합니다.
1. **[!UICONTROL 데이터 요소 유형]**&#x200B;에 대해 **[!UICONTROL JavaScript 변수]**&#x200B;를 선택합니다. 이 데이터 요소에 매핑할 JavaScript 변수를 입력할 수 있는 텍스트 필드가 오른쪽에 나타납니다.
1. 원하는 Javascript 변수를 일반적으로 데이터 레이어 내에 입력합니다. 예를 들어 조직의 데이터 레이어가 Adobe의 권장 방식과 거의 일치하는 경우 값은 `digitalData.page.pageInfo.pageName`가 될 수 있습니다. 브라우저의 콘솔을 사용하여 JavaScript 변수 구문 및 값의 유효성을 확인할 수 있습니다.
1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## 다음 단계

[데이터 요소를 Analytics 변수에 매핑](elements-to-variable.md): Analysis Workspace에서 차원으로 사용할 수 있도록 데이터 요소를 Analytics 변수에 할당합니다.
