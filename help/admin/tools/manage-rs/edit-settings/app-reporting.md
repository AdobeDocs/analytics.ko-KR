---
description: 모바일 애플리케이션 추적에 사용할 차원 및 지표를 활성화합니다.
title: 앱 보고
feature: Admin Tools
exl-id: ec19695a-2961-45e4-bf44-434f0ff9e3c9
TQID: https://experienceleague.adobe.com/oF-tETs2-MWjSLoo5bVUmrr2nS4N1o2shD4DkMDAVLU
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7aid: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
subfeature_v2: id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06id: b3a8b8a0-1cc2-48a8-ac82-ffd9c66ccab4id: c4cb071e-4667-4fb1-b1f1-d8994549cfb2id: c77ba355-6681-41fe-b719-563d3f507fdbid: ef60b66e-5984-4336-ba72-6d978b1b6f87id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 543
ht-degree: 11%

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

* [!UICONTROL 작업 이름]&#x200B;([시작](/help/components/dimensions/entry-dimensions.md) 및 [종료](/help/components/dimensions/exit-dimensions.md) 차원 포함)
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
* [!UICONTROL 해상도(SDK)]

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
* 블루투스 비콘(UUID, major, minor 및 proximity)을 추적합니다.

[!UICONTROL 위치 추적]을 사용하도록 설정하면 다음 차원을 사용할 수 있습니다.

* [!UICONTROL 비콘 Major]&#x200B;([시작](/help/components/dimensions/entry-dimensions.md) 및 [종료](/help/components/dimensions/exit-dimensions.md) 차원 포함)
* [!UICONTROL Beacon Minor]&#x200B;([Entry](/help/components/dimensions/entry-dimensions.md) 및 [Exit](/help/components/dimensions/exit-dimensions.md) 차원 포함)
* [!UICONTROL 비콘 근접]&#x200B;([시작](/help/components/dimensions/entry-dimensions.md) 및 [종료](/help/components/dimensions/exit-dimensions.md) 차원 사용)
* [!UICONTROL 비콘 UUID]&#x200B;([Entry](/help/components/dimensions/entry-dimensions.md) 및 [Exit](/help/components/dimensions/exit-dimensions.md) 차원 사용)
* [!UICONTROL 위치(10km까지)]
* [!UICONTROL 위치(100m까지)]
* [!UICONTROL 위치(1m까지)]
* [!UICONTROL 관심 영역 이름]
* [!UICONTROL 관심 영역 중앙까지의 거리]
* [!UICONTROL 관심 영역 ID]

## [!UICONTROL 음성 및 챗봇]

[!UICONTROL 음성 및 챗봇] 차원 및 지표를 사용하면 Alexa 또는 Google Home과 같은 음성 도우미를 측정할 수 있습니다. 또한 집에서 만든 채팅 봇을 측정할 수 있습니다. 측정 속성에는 다음이 포함됩니다.

* **라이프사이클**: 시작 수 및 플랫폼 유형과 같은 모든 앱에 대한 보고의 기초 수준입니다.
* **대화**: 대화와 관련된 의도, 응답 및 기타 지표 및 차원을 측정합니다.

[!UICONTROL 음성 및 챗봇]을 사용하도록 설정하면 다음 차원을 사용할 수 있습니다.

* [!UICONTROL 음성 장치 기능]&#x200B;([시작](/help/components/dimensions/entry-dimensions.md) 및 [종료](/help/components/dimensions/exit-dimensions.md) 차원 사용)
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

Adobe에서는 배경 히트가 표시되지 않도록 이전 보고를 비활성화하는 것이 좋습니다. 분석에 배경 히트를 포함하려면 [가상 보고서 세트](/help/components/vrs/vrs-about.md) 설정 **[!UICONTROL 배경 히트 포함]**&#x200B;을 사용하도록 설정할 수 있습니다.
