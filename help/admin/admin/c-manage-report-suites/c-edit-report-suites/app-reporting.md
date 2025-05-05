---
description: 모바일 애플리케이션 추적에 사용할 차원 및 지표를 활성화합니다.
title: 앱 보고
feature: Admin Tools
exl-id: ec19695a-2961-45e4-bf44-434f0ff9e3c9
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 13%

---

# 앱 보고

앱 보고 인터페이스를 사용하면 모바일 애플리케이션 추적 전용으로 사용되는 라이프사이클 차원 및 지표를 활성화할 수 있습니다.

**[!UICONTROL Analytics]** > **[!UICONTROL 관리자]** > **[!UICONTROL 보고서 세트]** > **[!UICONTROL 설정 편집]** > **[!UICONTROL 앱 관리]** > **[!UICONTROL 앱 보고]**

>[!IMPORTANT]
>
>이러한 기능은 활성화되면 비활성화할 수 없습니다. 주어진 기능을 활성화하면 해당 차원 및 지표를 Analysis Workspace에서 영구적으로 사용할 수 있습니다.

## [!UICONTROL 앱 보고서]

[!UICONTROL 앱 보고서] 차원 및 지표는 다음 용도로 사용됩니다.

* **획득**: 앱 다운로드 캠페인에 대한 참조 URL을 추적합니다.
* **라이프사이클**: 각 앱 실행 시 전송된 측정에서 제공하는 기본 보고 수준입니다.
* **앱 작업**: 인앱 작업을 기반으로 한 보고서 및 경로 지정.
* **라이프타임 값**: 사용자가 앱 KPI(예: 구매, 광고 보기, 비디오 전체 보기, 소셜 공유, 사진 업로드)를 사용하여 시간이 지남에 따라 값을 어떻게 누적하는지 이해합니다.
* **Timed Events**: 주요 앱 작업(예: 첫 구매까지 소요된 시간) 사이에 경과된 시간(인앱 및 총 시간)을 측정합니다.

[!UICONTROL 앱 보고서]를 사용하도록 설정하면 다음 차원을 사용할 수 있습니다.

* [!UICONTROL 작업 이름] ([시작](/help/components/dimensions/entry-dimensions.md) 및 [종료](/help/components/dimensions/exit-dimensions.md) 차원 포함)
* [!UICONTROL 앱 ID]
* [!UICONTROL 획득 콘텐츠]
* [!UICONTROL 획득 Medium]
* [!UICONTROL 획득 이름]
* [!UICONTROL 획득 Source]
* [!UICONTROL 획득 용어]
* [!UICONTROL 요일(SDK)]
* [!UICONTROL 최초 사용 이후 일 수]
* [!UICONTROL 마지막 사용 이후 일 수]
* [!UICONTROL 장치 이름(SDK)]
* [!UICONTROL 시간(SDK)]
* [!UICONTROL 첫 번째 실행 날짜]
* [!UICONTROL 시작 번호]
* [!UICONTROL 수명 값(evar)]
* [!UICONTROL 운영 체제 버전(SDK)]
* [!UICONTROL 해결 방법(SDK)]

다음 지표를 사용할 수 있습니다.

* [!UICONTROL 앱의 동작 시간]
* [!UICONTROL 총 동작 시간]
* [!UICONTROL 충돌]
* [!UICONTROL 첫 번째 실행]
* [!UICONTROL 시작]
* [!UICONTROL 라이프타임 값(이벤트)]
* [!UICONTROL 총 세션 길이]
* [!UICONTROL 업그레이드]

## [!UICONTROL 위치 추적]

[!UICONTROL 위치 추적] 차원은 다음 용도로 사용됩니다.

* 위도 및 경도 데이터 추적
* 특정 관심 영역을 식별, 생성 및 시각화합니다. 관심 영역은 모바일 SDK 구성 파일에서 정의해야 합니다.
* 블루투스 비콘(UUID, 주, 보조 및 근접) 추적.

[!UICONTROL 위치 추적]을 사용하도록 설정하면 다음 차원을 사용할 수 있습니다.

* [!UICONTROL 비콘 Major] ([시작](/help/components/dimensions/entry-dimensions.md) 및 [종료](/help/components/dimensions/exit-dimensions.md) 차원 포함)
* [!UICONTROL Beacon Minor] ([Entry](/help/components/dimensions/entry-dimensions.md) 및 [Exit](/help/components/dimensions/exit-dimensions.md) 차원 포함)
* [!UICONTROL 비콘 근접] ([시작](/help/components/dimensions/entry-dimensions.md) 및 [종료](/help/components/dimensions/exit-dimensions.md) 차원 사용)
* [!UICONTROL 비콘 UUID] ([Entry](/help/components/dimensions/entry-dimensions.md) 및 [Exit](/help/components/dimensions/exit-dimensions.md) 차원 사용)
* [!UICONTROL 위치(10km까지)]
* [!UICONTROL 위치(100m까지)]
* [!UICONTROL 위치(1m까지)]
* [!UICONTROL 관심 영역 이름]
* [!UICONTROL 관심 영역 중앙까지의 거리]
* [!UICONTROL 관심 영역 ID]

## [!UICONTROL 음성 및 챗봇]

[!UICONTROL 음성 및 챗봇] 차원 및 지표를 사용하면 Alexa 또는 Google 홈과 같은 음성 도우미를 측정할 수 있습니다. 또한 집에서 만든 채팅 봇을 측정할 수 있습니다. 측정 속성에는 다음이 포함됩니다.

* **라이프사이클**: 시작 수 및 플랫폼 유형과 같은 모든 앱에 대한 보고의 기초 수준입니다.
* **대화**: 대화와 관련된 의도, 응답 및 기타 지표 및 차원을 측정합니다.

[!UICONTROL 음성 및 챗봇]을 사용하도록 설정하면 다음 차원을 사용할 수 있습니다.

* [!UICONTROL 음성 장치 기능] ([시작](/help/components/dimensions/entry-dimensions.md) 및 [종료](/help/components/dimensions/exit-dimensions.md) 차원 사용)
* [!UICONTROL 음성 인증]
* [!UICONTROL 음성 오류 유형]
* [!UICONTROL 음성 의도]
* [!UICONTROL 음성 앱 응답]
* [!UICONTROL 음성 언어]

다음 지표를 사용할 수 있습니다.

* [!UICONTROL 음성 종료 세션]
* [!UICONTROL 음성 오류]
* [!UICONTROL 음성 발화]

## 백그라운드 히트에 대한 이전 보고 및 속성

이전 보고는 앱이 배경에 있을 때 생성된 히트가 일반 전경 히트로 처리됨을 의미합니다. 보고서에 표시되며 속성에 영향을 줍니다. 이 레거시 구성은 일반적으로 레거시 구현과의 일관성을 유지하는 데 바람직합니다.

Adobe 배경 히트가 표시되지 않도록 이전 보고를 비활성화하는 것이 좋습니다. 분석에 배경 히트를 포함하려면 [가상 보고서 세트](/help/components/vrs/vrs-about.md) 설정 **[!UICONTROL 배경 히트 포함]**&#x200B;을 사용하도록 설정할 수 있습니다.
