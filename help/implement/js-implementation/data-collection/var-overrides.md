---
description: 변수 무시는 하나의 추적 또는 추적 링크 호출에 대한 변수 값을 변경할 수 있도록 해줍니다.
keywords: Analytics 구현
seo-description: 변수 무시는 하나의 추적 또는 추적 링크 호출에 대한 변수 값을 변경할 수 있도록 해줍니다.
seo-title: 변수 무시
solution: Analytics
subtopic: 변수
title: 변수 무시
topic: 개발자 및 구현
uuid: 3ec09ae8-b9df-426f-8065-42b4518e6c5f
translation-type: ht
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 변수 무시

변수 무시는 하나의 추적 또는 추적 링크 호출에 대한 변수 값을 변경할 수 있도록 해줍니다.

변수를 무시하려면 새 개체를 만들고 변수 값을 지정한 다음 이 개체를 첫 번째 매개 변수로 `s.t()`에 전달하거나, 네 번째 매개 변수로 `s.tl()`에 전달합니다.

```js
s.eVar1="one"; 
s.eVar2="two"; 
s.eVar3="three"; 
  
overrides = new Object(); 
overrides.eVar1="1_one"; 
overrides.eVar2=""; 
  
s.t(overrides);  
// values passed: eVar1="1_one", eVar2="", eVar3="three"
```

```js
s.linkTrackVars="eVar1,eVar2,eVar3,events"; 
s.eVar1="one"; 
s.eVar2="two"; 
s.eVar3="three"; 
 
overrides = new Object(); 
overrides.eVar1="1_one"; 
overrides.eVar2=""; 
 
s.tl(this,'e','AnotherSite',overrides,'navigate')  
// values passed: eVar1="1_one", eVar2="", eVar3="three"
```

