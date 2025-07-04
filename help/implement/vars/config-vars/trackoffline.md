---
title: trackOffline
description: 오프라인 추적을 활성화하거나 비활성화하여 AppMeasurement가 데이터를 수집하는 방식을 변경합니다.
feature: Appmeasurement Implementation
exl-id: 23a17ddc-01e6-42b6-81b0-c60f15a07231
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 89%

---

# trackOffline

오프라인 추적은 Adobe Analytics에서 데이터를 수집할 때 선택할 수 있는 방법입니다. 방문자가 인터넷 연결이 끊겼지만 사이트를 계속 탐색하는 경우 디바이스가 인터넷에 다시 연결되기 전까지 히트는 오프라인 큐에 저장됩니다. 오프라인 추적은 대개 모바일 애플리케이션에 사용됩니다.

`trackOffline` 변수는 구현에서 오프라인 추적을 사용할지 여부를 결정합니다.

>[!WARNING]
>
>이 변수를 활성화하기 전에 타임스탬프가 지정된 히트를 허용하도록 보고서 세트를 구성해야 합니다. 보고서 세트가 타임스탬프가 지정된 히트를 허용하지 않는데 이 변수가 활성화되면 데이터가 손실되어 복구할 수 없습니다.

활성화하면 AppMeasurement가 다음 프로세스를 사용하여 데이터를 Adobe에 전송합니다.

* 이미지 요청을 컴파일할 때 타임스탬프 쿼리 문자열 매개 변수가 포함됩니다.
* 디바이스가 Adobe 데이터 수집 서버에 연결할 수 없는 경우 히트는 디바이스에 로컬로 저장됩니다.
* 이후 각 히트 동안 AppMeasurement는 이미지 요청을 Adobe에 전송하려고 시도합니다.
   * Adobe 데이터 수집 서버에 연결할 수 없는 경우 히트는 디바이스의 큐에 추가됩니다.
   * Adobe 데이터 수집 서버에 도달할 수 있는 경우에는 디바이스가 오프라인일 때 히트와 히트 큐가 전송됩니다.

## 웹 SDK을 사용한 오프라인 추적

웹 SDK은 오프라인 추적을 지원하지 않습니다.

## Adobe Analytics 확장을 사용한 오프라인 추적

Adobe Analytics 확장에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 정의 코드 편집기를 사용하십시오.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.trackOffline

`s.trackOffline` 변수는 오프라인 추적을 활성화하거나 비활성화하는 부울입니다. 기본값은 `false`입니다. 오프라인 수집을 활성화하려면 이 값을 `true`로 설정하십시오.

```js
s.trackOffline = true;
```
