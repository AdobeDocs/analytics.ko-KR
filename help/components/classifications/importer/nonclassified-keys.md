---
description: 분류되지 않는 키는 분류 보고서에 None으로 레이블이 지정된 단일 라인 항목으로 모두 그룹화됩니다. 이렇게 하면 None을 좀 더 설명적인 이름으로 바꾸는 데 유용할 수 있습니다.
title: 분류되지 않는 키
feature: Classifications
exl-id: 37288c2d-f6f6-4343-87a1-3c3a7b56fe32
source-git-commit: ce7f953b8f7f1f7d0616074454e4401937fcc0c7
workflow-type: ht
source-wordcount: '250'
ht-degree: 100%

---

# 분류되지 않는 키

분류되지 않는 키는 분류 보고서에 None으로 레이블이 지정된 단일 라인 항목으로 모두 그룹화됩니다. 이렇게 하면 None을 좀 더 설명적인 이름으로 바꾸는 데 유용할 수 있습니다.

## 분류되지 않는 키 {#concept_233E51DDF3084FF7B7EA89381C73C5FF}

분류되지 않는 키는 분류 보고서에 *`None`*&#x200B;으로 레이블이 지정된 단일 라인 항목으로 모두 그룹화됩니다. 이렇게 하면 *`None`*&#x200B;을 좀 더 설명적인 이름으로 바꾸는 데 유용할 수 있습니다.

예를 들어 추적 코드에 추적 코드와 연관된 모바일 캠페인 유형을 설명하는 정보가 포함되어 있다고 가정해보겠습니다. 분류(모바일 캠페인 유형)를 사용하여 이러한 추적 코드를 모바일 웹, iOS 애플리케이션, Android 애플리케이션 등과 같은 범주로 그룹화합니다. 일부 캠페인은 모바일 캠페인이 아닐 수 있으므로 모바일 캠페인 유형으로 분류되지 않습니다. 모든 분류되지 않는 추적 코드는 *`None`* ([!UICONTROL 모바일 캠페인 유형] 보고서) 아래에 그룹화됩니다.

## &quot;없음&quot; 분류 키 이름 바꾸기 {#task_8CD595DA82AA44D08CEF002B588C3C30}

<!-- 

t_rename_classification_none.xml

 -->

보고에 *`none`*&#x200B;으로 표시되는 비분류 키의 이름을 바꾸려면 다음 작업을 수행합니다.

1. 가져오기를 사용하여 분류를 로컬 파일로 내보냅니다.
1. 파일에 행을 추가하고 키 열에 `~none~`을 입력합니다.
1. 추가한 행에서 적절한 분류 열에 좀 더 설명적인 이름을 입력합니다.

   이 설명서에 나온 예를 따르려면 [!UICONTROL 모바일 캠페인 유형]이라고 하는 열에 &quot;비모바일 캠페인&quot;을 입력할 수 있습니다.

   이 항목은 [!UICONTROL 모바일 캠페인 유형] 보고서에서 *`None`*&#x200B;에서 *`non-mobile campaign`*&#x200B;로 이름을 바꿉니다.

   ![분류되지 않는 키 예시](/help/components/classifications/importer/assets/non-classified-key.png)

1. [데이터를](/help/components/classifications/importer/import-file.md) 다시 시스템으로 가져옵니다.
