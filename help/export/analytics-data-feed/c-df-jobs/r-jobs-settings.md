---
description: 피드를 설정할 때 일부 설정은 작업이 처리되는 빈도를 결정합니다.
keywords: 데이터 피드; 작업; 설정; 일별; 시간별; 시간별 데이터 피드를 위한 데이터 채우기채우기
seo-description: 피드를 설정할 때 일부 설정은 작업이 처리되는 빈도를 결정합니다.
seo-title: 작업 설정
solution: Analytics
title: 작업 설정
uuid: E 124 B 4 F 1-0168-4 EAA -8657-19207 B 2 F 263 F
translation-type: tm+mt
source-git-commit: b6169d2febded32d772f82d5917b1132695ab442

---


# 작업 설정

피드를 설정할 때 일부 설정은 작업이 처리되는 빈도를 결정합니다.

다음 설정을 사용하여 작업 처리 시간을 구성하십시오. 이 설정은 작업 수준이 아니라 피드 수준에서 설정됩니다.

<table id="table_2070F73212F245E98DADC6B5DFDB1C72"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 설정 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 일별 </td> 
   <td colname="col2"> <p>일별 데이터는 하나의 압축 파일로 제공됩니다. 이 파일의 크기 제한은 2GB입니다. 파일 크기가 압축 해제된 데이터로 2GB가 넘을 경우, 추가 파일이 만들어집니다. 매일 모든 파일을 한 번에 받게 됩니다. </p> <p>각 파일의 이름은 다음 형식으로 지정됩니다. </p> <p> <span class="filepath"><span class="varname"> Reportsuite</span>-<span class="varname"> Date</span>.tar</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 시간별(기본값) </td> 
   <td colname="col2"> <p>한 시간 동안의 데이터가 그 동안 수집된 모든 데이터를 포함한 단일 zip 파일로 배달됩니다. 한 시간 분량의 데이터가 처리된 후 각각의 파일이 하루 24회로 나뉘어 배달됩니다. </p> <p>"시간별"에서 시간이란, 배달되는 시간이 아니라 각각의 데이터 내보내기를 통해 발송되는 데이터의 시간을 의미합니다. 시간별 데이터 피드는 최선의 방법으로 처리 및 배달됩니다. </p> <p>시간별 데이터 피드의 경우 95%가 해당 시간 동안의 데이터 마감 후 12시간 내에 배달될 것으로 예상됩니다. 트래픽 볼륨이 높은 보고서 세트에 대한 데이터 피드는 처리 및 배달하는 데 시간이 더 오래 걸릴 수 있습니다. </p> <p>시간별 데이터 피드를 받는 것은 여러 파일 배달을 통해 일별 피드를 받는 것과 다릅니다. 시간별 데이터 피드를 받는 경우 하루 동안의 데이터가 해당 시간 동안 수집된 데이터를 기준으로 24개의 파일로 분할되고 각 파일이 준비되는 즉시 배달됩니다. 여러 개의 파일로 배달되는 일별 피드는 전날 데이터 처리 완료 후 하루에 한 번 배달되며 수집된 데이터의 양을 기준으로 2GB 단위로 분할됩니다. </p> <p>각 파일의 이름은 다음 형식으로 지정됩니다. </p> <p> <span class="filepath"><span class="varname"> Reportsuite</span>-<span class="varname"> Date</span>-<span class="varname"> Hour</span>.tar</span> </p> <p>시간별 피드에 영향을 줄 수 있는 요소에 대한 자세한 내용은 <a href="../../../export/analytics-data-feed/c-df-contents/jobs-faq.md#concept_7C67A012CCF64B0C8DA33E5A6CF7FD9E" format="dita" scope="local">작업 FAQ</a>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 시간별 데이터 피드를 위한 데이터 채우기 </td> 
   <td colname="col2"> <p>새 시간별 데이터 피드를 설정할 때 이전 날짜의 데이터를 요청하는 경우 60일이 넘는 이전 날짜의 데이터는 시간별 대신 일별 형식으로 제공될 수 있습니다. </p> <p>이러한 경우에는 이러한 날짜들에 대해 24개의 별도 제공을 받는 것이 아니라, 대신 해당 날짜의 모든 데이터가 들어 있고 자정 타임스탬프가 있는 단일 제공을 받게 됩니다. 이 유형의 채우기를 요청하는 경우 ETL이 일별 제공을 처리하도록 구성되어 있는지 확인하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

