---
description: 경로 분석을 기반으로 하는 보고서 그룹입니다. 기술적으로 경로 지정은 한 페이지 이름에서 다른 페이지 이름(한 값에서 다른 값으로)으로 이동하는 것을 의미합니다.
title: 경로 지정
topic: Reports
uuid: c4ff9fa8-e567-4039-9c86-322800a942da
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 경로 지정

경로 분석을 기반으로 하는 보고서 그룹입니다. 기술적으로 경로 지정은 한 페이지 이름에서 다른 페이지 이름(한 값에서 다른 값으로)으로 이동하는 것을 의미합니다.

보다 유연한 경로 지정 옵션이 필요하면 [Analysis Workspace 흐름](https://marketing.adobe.com/resources/help/ko_KR/analytics/analysis-workspace/flow.html)을 사용하십시오.

>[!NOTE] 경로 지정을 활성화하려면 로 **[!UICONTROL Admin > Report Suites > Edit Settings > Traffic > Traffic Variables]**&#x200B;이동합니다. 사이트 섹션 및 서버 보고서에서 경로 지정을 활성화하려면 고객 지원에 문의하십시오.

값이 수집되는 순서를 알아야 하는 경우 해당 값을 수집하는 변수에 대한 경로 지정을 활성화해야 합니다. 경로 지정은 기본적으로 페이지에 대해 활성화됩니다. 경로 지정은 특정 경우에만 적절하므로 기본적으로 모든 prop에 대해 활성화되지 않습니다. prop에 대한 경로 지정을 활성화하려면 고객 지원 센터에 문의하십시오.

>[!NOTE] Ad Hoc Analysis에서, prop에 대해 분류를 활성화하면 활성화된 prop에 대해 설정되어 있는 모든 분류에서 경로 지정 지표를 사용할 수 있게 됩니다.

**예 - 사이트 섹션의 경로 지정**

Enabling pathing for the *`s.channel`* variable allows you to track how site visitors move between Site Sections (as the value changes).

![](assets/path_sections.png)

그런 다음 방문자가 페이지 그룹 또는 사이트의 섹션을 이동하는 방법을 [!UICONTROL Next Site Section Flow]표시하는 등 다양한 경로 보고서에서 경로 지정을 사용할 수 있습니다.

![](assets/paths_report.png)

**예 - 검색 경로 지정**

한 값에서 다른 값으로 가는 동일한 개념이 다른 트래픽 변수에도 마찬가지로 적용됩니다  *`s.props`*. 예를 들어 내부 검색어 *`s.prop`*&#x200B;에 대해 경로 지정을 활성화하면 경로 방문자가 검색어를 따라 이동하는 것을 볼 수 있습니다.

**예 - 로그인 상태당 경로 지정**

방문자의 로그인 상태를 기반으로 사람들이 사이트를 통해 이동하는 방식을 알고 싶을 수 있습니다. 이 정보를 보려면 경로 지정 보고서에서 로그인 상태를 확인하지 않습니다. 방문자가 보고서에서 값을 어떻게 변경했는지, 또는 방문자가 로그인 상태에서 로그아웃 상태로 어떻게 변경되었을 수 있는지를 알 수 있기 때문입니다. 대신 세그먼트 값을 *`s.pageName`* 변수와 연결한 다음 결과 변수에 경로를 지정합니다. 다음은 멤버 상태당 페이지 경로 지정을 위한 샘플 코드입니다.

```js
s.pageName="Home Page"; 
s.prop18="Gold"; // Member Status 
s.prop19=s.prop18 + ":" + s.pageName;
```

그런 다음 경로 지정을 활성화하여 구성원이 페이지를 이동하는 *`s.prop19`* 방식을 확인합니다.

>[!NOTE] Ad Hoc Analysis를 수행하는 경우는 세그먼트 값을 연결하지 않고 페이지 경로를 세그먼트화한 후 세그먼트를 경로 지정 보고서에 적용할 수 있습니다.

