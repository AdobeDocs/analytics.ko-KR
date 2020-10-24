---
title: 알고리즘 속성
description: 알고리즘 속성 모델에 대한 세부 사항입니다.
translation-type: ht
source-git-commit: cd2225ec00190af6b616f313b419935c4f8dfafd
workflow-type: ht
source-wordcount: '257'
ht-degree: 100%

---


# 알고리즘 속성

Analysis Workspace의 알고리즘 [속성 모델](models.md)은 통계적 기법을 사용하여 보고서나 자유 형식 테이블의 차원 항목에 크레딧을 할당한다는 점에서 다른 모델과 다릅니다. Analysis Workspace의 다른 모든 속성 모델과 마찬가지로 모든 차원이나 지표에서 사용할 수 있으며 무제한 세그먼테이션 및 분류를 지원하고 테이블의 차원에 대한 100% 전환(&quot;분수&quot; 속성)을 분배합니다.

속성에 사용되는 알고리즘은 협업 게임 이론의 Harsanyi 배당을 기반으로 합니다. Harsanyi 배당은 결과에 불평등한 기여와 함께 플레이어들 간의 크레딧을 분배하기 위해 Shapley 값 솔루션(노벨 경제학상 수상자인 Lloyd Shapley의 이름을 따서 이름이 지어짐)의 일반화입니다.

높은 수준에서, 각 접점에 대한 전환 크레딧의 속성 계산에서는 전환 창 내의 각 마케팅 접점을 잉여금이 균등하게 분배되어야 하는 사용자의 연합으로 간주합니다. 각 연합의 잉여금은 각 하위 연합(또는 이전에 참가한 차원 항목)에 의해 이전에 생성된 잉여금에 따라 재귀적으로 결정됩니다. 자세한 내용은 John Harsanyi 및 Lloyd Shapley의 원본 논문을 참조하십시오.

* Shapley, Lloyd S. (1953). A value for n-person games. *Contributions to the Theory of Games, 2(28)*, 307-317.
* Harsanyi, John C. (1963). A simplified bargaining model for the n-person cooperative game. *International Economic Review 4(2)*, 194-220.

>[!NOTE]
>
>주어진 전환 창 내에 여러 접점이 있을 때 알고리즘 속성의 결과는 다른 모델과 다릅니다. 단일 접점을 사용하는 전환은 속성 모델에 상관없이 100% 크레딧을 받습니다.
