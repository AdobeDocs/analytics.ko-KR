---
description: 'null'
title: 알고리즘 속성
uuid: bb345642-4f45-4fb8-82d0-803248dd52ea
translation-type: tm+mt
source-git-commit: b5418e6321b09ddbab36e0052f75f36067086e3e

---


# 알고리즘 속성

![알고리즘](assets/algorithmic.png)

분석 작업 공간의 알고리즘 [속성 모델은](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/attribution/attribution.html#attribution-models) 통계적 기법을 사용하여 보고서나 자유 형식 테이블의 차원 값에 크레딧을 할당한다는 점에서 Attribution IQ 내의 다른 모델과 다릅니다. 분석 작업 공간의 다른 모든 기여도 모델과 마찬가지로, 차원 또는 지표에서 사용할 수 있으며 무제한 세그먼테이션 및 분류를 지원하고 테이블의 차원에 대한 변환 중 100%(&quot;분수&quot; 기여도)를 분배합니다.

기여도에 사용되는 알고리즘은 협업 게임 이론의 Harsanyi Probjection을 기반으로 합니다. Harsanyi 배당은 Shapley 값 솔루션(노벨 경제학상 수상자인 Lloyd Shapley의 이름을 따름)의 일반화로, 결과에 불평등한 기여로 게임 참가자의 신용을 분배하는 것입니다.

높은 수준에서 각 터치포인트의 전환 크레딧에 대한 기여도 계산은 전환 시점의 각 마케팅 접점을 흑자가 균등하게 분배되어야 하는 플레이어의 연합으로 간주합니다. 각 연합의 잉여금은 각 하위 연합(또는 이전에 참가한 차원 값)에 의해 이전에 생성된 잉여금에 따라 재귀적으로 결정됩니다. 자세한 내용은 John Harsanys&#39;s와 Lloyd Shapley의 원본 논문을 참조하십시오.

* Shapley, Lloyd S.&quot;개인전 게임에 대한 가치&quot; 게임이론 기여:307-317.

* 하산이, 존 C.&quot;1인 협력게임을 위한 간소화된 협상 모델&quot; International Economic Review 4.2 (1963):194-220.

*참고:주어진 전환 창 내에 여러 터치포인트가 있을 때 알고리즘 속성의 결과는 다른 모델과 다릅니다. 예를 들어 하나의 터치포인트만 있는 경우, 선택한 기여도 모델에 상관없이 크레딧의 100%가 해당 값에 할당됩니다.*