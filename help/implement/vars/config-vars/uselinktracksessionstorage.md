---
title: useLinkTrackSessionStorage
description: 링크 추적 데이터를 쿠키 대신 세션 저장소에 저장합니다.
translation-type: ht
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# useLinkTrackSessionStorage

조직에서 링크 추적을 사용하는 경우 AppMeasurement는 `s_sq` 쿠키를 사용하여 히트 간에 정보를 전달합니다. 일부 웹사이트 구성이 이 쿠키와 충돌합니다. 링크 추적에 브라우저 세션 저장소를 사용하고 쿠키 대신 Activity Map 데이터를 사용하려면 이 변수를 활성화합니다.

링크 추적을 위해 브라우저의 세션 저장소를 사용하는 경우 몇 가지 제한 사항이 있습니다.

* 프로토콜 간에 세션 저장소가 작동하지 않습니다. 예를 들어 HTTP에서 제공되는 페이지가 한 개 있고 HTTPS에서 제공되는 다음 페이지가 있습니다. 프로토콜 차이로 인해 AppMeasurement가 세션 저장소의 링크 추적 데이터에 액세스할 수 없습니다.
* 하위 도메인 간에 세션 저장소가 작동하지 않습니다. 예를 들어 방문자가 `store.example.com`로 이동한 다음 `toys.example.com`로 이동합니다. 다른 하위 도메인으로 인해 AppMeasurement가 세션 저장소의 링크 추적 데이터에 액세스할 수 없습니다.

>[!TIP] 링크 추적에 세션 저장소를 사용하는 가장 안정적인 구현은 단일 하위 도메인에서 HTTPS를 통해 모든 컨텐츠를 제공합니다.

AppMeasurement는 Adobe에 히트를 보낸 후 세션 저장소 링크 추적 데이터를 제거합니다. 또한 브라우저 탭이 닫히면 자동으로 만료됩니다.

## Adobe Experience Platform Launch에서 링크 추적 세션 스토리지 사용

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용하십시오.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.useLinkTrackSessionStorage

`s.useLinkTrackSessionStorage` 변수는 AppMeasurement가 `s_sq` 쿠키 대신 링크 추적 데이터에 세션 저장소를 사용하는지 여부를 결정하는 부울입니다. 기본값은 `false`입니다. AppMeasurement가 라인 추적 및 Activity Map에 `true` 쿠키 대신 세션 저장을 사용하도록 하려면 이 변수를 `s_sq`에 설정합니다.

```js
s.useLinkTrackSessionStorage = true;
```
