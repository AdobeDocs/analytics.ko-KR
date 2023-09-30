---
title: 브라우저
description: 사용된 브라우저의 이름 및 버전입니다.
feature: Dimensions
exl-id: 2bdf2a5a-3482-43fa-b2e1-fbea892918fb
source-git-commit: 206df584deab5f6f9b8eeb09d9c8ad4983424eea
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 59%

---

# 브라우저

&#39;[!UICONTROL 브라우저]&#39; [차원](overview.md) 히트를 전송하는 브라우저의 이름과 버전을 보고합니다. 이 차원은 방문자가 사용하는 가장 일반적인 브라우저를 측정하려는 경우에 유용합니다. 사이트의 새 버전을 테스트할 때 이 차원의 상위 브라우저에서 이러한 테스트를 실행하여 품질 관리 노력을 극대화할 수 있습니다.

## 이 차원을 데이터로 채우기

이 차원은 Adobe 내부의 조회 테이블을 참조합니다. 조회 값은 이미지 요청에 있는 `User-Agent` HTTP 헤더를 기반으로 합니다. 와 파트너 Adobe [DeviceAtlas](https://deviceatlas.com/) 사용자 에이전트와 브라우저 간 조회를 유지 관리합니다.

* AppMeasurement 구현의 경우 이 차원은 즉시 작동합니다.
* 웹 SDK 구현의 경우 다음을 활성화합니다 [!UICONTROL 장치 조회] 조건 [데이터스트림 구성](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=ko-KR).

## 차원 항목

차원 항목에는 사용된 브라우저 이름과 버전이 포함됩니다. 동일한 브라우저의 다른 버전은 별도의 차원 항목입니다.

일부 차원 항목은 버전 번호 대신 `"(unknown version)"`을 포함합니다. 이 차원 항목은 Adobe이 조회 테이블에 아직 추가하지 않은 최근 브라우저 릴리스를 참조합니다. 브라우저는 자주 업데이트되므로 주어진 브라우저에 대해 `"(unknown version)"`은 일반적이고 일시적입니다. Adobe는 일반적으로 월별 유지 관리 릴리스 동안 조회 테이블을 업데이트합니다.