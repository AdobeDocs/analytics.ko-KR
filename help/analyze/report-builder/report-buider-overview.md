---
title: 새로운 Adobe Report Builder 소개
description: 새로운 Report Builder 기능에 대해 설명합니다
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: b6f2b1f5-8790-4342-85c8-524fdf346073
source-git-commit: d7a6867796f97f8a14cd8a3cfad115923b329c7c
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 29%

---

# 새 Adobe Report Builder 정보

처음에 Customer Journey Analytics에서만 사용할 수 있었던 새로운 Javascript Report Builder 추가 기능이 이제 Adobe Analytics에도 도입되었습니다. 이 새 버전에는 다음과 같은 몇 가지 이점이 있습니다.

- 데이터 블록 유연성 향상 등 데이터 블록 생성 및 관리를 위한 향상된 워크플로를 통해 Excel의 통찰력을 더 빠르고 쉽게 찾을 수 있습니다
- 교차 플랫폼: 이제 PC, Mac 및 Excel Online을 지원하므로 Report Builder을 사용하기 위해 VM에 더 이상 로그인하지 않음
- API 2.0 업그레이드 덕분에 데이터 블록이 반환되기를 기다리는 시간이 단축됩니다.
- 속도 향상

레거시 Report Builder 도구 사용자는 [레거시 통합 문서를 ](/help/analyze/report-builder/convert-workbooks.md)새 Report Builder으로 변환할 수 있습니다.

Report Builder을 사용하면 Adobe Analytics 데이터를 사용하여 사용자 지정 보고서를 쉽게 만들고 편집하고 새로 고칠 수 있습니다. Report Builder의 간단하고 유연한 드래그 앤 드롭 UI를 통해 Excel 내의 모든 Adobe Analytics 데이터에서 복잡한 데이터 쿼리와 사용자 지정 보고서를 만들 수 있습니다.

Report Builder을 사용하여 다음을 수행할 수 있습니다.

- 기존 워크시트 셀을 참조하여 완벽한 행 순서, 날짜 범위 또는 필터를 얻을 수 있습니다.
- 달력, 셀 참조 또는 날짜 계산을 사용하여 사용자 정의 날짜를 만들 수 있습니다.
- 익숙한 Excel 서식 도구를 사용하여 테이블과 시각화를 디자인할 수 있습니다.

## 이전 Report Builder과 새 Report Builder을 나란히 사용

두 버전의 Report Builder을 다음 주의 사항과 함께 계속 사용할 수 있습니다.

- 동일한 파일에서 두 Report Builder 버전을 동시에 사용하지 마십시오. 그것들은 상호 배타적이다.
- 이전 통합 문서에서는 이전 Report Builder을, 새 통합 문서에서는 새 Report Builder을 계속 사용할 수 있습니다.
- 또한 [기존 통합 문서를 새 Report Builder 형식으로 자동 변환](/help/analyze/report-builder/convert-workbooks.md)할 수 있습니다. 이 작업을 수행하기 전에 파일을 복제하고 이름을 변경합니다.

## 새 Report Builder에서 지원되지 않는 기존 Report Builder 기능

레거시 Report Builder의 기능을 새 Report Builder 추가 기능과 비교할 때 일부 레거시 기능은 더 이상 사용할 수 없습니다.

- 실시간 요청

- 경로/폴아웃 보고

- 예약된 보고서에 대한 FTP 옵션

- 방문자 지표. 보고 결과가 정확히 일치하지 않더라도 다음 지표는 모두 &quot;고유 방문자 수&quot;로 변환됩니다. `visitorshourly`, `visitorsdaily`, `visitorsweekly`, `visitorsmonthly`, `visitorsquarterly` 및 `visitorsyearly`. 이는 `mobilevisitorshourly`, `mobilevisitorsdaily`, `mobilevisitorsweekly`, `mobilevisitorsmonthly`, `mobilevisitorsquarterly` 및 `mobilevisitorsyearly`에도 적용됩니다.

## 일반적인 사용 사례

- **데이터 추출**: Adobe Report Builder을 사용하면 Adobe Analytics의 데이터를 Excel로 추출할 수 있습니다. 사용자 정의 보고서 및 쿼리를 만들어 분석과 관련된 특정 데이터 포인트를 검색할 수 있습니다.

- **사용자 정의 보고**: 특정 보고 요구 사항에 맞게 Excel에서 사용자 정의 보고서를 디자인하고 포맷을 지정할 수 있습니다. 다양한 이해 당사자에 맞게 보고서를 맞춤화하는 데 특히 유용합니다.

- **애드혹 분석**: 사용자가 시간이 오래 걸리는 보고서 만들기 프로세스를 거치지 않고도 특정 질문에 답하거나 데이터 추세를 탐색하기 위해 애드혹 보고서를 신속하게 생성할 수 있습니다.

- **대시보드**: CJA에서 추출한 데이터를 사용하여 주요 성과 지표(KPI)의 상위 수준 개요를 위한 Excel 기반 대시보드 및 시각화를 만들 수 있습니다.

- **인사이트 공유**: CJA에 직접 액세스할 수 없는 팀원이나 이해 당사자와 Excel 보고서 및 인사이트를 공유할 수 있습니다.

## 개요 비디오

>[!IMPORTANT]
>
>이 개요 비디오는 Customer Journey Analytics의 Report Builder 사용자 인터페이스를 보여 줍니다. 사용자 인터페이스와 용어 중 일부는 다릅니다. 그렇지 않으면 사용자 경험은 동일합니다.


>[!BEGINSHADEBOX]

데모 비디오는 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Report Builder 개요](https://video.tv.adobe.com/v/337569?quality=12&learn=on){target="_blank"}를 참조하십시오.

>[!ENDSHADEBOX]

[Microsoft 스토어](https://appsource.microsoft.com/en-us/product/office/WA200003101?tab=Overview)에서 Report Builder을 다운로드할 수 있습니다.
