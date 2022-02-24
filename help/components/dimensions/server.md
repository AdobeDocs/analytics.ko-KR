---
title: 서버
description: 서버 이름입니다.
feature: Dimensions
exl-id: c2454c0d-497e-46f8-8569-7d0517097cab
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: ht
source-wordcount: '136'
ht-degree: 100%

---

# 서버

서버 차원은 일반적으로 사이트의 호스트 이름을 나열합니다. 여러 도메인 또는 하위 도메인을 결합하는 보고서 세트의 경우, 이 차원은 성과가 가장 좋은 도메인이나 하위 도메인을 확인하는 데 중요합니다.

이 차원은 [페이지](page.md) 및 [사이트 섹션](site-section.md) 차원과 관련되어 있습니다. 페이지는 가장 세분화된 차원이고, 서버는 가장 덜 세분화된 차원이며, 사이트 섹션은 그 둘의 사이에 있습니다.

## 이 차원을 데이터로 채우기

이 차원은 이미지 요청의 [`server` 쿼리 문자열](/help/implement/validate/query-parameters.md)에서 데이터를 검색합니다. AppMeasurement는 [`server`](/help/implement/vars/page-vars/server.md) 변수를 사용하여 이 데이터를 수집합니다.

## 차원 항목

차원 항목은 사이트의 서버를 포함합니다. 조직은 사용자가 사용하려는 특정 차원 항목을 파악합니다. 일부 조직에서는 `window.location.hostname`을 사용하는 반면, 다른 조직에서는 사용자 지정 값을 만듭니다. 어떤 방법을 사용하든 일관된 방법을 사용하고 [솔루션 디자인 문서](/help/implement/prepare/solution-design.md)에 기록하도록 하십시오.
