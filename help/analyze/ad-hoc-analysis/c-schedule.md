---
description: 보고서에 대한 배달 일정을 사용자 지정할 수 있습니다. 특정 시간에 배달을 중지하거나 보고서를 전송할 횟수를 지정할 수 있습니다. 새 예약은 보고서에 정의된 날짜 범위를 사용합니다. 예를 들어, 지난 90일에 대한 보고서를 만들어 일일 실행 일정을 지정하는 경우 지난 90일의 각 날에 대한 보고서를 받습니다. 달력에서 정적 날짜 범위를 갖는 보고서를 만드는 경우 전송할 때마다 동일한 보고서가 표시됩니다.
title: 예약 관리자
topic: Ad hoc analysis
uuid: 82a054ef-109d-414d-a6e1-e09ee57c163f
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 예약 관리자

보고서에 대한 배달 일정을 사용자 지정할 수 있습니다. 특정 시간에 배달을 중지하거나 보고서를 전송할 횟수를 지정할 수 있습니다. 새 예약은 보고서에 정의된 날짜 범위를 사용합니다. 예를 들어, 지난 90일에 대한 보고서를 만들어 일일 실행 일정을 지정하는 경우 지난 90일의 각 날에 대한 보고서를 받습니다. 달력에서 정적 날짜 범위를 갖는 보고서를 만드는 경우 전송할 때마다 동일한 보고서가 표시됩니다.

## 예약 관리자 {#concept_A1CDE14B72A54DD6AE17B816092CAB8B}

보고서에 대한 배달 일정을 사용자 지정할 수 있습니다. 특정 시간에 배달을 중지하거나 보고서를 전송할 횟수를 지정할 수 있습니다. 새 예약은 보고서에 정의된 날짜 범위를 사용합니다. 예를 들어, 지난 90일에 대한 보고서를 만들어 일일 실행 일정을 지정하는 경우 지난 90일의 각 날에 대한 보고서를 받습니다. 달력에서 정적 날짜 범위를 갖는 보고서를 만드는 경우 전송할 때마다 동일한 보고서가 표시됩니다.

>[!NOTE] 사용자 계정이 비활성화되면 해당 사용자가 만든 예약 보고서 배달이 일시 중단됩니다.

To ensure that line items in a breakdown are persistent in saved and scheduled reports, use the **[!UICONTROL Edit Items]** feature in the [Table Builder](/help/analyze/ad-hoc-analysis/c-tablebuilder.md) to create fixed dimension lists in breakdowns.

>[!IMPORTANT]
>
>Ad Hoc Analysis을 사용하면 애드혹 보고 요구에 맞는 시기적절한 특정 보고서를 신속하게 정의하고 예약할 수 있습니다. 데이터 추출을 사용하여 대량의 행 또는 행, 열, 지표 평가 또는 광범위한 분류로 데이터를 전체 내보내기용으로 설계된 것은 아닙니다.
>
>애드혹 분석의 예약된 보고를 위한 실용적인 제한은 다음 원칙을 기반으로 합니다.보고서가 10분(애드혹 분석의 시간 초과) 내에 작성되지 않으면 보고서가 너무 복잡할 수 있습니다.
>
>보고서에 너무 많은 지표, 너무 많은 차원 요소 분류, 너무 많은 행 또는 열, 또는 애드혹 분석을 위한 보고서 생성 프로세스가 너무 길어 보고서에 너무 오래 걸릴 수 있습니다. 이 유형의 보고서는 많은 시간 또는 며칠이 걸릴 수 있는 보고서 생성으로 오프라인으로 실행되는 전체 데이터 추출을 위해 만들어진 Adobe Analytics 기능인 데이터 웨어하우스에서 실행해야 합니다.
>
>예를 들어 애드혹 분석은 50,000개의 데이터 행을 처리할 수 있지만, 10개의 브라우저 유형에 대해 해당 데이터를 분류하면 50,000의 10이 되는데, 이는 임시 보고 도구에 비해 너무 복잡할 수 있는 지수 증가입니다. 추가적인 분류는 데이터 행을 기하급수적으로 증가시킵니다. 애드혹 분석 보고에 대해 제한할 실제 행, 열 및 분류를 정의하면 완전히 정의할 수 없지만 이러한 모든 요소가 결합됩니다.

## 보고서 배달 예약 {#task_7A3165C8C5C349718FE3B2B0C727ACFD}

보고서 배달을 예약하는 방법에 대해 설명하는 절차입니다.

<!-- 

t_schedule_delivery.xml

 -->

1. 을 **[!UICONTROL Tools]**&#x200B;클릭한 다음 을 클릭합니다 **[!UICONTROL Schedule Manager]**.
1. 에서 [!UICONTROL Schedule Manager]**[!UICONTROL New.]**

## 배달 옵션 - 정의를 참조하십시오{#reference_CA49AC560258471AAE959BCA243F170C}

배달 옵션의 설정에 대한 정의입니다.

<!-- 

r_delivery_options.xml

 -->

현재 선택된 보고서에 표시된 정보를 선택한 형식으로 보낼 수 있습니다. 한 번만 전송하거나 배달 일정을 설정하고 원하는 파일 형식을 지정할 수 있습니다. 디지털 서명을 만들어 전송하면 파일 수신자가 인증 파일인지 확인할 수 있습니다. 파일을 이메일 주소로 보내거나 FTP 서버에 업로드할 수 있습니다.

<table id="table_C18A0F1C9E214EB585A29801BA2400F8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>필드 </p> </th> 
   <th colname="col2" class="entry"> <p>정의 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>이름 </p> </td> 
   <td colname="col2"> <p> 이 보고서의 구성 가능한 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ID </p> </td> 
   <td colname="col2"> <p>보고서 ID를 알려줍니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 파일 형식 </p> </td> 
   <td colname="col2"> 
    <ul id="ul_711C2D9B216C48359F7B42521D927872"> 
     <li id="li_36E8DEFDA1B84890A4204A6DFF4E0267">Excel:모든 이미지를 포함하여 스프레드시트로 보고서를 출력합니다. Microsoft Excel에서 편집할 수 있습니다. </li> 
     <li id="li_C918FA3AE8194BD2B59E554DAC7CBBE2">CSV:보고서를 쉼표로 구분된 값으로 출력합니다. 단순 텍스트 편집기(메모장 등) 또는 스프레드시트 편집기(예: Excel)에서 편집할 수 있습니다. 이미지를 포함하지 않습니다. </li> 
     <li id="li_B7C8C098C5264B349C21077A0DEFE059">PDF:보고서를 PDF(Portable Document Format)로 출력합니다. Adobe Acrobat 또는 Adobe Reader에서 편집할 수 없고 볼 수 있습니다. </li> 
     <li id="li_B1183DB25DE34B689FBD0E5B44691F49">HTML:보고서를 HTML(Hypertext Markup Language) 첨부 파일로 출력합니다. 이 형식은 대부분의 웹 사이트를 구성하는 형식입니다. HTML 코드에 익숙하지 않은 경우 편집할 수 없습니다. </li> 
     <li id="li_5ED5F1862AB1490A9FF5695FF9F52C5E">Word:모든 이미지를 포함하여 보고서를 리치 텍스트 형식으로 출력합니다. Microsoft Word 또는 WordPad에서 편집할 수 있습니다. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 고급 </p> </td> 
   <td colname="col2"> <p> <a href="/help/analyze/ad-hoc-analysis/c-schedule.md"   >고급 형식 설정</a>을 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>파일 대상 </p> </td> 
   <td colname="col2"> <p>이메일:이메일을 통해 보내는 설정입니다. </p> <p>FTP:FTP 서버에 업로드하기 위한 설정입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>보고서 범위 및 배달 일정 </p> </td> 
   <td colname="col2"> <p>보고서를 제공할 시기를 지정합니다. 새 예약은 보고서에 정의된 날짜 범위를 사용합니다. 예를 들어, 지난 90일에 대한 보고서를 만들어 일일 실행 일정을 지정하는 경우 지난 90일의 각 날에 대한 보고서를 받습니다. 달력에서 정적 날짜 범위를 갖는 보고서를 만드는 경우 전송할 때마다 동일한 보고서가 표시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 고급 형식 설정 - 정의 {#reference_F99B65BF7C9746638D8147EED147015B}

고급 형식 설정의 정의.

<!-- 

r_advanced_format_settings_dsc.xml

 -->

<table id="table_CD0888E8390745F4B83DF6AC69CB0854"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>필드 </p> </th> 
   <th colname="col2" class="entry"> <p>정의 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>파일 이름 </p> </td> 
   <td colname="col2"> <p>사용자 정의 파일 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>파일 이름에 ID 추가 </p> </td> 
   <td colname="col2"> <p>보고서 ID를 파일 이름에 자동으로 추가합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 파일 이름에 날짜 추가 </p> </td> 
   <td colname="col2"> <p> 보고서 날짜를 파일 이름에 자동으로 추가합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>언어 </p> </td> 
   <td colname="col2"> <p> 보고서의 언어를 선택할 수 있습니다. 사용하는 언어에 관계없이 다음 언어로 보고서를 전송할 수 있습니다 </p> 
    <ul id="ul_BD3D331B0D6146F79A6D254136E43920"> 
     <li id="li_0EE6A371B1BB4627BD3F64BD0EF07E44">영어 </li> 
     <li id="li_5EF76261928543FDB36D99E4C89DE994">스페인어 </li> 
     <li id="li_FABF47E8CD64486BA1567E02460422C5">중국어 간체 </li> 
     <li id="li_8A6BC2DE92DB47DA9397B8931D8DCC6E">중국어 번체 </li> 
     <li id="li_EDA24D700BE040E8B839B82E31DABC28">프랑스어 </li> 
     <li id="li_A8D41DCCC91542BB8D0A522EC99575E8">독일어 </li> 
     <li id="li_E9F73C93C94A46B78BCE85A7261CEDD4">일본어 </li> 
     <li id="li_699B97050AA54D818659C191F4594E4E">포르투갈어 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>인코딩 </p> </td> 
   <td colname="col2"> <p>인코딩 유형을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 보고서를 압축 파일로 보내기 </p> </td> 
   <td colname="col2"> <p> 파일을 압축합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>디지털 서명 파일 전송 </p> </td> 
   <td colname="col2"> <p>이메일에 보낼 디지털 서명을 만듭니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

