---
title: linkDownloadFileTypes
description: 다운로드 링크로 자동 추적되는 파일 확장자를 결정합니다.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# linkDownloadFileTypes

이 [`trackDownloadLinks`](trackdownloadlinks.md) 활성화되고 방문자가 링크를 클릭하면 AppMeasurement는 링크의 URL에서 필터 유형 확장을 확인합니다. 링크 URL에 에 있는 파일 유형이 포함되어 `linkDownloadFileTypes`있으면 다운로드 링크 이미지 요청이 자동으로 전송됩니다.

다운로드 링크로 카운트할 파일 확장자를 사용자 `linkDownloadFileTypes` 지정하는 데 사용합니다.

> [!NOTE] 실제 클릭만 자동으로 추적됩니다. 다음 유형의 링크는 자동으로 추적되지 않습니다.
>
> * 페이지가 로드될 때 자동으로 시작되는 파일 다운로드
> * 리디렉션 후 트리거되는 다운로드
> * 마우스 오른쪽 단추를 클릭하고 &#39;다른 이름으로 대상 저장...&#39;을 선택합니다.
> * JavaScript를 사용하는 링크(예: `javascript:openLink()`
>
> 
이러한 다운로드 유형의 경우 해당 [`tl()`](../functions/tl-method.md) 메서드를 수동으로 호출할 수 있습니다.

클릭한 링크가 종료 링크와 다운로드 링크 기준을 모두 만족하는 경우 다운로드 링크 유형이 우선순위가 지정됩니다.

## Adobe Experience Platform Launch에서 익스텐션 다운로드

다운로드 익스텐션은 Adobe Analytics 익스텐션을 구성할 때 [!UICONTROL Link Tracking] 아코디언 아래에 더 추가할 필드가 있는 파일 확장자 목록입니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 탭으로 이동한 [!UICONTROL Extensions] 다음 Adobe Analytics 아래의 [!UICONTROL Configure] 단추를 클릭합니다.
4. 필드를 나타내는 [!UICONTROL Link Tracking] [!UICONTROL Download Extensions] 아코디언을 확장합니다.

필드에 텍스트를 입력하고 을 클릭하여 목록에 파일 확장자를 [!UICONTROL Add]추가합니다. 해당 &#39;X&#39; 아이콘을 클릭하여 목록에서 파일 확장자를 제거합니다.

## s.linkDownloadFileTypes in AppMeasurement 및 Launch 사용자 지정 코드 편집기

이 `s.linkDownloadFileTypes` 변수는 쉼표로 구분된 파일 확장명의 문자열입니다. 공백을 사용하지 마십시오.

이 변수가 정의되지 않은 경우 자동 다운로드 링크 추적은 작동하지 않습니다( [`trackDownloadLinks`](trackdownloadlinks.md) 있는 경우라도 `true`).

```js
s.linkDownloadFileTypes = "doc,docx,eps,jpg,png,svg,xls,ppt,pptx,pdf,xlsx,tab,csv,zip,txt,vsd,vxd,xml,js,css,rar,exe,wma,mov,avi,wmv,mp3,wav,m4v";
```
