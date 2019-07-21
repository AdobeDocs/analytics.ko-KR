---
description: 정의하는 시간 및 파일 형식에 따라 보고서를 전송하도록 예약할 수 있습니다.
seo-description: 정의하는 시간 및 파일 형식에 따라 보고서를 전송하도록 예약할 수 있습니다.
seo-title: 데이터 요청 예약
solution: Analytics
title: 데이터 요청 예약
topic: Report Builder
uuid: F 6 D 8 C 90 F-E 185-4 D 60-8035-F 20 F 74 BFCD 89
translation-type: tm+mt
source-git-commit: 6a70b32b576cc7b5b6a6f0037d98e35b3f8c1426

---


# 데이터 요청 예약

정의하는 시간 및 파일 형식에 따라 보고서를 전송하도록 예약할 수 있습니다.

**데이터 요청을 예약하는 방법**

1. 보고서를 생성하여 저장합니다.
1. On the Report Builder Toolbar, click **[!UICONTROL Schedule]**.

   [!UICONTROL 예약된 보고서] 탭에 남은 작업의 수는 물론 생성한 모든 작업이 요약됩니다.
1. **예약된 보고서** 탭에서 **[!UICONTROL 새로 만들기를 클릭합니다]**.
1. 기본 예약 마법사가 표시됩니다. 

   ![](assets/simple-schedule-wizard.png)

1. [!UICONTROL 기본 예약 마법사]에서 다음 옵션을 구성합니다. 

* **보고서 선택**: 보고서 이름. 새로운 예약된 보고서의 경우 이 필드에는 활성 상태의 통합 문서 이름이 입력되어 있습니다.

<table id="table_6D5B1B832EB0451293F1902E2A1D1068"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 필드 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>보고서 선택 </p> </td> 
   <td colname="col2"> <p>보고서 이름. 새로운 예약된 보고서의 경우 이 필드에는 활성 상태의 통합 문서 이름이 입력되어 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>선택 </p> </td> 
   <td colname="col2"> <p><span class="wintitle">보고서 선택</span> 페이지를 표시합니다. 서버(이전에 예약한 통합 문서가 저장된 곳)나 로컬 시스템에서 보고서를 선택할 수 있습니다. 로컬 드라이브에서 <span class="filepath">.xls</span> 형식의 통합 문서를 선택하면 시스템이 파일을 <span class="filepath">.xlsx</span>로 전환합니다. 이러한 전환 작업의 일부로서 파일은 Excel에서 열려서 활성화됩니다. 예약된 보고서에 대해 선택한 통합 문서의 파일 이름이 현재 Excel에 열려 있는 통합 문서와 동일하면 시스템은 이전에 업로드 한 파일 대신 로컬 파일을 선택합니다. 예약 보관소에서 보고서를 선택하는 경우에는 통합 문서의 사본이 만들어지고 이 사본의 파일 이름은 1로 업데이트되며 새로 만들어진 예약된 통합 문서는 복사된 통합 문서를 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용자 지정 </p> </td> 
   <td colname="col2"> <p>날짜 형식을 사용자 지정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>받는 사람 </p> </td> 
   <td colname="col2"> <p>사용할 수 있을 경우 Outlook 주소록을 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>수신인: 이메일 </p> </td> 
   <td colname="col2"> <p>보고서의 이메일 수신자. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>수신인: 게시 목록 </p> </td> 
   <td colname="col2"> <p>이 회사용의 사용 가능한 배포 목록의 목록을 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Power BI </p> </td> 
   <td colname="col2"> <p>자세한 내용은 <a href="../../analyze/report-builder/c-publish-power-bi/integration-power-bi.md#section_BA137EA92A46483F83BB5C1C40FBA002" format="dita" scope="local">Microsoft Power BI에 통합 문서 게시</a>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>제목 </p> </td> 
   <td colname="col2"> <p>사용자 정의 설명. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>예약 </p> </td> 
   <td colname="col2"> <p> 보고서를 보낼 시기를 지정할 수 있습니다. (즉시, 시간별, 일별, 주별, 월별 및 연도별.) </p> </td> 
  </tr> 
 </tbody> 
</table>

1. **[!UICONTROL 고급 배달 옵션을]** 클릭하여 파일 및 게시 옵션을 구성합니다.

<table id="table_1BA8A5600DE94A33B83B096E69CE15F3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 필드 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>예약</b> 탭 </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>전달 시간 </p> </td> 
   <td colname="col2"> <p>보고서를 즉시 또는 나중에 전달하도록 예약할 수 있습니다. 시각은 컴퓨터에 지정된 시간대를 기준으로 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>되풀이 패턴 </p> </td> 
   <td colname="col2"> <p>선택 사항을 기반으로 보고서를 전송합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>되풀이 범위 </p> </td> 
   <td colname="col2"> <p>보고서 수신을 시작 및 중단할 시기를 지정할 수 있습니다. </p> <p> <p>참고: 현재 기간(주, 월, 분기 또는 년도)의 첫째 날에 보고서를 예약하면 그 첫째 날에 대해서만 데이터를 반환합니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>파일 옵션</b> 탭 </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>파일 형식 </p> </td> 
   <td colname="col2"> <p>전달 형식을 Excel 2007(<span class="filepath">.xlsx</span>) 또는 2003 (<span class="filepath">.xls</span>), <span class="filepath">.pdf</span>,<span class="filepath"> .csv,</span> <span class="filepath">.mht</span>,<span class="filepath"> .txt</span> 및<span class="filepath"> .xml</span> 중에서 선택할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 파일 대상 </p> </td> 
   <td colname="col2"> <p> 이메일 또는 FTP를 지정합니다. 페이지의 선택 사항은 선택 내용에 따라 달라집니다. FTP의 경우 호스트를 외부에서 사용할 수 있도록 해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>게시 목록 </p> </td> 
   <td colname="col2"> <p> 예약된 보고서를 여러 게시 목록에 전송하면 보고서는 각 목록에 대해 한 번씩 실행됩니다. 변수 보고서 세트는 게시 목록에 지정된 보고서 세트로 대체됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>파일 내용 언어 </p> </td> 
   <td colname="col2"> <p>첨부 설명에 사용할 언어를 지정합니다. 한국어, 중국어(간체 또는 번체), 독일어, 프랑스어, 일본어, 브라질 포르투갈어 또는 스페인어를 선택할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>게시 옵션</b> 탭 </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Power BI에 게시 </p> </td> 
   <td colname="col2"> 
    <ul id="ul_40697E4FB2CE4F34B857FBF153D6D6D5"> 
     <li id="li_023E4750814D415EBC899269C9EA5D46"><a href="../../analyze/report-builder/c-publish-power-bi/integration-power-bi.md#section_BA137EA92A46483F83BB5C1C40FBA002" format="dita" scope="local"> Power BI에 통합 문서 게시</a> </li> 
     <li id="li_9B684BE22AF94ABC903405EE83951A80"><a href="../../analyze/report-builder/c-publish-power-bi/integration-power-bi.md#section_E48148793E794169B766C73995897B9F" format="dita" scope="local"> 모든 Report Builder 요청을 Power BI 데이터 세트로 게시</a> </li> 
     <li id="li_7B0BD285BC1749D1B2C65759CA97877B"><a href="../../analyze/report-builder/c-publish-power-bi/integration-power-bi.md#section_6F8422B90D3F4F7EB5D4C97BFFA807AD" format="dita" scope="local"> 형식이 지정된 표를 모두 Power BI 데이터 세트로 게시</a> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>이 Power BI 보고서를 다음과 같이 레이블 지정 </p> </td> 
   <td colname="col2"> <p>레이블 지정 세부 사항 </p> </td> 
  </tr> 
 </tbody> 
</table>

1. **[!UICONTROL 확인을]**&#x200B;클릭한 다음 **[!UICONTROL 종료를]**&#x200B;클릭합니다.

   Report Builder가 [예약된 작업 관리자](../../analyze/report-builder/r-arb-scheduled-reports.md#section_69306B8D833F4DF7BBFA53753B0E6C31)에 예약된 보고서를 표시합니다.
