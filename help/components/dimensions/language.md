---
title: 언어
description: 브라우저의 기본 언어 설정입니다.
feature: Dimensions
exl-id: 590406a4-d336-42c7-8048-e7cd8e611d43
TQID: https://experienceleague.adobe.com/KC8nBiwUbQaE8Wi5OVKdjwP-sTijGYYMBK74M-TnOFs
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 65%
---
# 언어

&#39;언어&#39; [차원](overview.md)은(는) 방문자가 콘텐츠를 볼 때 선호하는 상위 언어들을 보여줍니다. 이 차원은 현지화 작업에 도움이 되도록 방문자가 가장 자주 사용하는 선호 언어를 알려는 경우 중요합니다.

>[!NOTE]
>
>이 차원은 사이트의 언어를 수집하지 않습니다. 차원에서 사이트의 언어를 수집하려는 경우 [eVar](evar.md)와 같은 사용자 지정 변수를 사용하는 것이 좋습니다.

## 이 차원을 데이터로 채우기

이 차원은 Adobe 내부의 조회 테이블을 참조합니다. 조회 값은 이미지 요청에 있는 `Accept-Language` HTTP 헤더를 기반으로 합니다. AppMeasurement 또는 Web SDK(태그) 구현에서 즉시 작동하며 설정할 변수가 없습니다.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | 없음(HTTP 헤더) |
| **웹 SDK/XDM 필드** | 없음(HTTP 헤더) |
| **쿼리 매개 변수** | 없음(`Accept-Language` 헤더 사용) |
| **XML 태그** | [`<language>`](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference#variables) |
| **바이트 제한** | 해당 없음 |
| **지속성** | 해당 사항 없음 |

## 차원 항목

차원 항목에는 방문자가 선호하는 언어의 친숙한 이름이 포함됩니다. 예로는 `"English (United States)"`, `"English (United Kingom)"`, `"Chinese (China)"` 및 `"Spanish (Spain)"`가 있습니다. 이미지 요청의 HTTP 헤더에 올바른 언어가 포함되지 않으면 차원 항목은 `"None"`이 됩니다.
