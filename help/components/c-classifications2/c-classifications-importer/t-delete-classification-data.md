---
description: 분류 데이터를 삭제하거나 제거하는 방법을 설명하는 단계입니다.
solution: Analytics
subtopic: Classifications
title: 분류 데이터 삭제
topic: Admin tools
uuid: 5b1b0ac7-ee52-4fd8-b98e-25283595cf0c
translation-type: tm+mt
source-git-commit: e526a38415135440f666ecadd73c34920c0c4c1d

---


# 분류 데이터 삭제

경우에 따라 분류 데이터를 업로드한 후 제거해야 합니다. 제거할 내용에 따라 `~empty~` 또는 `~deletekey~`을 사용합니다.

## 분류 데이터를 제거하는 절차

분류 데이터를 제거하면 해당 셀을 포함하거나 포함하는 분류 파일을 업로드하는 `~empty~` 작업이 `~deletekey~` 포함됩니다.

1. Click **[!UICONTROL Admin]** &gt; **[!UICONTROL Classification Importer]**.
1. Click **[!UICONTROL Browser Export]**.
1. 분류 데이터를 제거할 보고서 세트 및 데이터 세트를 선택합니다.
1. Adjust any optional settings to filter specific data you're looking for, then click **[!UICONTROL Export File]**.
1. 파일이 다운로드되면 파일을 열고 분류 값을 `~empty~` 또는 으로 바꿉니다 `~deletekey~`.
1. 파일을 탭으로 구분된 텍스트 파일로 저장합니다.
1. 파일 **[!UICONTROL 가져오기를]**&#x200B;클릭하고 저장된 분류 파일을 다시 Adobe Analytics에 업로드합니다.

## 개별 분류 값 삭제

여러 분류가 동일한 변수에 속할 수 있습니다. 예를 들어, eVar1의 두 가지 분류를 가질 수 있습니다. 하나의 분류된 값만 제거하려면 분류 값을 로 바꿉니다 `~empty~`. 예:

| 인벤토리 SKU(eVar8) | 인벤토리 이름 | 재고 범주 |
| --- | --- | --- |
| 857467 | V목 스웨터 | 여성복 |
| 948203 | 발목 팔찌 | 보석류 |
| 174391 | 흰색 코르두로이 바지 | `~empty~` |

인벤토리 카테고리 분류 `~empty~` 아래에서 을 사용하면 여전히 인벤토리 이름 분류에 대한 데이터가 유지됩니다. 이 `~empty~` 값은 해당 셀에 대한 분류 데이터만 삭제합니다.

## 전체 분류 행 삭제

모든 `~deletekey~` 열에서 전체 분류 행을 삭제합니다. 예:

| 인벤토리 SKU(eVar8) | 인벤토리 이름 | 재고 범주 |
| --- | --- | --- |
| 857467 | V목 스웨터 | 여성복 |
| 948203 | 발목 팔찌 | 보석류 |
| 174391 | 흰색 코르두로이 바지 | `~deletekey~` |

인벤토리 카테고리 분류 `~deletekey~` 아래에서 을 사용하면 키 값에 대한 모든 분류 데이터가 삭제됩니다 `174391`. 이것은 행이 절대로 분류되지 않은 것처럼 됩니다.

## 함정 및 팁

* 를 사용하는 `~deletekey~`경우 분류 파일에 행당 하나만 있으면 됩니다.
* `~empty~` 와 `~deletekey~` 정확히 ** 일치해야 합니다. 공백이나 대문자를 사용할 수 없습니다.
* 키 열 내의 값은 삭제할 수 없습니다. 이러한 값은 변수에 직접 전달되고 영구적입니다.
* 하위 분류가 있는 분류 값을 제거하는 경우 해당 하위 분류도 제거됩니다. 분류는 키 값 없이 존재할 수 없으며 하위 분류의 상위는 하위 분류의 키 값입니다.
* 상위 분류를 온전한 상태로 두고 하위 분류를 제거할 수 있습니다.
