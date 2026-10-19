---
title: 모바일 라이프사이클 차원
description: Mobile SDK을 사용하여 수집된 데이터를 기반으로 하는 차원입니다.
feature: Dimensions
exl-id: b7ba45d7-7d30-48a3-a747-ea9fbb253abb
TQID: 'https://experienceleague.adobe.com/VUN8x5eMzIfJ9VGw76v2pWfKWU7b-ct-kI6liwWTObw'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
    internal-label: Data configuration and collection
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
  - id: b22bc0f7-b089-4966-95a1-31e7b3b69b79
    internal-label: Dimensions
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: 6fd4400b33fcfc8bc3cd3ffc54fa738fef3441ef
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 8%
---
# 모바일 라이프사이클 차원

>[!BEGINSHADEBOX]

*이 페이지에서는 Adobe Experience Platform Mobile SDK을 통해 일반적으로 추적된 데이터를 참조합니다. 사용자 에이전트를 사용하는 모바일 장치에 대한 자세한 내용은 [모바일 조회 차원](mobile-dimensions.md)을 참조하십시오. Mobile SDK을 사용하여 추적한 지표에 대해서는 [모바일 라이프사이클 지표](../metrics/lifecycle-metrics.md).*&#x200B;를 참조하십시오.

>[!ENDSHADEBOX]

| 라이프사이클 차원 이름 | 설명 | 컨텍스트 데이터 변수 |
| --- | --- | --- |
| **[!UICONTROL 첫 번째 실행 날짜]** | 앱을 설치하거나 다시 설치한 후 앱을 처음 실행한 날짜입니다. `M/d/yyyy` 형식입니다. | `a.InstallDate` |
| **[!UICONTROL 장치 이름(SDK)]** | SDK에서 수집하는 디바이스 이름입니다. | `a.DeviceName` |
| **[!UICONTROL 운영 체제 버전(SDK)]** | SDK에서 수집하는 운영 체제 이름 및 버전입니다. | `a.OSVersion` |
| **[!UICONTROL 해상도(SDK)]** | 디바이스의 화면 해상도(픽셀 단위, 너비 x 높이)입니다. | `a.Resolution` |
| **[!UICONTROL 획득 Source]** | 뉴스레터 또는 소셜 미디어 네트워크와 같은 앱 획득 캠페인에 대한 원본 레퍼러입니다. | `a.referrer.campaign.source` |
| **[!UICONTROL 앱 ID]** | `AppName BundleVersion (app version code)` 형식의 앱 이름 및 버전입니다. 예, `MyAppName 1.1(1)`. | `a.AppID` |
| **[!UICONTROL 획득 Medium]** | 배너 또는 이메일과 같은 앱 획득 캠페인에 대한 마케팅 미디어. | `a.referrer.campaign.medium` |
| **[!UICONTROL 획득 용어]** | 앱 획득 캠페인과 연결된 유료 키워드 또는 기타 용어입니다. | `a.referrer.campaign.term` |
| **[!UICONTROL 획득 콘텐츠]** | 앱 획득 링크를 표시한 콘텐츠의 이름 또는 ID입니다. | `a.referrer.campaign.content` |
| **[!UICONTROL 획득 이름]** | 앱 획득 캠페인의 이름입니다. | `a.referrer.campaign.name` |
| **[!UICONTROL 위치(10km까지)]** | 방문자의 위도와 경도로, 소수점 첫 번째 자리까지 정확합니다. 예: `040.9` `-111.9`. | `a.loc.lat.a` + `a.loc.lon.a` |
| **[!UICONTROL 위치(100m까지)]** | 방문자의 위도와 경도로 소수점 세 번째 자리까지 정확합니다. 예: `040.932` `-111.931`. | `a.loc.lat.a` + `a.loc.lat.b` + `a.loc.lon.a` + `a.loc.lon.b` |
| **[!UICONTROL 위치(1m까지)]** | 방문자의 위도와 경도로 소수점 다섯 번째 자리까지 정확합니다. 예: `040.93231` `-111.93152`. | `a.loc.lat.a` + `a.loc.lat.b` + `a.loc.lat.c` + `a.loc.lon.a` + `a.loc.lon.b` + `a.loc.lon.c` |
| **[!UICONTROL 관심 영역 이름]** | 장치가 있는 관심 영역(POI)의 이름입니다. [위치 확장](https://developer.adobe.com/client-sdks/solution/places/)을 사용하는 경우 이 값은 위치 지역 이름입니다. | `a.loc.poi` |
| **[!UICONTROL 관심 영역 중앙까지의 거리]** | 장치와 장치가 속한 관심 영역의 중심 사이의 거리입니다. | `a.loc.dist` |
| **[!UICONTROL 시작 번호]** | 앱을 시작하거나 백그라운드에서 나온 횟수입니다. | `a.Launches` |
| **[!UICONTROL 최초 사용 이후 일 수]** | 앱을 처음 실행한 이후 경과일 수입니다. | `a.DaysSinceFirstUse` |
| **[!UICONTROL 작업 이름]** | `trackAction` 호출 시 전송된 작업의 이름입니다. | `a.action` |
| **[!UICONTROL 수명 값(evar)]** | 라이프타임 구매, 광고 보기, 비디오 전체 보기 또는 소셜 공유와 같은 사용자의 라이프타임 값입니다. | `a.ltv.amount` |
| **[!UICONTROL 비콘 Major]** | 장치가 있는 비콘의 주요 ID입니다. | `a.beacon.major` |
| **[!UICONTROL 비콘 Minor]** | 장치가 있는 비콘의 부 ID입니다. | `a.beacon.minor` |
| **[!UICONTROL 비콘 UUID]** | 장치가 근처에 있는 비콘의 UUID입니다. | `a.beacon.uuid` |
| **[!UICONTROL 비콘 Proximity]** | 장치의 비콘 근접 거리: `0`(알 수 없음), `1`(즉시), `2`(근접) 또는 `3`(원거리). | `a.beacon.prox` |
| **[!UICONTROL 마지막 사용 이후 일 수]** | 앱을 마지막으로 사용한 이후 일 수입니다. | `a.DaysSinceLastUse` |
| **[!UICONTROL 시간(SDK)]** | 앱이 실행된 시간(24시간 형식)입니다. 피크 사용 시간을 결정하기 위한 시간 분할에 유용합니다. | `a.HourOfDay` |
| **[!UICONTROL 요일(SDK)]** | 앱이 실행된 요일입니다. | `a.DayOfWeek` |
| **[!UICONTROL 관심 영역 ID]** | 장치가 속한 관심 영역의 ID입니다. [위치 확장](https://developer.adobe.com/client-sdks/solution/places/)을 사용하는 경우 이 값은 위치 지역 ID입니다. | `a.loc.poi.id` |

>[!NOTE]
>
>이러한 차원 중 일부는 더 이상 지원되지 않는 레거시 Mobile Services SDK(4.x)의 메서드로 채워집니다. Adobe Experience Platform Mobile SDK은 자동으로 채우지 않습니다.
>
>* **획득 차원** ([!UICONTROL 획득 Source], [!UICONTROL Medium], [!UICONTROL 용어], [!UICONTROL 컨텐츠], [!UICONTROL 이름]): 모바일 앱 획득으로 채워지며, 모바일 SDK [에서는 이 차원을 지원하지 않습니다](https://developer.adobe.com/client-sdks/resources/upgrade-platform-sdks/comparison/).
>* **[!UICONTROL 위치] 차원 및 [!UICONTROL 관심 영역 중앙까지의 거리]**: 4.x `trackLocation` 메서드로 채워집니다. Mobile SDK은 이 메서드를 [Places extension](https://developer.adobe.com/client-sdks/solution/places/)&#x200B;(관심 영역 이름[!UICONTROL 및 [!UICONTROL 관심 영역 ID]을)로 대체합니다.]
>* **[!UICONTROL 수명 값(evar)]**: 4.x `trackLifetimeValueIncrease` 메서드로 채워집니다.
>* **비콘 차원**([!UICONTROL 비콘 Major], [!UICONTROL Minor], [!UICONTROL UUID] 및 [!UICONTROL Proximity]): 4.x `trackBeacon` 메서드로 채워집니다. Mobile SDK으로 비콘 데이터를 보내려면 [비콘 추적](https://developer.adobe.com/client-sdks/solution/adobe-analytics/track-beacon/)을 참조하세요.
>
>자세한 내용은 [Adobe 모바일 라이브러리(v4)에서 Experience Platform Analytics로 마이그레이션](https://developer.adobe.com/client-sdks/resources/upgrade-platform-sdks/analytics/)을 참조하십시오.
