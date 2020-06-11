---
title: 페이지를 찾을 수 없음
description: 오류가 포함된 히트 수입니다.
translation-type: tm+mt
source-git-commit: 54aeaa35fea8f725c87030936fa24f415064e333
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 5%

---


# 페이지를 찾을 수 없음

*이 도움말 페이지에서는 &#39;페이지를 찾을 수 없음&#39;이 지표로 작동하는 방식을 설명합니다. 자세한 내용은[페이지를 찾을](../dimensions/pages-not-found.md)수 없음 차원을 참조하십시오.*

&#39;페이지를 찾을 수 없음&#39; 지표는 페이지에 오류가 있는 히트 수를 보여줍니다. 이 지표는 오류 메시지(예: 404)가 포함된 페이지 또는 URL을 확인하려는 경우 매우 중요하므로 오류 원인을 파악하고 수정할 수 있습니다.

## 이 지표의 계산 방법

이 지표는 변수가 의 값과 같은 모든 히트 [`pageType`](/help/implement/vars/page-vars/pagetype.md) 를 계산합니다 `"errorPage"`. 페이지를 찾을 수 없는 [차원에 해당하는](../dimensions/pages-not-found.md) 지표입니다.