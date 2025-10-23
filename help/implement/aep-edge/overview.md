---
title: Adobe Experience Platform Edge를 사용하여 Adobe Analytics 구현
description: Adobe Analytics에서 Experience Platform의 XDM 데이터 사용 개요
exl-id: 7d8de761-86e3-499a-932c-eb27edd5f1a3
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: 9845f1bc73b6cf5fd932c6896a50379ddd008c20
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 15%

---

# Adobe Experience Platform Edge Network를 사용하여 Adobe Analytics 구현

Adobe Experience Platform Edge Network를 사용하면 여러 제품을 대상으로 한 데이터를 중앙 위치에 전송할 수 있습니다. Edge Network는 적절한 정보를 원하는 제품에 전달합니다. 이 개념을 사용하면 특히 여러 데이터 솔루션에 걸쳐 구현 노력을 통합할 수 있습니다. Adobe Analytics은 Edge Network을 사용하여 데이터를에 보낼 수 있는 제품 중 하나입니다.

## Adobe Analytics에서 Edge Network 데이터를 처리하는 방법

Edge Network 데이터와 AppMeasurement 데이터로 전송된 데이터는 다르게 작동하므로 Edge Network 페이로드는 Adobe Analytics이 히트를 처리하는 방법을 결정합니다. 자세한 내용은 [Adobe Analytics의 Edge Network 이벤트 유형](hit-types.md)을 참조하십시오.

Adobe Experience Platform Edge Network으로 전송된 데이터는 **XDM 개체**, **데이터 개체** 및 **컨텍스트 데이터**&#x200B;의 세 가지 형식을 따를 수 있습니다. 데이터스트림이 데이터를 Adobe Analytics에 전달하면 Adobe Analytics에서 처리할 수 있는 형식으로 변환됩니다.

## `xdm` 개체

[XDM](https://experienceleague.adobe.com/ko/docs/experience-platform/xdm/home)&#x200B;(경험 데이터 모델)을 기반으로 만든 스키마를 따릅니다. XDM을 통해 이벤트의 일부로 정의된 필드를 유연하게 작업할 수 있습니다. Adobe Analytics과 관련된 사전 정의된 스키마를 사용하려면 [Adobe Analytics ExperienceEvent 스키마 필드 그룹](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/analytics-full-extension)을 스키마에 추가할 수 있습니다. 추가한 후에는 웹 SDK의 `xdm` 개체를 사용하여 이 스키마를 채워 보고서 세트로 데이터를 보낼 수 있습니다. 데이터가 Edge Network에 도착하면 XDM 개체가 Adobe Analytics에서 인식하는 형식으로 변환됩니다.

XDM 필드에 대한 전체 참조 및 Analytics 변수에 매핑되는 방법은 [Adobe Analytics에 대한 XDM 개체 변수 매핑](xdm-var-mapping.md)을 참조하십시오.

>[!TIP]
>
>나중에 [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing)&#x200B;(으)로 이동할 계획이라면 Adobe에서 Adobe Analytics 스키마 필드 그룹을 사용하지 않는 것이 좋습니다. 대신 Adobe에서는 [고유한 스키마를 만들고](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/upgrade-to-cja/schema/cja-upgrade-schema-architect)데이터 스트림 매핑을 사용하여 원하는 Analytics 변수를 채우는 것을 권장합니다. 이 전략은 Customer Journey Analytics으로 이동할 준비가 되었을 때 prop 및 eVar 스키마에 사용자를 잠그지 않습니다.

## `data` 개체

`xdm` 개체를 사용하는 대신 `data` 개체를 사용할 수 있습니다. 데이터 개체는 현재 AppMeasurement을 사용하는 구현에 맞게 디자인되어 웹 SDK으로의 업그레이드가 훨씬 더 쉬워집니다. Edge Network은 스키마를 준수하지 않아도 Adobe Analytics과 관련된 필드가 있는지 감지합니다.

데이터 개체 필드에 대한 전체 참조와 Analytics 변수에 매핑하는 방법은 [Adobe Analytics에 데이터 개체 변수 매핑](data-var-mapping.md)을 참조하십시오.

## 컨텍스트 데이터 변수

원하는 형식으로 Edge Network에 데이터를 전송합니다. `xdm` 또는 `data` 개체 필드에 자동으로 매핑되지 않는 모든 필드는 Adobe Analytics에 전달될 때 [컨텍스트 데이터 변수](/help/implement/vars/page-vars/contextdata.md)(으)로 포함됩니다. 그런 다음 [처리 규칙](/help/admin/tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md)을 사용하여 원하는 필드를 해당 Analytics 변수에 매핑해야 합니다.

예를 들어 다음과 같은 사용자 지정 XDM 스키마가 있는 경우:

```json
{
  "xdm": {
    "key": "value",
    "animal": {
      "species": "Raven",
      "size": "13 inches"
    },
    "array": [
      "v0",
      "v1",
      "v2"
    ],
    "objectArray":[{
      "ad1": "300x200",
      "ad2": "60x240",
      "ad3": "600x50"
    }]
  }
}
```

그런 다음 이러한 필드는 처리 규칙 인터페이스에서 사용할 수 있는 컨텍스트 데이터 키가 됩니다.

```javascript
a.x.key // value
a.x.animal.species // Raven
a.x.animal.size // 13 inches
a.x.array.0 // v0
a.x.array.1 // v1
a.x.array.2 // v2
a.x.objectarray.0.ad1 // 300x200
a.x.objectarray.1.ad2 // 60x240
a.x.objectarray.2.ad3 // 600x50
```

주어진 컨텍스트 데이터 변수 페이로드(키 및 값 포함)의 최대 크기는 32KB입니다. [`xdm`](xdm-var-mapping.md) 또는 [`data`](data-var-mapping.md) 개체에서 Adobe Analytics이 인식하도록 관련 필드를 조정하여 이 페이로드의 크기를 줄일 수 있습니다.
