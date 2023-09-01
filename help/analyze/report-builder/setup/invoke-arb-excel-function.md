---
description: Report Builder 사용자 인터페이스에 액세스하지 않고 Report Builder 기능과 함께 Microsoft Excel을 사용하는 방법을 알아봅니다.
title: Report Builder 함수와 함께 Microsoft Excel을 사용하는 방법 알아보기
uuid: 5342cc4f-085d-4a2d-a498-38b00a3ef4d3
feature: Report Builder
role: User, Admin
exl-id: b412f2b5-affe-4297-af4b-85e8c6dfd257
source-git-commit: 66b7de0b008364e47253d319785c204ca479ab26
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 43%

---

# Microsoft Excel에서 Report Builder 함수 사용

Report Builder 사용자 인터페이스에 액세스하지 않고도 Report Builder 기능을 사용하여 기능에 액세스할 수 있습니다.

예를 들어 다른 소스에서 Excel로 가져온 데이터를 기반으로 입력 필터를 사용하여 Report Builder 요청을 자동으로 새로 고치려면 RefreshRequestsInCellsRange(..) 문자열을 사용합니다. 함수의 두 번째 매개 변수와 함께 세 보고서 중 어느 보고서로든 데이터를 보내도록 구성할 수 있습니다. 모든 호출은 비동기적으로 수행되며 즉시 반환되고 완전히 실행될 때까지 기다리지 않습니다.

**요구 사항**

* Report Builder 5.0 이상이 필요합니다.

다음 표에는 노출된 함수가 나열되어 있습니다.

| 함수 이름 | 유형 | 설명 |
|:---| --- | ---|
| AsyncRefreshAll() | 문자열 | 통합 문서에 있는 모든 Report Builder 요청을 새로 고칩니다. |
| AsyncRefreshRange(string rangeAddressInA1Format) | 문자열 | 지정된 셀 범위 주소에 있는 모든 Report Builder 요청을 새로 고칩니다(&quot;Sheet1!A2:A10&quot;과 같이 A1 형식으로 셀 범위를 나타내는 문자열 표현식). |
| AsyncRefreshRangeAltTextParam() | 문자열 | Ms 양식 컨트롤의 대체 텍스트를 통과하는 지정된 셀 범위에 있는 모든 Report Builder 요청을 새로 고칩니다. |
| AsyncRefreshActiveWorksheet() | 문자열 | 활성 워크시트에 있는 모든 Report Builder 요청을 새로 고칩니다. |
| AsyncRefreshWorksheet(string worksheetName) | 문자열 | 지정된 워크시트(탭에 나타나는 워크시트 이름)에 있는 모든 Report Builder 요청을 새로 고칩니다. |
| AsyncRefreshWorksheetAltTextParam(); | 문자열 | Ms 양식 컨트롤의 대체 텍스트를 통과하는 특정 워크시트 이름에 있는 모든 Report Builder 요청을 새로 고칩니다. |
| tring GetLastRunStatus() | 문자열 | 마지막 실행의 상태를 설명하는 문자열을 반환합니다. |

Report Builder 기능에 액세스하려면 **[!UICONTROL 공식]** > **[!UICONTROL 함수 삽입]**. 검색 필드를 사용하여 기능을 검색하거나 범주를 선택하여 해당 범주에 있는 기능을 나열합니다.

![카테고리 목록이 확장된 기능 삽입 창을 보여 주는 스크린샷입니다.](assets/arb_functions.png)

## 예 {#section_034311081C8D4D7AA9275C1435A087CD}

다음 예제는 *셀 P5의 값이 텍스트이거나 비어 있으면 셀 P9에 있는 범위를 새로 고칩니다*.

```
=IF(OR(ISTEXT(P5),ISBLANK(P5)),AsyncRefreshRange("P9"),"")
```

## Report Builder 함수와 컨트롤 서식 사용 {#section_26123090B5BD49748C8D8ED7A1C5ED84}

만든 컨트롤에 매크로를 지정할 수 있으며 이 컨트롤은 통합 문서 요청을 새로 고치는 함수가 될 수 있습니다. 예를 들어 함수 AsyncRefreshActiveWorksheet는 워크시트의 모든 요청을 새로 고칩니다. 그러나 특정 요청만 새로 고침하는 경우가 있습니다.

1. 매크로 매개 변수를 설정합니다.
1. 컨트롤을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Assign Macro]**.
1. Report Builder 함수 이름을 입력합니다(매개 변수 또는 괄호 없음).

![매크로 할당 창을 보여 주는 스크린샷입니다.](assets/assign_macro.png)

## 컨트롤 서식을 사용하여 Report Builder 함수에 매개 변수 전달 {#section_ECCA1F4990D244619DFD79138064CEF0}

매개 변수를 사용하는 두 함수는 Format Control에 사용할 수 있습니다. 다음을 사용해야 합니다. **대체 텍스트:** 필드:

* AsyncRefreshRange(string rangeAddressInA1Format)
* AsyncRefreshWorksheet(string worksheetName)

컨트롤 서식을 사용하여 Report Builder 함수에 매개 변수를 전달하려면

1. 컨트롤을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL 컨트롤 서식]**&#x200B;을 선택합니다.

   ![형식 제어를 보여주는 스크린샷이 선택되었습니다.](assets/format_control.png)

1. **[!UICONTROL 대체 텍스트]** 탭을 클릭합니다.

   ![대체 텍스트 탭과 대체 텍스트: 필드를 보여 주는 스크린샷입니다.](assets/alt_text.png)

1. **[!UICONTROL 대체 텍스트]**&#x200B;에서 새로 고치려는 셀 범위를 입력합니다.
1. 아래의 Report Builder 매개 변수 목록을 엽니다. **[!UICONTROL 공식]** > **[!UICONTROL 함수 삽입]**> **[!UICONTROL Adobe.ReportBuilder.Bridge]**.

1. AltTextParam으로 끝나는 두 함수 중 하나를 선택하고 **[!UICONTROL 확인]**&#x200B;을 클릭합니다.
