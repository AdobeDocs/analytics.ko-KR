---
description: 분류되지 않는 키는 분류 보고서에 없음으로 레이블이 지정된 단일 라인 항목으로 모두 그룹화됩니다. 이렇게 하면 없음을 좀 더 설명적인 이름으로 바꾸는 데 유용할 수 있습니다.
seo-description: 분류되지 않는 키는 분류 보고서에 없음으로 레이블이 지정된 단일 라인 항목으로 모두 그룹화됩니다. 이렇게 하면 없음을 좀 더 설명적인 이름으로 바꾸는 데 유용할 수 있습니다.
seo-title: 분류되지 않은 키
solution: Analytics
subtopic: 분류
title: 분류되지 않은 키
topic: 관리 도구
uuid: B 73 A 9161-0 C 6 F -4 C 8 D -900 B -54 AB 2 C 36147 C
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 분류되지 않은 키

분류되지 않는 키는 분류 보고서에 없음으로 레이블이 지정된 단일 라인 항목으로 모두 그룹화됩니다. 이렇게 하면 없음을 좀 더 설명적인 이름으로 바꾸는 데 유용할 수 있습니다.

## Non-classified keys {#concept_233E51DDF3084FF7B7EA89381C73C5FF}

분류되지 않는 키는 분류 보고서에 *`None`*. It can be useful to rename *`None`* to something more descriptive.

예를 들어 추적 코드에 추적 코드와 연관된 모바일 캠페인 유형을 설명하는 정보가 포함되어 있다고 가정해봅시다. 분류(모바일 캠페인 유형)를 사용하여 이러한 추적 코드를 모바일 웹, iOS 애플리케이션, Android 애플리케이션 등과 같은 카테고리로 그룹화합니다. 일부 캠페인은 모바일 캠페인이 아닐 수 있으므로 모바일 캠페인 유형으로 분류되지 않습니다. 모든 분류되지 않는 추적 코드는 *`None`*([!UICONTROL 모바일 캠페인 유형] 보고서) 아래에 그룹화됩니다.

## 없음 분류 키 이름 바꾸기 {#task_8CD595DA82AA44D08CEF002B588C3C30}

<!-- 

t_rename_classification_none.xml

 -->

Steps that describe how to rename a non-classified key that displays as *`none`* in reporting.

1. 가져오기를 사용하여 분류를 로컬 파일로 내보냅니다.
1. Add a row to the file, and type [!DNL ~none~] in the Key column.
1. 추가한 행에서 적절한 분류 열에 좀 더 설명적인 이름을 입력합니다. 

   이 설명서에 나온 예를 따르려면 [!UICONTROL 모바일 캠페인 이름]이라고 하는 열에 "비모바일 캠페인"을 입력할 수 있습니다.

   이렇게 입력하면 *`None`* 을 *`non-mobile campaign`*[!UICONTROL 클릭합니다] .
1. [데이터를](../../../components/c-classifications2/c-classifications-importer/import-file.md#concept_F88785E2BDFD448CB5D1DA3491466B0D) 다시 시스템으로 가져옵니다.
