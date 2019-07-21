---
title: Analytics 차원 호환성
seo-title: 분석 작업 공간, 보고서 및 분석 또는 둘 다와 호환되는 Analytics 차원 및 보고서.
description: Reference for Analytics Dimensions and Reports.
seo-description: 분석 작업 공간 차원, 보고 및 분석 차원, 차원, R & A 차원, 작업 공간 차원
translation-type: tm+mt
source-git-commit: e3b1ac3139f26ca3a97f3d2228276e690ec4cb79

---


# Analytics 차원 호환성

이 참조 문서에는 보고서 및 분석 및 분석 작업 공간에서, 분석 작업 공간에서만, 그리고 보고 및 분석에서만 지원되는 차원/보고서가 나열됩니다.

다음을 염두에 두십시오.

* 이러한 목록은 전체 목록이 아닙니다. 각 보고서 세트에는 지정된 제품 변수 집합이 활성화되어 있을 수도 있고 그렇지 않을 수도 있습니다. 또한 제공된 보고서 세트에 여러 사용자 지정 변수가 활성화 또는 비활성화되어 있거나 제품 변수에 매핑되어 있을 수 있습니다. 또한 방문자 속성 및 분류는 각 보고서 세트에만 해당하므로 제외했습니다.

* There are some cases of overlap, where Analytics tools use different terms for what is essentially the same thing, for example: `browserwidth` and `browserwidthbucketed`.

## Reports &amp; Analytics와 Analysis Workspace에서 모두 지원되는 차원

| 차원 이름 (Analytics UI에서 표시) | 차원 ID(API 요청에 사용됨) |
|---|---|
| 타겟 분석 | targetraw |
| 대상 ID | mcaudiences |
| 브라우저 | browser |
| 브라우저 유형 | browsertype |
| 카테고리 | category |
| 시 | geocity |
| 색상 깊이 | colordepth |
| 연결 유형 | connectiontype |
| 쿠키 지원 | cookie |
| 국가 | geocountry |
| 고객 충성도 | customerloyalty |
| 사용자 지정 전환 변수 | Evar 1, evar 2 등 |
| 사용자 지정 인사이트 변수 | prop 1, prop 2 등 |
| 사용자 지정 링크 | customlink |
| 첫 구매까지 소요된 일 수 | daysbeforefirstpurchase |
| 마지막 구매 이후 일 수 | dayssincelastpurchase |
| 도메인 | filtereddomain |
| 다운로드 링크 | downloadlink |
| 시작 페이지 | entrypage |
| 시작 페이지 원본 | entrypageoriginal |
| 종료 링크 | exitlink |
| 첫 번째 터치 채널 | firsttouchchannel |
| 첫 번째 터치 채널 세부 사항 | firsttouchchanneldetail |
| Java 활성화 | javaenabled |
| 언어 | language |
| 마지막 터치 채널 | lasttouchchannel |
| 마지막 터치 채널 세부 사항 | lasttouchchanneldetail |
| 목록 변수 | listvariables |
| 마케팅 채널 | marketingchannel |
| 모바일 오디오 지원 | mobileaudiosupport |
| 모바일 통신사 | mobilecarrier |
| 모바일 색상 깊이 | mobilecolordepth |
| 모바일 쿠키 지원 | mobilecookiesupport |
| 모바일 장치 | mobiledevicename |
| 모바일 장치 유형 | mobiledevicetype |
| 모바일 최대 이메일 길이 | mobileemaillength |
| 모바일 이미지 지원 | mobileimagesupport |
| 모바일 제조업체 | mobilemanufacturer |
| 모바일 운영 체제(더 이상 사용되지 않음) | mobileos |
| 모바일 화면 높이 | mobilescreenheight |
| 모바일 화면 크기 | mobilescreensize |
| 모바일 화면 너비 | mobilescreenwidth |
| 모바일 최대 브라우저 URL 길이 | mobileurllength |
| 모바일 비디오 지원 | mobilevideosupport |
| 모니터 해상도 | monitorresolution |
| 운영 체제 | operatingsystem |
| 최초 참조 도메인 | referringdomainoriginal |
| 페이지 | page |
| 페이지를 찾을 수 없음 | pagesnotfound |
| 제품 | product |
| 레퍼러 | referrer |
| 레퍼러 유형 | referrertype |
| 조회 도메인 | referringdomain |
| 지역 | georegion |
| 재방문 주기 | returnfrequency |
| SC-TnT | tntbase |
| 검색 엔진 | searchengine |
| 검색 키워드 | searchenginekeyword |
| 검색 엔진 - 자연어 | searchenginenatural |
| 검색 엔진 - 유료 | searchenginepaid |
| 검색 키워드 - 자연어 | searchenginenaturalkeyword |
| 검색 키워드 - 유료 | searchenginepaidkeyword |
| 모든 검색 페이지 등급 | searchenginepagerank |
| 서버 | server |
| 단일 페이지 방문 횟수 | singlepagevisits |
| 사이트 섹션 | sitesections |
| 방문당 체류 시간 - 세부기간 | sitetime |
| 추적 코드 | campaign |
| 미국 DMA | geodma |
| 미국 주 | state |
| 이벤트까지 남은 시간 | timeprior |
| 방문당 체류 시간 - 그룹화됨 | timespent |
| 방문 깊이 | pathlength |
| 방문 횟수 | visitnumber |
| 우편번호 | zip |

## Analysis Workspace에서만 지원되는 차원

| 차원 이름 (Analytics UI에서 표시) | 차원 ID(API 요청에 사용됨) |
|--- |--- |
| 오전/오후 | timepartampm |
| 브라우저 높이 - Bucketed | browserheightbucketed |
| 브라우저 너비 - Bucketed | browserwidthbucketed |
| 일 | daterangeday |
| 날짜 | timepartdayofmonth |
| 요일 | dayofweek |
| 요일 | timepartdayofweek |
| 일(한 해 기준) | timepartdayofyear |
| 마지막 방문 이후의 일수 | dayssincelastvisit |
| 시작 사용자 지정 인사이트 | entryprops |
| 시작 목록 변수 | entrylistvariables |
| 시작 서버 | entryserver |
| 시작 사이트 섹션 | entrysitesections |
| 종료 사용자 지정 인사이트 | exitprops |
| 종료 목록 변수 | exitlistvariables |
| 종료 페이지 | exitpage |
| 종료 서버 | exitserver |
| 종료 사이트 섹션 | exitsitesections |
| 히트 깊이 | hitdepth |
| 조회 유형 | hittype |
| 시간 | daterangehour |
| 시간 | timeparthourofday |
| 마케팅 채널 세부 사항 | marketingchanneldetail |
| 분 | daterangeminute |
| 모바일 최대 책갈피 길이 | mobilebookmarklength |
| 모바일 장치 번호 | mobiledevicenumber |
| 모바일 DRM | mobiledrm |
| 모바일 정보 서비스 | mobileinformationservices |
| 모바일 Java VM | mobilejavavm |
| 모바일 메일 데코레이션 | mobilemaildecoration |
| 모바일 네트 프로토콜 | mobilenetprotocols |
| 모바일 Push To Talk | mobilepushtotalk |
| 월 | daterangemonth |
| 월 | timepartmonthofyear |
| 운영 체제 유형 | operatingsystemgroup |
| 유료 검색 | paidsearch |
| 영구적 쿠키 지원 | persistentcookie |
| 분기 | daterangequarter |
| 사분기 | timepartquarterofyear |
| 설문 조사 | surveybase |
| 페이지 체류 시간 - 버킷 지정됨 | averagepagetime |
| 페이지 체류 시간 - 세부기간 | pagetimeseconds |
| 옵트아웃 이유 추적 중 | optoutreason |
| 평일/주말 | timepartweekdayweekend |
| 주 | daterangeweek |
| 년 | daterangeyear |

## Analysis Workspace에서만 지원되는 컨텐츠 인식 차원

| 차원 이름 (Analytics UI에서 표시) | 차원 ID(API 요청에 사용됨) |
|--- |--- |
| Activity Map XY | clickmapxy |
| 미디어 세션 ID | videosessionid |
| Nielsen 액세스 방법 | nielsenaccmethod |
| Nielsen 앱 ID | nielsenappid |
| Channel 채널 자산 | nielsenchannelasset |
| Nielsen 컨텐츠 유형 | nielsencontenttype |

## Reports &amp; Analytics에서만 지원되는 차원

| 차원 이름 (Analytics UI에서 표시) | 차원 ID(API 요청에 사용됨) |
|--- |--- |
| 브라우저 높이 | browserheight |
| 브라우저 너비 | browserwidth |
| 일별 고유 고객 수 | dailyuniquecustomers |
| JavaScript | javascriptsupport |
| JavaScript 버전 | javascriptversion |
| 월간 고유 고객 수 | monthlyuniquecustomers |
| 분기별 고유 고객 수 | quarterlyuniquecustomers |
| 시간대 | timezone |
| 최상위 수준 도메인 | topleveldomain |
| 방문자 주 | legacystate |
| 주간 고유 고객 수 | weeklyuniquecustomers |
| 연간 고유 고객 수 | yearlyuniquecustomers |

## Reports &amp; Analytics에 사전 구성된 보고서

Reports &amp; Analytics에는 특정 차원에 매핑되지 않는 여러 개의 사전 구성된 보고서가 포함되어 있거나 보고서에 차원 클래스가 사용됩니다. 이러한 보고서가 아래에 나열되어 있습니다.

* 책갈피 URL 길이
* 브라우저
* 브라우저 유형
* 캠페인 전환 단계
* 장바구니 전환 단계
* 시
* 페이지 클릭 수
* 국가
* 크로스셀
* 사용자 지정 이벤트 단계
* 데코레이션 메일 지원
* 장치 번호 전송(온/오프)
* 도메인
* DRM
* 시작 페이지
* 종료 페이지
* 폴아웃
* 전체 경로
* ICities
* 정보 서비스
* Java 버전
* 언어
* 최장 경로
* 미디어 Concurrent Viewer
* 미디어 방송 시간대
* 미디어 세부 사항
* 미디어 개요
* 모니터 해상도
* 네트 프로토콜
* Netscape 플러그인
* 다음 페이지
* 다음 페이지 흐름
* 운영 체제
* 운영 체제 유형
* 페이지 깊이
* 페이지 요약
* 경로 탐색
* 이전 페이지 흐름
* 이전 페이지
* PTT
* 제품 전환 단계
* 구매 전환 단계
* 참조 도메인
* 지역
* 다시 로드
* 검색 엔진 - 모두
* 검색 엔진 - 자연어
* 검색 엔진 - 유료
* 검색 키워드 - 모두
* 검색 키워드 - 자연어
* 검색 키워드 - 유료
* Target 활동 세부 사항
* 페이지에서 보낸 시간
* 시간대
* 최상위 수준 도메인
* 미국 DMA
* 미국 주(州)
* 방문 횟수
* 방문자 홈 페이지

## Reports &amp; Analytics와 Analysis Workspace에서 모두 지원되는 컨텐츠 인식 차원

### 비디오(Media Analytics)

| 차원 이름 (Analytics UI에서 표시) | 차원 ID(API 요청에 사용됨) |
|--- |--- |
| 컨텐츠 | video |
| 컨텐츠 세그먼트 | videosegment |
| 컨텐츠 유형 | videocontenttype |
| 광고 플레이어 이름 | videoadplayername |
| Pod의 광고 위치 | videoadinpod |
| 드롭된 프레임 | videoqoedroppedframecountevar |
| 오류 | videoqoeerrorcountevar |
| 평균 비트율 | videoqoebitrateaverageevar |
| 비트율 변경 | videoqoebitratechangecountevar |
| 총 버퍼 지속 시간 | videoqoebuffertimeevar |
| 버퍼 이벤트 | videoqoebuffercountevar |
| 시작 시간 | videoqoetimetostartevar |
| 광고 Pod | videoadpod |
| 미디어 경로 | videopath |
| 광고 | videoad |
| 컨텐츠 플레이어 이름 | videoplayername |
| 컨텐츠 채널 | videochannel |
| 챕터 | videochapter |
| 컨텐츠 이름(변수) | videoname |
| 컨텐츠 길이(변수) | videolength |
| 광고 이름(변수) | videoadname |
| 광고 길이(변수) | videoadlength |
| 표시 | videoshow |
| 시즌 | videoseason |
| 에피소드 | videoepisode |
| 네트워크 | videonetwork |
| 표시 유형 | videoshowtype |
| 광고 로드 | videoadload |
| MVPD | videomvpd |
| 방송 시간대 | videodaypart |
| 광고주 | videoadadvertiser |
| 캠페인 ID | videoadcampaign |
| 장르 | videogenre |
| 스트림 유형 | videostreamtype |
| 플레이어 SDK 오류 ID | videoqoeplayersdkerrors |
| 외부 오류 ID | videoqoeextneralerrors |
| 미디어 피드 유형 | videofeedtype |
| 시작 미디어 경로 | entryvideopath |
| 종료 미디어 경로 | exitvideopath |
| 시작 장르 | entryvideogenre |
| 종료 장르 | exitvideogenre |
| 시작 플레이어 SDK 오류 ID | entryvideoqoeplayersdkerrors |
| 종료 플레이어 SDK 오류 ID | exitvideoqoeplayersdkerrors |
| 시작 외부 오류 ID | entryvideoqoeextneralerrors |
| 종료 외부 오류 ID | exitvideoqoeextneralerrors |

### Adobe Social

| 차원 이름 (Analytics UI에서 표시) | 차원 ID(API 요청에 사용됨) |
|--- |--- |
| 용어 | socialterm |
| 소셜 플랫폼/속성 | socialcontentprovider |
| 작성자 | socialauthor |
| 언어 | sociallanguage |
| 위도/경도 | sociallatlong |
| 자산 추적 코드 | socialassettrackingcode |
| 소유한 소셜 속성 | socialaccountandappids |
| 소유한 게시 ID | socialownedpostids |
| 소유한 소셜 정의 | socialinteractiontype |
| 소유한 속성 ID | socialownedpropertyid |
| 소유한 속성과 애플리케이션 비교 | socialownedpropertypropertyvsapp |
| 소유한 속성 이름 | socialownedpropertyname |
| 소유한 정의 속성과 게시 비교 | socialowneddefinitionpropertyvspost |
| 소유한 정의 인사이트 유형 | socialowneddefinitioninsighttype |
| 소유한 정의 인사이트 값 | socialowneddefinitioninsightvalue |
| 소유된 정의 지표 | socialowneddefinitionmetric |
| 자산 | socialmediaid |

### Mobile SDK

| 차원 이름 (Analytics UI에서 표시) | 차원 ID(API 요청에 사용됨) |
|--- |--- |
| 첫 번째 실행 날짜 | mobileinstalldate |
| 앱 ID | mobileappid |
| 시작 번호 | mobilelaunchnumber |
| 최초 사용 이후 일 수 | mobiledayssincefirstuse |
| 마지막 사용 이후 일 수 | mobiledayssincelastuse |
| 시간(SDK) | mobilehourofday |
| 요일(SDK) | mobiledayofweek |
| 운영 체제(SDK) | mobileosenvironment |
| 마지막 업그레이드 이후 일 수 | mobiledayssincelastupgrade |
| 마지막 업그레이드 이후 출시 | mobilelaunchessincelastupgrade |
| 장치 이름(SDK) | mobiledevice |
| 운영 체제 버전(SDK) | mobileosversion |
| 비콘 Major | mobilebeaconmajor |
| 비콘 Minor | mobilebeaconminor |
| 비콘 UUID | mobilebeaconuuid |
| 비콘 Proximity | mobilebeaconproximity |
| 위치(10km까지) | latlon1 |
| 위치(100m까지) | latlon23 |
| 위치(1m까지) | latlon45 |
| 관심 영역 이름 | pointofinterest |
| 관심 영역 중앙까지의 거리 | pointofinterestdistance |
| 위치 정확성 | mobileplaceaccuracy |
| 장소 카테고리 | mobileplacecategory |
| 장소 ID | mobileplaceid |
| 시작 비콘 Major | entrymobilebeaconmajor |
| 종료 비콘 Major | exitmobilebeaconmajor |
| 시작 비콘 Minor | entrymobilebeaconminor |
| 종료 비콘 Minor | exitmobilebeaconminor |
| 시작 비콘 UUID | entrymobilebeaconuuid |
| 종료 비콘 UUID | exitmobilebeaconuuid |
| 시작 비콘 Proximity | entrymobilebeaconproximity |
| 종료 비콘 Proximity | exitmobilebeaconproximity |

### Adobe Advertising Cloud (AMO)

| 차원 이름 (Analytics UI에서 표시) | 차원 ID(API 요청에 사용됨) |
|--- |--- |
| AMO EF ID | amo_ef_id |
| AMO ID | amo_cid |

### Activity Map

| 차원 이름 (Analytics UI에서 표시) | 차원 ID(API 요청에 사용됨) |
|--- |--- |
| 지역별 Activity Map 링크 | clickmaplinkbyregion |
| Activity Map 영역 | clickmapregion |
| Activity Map 링크 | clickmaplink |
| Activity Map 페이지 | clickmappage |

### Nielsen 통합

이 통합을 구현하는 방법에 관한 자세한 내용은 [Nielsen 파트너 관계](https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/hbvideo/nielsen-partnership.html)를 참조하십시오.

| 차원 이름 (Analytics UI에서 표시) | 차원 ID(API 요청에 사용됨) |
|--- |--- |
| Nielsen 광고 모델 | nielsenadmodel |
| Nielsen 세그먼트 C | nielsensegmentc |
| Nielsen 세그먼트 B | nielsensegmentb |
| Nielsen 세그먼트 A | nielsensegmenta |
| Nielsen 컨텐츠 ID | nielsencontentid |
| Nielsen 자산/프로그램 | nielsenasset |
| Nielsen VCID | nielsenvcid |
| Nielsen 옵트 아웃 | nielsenoptout |
| Nielsen 클라이언트 ID + VCID | nielsenclientidvcid |
| Nielsen 클라이언트 ID | nielsenclientid |
| 시작 Nielsen 옵트 아웃 | entrynielsenoptout |
| 종료 Nielsen 옵트 아웃 | exitnielsenoptout |
| 시작 Nielsen 클라이언트 ID + VCID | entrynielsenclientidvcid |
| 종료 Nielsen 클라이언트 ID + VCID | exitnielsenclientidvcid |
| 시작 Nielsen 클라이언트 ID | entrynielsenclientid |
| 종료 Nielsen 클라이언트 ID | exitnielsenclientid |

### AEM(Adobe Experience Manager)

| 차원 이름 (Analytics UI에서 표시) | 차원 ID(API 요청에 사용됨) |
|--- |--- |
| 자산 ID | aemassetid |
| 자산 소스 | aemassetsource |
| 클릭한 자산 ID | aemclickedassetid |
| 시작 자산 ID | entryaemassetid |
| 종료 자산 ID | exitaemassetid |

### Adobe Campaign

| 차원 이름 (Analytics UI에서 표시) | 차원 ID(API 요청에 사용됨) |
|--- |--- |
| Adobe Campaign 수행된 배달 ID | ac_delivery_internal_name |
