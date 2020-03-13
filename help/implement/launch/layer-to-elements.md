---
description: 'null'
title: 데이터 레이어 개체를 데이터 요소에 매핑
uuid: null
translation-type: tm+mt
source-git-commit: 283fcd5832abe4c09caa332c2ebc3a22029e6707

---


# 데이터 레이어 개체를 데이터 요소에 매핑


구현을 위한 데이터 레이어를 [만든](https://docs.adobe.com/content/help/en/analytics/implementation/prepare/data-layer.html) 후 Launch의 [데이터 요소에 해당 개체의 매핑을 수행할 수 있습니다](https://docs.adobe.com/content/help/en/launch/using/reference/manage-resources/data-elements.html#create-a-data-element). 데이터 요소는 다양한 방식으로 활용할 수 있는 데이터 맵에 대한 기본 요소입니다. 데이터 요소를 사용하여 Analytics 보고서를 비롯한 Adobe Platform 솔루션에서 데이터를 수집, 구성 및 제공할 수 있습니다.

데이터 레이어 개체를 론치 데이터 요소에 매핑하려면 다음을 수행합니다.

1. 론치에서 데이터 요소를 추가할 속성의 이름을 클릭합니다. 속성을 이미 설정하지 않은 경우 론치 속성 [만들기 지침을 참조하십시오](https://docs.adobe.com/content/help/en/core-services-learn/implementing-in-websites-with-launch/configure-launch/launch.html).

2. Click **Data Elements** and then click **Create New Data Element**.

   ![데이터 요소 만들기](assets/createelement.png)


3. 데이터 요소의 이름을 입력합니다. 이 이름은 추적하려는 데이터 레이어의 JavaScript 변수에 해당하는 간단한 레이블이어야 합니다.

4. [확장]에서 [코어]를 **선택합니다.** 이 확장에는 필요한 모든 변수가 포함되어 있습니다.

5. For **Data Element Type**, select **JavaScript Variable**. 해당 **필드에 Javascript 변수 이름을** 입력합니다. 이는 JavaScript 데이터 레이어의 정확한 개체 이름과 일치해야 합니다.

6. 기본값 **에**&#x200B;기본적으로 설정하려는 값을 입력하거나 해당되는 경우 비워 둡니다.

7. 사용 사례에 따라, 소문자 값을 강제 적용하고 깔끔한 텍스트를 적용할 옵션을 선택할 수 있습니다(Launch는 일반적인 간격을 적용합니다).

8. 새 데이터 요소에 대한 Launch 스토어 값을 보유할 기간을 지정합니다.

9. **저장**&#x200B;을 클릭합니다.

다음 예는 Launch에서 데이터 레이어의 JavaScript 변수에 대해 생성된 페이지 이름 데이터 요소를 ``pageName`` 보여줍니다.

![요소 지정](assets/new_element.png)


데이터 레이어 개체를 데이터 요소에 매핑하면 이를 활용하여 Analytics 변수를 채울 수 있습니다. 자세한 내용은 데이터 요소를 [분석 변수에 매핑을 참조하십시오](https://docs.adobe.com/content/help/en/analytics/implementation/prepare/data-layer.html).
