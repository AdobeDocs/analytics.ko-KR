---
description: HTML 샘플 페이지 내에서 서버가 생성한 이미지 태그의 사용 예시입니다.
keywords: Analytics 구현; 변수
seo-description: HTML 샘플 페이지 내에서 서버가 생성한 이미지 태그의 사용 예시입니다.
seo-title: 샘플 코드
solution: Analytics
title: 샘플 코드
topic: 개발자 및 구현
uuid: 47 E 5 E 82 C-CFB 2-4912-919 B -720 B 2 EE 852 BA
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 샘플 코드

HTML 샘플 페이지 내에서 서버가 생성한 이미지 태그의 사용 예시입니다.

아래 표에는 샘플에 사용된 값들이 표시되어 있습니다.

| 변수 | 값 |
|---|---|
| pageName | Order Confirmation |
| Current URL | https://www.somesite.com/cart/confirmation.asp |
| events | purchase,event1 |
| c1 | Registered |
| purchaseID | 0123456 |
| products | Books;Book Name;1;19.95 |
| state | CA |
| zip | 90210 |
| a random # | 123456 |

## 예제 1 {#section_91D91CE318AE43F0ADDF6005607E83C7}

아래 예에는 서버측 이미지 태그가 표시됩니다. 강조 표시된 무작위 번호는 이미지 캐시를 방지합니다.

```
<html> 
<head> 
</head> 
<body> 
Order Confirmation<br> 
Thanks for your order #0123456. 
<img src="https://102.112.207.net/b/ss/suite1,suite2/1/G.4--NS 
<codeph outputclass="syntax">
  /123456?pageName=Order%20 Confirmation&events=purchase%2Cevent1&c1=Registered&purchaseID=0123456&products=Books%3BBook%20Name%3B1%3B19.95&state=CA&zip=90210&g=https%3A//www.somesite.com/cart/confirmation.asp" width="1" height="1" border="0" /> 
 </body> 
 </html> 
  
</codeph outputclass="syntax">
```

## 예제 2 {#section_726D12029583428BA853043F988ED1B8}

아래 예는 최소한의 JavaScript 이미지 태그를 보여 줍니다.

```
<html> 
<head> 
</head> 
<body> 
Order Confirmation<br> 
Thanks for your order #0123456. 
<script language="javascript"><!— 
s.s_date = new Date(); 
s.s_rdm = s.s_date.getTime(); 
s.s_desturl="<img width=\"1\" height=\"1\" 
src=\"https://102.112.207.net/b/ss/suite1,suite2/1/G.4--NS/" + s.s_rdm + 
"?pageName=Order%20Confirmation&events=purchase%2Cevent1&c1=Registered 
&purchaseID=0123456&products=Books%3BBook%20Name%3B1%3B19.95&state=CA&zip=90210&g=http 
s%3A//www.somesite.com/cart/confirmation.asp\">"; 
document.write(s.s_desturl); 
//--></script> 
</body> 
</html> 
```

