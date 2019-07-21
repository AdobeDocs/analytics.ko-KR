---
description: Report Builder의 요청 관리를 위한 필드 설명
seo-description: Report Builder의 요청 관리를 위한 필드 설명
seo-title: 요청 관리 - 정의
solution: Analytics
title: 요청 관리 - 정의
topic: Report Builder
uuid: 01 B 21 D 0 E-C 870-4 DF 8-95 B 9-F 4 AEF 1 F 4 D 16 B
translation-type: tm+mt
source-git-commit: 6a70b32b576cc7b5b6a6f0037d98e35b3f8c1426

---


# 요청 관리 - 정의

Report Builder의 요청 관리를 위한 필드 설명

## 개요 {#section_75C288C945FA4781A4EDF806711A5660}

[!UICONTROL 요청 관리자]는 활성 통합 문서의 모든 시트 또는 단 한 시트에 대해 만든 모든 요청의 상태를 자세히 볼 수 있도록 해줍니다. 이전 요청이 들어 있는 Excel 스프레드시트에서 사용할 수 있는 셀을 마우스 오른쪽 단추로 클릭하여 요청을 추가, 편집, 새로 고침 및 삭제(일반적으로 [!UICONTROL 요청 마법사] 및 [!UICONTROL 요청 관리자]와 연관된 기능들)할 수도 있습니다.

The [!UICONTROL Request Manager] displays when you click **[!UICONTROL Manage]** ( ![](assets/edit_request.gif) in the Report Builder toolbar.

>[!NOTE]
>
>Adobe Report Builder 에서는 요청이 아닌 동일한 워크시트 내에서만 요청 종속성을 적용합니다. 단일 워크시트 내의 종속성으로 제한하면 신속하게 실행할 수 있습니다.

## 정의 {#section_FD29D8614DE74F32A0027FA130F40304}

<table id="table_0880204181074BDBBA37E3DF2972A672"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 필드 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>모든 시트 </p> </td> 
   <td colname="col2"> <p>활성화 상태의 통합 문서에 있는 모든 시트의 요청을 표시합니다. 특정 시트의 요청을 보려면 이 선택 사항은 끄십시오. 이 선택 사항을 끄면 Excel 보고서의 하단에서 [시트] 탭을 클릭하여 <span class="wintitle">Request Manager</span>의 해당 시트와 관련된 요청을 표시해야 합니다. 확인란 옆에 있는 레이블은 통합 문서에서 현재 표시된 시트를 가리킵니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sheet </p> </td> 
   <td colname="col2"> <p>통합 문서에 있는 시트의 이름을 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>보고서 세트 </p> </td> 
   <td colname="col2"> <p>보고서 세트의 이름을 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>날짜 범위 </p> </td> 
   <td colname="col2"> <p>보고서의 지정된 날짜 범위를 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>세부기간 </p> </td> 
   <td colname="col2"> <p>요청의 세부기간을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 마지막 실행 </p> </td> 
   <td colname="col2"> <p>요청이 Report Builder에 의해 마지막으로 처리된 날짜를 지정합니다. 진단 메시지는 해당하는 경우 <span class="wintitle">마지막 실행</span> 열의 이 테이블에도 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>추가 </p> </td> 
   <td colname="col2"> <p>요청 마법사 대화 상자를 표시합니다. see <a href="../../../analyze/report-builder/data-requests/t-create-a-data-request.md#task_65B453C8F015429A8EA73A1B64025B6C" type="task" format="dita" scope="local"> 데이터 요청 만들기</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>편집 </p> </td> 
   <td colname="col2"> <p> (또는 [여러 개 편집]) 선택한 요청을 편집합니다. 시스템이 <span class="wintitle">요청 마법사</span> 대화 상자를 표시합니다. See <a href="../../../analyze/report-builder/manage-requests/t-edit-multiple-requests.md#task_70A13DBE43CD4BBEBE1B62459ADB3AD1" type="task" format="dita" scope="local"> Edit Multiple Requests</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>삭제 </p> </td> 
   <td colname="col2"> <p>요청을 삭제합니다. 여러 개의 선택된 요청을 삭제할 수 있습니다. 요청을 선택하고 키보드의 Delete 키를 눌러 목록에서 요청을 삭제할 수도 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 모두 선택 </p> </td> 
   <td colname="col2"> <p>모든 요청을 선택합니다. <span class="wintitle">Request Manager</span>가 요청 목록 하단에서 선택한 요청의 수를 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>셀에서 </p> </td> 
   <td colname="col2"> <p>워크시트의 요청에 대한 데이터를 가져옵니다. 요청이 활성 상태 워크시트에 있는 현재 선택된 셀과 연결되어 있을 경우 목록에 있는 연결된 요청이 선택됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 새로 고침 </p> </td> 
   <td colname="col2"> <p>단일 요청이나 선별된 요청들을 새로 고칩니다. ( <a href="../../../analyze/report-builder/manage-requests/t-refresh-a-request.md#task_96556DB051A2479A955999D3837EE609" type="task" format="dita" scope="local"> 요청 새로 고침</a>.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>목록 새로 고침 </p> </td> 
   <td colname="col2"> <p>표시된 모든 요청을 새로 고칩니다. 모든 요청을 새로 고칠 때 정보를 서버에서 보고서까지 업데이트하는 시간은 보고서에 있는 요청의 복잡성에 비례합니다. 매우 큰 보고서의 경우 모든 요청을 새로 고치는 데에는 수 분이 필요할 수 있습니다. 이러한 이유로 가장 긴박한 요청들을 개별적으로 업데이트하고 시간적으로 덜 중요한 다른 때 <span class="wintitle">모두 새로 고침</span>을 선택할 수 있습니다. </p> <p> <p>참고: 여러 개의 요청이 들어 있는 워크시트를 새로 고치는 경우 <span class="wintitle">요청 관리자</span>에서 종종 결과를 확인하는 것이 좋습니다. 요청이 실패하는 경우 진단 열의 오류 메시지가 오류의 원인을 찾는 데 도움이 됩니다. 대부분의 경우 요청이 실패하면 오류 메시지가 표시되지만 종종 오류 메시지가 생성되지 않는 경우도 있습니다. 참조가 들어 있는 셀에 있는 데이터가 새로 고침으로 업데이트되지 않거나 업데이트로 인해 셀의 데이터가 지워질 수 있습니다. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

