---
title: Activity Map 데이터 수집 문제 해결
description: 이미지 요청에 Activity Map 데이터를 볼 수 없는 이유를 결정합니다
feature: Activity Map
role: User, Admin
exl-id: 7f9e06ba-4040-483b-b18b-cdfe85bca486
source-git-commit: e6f3beadfba340cea07f5fd2694105ad31de9751
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 3%

---

# Activity Map 데이터 수집 문제 해결

Activity Map 차원에 대한 데이터가 표시되지 않는 경우 이 페이지를 사용하여 이유를 파악하십시오.

## 디버거를 사용하여 데이터 수집 확인

먼저 AppMeasurement가 Activity Map 데이터를 올바르게 수집하는지 확인합니다.

1. [Adobe Experience Cloud Debugger Chrome 확장 프로그램](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=ko-KR)을 다운로드하여 설치합니다.
2. 웹 페이지로 이동한 다음 링크를 클릭합니다.
3. 후속 페이지가 로드되면 디버거를 엽니다. `activitymap.` 과 `.activitymap` 사이에 있는 Activity Map 컨텍스트 데이터 변수가 표시되는지 확인합니다.

![디버거 데이터](assets/debugger.png)

## Activity Map 데이터가 없는 가능한 이유

Activity Map 구성 요소가 있는지 확인하려면 다음 각 사항을 확인하십시오.

* **AppMeasurement 버전**: Activity Map은 v1.6 이상에서 지원됩니다. 안정적인 최신 버전의 AppMeasurement로 업그레이드할 때 많은 에지 사례 문제가 해결됩니다.
* **Activity Map 모듈**: 모듈이  `AppMeasurement_Module_Activity_Map` 파일에 있는지  `AppMeasurement.js` 확인합니다. 구현에서 Adobe Experience Platform 데이터 수집(Launch)을 사용하는 경우 **[!UICONTROL 링크 추적]**&#x200B;에서 Analytics 확장을 구성할 때 **[!UICONTROL ClickMap 활성화]**&#x200B;를 선택해야 합니다.
* **쿠키  `s_sq`**: Activity Map은 데이터 수집을  `s_sq` 위한 쿠키에 따라 다릅니다.
   * 특히 `*.co.uk` 또는 `*.co.jp` 등의 지역 도메인에 대해 `cookieDomainPeriods` 변수가 올바르게 설정되었는지 확인합니다.
   * `linkInternalFilters` 변수가 원하는 값으로 설정되어 있는지 확인하십시오. 클릭한 링크가 내부 필터와 일치하지 않으면 Activity Map은 이를 종료 링크로 간주하여 데이터를 수집하지 않습니다.
* **Activity Map 오버레이가 실행** 중: Activity Map 오버레이가 활성화되어 있을 때 AppMeasurement는 웹 페이지에 대한 클릭 데이터를 추적하지 않습니다.
