---
title: trackDownloadLinks
description: 다운로드 링크에 대한 자동 링크 추적을 활성화하거나 비활성화합니다.
feature: Appmeasurement Implementation
exl-id: d92f722b-d605-40ad-bb55-ec71219a47e3
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 59%

---

# trackDownLoadLinks

Adobe는 각 다운로드 링크에 대한 [`tl()`](../functions/tl-method.md) 메서드를 수동으로 설정하지 않고도 다운로드 링크를 추적하는 기능을 제공합니다. 다운로드 링크에 대한 자동 링크 추적을 사용하려면 이 변수를 활성화하십시오.

활성화되면 AppMeasurement는 클릭한 모든 링크 URL을 [`linkDownloadFileTypes`](linkdownloadfiletypes.md)의 값과 비교합니다. 일치하는 항목이 있으면 다운로드 링크 추적 호출이 자동으로 실행됩니다.

## 웹 SDK 확장을 사용하여 클릭 컬렉션 활성화 또는 비활성화

웹 SDK을 구성할 때 [!UICONTROL 클릭 데이터 수집 사용] 확인란을 사용하십시오. 이 확인란은 종료 및 다운로드 링크를 모두 처리합니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 태그 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음 [!UICONTROL Adobe Experience Platform Web SDK] 아래의 **[!UICONTROL 구성]** 단추를 클릭합니다.
1. [!UICONTROL 데이터 수집]에서 **[!UICONTROL 데이터 수집 사용]** 확인란을 클릭합니다.

## 웹 SDK을 수동으로 구현하는 클릭 컬렉션 활성화 또는 비활성화

[`clickCollectionEnabled`](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html#clickCollectionEnabled)을(를) 사용하여 SDK을 구성하십시오. 필드는 링크 클릭과 관련된 데이터가 자동으로 수집되는지 여부를 결정하는 부울입니다. 기본값은 `true`입니다. 자동 링크 추적을 비활성화하려면 이 값을 `false`(으)로 설정하십시오. 이 설정은 다운로드 및 종료 링크 모두에 대한 자동 링크 추적을 처리합니다.

```json
alloy("configure", {
  "clickCollectionEnabled": true
});
```

## Adobe Analytics 확장을 사용하여 다운로드 링크 추적

다운로드 링크 추적은 Adobe Analytics 확장을 구성할 때 [!UICONTROL 링크 추적] 아코디언 아래에 있는 확인란입니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
2. 원하는 태그 속성을 클릭합니다.
3. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 **[!UICONTROL 구성]** 버튼을 클릭합니다.
4. [!UICONTROL 링크 추적] 아코디언을 확장합니다. 그러면 [!UICONTROL 다운로드 링크 추적] 확인란이 표시됩니다.

자동 다운로드 링크 추적을 활성화하려면 확인란을 클릭하십시오.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.trackDownloadLinks

`s.trackDownloadLinks`는 자동 다운로드 링크 추적을 활성화하거나 비활성화하는 부울입니다. 다운로드 링크를 추적하지 않으려는 경우 또는 `tl()` 메서드를 수동으로 호출하여 다운로드를 추적하려는 경우 이 변수를 `false`로 설정하십시오.

```js
s.trackDownloadLinks = true;
```
