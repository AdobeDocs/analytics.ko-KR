---
description: 페이지 변수는 pageName, List Props, List Variables 등과 같이, 보고서를 직접 채웁니다.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: 페이지 변수
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: ea6109f2f9aa421001fde6d7bec65b82beda883c

---


# channel

이 변수는 사이트의 섹션을 식별하는 데 종종 사용됩니다.

<!-- 

channel.xml

 -->

예를 들어 매장 주인에게는 전자 제품, 장난감 또는 의류 등의 섹션이 있을 수 있습니다. 미디어 사이트에는 뉴스, 스포츠 또는 비즈니스 등의 섹션이 포함될 수 있습니다.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 100바이트 | CH | 사이트 컨텐츠 &gt; 사이트 섹션 | "" |

모든 페이지에서 채널 변수를 채우는 것이 좋습니다. 또한 *`channel`* 과 [!UICONTROL page name] 변수 간에 상관 관계를 설정할 수도 있습니다.

섹션에 하나 이상의 하위 섹션 레벨이 있는 경우에는 *`channel`* 변수에서 그러한 섹션을 표시하거나 별도 변수를 사용하여 해당 레벨을 식별할 수 있습니다.

**구문 및 가능한 값**

```js
s.channel="value"
```

*`channel`* 변수에는 이 값에 대한 추가 제한이 없습니다.

**예** {#section_2527B2BB1CFD46CB952178ABF7A9028A}

```js
s.channel="Electronics"
```

```js
s.channel="Media"
```

**함정, 질문 및 팁** {#section_61941D5E4E644B59A267A4F44FD5DE8C}

사이트에 여러 수준이 포함되어 있는 경우는 *`hierarchy`* 또는 다른 변수를 사용하여 해당 수준을 지정할 수 있습니다. *`channel`* 변수는 지속적이 아니지만 동일한 페이지에서 실행된 성공 이벤트는 *`channel`* 값에 적용됩니다.
