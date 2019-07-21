---
description: 실시간 페이지 분석(라이브 모드)에서는 실시간으로 매우 세부적인 결과를 획득할 수 있습니다.
seo-description: 실시간 페이지 분석(라이브 모드)에서는 실시간으로 매우 세부적인 결과를 획득할 수 있습니다.
seo-title: 실시간 (라이브) 페이지 분석
solution: Analytics
title: 실시간 (라이브) 페이지 분석
topic: Activity Map
uuid: A 3 FAA 9 BD -73 D 8-48 B 3-BE 2 B-F 818 ED 7456 FB
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# 실시간 (라이브) 페이지 분석

실시간 페이지 분석(라이브 모드)에서는 실시간으로 매우 세부적인 결과를 획득할 수 있습니다.

이제 Activity Map에서는 분석 데이터를 1분에서 15분까지의 간격으로 표시하여 선택한 페이지에 대한 마이크로 트렌드를 기반으로 링크 인기도를 모니터링합니다. 이렇게 하는 것은 스토리에 대한 관심의 증가 또는 감소를 추적 및 대응하고 실시간 트래픽 흐름을 모니터링하는 게시 기업에게 특히 중요합니다.

사이트 컨텐츠 소유자로서의 작업 중 일부는 컨텐츠를 홍보 및 제거할 시기를 이해하고 환경을 지속적으로 적절하게 유지하는 것입니다. 실시간 데이터는 이러한 책임의 핵심 요소입니다. 지금 당장 트렌드를 만들고 있는 링크 및 컨텐츠를 알 수 있다면 신속하고 단호하게 대응하여 독자와 고객이 계속 여러분의 브랜드에 참여하도록 할 수 있습니다.

![](assets/live_mode.png)

<!-- 

Describe what you can do with the feature: - what is the data shown? why do I see trend lines everywhere? how do I choose a period in the trend? what do the overlays represent in live mode? how do you compute the gainers and losers overlays? what is the auto update mode?

 -->

## Data latency as a result of A4T configuration {#section_806CE36354FC4C539A0DED9266A5C704}

Adobe Target에서 A4T 통합이 활성화되면 Adobe Analytics에서 5~10분 동안 지연이 추가로 발생할 수 있습니다. 추가적인 지연 시간으로 인해 Analytics 및 Target의 데이터가 동일한 히트 수로 저장되므로 테스트를 페이지 및 사이트 섹션 단위로 분류할 수 있습니다.

추가적인 지연 시간은 라이브 스트림 및 실시간 보고를 비롯하여 모든 Adobe Analytics 서비스 및 도구에서 반영되며 다음과 같은 시나리오에서 적용됩니다.

* 라이브 스트림, 실시간 보고서 및 API 요청, 트래픽 변수의 현재 데이터의 경우 보충 데이터 ID가 있는 히트 수만 지연됩니다.
* 전환 지표의 현재 데이터, 완료된 데이터, 데이터 피드의 경우 모든 히트 수가 추가적으로 5-7분 지연됩니다.

[ID 서비스를](https://marketing.adobe.com/resources/help/en_US/mcvid/)구현한 후 이 통합을 완전히 구현하지 않은 경우에도 지연 증가가 시작됩니다.
