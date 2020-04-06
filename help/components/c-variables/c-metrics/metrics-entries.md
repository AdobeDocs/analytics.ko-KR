---
description: 시작은 주어진 값이 방문에서 첫 번째 값으로 캡처된 횟수를 나타냅니다. 시작은 방문당 한 번만 발생할 수 있습니다. 하지만 변수가 정의되지 않은 경우 반드시 첫 번째 히트가 되는 것은 아닙니다.
title: 항목
topic: Metrics
uuid: c4608b66-b70c-4e98-b7c6-9be5fbe4ec9c
translation-type: tm+mt
source-git-commit: e6aaf2754c6a5c33fbe3e093b4d7ca5a375c41e7

---


# 항목

&quot;시작 횟수&quot;는 주어진 값이 방문에서 첫 번째 값으로 캡처된 횟수를 나타냅니다. 시작은 방문당 한 번만 발생할 수 있습니다. 하지만 변수가 정의되지 않은 경우 반드시 첫 번째 히트가 되는 것은 아닙니다.

2020년 3월 현재 분석 작업 공간에서 &quot;없음&quot; 값이 시작/종료와 상호 작용하는 방식을 변경했습니다.  이제 분석 작업 공간에서 &quot;Ones&quot;를 켜거나 끌 수 있으므로 시작 또는 종료 후에 &quot;없음&quot;을 적용하고, (evar의 경우) 이전에 적용되었던 항목을 적용합니다.  예를 들어, 방문의 첫 번째 히트에 값이 없다고 가정하고, 예를 들어 eVar21은 값이 없지만 두 번째 히트는 값이 있다고 가정합니다. 보고 및 분석에서는 항목에 대해 &quot;지정되지 않음&quot;으로 표시되지만 분석 작업 공간에 두 번째 히트에 대한 값으로 표시됩니다.

시작 페이지에는 방문 분류 범위가 있으며, 이것은 한 방문에 대한 모든 히트에서 지속됨을 의미합니다. 자세한 내용은 [분류 및 세그먼테이션 컨테이너](https://marketing.adobe.com/resources/help/en_US/sc/user/c_Breakdown_and_segmentation_containers.html)를 참조하십시오.
