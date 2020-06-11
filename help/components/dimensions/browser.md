---
title: 브라우저
description: 사용된 브라우저의 이름 및 버전.
translation-type: tm+mt
source-git-commit: 4a7b3a00bdbf557c219de530e3e692c2b2db4a84
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---


# 브라우저

&#39;브라우저&#39; 차원은 히트를 전송하는 브라우저의 이름과 버전을 보고합니다. 이 차원은 방문자가 사용하는 가장 일반적인 브라우저를 파악하는 데 유용합니다. 사이트의 새 버전을 테스트할 때 이 차원의 상위 브라우저에서 이러한 테스트를 실행하여 품질 관리 노력을 극대화할 수 있습니다.

## 데이터로 이 차원 채우기

이 차원은 Adobe 내부 조회 테이블을 참조합니다. 조회 값은 이미지 요청의 `User-Agent` HTTP 헤더를 기반으로 합니다. AppMeasurement 라이브러리(예: Adobe Experience Platform Launch)를 사용하는 경우 이 차원은 기본적으로 작동합니다.

## 차원 값

차원 값에는 사용된 브라우저 이름과 버전이 포함됩니다. 동일한 브라우저의 다른 버전은 차원 값입니다.

일부 차원 값은 버전 번호 `"(unknown version)"` 대신 포함됩니다. 이 차원 값은 Adobe가 해당 조회 테이블에 추가하지 않은 최근 브라우저 릴리스를 참조합니다. 브라우저가 자주 업데이트되므로 해당 브라우저 `"(unknown version)"` 의 사용 방법은 일반적이고 일시적입니다. Adobe는 일반적으로 월별 유지 관리 릴리스 동안 조회 테이블을 업데이트합니다.
