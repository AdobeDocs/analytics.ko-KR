---
description: 조건으로 트리거할 작업을 설정합니다.
keywords: Dynamic Tag Management;규칙;규칙 만들기;새 규칙;javascript/타사 태그;조건에 대한 작업 설정;새 스크립트 추가;비순차적 javascript;순차적 javascript;비순차적 html
seo-description: 조건으로 트리거할 작업을 설정합니다.
seo-title: 조건이 트리거되는 작업 설정
solution: Experience Cloud,Analytics,Target,Dynamic Tag Management
title: 조건이 트리거되는 작업 설정
uuid: 2e892f0b-7261-41ee-b849-6e3054a38de0
translation-type: ht
source-git-commit: e060fb745d611f37f28708b3fe103c1191aa483b

---


# 조건이 트리거되는 작업 설정

조건으로 트리거할 작업을 설정합니다.

조건을 설정한 후에는 조건이 트리거되야 하는 작업을 설정해야 합니다. 이러한 작업에는 [!DNL Analytics] 이벤트, 타사 태그 및 사용자 지정 스크립트가 포함될 수 있습니다. 다음 예에서는 스크립트 또는 타사 태그를 설정하는 방법을 설명합니다.

[!DNL Adobe Analytics] 및 Google Analytics와 같은 통합 도구 이상의 기능을 수행하는 Dynamic Tag Management는 선별된 페이지나 특정 시나리오에서 모든 유형의 JavaScript를 트리거하거나 HTML을 사이트에 삽입할 수 있습니다.

각 규칙은 스크립트나 HTML 주입을 원하는 만큼 트리거할 수 있습니다.

>[!NOTE]
>
>DTM을 통해 페이지에 사용자 지정 코드를 삽입할 수 있으므로 교차 사이트 스크립팅(XSS) 취약점이 발생하지 않도록 주의하십시오(자세한 내용은 [OWASP 안내서](https://www.owasp.org/index.php/Cross-site_Scripting_(XSS)) 참조). 스크립트 내에 데이터 요소를 사용하는 경우 특별한 주의를 기울여야 합니다. 신뢰할 수 없는 소스로부터 데이터 요소 값을 가져올 수 있다는 점을 항상 유념하시기 바랍니다.

**조건이 트리거되는 작업 설정**

1. **[!UICONTROL Javascript/타사 태그]**&#x200B;를 클릭하여 새 스크립트를 규칙에 추가합니다.

   ![](assets/scripts-actions.png)

1. **[!UICONTROL 새 스크립트 추가를 클릭합니다]**.

   ![](assets/scripts-actions2.png)

1. 스크립트 이름을 지정합니다.
1. 스크립트를 트리거할 방법을 지정하고 원하는 컨텐츠를 텍스트 영역에 붙여넣습니다. ![](assets/scripts-actions3.png)

1. **[!UICONTROL 코드 저장]**&#x200B;을 클릭하면 스크립트가 규칙 큐에 추가됩니다. ![](assets/scripts-actions4.png)

