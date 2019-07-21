---
description: 예약된 작업 관리자에 대한 필드 설명입니다.
seo-description: 예약된 작업 관리자에 대한 필드 설명입니다.
seo-title: 예약된 작업 관리자
solution: Analytics
title: 예약된 작업 관리자
topic: Report Builder
uuid: dec 259 f 0-2 a 04-4 c 94-abbc -5008 cf 2 f 1 cb 8
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 예약된 작업 관리자

예약된 작업 관리자에 대한 필드 설명입니다.

예약된 작업 관리자를 사용하면 수신자, 일정 세부 사항 및 파일 형식과 함께, 기존의 예약된 보고서 목록을 확인할 수 있고, 실행에 실패한 예약된 통합 문서를 다시 활성화할 수도 있습니다.

<table id="table_21B07A0B5F1D4435A4E882E45A7A6B6E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 필드 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>예약된 보고서 </b>탭 </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>보고서 이름 </p> </td> 
   <td colname="col2"> <p>예약된 작업의 이름을 가리킵니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 이메일/FTP </p> </td> 
   <td colname="col2"> <p>수신자의 이메일 또는 FTP 주소. </p> <p>참고: [이메일]을 선택한 경우, 1MB가 넘는 보고서는 자동으로 이메일에 .zip 파일로 첨부됩니다. 이 기능은 첨부 파일의 크기를 작게 유지하는 데 도움이 되며, 비활성화할 수 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>게시 옵션 </p> </td> 
   <td colname="col2"> <p>Power BI 게시 옵션 중 하나가 선택된 경우 이 열에 Power BI가 나열됩니다. <a href="../../analyze/report-builder/c-publish-power-bi/integration-power-bi.md#concept_0C4105AA10F9460A872C2489C9CD7945" format="dita" scope="local"> Power BI 게시 옵션</a> 중 하나가 선택되어 있을 경우 Power BI가 나열됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>예약 </p> </td> 
   <td colname="col2"> <p>예약된 전달 유형. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 파일 형식 </p> </td> 
   <td colname="col2"> <p> Excel, PDF, HTML 등과 같은 보고서의 전달 형식. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>다시 활성화 </p> </td> 
   <td colname="col2"> <p>예약된 통합 문서가 실행되지 않으면, Report Builder는 15분마다 두 번 더 통합 문서 실행을 시도합니다. 이 시도가 세 번 실패하면, Report Builder는 예약을 비활성화하고 <span class="wintitle">다시 활성화</span> 단추를 표시합니다. 통합 문서를 다시 활성화하면 예약된 전달이 비활성화된 시점부터 다시 시작됩니다. </p> <p>예를 들어, 예약된 통합 문서가 14일 전에 비활성화되었고 오늘 다시 활성화하면 모든 누락된 날들에 대해 실행되고 14회 전달됩니다. 통합 문서가 누락된 날들에 대해 전달되기를 원하지 않을 경우 예약된 통합 문서를 삭제한 다음 동일한 예약 매개 변수를 사용하여 새로운 예약된 통합 문서를 만들 수 있습니다. </p> <p> <p>참고: 시스템이 비활성화한 이유를 모른다면 통합 문서를 다시 활성화해서는 안 됩니다. 한 가지 문제 해결 방법은 비활성화된 통합 문서를 다운로드하고 클라이언트 측에서 새로 고치는 것입니다. 오류가 표시되지 않는다면 다시 활성화할 수 있습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>마지막으로 보냄 </p> </td> 
   <td colname="col2"> <p>보고서를 마지막으로 보낸 날짜 및 시간입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>수신자 </b>탭 </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>수신자 이메일 </p> </td> 
   <td colname="col2"> 보고서의 이메일 수신자. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>보고서 </p> </td> 
   <td colname="col2"> 각 수신자에게 보내진 보고서. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>보고서 내역</b> 탭 </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>파일 이름 </p> </td> 
   <td colname="col2"> 예약된 작업의 이름을 가리킵니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>날짜 </p> </td> 
   <td colname="col2"> 보고서를 마지막으로 보낸 날짜 및 시간입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>상태 </p> </td> 
   <td colname="col2"> 보고서가 전송되었는지 또는 전송되지 않았는지를 나타냅니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>이메일/FTP </p> </td> 
   <td colname="col2"> 보고서 수신자의 이메일 또는 FTP 주소. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>파일 형식 </p> </td> 
   <td colname="col2"> Excel, PDF, HTML 등과 같은 보고서의 전달 형식. </td> 
  </tr> 
 </tbody> 
</table>
