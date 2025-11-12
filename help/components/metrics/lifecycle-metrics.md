---
name: Mobile lifecycle metrics
description: Mobile SDK를 사용하여 수집된 데이터를 기반으로 하는 지표입니다.
feature: Metrics
exl-id: 64af4942-d249-47a5-a62f-6051f4c44ee3
source-git-commit: 936644c719f46a1327c8a5aa247ed69a14d3da1e
workflow-type: tm+mt
source-wordcount: '37'
ht-degree: 100%

---

# 모바일 라이프사이클 지표

| 라이프사이클 지표 이름 | 설명 | 컨텍스트 데이터 변수 |
| --- | --- | --- |
| 첫 번째 실행 | | `a.InstallEvent` |
| 업그레이드 | | `a.UpgradeEvent` |
| 시작 | | `a.LaunchEvent` |
| 충돌 | | `a.CrashEvent` |
| 총 세션 길이 | | |
| 총 동작 시간 | | `a.action.time.total` |
| 앱의 동작 시간 | | `a.action.time.inapp` |
| 라이프타임 값 (이벤트) | | `a.ltv.amount` |

{style="table-layout:auto"}
