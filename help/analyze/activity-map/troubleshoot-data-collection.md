---
title: Activity Map 데이터 수집 문제 해결
description: 이미지 요청에 Activity Map 데이터가 표시되지 않는 이유 확인
feature: Activity Map
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 3%

---


# Activity Map 데이터 수집 문제 해결

Activity Map 차원에 대한 데이터가 없는 경우 이 페이지를 사용하여 이유를 파악하십시오.

## 디버거를 사용하여 데이터 수집 확인

먼저 AppMeasurement가 Activity Map 데이터를 올바르게 수집하는지 확인하십시오.

1. [Adobe Experience Cloud Debugger Chrome Extension](https://docs.adobe.com/content/help/ko/debugger/using/experience-cloud-debugger.html)을(를) 다운로드하고 설치합니다.
2. 웹 페이지로 이동한 다음 링크를 클릭합니다.
3. 후속 페이지가 로드되면 디버거를 엽니다. `activitymap.`과 `.activitymap` 사이에 있는 Activity Map 컨텍스트 데이터 변수가 있는지 확인합니다.

![디버거 데이터](assets/debugger.png)

## Activity Map 데이터가 없는 가능한 이유

Activity Map 구성 요소가 있는지 확인하려면 다음 각 사항을 확인하십시오.

* **AppMeasurement 버전**:Activity Map은 v1.6 이상에서 지원됩니다. 가장 안정적인 최신 버전의 AppMeasurement로 업그레이드하면 많은 에지 사례 문제가 해결됩니다.
* **Activity Map 모듈**:모듈이  `AppMeasurement_Module_Activity_Map` 파일에 있는지  `AppMeasurement.js` 확인합니다. 구현에서 Adobe Experience Platform Launch을 사용하는 경우 **[!UICONTROL 링크 추적]**&#x200B;에서 Analytics 확장을 구성할 때 **[!UICONTROL ClickMap]** 활성화를 선택해야 합니다.
* **쿠키 `s_sq`**:Activity Map은 데이터 수집을  `s_sq` 위한 쿠키에 따라 달라집니다.
   * 특히 `*.co.uk` 또는 `*.co.jp` 같은 지역 도메인의 경우 `cookieDomainPeriods` 변수가 올바르게 설정되어 있는지 확인합니다.
   * `linkInternalFilters` 변수가 원하는 값으로 설정되어 있는지 확인합니다. 클릭한 링크가 내부 필터와 일치하지 않는 경우 Activity Map은 이것을 종료 링크로 간주하며 데이터를 수집하지 않습니다.
* **실행 중인 Activity Map 오버레이**:Activity Map 오버레이가 활성화되면 AppMeasurement는 웹 페이지에 대한 클릭 데이터를 추적하지 않습니다.
