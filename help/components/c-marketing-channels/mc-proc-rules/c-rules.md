---
title: 마케팅 채널의 처리 규칙
description: 마케팅 채널 처리 규칙은 채널에 할당된 기준을 방문자 히트가 충족하는지 여부를 결정합니다. 규칙을 통해 사이트에서 방문자가 만드는 모든 히트가 처리됩니다. 규칙이 채널에 대한 기준을 충족하지 않는 경우 또는 규칙이 올바르게 구성되지 않은 경우, 시스템이 히트를 [식별된 채널 없음]에 할당합니다.
translation-type: tm+mt
source-git-commit: ea4d9e6c9396032fe323de594cb43eecbf97aa15

---


# 마케팅 채널의 처리 규칙

마케팅 채널 처리 규칙은 채널에 할당된 기준을 방문자 히트가 충족하는지 여부를 결정합니다. 규칙을 통해 사이트에서 방문자가 만드는 모든 히트가 처리됩니다. 규칙이 채널에 대한 기준을 충족하지 않는 경우 또는 규칙이 올바르게 구성되지 않은 경우, 시스템이 히트를 [식별된 채널 없음]에 할당합니다.

다음은 규칙을 만드는 중요한 지침입니다.

* 처리를 원하는 순서대로 규칙을 정렬합니다.
*  [기타]와 같은 다목적 캐치(catch-all) 규칙을 목록의 끝에 포함시킵니다. 이 규칙은 내부 트래픽을 제외하고 외부 트래픽을 식별합니다.

   [식별된 채널 없음](/help/components/c-marketing-channels/mc-faq/c-faq.md#no-channel-identified)을 참조하십시오.

> [!NOTE] 이러한 규칙은 마케팅 채널 외부의 보고에 영향을 주지 않지만 마케팅 채널 데이터 수집에는 영향을 줍니다. 이러한 규칙으로 수집한 데이터는 100% 영구적이며 데이터를 수집한 후에 수정한 규칙은 되돌릴 수 없습니다. It is strongly recommended to review and consider all circumstances before saving [!UICONTROL Marketing Channel Processing Rules] to mitigate data being collected in incorrect channels.

## 전제 조건

* 마케팅 채널 시작에서 [개념 정보를 검토하십시오](/help/components/c-marketing-channels/getting-started/c-getting-started-mchannel.md).
* 규칙을 할당할 수 있도록 하나 이상의 채널을 만듭니다. See [Add marketing channels.](/help/components/c-marketing-channels/mark-channel-mgr/c-channels.md)
