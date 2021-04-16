---
description: 처리 규칙은 데이터 수집을 간소화하고 데이터가 보고 기능으로 전송될 때 컨텐츠를 관리합니다.
subtopic: Processing rules
title: 처리 규칙 개요
feature: 관리 도구
uuid: 6b4ee7c9-2b86-47a6-b64c-c8d644fff67d
exl-id: 0244aba2-4345-463a-8528-d4dcd2f872ff
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 68%

---

# 처리 규칙 개요

처리 규칙은 데이터 수집을 간소화하고 데이터가 보고 기능으로 전송될 때 컨텐츠를 관리합니다. 처리 규칙은 다음에 대한 인터페이스를 제공하여 IT 그룹 및 웹 개발자와의 상호 작용을 단순화하는 데 도움이 됩니다.

* 제품 개요 페이지의 이벤트 설정
* 쿼리 문자열 매개 변수로 캠페인 채우기
* 더 쉽게 보고할 수 있도록 prop에서 카테고리 및 페이지 이름 연결
* evar를 prop에 복사하여 경로 보기
* 철자가 틀린 사이트 섹션 정리
* 쿼리 문자열에서 eVar까지의 내부 검색어 또는 캠페인 ID 가져오기

>[!VIDEO](https://video.tv.adobe.com/v/26124/?quality=12&learn=on)

## 처리 규칙 권한 {#section_8A4846688050453784DAE4D89355169A}

관리자는 기본적으로 처리 규칙 **을(를) 사용할 수 있는 권한을 가집니다.** 관리자는 관리 도구 인터페이스를 통해 관리자가 아닌 사용자에게 이러한 권한을 부여할 수도 있습니다. 자세한 내용은 []

![](assets/processing-rules.png)

>[!IMPORTANT]
>
>처리 규칙은 Analytics 데이터에 영구적으로 영향을 주므로, Adobe은 처리 규칙 관리자가 Adobe Analytics에서 인증 교육을 받고 보고서 세트의 모든 데이터 소스(표준 웹 사이트, 모바일 사이트, 모바일 앱, 데이터 삽입 API 등)에 익숙해야 합니다. 다양한 플랫폼에서 입력한 컨텍스트 데이터 변수 및 표준 변수에 대한 지식은 데이터를 실수로 삭제하거나 변경하는 일이 없도록 하는 데 도움이 됩니다.

## 컨텍스트 데이터를 사용하여 데이터 수집 단순화 {#section_09EEA03612D24C15839631AA9E9668D8}

컨텍스트 데이터 변수는 처리 규칙에만 사용할 수 있는 변수 유형입니다. 컨텍스트 데이터 변수를 사용하기 위해, 키/값 데이터 쌍이 구현에 의해 전송되며, 처리 규칙을 사용하여 표준 Analytics 변수에서 이러한 변수를 캡처합니다. 이를 통해 프로그래머가 어떤 prop 및/또는 eVar가 어떤 값을 포함해야 하는지 정확하게 이해할 필요가 없습니다.

```js
s.contextData['author'] = "Robert Munch";
s.contextData['section'] = "Books";
s.contextData['genre'] = "Youth";
```

코드를 설정하고 나면 처리 규칙을 설정하여 변수에 값을 할당할 수 있습니다. 예를 들어,

1. `author`을(를) `eVar2`에 매핑
2. `section`을 `prop1` 및 `eVar3`에 매핑
3. `author` 및 `section`이 존재하는 경우 `event5` 설정

자세한 내용은 구현 사용자 안내서의 [contextData](/help/implement/vars/page-vars/contextdata.md)을 참조하십시오.

## 처리 규칙을 사용하여 데이터 히트 및 이벤트 트리거 변환 {#section_8284E72E999244E091CD7FB1A22342B6}

처리 규칙은 들어오는 값을 모니터링하여 일반적인 오타를 변형하고 보고된 데이터를 기준으로 이벤트를 설정할 수 있습니다. Prop을 eVar에 복사하고, 보고서에 값을 연결하며, 이벤트를 설정할 수 있습니다.

## 보고에 컨텍스트 데이터 변수 사용  {#section_BD098BC503024A0B8703596628071134}

컨텍스트 데이터 변수가 구현 내에 정의된 경우 해당 변수를 eVar과 같은 변수에 복사해야 보고에 사용할 수 있습니다.

자세한 내용은 [컨텍스트 데이터 변수를 eVar](processing-rules-examples/processing-rules-copy-context-data.md)에 복사 및 [컨텍스트 데이터 변수](processing-rules-examples/processing-rules-copy-context-data-event.md)를 사용하여 이벤트 설정을 참조하십시오.
