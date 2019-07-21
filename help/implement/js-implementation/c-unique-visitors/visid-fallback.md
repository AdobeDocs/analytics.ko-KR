---
description: 다른 방문자 ID 방법이 실패할 경우, Adobe에서는 대체 쿠키를 설정하거나 IP 주소와 사용자 에이전트를 결합하여 방문자를 식별합니다.
keywords: Analytics 구현
seo-description: 다른 방문자 ID 방법이 실패할 경우, Adobe에서는 대체 쿠키를 설정하거나 IP 주소와 사용자 에이전트를 결합하여 방문자를 식별합니다.
seo-title: 폴백 ID 메서드
solution: Analytics
title: 폴백 ID 메서드
topic: 개발자 및 구현
uuid: F 242 D 481-81 F 0-4287-BE 4 F -52 FD 03 EB 01 FC
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 폴백 ID 메서드

다른 방문자 ID 방법이 실패할 경우, Adobe에서는 대체 쿠키를 설정하거나 IP 주소와 사용자 에이전트를 결합하여 방문자를 식별합니다.

## 방문자 식별 대비책 {#section_2BA15E4FA6034C3EBF43859406343EB6}

2013년 1월에 발표된 JavaScript 1.x 및 JavaScript H.25.3용 AppMeasurement에는 Adobe의 데이터 수집 서버에서 설정한 쿠키(`s_vi`라고 함)를 차단하는 브라우저를 사용하는 방문자를 위한 새로운 방문자 식별 대비책이 포함되어 있습니다. 이전에는 쿠키를 설정할 수 없을 경우, 데이터를 수집하는 동안 IP 주소와 사용자 에이전트 문자열의 조합을 사용하여 방문자를 식별했습니다.

이 업데이트를 사용하면 표준 `s_vi` 쿠키를 사용할 수 없을 경우, 무작위로 생성된 고유 ID를 사용하는 대체 쿠키가 웹 사이트의 도메인에 만들어집니다. `s_fid`라는 이 쿠키는 2년 동안 사용할 수 있으며 앞으로 식별 대비책으로 사용됩니다. This change should result in increased accuracy in visit and visitor counts in situations where the primary cookie ( `AMCV_` or `s_vi`) cannot be set.

총 방문 횟수에는 `s_vi` 쿠키나 대비책을 사용하여 식별된 모든 사용자가 포함됩니다.

## IP 주소, 사용자 에이전트, 게이트웨이 IP 주소 {#section_104819D74C594ECE879144FCC5DEF4BF}

라는 사용자 지정 코드에서 변수를 찾습니다. `AMCV_` 또는 `s_vi``s_fid` 쿠키를 설정할 수 없는 경우, 방문자는 IP 주소와 사용자 에이전트의 조합을 사용하여 식별됩니다.
