---
description: getValOnce 플러그인은 주어진 변수가 이전에 정의된 값으로 설정되는 것을 방지합니다. 여기서는 쿠키를 사용하여 변수에서 마지막으로 확인된 값을 파악합니다. 현재 값이 쿠키 값과 일치하는 경우는 변수를 Adobe의 처리 서버로 보내기 전에 빈 문자열로 덮어씁니다. 이 플러그인은 사용자가 페이지를 새로 고치거나 뒤로 단추를 클릭했을 때 전환 변수 인스턴스가 부풀려지는 문제를 방지하는 데 유용합니다.
keywords: Analytics 구현
seo-description: getValOnce 플러그인은 주어진 변수가 이전에 정의된 값으로 설정되는 것을 방지합니다. 여기서는 쿠키를 사용하여 변수에서 마지막으로 확인된 값을 파악합니다. 현재 값이 쿠키 값과 일치하는 경우는 변수를 Adobe의 처리 서버로 보내기 전에 빈 문자열로 덮어씁니다. 이 플러그인은 사용자가 페이지를 새로 고치거나 뒤로 단추를 클릭했을 때 전환 변수 인스턴스가 부풀려지는 문제를 방지하는 데 유용합니다.
seo-title: getValOnce
solution: Analytics
subtopic: 플러그인
title: getValOnce
topic: 개발자 및 구현
uuid: 82 FE 0 DA 5-3 BC 4-4632-8 C 62-7 B 5683 F 6 B 587
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# getValOnce

getValOnce 플러그인은 주어진 변수가 이전에 정의된 값으로 설정되는 것을 방지합니다. 여기서는 쿠키를 사용하여 변수에서 마지막으로 확인된 값을 파악합니다. 현재 값이 쿠키 값과 일치하는 경우는 변수를 Adobe의 처리 서버로 보내기 전에 빈 문자열로 덮어씁니다. 이 플러그인은 사용자가 페이지를 새로 고치거나 뒤로 단추를 클릭했을 때 전환 변수 인스턴스가 부풀려지는 문제를 방지하는 데 유용합니다.

>[!IMPORTANT]
>
>This plug-in has not been validated to be compatible with [AppMeasurement for JavaScript](../../../implement/js-implementation/c-appmeasurement-js/appmeasure-mjs.md#concept_F3957D7093A94216BD79F35CFC1557E8). [Appmeasurement 플러그인 지원을 참조하십시오](../../../implement/js-implementation/c-appmeasurement-js/plugins-support.md#concept_E31A189BC8A547738666EB5E00D2252A).

**매개 변수**

```js
s.eVar1=s.getValOnce(variable,cookie,expiration,minute);
```

* **변수:** 확인할 변수입니다. 일반적으로 정의되는 변수와 같습니다.
* **쿠키:** 비교할 이전 값을 저장하는 쿠키의 이름입니다. 쿠키에는 어떤 값이든 사용할 수 있습니다.
* (선택 사항) **만료:** 쿠키가 만료되는 일 수입니다. 0으로 설정되지 않은 경우 기본 만료 기간은 브라우저 세션입니다.
* (선택 사항) **분:** 문자열 값 *`m`*&#x200B;인 경우 만료 값은 일 수 대신 분 단위로 정의됩니다. If not set, *`days`* is the default expiration.

**속성**

* 이 플러그인은 일반적으로 전환 변수에 사용됩니다. 그러나 어떤 [!DNL Analytics] 변수에나 사용할 수 있습니다.
* Javascript에서 이 함수가 검색되면 정의된 값을 쿠키에 저장된 값과 비교합니다. 정의된 값이 쿠키 값과 다른 경우는 정의된 값이 설정됩니다. 정의된 값이 쿠키 값과 같은 경우는 빈 문자열이 반환됩니다.
* 쿠키에는 단일 값만 저장할 수 있으므로 플러그인은 마지막으로 정의된 값만 확인합니다.
* 플러그인은 정의된 후 모든 값의 변수 정의를 중지하지 않습니다. 플러그인은 마지막 값이 여러 번 연속으로 설정되는 것만 방지합니다.
* 최종 사용자가 쿠키를 차단하거나 거부한 경우는 항상 원본 값이 반환됩니다.
* 플러그인의 세션은 [!DNL Analytics]에서 정의하는 세션(또는 방문)과 다릅니다. [!DNL Analytics]는 활동이 있는 경우 12시간 또는 활동이 없는 경우 30분 후에 종료됩니다. 플러그인에서 브라우저의 세션 정의를 사용하기 때문에 사용자가 탭을 닫거나 브라우저를 종료한 후에만 종료됩니다.

   * 사용자가 페이지를 닫고 다른 탭을 열었다가 30분 이내에 사이트로 돌아올 경우, 플러그인은 [!DNL Analytics] 방문을 열어 둔 채로 새 세션을 생성합니다.
   * 사용자가 30분 이상 링크를 클릭하지 않고 브라우저 창을 열어 두면 브라우저 세션이 열려 있는 상태로 [!DNL Analytics] 방문이 만료됩니다.

>[!NOTE]
>
>다음 지침을 따르면 사이트에서 데이터 수집 코드를 수정해야 합니다. 이 작업은 사이트의 데이터 수집에 영향을 줄 수 있으며 [!DNL Analytics] 사용 및 구현 경험이 풍부한 개발자가 수행해야만 합니다.

## 구현 {#section_177FF7F425B64FFB83CDE15A6ACC8D21}

>[!NOTE]
>
>If your organization uses Marketing Channels and has rules set up based on `s.campaign`, it is recommended that you not use the getValOnce plugin when setting the `s.campaign`value. 이렇게 하면 보조 캠페인 클릭 스루에 잘못된 채널이 할당될 수 있습니다.

이 플러그인을 구현하려면 [!DNL s_code.js] 파일에 다음 코드를 넣습니다.

```js
/******************************************************************** 
 * 
 * Main Plug-in code (should be in Plug-ins section) 
 * 
 *******************************************************************/ 
/* 
 * Plugin: getValOnce_v1.11 
 */ 
s.getValOnce=new Function("v","c","e","t","" 
+"var s=this,a=new Date,v=v?v:'',c=c?c:'s_gvo',e=e?e:0,i=t=='m'?6000" 
+"0:86400000,k=s.c_r(c);if(v){a.setTime(a.getTime()+e*i);s.c_w(c,v,e" 
+"==0?0:a);}return v==k?'':v");
```

Once the above code is implemented, define the desired variable using the *`getValOnce`* function. 다음은 몇 가지 구현 방법의 예입니다.

**쿠키를 설정하고 30일 이내에 중복 값이 검색될 경우 같은 캠페인 값 정의 방지:**
`s.campaign=s.getValOnce(s.campaign,'s_cmp',30);`**쿠키를 설정하고 30 분 이내에 중복 값이 감지되면 동일한 Evar 1 값을 정의할 수 없습니다.**`s.eVar1=s.getValOnce(s.eVar1,'s_ev1',30,'m');`**동일한 브라우저 세션에서 동일한 Evar 2 값이 여러 번 정의되지 않도록 합니다.**`s.eVar2=s.getValOnce(s.eVar2,'s_ev2');`**참고 사항**

* 프로덕션 환경에 플러그인을 배포하기 전에 항상 플러그인 설치를 종합적으로 테스트하여 데이터 수집이 예상대로 수행되는지 확인하십시오.
* 테스트 동안 반드시 쿠키를 삭제하거나 새로운 고유값을 사용하십시오. 그렇지 않으면 변수가 전송되지 않습니다.

