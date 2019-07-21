---
description: 성공적인 링크 추적 구현의 열쇠는 s.linkTrackVars 변수와 s.linkTrackEvents 변수를 이해하는 것입니다. 이 변수들을 이해하면 사용자 작업 시 사용자 지정 변수 값을 전달할 수 있습니다.
keywords: Analytics 구현
seo-description: 성공적인 링크 추적 구현의 열쇠는 s.linkTrackVars 변수와 s.linkTrackEvents 변수를 이해하는 것입니다. 이 변수들을 이해하면 사용자 작업 시 사용자 지정 변수 값을 전달할 수 있습니다.
seo-title: s.linkTrackVars 및 s.linkTrackEvents 사용
solution: Analytics
title: s.linkTrackVars 및 s.linkTrackEvents 사용
topic: 개발자 및 구현
uuid: F 6 B 7019 B -987 B -4 B 7 D-A 446-80205 F 7 CC 36 C
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# s.linkTrackVars 및 s.linkTrackEvents 사용

성공적인 링크 추적 구현의 열쇠는 s.linkTrackVars 변수와 s.linkTrackEvents 변수를 이해하는 것입니다. 이 변수들을 이해하면 사용자 작업 시 사용자 지정 변수 값을 전달할 수 있습니다.

사용자 지정 링크 추적을 구현하고 [!UICONTROL 사용자 지정] 변수 및 *`events`*&#x200B;에 액세스하려면 [!UICONTROL 변수를] 포함하여 전달되는 모든 변수의 쉼표로 구분된 목록이 s. linktrackvars 변수에 들어 *`events`* 있어야 합니다. [!UICONTROL s.linkTrackEvents]에 전달하는 모든 이벤트들이 쉼표로 구분되어 있는 목록이 포함되어 있는지도 확인하십시오.

[!UICONTROL s.linkTrackVars] 및 [!UICONTROL s.linkTrackEvents] 설정을 한다고 해서 이러한 변수/이벤트가 실제로 설정되지는 않습니다. 이러한 설정은 단지 [!DNL Analytics] 코드가 이러한 변수/이벤트를 설정하도록 준비시키는 것입니다. 아래 예에서 보듯이, 변수들은 여전히 수동으로 설정해야 합니다.

```js
<script language="javascript"> 
function customLinks () { 
 var s=s_gi('myreportsuite'); 
 s.linkTrackVars="prop1,eVar7,products,events"; 
 s.linkTrackEvents="event5,event9"; 
 s.prop1="Link Click"; 
 s.eVar7="my_page.html"; 
 s.events="event5"; 
 s.tl(true,'o','Custom Link Click'); 
} 
</script> 
<a href="my_page.html" onclick="customLinks();">My Page</a> 
```

[!UICONTROL s.linkTrackVars] 변수에 이벤트들이 나열되어 있는 것에 주목하십시오. 전달할 수 있는 개별 이벤트들은 [!UICONTROL s.linkTrackEvents] 변수에 포함되어 있으며, 함수에서 나중에 [!UICONTROL s.events] 내에도 포함됩니다. 전달된 각 변수는 함수에서 나중에 채워지기 전에 [!UICONTROL s.linkTrackVars]에 나열되어 있습니다. 또한 "event9″는 [!UICONTROL s.linkTrackEvents]에 포함되었으나, [!UICONTROL s.events]에는 포함되지 않았습니다. 기록되지 않지만, 사용자가 s.events="event5,event9"를 설정하도록 선택했다면 기록될 수도 있습니다.

자동 파일 다운로드 및 [!UICONTROL 종료] 링크 추적은 다르게 작동합니다. [!UICONTROL s.linkTrackVars] 및 [!UICONTROL s.linkTrackEvents]는 표준 [!DNL s_code.js] 파일에 포함되어 있으며, 둘 다 none으로 설정됩니다. 이 변수들은 자동 링크 추적이 [!DNL s_code.js]사용자 지정 링크 추적[!UICONTROL 과는 달리 글로벌 JavaScript 파일에서 설정하는 ]s.linkTrackVars[!UICONTROL  및 ]s.linkTrackEvents[!UICONTROL  값을 사용하도록 보통은 ] 파일에서 none으로 설정해 둡니다. 또한 파일 다운로드나 [!UICONTROL 종료] 링크가 기록될 때마다 해당 변수의 기존 값이 무엇이든 기존 값을 전달합니다.

페이지가 로드될 때 s.channel="Home"이고, [!DNL s_code.js] 파일에서 s.linkTrackVars="channel"인 예를 생각해 보십시오. 사용자가 클릭하여 파일을 다운로드하면, 자동 파일 다운로드 추적은 페이지 로드에서 설정된 [!DNL Analytics]s.channel[!UICONTROL 의 값을 포함하여 데이터를 ]로 전달합니다. 다시 "Home"이 전달되고, 이로 인해 [!UICONTROL 사이트 섹션] 보고서에서 이 값에 대한 페이지 보기 데이터가 부풀려집니다.

[!UICONTROL s.linkTrackVars] 및 [!UICONTROL s.linkTrackEvents]를 글로벌 JavaScript 파일에서 "none"으로 설정해 두고, [!UICONTROL 사용자 지정 링크 추적] 구현에 필요함에 따라 이 변수들을 명시적으로 설정해야 합니다.
