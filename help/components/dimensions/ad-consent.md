---
title: 광고 플랫폼 동의
description: 타사 광고 공급자에 대한 광고 동의에 대한 구성을 참조하십시오.
feature: Dimensions
exl-id: bf63112d-7d20-4e35-9a59-5be21135ae51
source-git-commit: 5df5cffbb6abf712cb36fd807ef54b8ebaae1c73
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 3%

---

# 광고 플랫폼 동의

&#39;광고 플랫폼 동의&#39; [차원](overview.md)은(는) Google, Meta 등과 같은 타사 광고 공급자에게 데이터를 보내는 데 동의가 수집되었는지 여부를 표시합니다.

현재 이 차원은 Google에만 사용됩니다. 유럽의 개인 정보 보호 규정, 디지털 시장법(DMA)으로 인해 Google은 서버에 전송하여 유럽에서 수집한 데이터에 동의 수집 여부를 표시해야 합니다. 일부 Analytics 고객은 Adobe Advertising을 통해 이벤트 데이터를 Google에 전환 이벤트로 보냅니다.

향후 이 차원을 사용하여 다른 타사 광고 공급자에 대한 추가 동의 정보의 인코딩을 지원할 수 있습니다.

## 이 차원을 데이터로 채우기

이 차원은 다음 [컨텍스트 데이터 변수](/help/implement/vars/page-vars/contextdata.md)에서 데이터를 수집합니다.

* `contextData.['adConsent']`

컨텍스트 데이터 변수를 Google 동의 필드에 대한 관련 값으로 채웁니다

* `ad_user_data`(첫 번째 문자) 및
* `ad_personalization`(두 번째 문자).

자세한 내용은 [Google Ads API 참조의 동의](https://developers.google.com/google-ads/api/reference/rpc/v15/Consent)를 참조하십시오.

이러한 각 필드에 가능한 값은 다음과 같습니다.

| 값 | ad_user_data | ad_personalization |
|:-:|---|---|
| `Y` | 광고 사용자 데이터에 대해 Google에 동의합니다. | 광고 개인화를 위해 Google에 동의합니다. |
| `N` | 광고 사용자 데이터에 대한 Google의 동의를 거부합니다. | 광고 개인화를 위해 Google에 동의합니다. |
| `U` | 지정되지 않음. | 지정되지 않음. |

아래 예제는 광고 사용자 데이터에 대해 Google에 동의하지만 광고 개인화에 대해서는 동의하지 않습니다.

```
contextData.['adConsent'] = "YN..."
```

첫 번째 및 두 번째 문자 이외의 문자는 현재 무시됩니다.

## 데이터 사용

수집된 광고 동의 데이터를 사용할 수 있습니다.

* 데이터 피드: 광고 동의 데이터는 `dataprivacydmaconsent` [열](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md)을(를) 사용하여 사용할 수 있습니다.
* Data Warehouse 보고서: 광고 동의 데이터는 **[!UICONTROL 광고 플랫폼 동의]** 차원을 사용하여 사용할 수 있습니다.

조직은 이 컨텍스트 데이터 변수를 구현하는 논리를 결정합니다. 이 값은 설정된 히트 이후에 지속되지 않으므로 각 페이지에서 컨텍스트 데이터 변수를 설정해야 합니다.

Adobe Advertising을 통해 Adobe Analytics에서 전환 이벤트로 Google에 광고 데이터를 보낼 때 Adobe Advertising 팀에 문의하여 통합을 지원하십시오.

자세한 내용은 [개인 정보 보고](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/privacy-reporting.md)를 참조하세요.
