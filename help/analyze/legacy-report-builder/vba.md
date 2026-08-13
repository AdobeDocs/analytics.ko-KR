---
title: Report Builder에서 Visual Basic 매크로를 사용하는 방법
description: VBA 매크로를 사용하여 Excel 통합 문서 및 Report Builder의 기능을 확장하는 방법을 알아봅니다.
feature: Report Builder
role: User, Admin
exl-id: 0d92bce2-22ae-4b0c-af1d-3d12f2041ddf
TQID: https://experienceleague.adobe.com/RxOpojtJn2vi5uMO8CGzCCm7FcPp4qVwbH-XTEBSRsY
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 195
ht-degree: 64%

---

# Report Builder의 Visual Basic 매크로

{{legacy-arb}}

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
