---
title: linkURL
description: 링크 추적 호출에서 AppMeasurement가 사용하는 자동으로 생성된 링크 URL을 무시합니다.
exl-id: 15d6e423-d9fc-4f84-ad39-0bd91399cde4
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 80%

---

# linkURL

링크 추적 호출이 Adobe에 전송될 때마다 데이터 수집 서버가 자동으로 URL을 감지합니다. 감지된 URL을 무시하려면 `linkURL` 변수를 사용하십시오.

## Adobe Experience Platform에서 태그를 사용하여 URL 연결

데이터 수집 UI에 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용하십시오.

## AppMeasurement 및 사용자 지정 코드 편집기의 s.linkURL

`s.linkURL` 변수는 링크를 클릭할 때 브라우저의 URL을 포함하는 문자열입니다. 이 변수는 보고에서 사용할 수 있는 차원을 채우지 않습니다.

```js
s.linkURL = "https://example.com";
```

[tl ()](../functions/tl-method.md) 메서드의 세 번째 인수가 설정되어 있지 않으면, 대신 `linkURL` 변수를 사용합니다.
