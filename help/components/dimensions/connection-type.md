---
title: 연결 유형
description: 방문자가 인터넷에 연결하는 방법입니다.
feature: Dimensions
exl-id: 149b2353-6128-4e0c-a73a-bc5a37c66b52
TQID: https://experienceleague.adobe.com/5kdDrW5vGzc4EKpLOF4VWzXish439t-aGp6q-XcK3Fs
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 236
ht-degree: 94%

---

# 연결 유형

&#39;연결 유형&#39; [차원](overview.md)은(는) 방문자가 인터넷에 연결한 방법을 보여 줍니다. 이 차원은 방문자가 사이트를 탐색하기 위해 인터넷에 연결하는 방법을 결정하는 데 유용합니다. 방문자의 연결 속도에 따라 사이트 콘텐츠를 최적화하는 데 사용할 수 있습니다.

## 이 차원을 데이터로 채우기

이 차원은 [`ct` 쿼리 문자열](/help/implement/validate/query-parameters.md)과 Adobe 서버측 논리의 조합을 사용합니다. Adobe는 값을 결정하기 위해 다음 규칙을 사용합니다.

1. `ct` 쿼리 문자열이 `"modem"`인 경우 차원 항목을 `"Modem"`으로 설정합니다. AppMeasurement는 지원되지 않는 Internet Explorer 브라우저에서만 이 데이터를 수집하므로 이 차원 항목이 일반적이지는 않습니다.
1. 히트의 IP 주소를 확인하고 Adobe 내부의 조회 테이블을 참조합니다. IP 주소가 이동통신사의 주소인 경우 차원 항목을 `"Mobile Carrier"`로 설정합니다.
1. `ct` 쿼리 문자열이 `"lan"`인 경우 차원 항목을 `"LAN/Wifi"`로 설정합니다.
1. 히트가 [데이터 소스](/help/import/data-sources/overview.md)에서 발생하거나 특별한 유형의 조회로 간주되는 경우 차원 항목을 `"Not specified"`로 설정합니다.
1. 위의 규칙 중 어느 것도 충족되지 않으면 기본값은 `"LAN/Wifi"`입니다.

## 차원 항목

차원 항목에는 `LAN/Wifi`, `Mobile Carrier`, `Modem` 및 `Not Specified`가 포함됩니다.

* **`LAN/Wifi`**: 유선 또는 Wi-Fi 핫스팟을 통해 인터넷에 연결된 방문자입니다.
* **`Mobile Carrier`**: 이동통신사를 통해 인터넷에 연결된 방문자입니다.
* **`Modem`**: 지원되지 않는 Internet Explorer 브라우저에서 모뎀을 통해 인터넷에 연결된 방문자입니다.
* **`Not Specified`**: 히트에 연결 유형이 없습니다.
