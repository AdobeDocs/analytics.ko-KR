---
description: 마케팅 채널 처리 규칙은 채널에 할당된 기준을 방문자 히트가 충족하는지 여부를 결정합니다. 규칙을 통해 사이트에서 방문자가 만드는 모든 히트가 처리됩니다. 규칙이 채널에 대한 기준을 충족하지 않는 경우 또는 규칙이 올바르게 구성되지 않은 경우, 시스템이 히트를 [식별된 채널 없음]에 할당합니다.
seo-description: 마케팅 채널 처리 규칙은 채널에 할당된 기준을 방문자 히트가 충족하는지 여부를 결정합니다. 규칙을 통해 사이트에서 방문자가 만드는 모든 히트가 처리됩니다. 규칙이 채널에 대한 기준을 충족하지 않는 경우 또는 규칙이 올바르게 구성되지 않은 경우, 시스템이 히트를 [식별된 채널 없음]에 할당합니다.
seo-title: 마케팅 채널의 처리 규칙
solution: Analytics
subtopic: 마케팅 채널
title: 마케팅 채널의 처리 규칙
topic: Reports and Analytics
uuid: f6394f4b-a244-48e9-9892-7dfbceb5fc9
translation-type: tm+mt
source-git-commit: 57fe1f6d613b9f54a5191ac8684d36bccfebf4e5

---


# 마케팅 채널의 처리 규칙

마케팅 채널 처리 규칙은 채널에 할당된 기준을 방문자 히트가 충족하는지 여부를 결정합니다. 규칙을 통해 사이트에서 방문자가 만드는 모든 히트가 처리됩니다. 규칙이 채널에 대한 기준을 충족하지 않는 경우 또는 규칙이 올바르게 구성되지 않은 경우, 시스템이 히트를 [식별된 채널 없음]에 할당합니다.

다음은 규칙을 만드는 중요한 지침입니다.

* 처리를 원하는 순서대로 규칙을 정렬합니다.
*  [기타]와 같은 다목적 캐치(catch-all) 규칙을 목록의 끝에 포함시킵니다. 이 규칙은 내부 트래픽을 제외하고 외부 트래픽을 식별합니다.

   See [No Channel Identified.](/help/components/c-marketing-channels/c-faq.md#no-channel-identified)

> [!NOTE] 이러한 규칙은 마케팅 채널 외부의 보고에 영향을 주지 않지만 마케팅 채널 데이터 수집에 영향을 줍니다. 이러한 규칙으로 수집한 데이터는 100% 영구적이며 데이터를 수집한 후에 수정한 규칙은 되돌릴 수 없습니다. 데이터가 잘못된 채널에서 수집되는 일을 막을 수 있도록 [!UICONTROL 마케팅 채널 처리 규칙]을 저장하기 전에 모든 상황을 검토 및 고려하는 것이 좋습니다.

## 전제 조건

* 마케팅 채널 시작 [및 마케팅 채널 보고서](/help/components/c-marketing-channels/c-getting-started-mchannel.md) 정보에서 개념 [정보를 검토하십시오](/help/components/c-marketing-channels/c-overview.md).

* 규칙을 할당할 수 있도록 하나 이상의 채널을 만듭니다.

   자세한 내용은 [마케팅 채널 추가](/help/components/c-marketing-channels/c-channels.md)를 참조하십시오.
