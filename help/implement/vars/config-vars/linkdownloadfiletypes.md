---
title: linkDownloadFileTypes
description: 다운로드 링크로 자동 추적되는 파일 확장자를 결정합니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# linkDownloadFileTypes

When [`trackDownloadLinks`](trackdownloadlinks.md) is enabled and a visitor clicks on a link, AppMeasurement checks the URL of the link for filetype extensions. `linkDownloadFileTypes`에 있는 파일 유형이 링크 URL에 포함되어 있으면 다운로드 링크 이미지 요청이 자동으로 전송됩니다.

다운로드 링크로 카운트할 파일 확장자를 사용자 지정하려면 `linkDownloadFileTypes`를 사용하십시오.

>[!NOTE] 실제 클릭만 자동으로 추적됩니다. 다음 유형의 링크는 자동으로 추적되지 않습니다.
>
> * 페이지가 로드될 때 자동으로 시작되는 파일 다운로드
> * 리디렉션 후 트리거되는 다운로드
> * 마우스 오른쪽 단추를 클릭하고 &#39;다른 이름으로 대상 저장...&#39; 선택
> * JavaScript를 사용하는 링크(예: `javascript:openLink()`)
>
> 
For these download types, you can manually call the [`tl()`](../functions/tl-method.md) method.

클릭한 링크가 종료 링크와 다운로드 링크 기준을 모두 만족하는 경우에는 다운로드 링크 유형이 우선합니다.

## Adobe Experience Platform Launch의 다운로드 확장자

다운로드 확장자는 Adobe Analytics 확장을 구성할 때 [!UICONTROL 링크 추적] 아코디언 아래에 더 추가할 수 있는 필드가 있는 파일 확장자 목록입니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 [!UICONTROL 구성] 단추를 클릭합니다.
4. [!UICONTROL 링크 추적] 아코디언을 확장합니다. 그러면 [!UICONTROL 다운로드 확장자] 필드가 표시됩니다.

필드에 텍스트를 입력하고 [!UICONTROL 추가]를 클릭하여 목록에 파일 확장자를 추가하십시오. 해당 &#39;X&#39; 아이콘을 클릭하여 목록에서 파일 확장자를 제거합니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.linkDownloadFileTypes

`s.linkDownloadFileTypes` 변수는 쉼표로 구분된 파일 확장자로 이루어진 문자열입니다. 공백은 사용하지 마십시오.

이 변수가 정의되지 않으면 자동 다운로드 링크 추적이 작동하지 않습니다([`trackDownloadLinks`](trackdownloadlinks.md)가 `true`인 경우에도).

```js
s.linkDownloadFileTypes = "doc,docx,eps,jpg,png,svg,xls,ppt,pptx,pdf,xlsx,tab,csv,zip,txt,vsd,vxd,xml,js,css,rar,exe,wma,mov,avi,wmv,mp3,wav,m4v";
```
