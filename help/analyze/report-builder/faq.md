---
title: Report Builder FAQ
description: Report Builder에 대해 자주 묻는 질문.
feature: Report Builder
role: Business Practitioner, Administrator
exl-id: 86604d39-2965-45a5-98ab-3ee4adcb7f97
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '423'
ht-degree: 100%

---

# Report Builder FAQ

Report Builder 관련 자주 묻는 질문.

## 통합 문서에서 `TODAY()` 또는 `DATERANGE()` 함수를 사용할 수 있습니까?

Excel의 [`TODAY()` 함수](https://support.microsoft.com/ko-kr/office/today-function-5eb3078d-a82c-4736-8930-2f51a028fdd9) 는 현재 날짜를 반환합니다. [`DATEVALUE()` 함수](https://support.microsoft.com/ko-kr/office/datevalue-function-df8b07d4-7761-4a93-bc33-b7471bbff252)는 날짜 문자열을 직렬 값으로 변환합니다. Excel 내의 많은 기능에 유용하지만 이러한 함수를 Report Builder 예약 요청의 일부로 사용하지 않는 것이 좋습니다. Adobe 고객 지원 센터는 이러한 함수 중 하나를 사용하는 문제 해결 요청을 지원하지 않습니다.

예약 된 보고서는 시간대를 공유하지 않는 서버에서 보고서 세트로 처리됩니다. 사용자가 기대하는 `TODAY()`와 처리 서버가 사용하는 `TODAY()`는 종종 다를 수 있습니다. 또한 사용되는 날짜는 처리가 시작되는 때를 기준으로 합니다. 많은 보고서가 동시에 실행되는 경우 지연으로 인해 요청된 시간과 처리를 시작하는 시간 사이에 날짜가 변경될 수 있습니다. 이 문제는 예정된 시간이 자정에 가까운 경우 발생합니다.

예약된 보고서는 날짜 구문을 공유하지 않는 서버에서도 처리됩니다. 예를 들어 `7/1/YYYY`는 국가 또는 지역에 따라 7월 1일 또는 1월 7일을 나타낼 수 있습니다. 이 날짜에 `DATEVALUE()` 함수를 사용하면 이를 실행하는 컴퓨터에 따라 직렬 값이 달라집니다.

이러한 Excel 함수를 사용하는 대신 Report Builder 요청 내에서 날짜 범위를 사용하는 것이 좋습니다. 요청 마법사의 첫 페이지에 있는 드롭다운에서 **[!UICONTROL 사전 설정된 날짜]**&#x200B;를 선택한 다음 일반적으로 사용되는 날짜에서 **[!UICONTROL 오늘]** 또는 다른 원하는 날짜 범위를 선택합니다. 이 설정은 서버가 요청을 처리할 때가 아니라 보고서 세트가 실행될 때 시간이 걸립니다.

## 통합 문서를 얼마나 크고 복잡하게 만들 수 있습니까?

Report Builder의 통합 문서 지원 한도는 다음과 같습니다.

* **1000개의 요청**: 통합 문서는 단일 통합 문서에 최대 1000개의 데이터 요청을 포함할 수 있습니다. 1000개가 넘는 요청이 필요한 보고서 또는 프로젝트가 있는 경우 이를 여러 통합 문서로 분리하는 것이 좋습니다.
* **회사당 시간당 요청 2만 개**: Report Builder는 Analytics Reporting API를 사용하여 데이터를 검색합니다. 각 개별 요청은 생성되거나 새로 고쳐질 때마다 API 호출을 사용합니다. 조직에서 지정된 시간에 API 호출이 20,000개 이상 누적되는 경우 데이터를 다시 검색하려면 다음 시간까지 기다려야 합니다.
* **4시간 처리 시간**: 4시간이 이상 처리 후 예약된 보고서 시간 제한. 통합 문서에 대규모 데이터 세트를 사용하는 복잡한 요청이 많이 포함된 경우 예약된 보고서가 실패할 수 있습니다.
