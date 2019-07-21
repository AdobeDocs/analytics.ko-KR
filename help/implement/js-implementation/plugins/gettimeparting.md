---
description: getTimeParting 플러그인은 사용자 지정 변수를 시간, 요일, 주말 및 평일 값으로 사용자 지정 변수에 채웁니다. Analysis Workspace는 기본 시간 나누기 차원을 제공합니다. 이 플러그인은 Analysis Workspace 외부의 다른 Analytics 솔루션에서 시간 나누기 차원이 필요한 경우 사용해야 합니다.
keywords: Analytics 구현
seo-description: getTimeParting 플러그인은 사용자 지정 변수를 시간, 요일, 주말 및 평일 값으로 사용자 지정 변수에 채웁니다. Analysis Workspace는 기본 시간 나누기 차원을 제공합니다. 이 플러그인은 Analysis Workspace 외부의 다른 Analytics 솔루션에서 시간 나누기 차원이 필요한 경우 사용해야 합니다.
seo-title: getTimeParting
solution: Analytics
subtopic: 플러그인
title: getTimeParting
topic: 개발자 및 구현
uuid: 74 F 696 A 3-7169-4560-89 B 2-478 B 3 D 8385 E 1
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# getTimeParting

getTimeParting 플러그인은 사용자 지정 변수를 시간, 요일, 주말 및 평일 값으로 사용자 지정 변수에 채웁니다. Analysis Workspace는 기본 시간 나누기 차원을 제공합니다. The plug-in should be used if time parting dimensions are needed in other Analytics solutions, outside of [!UICONTROL Analysis Workspace].

이 플러그인은 사용자의 웹 브라우저에서 사용할 수 있는 날짜 및 시간 정보를 캡처합니다. 그리고 이 정보에서 시간과 요일을 가져옵니다. 그리고 이 데이터를 선택한 시간대로 변환합니다. 일광 절약 시간도 고려합니다.

>[!NOTE]
>
>다음 지침을 따르면 사이트에서 데이터 수집 코드를 수정해야 합니다. 이 작업은 사이트의 데이터 수집에 영향을 줄 수 있으며 [!DNL Analytics] 사용 및 구현 경험이 풍부한 개발자가 수행해야만 합니다.

## 플러그인 코드 {#section_1390D6FA53BE4C40B748B0C0AE09C4FA}

**구성 섹션**

[!DNL s_code.js] 파일에서 [!UICONTROL CONFIG SECTION] 레이블이 지정된 영역에 다음 코드를 넣고 아래 설명에 따라 필요한 사항을 업데이트합니다.

`s._tpDST` - DST 값의 배열. The array is structured in the following format: `YYYY:'MM/DD,MM/DD'`

```js
//time parting configuration 
//Australia 
s._tpDST = { 
2012:'4/1,10/7', 
2013:'4/7,10/6', 
2014:'4/6,10/5', 
2015:'4/5,10/4', 
2016:'4/3,10/2', 
2017:'4/2,10/1', 
2018:'4/1,10/7', 
2019:'4/7,10/6'} 
  
//US 
s._tpDST = { 
2012:'3/11,11/4', 
2013:'3/10,11/3', 
2014:'3/9,11/2', 
2015:'3/8,11/1', 
2016:'3/13,11/6', 
2017:'3/12,11/5', 
2018:'3/11,11/4', 
2019:'3/10,11/3'} 
  
//Europe 
s._tpDST = { 
2012:'3/25,10/28', 
2013:'3/31,10/27', 
2014:'3/30,10/26', 
2015:'3/29,10/25', 
2016:'3/27,10/30', 
2017:'3/26,10/29', 
2018:'3/25,10/28', 
2019:'3/31,10/27'}
```

북반구 클라이언트용 참고: 이 배열에서 DST 값은 DST 시작, DST 종료입니다.

남반구 클라이언트용 참고: 이 배열에서 DST 값은 DST 종료, DST 시작입니다.

**매개 변수**

```js
var tp = s.getTimeParting(h,z);
```

* h = (필수) 반구 - 시간을 어느 반구로 전환할지를 지정합니다. 값은 'n' 또는 's'입니다. 전달된 DST 배열을 사용하는 방법을 결정하는 데 사용됩니다. 'n'이 전달되면 플러그인에서는 DST가 설정된 날짜를 사용합니다. 's'가 전달되면 플러그인에서는 DST가 해제된 날짜를 사용합니다.
* z = (선택 사항) 표준 시간대 - 데이터가 특정 기간을 기반으로 하도록 하려면, 여기에서 GMT와는 다른 시간으로 지정해야 합니다. 비 DST 동안에는 GMT여야 합니다. 값을 지정하지 않으면 GMT가 기본값으로 설정됩니다(즉, 미국 동부 표준시의 경우 '-5').

**반환**

분 수준의 연속 값과 요일을 반환합니다. 예:

```
8:03 AM|Monday
```

[분류](https://marketing.adobe.com/resources/help/en_US/reference/classifications.html)를 사용하여 방문을 기간으로 그룹화할 수 있습니다. 예를 들어, 분류 규칙 빌더의 규칙을 설정하여 오전 9:00 ~ 오전 9:59 범위의 방문을 "오전 9:00 - 오전 10:00"으로 그룹화할 수 있습니다. 분류의 대체 방법으로 JavaScript에서 방문을 분류하는 추가적인 클라이언트 측 논리를 제공할 수 있습니다.

**호출 예**

```js
var tp = s.getTimeParting('n','-7'); 
s.prop1 = tp;
```

**플러그인 섹션**

다음 코드를 [!UICONTROL  파일의 ]PLUGINS SECTION[!DNL s_code.js]에 추가합니다.

```js
/* 
 * Plugin: getTimeParting 3.4 
 */ 
s.getTimeParting=new Function("h","z","" 
+"var s=this,od;od=new Date('1/1/2000');if(od.getDay()!=6||od.getMont" 
+"h()!=0){return'Data Not Available';}else{var H,M,D,U,ds,de,tm,da=['" 
+"Sunday','Monday','Tuesday','Wednesday','Thursday','Friday','Saturda" 
+"y'],d=new Date();z=z?z:0;z=parseFloat(z);if(s._tpDST){var dso=s._tp" 
+"DST[d.getFullYear()].split(/,/);ds=new Date(dso[0]+'/'+d.getFullYea" 
+"r());de=new Date(dso[1]+'/'+d.getFullYear());if(h=='n'&&d>ds&&d<de)" 
+"{z=z+1;}else if(h=='s'&&(d>de||d<ds)){z=z+1;}}d=d.getTime()+(d.getT" 
+"imezoneOffset()*60000);d=new Date(d+(3600000*z));H=d.getHours();M=d" 
+".getMinutes();M=(M<10)?'0'+M:M;D=d.getDay();U=' AM';if(H>=12){U=' P" 
+"M';H=H-12;}if(H==0){H=12;}D=da[D];tm=H+':'+M+U;return(tm+'|'+D);}");
```

**참고**

* 프로덕션 배포 전에 항상 플러그인 설치를 테스트하여 데이터 수집이 예상대로 수행되는지 확인하십시오.
* 플러그인이 올바르게 작동하려면 구성 변수가 설정되어 있어야 합니다.

