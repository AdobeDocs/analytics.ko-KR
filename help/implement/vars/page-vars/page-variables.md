---
title: 페이지 변수
description: 개별 페이지에서 값을 설정합니다.
feature: Appmeasurement Implementation
exl-id: 321d0db2-61a3-478e-ab51-8e06c7b2bb7b
role: Admin, Developer
TQID: https://experienceleague.adobe.com/mWfMumcPTklFPKUiGIOatDbC0WKW5RDYH56rXTFk3ZY
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: e7d92df1-c5ba-4e93-85df-f83171b889beid: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: d4db20e3498d54162806b3fdef0b34f45c93a6ff
workflow-type: tm+mt
source-wordcount: 148
ht-degree: 47%

---

# 페이지 변수 개요

페이지 변수는 보고의 차원 및 지표에 대한 값을 결정합니다.

다음 목록은 구현에 자주 사용되는 변수입니다.

* [`pageName`](pagename.md): 페이지 이름.
* [`campaign`](campaign.md): 이 변수를 캠페인 추적에 대한 쿼리 문자열 매개 변수로 설정합니다.
* [`events`](events/events-overview.md): 보고에 사용할 지표를 채웁니다.
* [`products`](products.md): eCommerce 사이트가 있는 경우 방문자가 제품을 보거나 구매할 때 이 변수를 설정하십시오.

## 폐기된 페이지 변수

다음 페이지 변수가 사용되지 않습니다. 기존 구현에서 이러한 문제가 발생하는 경우 참조할 수 있도록 여기에 문서화되어 있습니다.

* **`hier`**: 보고를 위해 사이트 구조를 캡처하도록 계층 변수(`hier1`-`hier5`)를 구현했습니다. 사용이 중단되었으며 Analysis Workspace에서 사용할 수 있는 차원이 아닙니다. 대신 [eVars](evar.md) 및 분류를 사용하십시오.
* **`state`**: 일반적으로 배송 또는 청구 양식을 통해 방문자가 입력한 미국 주를 캡처했습니다. 대신 Adobe이 방문자의 지리적 위치에서 자동으로 채워지는 [[!UICONTROL 미국 주]](/help/components/dimensions/us-states.md) 차원을 사용하십시오.
