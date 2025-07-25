---
title: contextData
description: 컨텍스트 데이터 변수를 사용하면 처리 규칙이 읽을 수 있는 각 페이지에서 사용자 정의 변수를 정의할 수 있습니다.
feature: Appmeasurement Implementation
exl-id: f2c747a9-1a03-4f9f-8025-9f4745403a81
role: Admin, Developer
source-git-commit: c2adf6d2e328378332cc290ba2dfd75ee6587ef6
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 68%

---

# contextData

컨텍스트 데이터 변수를 사용하면 처리 규칙이 읽을 수 있는 각 페이지에서 사용자 정의 변수를 정의할 수 있습니다. 코드에서 값을 Analytics 변수에 명시적으로 할당하는 대신 컨텍스트 데이터 변수에 데이터를 보낼 수 있습니다. 그러면 처리 규칙이 컨텍스트 데이터 변수 값을 가져와 각 Analytics 변수에 전달합니다. 관리자 사용 안내서의 [처리 규칙](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/processing-rules/pr-overview.md)을 참조하십시오.

컨텍스트 데이터 변수는 개발 팀이 번호가 매겨진 변수 대신 명명된 요소의 데이터를 수집하는 데 유용합니다. 예를 들어 개발 팀에게 페이지의 작성자를 `eVar10`에 할당하도록 요청하는 대신 `s.contextData["author"]`에 할당하도록 요청할 수 있습니다. 그런 다음 조직의 Analytics 관리자는 처리 규칙을 만들어 컨텍스트 데이터 변수를 보고를 위한 분석 변수에 매핑할 수 있습니다. 개발 팀은 궁극적으로 Adobe이 제공하는 많은 페이지 변수 대신 컨텍스트 데이터 변수만 걱정하게 됩니다.

## Web SDK를 사용한 컨텍스트 데이터 변수

[**XDM 개체**](/help/implement/aep-edge/xdm-var-mapping.md)&#x200B;를 사용하는 경우 Adobe Analytics 변수에 매핑되지 않은 모든 필드가 자동으로 컨텍스트 데이터 변수로 포함됩니다. XDM 개체를 사용하여 컨텍스트 데이터를 명시적으로 설정할 수도 있습니다. 그런 다음 [처리 규칙](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/processing-rules/pr-overview.md)을 사용하여 컨텍스트 데이터 변수를 원하는 Analytics 변수에 할당할 수 있습니다.  자세한 내용은 [Analytics 변수에 다른 XDM 필드 매핑](../../aep-edge/xdm-var-mapping.md#mapping-other-xdm-fields-to-analytics-variables)을 참조하십시오.

[**데이터 개체**](/help/implement/aep-edge/data-var-mapping.md)&#x200B;를 사용하는 경우 모든 컨텍스트 데이터 변수는 `data.__adobe.analytics.contextData` 내에 키-값 쌍으로 있습니다.

```js
alloy("sendEvent", {
  "data": {
    "__adobe": {
      "analytics": {
        "contextData": {
          "example_variable": "Example value",
          "second_example": "Another value"
        }
      }
    }
  }
});
```

[처리 규칙](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/processing-rules/pr-overview.md) 인터페이스는 적용 가능한 드롭다운 메뉴에 `example_variable` 및 `second_example`을(를) 표시합니다.

## Adobe Analytics 확장을 사용한 컨텍스트 데이터 변수

Adobe Experience Platform 데이터 수집에는 컨텍스트 데이터 변수를 설정하는 전용 필드가 없습니다. AppMeasurement 구문 다음에 나오는 사용자 정의 코드 편집기를 사용하십시오.

## AppMeasurement 및 Analytics 확장 사용자 정의 코드 편집기의 s.contextData

`s.contextData` 변수는 값을 바로 사용하지 않습니다. 대신 이 변수의 속성을 문자열로 설정합니다.

```js
// Assign the example_variable property a value
s.contextData["example_variable"] = "Example value";
```

* 유효한 컨텍스트 데이터 변수에는 영숫자, 밑줄 및 마침표만 포함됩니다. Adobe는 하이픈과 같은 다른 문자를 포함하는 경우 처리 규칙을 통한 데이터 수집을 보장하지 않습니다.
* 컨텍스트 데이터 변수를 `"a."`으로 시작하지 마십시오. 이 접두사는 Adobe에 의해 예약되어 사용 중입니다. 예를 들어 `s.contextData["a.InstallEvent"]`를 사용하지 마십시오.
* 컨텍스트 데이터 변수는 대/소문자를 구분하지 않습니다. 변수 `s.contextData["example"]`과 `s.contextData["EXAMPLE"]`은 동일합니다.
* 단일 키에는 두 개 이상의 값을 포함할 수 없습니다. 다중 값 변수에 컨텍스트 데이터 변수를 사용하려면 구분 기호(일반적으로 쉼표)를 사용하여 모든 값을 연결하고, 처리 규칙을 사용하여 [목록 prop](prop.md#list-props) 또는 [목록 변수](list.md)에 전달하십시오.

## 처리 규칙을 사용하여 분석 변수 채우기

>[!WARNING]
>
>컨텍스트 데이터 변수는 처리 규칙 실행 후 무시됩니다. 값을 변수에 배치하는 처리 규칙이 활성화되어 있지 않으면 해당 데이터가 영구적으로 손실됩니다.

1. 구현을 업데이트하여 컨텍스트 데이터 변수 이름 및 값을 설정합니다.
2. Adobe Analytics에 로그인하고 **[!UICONTROL 관리자]** > **[!UICONTROL 보고서]** 모음으로 이동합니다.
3. 원하는 보고서 세트를 선택한 다음 **[!UICONTROL 설정 편집]** > **[!UICONTROL 일반]** > **[!UICONTROL 처리 규칙]**&#x200B;으로 이동합니다.
4. Analytics 변수를 컨텍스트 데이터 변수 값으로 설정하는 처리 규칙을 만듭니다.
5. 변경 사항을 저장합니다.

처리 규칙은 저장 후 즉시 적용됩니다. 이전 데이터에는 적용되지 않습니다.

## 링크 추적 호출에서 컨텍스트 데이터 보내기

컨텍스트 데이터 변수를 [`s.linkTrackVars`](../config-vars/linktrackvars.md)의 다음 `contextData` 속성으로 포함하십시오.

```js
s.contextData["example_variable"] = "Example value";
s.linkTrackVars = "contextData.example_variable";
s.tl(true,"o","Example context data link");
```

## 컨텍스트 데이터 변수를 사용하여 이벤트 증가

처리 규칙을 만들 때 컨텍스트 데이터 변수를 이벤트에 지정할 수 있습니다.

* 컨텍스트 데이터 변수에 텍스트가 포함되어 있으면 이벤트가 하나씩 증가합니다.
* 컨텍스트 데이터 변수에 정수가 들어 있으면 이벤트가 해당 정수 단위로 증가합니다.

```js
// Assigning this context data variable to an event increments it by one
s.contextData["example_text"] = "Text value";

// Assigning this context data variable to an event increments it by four
s.contextData["example_number"] = "4";
```
