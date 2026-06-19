---
title: 히트 유형
description: 히트가 전경 히트인지 배경 히트인지 확인합니다.
feature: Dimensions
exl-id: b922adbb-fe36-46c7-aab2-b9471de07d2f
TQID: https://experienceleague.adobe.com/6G-XpOMMZGum9LAQzKn0zGdeNRmHFPpmYizqRrbKuUE
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: c4cb071e-4667-4fb1-b1f1-d8994549cfb2id: c77ba355-6681-41fe-b719-563d3f507fdbid: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: d4db20e3498d54162806b3fdef0b34f45c93a6ff
workflow-type: tm+mt
source-wordcount: 164
ht-degree: 34%

---

# 히트 유형

&#39;히트 유형&#39; [차원](overview.md)은(는) 히트가 Adobe 데이터 수집 서버로 전송될 때 모바일 앱이 전경에 있는지 배경에 있는지를 결정합니다. 이 차원은 모바일 애플리케이션용 데이터가 포함된 보고서 세트에만 관련이 있습니다. AppMeasurement을 통해 수집된 브라우저 데이터는 항상 히트를 `"Foreground"`(으)로 보고합니다.

## 이 차원을 데이터로 채우기

이 차원은 버전 4.13.6 이상에서 모든 Mobile SDK 구현에 대해 즉시 작동합니다. 모바일 SDK은 각 히트가 전경에서 발생했는지 배경에서 발생했는지 여부를 나타내기 위해 [`customerPerspective`](/help/implement/vars/page-vars/customerperspective.md) 변수(`cp` 쿼리 매개 변수)를 설정합니다. 모바일 SDK을 사용하지 않는 경우 `"Foreground"` 아래에 모든 히트가 나열됩니다. [가상 보고서 세트](../vrs/vrs-mobile-visit-processing.md)를 구성할 때 **[!UICONTROL 배경 히트 수로 새로운 방문이 시작되지 않도록 차단]**&#x200B;을 선택하면 배경 히트 수는 [[!UICONTROL 방문 수]](../metrics/visits.md) 및 [[!UICONTROL 고유 방문자 수]](../metrics/unique-visitors.md)를 부풀리지 않습니다.

## 차원 항목

차원 항목은 `"Foreground"` 및 `"Background"`를 포함합니다. 배경 히트 수는 추적된 애플리케이션이 배경에 있는 모바일 장치에서만 발생합니다.
