---
description: Adobe Analytics의 새로운 연속 기능 릴리스 전략에 대해 설명합니다.
title: Adobe Analytics 기능 릴리스
translation-type: tm+mt
source-git-commit: dcca8559c9e730c9e04981d69068786878062561
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 4%

---


# Adobe Analytics 기능 릴리스

지금까지 Adobe Analytics 기능 릴리스는 고정된 월별 일정을 따릅니다. 2020년 4월부터 Adobe Analytics는 기능 배포에 대한 확장 가능하고 단계별 접근 방식을 지원하는 지속적인 전달 모델로 전환했습니다.

## 출시 전략

[!UICONTROL 분석 작업 공간에서] 기능 플래그(&quot;전환&quot;이라고도 함)를 사용하여 새로운 기능의 가시성을 제어하고 전체 릴리스 전에 제어된 크기 테스트를 수행할 수 있습니다. 이 릴리스 전략에는 다음 단계가 포함됩니다.

* **프로덕션에 릴리스(RTP)**: 분석 작업 공간에서 기능 가시성이 꺼져 있는 상태로 코드가 프로덕션에 릴리스됩니다. **참고**: RTP에서 이 기능은 2.0 Analytics API에서 사용할 수 있습니다.

* **제한된 테스트**: 단계적인 릴리스는 내부 Adobe 사용자의 테스트부터 시작됩니다. 이후 몇 달 동안 0%에서 100%로 축소됩니다. 단계적 롤아웃은 Experience Cloud 조직 수준에서 발생하므로 조직의 권한 있는 모든 사용자는 동일한 경험을 받습니다.

* **GA(일반 가용성)**: 이 기능은 자격이 부여된 Experience Cloud 조직 중 100%에 제공되며 기능 릴리스가 완료되었습니다.

각 기능 릴리스를 통해 RTP에서 GA로의 타임라인이 다를 수 있습니다. 릴리스(RTP) 시작 2개월 이내에 기능이 GA가 되도록 릴리스를 짧게 유지하는 것이 목표입니다.

## 이점

단계별 릴리스를 통해 Adobe는 소프트웨어 배포 프로세스를 보다 효과적으로 확장할 수 있으며 GA 이전에 기능이 완전히 개선되도록 할 수 있습니다. 또한 고정된 월별 릴리스 창을 사용하지 않고 기능을 출시와 동시에 출시할 수 있습니다.

## FAQ

| 질문 | 답변 |
|---|---|
| 기능에 대한 빠른 액세스를 요청할 수 있습니까? | 아니요. 조기 액세스는 허용되지 않습니다.<br>초기 Analytics 개념을 테스트하려는 경우 [Adobe Analytics Labs](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/tech-previews/overview.html) 에서 업계 선도적인 혁신적인 기능에 대한 피드백을 제공하는 것이 좋습니다. |
| 이 릴리스 전략은 기능 액세스에 영향을 줍니까? | 아니요. 기능이 GA에 도달하면 Analytics 패키지에 포함된 경우 해당 기능에 액세스할 수 있습니다.<br>Analytics 패키지의 세부 사항은 관리 > [!UICONTROL 회사] 설정 [!UICONTROL >] 기능 액세스 수준 [아래에서](https://docs.adobe.com/content/help/en/analytics/admin/company-settings/feature-access-levels.html)확인할 수 있습니다. |