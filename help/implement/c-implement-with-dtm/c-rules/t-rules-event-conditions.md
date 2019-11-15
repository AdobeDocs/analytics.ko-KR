---
description: 조건은 언제 이벤트 기반 규칙이 트리거되는지 결정합니다.
keywords: Dynamic Tag Management;rule;create rule;new rule;event-based rule;delay link activation;apply event handler directly to element;bubbling;event bubbling
solution: Experience Cloud,Analytics,Target,Dynamic Tag Management
title: 이벤트 기반 규칙 조건 만들기
uuid: a847391c-5aec-4d64-8a35-388587731598
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 이벤트 기반 규칙 조건 만들기

조건은 언제 이벤트 기반 규칙이 트리거되는지 결정합니다.

1. 마우스 클릭이나 양식 제출과 같이 추적할 상호 작용 유형을 선택합니다.

   ![](assets/condition-event-based.png)

   자세한 내용은 Adobe Tag Management 제품 설명서에서 [이벤트 유형](https://marketing.adobe.com/resources/help/en_US/dtm/event_types.html)을 참조하십시오.

1. 다음 옵션을 필요에 따라 활성화합니다.

   | 요소 | 설명 |
   |--- |--- |
   | 링크 활성화 지연 | 이벤트가 링크를 활성화하고, 이벤트를 실행할 시간이 되기 전까지 링크가 지연되기를 원할 경우 비활성화합니다. |
   | 이벤트 핸들러를 요소에 바로 적용 | 타깃팅된 특정 요소에 이벤트 처리기를 적용합니다. 이 설정은 브라우저의 버블링 및 계층화 개념과 연결되어 있습니다. |

   예를 들어 `<a href="abc.html"><img src="xyz.png"/></a>`와 같은 앵커 태그의 내부에 있는 이미지를 클릭하면 태그가 버블 스트림에 있으므로 클릭이 앵커 태그와 연결되어 있을 것으로 예상할 수 있습니다. 하지만 개발자 도구에서 클릭을 검사하면 클릭은 실제로 `<img>` 태그에만 영향을 줄 수 있습니다. 이벤트가 올바로 처리되도록 하려면 클릭을 `<img>` 태그와 연결하되, 브라우저에서 클릭이 상위 요소로 버블링되도록 하지 마십시오. 클릭과 같은 이벤트는 잠재적으로 `<body>`까지 버블링될 수 있습니다. 이벤트가 실제로 연결되는 위치를 이해하고, 규칙이 올바로 실행되도록 명확하게 타깃팅하는 것은 중요합니다.

   *버블링*&#x200B;은 이벤트가 캡처되어 가장 안쪽의 요소에 의해 처리된 후 외부 요소로 전파됨을 의미합니다.

1. 추적할 태그의 이름과 태그에 있는 일치시킬 추가적인 속성을 가리킵니다.

   ![](assets/condition-event-based2.png)

   올바른 요소 태그 찾기에 대한 자세한 내용은 다이내믹 태그 관리 제품 설명서에서 [CSS 선택기 사용](https://marketing.adobe.com/resources/help/en_US/dtm/css-selector.html)을 참조하십시오.

1. 규칙에 연결할 추가적인 기준이나 조건 유형을 선택하여 설정합니다.

   ![](assets/condition-event-based3.png)

1. 이벤트 버블링에 대한 기본 설정을 가리킵니다.

   이벤트 버블링은 HTML DOM에서 이벤트 전파의 한 방식입니다.

   | 만약 ... | 다음 옵션을 확인하십시오 |
   |--- |--- |
   | 식별한 규칙 선택기의 하위 요소에 있는 관련 상호 작용이 규칙을 실행하도록 하려는 경우 | 하위 요소에 대한 이벤트의 버블링 허용에서 보냅니다. |
   | 하위 요소가 이미 자신의 이벤트를 트리거했다면 버블링이 되지 않도록 하려는 경우 | 이미 하위 요소에 의해 이벤트가 실행되는 경우 허용하지 않음 |
   | 식별한 규칙 선택기의 이벤트가 이벤트 계층 구조에서 요소 자체를 넘지 않도록 하려는 경우. | 이벤트가 상위까지 위쪽으로 버블링하는 것을 허용하지 않음. |
