---
title: AMO EF ID
description: Adobe Advertising 통합에 사용되는 Adobe Media Optimizer EF ID입니다.
feature: Dimensions
source-git-commit: 408d8db0d1e3c8301a066fe54d611ec7b8e3418a
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 4%

---

# AMO EF ID

**[!UICONTROL AMO EF ID]**&#x200B;은(는) Adobe Advertising 통합에 사용되는 광고 클릭 식별자입니다. Adobe Advertising이 방문자 수준에서 활동을 온라인 클릭 또는 광고 노출과 연결하는 데 사용하는 고유한 토큰입니다. [Analytics for Advertising](https://experienceleague.adobe.com/en/docs/advertising/integrations/analytics/overview) 통합을 사용하도록 설정하면 차원이 자동으로 만들어집니다.

## 이 차원을 데이터로 채우기

이 차원은 여러 가지 방법으로 값을 수집합니다.

* 클릭스루 트래픽의 경우 일반적으로 광고 기반 트래픽이 사이트로 들어오는 페이지에서 `ef_id`페이지 URL[의 ](page-url.md) 쿼리 문자열 매개 변수에서 데이터가 수집됩니다.
* URL에 추적 코드가 포함되어 있지 않지만 Adobe Advertising JavaScript이 이전 2분 내에 클릭을 감지하면 클릭스루 트래픽을 캡처할 수도 있습니다.
* 지원되는 뷰스루 트래픽의 경우 Adobe Advertising에서 보충 ID(`SDID`)를 사용하여 백엔드의 값을 보완합니다.

>[!NOTE]
>
>EF ID는 대/소문자를 구분합니다. 구현에서 URL 추적을 소문자로 강제하는 경우 Adobe Advertising에서 EF ID를 인식하지 못합니다.

## 차원 항목

Dimension 항목에는 지원되는 광고 네트워크에서 생성한 광고 클릭 식별자가 포함됩니다. 문자열 형식은 이 문자열을 생성한 네트워크 및 채널에 따라 다릅니다.

### Google 광고 검색 광고

```text
{gclid}:G:{s}
```

* **`gclid`**: Google 클릭 ID(GCLID)입니다.
* **`s`**: 네트워크 유형(검색의 경우 `"s"`).

### Microsoft Advertising 검색 광고

```text
{msclkid}:G:{s}
```

* **`msclkid`**: Microsoft 클릭 ID(MSCLKID)입니다.
* **`s`**: 네트워크 유형(검색의 경우 `"s"`).

### 다른 검색 엔진에 광고 및 검색 광고 표시

```text
{amovid}:{ts}:{channel}
```

* **`amovid`**: 서퍼 ID라고도 하는 Adobe Advertising 방문자 ID입니다.
* **`ts`**: Adobe Advertising에서 생성된 타임스탬프입니다.
* **`channel`**: 클릭 또는 노출을 담당하는 채널 유형:
   * **`d`**: DSP 디스플레이 광고 클릭(디스플레이 클릭스루)입니다.
   * **`i`**: DSP 디스플레이 광고(디스플레이 뷰스루)의 노출 횟수입니다.
   * **`s`**: 검색 광고 클릭(검색 클릭스루).

### 예

```text
CjwKCAiAkbbMBhB2EiwANbxtbb9L573Dys0rjTDqcMo3x7tv2yEfh1RGb8exG9N892NoMqAzMBEGmhoCWxwQAvD_BwE:G:s
06207ca63ae6f4fa832197585547393c:20260301111101:i
WcmibgAAAHJK1RyY:1551968087687:d
```
