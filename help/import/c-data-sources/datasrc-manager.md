---
description: 보고서 세트의 데이터 소스를 생성하고 관리하며 사용 현황을 볼 수 있습니다.
seo-description: 보고서 세트의 데이터 소스를 생성하고 관리하며 사용 현황을 볼 수 있습니다.
seo-title: 데이터 소스 관리자
solution: Analytics
subtopic: Data Sources
title: 데이터 소스 관리자
topic: 개발자 및 구현
uuid: CCFA 4 A 1 C -7 C 56-421 B -8 EE 6-A 42 B 334659 B 1
translation-type: tm+mt
source-git-commit: 887f48d2ea5f21b7db95a1a8f716f7da9cf43662

---


# 데이터 소스 관리자

보고서 세트의 데이터 소스를 생성하고 관리하며 사용 현황을 볼 수 있습니다.

**[!UICONTROL Analytics]** &gt; **[!UICONTROL 관리]** &gt; **[!UICONTROL 데이터 소스]**.

## 만들기 탭 {#section_74603FDA3D8842E49F1A51624A06DE20}

[!UICONTROL 만들기] 탭에서 현재 선택한 보고서 세트에 대해 새로운 데이터 소스를 구성할 수 있습니다. 데이터 소스를 활성화하면 [!UICONTROL 데이터 소스 마법사]에서 안내하는 데이터 소스 템플릿 생성 프로세스에 따라 데이터 업로드를 위한 FTP 위치를 만듭니다.

[만들기] 탭에서 선택하는 사항에 따라 만들어지는 템플릿의 초기 필드가 달라집니다. 자세한 내용은 다음을 참조하십시오. [가져오기 파일 템플릿 생성](../../import/c-data-sources/datasrc-template/t-datasrc-creating-data-sources-file.md#task_A2F150D9DC1A4D338E878534FA506267).

## 관리 탭 {#section_DD559A6701CA45F1A85E56F840F48DBE}

<table id="table_F74696EC855441328CFE0BF49C20D9B0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>옵션 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>처리 다시 시작 </p> </td> 
   <td colname="col2"> <p>오류나 경고로 중단된 데이터 소스 처리를 다시 시작합니다. 다음 오류가 발생할 때까지 처리가 계속됩니다. 데이터 소스는 <span class="uicontrol">오류 시 처리 중지</span>를 선택하는 경우에만 데이터 소스 파일 처리를 중지합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>처리 완료 </p> </td> 
   <td colname="col2"> <p>파일에서 열려 있는 방문을 닫도록 데이터 소스에 지시하고 데이터 소스 파일 처리를 완료로 간주하여 마칩니다. 이 옵션은 방문이 여러 데이터 소스 파일에서 발생한 경우 유용합니다. 이것은 <a href="../../import/c-data-sources/c-datasrc-types/datasrc-full-processing.md#concept_975B1BB9981D49139B4EE09C78CDE6ED" type="concept" format="dita" scope="local"> 전체 처리</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>비활성화 </p> </td> 
   <td colname="col2"> <p> 데이터 소스를 비활성화하면 데이터 소스가 삭제됩니다. 서버의 파일 처리가 시작된 경우 완료될 때까지 처리를 계속합니다. 아직 처리가 시작되지 않은 파일은 처리되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>오류/경고 시 처리 중지 </p> </td> 
   <td colname="col2"> <p> 오류가 발생하면 처리를 중지하도록 데이터 소스 처리 엔진에 지시합니다. [처리 다시 시작]을 선택해야 데이터 소스가 처리를 재시작합니다. [경고 시 처리 중지] 옵션은 <a href="../../import/c-data-sources/c-datasrc-types/datasrc-full-processing.md#concept_975B1BB9981D49139B4EE09C78CDE6ED" type="concept" format="dita" scope="local"> 전체 처리</a>. </p> <p>데이터 소스에 파일 오류가 발생하면 오류를 알리는 메시지를 받게 됩니다. 시스템은 오류가 발생한 데이터 소스 파일을 FTP 서버의 <span class="filepath">files_with_errors</span>라는 폴더로 이동시킵니다. 문제를 해결했으면 처리를 위해 데이터 소스 파일을 다시 전송합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>구성 </p> </td> 
   <td colname="col2"> <p>데이터 소스 템플릿 또는 해당 데이터 소스에 특정한 다른 설정을 변경할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>FTP 정보 </p> </td> 
   <td colname="col2"> <p>해당 데이터 소스에 대한 FTP 정보를 표시합니다. 이 정보를 사용하여 데이터 소스 템플릿에 액세스하고 데이터 소스 데이터를 전송합니다.  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>파일 이름 </p> </td> 
   <td colname="col2"> <p>업로드된 파일의 이름 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>상태 </p> </td> 
   <td colname="col2"> <p> 파일의 현재 상태. 가능한 상태 값은 다음과 같습니다. </p> 
    <ul id="ul_56A0BF8C1BE249F6BB39B0D11DA3997F"> 
     <li id="li_BAB359E08EDE4E0298C0362258789603">큐에서(1/3단계): 파일이 존재하지만 처리를 시작하지 않았습니다. 30분 안에 파일이 표시되지 않으면 연결된 <span class="filepath">.fin</span> 파일이 있는지 확인하십시오. </li> 
     <li id="li_A09A14F42CB74F01B694799740B3DA17">준비 중(2/3단계): 파일 오류나 경고를 검사하는 중입니다. </li> 
     <li id="li_793FDCDB64CF434D82CAF5B6E9BDE557">처리 중(3/3단계): 파일을 처리하는 중입니다. </li> 
     <li id="li_1D8C4B241FF0453EAF7DDFD8354C5573">실패: 오류로 인해 파일을 처리하지 않았습니다. </li> 
     <li id="li_A52507602FB4492B83A70AF6449A539A">성공: 파일을 성공적으로 처리했습니다. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 파일 로그 탭 {#section_B7AC7EE8CAD740A59DD53CF1919373F0}

파일 로그에는 데이터 소스 이름, 데이터 소스 유형, 파일 이름, 수신한 날짜 또는 상태별로 정보를 검색할 수 있는 검색 기능이 포함됩니다. 
