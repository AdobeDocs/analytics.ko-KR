---
title: Activity Map 데이터 수집 문제 해결
description: 이미지 요청에서 Activity Map 데이터를 볼 수 없는 이유를 파악합니다
feature: Activity Map
role: User, Admin
exl-id: 7f9e06ba-4040-483b-b18b-cdfe85bca486
source-git-commit: 9a70d79a83d8274e17407229bab0273abbe80649
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 2%

---

# Activity Map 데이터 수집 문제 해결

Activity Map 차원에 대한 데이터가 표시되지 않는 경우 이 페이지를 사용하여 이유를 확인하십시오.

## 디버거를 사용하여 데이터 수집 확인

먼저 AppMeasurement가 Activity Map 데이터를 올바로 수집하는지 확인하십시오.

1. 다운로드 및 설치 [Adobe Experience Cloud Debugger Chrome 확장 프로그램](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html).
2. 웹 페이지로 이동한 다음 링크를 클릭합니다.
3. 후속 페이지가 로드되면 디버거를 엽니다. 사이에 삽입된 Activity Map 컨텍스트 데이터 변수가 표시되는지 확인합니다. `activitymap.` 및 `.activitymap`:

![디버거 데이터](assets/debugger.png)

## Activity Map 데이터가 없는 가능한 이유

다음 각 항목을 확인하여 Activity Map 구성 요소가 있는지 확인하십시오.

* **AppMeasurement 버전**: Activity Map은 v1.6 이상에서 지원됩니다. 안정적인 최신 버전의 AppMeasurement로 업그레이드할 때 많은 에지 사례 문제가 해결됩니다.
* **Activity Map 모듈**: 다음 경우에 확인 `AppMeasurement_Module_Activity_Map` 모듈이 `AppMeasurement.js` 파일. 구현에서 Adobe Experience Platform을 사용하여 데이터를 수집하는 경우 **[!UICONTROL ClickMap 활성화]** 에서 Analytics 확장을 구성할 때 이 확인됩니다. **[!UICONTROL 링크 추적]**.
* **다음 `s_sq` 쿠키**: Activity Map은 다음에 따라 다릅니다. `s_sq` 데이터 수집용 쿠키.
   * 다음을 확인하십시오. `cookieDomainPeriods` 변수가 올바르게 설정됨, 특히 다음과 같은 지역 도메인의 경우 `*.co.uk` 또는 `*.co.jp`.
   * 다음을 확인하십시오. `linkInternalFilters` 변수가 원하는 값으로 설정되어 있습니다. 클릭한 링크가 내부 필터와 일치하지 않으면 Activity Map은 종료 링크로 간주하여 데이터를 수집하지 않습니다.
* **Activity Map 오버레이 실행 중**: Activity Map 오버레이가 활성화된 경우 AppMeasurement가 웹 페이지에 대한 클릭 데이터를 추적하지 않습니다.
