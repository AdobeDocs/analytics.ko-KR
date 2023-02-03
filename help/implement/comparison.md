---
title: 구현 방법 비교
description: Adobe Analytics로 데이터를 전송하는 각 방법의 이점을 확인하십시오.
source-git-commit: 96a5daaf9d8358e4a5222a20f64c381cb8340ab1
workflow-type: ht
source-wordcount: '273'
ht-degree: 100%

---

# 구현 방법 비교

Adobe Analytics를 구현하는 각 방법을 서로 비교하는 방법을 확인하십시오. 이 테이블은 조직에서 Adobe로 데이터를 보내는 가장 이상적인 방법을 결정하는 데 도움을 줄 수 있습니다.

|  | AppMeasurement | Adobe Analytics 확장 | Web SDK | Web SDK 확장 |
| --- | --- | --- | --- | --- |
| 구현 요구 사항 | 각 페이지에서 `AppMeasurement.js` 참조, 변수 정의, `s.t()`를 사용하여 데이터 전송 | 각 페이지에서 태그 로더 참조, 데이터 수집 UI를 사용하여 변수 정의 및 Adobe로 데이터 전송 | 각 페이지에서 `Alloy.js` 참조, `alloy("sendEvent",{})`를 사용하여 원하는 데이터가 포함된 JSON 오브젝트 전송 | 각 페이지에서 태그 로더 참조, 데이터 수집 UI를 사용하여 데이터 전송할 JSON 오브젝트 수립 |
| 데이터 대상 | Adobe Analytics로 직접 전송 | Adobe Analytics로 직접 전송 | Adobe Experience Platform Edge로 전송, 데이터를 Adobe Analytics로 전달 | Adobe Experience Platform Edge로 전송, 데이터를 Adobe Analytics로 전달 |
| 구현 조정의 어려움 | 모든 구현 변경에 대해 웹 사이트 코드에 대한 액세스 권한이 필요합니다. | 로더 태그를 설치하려면 웹 사이트 코드를 한 번만 변경하면 됩니다. 모든 추가 구현 업데이트는 데이터 수집 UI에서 수행할 수 있습니다. | 모든 구현 변경에 대해 웹 사이트 코드에 대한 액세스 권한이 필요합니다. | 로더 태그를 설치하려면 웹 사이트 코드를 한 번만 변경하면 됩니다. 모든 추가 구현 업데이트는 데이터 수집 UI에서 수행할 수 있습니다. |
| A4T 처리 방법 | A4T 호출은 Adobe로 전송된 히트에 포함됩니다. | A4T 호출은 Adobe로 전송된 히트에 포함됩니다. | A4T 호출은 별도의 히트로 전송됩니다. | A4T 호출은 별도의 히트로 전송됩니다. |
| 레퍼러 처리 방법 |