---
description: 웹 속성은 한 개의 포함 코드에 포함된 규칙 라이브러리로 된 하나 이상의 도메인 및 서브 도메인 그룹일 수 있습니다.
keywords: Analytics 구현;구현 방법;dynamic tag management;dtm;웹 속성;속성
seo-description: 웹 속성은 한 개의 포함 코드에 포함된 규칙 라이브러리로 된 하나 이상의 도메인 및 서브 도메인 그룹일 수 있습니다.
seo-title: 웹 속성 만들기
solution: Analytics
title: 웹 속성 만들기
topic: 개발자 및 구현
uuid: f19d5504-eb44-4d93-a387-7470ab4b3a3a
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# 웹 속성 만들기

웹 속성은 한 개의 포함 코드에 포함된 규칙 라이브러리로 된 하나 이상의 도메인 및 서브 도메인 그룹일 수 있습니다.

> [!NOTE] 관리자 권한이 있는 사용자만 속성을 만들 수 있습니다. 역할에 대한 자세한 내용은 다이내믹 태그 관리 [제품 설명서의 DTM에서](https://marketing.adobe.com/resources/help/en_US/dtm/groups.html) 그룹 만들기 및 관리를 참조하십시오.

DTM을 사용하여 이러한 자산을 관리하고 추적할 수 있습니다. 예를 들어 하나의 템플릿을 기반으로 한 여러 개의 웹 사이트가 있고 이러한 웹 사이트 모두에서 동일한 자산을 추적하려 하는 경우, 여러 도메인에 하나의 웹 속성을 적용할 수 있습니다.

웹 속성 및 모범 사례에 대한 일반 정보는 다이내믹 [태그](https://marketing.adobe.com/resources/help/en_US/dtm/web_property.html) 관리 제품 설명서의 웹 속성입니다.

1. 회사 페이지로 이동한 다음 **[!UICONTROL 속성 추가]**&#x200B;를 클릭합니다.

   ![](assets/dtm-create-web-property.png)

1. 다음 필드를 채웁니다.

   <table id="table_376D72251C4D4C4CA878D10C18D2532C"> 
    <thead> 
    <tr> 
    <th colname="col1" class="entry"> 요소 </th> 
    <th colname="col2" class="entry"> 설명 </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
    <td colname="col1"> <span class="uicontrol"> 이름 </span> </td> 
    <td colname="col2"> <p>속성의 이름입니다. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <span class="uicontrol"> URL</span> </td> 
    <td colname="col2"> <p>속성의 기본 URL입니다. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <span class="uicontrol">이 사이트는 여러 도메인을 포괄합니다.</span> </td> 
    <td colname="col2"> <p>방문자 데이터가 도메인 간에 유지되도록 하려는 경우 도메인을 추가 및 삭제할 수 있습니다. 이 옵션을 선택하면 방문에 대한 데이터가 서브 도메인 전체에서 유지됩니다.  </p> <p>이 설정을 사용하여 연결된 서브 도메인 또는 도메인 간의 트래픽 이동을 추적하는 방법을 지정할 수 있습니다. 서브 도메인에 대한 링크는 아웃바운드 링크로 처리됩니다. 서브 도메인에 대한 방문은 별도로 추적됩니다. </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. (선택 사항) [!UICONTROL 고급 설정]을 구성합니다.

   <table id="table_6E687FBE6ACC4301BCCD837F4DCBB9C9"> 
    <thead> 
    <tr> 
    <th colname="col1" class="entry"> 요소 </th> 
    <th colname="col2" class="entry"> 설명 </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
    <td colname="col1"> <span class="uicontrol"> 다중 규칙 승인 허용</span> </td> 
    <td colname="col2"> <p>이 속성에 대한 여러 규칙을 한 번에 승인할 수 있도록 해줍니다. 기본 승인은 하나의 규칙만 승인할 수 있습니다. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <span class="uicontrol"> 선택적 게시 활성화</span> </td> 
    <td colname="col2"> <p>사용자가 게시되는 승인된 규칙을 선택할 수 있는지 여부를 지정합니다. 기본 옵션입니다. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <span class="uicontrol"> 추적 쿠키 이름</span> </td> 
    <td colname="col2"> <p>기본 추적 쿠키 이름을 무시합니다. Dynamic Tag Management에서 다른 쿠키를 받기 위해 옵트아웃 상태를 추적하는 데 사용하는 이름을 사용자 지정할 수 있습니다. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <span class="uicontrol"> 태그 시간 초과</span> </td> 
    <td colname="col2"> <p>제한 시간이 초과되어 태그 요청을 취소하기 전에 태그가 시작될 때까지 Dynamic Tag Management가 대기하는 시간을 지정합니다. </p> <p> Dynamic Tag Management가 작동하는 방식으로 인해 이 시간이 길어지는 것에 대해 염려하지 마십시오. DTM에는 느린 태그가 사용자 환경에 영향을 미치지 않도록 하는 유효한 메서드가 있습니다. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <span class="uicontrol"> 앵커 지연</span> </td> 
    <td colname="col2"> <p>다음 페이지로 이동하기 전에 Dynamic Tag Management가 클릭한 링크에서 태그가 실행될 때까지 기다리는 시간을 지정합니다. 기본값은 100밀리초입니다. </p> <p>지연 시간이 길어질수록 추적 정확도는 향상됩니다. Adobe는 지연 시간을 500밀리초 이하로 설정하기를 권장하며 사용자는 이를 감지하지 못합니다. </p> <p>Dynamic Tag Management는 지정된 시간까지 기다리지만 비콘이 더 빨리 작동하는 경우 지연이 갑자기 종료됩니다. (즉 사용자가 언제나 전체 지연 시간을 기다리는 것은 아닙니다.) </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. **[!UICONTROL 속성 만들기를 클릭합니다]**.
