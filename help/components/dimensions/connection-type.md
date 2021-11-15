---
title: 연결 유형
description: 방문자가 인터넷에 연결하는 방법입니다.
exl-id: 149b2353-6128-4e0c-a73a-bc5a37c66b52
source-git-commit: 82d6137bc9229bbaa997c6856690bf76c20b755c
workflow-type: ht
source-wordcount: '235'
ht-degree: 100%

---

# 연결 유형

“연결 유형” 차원은 방문자가 인터넷에 연결한 방법을 보여 줍니다. 이 차원은 방문자가 사이트를 탐색하기 위해 인터넷에 연결하는 방법을 결정하는 데 유용합니다. 방문자의 연결 속도에 따라 사이트 콘텐츠를 최적화하는 데 사용할 수 있습니다.

## 이 차원을 데이터로 채우기

이 차원은 [`ct` 쿼리 문자열](/help/implement/validate/query-parameters.md)과 Adobe 서버측 논리의 조합을 사용합니다. Adobe는 값을 결정하기 위해 다음 규칙을 사용합니다.

1. `ct` 쿼리 문자열이 `"modem"`인 경우 차원 항목을 `"Modem"`으로 설정합니다. AppMeasurement는 지원되지 않는 Internet Explorer 브라우저에서만 이 데이터를 수집하므로 이 차원 항목이 일반적이지는 않습니다.
1. 히트의 IP 주소를 확인하고 Adobe 내부의 조회 테이블을 참조합니다. IP 주소가 이동통신사의 주소인 경우 차원 항목을 `"Mobile Carrier"`로 설정합니다.
1. `ct` 쿼리 문자열이 `"lan"`인 경우 차원 항목을 `"LAN/Wifi"`로 설정합니다.
1. 히트가 [데이터 소스](/help/import/c-data-sources/datasrc-home.md)에서 발생하거나 특별한 유형의 조회로 간주되는 경우 차원 항목을 `"Not specified"`로 설정합니다.
1. 위의 규칙 중 어느 것도 충족되지 않으면 기본값은 `"LAN/Wifi"`입니다.

## 차원 항목

차원 항목에는 `LAN/Wifi`, `Mobile Carrier`, `Modem` 및 `Not Specified`가 포함됩니다.

* **`LAN/Wifi`**: 유선 또는 Wi-Fi 핫스팟을 통해 인터넷에 연결된 방문자입니다.
* **`Mobile Carrier`**: 이동통신사를 통해 인터넷에 연결된 방문자입니다.
* **`Modem`**: 지원되지 않는 Internet Explorer 브라우저에서 모뎀을 통해 인터넷에 연결된 방문자입니다.
* **`Not Specified`**: 히트에 연결 유형이 없습니다.
