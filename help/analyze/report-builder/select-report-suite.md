---
title: Report Builder에서 보고서 세트 선택
description: Report Builder에서 보고서 세트를 선택하는 방법을 알아봅니다.
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: 96e24d5d-78fb-4e5c-8513-c5fe221d0aeb
TQID: https://experienceleague.adobe.com/eqAH1gQYgJ05VVa7THd7taOB7S3mhzyOk-29zQHoIxM
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2:
  - id: ac8a38fa-dec3-4581-8f64-178fde9f64e8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 383
ht-degree: 1%

---

# 보고서 세트 선택

드롭다운 메뉴에서 보고서 세트를 선택하거나 셀에서 보고서 세트를 선택하고 데이터 블록을 새 보고서 세트로 자동으로 업데이트할 수 있습니다.

## 셀에서 보고서 세트 선택

셀에서 보고서 세트를 선택하면 다른 보고서 세트를 사용하여 데이터 블록을 쉽게 새로 고칠 수 있습니다. 별도의 데이터 블록을 사용하여 완전히 새로운 보고서를 작성하는 대신 셀에서 선택한 보고서 세트로 데이터 블록을 새로 고칠 수 있습니다.

다음과 같은 경우 셀에서 보고서 세트를 선택하면 유용합니다.

* 구조가 유사하거나 동일한 여러 보고서 세트입니다.
* 사용자 지정된 구성 요소 및 레이아웃을 포함하는 복잡한 데이터 블록 형식입니다.

셀에서 보고서 세트를 선택하려면 먼저 데이터 블록을 빌드하고 데이터 블록 외부의 셀에 여러 보고서 세트를 할당합니다. 그런 다음 **[!UICONTROL 셀의 보고서 세트]** 패널을 사용하여 다른 보고서 세트의 데이터 블록을 새로 고칩니다.

1. 데이터 블록을 만듭니다. 데이터 블록 만들기에 대한 자세한 내용은 [데이터 블록 만들기](/help/analyze/report-builder/create-a-data-block.md)를 참조하십시오.

1. **[!UICONTROL 보고서 세트]**&#x200B;에서 ![DataViewSelector](/help/assets/icons/DataViewSelector.svg)을(를) 선택하십시오.

1. 데이터 블록 외부의 ![DataBlockSelector](/help/assets/icons/DataBlockSelector.svg)을(를) 사용하여 셀을 선택합니다.

1. 드래그 앤 드롭을 사용하여 **[!UICONTROL 셀에서 하나 이상의 보고서 세트를 추가]**&#x200B;하여 보고서 세트에 추가할 보고서 세트를 선택하십시오. 또는 보고서 세트를 두 번 선택하여 **[!UICONTROL 포함된 보고서 세트]** 목록에 추가할 수 있습니다.

   * ![검색](/help/assets/icons/Search.svg) **[!UICONTROL _보고서 세트 선택_]**&#x200B;을 사용하여 보고서 세트를 검색할 수 있습니다.
   * ![MoreSmall](/help/assets/icons/MoreSmall.svg)을 사용하여 컨텍스트 메뉴를 열면 **[!UICONTROL 포함된 보고서 세트]** 목록에서 보고서 세트를 위 또는 아래로 이동할 수 있습니다.
   * ![CrossSize75](/help/assets/icons/CrossSize75.svg)을(를) 사용하여 **[!UICONTROL 포함된 보고서 세트]** 목록에서 보고서 세트를 삭제하십시오.

   ![셀에서 보고서 세트 선택](assets/dataviews-from-a-cell.png){zoomable="yes"}

1. **[!UICONTROL 적용]**&#x200B;을 선택하여 선택한 셀에 선택한 보고서 세트를 적용합니다.


## 셀에서 보고서 세트 변경

1. 시트에서 보고서 세트 셀 위치를 선택합니다.
1. Report Builder 허브에서 **[!UICONTROL 빠른 편집]**&#x200B;의 **[!UICONTROL 셀의 보고서 세트]** 링크를 선택합니다.
1. **[!UICONTROL 보고서 세트]** 드롭다운 메뉴에서 보고서 세트를 선택합니다.

   ![셀에서 보고서 세트 변경](assets/change-data-view-from-cell.png){zoomable="yes"}
1. 선택 사항입니다. 변경 시 **[!UICONTROL 데이터 블록 새로 고침]**&#x200B;을 선택합니다.

1. **[!UICONTROL 적용]**&#x200B;을 선택합니다. Report Builder은 선택한 보고서 세트를 기반으로 데이터 블록을 새로 고칩니다.
