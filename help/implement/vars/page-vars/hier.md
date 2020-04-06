---
title: hier
description: Adobe Analytics에서 계층 변수를 구현합니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# hier

계층 변수는 사이트의 구조를 볼 수 있도록 해주는 사용자 지정 변수입니다.

>[!TIP] 이 변수는 이전 버전의 Adobe Analytics에서 더 일반적이었습니다. Adobe는 대신 [eVar](evar.md) 및 분류를 사용하는 것이 좋습니다.

이 변수는 사이트 구조에서 수준이 3개 이상인 사이트에 유용합니다. 예를 들어 미디어 사이트의 스포츠 섹션에는 4개 수준이 있을 수 있습니다. `Sports`, `Local Sports`, `Baseball`및 `Team name`를 참조하십시오. 누군가 야구 페이지, 스포츠, 로컬 스포츠 및 야구에 방문하는 경우 모든 수준이 해당 방문을 반영합니다.

Adobe는 구현에서 최대 5개의 계층 변수를 지원합니다. 계층이 활성화될 때 변수에 대한 구분 기호와 계층의 최대 수준 수를 결정합니다. 예를 들어, 구분 기호가 쉼표인 경우 계층은 다음과 비슷합니다.

```js
s.hier1 = "Sports,Local Sports,Baseball";
```

섹션 이름에 구분 기호가 없도록 하십시오. 예를 들어 섹션 중 하나를 호출하는 경우 쉼표 이외의 구분 기호를 `Coach Griffin, Jim`선택합니다. 총 변수 제한은 255바이트입니다. 구분 기호는 `||` 또는 과 같은 여러 문자로 구성되며 변수 값에 표시될 가능성이 `/|\`적습니다.

## 예

```js
s.hier1="Toys|Boys 6+|Legos|Super Block Tub";
```

```js
s.hier4="Sports/Local Sports/Baseball";
```
