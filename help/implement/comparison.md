---
title: 구현 방법 비교
description: Adobe Analytics에 데이터를 전송하는 각 방법의 이점을 참조하십시오.
source-git-commit: 96a5daaf9d8358e4a5222a20f64c381cb8340ab1
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 2%

---

# 구현 방법 비교

Adobe Analytics을 구현하는 각 방법이 서로 어떻게 비교되는지 확인하십시오. 이 테이블을 사용하면 조직에서 Adobe으로 데이터를 보내는 가장 이상적인 방법을 결정할 수 있습니다.

|  | AppMeasurement | Adobe Analytics 확장 | Web SDK | 웹 SDK 확장 |
| --- | --- | --- | --- | --- |
| 구현 요구 사항 | 참조 `AppMeasurement.js` 각 페이지에서 변수를 정의하고, `s.t()` | 각 페이지에서 태그 로더를 참조하고, 데이터 수집 UI를 사용하여 변수를 정의하고 데이터를 Adobe에 보냅니다 | 참조 `Alloy.js` 각 페이지에서 `alloy("sendEvent",{})` 원하는 데이터가 포함된 JSON 개체를 전송하려면 다음을 수행하십시오 | 각 페이지에서 태그 로더를 참조하고, 데이터 수집 UI를 사용하여 데이터를 전송할 JSON 개체를 설정합니다 |
| 데이터 대상 | Adobe Analytics으로 직접 전송 | Adobe Analytics으로 직접 전송 | Adobe Experience Platform Edge로 전송되고, 여기서 Adobe Analytics에 데이터를 전달합니다 | Adobe Experience Platform Edge로 전송되고, 여기서 Adobe Analytics에 데이터를 전달합니다 |
| 구현을 조정하는 데 어려움 | 구현 변경 시마다 웹 사이트 코드에 대한 액세스 필요 | 웹 사이트 코드는 로더 태그를 설치하려면 한 번만 변경하면 됩니다. 데이터 수집 UI에서 추가 구현 업데이트를 모두 수행할 수 있습니다 | 구현 변경 시마다 웹 사이트 코드에 대한 액세스 필요 | 웹 사이트 코드는 로더 태그를 설치하려면 한 번만 변경하면 됩니다. 데이터 수집 UI에서 추가 구현 업데이트를 모두 수행할 수 있습니다 |
| A4T 처리 방법 | A4T 호출은 Adobe으로 전송된 히트에 포함됩니다 | A4T 호출은 Adobe으로 전송된 히트에 포함됩니다 | A4T 호출은 별도의 히트로 전송됩니다 | A4T 호출은 별도의 히트로 전송됩니다 |
| 레퍼러를 처리하는 방법 |