---
title: 동적 조회
description: 동적 조회가 무엇이며 이를 활성화하는 방법에 대해 알아봅니다. 통신사, 모바일 속성 및 운영 체제 유형을 포함합니다.
exl-id: 12327239-06a2-4092-b27d-b94da39abf30
feature: Data Feeds
source-git-commit: 6b8366b451be1612331f517ee80fd57744deafdc
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---

# 동적 조회

동적 조회를 사용하면 데이터 피드에서 추가 조회 파일을 수신할 수 있습니다. 그렇지 않으면 사용할 수 없습니다. 이 설정을 사용하면 각 데이터 피드 파일과 함께 다음 조회 테이블을 전송할 수 있습니다.

* **통신사 이름**: `carrier` 열에 대한 추가 컨텍스트를 제공합니다. 포함된 파일 이름은 `carrier.tsv`입니다.
* **모바일 특성**: 각 모바일 장치에 대해 추적된 모든 기능을 포함하여 `mobile_id` 열에 대한 추가 컨텍스트를 제공합니다. 포함된 파일 이름은 `mobile_attributes.tsv`입니다.
* **운영 체제 유형**: `os` 열에 대한 대체 컨텍스트를 제공합니다. `operating_systems.tsv`과(와) `operating_system_type.tsv`은(는) 모두 `os` 열을 키로 사용하지만 `operating_system_type.tsv`만 동적 조회입니다.

## 동적 조회 활성화

언급된 조회 파일을 수신하려면 다음 전제 조건을 모두 충족해야 합니다.

* 키 열은 데이터 피드에 포함되어야 합니다.
   * `carrier.tsv`의 경우 `carrier`을(를) 포함해야 합니다.
   * `mobile_attributes.tsv`의 경우 `mobile_id`을(를) 포함해야 합니다.
   * `operating_system_type.tsv`의 경우 `os`을(를) 포함해야 합니다.
* 다음 열은 **제외됨**&#x200B;이어야 합니다. 이러한 열이 데이터 피드에 포함되어 있으면 `mobile_attributes.tsv` 동적 조회가 포함되지 않습니다.
   * `user_agent`
   * `ch_hdr`
   * `ch_js`

데이터 피드가 열 포함 및 제외 요구 사항을 충족하면 데이터 피드 ID 및 동적 조회를 활성화하기 위한 요청을 통해 고객 지원 센터에 문의하십시오.

## 조회 헤더 참조

이러한 조회 파일에 대한 열 헤더는 시간이 지나도 변경되지 않으므로 헤더가 각 데이터 피드 파일에 포함되지 않습니다. 이 열 헤더를 참조로 사용하거나 해당 `.tsv` 파일을 다운로드하십시오.

+++**통신사 이름**
[carrier_headers.tsv](assets/carrier_headers.tsv)을 다운로드하거나 아래 헤더를 참조하십시오.

`carrier`
`Carrier Name`
+++

+++**모바일 특성**
[mobile_attributes_headers.tsv](assets/mobile_attributes_headers.tsv)을 다운로드하거나 아래 헤더를 참조하십시오.

`mobile_id`
`Manufacturer`
`Device`
`Device Type`
`Operating System`
`Diagonal Screen Size`
`Screen Height`
`Screen Width`
`Cookie Support`
`Color Depth`
`MP3 Audio Support`
`AAC Audio Support`
`AMR Audio Support`
`Midi Monophonic Audio Support`
`Midi Polyphonic Audio Support`
`QCELP Audio Support`
`GIF87 Image Support`
`GIF89a Image Support`
`PNG Image Support`
`JPG Image Support`
`3GPP Video Support`
`MPEG4 Video Support`
`3GPP2 Video Support`
`WMV Video Support`
`MPEG4 Part 2 Video Support`
`Stream MP4 AAC LC Video Support`
`Stream 3GP H264 Level 10b Video Support`
`Stream 3GP AAC LC Video Support`
`3GP AAC LC Video Support`
`Stream MP4 H264 Level 11 Video Support`
`Stream MP4 H264 Level 13 Video Support`
`Stream 3GP H264 Level 12 Video Support`
`Stream 3GP H264 Level 11 Video Support`
`Stream 3GP H264 Level 10 Video Support`
`Stream 3GP H264 Level 13 Video Support`
`3GP AMR NB Video Support`
`3GP AMR WB Video Support`
`MP4 H264 Level 11 Video Support`
`3GP H263 Video Support`
`MP4 H264 Level 13 Video Support`
`Stream 3GP H263 Video Support`
`Stream 3GP AMR WB Video Support`
`3GP H264 Level 10b Video Support`
`MP4 ACC LC Video Support`
`Stream 3GP AMR NB Video Support`
`3GP H264 Level 10 Video Support`
`3GP H264 Level 13 Video Support`
`3GP H264 Level 11 Video Support`
`3GP H264 Level 12 Video Support`
`Stream HTTP Live Streaming Video Support`
+++

+++**운영 체제 유형**
[operating_system_type_headers.tsv](assets/operating_system_type_headers.tsv)을 다운로드하거나 아래 헤더를 참조하십시오.

`os`
`Operating System Type`
+++
