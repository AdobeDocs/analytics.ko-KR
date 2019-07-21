---
description: 방문자가 새로운 방문자인지 반복 방문자인지 결정하고 이 정보를 Analytics 변수에 캡처합니다.
keywords: Analytics 구현
seo-description: 방문자가 새로운 방문자인지 반복 방문자인지 결정하고 이 정보를 Analytics 변수에 캡처합니다.
seo-title: getNewRepeat
solution: Analytics
subtopic: 플러그인
title: getNewRepeat
topic: 개발자 및 구현
uuid: E 3 E 9 F 362-E 0 B 1-4 A 2 B-BB 5 B -98 EDDAA 0 A 7 F 4
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# getNewRepeat

방문자가 새로운 방문자인지 반복 방문자인지 결정하고 이 정보를 Analytics 변수에 캡처합니다.

이 플러그인을 사용하여 다음 질문에 대답할 수 있습니다.

* 방문자 중에서 반복 방문하지 않은 새 방문자의 비율은 어느 정도입니까?
* 다시 온 방문자가 새 방문자보다 인구 대비 높은 전환을 생성합니까? 비율은 어느 정도입니까?
* 마케팅 캠페인이 방문 간에 지속성을 유지합니까? 예를 들어, 내 캠페인을 클릭스루하여 온 사용자가 나중에 돌아옵니까?

>[!NOTE]
>
>다음 지침을 따르면 사이트에서 데이터 수집 코드를 수정해야 합니다. 이 작업은 사이트의 데이터 수집에 영향을 줄 수 있으며 [!DNL Analytics] 사용 및 구현 경험이 풍부한 개발자가 수행해야만 합니다.

## 플러그인 코드 및 구현 {#section_92E94A96A4764113B5588F1B83E3DE2C}

**CONFIG SECTION**: 이 섹션은 변경할 필요가 없습니다.

**플러그인 구성**

다음 코드를 *`s_doPlugins()`* 함수는 Plugin Config 라는 *`s_code.js`* 레이블의 영역에 *있습니다*. 지속되는 값 데이터를 캡처하는 데 사용할 사용자 지정 트래픽(s.prop) 변수 또는 사용자 지정 전환(s.eVar) 변수 하나를 선택합니다. 관리 콘솔을 사용하여 활성화했지만 현재 다른 목적으로 사용하고 있지는 않은 변수여야 합니다. 다음 예를 사용하여 요구 사항에 맞게 업데이트할 수 있습니다.

`s.prop1=s.getNewRepeat(30,'s_getNewRepeat');`

*`s.getNewRepeat`*&#x200B;에는 두 개의 선택 사항 인수가 있습니다.

1. 첫 번째 선택 사항 인수는 쿠키를 유지할 일 수입니다. 이 인수를 생략한 경우의 기본값은 30일입니다.
1. 두 번째 선택 사항 인수는 쿠키 이름입니다. 이 인수를 생략하면 기본값이 사용됩니다.

**PLUGINS SECTION**: [!DNL s_code.js] 파일에서 PLUGINS SECTION이라는 레이블이 지정된 영역에 다음 코드를 추가합니다. 플러그인 코드의 이 부분은 어떤 방식으로도 변경하지 마십시오.

```js
/* 
 * Plugin: getNewRepeat 1.2 - Returns whether user is new or repeat 
 */ 
s.getNewRepeat=new Function("d","cn","" 
+"var s=this,e=new Date(),cval,sval,ct=e.getTime();d=d?d:30;cn=cn?cn:" 
+"'s_nr';e.setTime(ct+d*24*60*60*1000);cval=s.c_r(cn);if(cval.length=" 
+"=0){s.c_w(cn,ct+'-New',e);return'New';}sval=s.split(cval,'-');if(ct" 
+"-sval[0]<30*60*1000&&sval[1]=='New'){s.c_w(cn,ct+'-New',e);return'N" 
+"ew';}else{s.c_w(cn,ct+'-Repeat',e);return'Repeat';}"); 
/* 
* Utility Function: split v1.5 (JS 1.0 compatible) 
*/ 
s.split=new Function("l","d","" 
+"var i,x=0,a=new Array;while(l){i=l.indexOf(d);i=i>-1?i:l.length;a[x" 
+"++]=l.substring(0,i);l=l.substring(i+d.length);}return a");
```

프로덕션 환경에 플러그인을 배포하기 전에 항상 플러그인 설치를 종합적으로 테스트하여 데이터 수집이 예상대로 수행되는지 확인하십시오.
