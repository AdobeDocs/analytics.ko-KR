---
title: Report Builder FAQ
description: Report Builder에 대한 FAQ
translation-type: tm+mt
source-git-commit: 47b14bde1bb1217bcb172c6d4f01d68f917d44db
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---


# Report Builder FAQ

Report Builder에 대한 FAQ

## 통합 문서에서 `TODAY()` 또는 `DATERANGE()` 기능을 사용할 수 있습니까?

Excel의 [`TODAY()` 함수는](https://support.microsoft.com/en-us/office/today-function-5eb3078d-a82c-4736-8930-2f51a028fdd9) 현재 날짜를 반환합니다. 이 [`DATEVALUE()` 함수는](https://support.microsoft.com/en-us/office/datevalue-function-df8b07d4-7761-4a93-bc33-b7471bbff252) 날짜 문자열을 일련 값으로 변환합니다. Excel의 많은 기능에 유용하지만 Report Builder 예약 요청의 일부로 이러한 기능을 사용하지 않는 것이 좋습니다. Adobe 고객 지원 센터는 이러한 기능 중 하나를 사용하는 문제 해결 요청을 지원하지 않습니다.

예약된 보고서는 보고서 세트로 시간대를 공유하지 않는 서버에서 처리됩니다. 사용자 `TODAY()` 가 예상하며 처리 `TODAY()` 서버에서 사용하는 것은 종종 다를 수 있습니다. 또한 사용된 날짜는 처리가 시작된 시기를 기반으로 합니다. 여러 보고서가 동시에 실행되는 경우, 요청이 요청된 시간과 지연으로 처리가 시작되는 시기 사이에 날짜가 변경될 수 있습니다. 예약된 시간이 자정에 가까운 경우 이 문제가 발생합니다.

예약된 보고서는 날짜 구문을 공유하지 않는 서버에서도 처리됩니다. 예를 들어 귀하의 국가 또는 지역에 따라 7월 1일 또는 1월 7일을 참조할 `7/1/YYYY` 수 있습니다. 이 날짜에 `DATEVALUE()` 함수를 사용하면 실행하는 컴퓨터에 따라 일련 값이 다를 수 있습니다.

이러한 Excel 함수를 사용하는 대신 Report Builder 요청 내에서 날짜 범위를 사용하는 것이 좋습니다. 요청 마법사의 첫 번째 페이지에서 드롭다운에서 **[!UICONTROL 사전 설정 날짜]** 를 선택한 다음, 일반적으로 사용되는 날짜에서 **[!UICONTROL 오늘]** 또는 다른 원하는 날짜 범위를 선택합니다. 이 설정은 보고서 세트가 실행될 때 시간이 걸리고 서버가 요청을 처리하는 시간이 아닙니다.

## 통합 문서를 얼마나 크고 복잡하게 만들 수 있습니까?

Report Builder은 통합 문서를 다음 제한 사항까지 지원합니다.

* **1000개 요청**:통합 문서는 단일 통합 문서에 최대 1,000개의 데이터 요청을 포함할 수 있습니다. 1,000개 이상의 요청이 필요한 보고서나 프로젝트가 있는 경우, Adobe은 이를 여러 통합 문서로 구분하는 것이 좋습니다.
* **회사당**&#x200B;시간당 20K 요청:Report Builder은 Analytics 보고 API를 사용하여 데이터를 검색합니다. 각 개별 요청은 API 호출이 생성되거나 새로 고쳐질 때마다 API 호출을 사용합니다. 조직에서 지정된 시간에 20,000개 이상의 API 호출을 누적하면 다음 시간까지 기다린 후 데이터를 다시 검색해야 합니다.
* **4시간 처리 시간**:예약된 보고서가 지난 4시간 후에 시간 초과됩니다. 통합 문서에 대용량 데이터 세트를 사용하는 복잡한 요청이 많이 포함되어 있으면 예약된 보고서가 실패할 수 있습니다.
