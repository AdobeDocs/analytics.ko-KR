---
description: .JS 파일이 페이지에서 올바로 참조되었는지 확인합니다. 경로는 현재 문서에 대해 상대적이거나 절대 경로 이름일 수 있습니다.
keywords: Analytics 구현
seo-description: .JS 파일이 페이지에서 올바로 참조되었는지 확인합니다. 경로는 현재 문서에 대해 상대적이거나 절대 경로 이름일 수 있습니다.
seo-title: JavaScript JS 파일
solution: Analytics
title: JavaScript JS 파일
topic: 개발자 및 구현
uuid: 6e83223f-2127-41d3-9806-bd085fa2a747
translation-type: ht
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# JavaScript JS 파일

.JS 파일이 페이지에서 올바로 참조되었는지 확인합니다. 경로는 현재 문서에 대해 상대적이거나 절대 경로 이름일 수 있습니다.

```js
<script language="JavaScript" 
src="https://www.sampleco.com/javascript/includes/s_code.js"></script>
```

사이트의 일부 페이지가 보안 프로토콜(https:)로 로드되고 JavaScript 파일용 [!DNL AppMeasurement]를 참조하는 경우 파일에 대한 참조가 (https:를 통해) 안전한지 아니면 아래에 표시된 대로 참조를 코딩하는지를 확인하십시오. 이 예에서는 현재 페이지의 프로토콜을 채택하고 "일부 요소가 안전하지 않습니다"라는 경고가 표시되지 않도록 합니다.

```js
<script language="JavaScript" 
src="//www.sampleco.com/javascript/includes/s_code.js"></script>
```

웹 서버의 [!DNL .JS] 파일에 웹 사이트 방문자들이 파일을 다운로드하여 실행할 수 있도록 권한이 적절히 설정되어 있는지 확인하십시오. 개발 서버에서 다른 [!DNL .JS] 파일을 사용하는 경우에는 프로덕션 서버에서 [!DNL .JS] 파일에 대해 "읽기 전용" 속성을 설정하여 덮어쓰기를 방지하십시오. 변경되는 경우 [!DNL .JS] 파일의 상단에 다음 설정이 적절히 설정되어 있는지 확인하십시오.

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

[!DNL .JS] 파일의 상단에 있는 값에 "*`s_account`*"가 지정되어 있다면 보고서 세트 ID([!UICONTROL s_account]변수에 채워짐)가 올바른지 확인하십시오. 또한 페이지에 있는 코드가 [!UICONTROL 보고서 세트 ID]( *`s_account`* 변수)를 설정하지 않았는지 확인합니다.

이미지 요청 및 변수를 검사하여 "대체 메서드"(위의 예에서 "분할" 코드의 세 번째 부분)가 [!DNL .JS] 파일 대신 이미지 요청을 만들지 않는지 확인합니다. 대비책은 최소한의 정보로만 이미지 요청을 만들므로 이와 같이 결정될 수 있습니다.
