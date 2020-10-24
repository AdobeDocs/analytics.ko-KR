---
title: 레퍼러 유형
description: 방문자가 어디에서 왔는지에 따른 레퍼러 유형입니다.
translation-type: ht
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: ht
source-wordcount: '423'
ht-degree: 100%

---


# 레퍼러 유형

레퍼러 유형 차원은 방문자가 사이트에 도달하기 위해 클릭스루한 일반 채널을 보고합니다. Adobe는 조직이 각 채널에 대한 규칙을 유지 관리하는 [마케팅 채널](marketing-channel.md)과 달리 각 차원 항목에 대한 규칙을 유지 관리합니다.

## 이 차원을 데이터로 채우기

이 차원은 Adobe 내부의 여러 조회 테이블을 참조합니다. 각 값은 히트의 [레퍼러](referrer.md)를 기반으로 하는데, 이것은 [내부 URL 필터](/help/admin/admin/internal-url-filter-admin.md)에 따라 달라집니다. 레퍼러 차원과 내부 URL 필터가 올바로 구성되어 있는지 확인하십시오.

## 차원 항목

차원 항목에는 히트의 레퍼러 유형이 포함됩니다. 구체적인 값으로는 다음 항목이 있습니다.

* **입력/책갈피 표시**: 히트에 대한 레퍼러 데이터가 없습니다.
* **검색 엔진**: 이 레퍼러는 키워드 쿼리 문자열을 포함하는 잘 알려진 검색 엔진에서 왔습니다.
* **소셜 네트워크:**: 레퍼러 데이터가 Adobe에서 인정한 소셜 네트워크에 속했습니다.
* **기타 웹 사이트**: 레퍼러 데이터가 Adobe에서 인정하는 검색 엔진 또는 소셜 네트워크에 속하지 않았습니다.
* **하드 드라이브**: 레퍼러가 방문자의 하드 드라이브에 있는 웹 페이지의 로컬 복사본에서 비롯되었습니다.
* **이메일**: 레퍼러가 `imap://` 또는 `mail://`의 프로토콜을 사용하는 URL에서 유래했습니다. 일반적으로 `https://` 프로토콜을 사용하기 때문에 온라인 이메일 서비스를 포함하지 않습니다.

### 소셜 네트워크

다음 목록은 Adobe에서 사용하는 &#39;소셜 네트워크&#39; 조회 테이블을 참조합니다. Adobe에서는 Adobe Analytics 고객을 위해 이 목록을 제공합니다. Adobe가 이 목록에 도메인을 추가하도록 권유하려면 조직의 지원 담당자를 통해 고객 지원 팀에 연락하십시오.

>[!NOTE]
>
>이 목록은 [마케팅 채널 처리 규칙](../c-marketing-channels/c-rules.md)의 기본 소셜 네트워크 목록과 다릅니다.

* `12seconds.tv`
* `t.163.com`
* `4travel.jp`
* `advogato.org`
* `ameba.jp`
* `anobii.com`
* `asmallworld.net`
* `avforums.com`
* `backtype.com`
* `badoo.com`
* `bebo.com`
* `bigadda.com`
* `bigtent.com`
* `biip.no`
* `blackplanet.com`
* `blogspot.com`
* `blogster.com`
* `blomotion.jp`
* `bolt.com`
* `brightkite.com`
* `buzznet.com`
* `cafemom.com`
* `care2.com`
* `classmates.com`
* `cloob.com`
* `collegeblender.com`
* `cyworld.co.kr`
* `cyworld.com.cn`
* `dailymotion.com`
* `yozm.daum.net`
* `delicious.com`
* `deviantart.com`
* `digg.com`
* `diigo.com`
* `disqus.com`
* `draugiem.lv`
* `facebook.com`
* `faceparty.com`
* `fc2.com`
* `flickr.com`
* `flixster.com`
* `fotolog.com`
* `foursquare.com`
* `friendfeed.com`
* `friendsreunited.com`
* `friendsreunited.co.uk`
* `friendster.com`
* `fubar.com`
* `gaiaonline.com`
* `geni.com`
* `goodreads.com`
* `plus.google.com`
* `plus.url.google.com`
* `grono.net`
* `habbo.com`
* `hatena.ne.jp`
* `t.hexun.com`
* `hi5.com`
* `hyves.nl`
* `ibibo.com`
* `identi.ca`
* `t.ifeng.com`
* `imeem.com`
* `hotnews.infoseek.co.jp`
* `instagram.com`
* `intensedebate.com`
* `irc-galleria.net`
* `iwiw.hu`
* `jaiku.com`
* `kaixin001.com`
* `kaixin002.com`
* `kakaku.com`
* `kanshin.com`
* `kozocom.com`
* `last.fm`
* `linkedin.com`
* `livejournal.com`
* `lnkd.in`
* `me2day.net`
* `meetup.com`
* `mister-wong.com`
* `mixi.jp`
* `mixx.com`
* `mouthshut.com`
* `multiply.com`
* `mumsnet.com`
* `myheritage.com`
* `mylife.com`
* `myspace.com`
* `myyearbook.com`
* `nasza-klasa.pl`
* `matome.naver.jp`
* `netlog.com`
* `nettby.no`
* `netvibes.com`
* `nextdoor.com`
* `nicovideo.jp`
* `ning.com`
* `odnoklassniki.ru`
* `ok.ru`
* `orkut.com`
* `pakila.jp`
* `t.people.com.cn`
* `photobucket.com`
* `pinterest.com (and all international domains)`
* `plaxo.com`
* `plurk.com`
* `po.st`
* `t.qq.com`
* `mp.weixin.qq.com`
* `boards.qwant.com`
* `reddit.com`
* `renren.com`
* `blog.seesaa.jp`
* `t.sina.com.cn`
* `skyrock.com`
* `slideshare.net`
* `smcb.jp`
* `smugmug.com`
* `t.sohu.com`
* `sonico.com`
* `studivz.net`
* `stumbleupon.com`
* `t.co`
* `tabelog.com`
* `tagged.com`
* `taringa.net`
* `thefancy.com`
* `toutiao.com`
* `tripit.com`
* `trombi.com`
* `trytrend.jp`
* `tuenti.com`
* `tumblr.com`
* `twine.com`
* `twitter.com`
* `uhuru.jp`
* `viadeo.com`
* `vimeo.com`
* `vk.com`
* `wayn.com`
* `weibo.com`
* `weourfamily.com`
* `wer-kennt-wen.de`
* `wordpress.com`
* `xanga.com`
* `xing.com`
* `answers.yahoo.com`
* `yammer.com`
* `yaplog.jp`
* `yelp.com`
* `yelp.co.uk`
* `youku.com`
* `youtube.com`
* `yuku.com`
* `zooomr.com`
* `zhihu.com`

### 기타 웹 사이트 차원 항목의 검색 엔진

레퍼러 유형 차원의 특정 도메인을 볼 때 &#39;기타 웹 사이트&#39; 아래 대신 나열되어 있는 &#39;검색 엔진&#39; 아래에 예상되는 도메인이 있을 수 있습니다. 예를 들어 &#39;기타 웹 사이트&#39; 아래에 `'google.com'`이 보일 수 있습니다.

* **검색 엔진 차원 항목의 검색 엔진 도메인**: 레퍼러가 Adobe에서 검색 엔진으로 분류하기 위한 모든 기준을 충족했습니다. 참조 도메인은 유효한 검색 엔진&#x200B;*이고* 참조 URL은 키워드 쿼리 문자열 매개 변수를 포함합니다.
* **기타 웹 사이트 차원 항목의 검색 엔진 도메인**: 참조 URL이 검색 엔진으로 분류하기 위한 모든 기준을 충족하지 않았습니다. 일반적인 예에는 검색 외에 다른 기능을 위한 전용 하위 도메인이 포함됩니다. 예를 들어, `mail.google.com` 또는 `autos.yahoo.com`은 검색 엔진이 아니지만 일반적으로 검색과 연관된 최상위 도메인에 있습니다. 이러한 하위 도메인은 키워드 쿼리 문자열을 포함하지 않습니다. 따라서 이러한 문자열은 &#39;검색 엔진&#39; 대신 &#39;기타 웹 사이트&#39;에 포함합니다.
