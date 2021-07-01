---
title: Analytics 변수에 Launch 데이터 요소 매핑
description: Analysis Workspace에서 차원으로 사용할 수 있도록 데이터 요소를 Analytics 변수에 할당합니다.
exl-id: 996c1204-3f8a-453e-8104-5e8e1279517c
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: ht
source-wordcount: '446'
ht-degree: 100%

---

# Analytics 변수에 Launch 데이터 요소 매핑

Adobe Experience Platform Launch에 데이터 요소가 저장되어 있으면 Analytics 차원에 할당할 수 있습니다.

## 사전 요구 사항

[데이터 레이어 개체를 데이터 요소에 매핑](layer-to-elements.md): Launch의 데이터 요소를 이해하고 여러 가지 기능을 사용할 수 있어야 합니다.

[솔루션 설계 문서 만들기](../prepare/solution-design.md): 솔루션 설계 문서는 체계적으로 구성해야 합니다. 솔루션 계산 문서를 따르면 데이터 요소를 Analytics 변수에 쉽게 할당할 수 있습니다.

## Analytics 변수에 데이터 요소 할당

이러한 단계를 수행한 후 Launch에 라이브러리를 게시하면 Analysis Workspace에서 사용자 지정 차원을 사용할 수 있습니다. Analytics 변수를 전역 또는 개별 규칙으로 설정할 수 있습니다.

### 전역 변수 설정

전역 변수는 데이터 요소가 있는 모든 페이지에서 변수 값을 설정하려는 경우에 이상적입니다.

1. [Adobe Experience Platform Launch](https://launch.adobe.com)로 이동한 후 메시지가 표시되면 로그인합니다.
1. 원하는 Launch 속성을 클릭합니다.
1. [!UICONTROL 확장 탭]을 클릭한 다음 Adobe Analytics 확장 프로그램 아래에서 [!UICONTROL 구성]을 클릭합니다.
1. [!UICONTROL 전역 변수] 아코디언을 클릭하면 전역 변수를 할당하는 인터페이스가 표시됩니다.

### 규칙의 변수 설정

규칙에 설정된 변수는 모든 페이지에서 변수를 설정하지 않으려는 경우에 이상적입니다. 규칙에서 기준을 정의합니다. Adobe Experience Platform Launch 사용 안내서의 [규칙](https://experienceleague.adobe.com/docs/launch/using/reference/manage-resources/rules.html?lang=ko-KR)을 참조하십시오.

1. [Adobe Experience Platform Launch](https://launch.adobe.com)로 이동한 후 메시지가 표시되면 로그인합니다.
1. 원하는 Launch 속성을 클릭합니다.
1. [!UICONTROL 규칙] 탭을 클릭하고 원하는 규칙을 클릭하거나 규칙을 만듭니다.
1. [!UICONTROL 작업] 아래의 [!UICONTROL 추가] 버튼을 클릭합니다.
1. [!UICONTROL 확장] 드롭다운을 Adobe Analytics로 설정하고 [!UICONTROL 작업 유형]을 변수 설정으로 설정합니다.
1. 원하는 Analytics 변수 오른쪽에 있는 ![데이터 요소](assets/data-element.png) 아이콘을 클릭합니다. 조직의 [솔루션 설계 문서](../prepare/solution-design.md)는 사용할 Analytics 변수를 지시합니다.
1. 모달 창에서 원하는 데이터 요소를 선택합니다. [!UICONTROL 선택]을 클릭합니다.
1. 데이터 요소 이름이 `%` 기호로 둘러싸인 텍스트 필드에 추가됩니다. 예를 들어 데이터 요소의 이름을 &quot;페이지 이름&quot;으로 지정한 경우 데이터 요소를 변수에 할당할 때 `%Page name%` 문자열이 표시됩니다.

>[!TIP]
>
>동일한 변수에 데이터 요소를 연결할 수 있습니다. 예를 들어 &quot;호스트 이름&quot; 데이터 요소와 &quot;경로 이름&quot; 데이터 요소가 있는 경우 `%Hostname%%Pathname%`를 사용하여 두 요소를 모두 단일 변수에 결합할 수 있습니다.

## 다음 단계

[페이지 변수](../vars/page-vars/page-variables.md): Analysis Workspace에서 더 많은 차원을 얻기 위해 구현에서 사용할 수 있는 페이지 수준 변수를 알아봅니다.

[구성 변수](../vars/config-vars/configuration-variables.md): 구현에서 Adobe Analytics의 더 많은 기능을 잠금 해제할 수 있는 구성 변수를 알아봅니다.
