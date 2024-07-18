---
title: Report Builder에서 Visual Basic 매크로를 사용하는 방법
description: VBA 매크로를 사용하여 Excel 통합 문서와 Report Builder의 기능을 확장하는 방법을 알아봅니다.
feature: Report Builder
role: User, Admin
exl-id: 0d92bce2-22ae-4b0c-af1d-3d12f2041ddf
source-git-commit: 66b7de0b008364e47253d319785c204ca479ab26
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 64%

---

# Report Builder의 Visual Basic 매크로

VBA 매크로는 Excel 통합 문서를 새로 고치는 데 도움이 되는 기능을 제공합니다. Visual Basic에서는 통합 문서, Excel 및 Windows에 액세스할 수 있습니다.

VBA 매크로를 실행하려면 먼저 최신 버전의 Report Builder을 실행하고 로그인해야 합니다.

>[!IMPORTANT]
>
>보안상의 이유로 매크로를 포함하는 통합 문서는 예약할 수 없습니다.

Adobe은 세 가지 Report Builder API 메서드를 지원합니다.

## `RefreshAllReportBuilderRequests()`

`RefreshAllReportBuilderRequests()` 매크로는 활성 통합 문서에서 모든 Report Builder 요청을 새로 고침합니다. 이 매크로는 제품 ID를 통해 Report Builder COM 추가 기능을 호출한 다음 `RefreshAllRequests()` API 명령을 호출합니다.

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

`RefreshAllReportBuilderRequestsInActiveWorksheet()` 매크로는 활성 워크시트에서 모든 Report Builder 요청을 새로 고침합니다. `RefreshWorksheetRequests()` API 호출은 워크시트 개체를 인수로 사용합니다. Report Builder 요청을 포함하는 모든 워크시트에 대해 이 호출을 사용할 수 있습니다.

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

`RefreshAllReportBuilderRequestsInCellsRange()` 매크로는 셀 출력이 지정된 셀 범위를 지나는 모든 Report Builder 요청을 새로 고침합니다. 이 예에 사용된 셀 범위는 활성 상태 통합 문서 내 &quot;데이터&quot; 워크시트의 `B1:B54` 범위를 가리킵니다. 범위 표현식은 지원되는 모든 Excel 범위 표현식을 지원합니다.

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
