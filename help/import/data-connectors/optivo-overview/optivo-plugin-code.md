---
description: JavaScript 플러그인 데이터 수집 방법을 선택한 경우 다음 코드 행을 복사하여 페이지의 Adobe Analytics 코드에 추가합니다.
seo-description: JavaScript 플러그인 데이터 수집 방법을 선택한 경우 다음 코드 행을 복사하여 페이지의 Adobe Analytics 코드에 추가합니다.
seo-title: Adobe Analytics 플러그인 코드
title: Adobe Analytics 플러그인 코드
uuid: e9999be-1800-4d63-a4cb-df68a1b53d0d
translation-type: tm+mt
source-git-commit: a31f25e8a4681cf34525a7994b00580aa3aac15d

---


# Adobe Analytics 플러그인 코드{#adobe-analytics-plug-in-code}

JavaScript 플러그인 데이터 수집 방법을 선택한 경우 다음 코드 행을 복사하여 페이지의 Adobe Analytics 코드에 추가합니다.

```
/* 
 * Plugin: getQueryParam 2.3 
 */ 
s.getQueryParam=new Function("p","d","u","" 
+"var s=this,v='',i,t;d=d?d:'';u=u?u:(s.pageURL?s.pageURL:s.wd.locati" 
+"on);if(u=='f')u=s.gtfs().location;while(p){i=p.indexOf(',');i=i<0?p" 
+".length:i;t=s.p_gpv(p.substring(0,i),u+'');if(t){t=t.indexOf('#')>-" 
+"1?t.substring(0,t.indexOf('#')):t;}if(t)v+=v?d+t:t;p=p.substring(i=" 
+"=p.length?i:i+1)}return v"); 
s.p_gpv=new Function("k","u","" 
+"var s=this,v='',i=u.indexOf('?'),q;if(k&&i>-1){q=u.substring(i+1);v" 
+"=s.pt(q,'&','p_gvf',k)}return v"); 
s.p_gvf=new Function("t","k","" 
+"if(t){var s=this,i=t.indexOf('='),p=i<0?t:t.substring(0,i),v=i<0?'T" 
+"rue':t.substring(i+1);if(p.toLowerCase()==k.toLowerCase())return s." 
+"epa(v)}return ''"); 
 
/* 
 * in the s_doPlugins function 
 */ 
s.eVar8=s.getQueryParam("MID"); // Message ID as assigned by broadmail 
s.eVar9=s.getQueryParam("RID"); // Recipient ID as assigned by broadmail 
 
I am not sure, if that is useful and/or necessary, but I though the  
client may specify the Post Click values in the s_doPlugins function as  
well. Maybe it were useful to add some example definitions like the  
following to indicate the use of these variables. 
 
/* 
 * Optional custom settings of the Post Click data that is transferred to optivo broadmail. 
 * Also to be defined in the s_doPlugins function. 
 */ 
s.eVar10="May 10, 2012"; // the date the Post Click occurred 
s.eVar11="Post Click Product ID"; // e.g. "shoes" 
s.eVar12="Post Click Type of Action"; // e.g. "purchase"; 
```

>[!NOTE]
>
>위의 플러그인은 특정 사용자 지정 상거래 변수(eVar)를 사용할 수 있다고 가정합니다. 위의 플러그인에 지정된 변수가 Adobe Analytics 배포 내에서 사용할 수 없는 경우, 변수를 사용 가능한 변수로 교체하면 됩니다.

