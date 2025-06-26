---
description: 세그먼트와 관련된 문제를 해결 및 수정합니다.
title: 세그먼테이션 문제 해결
feature: Segmentation
exl-id: ca51110e-1ba7-4182-b5b2-baf9b0c017af
source-git-commit: d85e6990998e3c153ef969d8dc7f3a4835f683bf
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 50%

---

# 세그먼테이션 문제 해결

<!-- Looks like this is not part anymore of the current UI.

## Error: "Incompatible elements in this segment" {#incompatible}

This error occurs when you try to save a segment in the Data Warehouse folder where the segment contains elements not compatible with Data Warehouse. To resolve this error, do one of two things:

* Save the segment in a different folder 
* Remove or change the incompatible portions of the segment.

-->

## 왜 세그먼트가 데이터를 전혀 반환하지 않습니까? {#no-data}

가능한 원인:

* 역방향 중첩 - 예를 들어 ![사용자](/help/assets/icons/User.svg) **[!UICONTROL 방문자]** 컨테이너를 ![방문](/help/assets/icons/Visit.svg) **[!UICONTROL 방문]** 컨테이너에 중첩합니다.
* 보고서가 세그먼테이션을 지원하지 않습니다.
* 세그먼테이션 기준과 일치하는 데이터가 없습니다.

## 세그먼트 관리자에서 만든 세그먼트가 표시되지 않는 이유는 무엇입니까? {#invisible}

가능한 원인:

* 일부 차원은 Data Warehouse에서만 사용할 수 있고 세그먼트 관리자에서는 사용할 수 없습니다.
* 세그먼트가 특정 보고서 세트에 대해서만 확인됩니다.
* 공유 세그먼트가 다른 사용자에 의해 삭제되었을 수 있습니다.
* 데이터 센터 또는 브라우저 캐시 문제로 인해 세그먼트를 로드할 수 없습니다.
* 세그먼트가 저장되지 않았습니다.
* IP 주소가 사용자 측에서 차단되어 있을 수 있습니다.

## 세그먼트를 적용한 후에 표시되는 데이터가 올바르지 않은 이유는 무엇입니까? {#page-data}

가능한 원인:

* 규칙 또는 연산자가 필수 결과에 대해 올바르지 않습니다.
* 세그먼트에서 컨테이너를 잘못 사용했습니다.
* 세그먼테이션하는 데 사용된 트래픽 변수가 잘못 설정되어 있거나 만료되었습니다.
