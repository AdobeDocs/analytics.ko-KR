---
description: 데이터 피드의 열을 설명하는 테이블 데이터
keywords: Data Feed;columns
subtopic: data feeds
title: 데이터 열 참조
topic: Reports and analytics
uuid: 9042a274-7124-4323-8cd6-5c84ab3eef6d
translation-type: tm+mt
source-git-commit: f3b227e7d2f239076f7c38abd42af6e1a86b0069
workflow-type: tm+mt
source-wordcount: '3403'
ht-degree: 79%

---


# 데이터 열 참조

이 페이지에서는 각 열에 포함된 데이터를 확인할 수 있습니다. 구현 대부분에서 모든 열을 사용하지는 않으므로 데이터 피드 내보내기에 포함할 열을 결정할 때 이 페이지를 참조할 수 있습니다.

>[!IMPORTANT]
>
>제공된 열(예: 255자로 정의된 열)에 대해 데이터 피드는 문자열의 값을 이스케이프 처리하는 문자 추가로 인해 추가 문자를 보낼 수 있습니다. 구현에서 문자 제한을 초과하는 값을 정기적으로 전송하는 경우 이러한 추가 문자를 염두에 두십시오.

## 열, 설명 및 데이터 유형

>[!NOTE]
>
>열 대부분은 `post_`라는 접두어가 있는 유사한 열을 포함합니다. 이후 열에는 서버 측 논리, 처리 규칙 및 VISTA 규칙 다음의 값이 있습니다. 대부분의 경우 이후 열을 사용하는 것이 좋습니다. 자세한 내용은 [데이터 피드 FAQ](../df-faq.md)를 참조하십시오.

| 열 이름 | 열 설명 | 데이터 유형 |
| --- | --- | --- |
| `accept_language` | 이미지 요청의 Accept-Language HTTP 헤더에 표시된 대로 모든 수락된 언어를 나열합니다. | char(20) |
| `aemassetid` | Adobe Experience Manager 자산 세트의 자산 ID(GUID)에 해당하는 다중 값 변수입니다. 노출 이벤트를 증가시킵니다. | text |
| `aemassetsource` | 자산 이벤트의 소스를 식별합니다. Adobe Experience Manager에서 사용됩니다. | varchar(255) |
| `aemclickedassetid` | Adobe Experience Manager 자산의 자산 ID입니다. 클릭 이벤트를 증가시킵니다. | varchar(255) |
| `browser` | 브라우저의 숫자 ID입니다. References the `browser.tsv` lookup table. | int 부호 없음 |
| `browser_height` | 브라우저 창의 높이(픽셀). | smallint 부호 없음 |
| `browser_width` | 브라우저 창의 폭(픽셀). | smallint 부호 없음 |
| `c_color` | 색 팔레트의 비트 깊이입니다. Used as part of calculating the [Color depth](/help/components/dimensions/color-depth.md) dimension. AppMeasurement는 JavaScript 함수를 사용합니다 `screen.colorDepth()`. | char(20) |
| `campaign` | Variable used in the [Tracking Code](/help/components/dimensions/tracking-code.md) dimension. | varchar(255) |
| `carrier` | Adobe Advertising Cloud 통합 변수입니다. 이동통신사를 지정합니다. References the `carrier` lookup table. | varchar(100) |
| `channel` | Variable used in the [Site sections](/help/components/dimensions/site-section.md) dimension. | varchar(100) |
| `click_action` | 더 이상 사용되지 않습니다. 이전 Clickmap 도구에서 클릭한 링크된 주소입니다. | varchar(100) |
| `click_action_type` | 더 이상 사용되지 않습니다. 이전 Clickmap 도구의 링크 유형입니다.<br>0: HREF URL<br>1: 사용자 지정 ID<br>2: JavaScript onClick 이벤트<br>3: 양식 요소 | tinyint 부호 없음 |
| `click_context` | 더 이상 사용되지 않습니다. 링크 클릭이 발생한 페이지 이름입니다. 이전 Clickmap 도구의 일부입니다. | varchar(255) |
| `click_context_type` | 더 이상 사용되지 않습니다. click_context에 설정된 페이지 이름이 있는지 또는 기본값이 페이지 URL로 설정되어 있는지 여부를 나타냅니다.<br>0: 페이지 URL<br>1: 페이지 이름 | tinyint 부호 없음 |
| `click_sourceid` | 더 이상 사용되지 않습니다. 클릭한 링크의 페이지에 있는 위치의 숫자 ID입니다. 이전 Clickmap 도구의 일부입니다. | int 부호 없음 |
| `click_tag` | 더 이상 사용되지 않습니다. 클릭한 HTML 요소의 유형입니다. | char(10) |
| `clickmaplink` | Activity Map 링크 | varchar(255) |
| `clickmaplinkbyregion` | 지역별 Activity Map 링크 | varchar(255) |
| `clickmappage` | Activity Map 페이지 | varchar(255) |
| `clickmapregion` | Activity Map 영역 | varchar(255) |
| `code_ver` | 이미지 요청을 컴파일하고 전송하는 데 사용되는 AppMeasurement 라이브러리 버전입니다. | char(16) |
| `color` | Color depth ID based on the value of the `c_color` column. References the `color_depth.tsv` lookup table. | smallint 부호 없음 |
| `connection_type` | 연결 유형을 나타내는 숫자 ID입니다. Variable used in the [Connection type](/help/components/dimensions/connection-type.md) dimension. References the `connection_type.tsv` lookup table. | tinyint 부호 없음 |
| `cookies` | Variable used in the [Cookie support](/help/components/dimensions/cookie-support.md) dimension.<br>Y: 활성화됨<br>N: 비활성화됨<br>U: 알 수 없음 | char(1) |
| `country` | 히트가 발생한 국가를 나타내는 숫자 ID입니다. Used in the [Countries](/help/components/dimensions/countries.md) dimension. 조회를 `country.tsv` 사용합니다. | smallint 부호 없음 |
| `ct_connect_type` | Related to the `connection_type` column. 가장 일반적인 값은 LAN/Wifi, 이동통신사 및 모뎀입니다. | char(20) |
| `curr_factor` | 통화 소수점 이하 자리 수를 결정하며 통화 전환에 사용됩니다. 예를 들어, USD는 소수점 이하 두 자리를 사용하므로 이 열 값은 2입니다. | tinyint |
| `curr_rate` | 거래가 발생했을 때 환율입니다. Adobe에서는 현재 날짜의 환율을 결정하기 위해 XE와 파트너 관계를 맺습니다. | decimal(24,12) |
| `currency` | 거래 중에 사용된 통화 코드입니다. | char(8) |
| `cust_hit_time_gmt` | 타임스탬프가 활성화된 보고서 세트 전용입니다. Unix 시간을 기반으로 한, 히트와 함께 전송된 타임스탬프입니다. | int |
| `cust_visid` | 사용자 지정 방문자 ID가 설정되면 이 열에 채워집니다. | varchar(255) |
| `daily_visitor` | 히트가 새 일일 방문자인지 판별하는 플래그입니다. | tinyint 부호 없음 |
| `date_time` | 보고서 세트의 시간대를 기반으로 한 읽을 수 있는 형식으로 된 히트 시간입니다. | datetime |
| `domain` | Variable used in the [Domain](/help/components/dimensions/domain.md) dimension. 방문자의 인터넷 액세스 지점을 기반으로 합니다. | varchar(100) |
| `duplicate_events` | 중복으로 카운트된 각 이벤트를 나열합니다. | varchar(255) |
| `duplicate_purchase` | 중복이라는 이유로 이 히트에 대한 구매 이벤트가 무시됨을 나타내는 플래그입니다. | tinyint 부호 없음 |
| `duplicated_from` | 히트 복사 VISTA 규칙을 포함하는 보고서 세트에서만 사용됩니다. 히트가 복사된 보고서 세트를 나타냅니다. | varchar(40) |
| `ef_id` | The `ef_id` used in Adobe Advertising Cloud integrations. | varchar(255) |
| `evar1 - evar250` | 사용자 지정 변수 1-250입니다. eVar [차원에](/help/components/dimensions/evar.md) 사용됩니다. 각 조직은 eVar을 다르게 사용합니다. 조직이 각 eVar을 채우는 방법에 대한 자세한 정보는 조직별 솔루션 설계 문서를 참조하십시오. | varchar(255) |
| `event_list` | 히트로 트리거된 이벤트를 나타내는 숫자 ID들을 쉼표로 구분한 목록입니다. 기본 이벤트와 사용자 지정 이벤트 1-1000을 모두 포함합니다. 조회를 `event.tsv` 사용합니다. | text |
| `exclude_hit` | 히트가 보고에서 제외되었음을 나타내는 플래그. The `visit_num` column is not incremented for excluded hits.<br>1: 사용되지 않음. 스크랩된 기능 일부입니다.<br>2: 사용되지 않음. 스크랩된 기능 일부입니다.<br>3: 더 이상 사용되지 않음. User agent exclusion<br>4: Exclusion based on IP address<br>5: Vital hit info missing, such as `page_url`, `pagename`, `page_event`, or `event_list`<br>6: JavaScript did not correctly process hit<br>7: Account-specific exclusion, such as in a VISTA rules<br>8: Not used. 대체 계정별 제외.<br>9: 사용되지 않음. 스크랩된 기능 일부입니다.<br>10: 잘못된 통화 코드<br>11: 타임스탬프 전용 보고서 세트에서 히트에 타임스탬프가 없거나 히트에 타임스탬프가 아닌 보고서 세트의 타임스탬프가 포함됨<br>12: 사용되지 않음. 스크랩된 기능 일부입니다.<br>13: 사용되지 않음. 스크랩된 기능 일부입니다.<br>14: Analytics 히트와 일치하지 않는 Target 히트<br>15: 현재 사용되지 않음.<br>16: Analytics 히트와 일치하지 않는 Advertising Cloud 히트 | tinyint 부호 없음 |
| `first_hit_page_url` | 방문자의 첫 번째 URL입니다. | varchar(255) |
| `first_hit_pagename` | Variable used in the [Entry page original](/help/components/dimensions/entry-dimensions.md) dimension. 방문자의 원래 시작 페이지 이름입니다. | varchar(100) |
| `first_hit_ref_domain` | Variable used in the [Original referring domain](/help/components/dimensions/original-referring-domain.md) dimension. 기준 `first_hit_referrer`. 방문자의 첫 번째 참조 도메인입니다. | varchar(100) |
| `first_hit_ref_type` | 방문자의 첫 번째 레퍼러 유형을 나타내는 숫자 ID입니다. 조회를 `referrer_type.tsv` 사용합니다. | tinyint 부호 없음 |
| `first_hit_referrer` | 방문자의 첫 번째 참조 URL입니다. | varchar(255) |
| `first_hit_time_gmt` | Unix 시간에서 방문자의 첫 번째 히트 타임스탬프입니다. | int |
| `geo_city` | IP를 기반으로 한, 히트가 발생한 시/군/구의 이름입니다. Used in the [Cities](/help/components/dimensions/cities.md) dimension. | char(32) |
| `geo_country` | IP를 기반으로 한, 히트가 발생한 국가의 약어입니다. | char(4) |
| `geo_dma` | IP를 기반으로 한, 히트가 발생한 인구 통계학적 영역의 숫자 ID입니다. 미국 [DMA 차원에](/help/components/dimensions/us-dma.md) 사용됩니다. | int 부호 없음 |
| `geo_region` | IP를 기반으로 한, 히트가 발생한 시/도 또는 지역의 이름입니다. Used in the [Regions](/help/components/dimensions/regions.md) dimension. | char(32) |
| `geo_zip` | IP를 기반으로 하며 히트가 발생한 지역의 우편 번호입니다. Zip 코드 [차원을 채우는 데](/help/components/dimensions/zip-code.md) 도움이 됩니다. See also `zip`. | varchar(16) |
| `hier1 - hier5` | 계층 변수에서 사용됩니다. 구분된 값 목록을 포함합니다. 구분 기호는 보고서 세트 설정에서 선택합니다. | varchar(255) |
| `hit_source` | 히트가 발생한 소스를 나타냅니다. 히트 소스 1, 2 및 6이 청구됩니다. <br>1:타임스탬프가 없는 표준 이미지 요청 <br>2:타임스탬프가 <br>3인 표준 이미지 요청:타임스탬프 <br>4를 사용한 라이브 데이터 소스 업로드:사용되지 않음 <br>5:범용 데이터 소스 업로드 <br>6:전체 처리 데이터 소스 업로드 <br>7:TransactionID 데이터 소스 업로드 <br>8:더 이상 사용되지 않음;Adobe Advertising Cloud 데이터 소스의 이전 버전 <br>9:더 이상 사용되지 않음;Adobe Social 요약 지표 <br>10:Audience Manager 서버측 전달이 사용됨 | tinyint 부호 없음 |
| `hit_time_gmt` | 히트 Adobe 데이터 수집 서버의 타임스탬프가 Unix 시간을 기준으로 히트를 받았습니다. | int |
| `hitid_high` | Used in combination with `hitid_low` to uniquely identify a hit. | bigint 부호 없음 |
| `hitid_low` | Used in combination with `hitid_high` to uniquely identify a hit. | bigint 부호 없음 |
| `homepage` | 더 이상 사용되지 않습니다. 현재 URL이 브라우저의 홈 페이지인지 여부를 나타냅니다. | char(1) |
| `hourly_visitor` | 히트가 새 시간별 방문자인지 판별하는 플래그입니다. | tinyint 부호 없음 |
| `ip` | 이미지 요청의 HTTP 헤더를 기반으로 한 IP 주소입니다. | char(20) |
| `ip2` | 사용되지 않습니다. IP 주소를 기반으로 하는 VISTA 규칙을 포함하는 보고서 세트용 백엔드 참조 변수입니다. | char(20) |
| `j_jscript` | 브라우저가 지원하는 JavaScript 버전입니다. | char(5) |
| `java_enabled` | Java가 사용되는지를 나타내는 플래그입니다. <br>Y: 활성화됨<br>N: 비활성화됨<br>U: 알 수 없음 | char(1) |
| `javascript` | Lookup ID of JavaScript version, based on `j_jscript`. 조회 테이블을 사용합니다. | tinyint 부호 없음 |
| `language` | 언어의 숫자 ID입니다. Uses `languages.tsv` lookup table. | smallint 부호 없음 |
| `last_hit_time_gmt` | 이전 히트의 타임스탬프(Unix 시간)입니다. Used to calculate the [Days since last visit](/help/components/dimensions/days-since-last-visit.md) dimension. | int |
| `last_purchase_num` | Variable used in the [Customer loyalty](/help/components/dimensions/customer-loyalty.md) dimension. 방문자가 이전에 구매한 횟수. <br>0: 이전 구매 없음(고객이 아님) <br>1: 1회 이전 구매(신규 고객) <br>2: 2회 이전 구매(재방문 고객) <br>3: 3회 이상 이전 구매(단골 고객) | int 부호 없음 |
| `last_purchase_time_gmt` | Used in the [Days since last purchase](/help/components/dimensions/days-since-last-purchase.md) dimension. 마지막으로 수행한 구매의 타임스탬프(Unix 시간)입니다. For first-time purchases and visitors that have not made a purchase before, this value is `0`. | int |
| `latlon1` | 위치(10km까지) | varchar(255) |
| `latlon23` | 위치(100m까지) | varchar(255) |
| `latlon45` | 위치(1m까지) | varchar(255) |
| `mc_audiences` | 방문자가 속한 Audience Manager 세그먼트 ID 목록입니다. | text |
| `mcvisid` | Experience Cloud 방문자 ID. 19자리에 채워진 두 개의 연결된 64비트 숫자로 구성된 128비트 숫자입니다. | varchar(255) |
| `mobile_id` | 사용자가 모바일 장치를 사용하는 경우 장치의 숫자 ID입니다. | int |
| `mobileaction` | 모바일 작업입니다. Automatically collected when `trackAction` is called in Mobile Services. 앱에서 경로를 지정하는 자동 작업을 허용합니다. | varchar(100) |
| `mobileappid` | 모바일 앱 ID입니다. 애플리케이션 이름과 버전을 다음 형식으로 저장: `[AppName] [BundleVersion]` | varchar(255) |
| `mobileappperformanceappid` | Apteligent Data Connector에서 사용됩니다. Apteligent에 사용되는 앱 ID입니다. | varchar(255) |
| `mobileappperformancecrashid` | Apteligent Data Connector에서 사용됩니다. Apteligent에 사용되는 충돌 ID입니다. | varchar(255) |
| `mobileappstoreobjectid` | Appfigures Data Connector에서 사용됩니다. 앱스토어 개체 ID. | varchar(255) |
| `mobilebeaconmajor` | Mobile Services 비콘 Major | varchar(100) |
| `mobilebeaconminor` | Mobile Services 비콘 Minor | varchar(100) |
| `mobilebeaconproximity` | Mobile Services 비콘 Proximity | varchar(255) |
| `mobilebeaconuuid` | Mobile Services 비콘 UUID | varchar(100) |
| `mobilecampaigncontent` | 링크를 표시한 콘텐츠의 이름 또는 ID입니다. 모바일 앱 획득을 통해 채워집니다. | varchar(255) |
| `mobilecampaignmedium` | 배너 또는 이메일과 같은 마케팅 매체입니다. 모바일 앱 획득을 통해 채워집니다. | varchar(255) |
| `mobilecampaignname` | 캠페인의 이름으로, 캠페인 변수에도 저장됩니다. 모바일 앱 획득을 통해 채워집니다. | varchar(255) |
| `mobilecampaignsource` | 뉴스레터 또는 소셜 미디어 네트워크와 같은 원본 레퍼러입니다. 모바일 앱 획득을 통해 채워집니다. | varchar(255) |
| `mobilecampaignterm` | 이 획득을 사용하여 추적하려는 유료 키워드 또는 기타 용어입니다. 모바일 앱 획득을 통해 채워집니다. | varchar(255) |
| `mobiledayofweek` | 앱을 시작한 요일의 수입니다. | varchar(255) |
| `mobiledayssincefirstuse` | 앱을 처음 실행한 이후 경과일 수입니다. | varchar(255) |
| `mobiledayssincelastupgrade` | 컨텍스트 데이터 변수 a.DaysSinceLastUpgrade에서 수집됩니다. 이전 세션 이후 경과된 일 수입니다. | varchar(255) |
| `mobiledayssincelastuse` | 앱을 마지막으로 실행한 이후 경과일 수입니다. | varchar(255) |
| `mobiledeeplinkid` | Collected from the context data variable `a.deeplink.id`. 모바일 획득 링크의 식별자로 획득 보고서에 사용됩니다. | varchar(255) |
| `mobiledevice` | 모바일 장치 이름입니다. iOS에서는 쉼표로 구분된 2자리 문자열로 저장됩니다. 첫 번째 숫자는 장치 생성을 나타내고 두 번째 숫자는 장치 제품군을 나타냅니다. | varchar(255) |
| `mobilehourofday` | 앱을 시작한 날의 시간을 정의합니다. 24시간 숫자 형식을 따릅니다. | varchar(255) |
| `mobileinstalldate` | 모바일 설치 날짜입니다. 사용자가 모바일 앱을 처음으로 여는 날짜를 제공합니다. | varchar(255) |
| `mobilelaunchessincelastupgrade` | 컨텍스트 데이터 변수 a.LaunchesSinceUpgrade에서 수집됩니다. 마지막 업그레이드 이후 시작 횟수를 보고합니다. | varchar(255) |
| `mobilelaunchnumber` | 모바일 앱을 시작할 때마다 1씩 증가합니다. | varchar(255) |
| `mobileltv` | 더 이상 사용되지 않습니다. trackLifetimeValue 메서드로 채워집니다. | varchar(255) |
| `mobilemessagebuttonname` | Collected from the context data variable `a.message.button.id`. 메시지를 닫은 단추를 식별하는 인앱 메시지에 사용됩니다. | varchar(100) |
| `mobilemessageid` | 인앱 메시지 ID | varchar(255) |
| `mobilemessageonline` | 인앱 메시지 온라인 | varchar(255) |
| `mobilemessagepushoptin` | Collected from the context data variable `a.push.optin`. 사용자가 푸시 메시지를 사용할 때 &quot;true&quot;로 설정됩니다. 그러지 않는 경우에는 값이 &quot;false&quot;입니다. | varchar(255) |
| `mobilemessagepushpayloadid` | Collected from the context data variable `a.push.payloadid`. 푸시 메시지에 페이로드 식별자로 사용됩니다. | varchar(255) |
| `mobileosenvironment` | Collected from the context data variable `a.OSEnvironment`. Android 또는 iOS와 같은 OS 환경을 명시합니다. | varchar(255) |
| `mobileosversion` | Mobile Services 운영 체제 버전 | varchar(255) |
| `mobileplaceaccuracy` | Collected from the context data variable `a.loc.acc`. 수집 시 GPS의 정확도를 미터 단위로 나타냅니다. | varchar(255) |
| `mobileplacecategory` | Collected from the context data variable `a.loc.category`. 특정 위치의 카테고리를 설명합니다. | varchar(255) |
| `mobileplaceid` | Collected from the context data variable `a.loc.id`. 지정된 관심 영역에 대한 식별자입니다. | varchar(255) |
| `mobilerelaunchcampaigncontent` | Mobile Services 실행 콘텐츠 | varchar(255) |
| `mobilerelaunchcampaignmedium` | Mobile Services 실행 미디어 | varchar(255) |
| `mobilerelaunchcampaignsource` | Mobile Services 실행 소스 | varchar(255) |
| `mobilerelaunchcampaignterm` | Mobile Services 실행 용어 | varchar(255) |
| `mobilerelaunchcampaigntrackingcode` | Collected from the context data variable `a.launch.campaign.trackingcode`. 실행 캠페인에 대한 추적 코드로 획득에 사용됩니다. | varchar(255) |
| `mobileresolution` | 모바일 장치의 해상도입니다. `[Width] x [Height]` 픽셀 단위. | varchar(255) |
| `monthly_visitor` | 방문자가 현재 월에 고유한지를 나타내는 플래그입니다. | tinyint 부호 없음 |
| `mvvar1` - `mvvar3` | 목록 변수 값입니다. 구현에 따라 구분된 사용자 지정 값 목록을 포함합니다. | text |
| `namespace` | 사용되지 않습니다. 스크랩된 기능 일부입니다. | varchar(50) |
| `new_visit` | 현재 히트가 새 방문인지를 판별하는 플래그입니다. 30분 동안 방문 활동이 없으면 Adobe 서버에 의해 설정됩니다. | tinyint 부호 없음 |
| `os` | 방문자의 운영 체제를 나타내는 숫자 ID입니다. Based on the `user_agent` column. 조회를 `os` 사용합니다. | int 부호 없음 |
| `p_plugins` | 더 이상 사용되지 않습니다. 브라우저에 사용할 수 있는 플러그인 목록. Used the JavaScript function `navigator.plugins()`. | text |
| `page_event` | 이미지 요청(표준 히트, 다운로드 링크, 사용자 지정 링크, 종료 링크)에서 전송된 히트 유형입니다. [페이지 이벤트 조회](datafeeds-page-event.md)를 참조하십시오. | tinyint 부호 없음 |
| `page_event_var1` | 링크 추적 이미지 요청에서만 사용됩니다. 클릭한 다운로드 링크, 종료 링크 또는 사용자 지정 링크의 URL입니다. | text |
| `page_event_var2` | 링크 추적 이미지 요청에서만 사용됩니다. 링크의 사용자 지정 이름(지정된 경우)입니다. | varchar(100) |
| `page_event_var3` | 더 이상 사용되지 않습니다. 포함된 설문 조사 및 미디어 모듈 데이터입니다. 이전 버전의 Adobe Analytics에서 이전 비디오 보고서를 채웠습니다. | text |
| `page_type` | Used to populate the [Pages not found](/help/components/dimensions/pages-not-found.md) dimension. Used exclusively for 404 pages. This variable should either be empty or contain the value `ErrorPage`. | char(20) |
| `page_url` | 히트의 URL입니다. 링크 추적 이미지 요청에서 제거됨. | varchar(255) |
| `pagename` | Used to populate the [Page](/help/components/dimensions/page.md) dimension. 변수가 [`pagename`](/help/implement/vars/page-vars/pagename.md) 비어 있으면 Analytics는 `page_url` 대신 사용합니다. | varchar(100) |
| `paid_search` | 히트가 유료 검색 발견과 일치하는 경우 설정되는 플래그입니다. | tinyint 부호 없음 |
| `partner_plugins` | 사용되지 않습니다. 스크랩된 기능 일부입니다. | varchar(255) |
| `persistent_cookie` | Used in the [Persistent cookie support](/help/components/dimensions/persistent-cookie-support.md) dimension. 방문자가 각 히트 후 삭제되지 않은 쿠키를 지원하는지 여부를 나타냅니다. | char(1) |
| `plugins` | 더 이상 사용되지 않습니다. 브라우저 내에서 사용할 수 있는 플러그인에 해당하는 숫자 ID의 목록입니다. 조회를 `plugins.tsv` 사용합니다. | varchar(180) |
| `pointofinterest` | Mobile Services 관심 영역 이름 | varchar(255) |
| `pointofinterestdistance` | Mobile Services 관심 영역 중앙까지의 거리 | varchar(255) |
| `post_` 열 | 보고서에서 최종적으로 사용되는 값을 포함합니다. 각 이후 열은 서버 측 논리, 처리 규칙 및 VISTA 규칙 다음에 채워집니다. 대부분의 경우 이후 열을 사용하는 것이 좋습니다. | 각각의 이후가 아닌 열을 참조하십시오. |
| `prev_page` | 사용되지 않습니다. 이전 페이지의 Adobe 독점 식별자입니다. | int 부호 없음 |
| `product_list` | Product list as passed in through the [`products`](/help/implement/vars/page-vars/products.md) variable. 제품은 쉼표로 구분되고, 개별 제품 속성은 세미콜론으로 구분됩니다. | text |
| `product_merchandising` | 사용되지 않습니다. 대신 `product_list`를 사용하십시오. | text |
| `prop1` - `prop75` | 사용자 지정 트래픽 변수 1 - 75. Prop [차원에](/help/components/dimensions/prop.md) 사용됩니다. | varchar(100) |
| `purchaseid` | Unique identifier for a purchase, as set using the [`purchaseID`](/help/implement/vars/page-vars/purchaseid.md) variable. Used by the `duplicate_purchase` column. | char(20) |
| `quarterly_visitor` | 히트가 새 분기별 방문자인지 판별하는 플래그입니다. | tinyint 부호 없음 |
| `ref_domain` | 레퍼러 열을 기반으로 합니다. 히트의 참조 도메인입니다. 참조 도메인 [차원에](/help/components/dimensions/referring-domain.md) 사용됩니다. | varchar(100) |
| `ref_type` | 히트에 대한 참조 유형을 나타내는 숫자 ID입니다. Used in the [Referrer type](/help/components/dimensions/referrer-type.md) dimension. <br>1: 사이트 내부<br>2: 기타 웹 사이트 <br>3: 검색 엔진 <br>4: 하드 드라이브 <br>5: USENET <br>6: 입력/책갈피 표시(레퍼러 없음) <br>7: 이메일 <br>8: JavaScript 없음 <br>9: 소셜 네트워크 | tinyint 부호 없음 |
| `referrer` | 이전 페이지의 페이지 URL입니다. Used in the [Referrer](/help/components/dimensions/referrer.md) dimension. `referrer`에서 varchar(255)의 데이터 유형을 사용하는 동안 `post_referrer`에서는 varchar(244)의 데이터 유형을 사용합니다. | varchar(255) |
| `resolution` | 모니터의 해상도를 나타내는 숫자 ID입니다. Used in the [Monitor resolution](/help/components/dimensions/monitor-resolution.md) dimension. Uses `resolution.tsv` lookup table. | smallint 부호 없음 |
| `s_kwcid` | Adobe Advertising Cloud 통합에 사용되는 키워드 ID입니다. | varchar(255) |
| `s_resolution` | Raw 화면 해상도 값입니다. JavaScript 함수를 사용하여 수집됩니다 `screen.width x screen.height`. | char(20) |
| `sampled_hit` | 더 이상 사용되지 않습니다. Ad Hoc Analysis에서 이전에 샘플링에 사용되었습니다. | char(1) |
| `search_engine` | 방문자에게 사이트를 참조하도록 하는 검색 엔진을 나타내는 숫자 ID입니다. 조회를 `search_engines.tsv` 사용합니다. | smallint 부호 없음 |
| `search_page_num` | Used by the [All Search Page Rank](/help/components/dimensions/all-search-page-rank.md) dimension. 사용자가 사이트에 클릭스루하기 전에 사이트가 표시된 검색 결과 페이지를 나타냅니다. | smallint 부호 없음 |
| `secondary_hit` | 보조 히트를 추적하는 플래그입니다. 일반적으로 히트를 복사하는 다중 세트 태깅 및 VISTA 규칙에서 발생합니다. | tinyint 부호 없음 |
| `service` | 사용되지 않습니다. 대신 `page_event`를 사용하십시오. | char(2) |
| `socialaccountandappids` | 더 이상 사용되지 않습니다. 소셜 계정 및 앱 ID | varchar(255) |
| `socialassettrackingcode` | 더 이상 사용되지 않습니다. 소셜 캠페인 변수 | varchar(255) |
| `socialauthor` | 더 이상 사용되지 않습니다. 소셜 작성자 변수 | varchar(255) |
| `socialcontentprovider` | 더 이상 사용되지 않습니다. 소셜 플랫폼/속성 | varchar(255) |
| `socialinteractiontype` | 더 이상 사용되지 않습니다. 소셜 상호 작용 유형 | varchar(255) |
| `sociallanguage` | 더 이상 사용되지 않습니다. 소셜 언어 | varchar(255) |
| `sociallatlong` | 더 이상 사용되지 않습니다. 소셜 위도/경도 | varchar(255) |
| `socialowneddefinitioninsighttype` | 더 이상 사용되지 않습니다. 소셜이 소유한 정의 통찰력 유형 | varchar(255) |
| `socialowneddefinitioninsightvalue` | 더 이상 사용되지 않습니다. 소셜이 소유한 정의 통찰력 값 | varchar(255) |
| `socialowneddefinitionmetric` | 더 이상 사용되지 않습니다. 소셜이 소유한 정의 지표 | varchar(255) |
| `socialowneddefinitionpropertyvspost` | 더 이상 사용되지 않습니다. 소셜이 소유한 정의 속성 대 게시 | varchar(255) |
| `socialownedpostids` | 더 이상 사용되지 않습니다. 소셜이 소유한 게시물 ID | varchar(255) |
| `socialownedpropertyid` | 더 이상 사용되지 않습니다. 소셜이 소유한 속성 ID | varchar(255) |
| `socialownedpropertyname` | 더 이상 사용되지 않습니다. 소셜이 소유한 속성 이름 | varchar(255) |
| `socialownedpropertypropertyvsapp` | 더 이상 사용되지 않습니다. 소셜이 소유한 속성 이름 대 앱 | varchar(255) |
| `state` | 상태 변수입니다. | varchar(50) |
| `stats_server` | 사용하지 않습니다. 히트를 처리한 Adobe 내부 서버입니다. | char(30) |
| `t_time_info` | 방문자의 로컬 시간입니다. 형식: `M/D/YYYY HH:MM:SS Month (0-11, 0=January) Timezone offset (in minutes)` | varchar(100) |
| `tnt` | Adobe Target 통합에서 사용됩니다. | text |
| `tnt_action` | Adobe Target 통합에서 사용됩니다. | text |
| `tnt_post_vista` | 더 이상 사용되지 않습니다. 대신 `post_tnt`를 사용하십시오. | text |
| `transactionid` | 데이터 소스를 통해 나중에 다양한 데이터 포인트를 업로드할 수 있는 고유 식별자입니다. 변수를 사용하여 [`transactionID`](/help/implement/vars/page-vars/transactionid.md) 수집됩니다. | text |
| `truncated_hit` | 이미지 요청이 잘렸음을 나타내는 플래그입니다. 부분 히트가 수신되었음을 나타냅니다. <br>Y: 히트가 잘림, 일부 히트 수신 <br>N: 히트가 잘리지 않음, 전체 히트 수신 | char(1) |
| `ua_color` | 더 이상 사용되지 않습니다. 이전에는 색상 깊이에 대한 대체 항목으로 사용되었습니다. | char(20) |
| `ua_os` | 더 이상 사용되지 않습니다. 이전에는 운영 체제에 대한 대체 항목으로 사용되었습니다. | char(80) |
| `ua_pixels` | 더 이상 사용되지 않습니다. 이전에는 브라우저 높이와 너비에 대한 대체 항목으로 사용되었습니다. | char(20) |
| `user_agent` | 이미지 요청의 HTTP 헤더에서 전송된 사용자 에이전트 문자열입니다. | text |
| `user_hash` | 사용하지 않습니다. 보고서 세트 ID의 해시. 대신 `username`를 사용하십시오. | int 부호 없음 |
| `user_server` | Used in the [Server](/help/components/dimensions/server.md) dimension. | varchar(100) |
| `userid` | 사용하지 않습니다. 보고서 세트 ID의 숫자 ID입니다. 대신 `username`를 사용하십시오. | int 부호 없음 |
| `username` | 히트에 대한 보고서 세트 ID. | char(40) |
| `va_closer_detail` | Variable used in the [Last touch detail](/help/components/dimensions/last-touch-detail.md) dimension. | varchar(255) |
| `va_closer_id` | Numeric ID that identifies the [Last touch channel](/help/components/dimensions/last-touch-channel.md) dimension. 이 ID에 대한 조회는 마케팅 채널 관리자에서 찾을 수 있습니다. | tinyint 부호 없음 |
| `va_finder_detail` | Variable used in the [First touch detail](/help/components/dimensions/first-touch-detail.md) dimension. | varchar(255) |
| `va_finder_id` | Numeric ID that identifies the [First touch channel](/help/components/dimensions/first-touch-channel.md) dimension. 이 ID에 대한 조회는 마케팅 채널 관리자에서 찾을 수 있습니다. | tinyint 부호 없음 |
| `va_instance_event` | Flag to identify Marketing Channel [Instances](/help/components/metrics/instances.md). | tinyint 부호 없음 |
| `va_new_engagement` | Flag to identify Marketing Channel [New engagements](/help/components/metrics/new-engagements.md). | tinyint 부호 없음 |
| `video` | 비디오 콘텐츠 | varchar(255) |
| `videoad` | 비디오 광고 이름 | varchar(255) |
| `videoadinpod` | Pod 위치의 비디오 광고 | varchar(255) |
| `videoadlength` | 비디오 광고 길이 | varchar(255) |
| `videoadload` | 비디오 광고 로드 | varchar(255) |
| `videoadname` | 비디오 광고 이름 | varchar(255) |
| `videoadplayername` | 비디오 광고 플레이어 이름 | varchar(255) |
| `videoadpod` | 비디오 광고 Pod | varchar(255) |
| `videoadvertiser` | 비디오 광고주 | varchar(255) |
| `videoaudioalbum` | 비디오 오디오 앨범 | varchar(255) |
| `videoaudioartist` | 비디오 오디오 아티스트 | varchar(255) |
| `videoaudioauthor` | 비디오 오디오 작성자 | varchar(255) |
| `videoaudiolabel` | 비디오 오디오 레이블 | varchar(255) |
| `videoaudiopublisher` | 비디오 오디오 게시자 | varchar(255) |
| `videoaudiostation` | 비디오 오디오 스테이션 | varchar(255) |
| `videocampaign` | 비디오 캠페인 | varchar(255) |
| `videochannel` | 비디오 채널 | varchar(255) |
| `videochapter` | 비디오 챕터 이름 | varchar(255) |
| `videocontenttype` | 동영상 콘텐츠 유형. 모든 비디오 보기에 대해 자동으로 &#39;비디오&#39;로 설정됩니다. | varchar(255) |
| `videodaypart` | 동영상 방송 시간대 | varchar(255) |
| `videoepisode` | 비디오 에피소드 | varchar(255) |
| `videofeedtype` | 비디오 피드 유형 | varchar(255) |
| `videogenre` | 비디오 장르 | text |
| `videolength` | 비디오 길이 | varchar(255) |
| `videomvpd` | 비디오 MVPD | varchar(255) |
| `videoname` | 비디오 이름 | varchar(255) |
| `videonetwork` | 비디오 네트워크 | varchar(255) |
| `videopath` | 비디오 경로 | varchar(100) |
| `videoplayername` | 비디오 플레이어 이름 | varchar(255) |
| `videoqoebitrateaverageevar` | 비디오 품질 평균 비트 전송률 | varchar(255) |
| `videoqoebitratechangecountevar` | 비디오 품질 변경 카운트 | varchar(255) |
| `videoqoebuffercountevar` | 비디오 품질 버퍼 카운트 | varchar(255) |
| `videoqoebuffertimeevar` | 비디오 품질 버퍼 시간 | varchar(255) |
| `videoqoedroppedframecountevar` | 비디오 품질 드롭된 프레임 카운트 | varchar(255) |
| `videoqoeerrorcountevar` | 비디오 품질 오류 카운트 | varchar(255) |
| `videoqoeextneralerrors` | 비디오 품질 외부 오류 | text |
| `videoqoeplayersdkerrors` | 비디오 품질 SDK 오류 | text |
| `videoqoetimetostartevar` | 비디오 품질 시작할 시간 | varchar(255) |
| `videoseason` | 비디오 시즌 | varchar(255) |
| `videosegment` | 비디오 세그먼트 | varchar(255) |
| `videoshow` | 비디오 표시 | varchar(255) |
| `videoshowtype` | 비디오 표시 유형 | varchar(255) |
| `videostreamtype` | 비디오 스트림 유형 | varchar(255) |
| `visid_high` | Used in combination with `visid_low` to uniquely identify a visitor. | bigint 부호 없음 |
| `visid_low` | Used in combination with `visid_high` to uniquely identify a visitor. | bigint 부호 없음 |
| `visid_new` | 히트에 새로 생성된 방문자 ID가 있는지 여부를 식별하는 플래그입니다. | char(1) |
| `visid_timestamp` | 방문자 ID가 새로 생성된 경우 방문자 ID가 생성된 시간의 타임스탬프(Unix 시간)를 제공합니다. | int |
| `visid_type` | 외부용이 아닙니다. Adobe가 최적화 처리를 위해 내부적으로 사용합니다. 방문자를 식별하는 데 사용된 방법을 나타내는 숫자 ID입니다.<br>0:사용자 지정 visitorID 또는 알 수 없음/해당<br>없음 1:IP 및 사용자 에이전트 폴백 <br>2:HTTP 모바일 구독자 헤더 <br>3:기존 쿠키 값(`s_vi`) <br>4:폴백 쿠키 값(`s_fid`) <br>5:ID 서비스 | tinyint 부호 없음 |
| `visit_keywords` | Variable used in the [Search keyword](/help/components/dimensions/search-keyword.md) dimension. 이 열은 Adobe에서 사용하는 백엔드 로직을 수용하기 위해 비표준 문자 한계인 varchar(244)를 사용합니다. | varchar(244) |
| `visit_num` | Variable used in the [Visit number](/help/components/dimensions/visit-number.md) dimension. 1에서 시작하여 새 방문이 방문자별로 시작될 때마다 증가합니다. | int 부호 없음 |
| `visit_page_num` | Variable used in the [Hit depth](/help/components/dimensions/hit-depth.md) dimension. 사용자가 생성하는 각 히트에 대해 1씩 증가합니다. 각 방문을 재설정합니다. | int 부호 없음 |
| `visit_ref_domain` | Based on the `visit_referrer` column. 방문의 첫 번째 참조 도메인입니다. | varchar(100) |
| `visit_ref_type` | 방문자의 첫 번째 레퍼러 유형을 나타내는 숫자 ID입니다. Uses the `referrer_type.tsv` lookup table. | tinyint 부호 없음 |
| `visit_referrer` | 방문의 첫 번째 레퍼러입니다. | varchar(255) |
| `visit_search_engine` | 방문의 첫 번째 검색 엔진에 대한 숫자 ID입니다. 조회를 `search_engines.tsv` 사용합니다. | smallint 부호 없음 |
| `visit_start_page_url` | 방문의 첫 번째 URL입니다. | varchar(255) |
| `visit_start_pagename` | 방문의 첫 번째 페이지 이름입니다. | varchar(100) |
| `visit_start_time_gmt` | 방문의 첫 번째 히트 타임스탬프(Unix 시간)입니다. | int |
| `weekly_visitor` | 히트가 새 주별 방문자인지 판별하는 플래그입니다. | tinyint 부호 없음 |
| `yearly_visitor` | 히트가 새 연별 방문자인지 판별하는 플래그입니다. | tinyint 부호 없음 |
| `zip` | Zip 코드 [차원을 채우는 데](/help/components/dimensions/zip-code.md) 도움이 됩니다. See also `geo_zip`. | varchar(50) |

## 빈 열

다음 열 목록은 사용되지 않으며 데이터를 포함하지 않습니다.

* `mobileacquisitionclicks`
* `mobileactioninapptime`
* `mobileactiontotaltime`
* `mobileappperformanceaffectedusers`
* `mobileappperformanceappid.app-perf-app-name`
* `mobileappperformanceappid.app-perf-platform`
* `mobileappperformancecrashes`
* `mobileappperformancecrashid.app-perf-crash-name`
* `mobileappperformanceloads`
* `mobileappstoreavgrating`
* `mobileappstoredownloads`
* `mobileappstoreinapprevenue`
* `mobileappstoreinapproyalties`
* `mobileappstoreobjectid.app-store-user`
* `mobileappstoreobjectid.application-name`
* `mobileappstoreobjectid.application-version`
* `mobileappstoreobjectid.appstore-name`
* `mobileappstoreobjectid.category-name`
* `mobileappstoreobjectid.country-name`
* `mobileappstoreobjectid.device-manufacturer`
* `mobileappstoreobjectid.device-name`
* `mobileappstoreobjectid.in-app-name`
* `mobileappstoreobjectid.platform-name-version`
* `mobileappstoreobjectid.rank-category-type`
* `mobileappstoreobjectid.region-name`
* `mobileappstoreobjectid.review-comment`
* `mobileappstoreobjectid.review-title`
* `mobileappstoreoneoffrevenue`
* `mobileappstoreoneoffroyalties`
* `mobileappstorepurchases`
* `mobileappstorerank`
* `mobileappstorerankdivisor`
* `mobileappstorerating`
* `mobileappstoreratingdivisor`
* `mobileavgprevsessionlength`
* `mobilecrashes`
* `mobilecrashrate`
* `mobiledailyengagedusers`
* `mobiledeeplinkid.name`
* `mobileinstalls`
* `mobilelaunches`
* `mobileltvtotal`
* `mobilemessageclicks`
* `mobilemessageid.dest`
* `mobilemessageid.name`
* `mobilemessageid.type`
* `mobilemessageimpressions`
* `mobilemessagepushpayloadid.name`
* `mobilemessageviews`
* `mobilemonthlyengagedusers`
* `mobileplacedwelltime`
* `mobileplaceentry`
* `mobileplaceexit`
* `mobileprevsessionlength`
* `mobilerelaunchcampaigntrackingcode.name`
* `mobileupgrades`
* `socialaveragesentiment`
* `socialaveragesentiment (deprecated)`
* `socialfbstories`
* `socialfbstorytellers`
* `socialinteractioncount`
* `sociallikeadds`
* `sociallink`
* `sociallink (deprecated)`
* `socialmentions`
* `socialpageviews`
* `socialpostviews`
* `socialproperty`
* `socialproperty (deprecated)`
* `socialpubcomments`
* `socialpubposts`
* `socialpubrecommends`
* `socialpubsubscribers`
* `socialterm`
* `socialtermslist`
* `socialtermslist (deprecated)`
* `socialtotalsentiment`
* `sourceid`
* `videoauthorized`
* `videoaverageminuteaudience`
* `videochaptercomplete`
* `videochapterstart`
* `videochaptertime`
* `videopause`
* `videopausecount`
* `videopausetime`
* `videoplay`
* `videoprogress10`
* `videoprogress25`
* `videoprogress50`
* `videoprogress75`
* `videoprogress96`
* `videoqoebitrateaverage`
* `videoqoebitratechange`
* `videoqoebuffer`
* `videoqoedropbeforestart`
* `videoqoedroppedframes`
* `videoqoeerror`
* `videoresume`
* `videototaltime`
* `videouniquetimeplayed`
