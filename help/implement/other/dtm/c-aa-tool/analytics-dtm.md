---
description: Dynamic Tag Management를 통해 Adobe Analytics 도구를 만들고 자동 또는 수동으로 페이지 코드를 구성하여 Adobe Analytics를 배포합니다. 대부분의 사용자에게는 자동 방법이 권장됩니다.
keywords: Analytics Implementation;implementation method;dynamic tag management;dtm;analytics tool;property;tool type;tool name;configuration method;analytics premium;evars;events
title: Adobe Analytics 도구 추가
topic: Developer and implementation
uuid: 1c54331e-de03-4f44-8002-a19723c585b0
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 100%

---


# Adobe Analytics 도구 추가

Dynamic Tag Management를 통해 Adobe Analytics 도구를 만들고 자동 또는 수동으로 페이지 코드를 구성하여 Adobe Analytics를 배포합니다. 대부분의 사용자에게는 자동 방법이 권장됩니다.

>[!NOTE]
>
>방문자 추적을 개선하려면 [Identity Service](https://docs.adobe.com/content/help/ko-KR/id-service/using/home.html)를 활성화하는 것이 좋습니다.

## Adobe Analytics 도구 추가 {#section_D5066B21581B4F7F811AD0027BF44EA5}

1. **[!UICONTROL *`Web Property Name`*]**>**[!UICONTROL &#x200B;개요&#x200B;]**>**[!UICONTROL &#x200B;도구 추가&#x200B;]**>**[!UICONTROL  Adobe Analytics ]**를 클릭합니다.

   ![](assets/dtm-add-analytics-tool.png)

1. 다음 필드를 채웁니다.

<table id="table_1CFB53FE72E74CCB8CAA5D4E3873D286"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 요소 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>도구 유형 </p> </td> 
   <td colname="col2"><span class="keyword">Adobe Analytics</span>와 같은 도구 유형입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>도구 이름 </p> </td> 
   <td colname="col2">도구의 수사적 이름입니다. 이 이름은 <span class="wintitle">설치된 도구</span> 아래의 <span class="wintitle">개요</span>에 표시됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="1"> <p>구성 방법 </p> </td> 
   <td colname="col2"> <p> <b>자동</b>(권장): Dynamic Tag Management를 사용해 구성을 관리합니다. 이 방법을 사용하면 <span class="keyword">Experience Cloud</span> 로그인 또는 웹 서비스 ID를 통해 <span class="keyword">Adobe Analytics</span> 보고서 세트를 자동으로 동기화하고 AppMeasurement 코드를 관리할 수 있습니다. </p> <p>계정이 연결되면 Dynamic Tag Management에서 <span class="keyword">Adobe Analytics</span> 보고서 세트 ID 및 이름을 도구 구성 인터페이스로 가져오므로 사용자 오류가 발생할 가능성은 감소하면서 도구 배포 속도가 빨라집니다. </p> <p> <p>참고: <span class="wintitle">Adobe Analytics Premium</span> 고객은 <span class="keyword">자동</span>옵션을 선택해야 합니다. </p> </p> <p>자동 구성에 해당하는 필드 입력: </p> 
    <ul id="ul_8D9797B01E444B9C85B862A9F96B447C"> 
     <li id="li_0AC84C1F37B24C658F2178E50ECCC4B0"> <p> <b>Experience Cloud</b>: (기본값) <span class="keyword">Experience Cloud</span> Single Sign-On을 사용합니다. Experience Cloud ID와 암호를 지정합니다. </p> </li> 
     <li id="li_6C80468835D04CC09F4AEC46D1300310"> <p><b>웹 서비스</b>: 웹 서비스 사용자 이름과 공유 암호를 지정합니다. </p> <p>공유 암호 자격 증명은 <span class="uicontrol">관리자</span> &gt; <span class="uicontrol">회사 설정</span> &gt; <a href="https://docs.adobe.com/content/help/ko-KR/analytics/admin/company-settings/web-services-admin.html">웹 서비스</a>에 있습니다. </p> <p>개발자인 경우 웹 서비스 자격 증명을 획득하는 데 도움이 필요하면 <a href="https://marketing.adobe.com/developer/ko_KR/get-started/enterprise-api/c-get-web-service-access-to-the-enterprise-api">엔터프라이즈 API에 대한 웹 서비스 액세스 권한 얻기</a>를 참조하십시오. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <b>수동</b>: AppMeasurement 코드를 수동으로 관리합니다. <span class="ignoretag"><span class="uicontrol">관리 도구</span> &gt; <span class="uicontrol">코드 관리자</span></span>에서 <span class="keyword">Analytics</span><span class="keyword"> AppMeasurement</span> 코드를 다운로드할 수 있습니다. </p> <p><a href="/help/implement/other/dtm/c-aa-tool/library-management.md">라이브러리 관리</a>의 <span class="wintitle">코드 편집</span> 필드에 복사하여 붙여넣을 코드를 로컬로 다운로드하기에 대한 내용을 보려면 <a href="https://docs.adobe.com/content/help/ko-KR/analytics/implementation/js/migrate-from-hcode.html">JavaScript (신규)</a>를 클릭합니다. </p> <p>수동 구성에 해당하는 필드 입력: </p> 
    <ul id="ul_CFB6CE78AEB743EF8B47BAAC42E2DB0A"> 
     <li id="li_5B7046CD95AB416F8C113B381A264D91"> <p><b>프로덕션 계정 ID: </b>(필수) 데이터 수집에 사용할 프로덕션 계정입니다. Analytics의 경우 보고서 세트 ID입니다. Dynamic Tag Management는 프로덕션 및 스테이징 환경에서 올바른 계정을 자동으로 설치합니다. </p> </li> 
     <li id="li_14E840FD79A0451BABEDD15DC0584768"> <p><b>스테이징 계정 ID: </b>(필수) 개발 또는 테스트 환경에서 사용합니다. Analytics의 경우 보고서 세트 ID입니다. 스테이징 계정은 테스트 데이터를 프로덕션과 분리시킵니다. </p> </li> 
     <li id="li_69E6C6A41F5240E1ABE8ABE0B9D151FC"> <p><b>추적 서버: </b> 추적 서버의 정보를 지정합니다. </p> <p><span class="wintitle">추적 서버</span> 및 <span class="wintitle">SSL 추적 서버</span> 변수는 이미지 요청 및 쿠키가 작성된 도메인을 지정하는 퍼스트 파티 쿠키 구현에 사용됩니다. 자세한 내용은 <a href="https://helpx.adobe.com/kr/analytics/kb/determining-data-center.html">trackingServer 및 trackingServerSecure 변수 올바른 입력</a> 도움말을 참조하십시오. </p> </li> 
     <li id="li_1A7271C68205428F8CA5548A96CACBEC"> <p><b>SSL 추적 서버: </b>SSL 추적 서버의 정보를 지정합니다. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

1. **[!UICONTROL 도구 만들기]**&#x200B;를 클릭하여 도구를 만들고 편집할 수 있도록 표시합니다.

   도구는 [!UICONTROL 개요] 탭의 [!UICONTROL 설치된 도구] 아래에 표시됩니다.

1. (조건부) 필요한 경우 아래 링크([!UICONTROL 일반], [!UICONTROL 라이브러리 관리], [!UICONTROL 전역 변수], [!UICONTROL 페이지 보기 횟수 및 컨텐츠], [!UICONTROL 링크 추적], [!UICONTROL 레퍼러 및 캠페인], [!UICONTROL 쿠키] 및 [!UICONTROL 페이지 코드 사용자 지정])의 안내에 따라 도구를 추가로 구성합니다.

이 도구에 대한 자세한 내용은 [Adobe Analytics 도구에 대해 자주 묻는 질문](/help/implement/faq.md)을 참조하십시오.

## 기존 Adobe Analytics 도구 편집 {#section_148B16AF429B4949B06238D90635B726}

기존 Adobe Analytics 도구를 편집하여 구성 설정을 변경할 수 있습니다.

1. ![](assets/settings_gear.png)개요 탭에서 설치된 도구 옆의  아이콘을 클릭합니다.
1. 원하는 대로 필드를 편집합니다.

   아래 표에는 위에서 설명한 Analytics 도구를 만들 때 사용할 수 있는 요소 이외의 다른 요소만 표시됩니다. 하지만 두 표에서 설명한 대로 페이지의 요소를 변경할 수 있습니다.

<table id="table_2B60CD109CFF4839AB7F91D61125EDFF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 요소 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>자동 구성 활성화 </p> </td> 
   <td colname="col2"> <p>참고: 이 설정을 활성화하면 수동으로 구성한 구현이 <span class="term">구성 방법</span>에서 설명한 자동 구성 방법으로 변경됩니다. </p> <p>이 옵션을 사용하면 Dynamic Tag Management에서 <span class="keyword">Adobe Analytics</span> 계정의 구성을 자동으로 검색합니다. </p> <p>사용 가능한 최신 AppMeasurement 코드가 사용되고 새 버전이 공개되는 대로 선택할 수 있게 업그레이드 알림이 표시됩니다. 호환성 등을 위해 필요할 경우 이전 AppMeasurement 버전으로 롤백할 수도 있습니다. 최대 5개의 이전 버전이 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>자격 증명 업데이트 </p> </td> 
   <td colname="col2"> <p>예를 들어 사용자와 관련된 보고서 세트를 업데이트하기 위해 API를 새로 고칩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. (조건부) 필요한 경우 아래 링크([!UICONTROL 일반], [!UICONTROL 라이브러리 관리], [!UICONTROL 전역 변수], [!UICONTROL 페이지 보기 횟수 및 컨텐츠], [!UICONTROL 링크 추적], [!UICONTROL 레퍼러 및 캠페인], [!UICONTROL 쿠키] 및 [!UICONTROL 페이지 코드 사용자 지정])의 안내에 따라 도구를 추가로 구성합니다.
1. **[!UICONTROL 변경 내용 저장]**&#x200B;을 클릭합니다.
