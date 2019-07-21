---
description: 브라우저 창에서만 데이터의 가로/세로 거리를 참조하는 지표입니다. 즉, 브라우저
seo-description: 브라우저 창에서만 데이터의 가로/세로 거리를 참조하는 지표입니다. 즉, 브라우저
seo-title: 브라우저 너비/높이
solution: Analytics
title: 브라우저 너비/높이
topic: 지표
uuid: 1 C 0 D 3 EA 9-E 001-4152-9 BFC -8 FE 6406 BC 755
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 브라우저 너비/높이

브라우저 창에서만 데이터의 가로/세로 거리를 참조하는 지표입니다. 즉, 브라우저

Adobe Analytics에서는 방문의 첫 번째 히트에 해당하는 브라우저 높이 및 너비만 사용합니다. 나머지 방문 횟수는 동일한 방문에 기여되지 않습니다.
The browser width/height dimensions capture similar but distinct values when compared with [mobile screen size](../../../components/c-variables/dimensionslist/reports-mobile.md#topic_D306EA4558194488AC47A45B9C570150).

예를 들어, 모바일 해상도로 브라우저 너비 또는 높이를 분류하는 경우 다음과 같은 차이점을 알고 있어야 합니다.

* 모바일 장치 해상도는 장치와 관련된 실제 값입니다. 예를 들어, 모바일 장치 해상도에서 Galaxy S8은 2,960 x 1,440으로 표시됩니다. 모바일 장치 해상도는 장치가 식별된 후에 타사 서비스에서 검색됩니다.
* 이와 반대로 브라우저 높이 및 너비 값에 CSS(논리적) 값 740 x 360이 표시됩니다. 브라우저 값은 Javascript/CSS 데이터를 사용합니다.
* 간략한 설명은 [이 스레드](https://stackoverflow.com/questions/8785643/what-exactly-is-device-pixel-ratio)를 참조하십시오.

