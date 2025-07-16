---
description: 처리 규칙은 데이터 수집을 간소화하고 데이터가 보고 기능으로 전송될 때 콘텐츠를 관리합니다.
subtopic: Processing rules
title: 처리 규칙 개요
feature: Processing Rules
role: Admin
exl-id: 0244aba2-4345-463a-8528-d4dcd2f872ff
source-git-commit: 0bed2622f54bf2f46aa57dbfad7bd55a61d6c7d0
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 3%

---

# 처리 규칙 개요

처리 규칙을 사용하면 보고서 세트에 기록되기 전에 데이터를 수집하는 방법을 수정할 수 있습니다.

**[!UICONTROL 관리자]** > **[!UICONTROL 보고서 세트]** > 보고서 세트 선택 > **[!UICONTROL 설정 편집]** > **[!UICONTROL 일반]** > **[!UICONTROL 처리 규칙]**

>[!WARNING]
>
>처리 규칙은 데이터 수집에 직접 영향을 미치며, 잘못 사용될 경우 데이터 손실을 초래할 수 있습니다. 데이터 품질 문제를 완화하도록 프로덕션 보고서 세트에서 활성화하기 전에 항상 개발 보고서 세트에서 처리 규칙을 테스트하십시오.

처리 규칙에 대한 두 가지 주요 사용 사례는 다음과 같습니다.

* **컨텍스트 데이터 변수 구현 워크플로 사용**: 구현에서 변수를 직접 설정하는 대신 [컨텍스트 데이터 변수](/help/implement/vars/page-vars/contextdata.md)를 사용하여 키/값 쌍을 설정할 수 있습니다. 예를 들어 를 설정하는 대신

  ```js
  s.eVar1 = "Robert Munch";
  s.eVar2 = "Books";
  s.eVar3 = "Youth";
  ```

  대신 다음을 설정할 수 있습니다.

  ```js
  s.contextData['author'] = "Robert Munch";
  s.contextData['section'] = "Books";
  s.contextData['genre'] = "Youth";
  ```

  그런 다음 컨텍스트 데이터 변수를 Analytics UI에서 원하는 차원 및 지표에 매핑할 수 있습니다.

  속성에 Analytics를 구현하기 위해 조직의 개발자와 통신할 때 컨텍스트 데이터 변수를 사용하면 통신 프로세스를 간소화할 수 있습니다. 개발자는 각 키/값 쌍을 한 번만 구현할 수 있으며, 그런 다음 Analytics 관리자는 데이터가 올바른 구현 변수를 사용하도록 할 수 있습니다.

* **수집된 데이터를 수정합니다**: 이 사용 사례에는 데이터 품질에 대한 임시 수정 사항이나 구현 공백을 채우는 데 도움이 되는 등 다양한 응용 프로그램이 있습니다. 자세한 내용 및 특정 예는 [처리 규칙 사용 사례](pr-use-cases.md)를 참조하십시오.

## 권한

제품 관리자는 기본적으로 처리 규칙에 액세스할 수 있습니다. **[!UICONTROL 처리 규칙]** 권한 항목을 포함하는 제품 프로필에 처리 규칙을 포함하여 관리자가 아닌 사용자에게 처리 규칙에 대한 액세스 권한을 부여할 수 있습니다. 자세한 내용은 [보고서 세트 도구에 대한 제품 프로필 권한](/help/admin/admin-console/permissions/report-suite-tools.md)을 참조하세요.

## 처리 규칙 만들기 또는 편집 시 고려 사항

처리 규칙을 만들거나 편집할 때 다음 사항을 고려하십시오.

* **가능한 빈 값**: 규칙을 만들 때 덮어쓰기 값이 비어 있는 경우를 고려하십시오. 예를 들어, eVar1을 eVar2 및 eVar2로 덮어쓰는 규칙이 비어 있으면 두 변수가 모두 공백으로 표시됩니다. Adobe에서는 변수 값을 사용하여 다른 값을 덮어쓰기 전에 변수 값을 확인하는 조건을 추가할 것을 권장합니다.
* **저장 시 즉시 적용**: 처리 규칙은 데이터를 저장하는 즉시 수집된 데이터에 적용됩니다. 이미 수집된 데이터에는 소급하여 적용되지 않습니다.
* **규칙 내 처리 순서**: 처리 규칙이 여러 개 있는 경우 규칙이 실행되는 순서가 중요합니다. 여러 규칙에서 주어진 변수를 사용하는 경우 올바른 순서로 실행되도록 합니다. 규칙 1의 eVar3을 덮어쓰는 경우 원래의 eVar3 값을 후속 규칙에서 사용할 수 없습니다.
* **데이터 수집 파이프라인 내의 처리 순서**: 전체 데이터 수집 파이프라인에서 처리 규칙이 적용되는 위치를 이해하려면 [Adobe Analytics의 데이터 처리 순서](/help/technotes/processing-order.md)를 참조하세요.
* **인코딩**: 거의 모든 경우에 UTF-8 인코딩을 사용하십시오.
* **대소문자 구분**: 처리 규칙의 문자열 비교는 대소문자를 구분하지 않습니다. 값을 덮어쓰는 데 사용하는 문자열 값은 변수를 직접 채우는 것과 동일한 규칙을 사용합니다.
* **단일 보고서 세트**: 처리 규칙을 편집할 때 하나의 보고서 세트에만 적용됩니다. 보고서 세트 관리자에서 여러 보고서 세트를 선택하면 단일 보고서 세트가 강제로 선택됩니다. 원하는 처리 규칙을 만들거나 편집한 후에는 [해당 규칙을 다른 보고서 세트에 복사](pr-copy.md)할 수 있습니다.
* **데이터 제외 없음**: 데이터를 제외하는 것은 처리 규칙의 의도한 기능이 아닙니다. 데이터 수집 수준에서 [`abort`](/help/implement/vars/config-vars/abort.md)을(를) 사용하거나 데이터를 수집한 후 [VISTA 규칙](/help/technotes/vista.md)을(를) 사용하는 것이 좋습니다.
* **사용 가능한 변수**: 처리 규칙에서 일부 차원과 지표를 사용할 수 있는 것은 아닙니다. 지원되는 항목의 전체 목록은 [처리 규칙에 사용할 수 있는 차원 및 지표](pr-variables.md)를 참조하십시오.
* **허용되는 규칙 수**: 각 보고서 세트에는 최대 150개의 규칙이 포함될 수 있습니다. 각 규칙에는 최대 30개의 조건이 포함될 수 있습니다.

>[!MORELIKETHIS]
>
>![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [처리 규칙을 사용하여 컨텍스트 데이터 변수를 prop 및 eVar에 매핑](https://experienceleague.adobe.com/ko/docs/analytics-learn/tutorials/implementation/implementation-basics/map-contextdata-variables-into-props-and-evars-with-processing-rules){target="_blank"}
