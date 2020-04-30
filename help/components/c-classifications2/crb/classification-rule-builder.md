---
description: 코드 변경을 추적할 때마다 분류를 유지 관리하고 업로드하는 대신 규칙 기반의 자동 분류를 만들어 여러 보고서 세트에 적용할 수 있습니다. 규칙은 분류 관련 트래픽 볼륨에 따라 빈번하게 처리됩니다.
subtopic: Classifications
title: 분류 규칙 빌더 워크플로우
topic: Admin tools
uuid: edb1f07e-fa86-4055-8f4b-cce2d370edbb
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8

---


# 분류 규칙 빌더 워크플로우

코드 변경을 추적할 때마다 분류를 유지 관리하고 업로드하는 대신 규칙 기반의 자동 분류를 만들어 여러 보고서 세트에 적용할 수 있습니다. 규칙은 분류 관련 트래픽 볼륨에 따라 빈번하게 처리됩니다.

## 시작하기 전 중요 유의 사항

분류 규칙을 사용하기 전에 다음 사항에 유의하십시오.

* 하위 분류는 분류 규칙 빌더(CRB)에서 지원되지 않습니다.
* 현재 분류 시스템은 한 번에 최대 1,000만 개의 행만 내보낼 수 있습니다.
* CRB가 내보내기를 요청하면 분류되지 않은 값과 분류되지 않은 값을 모두 가져옵니다. 이때 내보내기가 완료되면 분류되지 않은 값이 전달됩니다. 이것은 시간이 지남에 따라 분류되지 않은 값에 영향을 주지 않고 1,000만 개의 분류된 값을 채울 수 있음을 의미합니다.
* 아키텍처는 CRB가 &quot;n&quot;개의 서버에서 가져오는 방식으로 설정되므로, 이렇게 되면 어떤 순서로 어느 서버를 선택할지에 대해 일치하지 않을 수 있습니다. 이러한 이유로, 분류되지 않은 값에 영향을 주는 것은 매우 어렵습니다.

차원에 대해 분류된 값이 1,000만 개 이상인 사용자에 대한 **해결 방법**&#x200B;은 FTP를 통해 분류되지 않은 값을 1000천만 묶음으로 내보내고 수동으로 분류하는 것입니다.

## 분류 규칙 시작하기 {#section_3FF666EF9D5B4E37A23B3FB400CDA2E6}

**[!UICONTROL Admin]** > **[!UICONTROL Classification Rule Builder]**

분류 규칙을 구현할 수 있는 높은 수준의 단계는 다음과 같습니다.

| 단계.  | 수행 위치 | 설명 |
|--- |--- |--- |
| 1단계(전제 조건): [분류 스키마를 설정합니다](https://docs.adobe.com/content/help/en/analytics/components/classifications/c-classifications.html). | [!UICONTROL Admin] > [!UICONTROL Report Suites] > [!UICONTROL Edit Settings] > &lt;트래픽 분류 또는 전환 분류> | 변수를 선택하고 해당 변수에 사용할 분류를 정의하십시오. <br>변수에는 변수가 규칙에 사용되기 전에 만들어진 분류 열이 최소 1개 있어야 합니다.<br>분류가 활성화되면, 가져오기 및 규칙 빌더를 사용하여 특정 값을 분류할 수 있습니다. |
| 2단계: [규칙 세트를 만듭니다](/help/components/c-classifications2/crb/classification-rule-set.md). | [!UICONTROL Admin] >  [!UICONTROL Classification Rule Builder] > [!UICONTROL Add Rule Set] | 규칙 세트는 특정 변수에 대한 분류 규칙 그룹입니다. |
| 3단계: 보고서 세트 및 변수를 구성합니다. | [!UICONTROL Classification Rule Builder] >  &lt;규칙 세트> | 규칙 세트를 보고서 세트 및 변수에 적용합니다. |
| 4단계: [세트에 분류 규칙을 추가합니다](/help/components/c-classifications2/crb/classification-quickstart-rules.md). | [!UICONTROL Classification Rule Builder] >  &lt;규칙 세트> | 조건을 분류에 일치시킨 다음 규칙에 적용할 작업을 지정합니다.  [규칙 처리 방법](/help/components/c-classifications2/crb/classification-quickstart-rules.md)의 정보를 숙지하십시오. |
| 5단계: [분류 규칙 세트를 테스트합니다](/help/components/c-classifications2/crb/classification-quickstart-rules.md). | [!DNL Testing Page] | 초안 모드에서 규칙을 편집하여 유효성 확인을 위한 규칙을 테스트하려고 합니다. 초안 모드에서는 규칙을 실행할 수 없습니다.<br>이 단계는 [정규 표현식](/help/components/c-classifications2/crb/classification-quickstart-rules.md)을 사용할 때 중요합니다. |
| 6단계: [유효한 규칙을 활성화합니다](/help/components/c-classifications2/crb/classification-rule-definitions.md). | [!DNL Rules Page] | 규칙이 유효하면 규칙 세트를 활성화합니다.  필요하면 기존의 키를 덮어쓸 수 있습니다. 자세한 내용은 [규칙 처리 방법](/help/components/c-classifications2/crb/classification-quickstart-rules.md). |
| 7단계(선택 사항): [원치 않는 규칙을 삭제합니다](/help/components/c-classifications2/crb/classification-rule-definitions.md). | [!DNL Rules Page] | 세트에서 원하지 않는 규칙을 삭제합니다.<br>참고: 규칙을 삭제해도 업로드된 분류 데이터는 삭제되지 않습니다.  분류된 데이터를 삭제해야 할 경우 [분류 데이터 삭제](/help/components/c-classifications2/c-classifications-importer/t-delete-classification-data.md)를 참조하십시오. |

>[!NOTE]
>
>분류 가져오기 도구를 사용할 수 있는 권한이 있는 그룹은 분류 규칙을 사용할 수 있습니다. 중요한 처리 정보에 대해서는 [규칙 처리 방법](/help/components/c-classifications2/crb/classification-quickstart-rules.md)을 참조하십시오.

**추가 리소스**

**블로그**: 이 기능에 대한 추가 정보를 보려면 디지털 마케팅 블로그: [규칙 기반 분류](https://blogs.adobe.com/digitalmarketing/analytics/rule-based-classifications-part-1-making-classifications-easier/?utm_source=feedburner&amp;utm_medium=feed&amp;utm_campaign=Feed%3A+AdobeDigitalMarketing+%28Adobe+Digital+Marketing+Blog%29)를 참조하십시오.

**비디오**:YouTube [를](https://www.youtube.com/watch?v=6laI5SBXY-I) 방문하여 [!UICONTROL Classifications Overview] 비디오를 보십시오.
