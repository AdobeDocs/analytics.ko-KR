---
description: '상호 장치 방문자 식별은 여러 장치의 방문자들을 연결하는 데 도움이 됩니다. 상호 장치 방문자 식별에서는 방문자 ID 변수 s.visitorID를 사용하여 여러 장치의 사용자를 연결합니다. '
keywords: Analytics Implementation
subtopic: Visitors
title: 여러 장치에서 사용자 연결
topic: Developer and implementation
uuid: 6243957b-5cc1-49ef-aa94-5b5ec4eac313
translation-type: tm+mt
source-git-commit: 0439440e10dddf8a5d64e4ea8f9868b521e5ca20

---


# 여러 장치에서 사용자 연결

> [!IMPORTANT] 장치 간에 방문자를 식별하는 이 방법은 더 이상 권장되지 않습니다. 구성 [요소](/help/components/cda/cda-home.md) 사용 안내서의 장치 간 분석을 참조하십시오.

상호 장치 방문자 식별은 여러 장치의 방문자들을 연결하는 데 도움이 됩니다. Cross-device visitor identification uses the `visitorID` variable to associate a user across devices. 이 `visitorID` 변수는 고유 방문자를 식별할 때 우선 순위가 가장 높습니다.

사용자 지정 방문자 ID로 히트를 전송하면 Adobe는 방문자 ID가 일치하는 모든 방문자 프로필을 확인합니다. 이 프로필이 있으면, 해당 시점부터 이미 시스템에 있는 방문자 프로필이 사용되고 이전 방문자 프로필은 더 이상 사용되지 않습니다.

Setting the `visitorID` variable is typically set after authentication, or after a visitor performs some other action that allows you to uniquely identify them independently of the device that is used. 유효한 식별자에는 사용자 이름, 이메일 주소 또는 개인 식별 정보가 포함되지 않은 내부 ID의 해시가 포함됩니다.

고객이 각 장치에서 로그인하면 모두 동일한 사용자 프로필에 연결됩니다. 방문자가 나중에 장치에서 로그아웃해도 Adobe는 각 장치의 브라우저 쿠키가 동일한 방문자 프로필에 속한다고 인식하므로 동일한 방문자 프로필에 계속 포함됩니다. 브라우저 쿠키가 삭제될 경우 가능하면 항상 변수를 사용하는 것이 좋습니다. `visitorID`

## 제한

자체 사용자 지정 방문자 ID를 사용하면 방문자 식별에 대한 제어를 강화할 수 있지만 그 제한이 있습니다.

* **방문자 중복 제거는 소급**&#x200B;적용되지 않습니다.방문자가 처음으로 사이트에 액세스한 후 인증하면 두 개의 고유 방문자가 계산됩니다. 일반 Analytics ID에 대한 고유 방문자 수 중 하나는 자동으로 생성되며, 다른 카운트는 로그인할 때 사용자 지정 방문자 ID에 대해 계산됩니다. 방문자가 새 장치를 사용하거나 쿠키를 지울 때마다 이러한 고유 방문자 복제가 발생합니다.
* **Experience Cloud ID 서비스와 비호환성**:상호 장치 방문자 식별이 도입된 이후 Adobe는 장치 전체에서 방문자를 추적하는 보다 강력하고 안정적인 방법을 발표했습니다. 이러한 새로운 식별 방법은 사용자 지정 방문자 ID 재정의와 호환되지 않습니다. ID 서비스, CDA(Cross-device Analytics) 또는 Device Co-op를 사용하려는 경우 Adobe는 `visitorID` 변수 사용을 강력히 권장합니다.
