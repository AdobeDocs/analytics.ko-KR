---
title: 모바일 라이프사이클 지표
description: Mobile SDK를 사용하여 수집된 데이터를 기반으로 하는 지표입니다.
feature: Metrics
exl-id: 64af4942-d249-47a5-a62f-6051f4c44ee3
TQID: 'https://experienceleague.adobe.com/Y1IigGbQygTsS9UD3WEp9z8rLTqkeDuhZZ83AJQMa3o'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: 6fd4400b33fcfc8bc3cd3ffc54fa738fef3441ef
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 10%
---
# 모바일 라이프사이클 지표

>[!BEGINSHADEBOX]

*이 페이지에서는 Adobe Experience Platform Mobile SDK을 통해 일반적으로 추적된 데이터를 참조합니다. Mobile SDK을 사용하여 추적한 차원에 대해서는 [모바일 라이프사이클 차원](../dimensions/lifecycle-dimensions.md)을 참조하십시오. 사용자 에이전트를 사용하는 모바일 장치에 대한 자세한 내용은 [모바일 조회 차원](../dimensions/mobile-dimensions.md).*&#x200B;을 참조하세요.

>[!ENDSHADEBOX]

| 라이프사이클 지표 이름 | 설명 | 컨텍스트 데이터 변수 |
| --- | --- | --- |
| **[!UICONTROL 첫 번째 실행]** | 앱을 설치하거나 다시 설치한 후 처음으로 앱을 실행한 횟수입니다. | `a.InstallEvent` |
| **[!UICONTROL 업그레이드]** | 업그레이드 후 또는 버전 번호가 변경된 후 앱을 처음 실행한 횟수입니다. | `a.UpgradeEvent` |
| **[!UICONTROL 시작]** | 충돌 및 설치 후 실행을 포함하여 앱이 실행된 횟수입니다. 라이프사이클 세션 시간이 초과된 후 앱이 백그라운드에서 다시 시작될 때도 시작이 계산됩니다. | `a.LaunchEvent` |
| **[!UICONTROL 충돌]** | 앱이 닫히기 전에 충돌한 횟수입니다. 다음에 앱을 시작할 때 충돌이 보고됩니다. | `a.CrashEvent` |
| **[!UICONTROL 총 세션 길이]** | 앱이 전경에서 열려 있는 시간을 기반으로 하여 앱 세션이 지속된 총 시간(초)입니다. 각 론치는 이전 세션의 길이를 보고합니다. 이 지표는 이러한 값의 합계입니다. | `a.PrevSessionLength` |
| **[!UICONTROL 총 동작 시간]** | 세션 간 시간 작업의 시작과 끝 사이의 총 시간(초)(시계 시간)입니다. 기존 Mobile Services SDK(4.x)에서 `trackTimedAction` 메서드로 채워집니다. | `a.action.time.total` |
| **[!UICONTROL 앱의 동작 시간]** | 세션 간 시간 작업의 시작과 끝 사이에 앱에서 소요된 시간(초)입니다. 기존 Mobile Services SDK(4.x)에서 `trackTimedAction` 메서드로 채워집니다. | `a.action.time.inapp` |
| **[!UICONTROL 라이프타임 값(이벤트)]** | 라이프타임 구매, 광고 보기, 비디오 전체 보기 또는 소셜 공유와 같은 사용자의 라이프타임 값입니다. 기존 Mobile Services SDK(4.x)에서 `trackLifetimeValueIncrease` 메서드로 채워집니다. | `a.ltv.amount` |

>[!NOTE]
>
>[!UICONTROL 총 동작 시간], [!UICONTROL 앱의 동작 시간] 및 [!UICONTROL 라이프타임 값(이벤트)] 지표는 더 이상 지원되지 않는 레거시 Mobile Services SDK(4.x)의 메서드로 채워집니다. Adobe Experience Platform Mobile SDK은 이러한 지표를 자동으로 채우지 않습니다. 시간 작업 및 라이프타임 값 추적에 대한 대안은 [Adobe 모바일 라이브러리(v4)에서 Experience Platform Analytics로 마이그레이션](https://developer.adobe.com/client-sdks/resources/upgrade-platform-sdks/analytics/)을 참조하십시오.
