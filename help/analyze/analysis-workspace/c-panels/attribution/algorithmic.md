---
title: 알고리즘 속성
description: Adobe Analytics의 알고리즘 속성 모델에 대한 자세한 정보입니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 알고리즘 속성

>[!NOTE] 알고리즘 속성은 현재 Adobe Analytics Labs를 통해서만 [제공됩니다](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/tech-previews/overview.html). 이 기능은 결국 일반 릴리스의 일부가 됩니다.

분석 작업 공간의 알고리즘 [속성 모델은](attribution.md) 통계적 기법을 사용하여 보고서나 자유 형식 테이블의 차원 값에 크레딧을 할당한다는 점에서 다른 모델과 다릅니다. 분석 작업 공간의 다른 모든 기여도 모델과 마찬가지로, 차원 또는 지표에서 사용할 수 있으며 무제한 세그먼테이션 및 분류를 지원하고 테이블의 차원에 대한 변환 중 100%(&quot;분수&quot; 기여도)를 분배합니다.

기여도에 사용되는 알고리즘은 협업 게임 이론의 Harsanyi Probjection을 기반으로 합니다. Harsanyi 배당은 Shapley 값 솔루션(노벨 경제학상 수상자인 Lloyd Shapley의 이름을 따름)의 일반화로, 결과에 불평등한 기여로 게임 참가자의 신용을 분배하는 것입니다.

높은 수준에서 각 터치포인트의 전환 크레딧에 대한 기여도 계산은 전환 시점의 각 마케팅 접점을 흑자가 균등하게 분배되어야 하는 플레이어의 연합으로 간주합니다. 각 연합의 잉여금은 각 하위 연합(또는 이전에 참가한 차원 값)에 의해 이전에 생성된 잉여금에 따라 재귀적으로 결정됩니다. 자세한 내용은 John Harsanys와 Lloyd Shapley의 원본 논문을 참조하십시오.

* Shapley, Lloyd S.(1953). 개인 게임에 대한 가치 *게임이론, 2(28)*, 307-317 공헌.
* 하산이, 존 C.(1963). N-Person 협력 게임을 위한 간소화된 협상 모델 *International Economic Review 4(2)*, 194-220.

>[!NOTE] 주어진 전환 창 내에 여러 터치포인트가 있을 때 알고리즘 속성의 결과는 다른 모델과 다릅니다. 단일 터치포인트를 통한 전환은 기여도 모델에 상관없이 100% 크레딧을 받습니다.
