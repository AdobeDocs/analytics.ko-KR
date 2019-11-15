---
description: 브라우저를 사용하여 분류 데이터를 가져올(다운로드) 수 있습니다. 이 방법은 분류 데이터 업로드를 단일 보고서 세트로 제한합니다
solution: Analytics
subtopic: Classifications
title: 브라우저 가져오기
topic: Admin tools
uuid: 56dfbf4c-36e6-49f4-b5cb-8ab714432825
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 브라우저 가져오기

브라우저를 사용하여 분류 데이터를 가져올(다운로드) 수 있습니다. 이 방법은 분류 데이터 업로드를 단일 보고서 세트로 제한합니다

## 브라우저 가져오기 {#concept_314FB3D5FD5A439B9CFEDE37A3337BA7}

브라우저를 사용하여 분류 데이터를 가져올(다운로드) 수 있습니다. 이 방법은 분류 데이터 업로드를 단일 보고서 세트로 제한합니다

**[!UICONTROL 관리]** &gt; **[!UICONTROL 분류 가져오기]**

## 분류 브라우저 가져오기 - 필드 설명 {#section_F628C47081DA4026A4D30E3D3454B1DA}

<table id="table_7FC7E510E7E74C2D9E8F316C5C6B66DB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 요소 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 보고서 세트 선택 </td> 
   <td colname="col2"> <p>분류 데이터를 가져오려는 보고서 세트입니다. 가져오기 데이터 파일은 보고서 세트의 데이터 세트 형식과 일치해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 분류할 데이터 세트 </td> 
   <td colname="col2"> <p>분류를 받을 데이터 세트입니다. 분류에 대해 구성된 보고서 세트의 모든 보고서가 드롭다운 목록에 포함됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 가져올 파일 선택 </td> 
   <td colname="col2"> <p>업로드하려는 가져오기 데이터 파일의 위치를 찾아봅니다. </p> <p>참고: 업로드 파일 크기 제한은 1MB입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 충돌 시 데이터 덮어쓰기 </td> 
   <td colname="col2"> <p>가져온 데이터와 충돌하는 기존 데이터를 자동으로 덮어씁니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 가져오기 완료 후 자동으로 분류 파일 다운로드 </td> 
   <td colname="col2"> <p>새로 업로드한 분류 데이터로 데이터 세트를 나타내는 탭 구분 파일을 자동으로 다운로드합니다. 가져오기 작업 때문에 고유 ID가 만들어지거나 오류가 발생하는 경우 Adobe에서 이 파일을 자동으로 만듭니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 브라우저를 통한 분류 가져오기 {#task_D7D51CB6FB35437AB68599B1B23FEAC1}

<!-- 

t_upload_a_saint_data_file_via_web_browser.xml

 -->

1. Click **[!UICONTROL Admin]** &gt; **[!UICONTROL Classification Importer]**.
1. Click **[!UICONTROL Import File]**.
1. 브라우저 **[!UICONTROL 가져오기]** 필드를 구성합니다.
1. Click **[!UICONTROL Import File]**.
1. 처리 메시지가 표시되는 상태 창을 확인하십시오.
1. (Conditional) If you selected **[!UICONTROL Automatically Download Classification File After Upload is Complete]**, specify where you want to store the resulting file when processing completes.
>가져오기에 성공하면 해당하는 변경 내용이 내보내기에 바로 표시됩니다. 하지만 보고서에서 데이터를 변경하면 브라우저 가져오기를 사용하는 경우 최대 4시간, FTP 가져오기를 사용하는 경우 최대 24시간이 걸립니다.

