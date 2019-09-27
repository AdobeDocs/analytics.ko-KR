---
description: 데이터 소스를 사용하기 전에 보고서 세트에 대한 요구 사항 정보.
seo-description: 데이터 소스를 사용하기 전에 보고서 세트에 대한 요구 사항 정보.
seo-title: 요구 사항 및 업로드 제한
solution: Analytics
subtopic: 데이터 소스
title: 요구 사항 및 업로드 제한
topic: 개발자 및 구현
uuid: d79fca77-fa0e-4171-b978-cdee5c67d9df
translation-type: tm+mt
source-git-commit: 3c5cc9275c9978caf57e4e29704e23405ac24b65

---


# 요구 사항 및 업로드 제한

데이터 소스를 사용하기 전에 보고서 세트에 대한 요구 사항 정보.

다음 섹션에서는 데이터 소스에 적용되는 제한 및 마케팅 보고 및 분석에 가져온 데이터에 적용되는 제한을 나열합니다.

* [크기 제한](../../import/c-data-sources/datasrc-requirements.md#section_77B06D82CB374FFABD39F7D9A49D8E18)
* [날짜](../../import/c-data-sources/datasrc-requirements.md#section_2B8E69BA1E0B4DEAB4E2034C2B9E16C2)
* [일반](../../import/c-data-sources/datasrc-requirements.md#section_1CD337F660484ABDB7D8CAE96FF46ACF)
* [멀티바이트 지원](../../import/c-data-sources/datasrc-requirements.md#section_96C8D26B21184C3E839865DB6F23EA22)
* [웹 로그 파일 업로드](../../import/c-data-sources/datasrc-requirements.md#section_DD736FC971FE45C89AB310BEDC1FE707)

## 크기 제한 {#section_77B06D82CB374FFABD39F7D9A49D8E18}

* 각 FTP 계정은 모든 파일에 대해 총 50MB의 데이터로 제한됩니다. 크기가 50MB를 초과하는 경우 처리가 일시 중지되며 총 크기가 50MB 아래로 떨어져야 다시 시작됩니다. 

## 날짜 {#section_2B8E69BA1E0B4DEAB4E2034C2B9E16C2}

* 각 달력에 대해 90개의 고유 날짜에 대한 데이터를 업로드할 수 있습니다. 이 제한을 초과하는 경우 업로드가 실패하고 최대 고유 일 수를 초과했다는 오류 메시지가 표시됩니다.
* 현재 또는 이전 날짜의 데이터만 가져올 수 있습니다. 데이터 소스 데이터에 미래 날짜를 사용하지 마십시오.
* 모든 행에는 보고서 그래프 생성 기능을 활성화하도록 지정된 날짜가 있어야 합니다. 행에 날짜가 없으면 데이터 소스에서 오류가 발생하고 파일이 거부됩니다. 날짜/시간 형식은 데이터 소스 유형에 따라 달라집니다.

   * **전체 처리 데이터 소스**:ISO 8601 날짜 형식( `YYYY-MM-DDThh:mm:ss±UTC_offset` 예: `2013-09-01T12:00:00-07:00`) 또는 Unix 시간 형식(1970년 1월 1일 이후 경과한 초)을 사용합니다.

   * **표준 및 통합 데이터 소스**:다음 날짜 형식을 사용합니다. `MM/DD/YYYY/HH/mm/SS` (예: `01/01/2013/06/00/00`)

## 일반 {#section_1CD337F660484ABDB7D8CAE96FF46ACF}

* 데이터 소스 파일을 업로드하면 데이터 소스는 기본적인 데이터 유효성 검사를 수행하여 파일에 형식 오류가 없는지 확인합니다. 파일에서 오류가 발생하면 이메일 알림이 발송되고 처리가 중지됩니다.
* 데이터 필드는 세미콜론을 포함할 수 없습니다. 데이터 소스는 세미콜론을 포함한 레코드를 건너뜁니다.
* 웹 로그, 트래픽, 일부 범용 데이터 소스 그룹의 데이터는 데이터 웨어하우스 또는 Discover에서 사용할 수 없습니다. 자세한 내용은 데이터 [유형 및 카테고리를 참조하십시오](../../import/c-data-sources/c-datasrc-types/datasrc-categories.md#concept_42D1534F48324F20B4F9297FC4022105).
* 데이터 소스는 직렬화된 이벤트를 지원하지 않습니다.

## 멀티바이트 지원 {#section_96C8D26B21184C3E839865DB6F23EA22}

데이터 소스는 멀티바이트 인코딩을 지원합니다. 데이터 소스는 수신 데이터 소스 파일의 형식을 감지하고 필요한 경우 지원되는 형식으로 전환합니다. 다음 표는 일반적인 문자 서식과 지원 현황입니다.

<table id="table_F9E685D7EEAB49A9ABAD622AE630EC21"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 문자 서식 </th> 
   <th colname="col2" class="entry"> 지원 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> UTF-8 </td> 
   <td colname="col2"> <p>지원됨. 데이터 소스에서 사용하는 보고서 세트에 멀티바이트 문자 지원이 활성화되어 있어야 합니다.  </p> <p>도움말에서 <a href="https://marketing.adobe.com/resources/help/en_US/reference/new_report_suite.html" format="https" scope="external">새 보고서 세트</a>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Byte Order Mark(EF BB BF)를 포함한 UTF-8 </td> 
   <td colname="col2"> <p>지원됨. 많은 Windows 응용 프로그램에서 이 형식으로 저장하고 있지만 표준은 아닙니다.  </p> <p>예를 들어 WordPad에서 "UTF-8" 선택 시 이 형식으로 저장됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ISO-8859-1(Latin-1 또는 Windows-1252) </td> 
   <td colname="col2"> 지원됨. Microsoft Excel에서 "탭으로 구분" 내보내기 선택 시 이 형식으로 저장됩니다. 보고서 세트는 반드시 ISO-8859-1 로케일을 사용해야 합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Byte Order Mark(FF FE)를 포함한 UTF-16 Little-endian </td> 
   <td colname="col2"> 보고서 세트 구성에 따라 ISO-8859-1 또는 UTF-8로 변환됩니다. Microsoft Excel에서 유니코드 내보내기 선택 시 이 형식으로 저장됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Byte Order Mark(EF FF)를 포함한 UTF-16 Big-endian </td> 
   <td colname="col2"> 보고서 세트 구성에 따라 ISO-8859-1 또는 UTF-8로 변환됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Byte Order Mark가 없는 UTF-16 </td> 
   <td colname="col2"> 지원되지 않음. </td> 
  </tr> 
 </tbody> 
</table>

UTF-8 또는 ISO-8859-1 파일을 전송할 때 보고서 세트가 이를 지원하도록 구성되지 않은 경우 다음 중 하나가 발생합니다.

* 전환 중 오류가 발생하고 UTF-8에서 ISO-8859-1로 변환하는 중 위치 18에서 잘못된 문자 발견과 같은 메시지가 표시됩니다.
* 오류 없이 파일이 처리되지만 보고서 데이터가 왜곡됩니다.

## 웹 로그 파일 업로드 {#section_DD736FC971FE45C89AB310BEDC1FE707}

* 웹 로그 데이터를 보기에 가장 유용한 보고서는 페이지 보기 횟수와 같은 트래픽 보고서입니다.
* 페이지 이름은 쿼리 문자열을 포함한 전체 URL로 표시됩니다.
* 각 파일 요청은 스타일 시트와 이미지 파일을 포함한 별도의 페이지 보기로 표시됩니다.
* URL에 정보를 첨부하면 파일이 별도 페이지로 기록되지 않을 수 있습니다. 예를 들어 마케팅 보고서는 다음 URL을 두 개의 분리된 페이지로 기록합니다.

[!DNL /jokes/misc/snail_joke.html?userid=12345]

[!DNL /jokes/misc/snail_joke.html?userid=98765]
