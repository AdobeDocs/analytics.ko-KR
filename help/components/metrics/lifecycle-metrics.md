---
name: Mobile lifecycle metrics
description: Mobile SDK를 사용하여 수집된 데이터를 기반으로 하는 지표입니다.
feature: Metrics
source-git-commit: fa9ba599ccc3d6fe1176e6b2ec20457f30cb5959
workflow-type: ht
source-wordcount: '38'
ht-degree: 100%

---

# 모바일 라이프사이클 지표

| 라이프사이클 지표 이름 | 설명 | 컨텍스트 데이터 변수 |
| --- | --- | --- |
| 첫 번째 실행 | | `a.InstallEvent` |
| 업그레이드 | | `a.UpgradeEvent` |
| 시작 | | `a.LaunchEvent` |
| 충돌 | | `a.CrashEvent` |
| 총 세션 길이 | | TBD |
| 총 동작 시간 | | `a.action.time.total` |
| 앱의 동작 시간 | | `a.action.time.inapp` |
| 라이프타임 값 (이벤트) | | `a.ltv.amount` |

{style="table-layout:auto"}
