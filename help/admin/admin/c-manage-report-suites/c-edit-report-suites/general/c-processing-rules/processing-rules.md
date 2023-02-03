---
description: 처리 규칙은 데이터 수집을 간소화하고 데이터가 보고 기능으로 전송될 때 콘텐츠를 관리합니다.
subtopic: Processing rules
title: 처리 규칙 개요
feature: Processing Rules
exl-id: 0244aba2-4345-463a-8528-d4dcd2f872ff
source-git-commit: 71ff81a0ae67c6f4cc9a8df567e27223cc63f18c
workflow-type: ht
source-wordcount: '373'
ht-degree: 100%

---

# 처리 규칙 개요

처리 규칙은 데이터 수집을 간소화하고 데이터가 보고 기능으로 전송될 때 콘텐츠를 관리합니다. 처리 규칙은 다음에 대한 인터페이스를 제공하여 IT 그룹 및 웹 개발자와의 상호 작용을 단순화하는 데 도움이 됩니다.

* 제품 개요 페이지의 이벤트 설정
* 쿼리 문자열 매개변수로 캠페인 채우기
* 더 쉽게 보고할 수 있도록 prop에서 범주 및 페이지 이름 연결
* evar를 prop에 복사하여 경로 보기
* 철자가 틀린 사이트 섹션 정리
* 쿼리 문자열에서 eVar까지의 내부 검색어 또는 캠페인 ID 가져오기

>[!VIDEO](https://video.tv.adobe.com/v/26124/?quality=12&learn=on)

## 처리 규칙 권한 {#section_8A4846688050453784DAE4D89355169A}

관리자는 **기본적으로** 처리 규칙을 사용할 수 있는 권한이 있습니다. 관리자는 관리 도구 인터페이스를 통해 관리자가 아닌 사용자에게 이러한 권한을 부여할 수도 있습니다. 자세한 내용은 다음을 참조하십시오. []

![처리 규칙](assets/processing-rules.png)

## 컨텍스트 데이터를 사용하여 데이터 수집 단순화 {#section_09EEA03612D24C15839631AA9E9668D8}

컨텍스트 데이터 변수는 처리 규칙에만 사용할 수 있는 변수 유형입니다. 컨텍스트 데이터 변수를 사용하기 위해, 키/값 데이터 쌍이 구현에 의해 전송되며, 처리 규칙을 사용하여 표준 Analytics 변수에서 이러한 변수를 캡처합니다. 이를 통해 프로그래머가 어떤 prop 및/또는 eVar가 어떤 값을 포함해야 하는지 정확하게 이해할 필요가 없습니다.

```js
s.contextData['author'] = "Robert Munch";
s.contextData['section'] = "Books";
s.contextData['genre'] = "Youth";
```

코드에 설정되면 처리 규칙을 설정하여 변수에 값을 할당할 수 있습니다. 예:

1. `author`를 `eVar2`에 매핑
2. `section`을 `prop1` 및 `eVar3`에 매핑
3. `author` 및 `section`이 있는 경우 `event5` 설정

자세한 정보는 구현 사용 안내서에서 [contextData](/help/implement/vars/page-vars/contextdata.md)를 참조하십시오.

## 처리 규칙을 사용하여 데이터 히트 및 이벤트 트리거 변환 {#section_8284E72E999244E091CD7FB1A22342B6}

처리 규칙은 들어오는 값을 모니터링하여 일반적인 오타를 변형하고 보고된 데이터를 기준으로 이벤트를 설정할 수 있습니다. Prop을 eVar에 복사하고, 보고서에 값을 연결하며, 이벤트를 설정할 수 있습니다.

## 보고에 컨텍스트 데이터 변수 사용 {#section_BD098BC503024A0B8703596628071134}

컨텍스트 데이터 변수가 구현 내에 정의된 경우 해당 변수를 eVar와 같은 변수에 복사해야 보고에 사용할 수 있습니다.

자세한 내용은 [eVar에 컨텍스트 데이터 변수를 복사](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md) 및 [컨텍스트 데이터 변수를 사용하여 이벤트 설정](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data-event.md)을 참조하십시오.

## 알려진 제한 사항

**처리 규칙에서 캐럿(^) 사용.**&#x200B;처리 규칙에서 구분 기호로 또는 다른 목적으로 캐럿을 사용하려는 경우 각 단일 캐럿은 2캐럿으로 표시되어야 합니다. 예를 들어 단일 캐럿은 ^^, 중복 캐럿은 ^^^^ 등으로 표시합니다.