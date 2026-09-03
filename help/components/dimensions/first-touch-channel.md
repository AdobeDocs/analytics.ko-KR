---
title: 첫 번째 터치 채널
description: 방문자의 참여 만료 내 첫 번째 마케팅 채널입니다.
feature: Dimensions
exl-id: cca9794c-1305-4e54-aa13-809b9ebc6230
TQID: https://experienceleague.adobe.com/1XBUjwxlZXmhXJtQZgpv9yU5Fwhns-bb9Q7BcP5S30Q
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2: id: c80b99d6-98b9-4aeb-b5c4-933ef2ef705cid: f836f655-eebe-4b76-82bc-697955ec1ce3id: fab61dd8-112a-4e5e-ad5f-fb0240b7a60b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 284
ht-degree: 91%

---

# 첫 번째 터치 채널

첫 번째 터치 채널 [차원](overview.md)은(는) 해당 방문자의 참여 기간(기본적으로 30일) 동안 방문자가 일치하는 첫 번째 마케팅 채널을 보고합니다. 이 차원은 초기 사이트 트래픽을 유도하는 마케팅 채널을 파악하여 가장 효과적인 영역에서 마케팅 활동에 집중할 수 있도록 하는 데 유용합니다.

## 이 차원을 데이터로 채우기

이 차원은 [마케팅 채널 관리자](/help/admin/tools/manage-rs/edit-settings/marketing-channels/c-channels.md)에서 정의한 채널 이름을 직접 참조합니다.

Adobe 데이터 수집 서버로 전송된 모든 히트는 보고서 세트의 마케팅 채널 처리 규칙을 통해 실행됩니다. 해당 마케팅 채널이 히트와 연결되는 일치를 찾을 때까지 각 규칙을 숫자 순서로 반복합니다. 첫 번째 터치 채널은 방문자 참여 기간 (기본적으로 30일)보다 오랫동안 방문자가 사이트를 방문하지 않을 때까지 방문자와 함께 유지됩니다.

이 차원을 특정 값으로 설정하려면 다음 단계를 수행해야 합니다.

* 원하는 차원 항목을 보고서 세트 설정 아래의 마케팅 채널 관리자에서 채널로 설정합니다.
* 히트에 대해 원하는 기준을 포함하는 마케팅 채널 처리 규칙을 설정합니다.
* 사이트에 대한 방문자의 히트는 마케팅 채널 처리 규칙에 설명된 기준과 일치해야 _하며_ 방문자의 참여 기간에 그렇게 하려면 첫 번째 마케팅 채널 값이어야 합니다.

후속 히트가 다른 마케팅 채널의 기준과 일치하는 경우 이 차원은 새 마케팅 채널로 덮어써지지 않습니다.

## 차원 항목

차원 항목에 마케팅 채널 관리자의 채널 이름이 포함됩니다. 기본적으로 값에는 `"Paid search"`, `"Natural search"`, `"Display"`, `"Email"`, `"Affiliate"`, `"Direct"`, `"Internal"`, `"Social networks"` 및 `"Referring domains"`이 포함됩니다. 마케팅 채널 관리자에서 이 차원의 값에 영향을 주는 채널을 추가하거나 삭제할 수 있습니다.
