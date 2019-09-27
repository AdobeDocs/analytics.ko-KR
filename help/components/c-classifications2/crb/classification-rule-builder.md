---
description: 코드 변경을 추적할 때마다 분류를 유지 관리하고 업로드하는 대신 규칙 기반의 자동 분류를 만들어 여러 보고서 세트에 적용할 수 있습니다. 규칙은 분류 관련 트래픽 볼륨에 따라 빈번하게 처리됩니다.
seo-description: 코드 변경을 추적할 때마다 분류를 유지 관리하고 업로드하는 대신 규칙 기반의 자동 분류를 만들어 여러 보고서 세트에 적용할 수 있습니다. 규칙은 분류 관련 트래픽 볼륨에 따라 빈번하게 처리됩니다.
seo-title: 분류 규칙 빌더 워크플로우
solution: Analytics
subtopic: 분류
title: 분류 규칙 빌더 워크플로우
topic: 관리 도구
uuid: edb1f07e-fa86-4055-8f4b-cce2d370edbb
translation-type: tm+mt
source-git-commit: 0dbc8ac9b416ce50f197a884bb71c6cd389cd0bb

---


# 분류 규칙 빌더 워크플로우

코드 변경을 추적할 때마다 분류를 유지 관리하고 업로드하는 대신 규칙 기반의 자동 분류를 만들어 여러 보고서 세트에 적용할 수 있습니다. 규칙은 분류 관련 트래픽 볼륨에 따라 빈번하게 처리됩니다.

## Important Notice before you get started

분류 규칙 사용을 시작하기 전에 다음 사항에 유의하십시오.

* 현재 분류 시스템은 한 번에 최대 1,000만 개의 행만 내보낼 수 있습니다.
* 분류 규칙 빌더(CRB)가 내보내기를 요청하면 분류되지 않은 값과 분류되지 않은 값을 모두 가져옵니다. 이때 분류되지 않은 값은 내보내기가 끝날 때 전달됩니다. 즉, 시간이 지남에 따라 분류되지 않은 값을 가져오지 않고도 1,000만 개의 분류된 값을 채울 수 있습니다.
* Because the architecture is set up in a way that CRB could be pulling from "n" number of servers, this can lead to inconsistencies as to which servers get picked up and in what order. 이러한 이유로, 분류되지 않은 값을 얻는 것은 매우 어렵습니다.

차원에 대해 분류된 값이 1,000만 개 이상인 사용자에 대한 **해결책** :FTP를 통해 분류되지 않은 값을 1천만 묶음으로 내보내고 수동으로 분류해야 합니다.

## 분류 규칙 시작하기 {#section_3FF666EF9D5B4E37A23B3FB400CDA2E6}

**[!UICONTROL 관리]** &gt; **[!UICONTROL 분류 규칙 빌더]**

다음은 분류 규칙을 구현하기 위해 수행하는 상위 수준 단계입니다.

| 단계 | 수행 위치 | 설명 |
|--- |--- |--- |
| Step 1 (Prerequisite): [Set up your classification schema](https://marketing.adobe.com/resources/help/en_US/reference/c_classifications.html). | [!UICONTROL 관리] &gt; [!UICONTROL 보고서] 세트 [!UICONTROL &gt; 설정] 편집 &gt; &lt;트래픽 분류또는 전환 분류&gt; | 변수를 선택하고 해당 변수에 사용할 분류를 정의하십시오. <br>변수에는 변수가 규칙에 사용되기 전에 만들어진 분류 열이 최소 1개 있어야 합니다.<br>분류가 활성화되면, 가져오기 및 규칙 빌더를 사용하여 특정 값을 분류할 수 있습니다. |
| Step 2: [Create a rule set](../../../components/c-classifications2/crb/classification-rule-set.md). | [!UICONTROL 관리] &gt; [!UICONTROL 분류 규칙 빌더] &gt; [!UICONTROL 규칙 세트 추가] | 규칙 세트는 특정 변수에 대한 분류 규칙 그룹입니다. |
| 3단계:보고서 세트 및 변수를 구성합니다. | [!UICONTROL 분류 규칙 빌더] &gt; &lt;규칙 세트&gt; | 규칙 세트를 보고서 세트 및 변수에 적용합니다. |
| Step 4: [Add classification rules to the set](../../../components/c-classifications2/crb/classification-quickstart-rules.md). | [!UICONTROL 분류 규칙 빌더] &gt; &lt;규칙 세트&gt; | 조건을 분류에 일치시킨 다음 규칙에 적용할 작업을 지정합니다.  규칙 [처리](../../../components/c-classifications2/crb/classification-quickstart-rules.md)방법에 대한 정보에 익숙해지십시오. |
| 5단계:분류 [규칙 세트 테스트](../../../components/c-classifications2/crb/classification-quickstart-rules.md) | [!DNL Testing Page] | 초안 모드에서 규칙을 편집하여 유효성 확인을 위한 규칙을 테스트하려고 합니다. 초안 모드에서는 규칙을 실행할 수 없습니다.<br>이 단계는 [정규 표현식을](../../../components/c-classifications2/crb/classification-quickstart-rules.md)사용할 때 중요합니다. |
| 6단계:유효한 [규칙을](../../../components/c-classifications2/crb/classification-rule-definitions.md)활성화합니다. | [!DNL Rules Page] | 규칙이 유효하면 규칙 세트를 활성화합니다.  필요하면 기존의 키를 덮어쓸 수 있습니다. 자세한 내용은 [규칙 처리 방법](../../../components/c-classifications2/crb/classification-quickstart-rules.md). |
| Step 7 (Optional): [Delete unwanted rules](../../../components/c-classifications2/crb/classification-rule-definitions.md). | [!DNL Rules Page] | 세트에서 원하지 않는 규칙을 삭제합니다.<br>참고: 규칙을 삭제해도 업로드된 분류 데이터는 삭제되지 않습니다.  See  [Delete classification data](../../../components/c-classifications2/c-classifications-importer/t-delete-classification-data.md) if you need to delete classified data. |

>[!NOTE]
>
>분류 가져오기 도구를 사용할 권한이 있는 그룹은 분류 규칙을 사용할 수 있습니다. See [How Rules Are Processed](../../../components/c-classifications2/crb/classification-quickstart-rules.md) for important processing information.

**추가 리소스**

**블로그**:이 기능에 대한 자세한 내용은 Digital Marketing 블로그를 참조하십시오.규칙 [기반 분류를](https://blogs.adobe.com/digitalmarketing/analytics/rule-based-classifications-part-1-making-classifications-easier/?utm_source=feedburner&utm_medium=feed&utm_campaign=Feed%3A+AdobeDigitalMarketing+%28Adobe+Digital+Marketing+Blog%29)참조하십시오.

**비디오**:YouTube [를 방문하여](https://www.youtube.com/watch?v=6laI5SBXY-I) 분류 [!UICONTROL 개요] 비디오를봅니다.
