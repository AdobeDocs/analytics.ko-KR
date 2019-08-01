---
description: 'JavaScript 플러그인 데이터 수집 방법을 선택한 경우 다음 코드 줄을 복사하여 페이지의 Analytics 코드에 추가합니다. '
seo-description: 'JavaScript 플러그인 데이터 수집 방법을 선택한 경우 다음 코드 줄을 복사하여 페이지의 Analytics 코드에 추가합니다. '
seo-title: Analytics 플러그인 코드
title: Analytics 플러그인 코드
uuid: 534874 BD -49 D 9-4 B 15-8019-B 503 DFCF 3182
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Analytics Plug-In Code{#analytics-plug-in-code}

JavaScript 플러그인 데이터 수집 방법을 선택한 경우 다음 코드 줄을 복사하여 페이지의 Analytics 코드에 추가합니다.

`/*`

`* Plugin: getQueryParam 2.3`

`*/ s.getQueryParam=new Function("p","d","u","" +"var s=this,v='',i,t;d=d?d:'';u=u?u:(s.pageURL?s.pageURL:s.wd.locati" +"on);if(u=='f')u=s.gtfs().location;while(p){i=p.indexOf(',');i=i<0?p" +".length:i;t=s.p_gpv(p.substring(0,i),u+'');if(t){t=t.indexOf('#')>-" +"1?t.substring(0,t.indexOf('#')):t;}if(t)v+=v?d+t:t;p=p.substring(i=" +"=p.length?i:i+1)}return v"); s.p_gpv=new Function("k","u","" +"var s=this,v='',i=u.indexOf('?'),q;if(k&&i>-1){q=u.substring(i+1);v" +"=s.pt(q,'&','p_gvf',k)}return v"); s.p_gvf=new Function("t","k","" +"if(t){var s=this,i=t.indexOf('='),p=i<0?t:t.substring(0,i),v=i<0?'T" +"rue':t.substring(i+1);if(p.toLowerCase()==k. oLowerCase())return s." +"epa(v)}return ''");`

`/*in the s_doPlugins function`

`s.campaign=s.getQueryParam("ET_CID"); //places query param value from cid in campaign variable s.eVar2=s.getQueryParam("ET_RID"); //places query param value from rid in eVar2 variable`

>[!NOTE]
>
>위의 플러그인은 특정 사용자 지정 상거래 변수 (Evar) 를 사용할 수 있다고 가정합니다. 위의 플러그인에 지정된 변수를 Analytics 배포 내에서 사용할 수 없는 경우, 사용 가능한 것으로 대체하면 됩니다.

