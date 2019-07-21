---
description: 컨텍스트 데이터 변수를 사용하여 처리 규칙으로 읽을 수 있는 각 페이지에서 사용자 지정 변수를 정의할 수 있습니다.
keywords: Analytics 구현; Contextdata; s. contextdata
seo-description: 컨텍스트 데이터 변수를 사용하여 처리 규칙으로 읽을 수 있는 각 페이지에서 사용자 지정 변수를 정의할 수 있습니다.
seo-title: 컨텍스트 데이터 변수
solution: Analytics
subtopic: 변수
title: 컨텍스트 데이터 변수
topic: 개발자 및 구현
uuid: 4 B 215803-99 D 4-46 F 2-B 3 C 1-E 78558987764
translation-type: tm+mt
source-git-commit: 01a6fc7e44dc71b868bd38a4f6a5a4089eae6349

---


# 컨텍스트 데이터 변수

컨텍스트 데이터 변수를 사용하여 처리 규칙으로 읽을 수 있는 각 페이지에서 사용자 지정 변수를 정의할 수 있습니다.

코드에서 값을 prop 및 eVar에 명시적으로 할당하는 대신 처리 규칙을 사용하여 매핑되는 컨텍스트 데이터 변수에 데이터를 전송할 수 있습니다. 처리 규칙은 데이터를 수신할 때 데이터를 변경하는 강력한 그래픽 인터페이스를 제공합니다. 컨텍스트 데이터에서 전송된 값을 기반으로 하여 이벤트를 설정하고 eVars 및 props에 값을 복사하고 추가 조건문을 실행할 수 있습니다.

>[!NOTE]
>
>컨텍스트 데이터 변수는 대/소문자를 구분하지 않습니다. 예를 들어 다음 2 개의 변수는 사실상 동일합니다. &gt;
>```>
>s.contextData['article_title'] = 'Weekend Concert Controversy'; 
>
>
```>
>and 
>
>
```>
>s.contextData['ARTICLE_TITLE'] = 'Weekend Concert Controversy';
>```>



컨텍스트 데이터를 사용하면 다른 보고서 세트 구성을 지원하기 위해 코드를 업데이트하는 것이 방지됩니다.

예를 들어 *`s.contextData`* 변수:

```
s.contextData['myco.rsid'] = 'value'
```

처리 규칙을 사용하여 `myco.rsid` 컨텍스트 데이터 변수를 확인하는 조건을 추가할 수 있습니다. 이 변수가 발견되면 작업을 추가하여 prop 또는 eVar에 복사할 수 있습니다.

또한 처리 규칙 인터페이스에서 직접 컨텍스트 데이터 변수를 정의하여 임시로 값을 저장하거나, 보고서 세트에 사용될 컨텍스트 데이터 변수의 값을 수집할 수 있습니다. 예를 들어 두 값을 교환해야 하는 경우 컨텍스트 데이터 변수를 만들어 교환 중에 값을 저장할 수 있습니다.

처리 규칙은 데이터가 수집될 때만 적용되므로, 컨텍스트 데이터 전송을 시작하기 전에 처리 규칙을 설정하는 것이 중요합니다. 히트가 처리될 때 처리 규칙으로 읽히지 않는 컨텍스트 데이터 값은 무시됩니다.

## 규칙 {#section_2229739F6B1A4C1CAD7140BDF4687523}

<table id="table_4433A32A952340699B189CAEAF158B06"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>규칙 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>지원되는 이름 및 문자 </p> </td> 
   <td colname="col2"> <p>컨텍스트 데이터 변수 이름은 영숫자, 밑줄 및 점만 포함할 수 있습니다. 모든 추가적인 문자는 삭제됩니다. 컨텍스트 데이터 변수에는 숫자 지정이 없고, 오히려 이름이 지정됩니다. </p> <p>예를 들어 컨텍스트 데이터 변수 <code>login_page-home</code>은 자동으로 <code>login_pagehome</code>이 됩니다 . <code>login_page-home</code> 변수로 전송된 모든 데이터는 <code>login_pagehome</code>에 할당됩니다 . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>네임스페이스 </p> </td> 
   <td colname="col2"> <p>회사 이름, 사이트 이름 또는 유사한 값을 변수 앞에 붙여 보고서 세트에서 이름이 고유하게 하는 것이 좋습니다. </p> <p>컨텍스트 데이터 변수는 기타 JavaScript 변수와 유사한 이름으로 지정될 수 있습니다. 네임스페이스 <code>a.*</code>는 컨텍스트 변수 이름에서 Adobe 제품이 사용하도록 예약되어 있음을 알아두십시오. 예를 들어 iOS용 AppMeasurement 라이브러리는 <code>a.InstallEvent</code>를 사용하여 애플리케이션 설치를 측정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Internet Explorer의 URL 제한 </p> </td> 
   <td colname="col2"> <p>Internet Explorer 6 및 7의 경우 URL이 2000바이트에서 잘리는 오래된 URL 제한이 있을 수 있습니다. <span class="keyword">DigitalPulse</span> Debugger를 사용하여 URL 문자열 크기를 결정할 수 있습니다. </p> <p>AppMeasurement(2014년 9월)의 최신 업데이트가 있으면 Internet Explorer 8+에 HTTP POST가 사용되어 URL이 잘리는 문제가 해결됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>지원되는 AppMeasurement 버전 </p> </td> 
   <td colname="col2"> <p>컨텍스트 데이터 변수는 적어도 H23 코드 이상을 필요로 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Track Link Call에서 컨텍스트 데이터 전송 {#section_35EBE5D1CF29427598BD4B2165CE64FC}

`ContextData`에 포함할 `s.linkTrackVars` + 변수 이름 입력:

```
s.contextData['myco.value'] = "some value"; 
s.linkTrackVars = "contextData.myco.value"; 
s.tl(true,"o","Link Name"); 
```

## 예 {#section_A16AD9E6E0E84F6A85CA4F08512480B3}

Possible ways to replace implementation of the *`s.pageName`* variable, assuming that processing rules are set up correctly for each:

```
s.contextData['page'] = "Home Page" 
s.contextData['pagename'] = document.title // Takes the web page's title and passes it into the pageName context data variable 
s.contextData['pagevar'] = s.pageName // This example would be considered redundant, as both the pageName and contextData variable are available in Processing rules
```

컨텍스트 데이터 변수를 구현하는 다른 예:

```
s.contextData['owner'] = "Jesse" 
s.contextData['campaign'] = "Campaign A" 
s.contextData['author'] = "Sheridan Andrius"
```

예가 필요하면, Analytics 참조에서 [컨텍스트 데이터 변수를 eVar에 복사](https://marketing.adobe.com/resources/help/en_US/reference/?f=processing_rules_copy_context_data)를 참조하십시오.
