---
description: 데이터 피드의 열을 설명하는 테이블 데이터
keywords: 데이터 피드; 열
seo-description: 데이터 피드의 열을 설명하는 테이블 데이터
seo-title: 데이터 열 참조
solution: Analytics
subtopic: 데이터 피드
title: 데이터 열 참조
topic: Reports & Analytics
uuid: 9042 A 274-7124-4323-8 CD 6-5 C 84 AB 3 EEF 6 D
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# 데이터 열 참조

이 페이지를 사용하여 각 열에 포함된 데이터를 알아봅니다. 대부분의 구현은 모든 열을 사용하지 않으므로 데이터 피드 내보내기에 포함할 열을 결정할 때 이 페이지를 참조할 수 있습니다.

> [!IMPORTANT] 지정된 열 (예: 255 자로 정의된 열) 의 경우, 문자열에서 값을 이스케이프 이스케이프 처리하는 문자가 추가되므로 데이터 피드가 추가 문자를 보낼 수 있습니다. 구현에서 문자 제한을 초과하는 값을 정기적으로 전송하는 경우 이 항목을 염두에 두십시오.

## 열, 설명 및 데이터 유형

> [!NOTE] 대부분의 열에는 접두사가 있는 비슷한 열이 포함되어 `post_`있습니다. 이후 열에는 서버 측 논리, 처리 규칙 및 VISTA 규칙 다음의 값이 있습니다. 대부분의 경우 이후 열을 사용하는 것이 좋습니다.

| 열 이름 | 열 설명 | 데이터 유형 |
| --- | --- | --- |
| accept_language | 이미지 요청의 Accept-Language HTTP 헤더에 표시된 대로 모든 수락된 언어를 나열합니다. | char(20) |
| aemassetid | Adobe Experience Manager 자산 세트의 자산 ID(GUID)에 해당하는 다중 값 변수입니다. 노출 이벤트를 증가시킵니다. | text |
| aemassetsource | 자산 이벤트의 소스를 식별합니다. Adobe Experience Manager에서 사용됩니다. | varchar(255) |
| aemclickedassetid | Adobe Experience Manager 자산의 자산 ID입니다. 클릭 이벤트를 증가시킵니다. | varchar(255) |
| browser | 브라우저의 숫자 ID입니다. browser.tsv 조회 테이블을 참조합니다. | 부호 없는 int |
| browser_height | 브라우저 창의 높이(픽셀). | Smallint 부호 없음 |
| browser_width | 브라우저 창의 폭(픽셀). | Smallint 부호 없음 |
| c_color | 색 팔레트의 비트 깊이입니다. 색상 깊이 차원 계산의 일부로 사용됩니다. JavaScript 함수 screen.colorDepth()를 사용합니다. | char(20) |
| campaign | 추적 코드 차원에 사용되는 변수입니다. | varchar(255) |
| carrier | Adobe Advertising Cloud 통합 변수입니다. 이동통신사를 지정합니다. 통신사 조회 테이블을 참조합니다. | varchar(100) |
| channel | 사이트 섹션 차원에 사용되는 변수입니다. | varchar(100) |
| click_action | 더 이상 사용되지 않습니다. 이전 Clickmap 도구에서 클릭한 링크된 주소입니다. | varchar(100) |
| click_action_type | 더 이상 사용되지 않습니다. 이전 Clickmap 도구의 링크 유형입니다.<br>0: HREF URL<br>1: 사용자 정의 ID<br>2: JavaScript onclick event<br>3: 양식 요소 | tinyint 부호 없음 |
| click_context | 더 이상 사용되지 않습니다. 링크 클릭이 발생한 페이지 이름입니다. 이전 Clickmap 도구의 일부입니다. | varchar(255) |
| click_context_type | 더 이상 사용되지 않습니다. click_context에 설정된 페이지 이름이 있는지 또는 기본값이 페이지 URL로 설정되어 있는지 여부를 나타냅니다.<br>0: 페이지 URL<br>1: 페이지 이름 | tinyint 부호 없음 |
| click_sourceid | 더 이상 사용되지 않습니다. 클릭한 링크의 페이지에 있는 위치의 숫자 ID입니다. 이전 Clickmap 도구의 일부입니다. | 부호 없는 int |
| click_tag | 더 이상 사용되지 않습니다. 클릭한 HTML 요소의 유형입니다. | char(10) |
| clickmaplink | Activity Map 링크 | varchar(255) |
| clickmaplinkbyregion | 지역별 Activity Map 링크 | varchar(255) |
| clickmappage | Activity Map 페이지 | varchar(255) |
| clickmapregion | Activity Map 영역 | varchar(255) |
| code_ver | 이미지 요청을 컴파일하고 전송하는 데 사용되는 AppMeasurement 라이브러리 버전입니다. | char(16) |
| color | c_color 열의 값을 기반으로 하는 색상 깊이 ID입니다. color_depth.tsv 조회 테이블을 참조합니다. | Smallint 부호 없음 |
| connection_type | 연결 유형을 나타내는 숫자 ID입니다. 연결 유형 차원에 사용되는 변수입니다. connection_type.tsv 조회 테이블을 참조합니다. | tinyint 부호 없음 |
| cookies | 쿠키 지원 차원에 사용되는 변수입니다.<br>Y: Enabledn<br>: Disabledu<br>: 알 수 없음 | char(1) |
| country | 히트가 발생한 국가를 나타내는 숫자 ID입니다. Adobe에서는 IP 주소를 국가에 일치시키기 위해 Digital Envoy와 파트너 관계를 맺습니다. country.tsv 조회를 사용합니다. | Smallint 부호 없음 |
| ct_connect_type | connection_type 열과 관련이 있습니다. 가장 일반적인 값은 LAN/Wifi, 이동통신사 및 모뎀입니다. | char(20) |
| curr_factor | 통화 소수점 이하 자리 수를 결정하며 통화 전환에 사용됩니다. 예를 들어, USD는 소수점 이하 두 자리를 사용하므로 이 열 값은 2입니다. | tinyint |
| curr_rate | 거래가 발생했을 때 환율입니다. Adobe에서는 현재 날짜의 환율을 결정하기 위해 XE와 파트너 관계를 맺습니다. | decimal(24,12) |
| currency | 거래 중에 사용된 통화 코드입니다. | char(8) |
| cust_hit_time_gmt | 타임스탬프가 활성화된 보고서 세트 전용입니다. Unix 시간을 기반으로 한, 히트와 함께 전송된 타임스탬프입니다. | int |
| cust_visid | 사용자 지정 방문자 ID가 설정되면 이 열에 채워집니다. | varchar(255) |
| daily_visitor | 히트가 새 일일 방문자인지 판별하는 플래그입니다. | tinyint 부호 없음 |
| date_time | 보고서 세트의 시간대를 기반으로 한 읽을 수 있는 형식으로 된 히트 시간입니다. | datetime |
| domain | 도메인 차원에 사용되는 변수입니다. 사용자의 인터넷 서비스 제공자(ISP)를 기반으로 합니다. | varchar(100) |
| duplicate_events | 중복으로 카운트된 각 이벤트를 나열합니다. | varchar(255) |
| duplicate_purchase | 중복이라는 이유로 이 히트에 대한 구매 이벤트가 무시됨을 나타내는 플래그입니다. | tinyint 부호 없음 |
| duplicated_from | 히트 복사 VISTA 규칙을 포함하는 보고서 세트에서만 사용됩니다. 히트가 복사된 보고서 세트를 나타냅니다. | varchar(40) |
| ef_id | Adobe Advertising Cloud 통합에 사용되는 ef_id입니다. | varchar(255) |
| evar1-evar250 | 사용자 지정 변수 1-250입니다. 각 조직은 eVar을 다르게 사용합니다. 조직이 각 eVar을 채우는 방법에 대한 자세한 정보는 조직별 솔루션 설계 문서를 참조하십시오. | varchar(255) |
| event_list | 히트로 트리거된 이벤트를 나타내는 숫자 ID들을 쉼표로 구분한 목록입니다. 기본 이벤트와 사용자 지정 이벤트 1-1000을 모두 포함합니다. event.tsv 조회를 사용합니다. | text |
| exclude_hit | 히트가 보고에서 제외됨을 나타내는 플래그입니다. visit_ num 열은 제외된 히트에 대해 증가하지 않습니다.<br>1: 사용되지 않음. 스크랩된 기능의 일부<br>2: 사용되지 않음. 스크랩된 기능의 일부<br>3: 더 이상 사용되지 않습니다. User agent exclusion<br>4: Exclusion based on IP address<br>5: Vital hit info missing, such as page_url, pagename, page_event, or event_list<br>6: JavaScript did not correctly process hit<br>7: Account-specific exclusion, such as in a VISTA rules<br>8: Not used. 대체 계정별 제외.<br>9: 사용되지 않음. 스크랩된 기능의 일부<br>10: 잘못된 통화 코드<br>11: 타임스탬프가 타임스탬프 전용 보고서 세트에 없거나 타임스탬프에 타임스탬프가 아닌 보고서 세트<br>12에 타임스탬프가 들어 있는 경우: 사용되지 않음. 스크랩된 기능의 일부<br>13: 사용되지 않음. 스크랩된 기능의 일부<br>14: Analytics 히트<br>15와 일치하지 않는 타겟 히트: 현재 사용되지 않습니다.<br>16: Analytics 히트 수와 일치하지 않는 Advertising Cloud 히트 | tinyint 부호 없음 |
| first_hit_page_url | 방문자의 첫 번째 URL입니다. | varchar(255) |
| first_hit_pagename | 원래 시작 페이지 차원에 사용되는 변수입니다. 방문자의 원래 시작 페이지 이름입니다. | varchar(100) |
| first_hit_ref_domain | 최초 참조 도메인 차원에 사용되는 변수입니다. first_hit_referrer를 기반으로 합니다. 방문자의 첫 번째 참조 도메인입니다. | varchar(100) |
| first_hit_ref_type | 방문자의 첫 번째 레퍼러 유형을 나타내는 숫자 ID입니다. referrer_type.tsv 조회를 사용합니다. | tinyint 부호 없음 |
| first_hit_referrer | 방문자의 첫 번째 참조 URL입니다. | varchar(255) |
| first_hit_time_gmt | Unix 시간에서 방문자의 첫 번째 히트 타임스탬프입니다. | int |
| geo_city | IP를 기반으로 한, 히트가 발생한 시/군/구의 이름입니다. Adobe에서는 IP 주소를 시에 일치시키기 위해 Digital Envoy와 파트너 관계를 맺습니다. | char(32) |
| geo_country | IP를 기반으로 한, 히트가 발생한 국가의 약어입니다. Adobe에서는 IP 주소를 국가에 일치시키기 위해 Digital Envoy와 파트너 관계를 맺습니다. | char(4) |
| geo_dma | IP를 기반으로 한, 히트가 발생한 인구 통계학적 영역의 숫자 ID입니다. Adobe에서는 IP 주소를 인구 통계학적 영역에 일치시키기 위해 Digital Envoy와 파트너 관계를 맺습니다. | 부호 없는 int |
| geo_region | IP를 기반으로 한, 히트가 발생한 시/도 또는 지역의 이름입니다. Adobe에서는 IP 주소를 시/도 또는 지역에 일치시키기 위해 Digital Envoy와 파트너 관계를 맺습니다. | char(32) |
| geo_zip | 히트가 발생한 우편번호에 IP를 기반으로 합니다. Adobe에서는 IP 주소를 우편 번호에 일치시키기 위해 Digital Envoy와 파트너 관계를 맺습니다. | varchar(16) |
| hier1 - hier5 | 계층 변수에서 사용됩니다. 구분된 값 목록을 포함합니다. 구분 기호는 보고서 세트 설정에서 선택합니다. | varchar(255) |
| hit_source | 히트가 발생한 소스를 나타냅니다. <br>1: 타임스탬프 <br>2 없이 표준 이미지 요청: 타임스탬프 <br>3 이 있는 표준 이미지 요청: 타임스탬프 <br>4를 사용한 라이브 데이터 소스 업로드: 사용되지 <br>않음 5: 범용 데이터 소스 업로드 <br>6: 전체 처리 데이터 소스 업로드 <br>7: Transactionid 데이터 소스 업로드 <br>8: 더 이상 사용되지 않음; Adobe Advertising Cloud Data Sources <br>9의 이전 버전: 더 이상 사용되지 않음; Adobe Social 요약 지표 | tinyint 부호 없음 |
| hit_time_gmt | 히트 Adobe 데이터 수집 서버의 타임스탬프가 Unix 시간에 따라 히트를 받았습니다. | int |
| hitid_high | 히트를 고유하게 식별하기 위해 hitid_low와 함께 사용됩니다. | bigint unsigned |
| hitid_low | 히트를 고유하게 식별하기 위해 hitid_high와 함께 사용됩니다. | bigint unsigned |
| homepage | 더 이상 사용되지 않습니다. 현재 URL이 브라우저의 홈 페이지인지 여부를 나타냅니다. | char(1) |
| hourly_visitor | 히트가 새 시간별 방문자인지 판별하는 플래그입니다. | tinyint 부호 없음 |
| ip | 이미지 요청의 HTTP 헤더를 기반으로 한 IP 주소입니다. | char(20) |
| ip2 | 사용되지 않습니다. IP 주소를 기반으로 하는 VISTA 규칙을 포함하는 보고서 세트용 백엔드 참조 변수입니다. | char(20) |
| j_jscript | 브라우저가 지원하는 JavaScript 버전입니다. | char(5) |
| java_enabled | Java가 사용되는지 여부를 나타내는 플래그입니다. <br>Y: 활성화된 <br>N: Disabled <br>U: 알 수 없음 | char(1) |
| javascript | j_jscript를 기반으로 하는 JavaScript 버전의 조회 ID입니다. 조회 테이블을 사용합니다. | tinyint 부호 없음 |
| language | 언어의 숫자 ID입니다. languages.tsv 조회 테이블을 사용합니다. | Smallint 부호 없음 |
| last_hit_time_gmt | 이전 히트의 타임스탬프(Unix 시간)입니다. 마지막 방문 이후의 일수 차원을 계산하는 데 사용됩니다. | int |
| last_purchase_num | 고객 충성도 차원에 사용되는 변수입니다. 방문자가 수행한 이전 구매 횟수를 나타냅니다. <br>0: 이전 구매 없음 (고객 아님) <br>1: 1 이전 구매 (신규 고객) <br>2: 2 이전 구매 (재방문 고객) <br>3: 3 개 이상의 이전 구매 (단골 고객) | 부호 없는 int |
| last_purchase_time_gmt | 마지막 구매 이후 일 수 차원에 사용됩니다. 마지막으로 수행한 구매의 타임스탬프(Unix 시간)입니다. 이전에 구입한 적이 없는 최초 구매 및 방문자의 경우 이 값은 0입니다. | int |
| latlon1 | 위치(10km까지) | varchar(255) |
| latlon23 | 위치(100m까지) | varchar(255) |
| latlon45 | 위치(1m까지) | varchar(255) |
| mc_audiences | 방문자가 속한 Audience Manager 세그먼트 ID 목록입니다. | text |
| mcvisid | Experience Cloud 방문자 ID. 19자리에 채워진 두 개의 연결된 64비트 숫자로 구성된 128비트 숫자입니다. | varchar(255) |
| mobile_id | 사용자가 모바일 장치를 사용하는 경우 장치의 숫자 ID 입니다. | int |
| mobileaction | 모바일 작업입니다. Trackaction 이 Mobile Services에서 호출될 때 자동으로 수집됩니다. 앱에서 경로를 지정하는 자동 작업을 허용합니다. | varchar(100) |
| mobileappid | 모바일 앱 ID입니다. 애플리케이션 이름과 버전을 다음 형식으로 저장:[Appname] [bundleversion] | varchar(255) |
| mobileappperformanceappid | Apteligent 데이터 커넥터에 사용됩니다. Apteligent에서 사용되는 앱 ID. | varchar(255) |
| mobileappperformancecrashid | Apteligent 데이터 커넥터에 사용됩니다. Apteligent에 사용된 충돌 ID. | varchar(255) |
| mobileappstoreobjectid | Appfigures 데이터 커넥터에 사용됩니다. 앱스토어 개체 ID | varchar(255) |
| mobilebeaconmajor | Mobile Services 비콘 주요 | varchar(100) |
| mobilebeaconminor | Mobile Services Beacon Minor | varchar(100) |
| mobilebeaconproximity | 모바일 서비스 비콘 근접 | varchar(255) |
| mobilebeaconuuid | Mobile Services 비콘 UUID | varchar(100) |
| mobilecampaigncontent | 링크를 표시한 콘텐츠의 이름 또는 ID입니다. 모바일 앱 획득을 통해 채워집니다. | varchar(255) |
| mobilecampaignmedium | 배너 또는 이메일과 같은 마케팅 매체입니다. 모바일 앱 획득을 통해 채워집니다. | varchar(255) |
| mobilecampaignname | 캠페인의 이름으로, 캠페인 변수에도 저장됩니다. 모바일 앱 획득을 통해 채워집니다. | varchar(255) |
| mobilecampaignsource | 뉴스레터 또는 소셜 미디어 네트워크와 같은 원본 레퍼러입니다. 모바일 앱 획득을 통해 채워집니다. | varchar(255) |
| mobilecampaignterm | 이 획득을 사용하여 추적하려는 유료 키워드 또는 기타 용어입니다. 모바일 앱 획득을 통해 채워집니다. | varchar(255) |
| mobiledayofweek | 앱을 시작한 요일의 수입니다. | varchar(255) |
| mobiledayssincefirstuse | 앱을 처음 실행한 이후 경과일 수입니다. | varchar(255) |
| mobiledayssincelastupgrade | 컨텍스트 데이터 변수 a. dayssincelastupgrade에서 수집되었습니다. 이전 세션 이후 경과된 일 수입니다. | varchar(255) |
| mobiledayssincelastuse | 앱을 마지막으로 실행한 이후 경과일 수입니다. | varchar(255) |
| mobiledeeplinkid | Collected from the context data variable a.<span>deeplink</span>.id. 획득 보고서에 모바일 획득 링크의 식별자로 사용됩니다. | varchar(255) |
| mobiledevice | 모바일 장치 이름입니다. iOS에서는 쉼표로 구분된 2자리 문자열로 저장됩니다. 첫 번째 숫자는 장치 생성을 나타내고 두 번째 숫자는 장치 제품군을 나타냅니다. | varchar(255) |
| mobilehourofday | 앱을 시작한 날의 시간을 정의합니다. 24시간 숫자 형식을 따릅니다. | varchar(255) |
| mobileinstalldate | 모바일 설치 날짜입니다. 사용자가 모바일 앱을 처음으로 여는 날짜를 제공합니다. | varchar(255) |
| mobilelaunchessincelastupgrade | 컨텍스트 데이터 변수 a. launchessinceupgrade에서 수집되었습니다. 마지막 업그레이드한 이후의 시작 횟수를 보고합니다. | varchar(255) |
| mobilelaunchnumber | 모바일 앱을 시작할 때마다 1씩 증가합니다. | varchar(255) |
| mobileltv | 더 이상 사용되지 않습니다. trackLifetimeValue 메서드로 채워집니다. | varchar(255) |
| Mobilemessagebuttonname | Collected from the context data variable a.<span>message</span>.button.id. In-App 메시지에 사용되어 메시지를 닫은 단추를 식별합니다. | varchar(100) |
| mobilemessageid | 인앱 메시지 ID | varchar(255) |
| mobilemessageonline | 인앱 메시지 온라인 | varchar(255) |
| mobilemessagepushoptin | 컨텍스트 데이터 변수 a. push. optin에서 수집되었습니다. 사용자가 푸시 메시지를 옵트인할 때 "true" 로 설정합니다. 그렇지 않으면 값이 "false" 입니다. | varchar(255) |
| Mobilemessagepushpayloadid | 컨텍스트 데이터 변수 a. push. payloadid에서 수집되었습니다. 페이로드 식별자로 푸시 메시지에 사용됩니다. | varchar(255) |
| mobileosenvironment | 컨텍스트 데이터 변수 a. osenvironment에서 수집됩니다. Android 또는 iOS와 같은 상태 OS 환경 | varchar(255) |
| mobileosversion | Mobile Services 운영 체제 버전 | varchar(255) |
| mobileplaceaccuracy | 컨텍스트 데이터 변수 a. loc. acc에서 수집됩니다. 수집 시 GPS의 정확도를 미터 단위로 나타냅니다. | varchar(255) |
| mobileplacecategory | 컨텍스트 데이터 변수 a. loc. category에서 수집됨. 특정 장소의 카테고리에 대해 설명합니다. | varchar(255) |
| mobileplaceid | Collected from the context data variable a.<span>loc</span>.id. 주어진 관심 영역에 대한 식별자입니다. | varchar(255) |
| Mobilerelaunchcampaigncontent | Mobile Services 시작 컨텐츠 | varchar(255) |
| mobilerelaunchcampaignmedium | Mobile Services 시작 매체 | varchar(255) |
| mobilerelaunchcampaignsource | Mobile Services 시작 소스 | varchar(255) |
| mobilerelaunchcampaignterm | Mobile Services 시작 기간 | varchar(255) |
| Mobilerelaunchcampaigntrackingcode | 컨텍스트 데이터 변수 a. launch. campaign. trackingcode에서 수집되었습니다. 획득 캠페인의 추적 코드로 획득에서 사용됨. | varchar(255) |
| mobileresolution | 모바일 장치의 해상도입니다. 너비 x 높이(픽셀)입니다. | varchar(255) |
| monthly_visitor | 방문자가 현재 월에 고유한지를 나타내는 플래그입니다. | tinyint 부호 없음 |
| mvvar 1 - mvvar 3 | 목록 변수 값입니다. 구현에 따라 구분된 사용자 지정 값 목록을 포함합니다. | text |
| namespace | 사용되지 않습니다. 수년 전에 폐기한 기능의 일부입니다. | varchar(50) |
| new_visit | 현재 히트가 새 방문인지를 판별하는 플래그입니다. 30분 동안 방문 활동이 없으면 Adobe 서버에 의해 설정됩니다. | tinyint 부호 없음 |
| os | 방문자의 운영 체제를 나타내는 숫자 ID입니다. user_agent 열을 기반으로 합니다. os 조회를 사용합니다. | 부호 없는 int |
| p_plugins | 더 이상 사용되지 않습니다. 브라우저에 사용할 수 있는 플러그인 목록. JavaScript 함수 navigator.plugins()를 사용합니다. | text |
| page_event | 이미지 요청(표준 히트, 다운로드 링크, 사용자 지정 링크, 종료 링크)에서 전송된 히트 유형입니다. | tinyint 부호 없음 |
| page_event_var1 | 링크 추적 이미지 요청에서만 사용됩니다. 클릭한 다운로드 링크, 종료 링크 또는 사용자 지정 링크의 URL입니다. | text |
| page_event_var2 | 링크 추적 이미지 요청에서만 사용됩니다. 링크의 사용자 지정 이름(지정된 경우)입니다. | varchar(100) |
| page_event_var3 | 더 이상 사용되지 않습니다. 포함된 설문 조사 및 미디어 모듈 데이터입니다. 이전 버전의 Adobe Analytics에서 이전 비디오 보고서를 채웠습니다. | text |
| page_type | 404 페이지에만 사용되는 페이지를 찾을 수 없음 차원을 채우는 데 사용됩니다. 이 변수는 비어 있거나 "ErrorPage"를 포함해야 합니다. | char(20) |
| page_url | 히트의 URL입니다. 링크 추적 이미지 요청에서 사용되지 않습니다. | varchar(255) |
| pagename | 페이지 차원을 채우는 데 사용됩니다. 페이지 이름 변수가 비어 있으면 Analytics에서는 page_url을 대신 사용합니다. | varchar(100) |
| paid_search | 히트가 유료 검색 발견과 일치하는 경우 설정되는 플래그입니다. | tinyint 부호 없음 |
| partner_plugins | 사용되지 않습니다. 수년 전에 폐기한 기능의 일부입니다. | varchar(255) |
| persistent_cookie | 영구적 쿠키 지원 차원에 사용됩니다. 방문자가 각 히트 후 삭제되지 않은 쿠키를 지원하는지 여부를 나타냅니다. | char(1) |
| plugins | 더 이상 사용되지 않습니다. 브라우저 내에서 사용할 수 있는 플러그인에 해당하는 숫자 ID의 목록입니다. plugins.tsv 조회를 사용합니다. | varchar(180) |
| pointofinterest | Mobile Services 관심 영역 이름 | varchar(255) |
| pointofinterestdistance | 관심 영역 중앙까지의 모바일 서비스 거리 | varchar(255) |
| post_ columns | 보고서에서 최종적으로 사용되는 값을 포함합니다. 각 이후 열은 서버 측 논리, 처리 규칙 및 VISTA 규칙 다음에 채워집니다. 대부분의 경우 이후 열을 사용하는 것이 좋습니다. | 각각의 이후가 아닌 열을 참조하십시오. |
| prev_page | 사용되지 않습니다. 이전 페이지의 Adobe 소유 ID입니다. | 부호 없는 int |
| product_list | 제품 변수를 통해 전달될 때의 제품 목록입니다. 제품은 쉼표로 구분되고, 개별 제품 속성은 세미콜론으로 구분됩니다. | text |
| product_merchandising | 사용되지 않습니다. 대신 product_list를 사용하십시오. | text |
| prop1 - prop75 | 사용자 지정 트래픽 변수 1 - 75. | varchar(100) |
| purchaseid | s_purchaseID 변수를 사용하여 설정되는 구매의 고유 식별자입니다. duplicate_purchase 열에서 사용됩니다. | char(20) |
| quarterly_visitor | 히트가 새 분기별 방문자인지 판별하는 플래그입니다. | tinyint 부호 없음 |
| ref_domain | 레퍼러 열을 기반으로 합니다. 히트의 참조 도메인입니다. | varchar(100) |
| ref_type | 히트에 대한 참조 유형을 나타내는 숫자 ID입니다.<br>1: 사이트<br>2 내: 기타 웹 사이트 <br>3: 검색 엔진 <br>4: 하드 드라이브 <br>5: USENET <br>6: 입력/책갈피 표시 (레퍼러 없음) <br>7: 이메일 <br>8: JavaScript <br>9 없음: 소셜 네트워크 | tinyint 부호 없음 |
| referrer | 이전 페이지의 페이지 URL입니다. | varchar(255) |
| resolution | 모니터의 해상도를 나타내는 숫자 ID입니다. 모니터 해상도 차원을 채웁니다. resolution.tsv 조회 테이블을 사용합니다. | Smallint 부호 없음 |
| s_kwcid | Adobe Advertising Cloud 통합에서 사용되는 키워드 ID. | varchar(255) |
| s_resolution | Raw 화면 해상도 값입니다. JavaScript 함수 screen.width x screen.height를 사용하여 수집합니다. | char(20) |
| sampled_hit | 더 이상 사용되지 않습니다. Ad Hoc Analysis에서 이전에 샘플링에 사용되었습니다. | char(1) |
| search_engine | 방문자에게 사이트를 참조하도록 하는 검색 엔진을 나타내는 숫자 ID입니다. search_engines.tsv 조회를 사용합니다. | Smallint 부호 없음 |
| search_page_num | 모든 검색 페이지 등급 차원에 사용됩니다. 사용자가 사이트에 클릭스루하기 전에 사이트가 표시된 검색 결과 페이지를 나타냅니다. | Smallint 부호 없음 |
| secondary_hit | 보조 히트를 추적하는 플래그입니다. 일반적으로 히트 수를 복사하는 다중 세트 태그 및 VISTA 규칙에서 시작됩니다. | tinyint 부호 없음 |
| service | 사용되지 않습니다. 대신 page_event를 사용하십시오. | char(2) |
| socialaccountandappids | 더 이상 사용되지 않습니다. 소셜 계정 및 앱 ID | varchar(255) |
| socialassettrackingcode | 더 이상 사용되지 않습니다. 소셜 캠페인 변수 | varchar(255) |
| socialauthor | 더 이상 사용되지 않습니다. 소셜 작성자 변수 | varchar(255) |
| socialcontentprovider | 더 이상 사용되지 않습니다. 소셜 플랫폼/속성 | varchar(255) |
| socialinteractiontype | 더 이상 사용되지 않습니다. 소셜 상호 작용 유형 | varchar(255) |
| sociallanguage | 더 이상 사용되지 않습니다. 소셜 언어 | varchar(255) |
| sociallatlong | 더 이상 사용되지 않습니다. 소셜 위도/경도 | varchar(255) |
| socialowneddefinitioninsighttype | 더 이상 사용되지 않습니다. 소셜이 소유한 정의 통찰력 유형 | varchar(255) |
| socialowneddefinitioninsightvalue | 더 이상 사용되지 않습니다. 소셜이 소유한 정의 통찰력 값 | varchar(255) |
| socialowneddefinitionmetric | 더 이상 사용되지 않습니다. 소셜이 소유한 정의 지표 | varchar(255) |
| socialowneddefinitionpropertyvspost | 더 이상 사용되지 않습니다. 소셜이 소유한 정의 속성 대 게시 | varchar(255) |
| socialownedpostids | 더 이상 사용되지 않습니다. 소셜이 소유한 게시물 ID | varchar(255) |
| socialownedpropertyid | 더 이상 사용되지 않습니다. 소셜이 소유한 속성 ID | varchar(255) |
| socialownedpropertyname | 더 이상 사용되지 않습니다. 소셜이 소유한 속성 이름 | varchar(255) |
| socialownedpropertypropertyvsapp | 더 이상 사용되지 않습니다. 소셜이 소유한 속성 이름 대 앱 | varchar(255) |
| state | 상태 변수입니다. | varchar(50) |
| stats_server | 사용하지 않습니다. 히트를 처리한 Adobe 내부 서버. | char(30) |
| t_time_info | 방문자의 로컬 시간입니다. 형식은 다음과 같습니다. M/D/YYYY HH: MM: SS 월 (0-11, 0 = 1 월) 시간대 오프셋 (분 단위) | varchar(100) |
| tnt | Adobe Target 통합에서 사용됩니다. | text |
| tnt_action | Adobe Target 통합에서 사용됩니다. | text |
| tnt_post_vista | 더 이상 사용되지 않습니다. 대신 post_tnt를 사용하십시오. | text |
| transactionid | 데이터 소스를 통해 나중에 다양한 데이터 포인트를 업로드할 수 있는 고유 식별자입니다. | text |
| truncated_hit | 이미지 요청이 잘렸음을 나타내는 플래그입니다. 부분 히트가 수신되었음을 나타냅니다. <br>Y: 히트가 잘렸습니다. 부분 히트가 <br>N: 히트가 잘리지 않았습니다. 전체 히트 수신 | char(1) |
| ua_color | 더 이상 사용되지 않습니다. 이전에는 색상 깊이에 대한 대체 항목으로 사용되었습니다. | char(20) |
| ua_os | 더 이상 사용되지 않습니다. 이전에는 운영 체제에 대한 대체 항목으로 사용되었습니다. | char(80) |
| ua_pixels | 더 이상 사용되지 않습니다. 이전에는 브라우저 높이와 너비에 대한 대체 항목으로 사용되었습니다. | char(20) |
| user_agent | 이미지 요청의 HTTP 헤더에서 전송된 사용자 에이전트 문자열입니다. | text |
| user_hash | 사용하지 않습니다. 보고서 세트 ID의 해시. 대신 사용자 이름을 사용하십시오. | 부호 없는 int |
| user_server | 서버 차원에 사용되는 변수입니다. | varchar(100) |
| userid | 사용하지 않습니다. 보고서 세트 ID의 숫자 ID입니다. 대신 사용자 이름을 사용하십시오. | 부호 없는 int |
| username | 보고서 세트 ID (히트에 대한) | char(40) |
| va_closer_detail | 마지막 터치 세부 사항 차원에 사용되는 변수입니다. | varchar(255) |
| va_closer_id | 마지막 터치 채널 차원을 식별하는 숫자 ID입니다. 이 ID에 대한 조회는 마케팅 채널 관리자에서 찾을 수 있습니다. | tinyint 부호 없음 |
| va_finder_detail | 첫 번째 터치 세부 사항 차원에 사용되는 변수입니다. | varchar(255) |
| va_finder_id | 첫 번째 터치 채널 차원을 식별하는 숫자 ID입니다. 이 ID에 대한 조회는 마케팅 채널 관리자에서 찾을 수 있습니다. | tinyint 부호 없음 |
| va_instance_event | 마케팅 채널 인스턴스를 식별하는 플래그입니다. 마케팅 채널 마지막 터치 인스턴스 지표에 사용됩니다. | tinyint 부호 없음 |
| va_new_engagement | 마케팅 채널 새 참여를 식별하는 플래그입니다. 새 참여 지표에서 사용됩니다. | tinyint 부호 없음 |
| video | 비디오 컨텐츠 | varchar(255) |
| videoad | 비디오 광고 이름 | varchar(255) |
| videoadinpod | 창 위치의 비디오 광고 | varchar(255) |
| videoadlength | 비디오 광고 길이 | varchar(255) |
| videoadload | 비디오 광고 로드 | varchar(255) |
| videoadname | 비디오 광고 이름 | varchar(255) |
| videoadplayername | 비디오 광고 플레이어 이름 | varchar(255) |
| videoadpod | 비디오 광고 창 | varchar(255) |
| videoadvertiser | 비디오 광고주 | varchar(255) |
| Videoaudioalbum | 비디오 오디오 앨범 | varchar(255) |
| Videoaudioartist | Video Audio Artist | varchar(255) |
| Videoaudioauthor | 비디오 오디오 작성자 | varchar(255) |
| Videoaudiolabel | 비디오 오디오 레이블 | varchar(255) |
| Videoaudiopublisher | 비디오 오디오 게시자 | varchar(255) |
| Videoaudiostation | 비디오 오디오 스테이션 | varchar(255) |
| Videocampaign | 비디오 캠페인 | varchar(255) |
| videochannel | 비디오 채널 | varchar(255) |
| videochapter | 비디오 챕터 이름 | varchar(255) |
| videocontenttype | 비디오 컨텐츠 유형을 참조하십시오. 모든 비디오 보기에 대해 자동으로 '비디오'로 설정됩니다. | varchar(255) |
| videodaypart | 비디오 한시적 입찰 | varchar(255) |
| videoepisode | 비디오 에피소드 | varchar(255) |
| videofeedtype | 비디오 피드 유형 | varchar(255) |
| videogenre | Video Genre | text |
| videolength | 비디오 길이 | varchar(255) |
| videomvpd | Video MVPD | varchar(255) |
| videoname | 비디오 이름 | varchar(255) |
| videonetwork | 비디오 네트워크 | varchar(255) |
| videopath | 비디오 경로 | varchar(100) |
| videoplayername | 비디오 플레이어 이름 | varchar(255) |
| videoqoebitrateaverageevar | 비디오 품질 평균 비트 전송률 | varchar(255) |
| videoqoebitratechangecountevar | 비디오 품질 변경 카운트 | varchar(255) |
| videoqoebuffercountevar | 비디오 품질 버퍼 카운트 | varchar(255) |
| videoqoebuffertimeevar | 비디오 품질 버퍼 시간 | varchar(255) |
| videoqoedroppedframecountevar | 비디오 품질 드롭된 프레임 카운트 | varchar(255) |
| videoqoeerrorcountevar | 비디오 품질 오류 카운트 | varchar(255) |
| videoqoeextneralerrors | 비디오 품질 외부 오류 | text |
| videoqoeplayersdkerrors | 비디오 품질 SDK 오류 | text |
| videoqoetimetostartevar | 비디오 품질 시작할 시간 | varchar(255) |
| videoseason | 비디오 시즌 | varchar(255) |
| videosegment | 비디오 세그먼트 | varchar(255) |
| videoshow | 비디오 표시 | varchar(255) |
| videoshowtype | 비디오 표시 유형 | varchar(255) |
| videostreamtype | 비디오 스트림 유형 | varchar(255) |
| visid_high | 방문을 고유하게 식별하기 위해 visid_low와 함께 사용됩니다. | bigint unsigned |
| visid_low | 방문을 고유하게 식별하기 위해 visid_high와 함께 사용됩니다. | bigint unsigned |
| visid_new | 히트에 새로 생성된 방문자 ID가 있는지 여부를 식별하는 플래그입니다. | char(1) |
| visid_timestamp | 방문자 ID가 새로 생성된 경우 방문자 ID가 생성된 시간의 타임스탬프(Unix 시간)를 제공합니다. | int |
| visid_type | 방문자를 식별하는 데 사용된 방법을 나타내는 숫자 ID입니다. <br>0: 사용자 지정 Visitorid <br>1: IP 및 사용자 에이전트 폴백 <br>2: HTTP 모바일 가입자 헤더 <br>3: 이전 쿠키 값 (s_ vi) <br>4: 대체 쿠키 값 (s_ fid) <br>5: ID 서비스 | tinyint 부호 없음 |
| visit_keywords | 검색 키워드 차원에 사용되는 변수입니다. 이 열은 비표준 문자 제한을 사용하여 Adobe에서 사용하는 백엔드 로직을 수용합니다. | varchar(244) |
| visit_num | 방문 번호 차원에 사용되는 변수입니다. 1에서 시작하여 새 방문이 방문자별로 시작될 때마다 증가합니다. | 부호 없는 int |
| visit_page_num | 히트 깊이 차원에 사용되는 변수입니다. 사용자가 생성하는 각 히트에 대해 1씩 증가합니다. 각 방문을 재설정합니다. | 부호 없는 int |
| visit_ref_domain | visit_referrer 열을 기반으로 합니다. 방문의 첫 번째 참조 도메인입니다. | varchar(100) |
| visit_ref_type | 방문자의 첫 번째 레퍼러 유형을 나타내는 숫자 ID입니다. referrer_type.tsv 조회 테이블을 사용합니다. | tinyint 부호 없음 |
| visit_referrer | 방문의 첫 번째 레퍼러입니다. | varchar(255) |
| visit_search_engine | 방문의 첫 번째 검색 엔진에 대한 숫자 ID입니다. search_engines.tsv 조회 테이블을 사용합니다. | Smallint 부호 없음 |
| visit_start_page_url | 방문의 첫 번째 URL입니다. | varchar(255) |
| visit_start_pagename | the 방문의 첫 번째 페이지 이름입니다. | varchar(100) |
| visit_start_time_gmt | 방문의 첫 번째 히트 타임스탬프(Unix 시간)입니다. | int |
| weekly_visitor | 히트가 새 주별 방문자인지 판별하는 플래그입니다. | tinyint 부호 없음 |
| yearly_visitor | 히트가 새 연별 방문자인지 판별하는 플래그입니다. | tinyint 부호 없음 |
| zip | 우편 번호 차원을 채우는 데 사용됩니다. | varchar(50) |