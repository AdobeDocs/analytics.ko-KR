---
title: linkDownloadFileTypes
description: 다운로드 링크로 자동 추적되는 파일 확장자를 결정합니다.
feature: Appmeasurement Implementation
exl-id: 5089571a-d387-4ac7-838f-8bc95b2856fb
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 55%

---

# linkDownloadFileTypes

[`trackDownloadLinks`](trackdownloadlinks.md)(AppMeasurement) 또는 [`clickCollectionEnabled`](trackdownloadlinks.md)(Web SDK)이 활성화되어 있고 방문자가 링크를 클릭하면 AppMeasurement에서 파일 유형 확장자에 대한 링크의 URL을 확인합니다. 링크 URL에 일치하는 파일 유형이 포함되어 있으면 다운로드 링크 이미지 요청이 자동으로 전송됩니다.

다운로드 링크로 카운트할 파일 확장자를 사용자 지정하려면 `linkDownloadFileTypes` 를 사용하십시오.

>[!NOTE]
>
>실제 클릭만 자동으로 추적됩니다. 다음 유형의 링크는 자동으로 추적되지 않습니다.
>
>* 페이지가 로드될 때 자동으로 시작되는 파일 다운로드
>* 리디렉션 후 트리거되는 다운로드
>* 마우스 오른쪽 버튼을 클릭하고 다른 이름으로 대상 저장... 선택
>* JavaScript를 사용하는 링크 (예: `javascript:openLink()` )
>
>이러한 다운로드 유형의 경우 [`link tracking`](../functions/tl-method.md) 호출을 수동으로 보낼 수 있습니다.

클릭한 링크가 종료 링크와 다운로드 링크 기준을 모두 만족하는 경우에는 다운로드 링크 유형이 우선합니다.

## 웹 SDK 확장을 사용하여 링크 한정자 다운로드

[!UICONTROL 다운로드 링크 한정자] 텍스트 필드는 regex를 사용하여 클릭한 링크가 다운로드 링크가 될 수 있는지 확인합니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 원하는 태그 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음 [!UICONTROL Adobe Experience Platform Web SDK] 아래의 **[!UICONTROL 구성]** 단추를 클릭합니다.
1. [!UICONTROL 데이터 수집]에서 **[!UICONTROL 다운로드 링크 한정자]** 텍스트 필드에 원하는 값을 설정하십시오.

## 웹 SDK을 수동으로 구현하는 링크 한정자 다운로드

[`downloadLinkQualifier`](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/track-links.html#automaticLinkTracking)을(를) 사용하여 SDK을 [구성](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=ko-KR)합니다. 필드는 클릭한 URL의 regex를 사용하여 올바른 다운로드 링크인지 확인합니다. `downloadLinkQualifier`이(가) 정의되지 않으면 기본값이 `\\.(exe|zip|wav|mp3|mov|mpg|avi|wmv|pdf|doc|docx|xls|xlsx|ppt|pptx)$`(으)로 설정됩니다.

```json
alloy("configure", {
  "downloadLinkQualifier": "\\.(exe|zip|wav|mp3|mov|mpg|avi|wmv|pdf|doc|docx|xls|xlsx|ppt|pptx)$"
});
```

## Adobe Analytics 확장을 사용하여 확장 다운로드

확장 다운로드는 Adobe Analytics 확장을 구성할 때 [!UICONTROL 링크 추적] 아코디언 아래에 더 많은 항목을 추가하는 필드가 있는 파일 확장 목록입니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
2. 원하는 태그 속성을 클릭합니다.
3.  [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 **[!UICONTROL 구성]** 버튼을 클릭합니다.
4.  [!UICONTROL 링크 추적] 아코디언을 확장합니다. 그러면 **[!UICONTROL 다운로드 확장자]** 필드가 표시됩니다.

필드에 텍스트를 입력하고 **[!UICONTROL 추가]** 를 클릭하여 목록에 파일 확장자를 추가하십시오. 각각의 **&#39;X&#39;** 아이콘을 클릭하여 목록에서 파일 확장자를 제거하십시오.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.linkDownloadFileTypes

 `s.linkDownloadFileTypes` 변수는 쉼표로 구분된 파일 확장자로 이루어진 문자열입니다. 공백은 사용하지 마십시오.

이 변수가 정의되지 않으면 자동 다운로드 링크 추적이 작동하지 않습니다( [`trackDownloadLinks`](trackdownloadlinks.md) 가 `true`인 경우에도).

```js
s.linkDownloadFileTypes = "doc,docx,eps,jpg,png,svg,xls,ppt,pptx,pdf,xlsx,tab,csv,zip,txt,vsd,vxd,xml,js,css,rar,exe,wma,mov,avi,wmv,mp3,wav,m4v";
```
