---
title: Analytics 차원 호환성
description: Analytics 차원 및 보고서에 대한 참조.
feature: Dimensions
exl-id: 1884bc20-b04d-4f9a-b057-2b2fbe53190d
source-git-commit: 7609ecb3c34fb0bc8293fc1ecd409cfabb327295
workflow-type: tm+mt
source-wordcount: '896'
ht-degree: 60%

---

# Analytics 차원 호환성

이 페이지에는 각 Analytics 기능에서 지원되는 [차원](overview.md)이 나열됩니다.

>[!NOTE]
>
>사용자 정의 변수 이름, 분류 및 방문자 속성은 이 목록에서 생략됩니다. 이러한 차원 항목은 개별 보고서 세트에 따라 다릅니다.

## Analysis Workspace에서 지원되는 차원

| 차원 이름 (Analytics UI에 표시됨) | 차원 ID (API 요청에 사용됨) |
|---|---|
| Target용 Analytics | `targetraw` |
| 대상자 ID | `mcaudiences` |
| [브라우저](browser.md) | `browser` |
| [브라우저 유형](browser-type.md) | `browsertype` |
| [카테고리](category.md) | `category` |
| [도시](cities.md) | `geocity` |
| [색상 깊이](color-depth.md) | `colordepth` |
| [연결 유형](connection-type.md) | `connectiontype` |
| [쿠키 지원](cookie-support.md) | `cookie` |
| [국가](countries.md) | `geocountry` |
| [고객 충성도](customer-loyalty.md) | `customerloyalty` |
| [사용자 지정 전환 변수](evar.md) | `evar1`, `evar2` 등 |
| [Custom Insight 변수](prop.md) | `prop1`, `prop2` 등 |
| [사용자 지정 링크](custom-link.md) | `customlink` |
| [첫 구매까지 소요된 일 수](days-before-first-purchase.md) | `daysbeforefirstpurchase` |
| [마지막 구매 이후 일 수](days-since-last-purchase.md) | `dayssincelastpurchase` |
| [도메인](domain.md) | `filtereddomain` |
| [링크 다운로드](download-link.md) | `downloadlink` |
| [시작 페이지](entry-dimensions.md) | `entrypage` |
| [원래 시작 페이지](entry-dimensions.md) | `entrypageoriginal` |
| [종료 링크](exit-link.md) | `exitlink` |
| [첫 번째 터치 채널](first-touch-channel.md) | `firsttouchchannel` |
| [첫 번째 터치 채널 세부 정보](first-touch-detail.md) | `firsttouchchanneldetail` |
| [Java 활성화](java-enabled.md) | `javaenabled` |
| [언어](language.md) | `language` |
| [마지막 터치 채널](last-touch-channel.md) | `lasttouchchannel` |
| [마지막 터치 채널 세부 정보](last-touch-detail.md) | `lasttouchchanneldetail` |
| 목록 변수 | `listvariables` |
| [마케팅 채널](marketing-channel.md) | `marketingchannel` |
| [모바일 오디오 지원](mobile-dimensions.md) | `mobileaudiosupport` |
| [모바일 통신사](mobile-dimensions.md) | `mobilecarrier` |
| [모바일 색상 깊이](mobile-dimensions.md) | `mobilecolordepth` |
| [모바일 쿠키 지원](mobile-dimensions.md) | `mobilecookiesupport` |
| [모바일 장치](mobile-dimensions.md) | `mobiledevicename` |
| [모바일 장치 유형](mobile-dimensions.md) | `mobiledevicetype` |
| [모바일 최대 전자 메일 길이](mobile-dimensions.md) | `mobileemaillength` |
| [모바일 이미지 지원](mobile-dimensions.md) | `mobileimagesupport` |
| [모바일 제조업체](mobile-dimensions.md) | `mobilemanufacturer` |
| [모바일 운영 체제(더 이상 사용되지 않음)](mobile-dimensions.md) | `mobileos` |
| [모바일 화면 높이](mobile-dimensions.md) | `mobilescreenheight` |
| [모바일 화면 크기](mobile-dimensions.md) | `mobilescreensize` |
| [모바일 화면 너비](mobile-dimensions.md) | `mobilescreenwidth` |
| [모바일 최대 브라우저 URL 길이](mobile-dimensions.md) | `mobileurllength` |
| [모바일 비디오 지원](mobile-dimensions.md) | `mobilevideosupport` |
| [모니터 해상도](monitor-resolution.md) | `monitorresolution` |
| [운영 체제](operating-systems.md) | `operatingsystem` |
| [원래 참조 도메인](original-referring-domain.md) | `referringdomainoriginal` |
| [페이지](page.md) | `page` |
| [페이지를 찾을 수 없음](pages-not-found.md) | `pagesnotfound` |
| [제품](product.md) | `product` |
| [레퍼러](referrer.md) | `referrer` |
| [레퍼러 유형](referrer-type.md) | `referrertype` |
| [참조 도메인](referring-domain.md) | `referringdomain` |
| [지역](regions.md) | `georegion` |
| [반환 빈도](return-frequency.md) | `returnfrequency` |
| SC-TnT | `tntbase` |
| [검색 엔진](search-engine.md) | `searchengine` |
| [검색 키워드](search-keyword.md) | `searchenginekeyword` |
| [검색 엔진 - 자연어](search-engine.md) | `searchenginenatural` |
| [검색 엔진 - 유료](search-engine.md) | `searchenginepaid` |
| [검색 키워드 - 자연어](search-keyword.md) | `searchenginenaturalkeyword` |
| [검색 키워드 - 유료](search-keyword.md) | `searchenginepaidkeyword` |
| [모든 검색 페이지 등급](all-search-page-rank.md) | `searchenginepagerank` |
| [서버](server.md) | `server` |
| [단일 페이지 방문 횟수](single-page-visits.md) | `singlepagevisits` |
| [사이트 섹션](site-section.md) | `sitesections` |
| [방문당 체류 시간 - 세부기간](time-spent-per-visit.md) | `sitetime` |
| [추적 코드](tracking-code.md) | `campaign` |
| [US DMA](us-dma.md) | `geodma` |
| [미국 주](us-states.md) | `state` |
| [이벤트까지 남은 시간](time-prior-to-event.md) | `timeprior` |
| [방문당 체류 시간 - 그룹화됨](time-spent-per-visit.md) | `timespent` |
| [방문 깊이](visit-depth.md) | `pathlength` |
| [방문 횟수](visit-number.md) | `visitnumber` |
| [우편번호](zip-code.md) | `zip` |
| [오전/오후](am-pm.md) | `timepartampm` |
| [브라우저 높이 - 전체기간](browser-height.md) | `browserheightbucketed` |
| [브라우저 너비 - 전체기간](browser-width.md) | `browserwidthbucketed` |
| [일](day.md) | `daterangeday` |
| [날짜](day-of-month.md) | `timepartdayofmonth` |
| [요일](day-of-week.md) | `dayofweek` |
| [요일](day-of-week.md) | `timepartdayofweek` |
| [일 (한 해 기준)](day-of-year.md) | `timepartdayofyear` |
| [마지막 방문 이후의 일수](days-since-last-visit.md) | `dayssincelastvisit` |
| [시작 사용자 지정 인사이트](entry-dimensions.md) | `entryprops` |
| [시작 목록 변수](entry-dimensions.md) | `entrylistvariables` |
| [시작 서버](entry-dimensions.md) | `entryserver` |
| [시작 사이트 섹션](entry-dimensions.md) | `entrysitesections` |
| [사용자 지정 인사이트 종료](exit-dimensions.md) | `exitprops` |
| [종료 목록 변수](exit-dimensions.md) | `exitlistvariables` |
| [종료 페이지](exit-dimensions.md) | `exitpage` |
| [서버 종료](exit-dimensions.md) | `exitserver` |
| [사이트 섹션 종료](exit-dimensions.md) | `exitsitesections` |
| [히트 깊이](hit-depth.md) | `hitdepth` |
| [히트 유형](hit-type.md) | `hittype` |
| [시간](hour.md) | `daterangehour` |
| [시간 (일 기준)](hour-of-day.md) | `timeparthourofday` |
| [마케팅 채널 세부 정보](marketing-detail.md) | `marketingchanneldetail` |
| [분](minute.md) | `daterangeminute` |
| [모바일 최대 책갈피 길이](mobile-dimensions.md) | `mobilebookmarklength` |
| [모바일 장치 번호](mobile-dimensions.md) | `mobiledevicenumber` |
| [모바일 DRM](mobile-dimensions.md) | `mobiledrm` |
| [모바일 정보 서비스](mobile-dimensions.md) | `mobileinformationservices` |
| [모바일 Java VM](mobile-dimensions.md) | `mobilejavavm` |
| [모바일 메일 장식](mobile-dimensions.md) | `mobilemaildecoration` |
| [모바일 네트 프로토콜](mobile-dimensions.md) | `mobilenetprotocols` |
| [Mobile Push To Talk](mobile-dimensions.md) | `mobilepushtotalk` |
| [월](month.md) | `daterangemonth` |
| [월 (연 기준)](month-of-year.md) | `timepartmonthofyear` |
| [운영 체제 유형](operating-system-types.md) | `operatingsystemgroup` |
| [유료 검색](paid-search.md) | `paidsearch` |
| [영구적 쿠키 지원](persistent-cookie-support.md) | `persistentcookie` |
| [분기](quarter.md) | `daterangequarter` |
| [사분기](quarter-of-year.md) | `timepartquarterofyear` |
| 설문 조사 | `surveybase` |
| [페이지 체류 시간 - 그룹화됨](time-spent-on-page.md) | `averagepagetime` |
| [페이지 체류 시간 - 세부기간](time-spent-on-page.md) | `pagetimeseconds` |
| [옵트아웃 이유 추적](tracking-opt-out-reason.md) | `optoutreason` |
| [평일/주말](weekday-weekend.md) | `timepartweekdayweekend` |
| [주](week.md) | `daterangeweek` |
| [년](year.md) | `daterangeyear` |

## Analysis Workspace에서만 지원되는 콘텐츠 인식 차원

| 차원 이름 (Analytics UI에 표시됨) | 차원 ID (API 요청에 사용됨) |
|--- |--- |
| Activity Map XY | `clickmapxy` |
| 미디어 세션 ID | `videosessionid` |
| Nielsen 액세스 방법 | `nielsenaccmethod` |
| Nielsen 앱 ID | `nielsenappid` |
| Channel 채널 자산 | `nielsenchannelasset` |
| Nielsen 콘텐츠 유형 | `nielsencontenttype` |

## Analysis Workspace에서 지원하는 컨텐츠 인식 차원

### 비디오(스트리밍 미디어 서비스)

| 차원 이름 (Analytics UI에 표시됨) | 차원 ID (API 요청에 사용됨) |
|--- |--- |
| [콘텐츠](sm-core.md) | `video` |
| [컨텐츠 세그먼트](sm-core.md) | `videosegment` |
| [컨텐츠 유형](sm-core.md) | `videocontenttype` |
| [광고 플레이어 이름](sm-ads.md) | `videoadplayername` |
| [Pod의 광고 위치](sm-ads.md) | `videoadinpod` |
| [드롭된 프레임](sm-quality.md) | `videoqoedroppedframecountevar` |
| [오류](sm-quality.md) | `videoqoeerrorcountevar` |
| [평균 비트율](sm-quality.md) | `videoqoebitrateaverageevar` |
| [비트율 변경](sm-quality.md) | `videoqoebitratechangecountevar` |
| [총 버퍼 지속 시간](sm-quality.md) | `videoqoebuffertimeevar` |
| [버퍼 이벤트](sm-quality.md) | `videoqoebuffercountevar` |
| [시작 시간](sm-quality.md) | `videoqoetimetostartevar` |
| [광고 Pod](sm-ads.md) | `videoadpod` |
| [미디어 경로](sm-core.md) | `videopath` |
| [광고](sm-ads.md) | `videoad` |
| [컨텐츠 플레이어 이름](sm-core.md) | `videoplayername` |
| [컨텐츠 채널](sm-core.md) | `videochannel` |
| [챕터](sm-chapters.md) | `videochapter` |
| [컨텐츠 이름(변수)](sm-core.md) | `videoname` |
| [컨텐츠 길이(변수)](sm-core.md) | `videolength` |
| [광고 이름(변수)](sm-ads.md) | `videoadname` |
| [광고 길이(변수)](sm-ads.md) | `videoadlength` |
| [정보](sm-video-metadata.md) | `videoshow` |
| [시즌](sm-video-metadata.md) | `videoseason` |
| [에피소드](sm-video-metadata.md) | `videoepisode` |
| [네트워크](sm-video-metadata.md) | `videonetwork` |
| [표시 유형](sm-video-metadata.md) | `videoshowtype` |
| [광고 로드](sm-ads.md) | `videoadload` |
| [MVPD](sm-video-metadata.md) | `videomvpd` |
| [방송 시간대](sm-video-metadata.md) | `videodaypart` |
| [광고주](sm-ads.md) | `videoadadvertiser` |
| [캠페인 ID](sm-ads.md) | `videoadcampaign` |
| [장르](sm-video-metadata.md) | `videogenre` |
| [스트림 유형](sm-core.md) | `videostreamtype` |
| [플레이어 SDK 오류 ID](sm-quality.md) | `videoqoeplayersdkerrors` |
| [외부 오류 ID](sm-quality.md) | `videoqoeextneralerrors` |
| [미디어 피드 유형](sm-video-metadata.md) | `videofeedtype` |
| [시작 미디어 경로](entry-dimensions.md) | `entryvideopath` |
| [미디어 경로 종료](exit-dimensions.md) | `exitvideopath` |
| [시작 장르](entry-dimensions.md) | `entryvideogenre` |
| [장르 종료](exit-dimensions.md) | `exitvideogenre` |
| [시작 플레이어 SDK 오류 ID](entry-dimensions.md) | `entryvideoqoeplayersdkerrors` |
| [종료 플레이어 SDK 오류 ID](exit-dimensions.md) | `exitvideoqoeplayersdkerrors` |
| [항목 외부 오류 ID](entry-dimensions.md) | `entryvideoqoeextneralerrors` |
| [외부 오류 ID 종료](exit-dimensions.md) | `exitvideoqoeextneralerrors` |

### Adobe Social

Adobe Social이 사용 중단되었습니다.

| 차원 이름 (Analytics UI에 표시됨) | 차원 ID (API 요청에 사용됨) |
|--- |--- |
| 용어 | `socialterm` |
| 소셜 플랫폼/속성 | `socialcontentprovider` |
| 작성자 | `socialauthor` |
| 언어 | `sociallanguage` |
| 위도/경도 | `sociallatlong` |
| 자산 추적 코드 | `socialassettrackingcode` |
| 소유한 소셜 속성 | `socialaccountandappids` |
| 소유한 게시 ID | `socialownedpostids` |
| 소유한 소셜 정의 | `socialinteractiontype` |
| 소유한 속성 ID | `socialownedpropertyid` |
| 소유한 속성과 애플리케이션 비교 | `socialownedpropertypropertyvsapp` |
| 소유한 속성 이름 | `socialownedpropertyname` |
| 소유한 정의 속성과 게시 비교 | `socialowneddefinitionpropertyvspost` |
| 소유한 정의 인사이트 유형 | `socialowneddefinitioninsighttype` |
| 소유한 정의 인사이트 값 | `socialowneddefinitioninsightvalue` |
| 소유된 정의 지표 | `socialowneddefinitionmetric` |
| 자산 | `socialmediaid` |

### Mobile SDK

| 차원 이름 (Analytics UI에 표시됨) | 차원 ID (API 요청에 사용됨) |
|--- |--- |
| [첫 번째 실행 날짜](lifecycle-dimensions.md) | `mobileinstalldate` |
| [앱 ID](lifecycle-dimensions.md) | `mobileappid` |
| [시작 번호](lifecycle-dimensions.md) | `mobilelaunchnumber` |
| [최초 사용 이후 일 수](lifecycle-dimensions.md) | `mobiledayssincefirstuse` |
| [마지막 사용 이후 일 수](lifecycle-dimensions.md) | `mobiledayssincelastuse` |
| [시간(SDK)](lifecycle-dimensions.md) | `mobilehourofday` |
| [요일(SDK)](lifecycle-dimensions.md) | `mobiledayofweek` |
| [운영 체제(SDK)](lifecycle-dimensions.md) | `mobileosenvironment` |
| [마지막 업그레이드 이후 일 수](lifecycle-dimensions.md) | `mobiledayssincelastupgrade` |
| [마지막 업그레이드 이후 출시](lifecycle-dimensions.md) | `mobilelaunchessincelastupgrade` |
| [장치 이름(SDK)](lifecycle-dimensions.md) | `mobiledevice` |
| [운영 체제 버전(SDK)](lifecycle-dimensions.md) | `mobileosversion` |
| [비콘 Major](lifecycle-dimensions.md) | `mobilebeaconmajor` |
| [비콘 Minor](lifecycle-dimensions.md) | `mobilebeaconminor` |
| [비콘 UUID](lifecycle-dimensions.md) | `mobilebeaconuuid` |
| [비콘 Proximity](lifecycle-dimensions.md) | `mobilebeaconproximity` |
| [위치(10km까지)](lifecycle-dimensions.md) | `latlon1` |
| [위치(100m까지)](lifecycle-dimensions.md) | `latlon23` |
| [위치(1m까지)](lifecycle-dimensions.md) | `latlon45` |
| [관심 영역 이름](lifecycle-dimensions.md) | `pointofinterest` |
| [관심 영역 중앙까지의 거리](lifecycle-dimensions.md) | `pointofinterestdistance` |
| [위치 정확도](lifecycle-dimensions.md) | `mobileplaceaccuracy` |
| [범주 배치](lifecycle-dimensions.md) | `mobileplacecategory` |
| [위치 ID](lifecycle-dimensions.md) | `mobileplaceid` |
| [시작 비콘 Major](lifecycle-dimensions.md) | `entrymobilebeaconmajor` |
| [종료 비콘 Major](lifecycle-dimensions.md) | `exitmobilebeaconmajor` |
| [시작 비콘 Minor](lifecycle-dimensions.md) | `entrymobilebeaconminor` |
| [종료 비콘 Minor](lifecycle-dimensions.md) | `exitmobilebeaconminor` |
| [시작 비콘 UUID](lifecycle-dimensions.md) | `entrymobilebeaconuuid` |
| [종료 비콘 UUID](lifecycle-dimensions.md) | `exitmobilebeaconuuid` |
| [시작 비콘 Proximity](lifecycle-dimensions.md) | `entrymobilebeaconproximity` |
| [종료 비콘 Proximity](lifecycle-dimensions.md) | `exitmobilebeaconproximity` |

### AMO (Adobe Advertising Cloud)

| 차원 이름 (Analytics UI에 표시됨) | 차원 ID (API 요청에 사용됨) |
|--- |--- |
| AMO EF ID | `amo_ef_id` |
| AMO ID | `amo_cid` |

### Activity Map

| 차원 이름 (Analytics UI에 표시됨) | 차원 ID (API 요청에 사용됨) |
|--- |--- |
| 지역별 [Activity Map 링크](activity-map-link-by-region.md) | `clickmaplinkbyregion` |
| [Activity Map 지역](activity-map-region.md) | `clickmapregion` |
| [Activity Map 링크](activity-map-link.md) | `clickmaplink` |
| [Activity Map 페이지](activity-map-page.md) | `clickmappage` |

### Nielsen 통합

이 통합을 구현하는 방법에 관한 자세한 내용은 Adobe Exchange에서 [Nielsen Extension](https://exchange.adobe.com/apps/ec/101361)을 참조하십시오.

| 차원 이름 (Analytics UI에 표시됨) | 차원 ID (API 요청에 사용됨) |
|--- |--- |
| Nielsen 광고 모델 | `nielsenadmodel` |
| Nielsen 세그먼트 C | `nielsensegmentc` |
| Nielsen 세그먼트 B | `nielsensegmentb` |
| Nielsen 세그먼트 A | `nielsensegmenta` |
| Nielsen 콘텐츠 ID | `nielsencontentid` |
| Nielsen 자산 / 프로그램 | `nielsenasset` |
| Nielsen VCID | `nielsenvcid` |
| Nielsen 옵트 아웃 | `nielsenoptout` |
| Nielsen 클라이언트 ID + VCID | `nielsenclientidvcid` |
| Nielsen 클라이언트 ID | `nielsenclientid` |
| 시작 Nielsen 옵트 아웃 | `entrynielsenoptout` |
| 종료 Nielsen 옵트 아웃 | `exitnielsenoptout` |
| 시작 Nielsen 클라이언트 ID + VCID | `entrynielsenclientidvcid` |
| 종료 Nielsen 클라이언트 ID + VCID | `exitnielsenclientidvcid` |
| 시작 Nielsen 클라이언트 ID | `entrynielsenclientid` |
| 종료 Nielsen 클라이언트 ID | `exitnielsenclientid` |

### AEM (Adobe Experience Manager)

| 차원 이름 (Analytics UI에 표시됨) | 차원 ID (API 요청에 사용됨) |
|--- |--- |
| 자산 ID | `aemassetid` |
| 자산 소스 | `aemassetsource` |
| 클릭한 자산 ID | `aemclickedassetid` |
| 시작 자산 ID | `entryaemassetid` |
| 종료 자산 ID | `exitaemassetid` |

### Adobe Campaign

| 차원 이름 (Analytics UI에 표시됨) | 차원 ID (API 요청에 사용됨) |
|--- |--- |
| Adobe Campaign 수행된 배달 ID | `ac_delivery_internal_name` |
