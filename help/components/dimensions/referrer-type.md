---
title: 레퍼러 유형
description: 방문자의 위치에 따라 레퍼러 유형입니다.
translation-type: tm+mt
source-git-commit: 87d0c7e20594e2e39f55284e8d50d425cc1cdacf
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 0%

---


# 레퍼러 유형

&#39;레퍼러 유형&#39; 차원은 방문자가 사이트에 도달하기 위해 클릭스루한 범용 채널을 보고합니다. Adobe는 조직에서 각 채널에 대한 규칙을 유지하는 [마케팅 채널과](marketing-channel.md)달리 각 차원 값에 대한 규칙을 유지합니다.

## 데이터로 이 차원 채우기

이 차원은 Adobe 내부 여러 조회 테이블을 참조합니다. 각 값은 히트의 [레퍼러를](referrer.md) 기반으로 하며, 이것은 [내부 URL 필터에 따라 달라집니다](/help/admin/admin/internal-url-filter-admin.md). 레퍼러 차원과 내부 URL 필터가 올바르게 구성되어 있는지 확인합니다.

## 차원 값

차원 값에는 히트의 레퍼러 유형이 포함됩니다. 특정 값에는 다음이 포함됩니다.

* **입력/책갈피 표시**: 히트에 대한 레퍼러 데이터가 없습니다.
* **검색 엔진**: 레퍼러는 키워드 쿼리 문자열이 포함된 인식된 검색 엔진에서 왔습니다.
* **소셜 네트워크:**: 레퍼러 데이터는 Adobe에서 인증한 소셜 네트워크에 속해 있습니다.
* **기타 웹 사이트**: 레퍼러 데이터는 Adobe에서 인식하는 검색 엔진 또는 소셜 네트워크에 속하지 않았습니다.
* **하드 드라이브**: 레퍼러는 방문자의 하드 드라이브에 있는 웹 페이지의 로컬 복사본에서 비롯되었습니다.
* **이메일**: 레퍼러는 또는 의 프로토콜이 있는 URL에서 `imap://` 유래했습니다 `mail://`. 일반적으로 `https://` 프로토콜을 사용하기 때문에 온라인 이메일 서비스를 포함하지 않습니다.

### 소셜 네트워크

다음 목록은 Adobe에서 사용하는 &#39;소셜 네트워크&#39; 조회 테이블을 참조합니다. Adobe는 Adobe Analytics 고객을 위한 편의를 위해 이 목록을 제공합니다. Adobe에서 이 목록에 도메인을 추가하도록 권장하려면 조직의 지원 위임자가 고객 지원 센터에 연락하도록 하십시오.

>[!NOTE] 이 목록은 [마케팅 채널 처리 규칙의 기본 소셜 네트워크 목록과 다릅니다](../c-marketing-channels/c-rules.md).

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

### &#39;기타 웹 사이트&#39; 차원 값의 검색 엔진

&#39;레퍼러 유형&#39; 차원의 특정 도메인을 볼 때 &#39;기타 웹 사이트&#39; 아래에 나열된 &#39;검색 엔진&#39; 아래에 표시될 도메인이 있을 수 있습니다. 예를 들어 &#39;기타 웹 사이트&#39; `'google.com'` 아래에 표시될 수 있습니다.

* **&#39;검색 엔진&#39; 차원 값의 검색 엔진 도메인**: 레퍼러는 Adobe에서 검색 엔진으로 분류하기 위해 모든 기준을 충족했습니다. 참조 도메인은 유효한 검색 엔진이고 참조 URL에는 키워드 쿼리 문자열 매개 변수 *가* 포함됩니다.
* **&#39;기타 웹 사이트&#39; 차원 값의 검색 엔진 도메인**: 참조 URL이 검색 엔진으로 분류할 모든 기준을 충족하지 않았습니다. 일반적인 예로는 검색 외에 다른 기능에 전용 하위 도메인이 있습니다. 예를 들어, `mail.google.com` 또는 검색 엔진은 `autos.yahoo.com` 아니지만 일반적으로 검색과 연관된 최상위 도메인에 상주합니다. 이러한 하위 도메인은 키워드 쿼리 문자열을 포함하지 않습니다. 이 문자열이 &#39;검색 엔진&#39; 대신 &#39;기타 웹 사이트&#39;에 포함되는 이유입니다.
