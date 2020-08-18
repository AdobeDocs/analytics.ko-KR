---
title: Report Builder의 Visual Basic 매크로
description: VBA를 사용하여 Excel 통합 문서 및 Report Builder의 기능을 확장합니다.
translation-type: tm+mt
source-git-commit: b569f87dde3b9a8b323e0664d6c4d1578d410bb7
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---


# Report Builder의 Visual Basic 매크로

Visual Basic 매크로라고도 하는 VBA 매크로를 사용하면 Microsoft Excel에서만 할 수 없는 방식으로 통합 문서를 조작할 수 있습니다. Visual Basic은 통합 문서, Excel 및 Windows에도 액세스할 수 있습니다.

Adobe은 세 가지 Report Builder API 메서드를 지원합니다. 최신 버전의 리포트 빌더가 설치되어 있는지 확인하고 매크로를 실행하기 전에 로그인합니다.

>[!IMPORTANT]
>
>보안상의 이유로 매크로를 포함한 통합 문서는 예약할 수 없습니다.

## `RefreshAllReportBuilderRequests()`

The `RefreshAllReportBuilderRequests()` macro refreshes all Report Builder requests in the active workbook. 제품 ID를 통해 Report Builder COM Add-in을 호출한 다음 `RefreshAllRequests()` API 명령을 호출합니다.

```vba
Sub RefreshAllReportBuilderRequests()
 
 Dim addIn As COMAddIn
 Dim automationObject As Object
 Dim success As String
 Set addIn = Application.COMAddIns("ReportBuilderAddIn.Connect")
 Set automationObject = addIn.Object
 success = automationObject.RefreshAllRequests(ActiveWorkbook)
 
End Sub
```

## `RefreshAllReportBuilderRequestsInActiveWorksheet()`

The `RefreshAllReportBuilderRequestsInActiveWorksheet()` macro refreshes all Report Builder requests in the active worksheet. API `RefreshWorksheetRequests()` 호출은 워크시트 개체를 인수로 사용합니다. Report Builder 요청이 들어 있는 모든 워크시트에 대해 이 호출을 사용할 수 있습니다.

```vba
Sub RefreshAllReportBuilderRequestsInActiveWorksheet()
 
 Dim addIn As COMAddIn
 Dim automationObject As Object
 Dim success As String
 Set addIn = Application.COMAddIns("ReportBuilderAddIn.Connect")
 Set automationObject = addIn.Object
 success = automationObject.RefreshWorksheetRequests(ActiveWorkbook.ActiveSheet)
 
End Sub
```

## `RefreshAllReportBuilderRequestsInCellsRange()`

The `RefreshAllReportBuilderRequestsInCellsRange()` macro refreshes all Report Builder requests whose cell outputs intersect the specified range of cells. 이 예에서 사용된 셀 범위는 활성 통합 문서 내 &quot;데이터&quot; 워크시트 `B1:B54` 의 범위를 가리킵니다. 범위 표현식은 지원되는 모든 Excel 범위 표현식을 지원합니다.

```vba
Sub RefreshAllReportBuilderRequestsInCellsRange()
 
 Dim addIn As COMAddIn
 Dim automationObject As Object
 Dim success As String
 Set addIn = Application.COMAddIns("ReportBuilderAddIn.Connect")
 Set automationObject = addIn.Object
 success = automationObject.RefreshRequestsInCellsRange("'Data'!B1:B54")
  
End Sub
```
