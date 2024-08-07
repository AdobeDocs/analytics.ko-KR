---
title: 언어
description: 브라우저의 기본 언어 설정입니다.
feature: Dimensions
exl-id: 590406a4-d336-42c7-8048-e7cd8e611d43
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 91%

---

# 언어

&#39;언어&#39; [차원](overview.md)은(는) 방문자가 콘텐츠를 볼 때 선호하는 상위 언어들을 보여줍니다. 이 차원은 현지화 작업에 도움이 되도록 방문자가 가장 자주 사용하는 선호 언어를 알려는 경우 중요합니다.

>[!NOTE]
>
>이 차원은 사이트의 언어를 수집하지 않습니다. 차원에서 사이트의 언어를 수집하려는 경우 [eVar](evar.md)와 같은 사용자 지정 변수를 사용하는 것이 좋습니다.

## 이 차원을 데이터로 채우기

이 차원은 Adobe 내부의 조회 테이블을 참조합니다. 조회 값은 이미지 요청에 있는 `Accept-Language` HTTP 헤더를 기반으로 합니다. AppMeasurement 라이브러리를 사용하는 경우(Adobe Experience Platform의 태그 등을 통해) 이 차원은 즉시 작동합니다.

## 차원 항목

차원 항목에는 방문자가 사용하는 친숙한 기본 언어 이름이 포함됩니다. 예로는 `"English (United States)"`, `"English (United Kingom)"`, `"Chinese (China)"` 및 `"Spanish (Spain)"`가 있습니다. 이미지 요청의 HTTP 헤더에 올바른 언어가 포함되지 않으면 차원 항목은 `"None"`이 됩니다.
