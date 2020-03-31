---
title: Analytics 변수에 론치 데이터 요소 매핑
description: 분석 작업 공간에서 차원으로 사용할 수 있도록 데이터 요소를 Analytics 변수에 할당합니다.
translation-type: tm+mt
source-git-commit: 6937d47e3cf980a21bec680cdbd2931a4a368221

---


# Analytics 변수에 론치 데이터 요소 매핑

Adobe Experience Platform Launch에 데이터 요소 저장소가 있으면 Analytics 차원에 할당할 수 있습니다.

## 전제 조건

[데이터 레이어 개체를 데이터 요소에](layer-to-elements.md)매핑:Launch의 데이터 요소를 이해하고 여러 가지 기능을 사용해야 합니다.

[솔루션 디자인 문서](../prepare/solution-design.md)만들기:솔루션 디자인 문서는 체계적으로 구성해야 합니다. 솔루션 디자인 문서를 팔로우하면 데이터 요소를 Analytics 변수에 쉽게 할당할 수 있습니다.

## Analytics 변수에 데이터 요소 할당

다음 단계 후에 Launch에서 라이브러리를 게시하면 분석 작업 공간에서 사용자 정의 차원을 사용할 수 있습니다. Analytics 변수를 전역 또는 개별 규칙으로 설정할 수 있습니다.

### 전역 변수 설정

전역 변수는 데이터 요소가 있는 모든 페이지에서 변수 값을 설정하려는 경우에 이상적입니다.

1. [Adobe Experience Platform Launch](https://launch.adobe.com)로 이동한 후 메시지가 표시되면 로그인합니다.
1. 원하는 론치 속성을 클릭합니다.
1. 을 [!UICONTROL Extensions tab]클릭한 다음 Adobe Analytics [!UICONTROL Configure] 확장 프로그램 아래에서 을 클릭합니다.
1. 전역 변수를 할당할 인터페이스를 표시하는 [!UICONTROL Global variables] 아코디언을 클릭합니다.

### 규칙에서 변수 설정

규칙에 설정된 변수는 모든 페이지에서 변수를 설정하지 않으려는 경우에 이상적입니다. 규칙에서 기준을 정의합니다. See [Rules](https://docs.adobe.com/content/help/en/launch/using/reference/manage-resources/rules.html) in the Adobe Experience Platform Launch user guide.

1. [Adobe Experience Platform Launch](https://launch.adobe.com)로 이동한 후 메시지가 표시되면 로그인합니다.
1. 원하는 론치 속성을 클릭합니다.
1. 탭을 [!UICONTROL Rules] 클릭한 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다.
1. 아래의 [!UICONTROL Add] 단추를 클릭합니다 [!UICONTROL Actions].
1. Set the [!UICONTROL Extension] dropdown to Adobe Analytics, and the [!UICONTROL Action Type] to Set Variables.
1. 원하는 ![Analytics 변수 오른쪽에 있는 데이터 요소](assets/data-element.png) 아이콘을 클릭합니다. 조직의 [솔루션 디자인 문서는](../prepare/solution-design.md) 사용할 Analytics 변수를 나타냅니다.
1. 모달 창에서 원하는 데이터 요소를 선택합니다. 클릭 [!UICONTROL Select].
1. 데이터 요소 이름이 `%` 기호로 둘러싸인 텍스트 필드에 추가됩니다. 예를 들어 데이터 요소의 이름을 &quot;페이지 이름&quot;으로 지정한 경우 데이터 요소를 변수에 할당할 `%Page name%` 때 문자열이 표시됩니다.

> [!TIP] 동일한 변수에 데이터 요소를 연결할 수 있습니다. 예를 들어 &quot;호스트 이름&quot; 데이터 요소와 &quot;경로 이름&quot; 데이터 요소가 있는 경우 를 사용하여 두 요소를 하나의 변수에 결합할 수 `%Hostname%%Pathname%`있습니다.

## 다음 단계

[페이지 변수](../vars/page-vars/page-variables.md):분석 작업 공간에서 차원을 최대한 활용하기 위해 구현에서 사용할 수 있는 페이지 수준 변수를 알아봅니다.

[구성 변수](../vars/config-vars/configuration-variables.md):구현에서 Adobe Analytics의 더 많은 기능을 잠금 해제할 수 있는 구성 변수를 알아봅니다.
