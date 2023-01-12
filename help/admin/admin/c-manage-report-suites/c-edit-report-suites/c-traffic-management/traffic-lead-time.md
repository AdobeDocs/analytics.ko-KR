---
description: Adobe에서는 새 계정 설정, 트래픽 스파이크 및 트래픽 증가에 대한 사전 공지를 필요로 합니다. 하드웨어는 미리 할당하여 지연과 전체 시스템에 대한 가능한 역효과를 최소화해야 합니다.
title: 트래픽 증가에 대한 필수 리드 타임
feature: Traffic Management
exl-id: fb428f8d-9dff-43a6-a1e8-1a892cbed7ac
source-git-commit: 6f7f46b0fee46e572a65f639ea511478c0118f4e
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 78%

---

# 트래픽 증가에 대한 필수 리드 타임

Adobe에서는 새 계정 설정, 트래픽 스파이크 및 트래픽 증가에 대한 사전 공지를 필요로 합니다. 하드웨어는 미리 할당하여 지연과 전체 시스템에 대한 가능한 역효과를 최소화해야 합니다.

하드웨어 할당은 Reports &amp; Analytics 사용자 인터페이스를 통해 제출된 경고를 기반으로 수행됩니다.

>[!IMPORTANT]
>
>Adobe는 &quot;자리 표시자&quot; 트래픽 변경 요청을 수용할 수 없습니다. 달리 지정하지 않는다면, 너무 일찍 경고를 보내지 않는 것을 포함하여 제안된 리드 타임에 가능한 한 가까운 시간을 사용하십시오. [트래픽 스파이크 예약](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/c-traffic-management/t-traffic-schedule-spike.md) 또는 [영구 트래픽 증가 지정](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/c-traffic-management/t-traffic-permanent.md)을 참조하십시오.

트래픽 경고를 얼마나 일찍 제출해야 하는지를 결정하려면 다음 지침을 사용하십시오.

## 하드웨어 할당 리드 타임


<table id="table_A67CC3B164F740088797BD8913244E47">
 <thead>
  <tr>
   <th colname="col1" class="entry"> 트래픽 변경 유형 </th>
   <th colname="col2" class="entry"> 필요한 리드 타임 </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> 새 계정 설정 </td>
   <td colname="col2"> <ul><li>3영업일</li></ul></td>
  </tr>
  <tr>
   <td colname="col1"> 지난 30일에 비해 일일 평균 교통량이 최고 25%의 트래픽 스파이크나 갑작스러운 영구 트래픽 증가</td>
   <td colname="col2"> <ul><li>100M 히트/일 : 알림 필요 없음</li><li>100M 히트/날이 속하는 보고서 세트: 영업일 기준</li></ul></td>
  </tr>
  <tr>
   <td colname="col1"> 지난 30일에 비해 일일 평균 교통량이 25% 이상 증가한 트래픽 스파이크나 갑작스러운 영구 트래픽 증가</td>
   <td colname="col2"> <ul><li>영업일 기준</li></ul></td>
  </tr>
  <tr>
   <td colname="col1"> 휴일 이벤트 10월 - 12월 </td>
   <td colname="col2"> <ul><li>1개월</li></ul> </td>
  </tr>
 </tbody>
</table>

기타 고려 사항:

* 시작하거나 증가하여 위에 나열된 숫자로 합산되는 여러 개의 보고서 세트가 있는 경우 리드 타임은 각 보고서 세트에 대해 예상된 트래픽의 합으로 적용됩니다.
* 트래픽 변경을 제출하려면 다음 정보를 준비하십시오.

   * 보고서 세트 ID
   * 일당 예상 히트 수
   * Go Live 날짜

* 클라이언트 경고는 트래픽이 감소하거나 특정 보고서 세트를 더 이상 사용하지 않을 때에도 필요합니다.

## 트래픽 미실현으로 인한 하드웨어 할당 취소

새 계정, 트래픽 스파이크 및 트래픽 증가를 위한 하드웨어는 클라이언트 경고에서 전망한 트래픽이 &quot;Go Live 날짜&quot; 이후 4주 내에 실현되지 않는 경우 할당이 취소됩니다. 트래픽이 여전히 예상된다면, 새 클라이언트 경고를 트래픽 증가로 생성해야 합니다.