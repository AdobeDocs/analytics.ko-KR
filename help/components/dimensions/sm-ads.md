---
title: 스트리밍 미디어 서비스 광고 차원
description: 보고서 세트에 대해 [!UICONTROL 미디어 광고]를 사용하도록 설정하는 경우 사용할 수 있는 차원입니다.
feature: Dimensions
exl-id: 3f17bacc-8c36-499a-a863-9298e2d54370
TQID: https://experienceleague.adobe.com/5d5RQ-2dkRD-R5U0iVyApP7WdCH2O1Rsk-qlPLYJm9c
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 1be0f3577403db7cf9bd40ef9e7c4bfcfa6c0b17
workflow-type: tm+mt
source-wordcount: 353
ht-degree: 2%

---

# 스트리밍 미디어 서비스 광고 차원

Streaming Media 서비스 및 차원은 Streaming Media 수집 라이브러리를 통해 수집된 데이터에 대한 보충 보고 기능을 제공합니다. 이러한 차원에는 **[!UICONTROL 스트리밍 미디어용 Adobe Analytics 추가 기능]**&#x200B;이 필요합니다. 자세한 내용은 Adobe 계정 팀에 문의하십시오.

이 차원을 사용하려면 보고서 세트에 대해 [[!UICONTROL 미디어 보고]](/help/admin/tools/manage-rs/edit-settings/media-management.md)에서 **[!UICONTROL 미디어 광고]**&#x200B;를 사용하도록 설정하십시오.

다음 차원을 사용할 수 있습니다.

* [[!UICONTROL 광고]](https://experienceleague.adobe.com/ko/docs/media-analytics/using/reporting/dimensions/ad)
* [[!UICONTROL Pod 위치의 광고]](https://experienceleague.adobe.com/ko/docs/media-analytics/using/reporting/dimensions/ad-in-pod-position)
* [[!UICONTROL 광고 길이(변수)]](https://experienceleague.adobe.com/ko/docs/media-analytics/using/reporting/dimensions/ad-length)
* [[!UICONTROL 광고 이름(변수)]](https://experienceleague.adobe.com/ko/docs/media-analytics/using/reporting/dimensions/ad-name)
* [[!UICONTROL 광고 플레이어 이름]](https://experienceleague.adobe.com/ko/docs/media-analytics/using/reporting/dimensions/ad-player-name)
* [[!UICONTROL 광고 pod]](https://experienceleague.adobe.com/ko/docs/media-analytics/using/reporting/dimensions/ad-pod)
* [[!UICONTROL 광고주]](https://experienceleague.adobe.com/ko/docs/media-analytics/using/reporting/dimensions/advertiser)
* [[!UICONTROL 캠페인 ID]](https://experienceleague.adobe.com/ko/docs/media-analytics/using/reporting/dimensions/campaign-id)

위의 차원 외에도 Adobe은 자동으로 다음 분류 차원을 생성합니다. 이러한 차원을 사용하는 보고서를 보려면 분류 데이터를 업로드해야 합니다.

| 분류 이름 | 상위 차원 |
| --- | --- |
| [[!UICONTROL 자산 ID]](https://experienceleague.adobe.com/ko/docs/media-analytics/using/reporting/dimensions/asset-id) | [[!UICONTROL 콘텐츠]](sm-core.md) |
| [[!UICONTROL 콘텐츠 등급]](https://experienceleague.adobe.com/ko/docs/media-analytics/using/reporting/dimensions/content-rating) | [[!UICONTROL 콘텐츠]](sm-core.md) |
| [[!UICONTROL 첫 방송 날짜]](https://experienceleague.adobe.com/ko/docs/media-analytics/using/reporting/dimensions/first-air-date) | [[!UICONTROL 콘텐츠]](sm-core.md) |
| [[!UICONTROL 첫 번째 디지털 날짜]](https://experienceleague.adobe.com/ko/docs/media-analytics/using/reporting/dimensions/first-digital-date) | [[!UICONTROL 콘텐츠]](sm-core.md) |
| [[!UICONTROL 광고 길이]](https://experienceleague.adobe.com/ko/docs/media-analytics/using/reporting/dimensions/ad-length) | [!UICONTROL 광고] |
| [[!UICONTROL 광고 이름]](https://experienceleague.adobe.com/ko/docs/media-analytics/using/reporting/dimensions/ad-name) | [!UICONTROL 광고] |
| [[!UICONTROL Creative ID]](https://experienceleague.adobe.com/ko/docs/media-analytics/using/reporting/dimensions/creative-id) | [!UICONTROL 광고] |
| [[!UICONTROL Pod 이름]](https://experienceleague.adobe.com/ko/docs/media-analytics/using/reporting/dimensions/pod-name) | [!UICONTROL 광고 pod] |
| [[!UICONTROL Pod 위치]](https://experienceleague.adobe.com/ko/docs/media-analytics/using/reporting/dimensions/pod-position) | [!UICONTROL 광고 pod] |

해당 지표는 [스트리밍 미디어 서비스 광고 지표](../metrics/sm-ads.md)를 참조하십시오.
