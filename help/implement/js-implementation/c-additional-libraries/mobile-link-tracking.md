---
description: 'null'
keywords: Analytics 구현; 링크 참조; REDIR
seo-description: 'null'
seo-title: 모바일 프로토콜에서의 사용자 지정 링크 측정
solution: Analytics
title: 모바일 프로토콜에서의 사용자 지정 링크 측정
topic: 개발자 및 구현
uuid: EB 82 DE 26-DA 2 E -41 C 2-8924-59 B 6 B 5 CCEF 28
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 모바일 프로토콜에서의 사용자 지정 링크 측정

많은 모바일 장치 사용자가 podcast, 벨소리 등의 파일을 장치로 다운로드합니다. JavaScript를 지원하지 않는 모바일 장치가 많기 때문에 링크 측정은 리디렉션을 통해 구현되어야 합니다. 리디렉션을 사용하려면 html의 href 링크를 수정해서 REDIR 요소를 포함시켜야 합니다. 사용자 지정 링크에 대한 일반 포맷은 다음과 같습니다.

```
https://<your_Namespace>.112.2o7.net/b/ss/<RSID>/4/REDIR/
?url=<destination_URL>&pe=<link_type>&pev1=<current_URL>&pev2=<link_name>
```

링크 참조를 만들 때 다음을 유의하십시오.

* URL 값은 URL 인코딩되어야 합니다.
* pageName 또는 페이지 URL(g) 매개 변수를 설정해야 합니다.
* 동적 변수는 URL 매개 변수를 읽을 수 있지만 설정할 수 없습니다.
* 쿠키가 설정되지 않은 경우 Adobe 서버는 일반적인 쿠키 handshake를 수행합니다.
* 링크를 추적하려면 pe, pev1 및 pev2 매개 변수를 포함해야 합니다.

사용자 지정 링크 측정 URL은 다음과 비슷한 모양입니다.

```
<a href=" https://johnny_appleseed.122.2o7.net/b/ss/appleseedpodcasts/4/REDIR/
?url=http%3A%2F%2Fwww.johnny_appleseed.org%2Fmpegs%2Fplanting_apple_trees.mpeg&pe=lnk_d
&pev1=http%3A%2F%2Fwww.johnny_appleseed.org%2Fmpegs%2Fplanting_apple_trees.mpeg&pev2=pl anting_apple_trees&">Planting an Apple Tree</a>
```

자세한 내용은 [종료 링크 추적 재지정 백서](https://marketing.adobe.com/resources/help/en_US/whitepapers/redirects/)를 참조하십시오.
