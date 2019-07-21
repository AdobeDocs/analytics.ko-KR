---
description: 사용자가 사이트에 마지막으로 방문한 후로 지난 일 수를 결정하고 이 정보를 Analytics 변수로 캡처합니다.
keywords: Analytics 구현
seo-description: 사용자가 사이트에 마지막으로 방문한 후로 지난 일 수를 결정하고 이 정보를 Analytics 변수로 캡처합니다.
seo-title: getDaysSinceLastVisit
solution: Analytics
subtopic: 플러그인
title: getDaysSinceLastVisit
topic: 개발자 및 구현
uuid: cad 95882-3 bd 0-4 f 94-a 0 c 3-4 e 7 b 6058 d 246
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# getDaysSinceLastVisit

사용자가 사이트에 마지막으로 방문한 후로 지난 일 수를 결정하고 이 정보를 Analytics 변수로 캡처합니다.

>[!IMPORTANT]
>
>[이제 분석 작업 공간에](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/) 마지막 **[!UICONTROL 방문]** 차원 이후의 일 수가 포함되어 있어 이 플러그인의 필요성을 무효화합니다.

이 재방문 주기 데이터를 사용하여 다음과 같은 질문에 대답할 수 있습니다.

* 사용자가 내 사이트를 얼마나 자주 다시 방문합니까?
* 재방문 주기와 전환 사이에는 어떤 상관 관계가 있습니까? 반복 구매자들은 자주 방문하는 편입니까 가끔 방문하는 편입니까?
* 캠페인 클릭스루로 방문한 사용자는 자주 돌아옵니까?

플러그인이 세그먼테이션에 사용된 값을 생성할 수도 있습니다. 예를 들어, 세그먼트를 생성한 후 30일 이상 방문하지 않고 있던 사용자의 방문에 대한 데이터만 모두 볼 수도 있습니다.

>[!NOTE]
>
>다음 지침을 따르면 사이트에서 데이터 수집 코드를 수정해야 합니다. 이 작업은 사이트의 데이터 수집에 영향을 줄 수 있으며 [!DNL Analytics] 사용 및 구현 경험이 풍부한 개발자가 수행해야만 합니다.

## 플러그인 코드 및 구현 {#section_5600DBB819F143D59527A73BD94418DE}

**CONFIG SECTION**

변경은 필요 없습니다.

**플러그인 구성**

Place the following code within the `s_doPlugins()` function, which is located in the area of the [!DNL s_code.js] file labeled *Plugin Config*. 재방문 주기 데이터를 캡처하는 데 사용할 사용자 지정 트래픽(s.prop) 변수 및/또는 사용자 지정 전환(s.eVar) 변수 하나를 선택합니다. 관리 콘솔을 사용하여 활성화했지만 현재 다른 목적으로 사용하고 있지는 않은 변수를 선택해야 합니다. 다음은 한 가지 예입니다. 필요에 따라 적절하게 업데이트하십시오.

```js
s.prop1=s.getDaysSinceLastVisit(Cookie_Name);
```

**PLUGINS SECTION**
[!DNL s_code.js] 파일에서 *PLUGINS SECTION* 레이블이 표시된 영역에 다음 코드를 추가합니다. 플러그인 코드의 이 부분은 어떤 방식으로도 변경하지 마십시오.

```js
/* 
 * Plugin: Days since last Visit 1.1 - capture time from last visit 
 */ 
s.getDaysSinceLastVisit=new Function("c","" 
+"var s=this,e=new Date(),es=new Date(),cval,cval_s,cval_ss,ct=e.getT" 
+"ime(),day=24*60*60*1000,f1,f2,f3,f4,f5;e.setTime(ct+3*365*day);es.s" 
+"etTime(ct+30*60*1000);f0='Cookies Not Supported';f1='First Visit';f" 
+"2='More than 30 days';f3='More than 7 days';f4='Less than 7 days';f" 
+"5='Less than 1 day';cval=s.c_r(c);if(cval.length==0){s.c_w(c,ct,e);" 
+"s.c_w(c+'_s',f1,es);}else{var d=ct-cval;if(d>30*60*1000){if(d>30*da" 
+"y){s.c_w(c,ct,e);s.c_w(c+'_s',f2,es);}else if(d<30*day+1 && d>7*day" 
+"){s.c_w(c,ct,e);s.c_w(c+'_s',f3,es);}else if(d<7*day+1 && d>day){s." 
+"c_w(c,ct,e);s.c_w(c+'_s',f4,es);}else if(d<day+1){s.c_w(c,ct,e);s.c" 
+"_w(c+'_s',f5,es);}}else{s.c_w(c,ct,e);cval_ss=s.c_r(c+'_s');s.c_w(c" 
+"+'_s',cval_ss,es);}}cval_s=s.c_r(c+'_s');if(cval_s.length==0) retur" 
+"n f0;else if(cval_s!=f1&&cval_s!=f2&&cval_s!=f3&&cval_s!=f4&&cval_s" 
+"!=f5) return '';else return cval_s;");
```

**참고**

* 프로덕션 환경에 플러그인을 배포하기 전에 항상 플러그인 설치를 종합적으로 테스트하여 데이터 수집이 예상대로 수행되는지 확인하십시오.
* 플러그인은 재방문 주기를 다음 그룹으로 나누어 사용자를 분류합니다.

   * 처음 방문
   * 1일 미만
   * 7일 미만
   * 7일 초과
   * 30일 초과

* 이 플러그인은 쿠키를 사용하여 이전에 방문했던 사용자에게 플래그를 지정합니다. 브라우저에서 쿠키를 허용하지 않는 경우는 플러그인에서 *쿠키가 지원되지 않음* 값을 반환합니다.

