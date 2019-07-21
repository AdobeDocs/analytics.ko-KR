---
description: Analytics 코드는 이미지 개체를 만드는데, 이 개체는 페이지에 나타나지 않는 볼 수 없는 이미지입니다.
keywords: Analytics 구현
seo-description: Analytics 코드는 이미지 개체를 만드는데, 이 개체는 페이지에 나타나지 않는 볼 수 없는 이미지입니다.
seo-title: 헤드 태그에 Analytics 코드 넣기
solution: Analytics
title: 헤드 태그에 Analytics 코드 넣기
topic: 개발자 및 구현
uuid: e 8 f 91 d 3 c-cb 72-454 d -9 bd 4-ff 54 d 83 d 981 f
translation-type: tm+mt
source-git-commit: 76d0ce11d9b560e0df866be9e753804b6fa4bb3d

---


# 헤드 태그에 Analytics 코드 넣기

Analytics 코드는 이미지 개체를 만드는데, 이 개체는 페이지에 나타나지 않는 볼 수 없는 이미지입니다.

>[!NOTE]
>
>이 섹션은 기존 s_ code. js 구현에만 적용됩니다. [JavaScript 1.0](../../../implement/js-implementation/c-appmeasurement-js/appmeasure-mjs.md#concept_F3957D7093A94216BD79F35CFC1557E8) 용 appmeasurement는 `<head>` 태그에서 라이브러리 및 페이지 코드 배포를 지원합니다.

이전에는 일반적인 구현 방법이 Analytics JavaScript 코드를 <head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8"> 및 </head> 태그가 있는 세그먼트만 필터링할 수 있습니다. 이 태그들 사이에 코드를 삽입함으로써 Adobe 서버로 데이터를 보낸 요청에 의해 반환된 1x1 픽셀 이미지가 어떤 방식으로든 페이지 레이아웃에 영향을 주는 것을 방지했습니다. 문서 시작 부분에 코드를 넣는 것은 이 코드가 코드에서 더 일찍 나타남을 의미합니다. 이렇게 되면 코드가 더 일찍 실행되어, 부분적 페이지 로드에 대해 더 효과적으로 페이지 보기를 카운트할 수 있습니다.

코드의 특정 요소에는 본문 개체가 있어야 합니다. 웹 브라우저들은 코드가 들어오는 순서로 코드를 실행하므로, Analytics JavaScript 코드가 문서 시작 부분에 있으면 본문 개체가 존재하기 전에 실행됩니다. 그 결과, 구현은 [!UICONTROL ClickMap] 데이터를 모으지 않고 파일 다운로드나 [!UICONTROL 종료] 링크에 대한 자동 추적은 사용할 수 없습니다. 연결 유형 데이터나 방문자 홈 페이지 데이터도 받지 않습니다. 문서 시작 부분에 코드를 넣는 것은 가능하지만 그 결과는 Analytics의 매우 제한된 버전이며 [!UICONTROL ClickMap]을 포함한 특정 보고서와 도구는 데이터를 기록하지 않을 수 있습니다.

Analytics 코드는 본문 태그 (<BODY></BODY>) 잘 구성된 HTML 페이지 코드는 페이지 상단에서 글로벌 include file에 삽입하는 것이 좋습니다(HTML 본문 태그 내부). 이 코드는 아래 언급된 경우를 제외하고 페이지의 어디든지 삽입할 수 있습니다.

* 테이블에 삽입하는 경우는 <td></td> 태그가 있는 세그먼트만 필터링할 수 있습니다. 예를 들어, 여는 사이에 코드를 삽입하지 마십시오. <tr> 태그 및 열기 <td> 태그.
* 변수를 설정하는 코드는 s_code.js 파일 참조 뒤에 삽입해야 합니다.
* Make certain that the [!UICONTROL report suite ID]s in the *`s_account`* variable in the s_code.js file are set correctly. 이 변수는 특정 보고서 세트용으로 코드 관리자로부터 코드를 다운로드할 때 또는 Adobe 기술 컨설턴트가 제공함에 따라 일반적으로 올바로 설정됩니다.

Analytics를 Target과 통합하려면, JavaScript 포함 파일을 페이지 하단에 삽입해야 합니다. 다음 예는 Analytics 코드의 올바른 배치를 보여 줍니다.

```js
<html> 
<head></head> 
<body> 
<!-- Analytics code version: H.20.3. 
Copyright 1997-2009 Omniture, Inc. More info available at 
https://www.omniture.com --> 
<script language="JavaScript" type="text/javascript" src="https://www.yourdomain.com/js/s_code.js"></script> 
<script language="JavaScript" type="text/javascript"><!-- 
/* You may give each page an identifying name, server, and channel on 
the next lines. */ 
s.pageName="" 
s.server="" 
s.channel="" 
s.pageType="" 
s.prop1="" 
s.prop2="" 
s.prop3="" 
s.prop4="" 
s.prop5="" 
/* Conversion Variables */ 
s.campaign="" 
s.state="" 
s.zip="" 
s.events="" 
s.products="" 
s.purchaseID="" 
s.eVar1="" 
s.eVar2="" 
s.eVar3="" 
s.eVar4="" 
s.eVar5="" 
/************* DO NOT ALTER ANYTHING BELOW THIS LINE ! **************/ 
var s_code=s.t();if(s_code)document.write(s_code)//--></script> 
<!-- End Analytics code version: H.20.3. --> 
</body> 
</html> 
```

