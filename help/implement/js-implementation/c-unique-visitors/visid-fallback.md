---
description: 다른 방문자 ID 방법이 실패할 경우, Adobe에서는 대체 쿠키를 설정하거나 IP 주소와 사용자 에이전트를 결합하여 방문자를 식별합니다.
keywords: Analytics Implementation
solution: Analytics
title: 대체 ID 방법
topic: Developer and implementation
uuid: f242d481-81f0-4287-be4f-52fd03eb01fc
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 대체 ID 방법

다른 방문자 ID 방법이 실패할 경우, Adobe에서는 대체 쿠키를 설정하거나 IP 주소와 사용자 에이전트를 결합하여 방문자를 식별합니다.

## 방문자 식별 대비책 {#section_2BA15E4FA6034C3EBF43859406343EB6}

AppMeasurement for JavaScript 1.x and JavaScript H.25.3 (released January 2013) contain a new fallback visitor identification method for visitors whose browser blocks the cookie set by Adobe's data collection servers (called `s_vi`). 이전에는 쿠키를 설정할 수 없을 경우, 데이터를 수집하는 동안 IP 주소와 사용자 에이전트 문자열의 조합을 사용하여 방문자를 식별했습니다.

이 업데이트를 사용하면 표준 `s_vi` 쿠키를 사용할 수 없을 경우, 무작위로 생성된 고유 ID를 사용하는 대체 쿠키가 웹 사이트의 도메인에 만들어집니다. `s_fid`라는 이 쿠키는 2년 동안 사용할 수 있으며 앞으로 식별 대비책으로 사용됩니다. 기본 쿠키(`AMCV_` 또는 `s_vi`)를 설정할 수 없는 상황에서는 이 변경 사항으로 인해 방문 및 방문자 수의 정확도가 높아집니다.

총 방문 횟수에는 `s_vi` 쿠키나 대비책을 사용하여 식별된 모든 사용자가 포함됩니다.

## IP 주소, 사용자 에이전트, 게이트웨이 IP 주소 {#section_104819D74C594ECE879144FCC5DEF4BF}

라는 사용자 지정 코드에서 변수를 찾습니다. `AMCV_` 또는 `s_vi` 및 `s_fid` 쿠키를 설정할 수 없는 경우에는 IP 주소와 사용자 에이전트의 조합을 사용하여 방문자를 식별합니다.
