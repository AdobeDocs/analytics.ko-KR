---
description: Deploy Adobe Analytics using Dynamic Tag Management by creating the Adobe Analytics tool and configuring the page code either automatically or manually. 대부분의 사용자에게는 자동 방법이 권장됩니다.
keywords: Analytics Implementation;implementation method;dynamic tag management;dtm;analytics tool;property;tool type;tool name;configuration method;analytics premium;evars;events
seo-description: Deploy Adobe Analytics using Dynamic Tag Management by creating the Adobe Analytics tool and configuring the page code either automatically or manually. 대부분의 사용자에게는 자동 방법이 권장됩니다.
seo-title: Adobe Analytics 도구 추가
solution: Analytics
title: Adobe Analytics 도구 추가
topic: 개발자 및 구현
uuid: 1c54331e-de03-4f44-8002-a19723c585b0
translation-type: tm+mt
source-git-commit: 831ae375a90f021feddc6817a2602464be0d8414

---


# Adobe Analytics 도구 추가

Adobe Analytics 도구를 만들고 페이지 코드를 자동 또는 수동으로 구성하여 다이내믹 태그 관리를 사용하여 Adobe Analytics를 배포합니다. 대부분의 사용자에게는 자동 방법이 권장됩니다.

>[!NOTE]
>
>For improved visitor tracking, we strongly recommend that you enable Identity Service.[](https://marketing.adobe.com/resources/help/en_US/mcvid/)

## Adobe Analytics 도구 추가 {#section_D5066B21581B4F7F811AD0027BF44EA5}

1. Click  **[!UICONTROL *`Web Property Name`*]** &gt; **[!UICONTROL Overview]** &gt; **[!UICONTROL Add a Tool]** &gt; **[!UICONTROL Adobe Analytics]** .

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
   <td colname="col1" morerows="1"> <p>[구성 방법] </p> </td> 
   <td colname="col2"> <p> <b>자동</b>(권장): 다이내믹 태그 관리를 사용해 구성을 관리합니다. This method enables automatic synchronization of <span class="keyword"> Adobe Analytics</span> report suites via a <span class="keyword"> Experience Cloud</span> login or Web Services ID, and manages the [!DNL AppMeasurement] code. </p> <p>계정이 연결되면 다이내믹 태그 관리에서 <span class="keyword">Adobe Analytics</span> 보고서 세트 ID 및 이름을 도구 구성 인터페이스로 가져오므로 사용자 오류가 발생할 가능성은 감소하면서 도구 배포 속도가 빨라집니다. </p> <p> <p>참고: <span class="wintitle">Adobe Analytics Premium</span> 고객은 <span class="keyword">자동</span>옵션을 선택해야 합니다. 아래 <a href="../../../implement/c-implement-with-dtm/c-aa-tool/analytics-dtm.md#section_AEAA44566B5A46D2922E17A11D7EA217" format="dita" scope="local">Adobe Analytics Premium 활성화</a>를 참조하십시오. </p> </p> <p>자동 구성에 해당하는 필드 입력: </p> 
    <ul id="ul_8D9797B01E444B9C85B862A9F96B447C"> 
     <li id="li_0AC84C1F37B24C658F2178E50ECCC4B0"> <p> <b>Experience Cloud</b>: (기본값) <span class="keyword">Experience Cloud</span> Single Sign-On을 사용합니다. Experience Cloud ID와 암호를 지정합니다. </p> </li> 
     <li id="li_6C80468835D04CC09F4AEC46D1300310"> <p><b>웹 서비스</b>: 웹 서비스 사용자 이름과 공유 암호를 지정합니다. </p> <p>Shared secret credentials are located in <span class="uicontrol"> Admin </span> &gt; <span class="uicontrol"> Company Settings</span> &gt; <a href="https://docs.adobe.com/content/help/en/analytics/admin/company-settings/web-services-admin.html" format="html" scope="external"> Web Services</a>. </p> <p>개발자인 경우 웹 서비스 자격 증명을 획득하는 데 도움이 필요하면 <a href="https://marketing.adobe.com/developer/en_US/get-started/enterprise-api/c-get-web-service-access-to-the-enterprise-api" format="https" scope="external">엔터프라이즈 API에 대한 웹 서비스 액세스 권한 얻기</a>를 참조하십시오. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <b>수동</b>:[!DNL AppMeasurement] 코드를 수동으로 관리합니다. <span class="keyword"></span>관리 도구<span class="keyword"> &gt; </span>코드 관리자<span class="ignoretag"><span class="uicontrol">에서 </span>Analytics<span class="uicontrol"> </span>AppMeasurement</span> 코드를 다운로드할 수 있습니다. </p> <p>Click <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/appmeasure_mjs.html" format="https" scope="external"> JavaScript (new)</a> for information about downloading the code locally to copy and paste in the <span class="wintitle"> Edit Code</span> field in <a href="../../../implement/c-implement-with-dtm/c-aa-tool/library-management.md#concept_24654766343B4E82A9416A112D2125FE" format="dita" scope="local"> Library Management</a>. </p> <p>수동 구성에 해당하는 필드 입력: </p> 
    <ul id="ul_CFB6CE78AEB743EF8B47BAAC42E2DB0A"> 
     <li id="li_5B7046CD95AB416F8C113B381A264D91"> <p><b>프로덕션 계정 ID: </b>(필수) 데이터 수집에 사용할 프로덕션 계정입니다. Analytics에서 사용할 보고서 세트 ID입니다. 다이내믹 태그 관리는 프로덕션 및 스테이징 환경에서 올바른 계정을 자동으로 설치합니다. </p> </li> 
     <li id="li_14E840FD79A0451BABEDD15DC0584768"> <p><b>스테이징 계정 ID: </b>(필수) 개발 또는 테스트 환경에서 사용합니다. Analytics에서 사용할 보고서 세트 ID입니다. 스테이징 계정은 테스트 데이터를 프로덕션과 구별합니다. </p> </li> 
     <li id="li_69E6C6A41F5240E1ABE8ABE0B9D151FC"> <p><b>추적 서버: </b>추적 서버의 정보를 지정합니다. </p> <p><span class="wintitle">추적 서버</span> 및 <span class="wintitle">SSL 추적 서버</span> 변수는 이미지 요청 및 쿠키가 작성된 도메인을 지정하는 퍼스트 파티 쿠키 구현에 사용됩니다. 자세한 내용은 <a href="https://helpx.adobe.com/analytics/kb/determining-data-center.html" format="https" scope="external">trackingServer 및 trackingServerSecure 변수 올바른 입력</a> 도움말을 참조하십시오. </p> </li> 
     <li id="li_1A7271C68205428F8CA5548A96CACBEC"> <p><b>SSL 추적 서버: </b>SSL 추적 서버의 정보를 지정합니다. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

1. **[!UICONTROL 도구 만들기]를 클릭하여 도구를 만들고 편집할 수 있도록 표시합니다.**

   도구는 [!UICONTROL [개요]] 탭의 [!UICONTROL [설치된 도구]] 아래에 표시됩니다.

1. (조건부) 필요한 경우 아래 링크([!UICONTROL 일반], [!UICONTROL 라이브러리 관리], [!UICONTROL 전역 변수], [!UICONTROL 페이지 보기 횟수 및 컨텐츠], [!UICONTROL 링크 추적], [!UICONTROL 레퍼러 및 캠페인], [!UICONTROL 쿠키] 및 [!UICONTROL 페이지 코드 사용자 지정])의 안내에 따라 도구를 추가로 구성합니다.

See [Frequently Asked Questions About the Adobe Analytics Tool](../../../implement/faq.md#concept_00DF9AF14D30469BB986BF56A448806B) for additional information about this tool.

## 기존 Adobe Analytics 도구 편집 {#section_148B16AF429B4949B06238D90635B726}

기존 Adobe Analytics 도구를 편집하여 구성 설정을 변경할 수 있습니다.

1. ![개요](assets/settings_gear.png) 탭에서 설치된 도구 옆의  아이콘을 클릭합니다.
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
   <td colname="col2"> <p>Note: Enabling this setting changes a manually configured implementation to the automatic configuration method described in <span class="term"> Configuration Method</span>. </p> <p>이 옵션을 사용하면 다이내믹 태그 관리에서 <span class="keyword">Adobe Analytics</span> 계정의 구성을 자동으로 검색합니다. </p> <p>사용 가능한 최신 [!DNL AppMeasurement] 코드가 사용되고 새 버전이 사용 가능하게 되면 선택할 수 있는 업그레이드 알림이 표시됩니다. You can also roll back to previous [!DNL AppMeasurement] versions as necessary, such as for compatibility reasons. 최대 5개의 이전 버전이 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>자격 증명 업데이트 </p> </td> 
   <td colname="col2"> <p>예를 들어 사용자와 관련된 보고서 세트를 업데이트하기 위해 API를 새로 고칩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. (조건부) 필요한 경우 아래 링크([!UICONTROL 일반], [!UICONTROL 라이브러리 관리], [!UICONTROL 전역 변수], [!UICONTROL 페이지 보기 횟수 및 컨텐츠], [!UICONTROL 링크 추적], [!UICONTROL 레퍼러 및 캠페인], [!UICONTROL 쿠키] 및 [!UICONTROL 페이지 코드 사용자 지정])의 안내에 따라 도구를 추가로 구성합니다.
1. **[!UICONTROL 변경 내용 저장을 클릭합니다]**.
