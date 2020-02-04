---
title: 데이터 수집 쿼리 매개 변수
description: 이미지 요청에 사용된 모든 쿼리 문자열 매개 변수를 나열합니다.
translation-type: tm+mt
source-git-commit: 2ffa989156dd9bc4f6ef9a216e8c06425cc39440

---


# 데이터 수집 쿼리 매개 변수

다음 표에는 Adobe가 이미지 요청에 사용하는 모든 쿼리 문자열 매개 변수가 나와 있습니다. 이 정보는 패킷 분석기를 사용하여 디버깅하거나, [이미지 요청을](packet-monitor.md)[하드코딩하거나, 동적 변수를](../other/hardcoded.md)사용할 때 사용할 수 [있습니다](../vars/page-vars/dynamic-variables.md).

| 매개 변수 | Analytics 구현 변수 | 설명 |
| --- | --- | --- |
| `aamlh` | 없음 | Audience Manager 위치 힌트.Experience Cloud 공유 프로필 통합에 사용됩니다. |
| `aamb` | 없음 | Audience Manager blob.Experience Cloud 공유 프로필 통합에 사용됩니다. |
| `aid` | 없음 | Analytics 방문자 ID. |
| `AQB` | 없음 | 이미지 요청 쿼리 문자열의 시작을 나타냅니다. |
| `AQE` | 없음 | 이미지 요청의 끝을 나타냅니다. 즉, 요청이 잘리지 않았습니다. |
| `bh` | 없음 | 브라우저 높이(픽셀 단위). 브라우저 높이 차원에 사용됩니다. |
| `bw` | 없음 | 브라우저 너비(픽셀 단위). 브라우저 너비 차원에 사용됩니다. |
| `c` | 없음 | 색상 품질(비트). 색상 깊이 차원에 사용됩니다. |
| `c.` | `contextData` | 컨텍스트 데이터 변수의 시작을 나타냅니다. 값을 포함하지 않습니다. |
| `.c` | `contextData` | 컨텍스트 데이터 변수의 끝을 나타냅니다. 값을 포함하지 않습니다. |
| `c1` - `c75` | `prop1` - `prop75` | 사용자 지정 트래픽 변수. |
| `cc` | `currencyCode` | 히트에 사용된 통화 유형. |
| `cdp` | `cookieDomainPeriods` | 도메인의 기간 수입니다. 쿠키를 올바로 저장하는 데 사용됩니다. |
| `ce` | `charSet` | 이미지 요청의 문자 인코딩. |
| `cl` | `cookieLifetime` |  방문자 쿠키의 수명입니다. |
| `ch` | `channel` | 사이트 섹션 차원에 사용됩니다. |
| `cp` | 없음 | 히트 유형 차원에 사용됩니다. |
| `ct` | 없음 | 연결 유형 차원에 사용됩니다. |
| `D` | `dynamicVariablePrefix` | 동적 변수에 사용할 항목을 나타냅니다. |
| `ev` | `events` | 쿼리 문자열의 축약입니다 `events` . |
| `events` | `events` | 페이지에 있는 이벤트의 쉼표로 구분된 목록입니다. |
| `g` | `pageURL` | 페이지의 현재 URL최대 255바이트 |
| `-g` | `pageURL` | 255바이트보다 긴 URL은 분할됩니다. 처음 255바이트는 `g` 매개 변수에 나타나고 나머지 모든 바이트는 `-g` 매개 변수에 나타납니다. |
| `gn` | `pageName` | 쿼리 문자열의 축약입니다 `pageName` . |
| `gt` | `pageType` | 쿼리 문자열의 축약입니다 `pageType` . |
| `h1` - `h5` | `hier1` - `hier5` | 계층 변수. |
| `hp` | 없음 | 더 이상 사용되지 않습니다. 이전 버전의 Adobe Analytics에서 현재 URL이 브라우저의 홈 페이지인지 확인했습니다. |
| `j` | 없음 | 브라우저에 설치된 JavaScript 버전. |
| `k` | 없음 | 쿠키 지원 차원에 사용됩니다. |
| `l1` - `l3` | `list1` - `list3` | 목록 변수. |
| `mid` | 없음 | Experience Cloud 방문자 ID. |
| `ndh` | 없음 | 이미지 요청이 AppMeasurement에서 발생했는지 여부를 나타내는 플래그. |
| `ns` | `visitorNameSpace` | 쿠키가 설정된 위치를 확인하는 데 도움이 됩니다. |
| `oid` | `objectID` | 마지막 페이지의 개체 식별자입니다. Activity Map에 사용됩니다. |
| `ot` | 없음 | 마지막 페이지의 개체 이름입니다. 이전 버전의 Activity Map에서 사용됩니다. |
| `p` | 없음 | 더 이상 사용되지 않습니다. 브라우저에서 사용되는 플러그인 목록입니다. |
| `pageName` | `pageName` | 페이지 차원에 사용됩니다. |
| `pageType` | `pageType` | 페이지를 찾을 수 없음 차원에 사용됩니다. |
| `pccr` | 없음 | 새 방문자에 대해서만 설정되고 항상 로 `true`설정됩니다. 무한 리디렉션을 방지합니다. |
| `pe` | `linkType` | 사용자 지정 링크의 유형을 결정합니다. |
| `pev1` | 없음 | 사용자 지정 링크가 발생한 URL입니다. |
| `pev2` | 없음 | 사용자 지정 링크 이름. |
| `pev3` | 없음 | 더 이상 사용되지 않습니다. 비디오 보고의 이전 버전에서 추적된 마일스톤입니다. |
| `pf` | 없음 | 플랫폼 플래그;for Adobe use only. 변경하지 마십시오. |
| `pid` | 없음 | 마지막 페이지의 페이지 식별자입니다. 이전 버전의 Activity Map에서 사용됩니다. |
| `pidt` | 없음 | 마지막 페이지의 페이지 식별자 유형입니다. 이전 버전의 Activity Map에서 사용됩니다. |
| `pl` | `products` | 쿼리 문자열의 축약입니다 `products` . |
| `products` | `products` | Products 변수. |
| `purchaseID` | `purchaseID` | 구매 중복 제거에 사용됩니다. |
| `r` | `referrer` | 히트의 참조 URL입니다. |
| `s` | 없음 | 모니터 해상도 차원에 사용됩니다. 화면 해상도를 `width x height`참조하십시오. |
| `server` | `server` | 서버 차원. |
| `sv` | `server` | 쿼리 문자열의 축약입니다 `server` . |
| `state` | `state` | 상태 차원입니다. |
| `t` | 없음 | 히트의 생성된 날짜/시간입니다. 형식을 `dd/mm/yyyy hh:mm:ss w o`사용합니다.<br>- `dd/mm/yyyy hh:mm:ss` JavaScript의 날짜/시간입니다. 달은 `0` `11` 1월이고 달은 12월입니다.<br>- `w` 요일이다. `0` 은 일요일이고 토요일은 `6` 토요일이다.<br>- `o` 음수 GMT 오프셋(분 단위)입니다. 예를 들어 GMT-7 `420` 입니다. |
| `ts` | `timestamp` | 히트와 함께 설정된 사용자 지정 타임스탬프. 보통 오프라인 추적에 사용됩니다. |
| `v` | 없음 | Java 활성화 차원에 사용됩니다. |
| `v0` | `campaign` | 추적 코드 차원입니다. |
| `v1` - `v250` | `evar1` - `eVar250` | 사용자 지정 전환 차원. |
| `vid` | `visitorID` | 방문자 ID 변수. |
| `vmk` | `vmk` | 더 이상 사용되지 않습니다. 서드 파티 쿠키에서 퍼스트 파티 쿠키로 마이그레이션할 수 있었습니다. |
| `vvp` | `variableProvider` | 데이터 커넥터에서 사용됩니다. |
| `xact` | `transactionID` | 데이터를 함께 연결하는 데 Data Sources와 함께 사용됩니다. |
| `zip` | `zip` | 우편 번호 차원에 사용됩니다. |
