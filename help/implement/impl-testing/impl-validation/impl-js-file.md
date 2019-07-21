---
description: .JS 파일이 페이지에서 올바로 참조되었는지 확인합니다. 경로는 현재 문서에 대해 상대적이거나 절대 경로 이름일 수 있습니다.
keywords: Analytics 구현
seo-description: .JS 파일이 페이지에서 올바로 참조되었는지 확인합니다. 경로는 현재 문서에 대해 상대적이거나 절대 경로 이름일 수 있습니다.
seo-title: JavaScript JS 파일
solution: Analytics
title: JavaScript JS 파일
topic: 개발자 및 구현
uuid: 6 E 83223 F -2127-41 D 3-9806-BD 085 FA 2 A 747
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# JavaScript JS 파일

.JS 파일이 페이지에서 올바로 참조되었는지 확인합니다. 경로는 현재 문서에 대해 상대적이거나 절대 경로 이름일 수 있습니다.

```js
<script language="JavaScript" 
src="https://www.sampleco.com/javascript/includes/s_code.js"></script>
```

If some pages of the site are loaded in a secure protocol (https:), and reference the [!DNL AppMeasurement] for JavaScript file, ensure that the reference to the file is either secure (via https:) or code the reference as shown below. 이 예에서는 현재 페이지의 프로토콜을 채택하고 "일부 요소가 안전하지 않습니다"라는 경고가 표시되지 않도록 합니다.

```js
<script language="JavaScript" 
src="//www.sampleco.com/javascript/includes/s_code.js"></script>
```

Ensure that the [!DNL .JS] file on the web servers have permissions appropriately set so that the file may be downloaded and executed by website visitors. If a different [!DNL .JS] file is used on development servers, set the "read only" attribute for the [!DNL .JS] file on production servers to avoid an overwrite. If altered, ensure that the following settings are set appropriately at the top of the [!DNL .JS] file:

```js
/************************** CONFIG SECTION **************************/
/* You may add or alter any code config here.                       */
/* Link Tracking Config */
s.trackDownloadLinks=false /* true for download tracking */
s.trackExternalLinks=false /* true for exit link tracking */
s.trackInlineStats=false /* true for ClickMap support */
s.linkDownloadFileTypes="exe,zip,wav,mp3,mov,mpg,avi,doc,pdf,xls"
s.linkInternalFilters="javascript:"
s.linkLeaveQueryString=false
s.linkTrackVars="None" 
s.linkTrackEvents="None"
```

If " *`s_account`*" is assigned a value at the top of the [!DNL .JS] file, ensure that the report suite ID (populated in the [!UICONTROL s_account]variable) is correct. Also ensure that the code in the page is not setting the [!UICONTROL Report Suite ID] ( *`s_account`* variable).

Examine the image request and variables to ensure that the "fallback method" (the third part of the "split" code in the example above) is not creating the image request instead of the [!DNL .JS] file. "대비"책은 최소한의 정보로만 이미지 요청을 만들므로 이와 같이 결정될 수 있습니다.
