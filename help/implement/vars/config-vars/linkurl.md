---
title: linkURL
description: 링크 추적 호출에서 자동으로 생성된 링크 URL AppMeasurement가 사용하는 링크를 재정의합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# linkURL

링크 추적 호출이 Adobe로 전송될 때마다 데이터 수집 서버는 자동으로 URL을 검색합니다. 이 `linkURL` 변수를 사용하여 감지된 URL을 무시합니다.

## Adobe Experience Platform Launch의 링크 URL

Launch에는 이 변수를 사용할 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 지정 코드 편집기를 사용합니다.

## s.linkAppMeasurement 및 Launch 사용자 지정 코드 편집기의 URL

이 `s.linkURL` 변수는 링크를 클릭할 때 브라우저의 URL을 포함하는 문자열입니다. 이 변수는 보고에서 사용할 수 있는 차원을 채우지 않습니다.

```js
s.linkURL = "https://example.com";
```

이 [`linkName`](linkname.md) 변수가 링크 추적 호출에 설정되지 않은 경우 `linkURL` 변수가 대신 사용됩니다.
