---
description: Adobe Analytics의 연속 기능 릴리스 전략에 대해 설명합니다.
title: Adobe Analytics 기능 릴리스
exl-id: 1e403bef-4aab-4a9a-a358-62449ce801ff
source-git-commit: a6f2e241617d118479b79d00305f7ed4dc3dfd67
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 92%

---

# Adobe Analytics 기능 릴리스

Adobe Analytics 릴리스는 기능 배포에 대한 확장 가능한 단계별 접근 방식을 고려하는 연속 제공 모델에서 작동합니다.

## 출시 전략

[!UICONTROL Analysis Workspace]는 기능 플래그 (&quot;전환&quot;이라고도 함)를 사용하여 새로운 기능의 가시성을 제어하므로 전체 릴리스 전에 통제된 크기 테스트를 수행할 수 있습니다. 이 릴리스 전략에는 다음 단계가 포함됩니다.

* **프로덕션에 릴리스 (RTP)**: Analysis Workspace에서 기능 가시성이 해제되어 있는 상태로 코드가 프로덕션에 릴리스됩니다. 이 기능은 때때로 2.0 Analytics API에서 사용할 수 있습니다.

* **제한된 테스트**: 단계적인 릴리스는 내부 Adobe 사용자에 의한 테스트부터 시작됩니다. 그런 다음 릴리스의 가용성은 몇 개월 동안 0%에서 100%로 확장됩니다. 단계적 롤아웃은 Experience Cloud 조직 수준에서 발생하므로 조직에서 권한이 있는 모든 사용자는 동일한 경험을 합니다.

* **GA (일반 배포)**: 권한이 있는 Experience Cloud 조직의 100%가 이 기능을 사용할 수 있으며 기능 릴리스가 완료되었습니다.

각 기능 릴리스 시 RTP에서 GA로의 타임라인은 달라질 수 있습니다. 릴리스 시작 (RTP) 2개월 이내에 기능이 GA 상태가 되도록 릴리스를 짧게 유지하는 것이 목표입니다.

## 기능 플래그

기능 플래그는 릴리스 중 새로운 기능의 가시성을 제어하는 데 사용됩니다. Adobe는 릴리스 중 최적의 환경을 위해 `app.launchdarkly.com`을 방화벽의 [허용 목록](/help/technotes/ip-addresses.md)에 추가할 것을 권장합니다. GA에 도달한 직후 플래그가 제거됩니다.

**도움말 > Workspace 정보 > 활성 기능 플래그**&#x200B;에서 언제든지 활성 기능 플래그를 볼 수 있습니다.

## 이점

단계별 릴리스를 통해 Adobe는 소프트웨어 배포 프로세스를 보다 효과적으로 확장할 수 있으며 GA 전에 기능을 완전히 확정할 수 있습니다. 또한 고정된 월별 릴리스 기간에 얽매이지 않고 기능을 개발하자마자 출시할 수 있습니다.

## FAQ

| 질문 | 답변 |
| --- | --- |
| 기능에 대한 조기 액세스를 요청할 수 있습니까? | 아니요. 조기 액세스는 허용되지 않습니다.<br>초기 Analytics 개념을 테스트하려는 경우 [Adobe Analytics Labs](/help/analyze/labs.md)를 사용하여 업계를 선도하는 혁신적인 기술에 대한 피드백을 제공할 것을 권장합니다. |
| 이 릴리스 전략은 기능 액세스에 영향을 줍니까? | 아니요. 기능이 GA에 도달하면 Analytics 패키지에 포함된 경우 이 기능에 액세스할 수 있습니다.<br>Analytics 패키지에 대한 세부 사항은 [기능 액세스 수준](/help/admin/company/feature-access-levels.md)에서 확인할 수 있습니다. |
