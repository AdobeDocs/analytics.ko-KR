---
description: 작업 공간 FAQ
title: FAQ 및 Analysis Workspace 문제 해결
translation-type: tm+mt
source-git-commit: d0fe97b9368cbc4c9e79f9e56adf9786b58dce1a
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 100%

---


# FAQ

| 질문 | 답변 |
|--- |--- |
| Analysis Workspace을 사용하기 위한 사전 요구 사항은 무엇입니까? | [Adobe Experience Platform Launch를 사용하여 Adobe Analytics에 데이터 보내기](/help/implement/launch/validate-publish-prod.md): Analysis Workspace를 사용하려면 실제로 구현해야 합니다. 도구를 사용하기 전에 조직에서 Adobe에 데이터를 보내도록 하십시오. DTM이나 기존 수동 구현과 같은 다른 구현도 작동할 수 있습니다. |
| Analysis Workspace에 대한 관리 및 액세스 요구 사항은 무엇입니까? | 자세한 내용은 [관리 요구 사항](/help/analyze/analysis-workspace/workspace-faq/frequently-asked-questions-analysis-workspace.md). |
| Analysis Workspace을 사용하는 것이 데이터 수집에 영향을 줍니까? | Analysis Workspace는 보고 도구이므로 데이터 수집에는 영향을 주지 않습니다. 구성 요소를 프로젝트에 마구잡이로 드래그하여 놓아서 어떤 것이 효과가 있는지를 확인하는 데에는 아무 영향이 없습니다. 다양한 차원과 지표의 조합을 작업 공간 프로젝트에 드래그하여 사용 가능한 조합을 확인하십시오. 실수로 유효하지 않은 구성 요소를 작업 공간 프로젝트에 드래그하거나 단계를 다시 수행하려면 Ctrl+Z(Windows) 또는 Cmd+Z(Mac)를 눌러 마지막으로 수행한 작업을 취소하십시오. 왼쪽 위 메뉴에서 *[!UICONTROL 프로젝트] > [!UICONTROL 신규]*&#x200B;를 클릭하여 깨끗한 슬레이트로 시작할 수도 있습니다. |
| Analysis Workspace 프로젝트에는 몇 개의 보고서 세트를 표시할 수 있습니까? | 이제 Analysis Workspace에서 더 많은 [여러 보고서 세트](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/build-workspace-project/multiple-report-suites.html)의 데이터를 사용하여 프로젝트를 만들 수 있습니다. |
| Analysis Workspace은 어떻게 구현합니까? | 특별한 구현은 필요하지 않습니다. Analysis Workspace은 Analytics Standard 또는 Premium이 있는 모든 회사에서 사용할 수 있습니다. 그렇지만 컨텐츠(예: 보고서 세트 및 프로젝트 구성 요소)에 대한 표준 권한이 적용되고 프로젝트를 조정하고 공유할 수 있습니다. [관리 및 액세스 요구 사항](/help/analyze/analysis-workspace/workspace-faq/frequently-asked-questions-analysis-workspace.md)을 참조하십시오. |
| Analysis Workspace이 Adobe Analytics에서 사전 구성된 보고서를 변경합니까? | 아니요. 이것은 별도의 환경이므로, Adobe Analytics에서 기존의 보고서나 사전 구성된 보고서에 대한 변경 사항이 없습니다. 여전히 Analysis Workspace을 사용하여 표준 Reports &amp; Analytics과 Report Builder 보고서를 채택할 수 있습니다. |
| Data Warehouse에 Analysis Workspace을 사용할 수 있습니까? | Analysis Workspace은 벌크 데이터 내보내기에 권장되지 않습니다. 대시보드와 유사한 분석 프로젝트를 만드는 시각화 작업 공간입니다. |
| Analysis Workspace의 성능을 최적화하려면 어떻게 해야 합니까? | [성능 최적화](/help/analyze/analysis-workspace/workspace-faq/optimizing-performance.md)를 참조하십시오. |

## 문제 해결

**지표를 드래그하면 &#39;잘못된 데이터&#39;라고 표시됩니다.**

잘못된 데이터는 Adobe가 보고서에 사용된 차원과 지표의 조합을 사용하여 데이터를 반환할 수 없음을 의미합니다. 예를 들어, 서로 위에 스택된 두 개의 지표는 이런 식으로 두 개의 지표를 표시할 수 있는 방법이 없으므로 데이터로 반환되지 않습니다. 대신 지표를 나란히 배치합니다.

**지표를 드래그하면 실제 데이터가 표시되지 않고, 0만 표시됩니다.**

작업 공간 보고서를 생성했지만 데이터가 없다면 확인할 수 있는 몇 가지 사항이 있습니다.

* 보고서 세트를 다시 확인하여 데이터가 채워져 있는지 확인하십시오.
* 보고서에서 세그먼트를 적용했다면 세그먼트 기준이 데이터와 일치하지 않을 수 있습니다. 세그먼트를 제거하거나 세그먼트 정의를 조정해 보십시오.
* 오른쪽 상단 모서리의 날짜 범위를 확인하고 예상한 값으로 설정되어 있는지 확인하십시오.
* 웹 사이트로 이동하고 [디버거](https://docs.adobe.com/content/help/ko-KR/debugger/using/experience-cloud-debugger.html)를 사용하여 데이터가 수집되고 있는지 확인하십시오.