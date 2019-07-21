---
description: 다음은 Power BI와 함께 Report Builder를 사용할 때 발생할 수 있는 몇 가지 일반적인 문제입니다.
seo-description: 다음은 Power BI와 함께 Report Builder를 사용할 때 발생할 수 있는 몇 가지 일반적인 문제입니다.
seo-title: Power BI 통합 문제 해결
title: Power BI 통합 문제 해결
uuid: C 1 E 7 E 164-4 BC 6-4513-9332-92 C 53 BE 021 CC
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Power BI 통합 문제 해결

다음은 Power BI와 함께 Report Builder를 사용할 때 발생할 수 있는 몇 가지 일반적인 문제입니다.

## 1단계. Failure to publish to Power BI {#section_5B87DC1C302C4FD8AB9E4DD6B162DC9B}

Power BI 게시를 필요로 하는 예약된 통합 문서는 시작하여 실행하는 Power BI 서비스에 의존합니다. 게시 실패에 대한 두 가지 주된 원인은 다음과 같습니다.

* Power BI 서비스가 중단될 수 있습니다.
* 통합 문서를 예약한 사용자에게 더 이상 유효한 Microsoft 계정 자격 증명이 없습니다.

각 Report Builder 예약 작업은 예약된 실행당 세 번을 시도하게 됩니다.

* 첫 번째 시도에 성공하지 못하면 "이 예약된 통합 문서를 Microsoft Power BI에 게시할 수 없습니다. 곧 다시 시도하겠습니다."라는 메시지가 표시됩니다.
* 두 번째 시도에 성공하지 못하면 메시지가 표시되지 않습니다.
* 세 번째 시도에 성공하지 못하면 "이 통합 문서를 Power BI에 게시할 수 없습니다."라는 메시지가 표시됩니다.

## 2단계. Broken visualizations in Power BI {#section_FFFE200D06F843B2AF093710FD678166}

Report Builder 요청을 Power BI에 게시한 후 시각화가 손상될 수 있는 가장 가능성 있는 원인은 다음과 같습니다.

* 지표나 차원 변경과 같은 요청을 Report Builder에서 편집한 다음, Power BI에 다시 게시했습니다. 요청을 편집하면 시각화가 손상될 수 있습니다.
* 시각화에 사용된 요청을 삭제했습니다.

