---
description: Activity Map에서의 링크 추적에 대한 FAQ.
title: 링크 추적 FAQ
uuid: 10172073-b98b-4950-8397-67a18b37b3b4
feature: Activity Map
role: User, Admin
exl-id: b6ccdf91-98ce-413f-842d-c5423598ed49
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 59%

---

# 링크 추적 FAQ

Activity Map에서의 링크 추적에 대한 FAQ.

>[!CAUTION]
>
>Activity Map 추적을 켜면 **개인 식별 정보(PII) 데이터를 수집할 수 있습니다.** 이 데이터는 단독으로 사용하거나 다른 정보와 함께 사용하여 한 개인을 식별, 연락 또는 위치를 파악하거나, 혹은 컨텍스트에서 개인을 식별하는 데 쓰일 수 있습니다.

다음은 Activity Map 추적을 사용하여 PII 데이터를 수집할 수 있는 알려진 몇 가지 경우입니다.

* `Mailto` 링크. mailto 링크는 이메일을 보내기 위해 컴퓨터에서 기본 메일 클라이언트를 활성화하는 HTML 링크의 유형입니다.
* `User ID`. 사용자가 로그인한 후 웹 사이트의 머리글/바닥글에 표시될 수 있는 링크입니다.
* 금융 기관의 경우 계정 번호가 링크로 표시될 수 있습니다. 클릭하면 링크의 텍스트가 수집됩니다.
* Healthcare 웹 사이트에는 링크로 표시된 PII 데이터가 있을 수 있습니다. 이러한 링크를 클릭하면 링크의 텍스트를 수집하므로 PII 데이터가 수집됩니다.

## 언제 링크 추적이 발생합니까?

Activity Map 링크 및 영역 식별은 사용자가 페이지를 클릭하면 수행됩니다.

## 기본적으로 추적되는 항목은 무엇입니까?

요소에서 클릭 이벤트가 발생하면, 요소는 확인 사항을 전달하여 AppMeasurement에서 이것이 링크로 처리하는지 여부를 판단해야 합니다. 확인 사항은 다음과 같습니다.

* `A` 또는 `AREA` 태그가 `href` 속성과 함께 있습니까?
* `s_objectID` 변수를 설정하는 `onclick` 특성이 있습니까?
* `INPUT` 태그 또는 `SUBMIT` 단추이며 값 또는 하위 텍스트가 있습니까?
* `IMAGE` 유형과 `src` 속성을 포함하는 `INPUT` 태그입니까?
* `BUTTON`입니까?

위의 질문 중 하나라도 답이 예이면, 요소가 링크로 처리되고 추적됩니다.

>[!IMPORTANT]
>
>속성 유형이 &quot;button&quot;인 단추 태그는 AppMeasurement에서 링크로 간주되지 않습니다. 단추 태그에서 type=&quot;button&quot;을 제거하고 role=&quot;button&quot; 또는 submit=&quot;button&quot;을 대신 추가합니다.

>[!IMPORTANT]
>
>&quot;#&quot;로 시작하는 &quot;href&quot;가 있는 앵커 태그는 링크가 아닌 AppMeasurement의 내부 대상 위치로 간주됩니다(페이지를 나가지 않기 때문에). 기본적으로 Activity Map은 이러한 내부 대상 위치를 추적하지 않습니다. 사용자를 새 페이지로 이동하는 링크만 추적합니다.

## Activity Map은 어떻게 다른 시각적 HTML 요소를 추적합니까?

a. `s.tl()` 함수를 통해

`s.tl()` 호출을 통해 클릭이 발생한 경우 Activity Map은 이 클릭 이벤트도 수신하고 `linkName` 문자열 변수가 발견되었는지 확인합니다. `s.tl()` 실행 중에 해당 linkName이 Activity Map 링크 ID로 설정됩니다. `s.tl()` 호출을 시작한 클릭한 요소는 영역을 결정하는 데 사용됩니다. 예:

```
<img onclick="s.tl(true,'o','abc')" src="someimageurl.png"/>
```

나. `s_objectID` 변수를 통해 액세스합니다. 예:

    &quot;
    
    &lt;a>&lt;img>&lt;/a>
    
    &lt;a>여기에 텍스트 연결&lt;/a>
    
    
    &quot;

>[!IMPORTANT]
>
>Activity Map에서 `s_objectID`을 사용할 때는 후행 세미콜론(;)이 필요합니다.

## 추적되는 링크의 예를 제공할 수 있습니까?

### 예제 1

```
  <a hef="/home?lang=en>Home</a>
```

### 예제 2

```
 <input type="submit" value="Submit"/>
```

### 예제 3

```
  <input type="image" src="submit-button.png"/>
```

### 예제 4

```
    <p onclick="var s_objectID='custom link id';">
      <span class="title">Current Market Rates</span>
      <span class="subtitle">1.45USD</span>
    </p>
```

### 예제 5

```
    <div onclick="s.tl(true,'o','custom link id')">
      <span class="title">Current Market Rates</span>
      <span class="subtitle">1.45USD</span>
    </div>
```

## 추적되지 않는 링크의 예를 제공할 수 있습니까?

1. 이유: 앵커 태그에 올바른 `href`이 없습니다.
   `<a name="innerAnchor">Section header</a>`

1. 이유: `s_ObjectID` 및 `s.tl()` 모두 없습니다.

   ```
   <p onclick="showPanel('market rates')">
     <span class="title">Current Market Rates</span>
     <span class="subtitle">1.45USD</span>
   </p>
   ```

1. 이유: `s_ObjectID` 및 `s.tl()` 모두 없습니다.

   ``` 
   <input type="radio" onclick="changeState(this)" name="group1" value="A"/>
   <input type="radio" onclick="changeState(this)" name="group1" value="B"/>
   <input type="radio" onclick="changeState(this)" name="group1" value="C"/>
   
   ```  
   
1. 이유: &quot;src&quot; 속성에 양식 입력 요소가 없습니다.

   `<input type="image"/>`
