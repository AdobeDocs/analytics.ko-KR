---
title: 웹 SDK JavaScript 라이브러리를 사용하여 Adobe Analytics에 데이터 보내기
description: JavaScript 라이브러리를 사용하여 Adobe Analytics으로 데이터를 전송할 수 있는 깔끔한 웹 SDK 구현으로 시작합니다.
hide: true
hidefromtoc: true
source-git-commit: d4c9bddf18311e13d025ed9d62c0636a33eb7b85
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# 웹 SDK JavaScript 라이브러리를 사용하여 Adobe Analytics에 데이터 보내기

이 구현 경로에는 Web SDK JavaScript 라이브러리를 사용한 새 웹 SDK 설치가 포함됩니다. 다른 구현 경로는 별도의 페이지에서 다룹니다.

* [Web SDK 태그 확장](web-sdk-tag-extension.md): Web SDK 태그 확장을 사용한 새로운 웹 SDK 설치입니다. Adobe Experience Platform 데이터 수집의 태그를 사용하여 구현을 관리한다는 점을 제외하면 웹 SDK JavaScript 라이브러리 접근 방식(이 페이지)과 유사합니다. XDM 스키마에 포함할 일반적인 Analytics 변수를 포함하는 Adobe Analytics ExperienceEvent 필드 그룹이 필요합니다.
* [Analytics 확장을 웹 SDK 확장으로](analytics-extension-to-web-sdk.md): Adobe Analytics 태그 확장 기능에서 웹 SDK 태그 확장 기능으로 이동하려면 유연하고 방법적인 접근 방식을 사용하십시오. 이 접근 방법에서는 조직이 Customer Journey Analytics과 같은 Adobe Experience Platform 서비스를 사용할 준비가 될 때까지 XDM을 사용할 필요가 없습니다. 사용 `data` 개체 대신 `xdm` Adobe에 데이터를 보낼 개체입니다.
* [웹 SDK JavaScript 라이브러리에 AppMeasurement](appmeasurement-to-web-sdk.md): 태그를 사용하지 않는 경우를 제외하고 웹 SDK로 마이그레이션하는 유연하고 체계적인 방법입니다. 대신 Adobe Analytics 데이터 수집 라이브러리( )를 수동으로 제거할 수 있습니다.`AppMeasurement.js`) 웹 SDK JavaScript 라이브러리( )로 대체합니다`alloy.js`).

## 이 구현 경로의 장단점

Web SDK JavaScript 라이브러리를 사용하여 데이터를 Adobe Analytics으로 전송하는 데에는 장점과 단점이 모두 있습니다. 각 옵션을 신중히 평가하여 조직에 가장 적합한 접근 방식을 결정하십시오.

| 장점 | 단점 |
| --- | --- |
| <ul><li>**직접 접근**: 이 구현 경로는 기존 Adobe Analytics 구현을 이동하는 접근 방식보다 더 간단합니다. 현재 Adobe Analytics 구현에 대해 걱정할 필요가 없는 경우 해당 웹 SDK XDM 필드를 채웁니다.</li><li>**사전 정의된 스키마**: 조직에 자체 스키마가 필요하지 않은 경우 Adobe Analytics에 맞게 구성된 스키마를 사용할 수 있습니다. 이 개념은 Customer Journey Analytics으로 이동할 때에도 적용됩니다. prop 및 eVar의 개념은 Customer Journey Analytics에 적용되지 않지만 prop 및 eVar를 단순 사용자 지정 차원으로 계속 사용할 수 있습니다.</li></ul> | <ul><li>**구현을 변경하려면 개발자의 개입이 필요합니다**: 웹 SDK 구현을 변경하려면 개발 팀과 함께 사이트에서 코드를 편집해야 합니다. 를 사용하는 접근 방식 [Web SDK 태그 확장](web-sdk-tag-extension.md) 이 단점을 방지합니다.</li><li>**특정 스키마를 사용하여 잠김**: 조직이 Customer Journey Analytics으로 이동할 때 Adobe Analytics 스키마를 계속 사용하도록 선택하거나 조직의 스키마(별도의 데이터 세트)로 마이그레이션해야 합니다. 조직에서 Customer Journey Analytics으로 이동할 때 Adobe Analytics 스키마와 별도의 데이터 세트로의 마이그레이션을 모두 방지하려면, Adobe에서는 다음 두 가지 방법 중 하나를 권장합니다.</li><ul><li>사용 `data` 개체: `data` 개체를 사용하면 XDM 스키마를 따르지 않고 Adobe Analytics으로 데이터를 보낼 수 있습니다. 조직의 스키마가 생성되면 데이터 스트림 매핑을 사용하여 매핑할 수 있습니다 `data` xdm에 대한 오브젝트 필드. 두 가지 모두 [Analytics 확장을 웹 SDK 확장으로](analytics-extension-to-web-sdk.md) 및 [웹 SDK JavaScript 라이브러리에 AppMeasurement](appmeasurement-to-web-sdk.md) 사용 `data` 개체.</li><li>Adobe Analytics 전체 건너뛰기: Web SDK를 구현하는 경우 해당 데이터를 Adobe Experience Platform의 데이터 세트로 전송하여 Customer Journey Analytics에서 사용할 수 있습니다. 원하는 스키마를 사용할 수 있습니다. Adobe Analytics은 이 워크플로에 전혀 포함되지 않으므로 Adobe Analytics ExperienceEvent 필드 그룹이 필요하지 않습니다. 이 방법은 기술적인 부채를 최소한으로 발생시키지만 Adobe Analytics을 완전히 배제시킵니다.</li></ul></ul> |
