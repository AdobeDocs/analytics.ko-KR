---
description: Adobe에서는 새 계정 설정, 트래픽 스파이크 및 트래픽 증가에 대한 사전 공지를 필요로 합니다. 하드웨어는 미리 할당하여 지연과 전체 시스템에 대한 가능한 역효과를 최소화해야 합니다.
seo-description: Adobe에서는 새 계정 설정, 트래픽 스파이크 및 트래픽 증가에 대한 사전 공지를 필요로 합니다. 하드웨어는 미리 할당하여 지연과 전체 시스템에 대한 가능한 역효과를 최소화해야 합니다.
seo-title: 트래픽 증가에 대한 필수 리드 타임
solution: Analytics
title: 트래픽 증가에 대한 필수 리드 타임
topic: 관리 도구
uuid: AA 3 FB 882-51 B 0-458 F -917 B -7 C 54 D 5659623
translation-type: tm+mt
source-git-commit: e373297bcf1c9ae0f421ed246125204f31c39cc3

---


# 트래픽 증가에 대한 필수 리드 타임

Adobe에서는 새 계정 설정, 트래픽 스파이크 및 트래픽 증가에 대한 사전 공지를 필요로 합니다. 하드웨어는 미리 할당하여 지연과 전체 시스템에 대한 가능한 역효과를 최소화해야 합니다.

하드웨어 할당은 Reports &amp; Analytics 사용자 인터페이스를 통해 제출된 경고를 기반으로 수행됩니다.

> [!IMPORTANT] Adobe는 "자리 표시자" 트래픽 변경 요청을 수용할 수 없습니다. 별도로 표시되지 않는 한, 너무 일찍 경고를 보내지 않는 것을 포함하여 제안된 리드 타임에 가능한 한 가깝게 적용합니다. See [Schedule a traffic spike](../../admin/c-traffic-management/t-traffic-schedule-spike.md) or [Specify permanent traffic increase](../../admin/c-traffic-management/t-traffic-permanent.md).

트래픽 경고를 얼마나 일찍 제출해야 하는지를 결정하려면 다음 지침을 사용하십시오.

## 하드웨어 할당 리드 타임

<table id="table_A67CC3B164F740088797BD8913244E47">
 <thead>
  <tr>
   <th colname="col1" class="entry"> 일별 예상 트래픽(히트) </th>
   <th colname="col2" class="entry"> <p>리드 타임 필요 (1 월 ~ 10 월) </p> </th>
   <th colname="col3" class="entry"> <p>리드 타임 필요 (11 월 ~ 12 월) </p> </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> 최대 1,000,000 </td>
   <td colname="col2"> 리드 타임 불필요 </td>
   <td colname="col3"> 리드 타임 불필요 </td>
  </tr>
  <tr>
   <td colname="col1"> 1,000,000 - 5,000,000 </td>
   <td colname="col2"> 업무일 기준 2일 </td>
   <td colname="col3" morerows="3"> 11 월 ~ 12 월을 목표로 하는 모든 트래픽 증가는 9 월 1 일까지 제출해야 합니다. 그렇게 해야 휴일 트래픽을 수용하는 데 필요할 경우 용량을 구입할 시간이 생깁니다. </td>
  </tr>
  <tr>
   <td colname="col1"> 5,000,000 - 10,000,000 </td>
   <td colname="col2"> 1주일 </td>
  </tr>
  <tr>
   <td colname="col1"> 10,000,000 - 25,000,000 </td>
   <td colname="col2"> 2주일 </td>
  </tr>
  <tr>
   <td colname="col1"> <p>25,000,000 이상 </p> </td>
   <td colname="col2"> 1개월 이상 </td>
  </tr>
 </tbody>
</table>

기타 고려 사항:

* 시작하거나 증가하여 위에 나열된 숫자로 합산되는 여러 개의 보고서 세트가 있는 경우 리드 타임은 각 보고서 세트에 대해 예상된 트래픽의 합으로 적용됩니다.
* 트래픽 변경을 제출하려면 다음 정보를 준비하십시오.

   * 보고서 세트 ID
   * 일당 예상 히트 수
   * Go Live 날짜

* 클라이언트 경고는 트래픽이 감소하거나 특정 보고서 세트가 삭제되었을 때도 필요합니다.

## 트래픽 미실현으로 인한 하드웨어 할당 취소

새 계정, 트래픽 스파이크 및 트래픽 증가를 위한 하드웨어는 클라이언트 경고에서 전망한 트래픽이 "Go Live 날짜" 이후 4주 내에 실현되지 않는 경우 할당이 취소됩니다. 트래픽이 여전히 예상된다면, 새 클라이언트 경고를 트래픽 증가로 생성해야 합니다.
