---
description: 앱 관리를 활성화하면 모바일 애플리케이션에서 라이프사이클 및 기타 지표를 캡처하는 모바일 솔루션 변수를 활성화합니다.
title: 앱 관리
feature: Admin Tools
exl-id: ec19695a-2961-45e4-bf44-434f0ff9e3c9
source-git-commit: a17297af84e1f5e7fe61f886eb3906c462229087
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 100%

---

# 앱 관리

앱 관리를 활성화하면 모바일 애플리케이션에서 라이프사이클 및 기타 지표를 캡처하는 모바일 솔루션 변수를 활성화합니다.

Adobe Analytics와 Mobile Services 간의 통합은:

* KPI(핵심 성능 지표) 데이터를 Mobile Services에서 Adobe Analytics에 공유할 수 있도록 해줍니다.
* 위치 추적을 가능하게 해줍니다.
* Analytics > [보고서] > [모바일 앱]에 새 보고서를 추가합니다.
* 25개의 새로운 Adobe Mobile 분류를 추가합니다.
* 5개의 새로운 Adobe Mobile 지표를 추가합니다.
* 새로운 Adobe Mobile 차원을 추가합니다.
* 데이터가 15분마다 Analytics에 동기화됩니다

**[!UICONTROL Analytics]** > **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]** > **[!UICONTROL 설정 편집]** > **[!UICONTROL 앱 관리]** > **[!UICONTROL 앱 보고]**.

## 1단계. 앱 보고서 활성화 {#section_FBADF80AED2B4978A904ABB770B3B931}

다음 지표를 측정하려면 앱 보고서 v3.0을 사용하십시오.

* **고객 확보** - 앱 다운로드 캠페인용 참조 URL을 추적합니다.
* **라이프사이클** - 각 앱 실행 시 보내진 측정으로 제공되는 보고에 대한 기초 수준입니다.
* **앱 작업** - 인앱 작업을 기반으로 한 보고서 및 경로 지정입니다.
* **라이프타임 값** - 사용자가 구입, 광고 보기, 비디오 완료, 소셜 공유, 사진 업로드와 같은, 앱 KPI를 사용하여 시간이 지남에 따라 값을 누적시키는 방법을 이해합니다.
* **시간 제한 이벤트** - 첫 번째 구입 전 시간과 같이, 주요 앱 작업 간에 경과하는 시간의 크기(인앱 및 총 시간)를 측정합니다.

## 2단계. 위치 추적 활성화 {#section_2CCBD205191C4CA3B7B71A6F11FF97EC}

위치 추적을 활성화하면 다음 작업을 수행할 수 있습니다.

* 위도 및 경도 데이터를 추적하고 Analysis Workspace 및 Mobile Services에서 해당 데이터에 대해 보고.
* Mobile Services 내의 특정 관심 영역(POI)을 식별, 생성 및 시각화. POI는 모바일 SDK 구성 파일에 정의되어 있어야 합니다.
* 블루투스 비콘(UUID, 주, 보조 및 근접) 추적.

## 3단계. (선택 사항) 백그라운드 히트에 대해 이전 보고 및 속성 활성화/비활성화 {#section_1708BCAA87AA4884986F7532759C5DD4}

활성화된 배경 조회(앱이 배경에 있을 때 생성되는 조회)는 일반적인 전경 조회로 취급된다는 의미입니다. 이제 이러한 조회가 일반적인 보고에 표시되며 이는 속성에 영향을 줍니다. 이 구성은 일반적으로 이전 구현과의 일관성을 유지하는 경우에만 바람직합니다.

대신 [가상 보고서 세트](/help/components/vrs/vrs-about.md)에 &quot;배경 조회수&quot;를 포함하는 것이 좋습니다. 이렇게 하면 조회 수를 볼 수는 있지만 조회 수가 방문 및 방문자 수에 부정적인 영향을 미치지는 않습니다.
모바일 분류는 **[!UICONTROL 앱 관리]** > **[!UICONTROL 앱 보고]**&#x200B;를 활성화하면 활성화됩니다.

분류는 값을 그룹으로 분류하고 그룹 수준으로 보고하는 데 사용됩니다. 예를 들어 모든 유료 검색 캠페인을 &quot;팝 뮤직 용어&quot;와 같은 카테고리로 분류하고 인스턴스(클릭스루라고도 함) 같은 지표와 관련한 해당 카테고리의 성공 및 성공 이벤트로의 전환을 보고합니다.

| 분류 | 정의 |
|--- |--- |
| 첫 번째 실행 날짜 | 설치 또는 재설치 후 처음 실행하는 날짜입니다.   YYYY/MM/DD |
| 앱 ID | 응용 프로그램 이름과 버전을 다음 형식으로 저장:   `[AppName] [BundleVersion]`  예, `myapp 1.1.` |
| 시작 번호 | 응용 프로그램을 시작하거나 백그라운드에서 나온 횟수입니다. |
| 최초 사용 이후 일 수 | 처음 실행한 이후 일수입니다. |
| 마지막 사용 이후 일 수 | 마지막 사용한 이후 일수. |
| 시간 | 앱이 실행된 시간을 측정하고 24시간 숫자 형식을 사용합니다. 피크 사용 시간을 결정하기 위한 시간 분할에 사용됩니다. |
| 요일 | 앱을 시작한 평일 횟수. |
| 장치 이름 | 장치 이름을 저장합니다.   장치를 식별하는 쉼표로 구분된 두 자리 문자열입니다. 첫 번째 번호는 일반적으로 장치 생성을 나타내고, 두 번째 번호는 장치 제품군의 다른 구성원을 나타냅니다. |
| 운영 체제 버전 | OS 버전. |
| 해상도 | 너비 x 높이(실제 픽셀) |
| 라이프타임 값(eVar) | trackLifetimeValue 메서드로 채워집니다. |
| 고객 확보 소스 |  |
| 고객 확보 미디어 |  |
| 고객 확보 용어 |  |
| 고객 확보 컨텐츠 |  |
| 고객 확보 이름 |  |
| 위치(10km까지) | trackLocation 메서드로 채워집니다. |
| 위치(100m까지) | trackLocation 메서드로 채워집니다. |
| 위치(1m까지) | trackLocation 메서드로 채워집니다. |
| 관심 영역 이름 | 정의된 POI 내에 장치가 있을 때 trackLocation 메서드로 채워집니다. |
| 관심 영역 중앙까지의 거리 | 정의된 POI 내에 장치가 있을 때 trackLocation 메서드로 채워집니다. |
| 인앱 메시지 ID |  |
| 인앱 메시지 온라인 |  |
| 푸시 옵트인 |  |
| 페이로드 ID |  |