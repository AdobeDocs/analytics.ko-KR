---
title: 데이터 레이어 개체를 데이터 요소에 매핑
description: 데이터 레이어에서 읽도록 론치를 구성합니다.
translation-type: tm+mt
source-git-commit: 283fcd5832abe4c09caa332c2ebc3a22029e6707

---


# 데이터 레이어 개체를 데이터 요소에 매핑

조직에서 사이트에 데이터 레이어를 설정하고 구현하면 Launch 내의 데이터 요소에 데이터 레이어 개체를 매핑할 수 있습니다.

## 전제 조건

[데이터 레이어](../prepare/data-layer.md)만들기:사이트에 데이터 레이어가 있는지 확인합니다. 기술적으로 모든 JavaScript 개체를 매핑하거나 페이지에서 직접 CSS 요소를 스크랩할 수 있지만 Adobe에서는 이 방법을 마지막 수단으로 권장합니다. 사이트 레이아웃이 변경되면 론치에 사용된 CSS 선택기의 작동이 중지되어 데이터가 손실됩니다.

## Adobe Experience Platform Launch를 사용하여 데이터 요소 제작

[데이터 요소는](https://docs.adobe.com/content/help/ko-KR/launch/using/reference/manage-resources/data-elements.html#create-a-data-element) Launch의 구성 요소로서 도구 전체에서 사용할 수 있습니다. 데이터 요소를 사용하여 Adobe Analytics 확장 프로그램에서 변수 값을 할당할 수 있습니다.

1. [Adobe Experience Platform Launch](https://launch.adobe.com)로 이동한 후 메시지가 표시되면 로그인합니다.
1. 원하는 론치 속성을 클릭합니다.
1. Click the [!UICONTROL Data Elements] tab, then click [!UICONTROL Add Data Element].

   ![데이터 요소 만들기](assets/createelement.png)

1. 데이터 요소의 이름을 입력합니다. 추적하려는 데이터 레이어의 JavaScript 변수에 해당하는 간단한 레이블이 될 수 있습니다.
1. 확장 [!UICONTROL 드롭다운 아래에서] 코어를 [!UICONTROL 선택합니다].
1. Under the [!UICONTROL Data Element Type] dropdown, select [!UICONTROL JavaScript Variable]. 이 데이터 요소에 매핑할 JavaScript 변수를 입력할 수 있는 텍스트 필드가 오른쪽에 나타납니다.
1. 원하는 Javascript 변수를 일반적으로 데이터 레이어 내에 입력합니다. 예를 들어 조직의 데이터 레이어가 Adobe의 권장 방식과 거의 일치하는 경우 값이 될 수 `digitalData.page.pageInfo.pageName`있습니다. 브라우저의 콘솔을 사용하여 JavaScript 변수 구문 및 값의 유효성을 검사할 수 있습니다.
1. [!UICONTROL 저장을] 클릭합니다.

## 다음 단계

[데이터 요소를 Analytics 변수에](elements-to-variable.md)매핑:분석 작업 공간에서 차원으로 사용할 수 있도록 데이터 요소를 Analytics 변수에 할당합니다.
