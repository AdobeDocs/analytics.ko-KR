---
description: 버전 14에서 고유 방문자는 지정된 기간 내에 처음 사이트를 방문하는 방문자를 말합니다. 예를 들어 고유 방문자는 일주일에 10번 사이트를 방문할 수 있지만, 기간이 주인 경우 단일 고유 방문자는 해당 주에 한 번만 카운트됩니다. 그 주가 끝나면 같은 고유 방문자가 다른 기간 동안 다시 카운트될 수 있습니다.
seo-description: 버전 14에서 고유 방문자는 지정된 기간 내에 처음 사이트를 방문하는 방문자를 말합니다. 예를 들어 고유 방문자는 일주일에 10번 사이트를 방문할 수 있지만, 기간이 주인 경우 단일 고유 방문자는 해당 주에 한 번만 카운트됩니다. 그 주가 끝나면 같은 고유 방문자가 다른 기간 동안 다시 카운트될 수 있습니다.
seo-title: 고유 방문자 수
solution: Analytics
title: 고유 방문자 수
topic: 지표
uuid: AE 210698-99 F 9-485 E-A 640-C 7520807 ADC 7
translation-type: tm+mt
source-git-commit: ecc762f73f9a303cebf48668b807fef9a2f055c5

---


# 고유 방문자 수

버전 14에서 고유 방문자는 지정된 기간 내에 처음 사이트를 방문하는 방문자를 말합니다. 예를 들어 고유 방문자는 일주일에 10번 사이트를 방문할 수 있지만, 기간이 주인 경우 단일 고유 방문자는 해당 주에 한 번만 카운트됩니다. 그 주가 끝나면 같은 고유 방문자가 다른 기간 동안 다시 카운트될 수 있습니다.

## 버전 14와 15 간 차이점

Version 14 does not remove duplicate [!UICONTROL Visits] and [!UICONTROL Unique Visitors] metrics from classifications-based reports. 예를 들어 두 개의 비디오 클립이 동일 분류를 공유한 경우, 두 클립을 모두 본 한 명의 방문자가 분류 기반 보고서에서 두 개의 [!UICONTROL 방문] 횟수 및 [!UICONTROL 고유 방문자 수]로 기록되었습니다.

버전 15는 이제 분류 기반 보고서로부터 중복 [!UICONTROL 방문] 횟수와 [!UICONTROL 고유 방문자 수]를 제거합니다. 이 방식이 보다 정확한 [!UICONTROL 방문] 횟수와 [!UICONTROL 방문자] 수 파악이 가능하지만, 일반적으로 분류 기반 보고서의 경우 [!UICONTROL 방문] 횟수와 [!UICONTROL 고유 방문자 수] 지표에 있어 업그레이드 전에 수집된 데이터에 비해 수치가 낮아지는 결과가 생깁니다.

| 사용 | 설명 |
|---|---|
| 트래픽 | 방문자는 웹 사이트에 들어오는 사람입니다. 영구적 쿠키는 필요하지 않습니다. |
| 전환 | 방문자는 웹 사이트에 들어오는 사람입니다. 전환 관련 이벤트 또는 작업이 발생할 때 카운트됩니다. |
| Ad Hoc Analysis | 방문자는 웹 사이트에 들어오는 사람입니다. 영구적 쿠키는 필요하지 않습니다. |

[고유 방문자 보고서 - 버전 15 및 애드혹 분석을 참조하십시오](../../../components/c-variables/dimensionslist/reports-unique-visitors-v15-dsc.md#concept_877141D6D1E743DA9FAB41C72A8121C7).

>[!MORE_LIKE_THIS]
>
>* [일일 고유 방문자 명](/help/components/c-variables/c-metrics/metrics-daily-unique-visitors.md)

