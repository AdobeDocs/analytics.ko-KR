---
title: hier
description: Adobe Analytics에서 계층 변수를 구현합니다.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 100%

---


# hier

계층 변수는 사이트의 구조를 볼 수 있도록 해주는 사용자 지정 변수입니다.

>[!TIP]
>
>이 변수는 이전 버전의 Adobe Analytics에서 더 일반적이었습니다. Adobe에서는 대신 [eVar](evar.md) 및 분류를 사용하는 것이 좋습니다.

이 변수는 사이트 구조의 수준이 4 이상인 사이트에 유용합니다. 예를 들어 미디어 사이트의 스포츠 섹션에는 4개 수준(`Sports`, `Local Sports`, `Baseball`및 `Team name`)이 있을 수 있습니다. 누군가 야구 페이지를 방문하면 스포츠, 해외 스포츠 및 야구가 해당 방문을 모두 반영합니다.

Adobe는 구현에서 최대 5개의 계층 변수를 지원합니다. 계층 활성화 시, 변수에 대한 구분 기호와 계층의 최대 수준 수를 결정합니다. 예를 들어 구분 기호가 쉼표인 경우 계층은 다음과 유사하게 보입니다.

```js
s.hier1 = "Sports,Local Sports,Baseball";
```

섹션 이름 중에 그 안에 구분 기호가 포함되는 섹션이 없도록 하십시오. 예를 들어 섹션 중 하나를 호출하면 `Coach Griffin, Jim`쉼표가 아닌 구분 기호를 선택합니다. 총 변수 제한은 255바이트입니다. 구분 기호는 `||` 또는 `/|\` 등의 여러 문자로 구성될 수 있으며 변수 값에 표시될 가능성이 줄어듭니다.

## 예

```js
s.hier1="Toys|Boys 6+|Legos|Super Block Tub";
```

```js
s.hier4="Sports/Local Sports/Baseball";
```
