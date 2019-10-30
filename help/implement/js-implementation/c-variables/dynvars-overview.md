---
description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
keywords: Analytics 구현
seo-description: 동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.
seo-title: 다이내믹 변수
solution: Analytics
subtopic: 변수
title: 다이내믹 변수
topic: 개발자 및 구현
uuid: 1c6db083-570e-4bc4-858d-84cf46e7bec8
translation-type: ht
source-git-commit: 76d0ce11d9b560e0df866be9e753804b6fa4bb3d

---


# 다이내믹 변수

동적 변수를 사용하면 사이트의 이미지 요청에 전체 값을 여러 번씩 입력하지 않고도 한 변수에서 다른 변수로 값을 복사할 수 있습니다.

동적 변수는 여러 변수에서 동시에 같은 데이터(예: 캠페인 추적 코드)를 캡처하는 데 사용됩니다. 일반적으로 여러 보고서에서 고유하고 중요한 지표를 제공하는 경우에 사용됩니다. 예를 들어 [!UICONTROL 사용자 지정 전환] 변수와 [!UICONTROL 사용자 지정 트래픽] 변수에서 내부 검색 키워드를 캡처하면 이러한 키워드와 각각 연결된 [!UICONTROL 매출] 및 [!UICONTROL 주간 고유 방문자] 지표를 볼 수 있습니다..

동적 변수는 다양한 보고 조건에서 데이터를 보는 경우에도 유용합니다. 다양한 할당 및 쿠키 만료 설정을 사용하여 여러 eVar에서 캠페인 추적 코드를 캡처할 수 있습니다. 그러면 사용자는 이러한 캠페인에 전환 지표를 사용할 방법을 선택할 수 있습니다.

>[!NOTE]
>
>동적 변수는 쿠키(s_cc, s_sq, s_fid, s_vi 및 플러그인으로 설정된 모든 쿠키)와 함께 지원되지 않습니다. `D=<cookie value>`를 사용할 수 없습니다.

동적 변수의 가장 큰 장점은 긴 문자열을 반복해서 실제로 전달하지 않고도 여러 변수의 데이터에 있는 긴 문자열을 캡처하는 능력입니다. 일부 브라우저에서는 HTTP GET 요청(Adobe 이미지 요청 포함)의 최대 길이를 제한합니다. 동적 변수를 사용하면 여러 변수에 데이터가 중복된 경우 Adobe 서버에 대한 요청의 길이를 줄여 모든 데이터를 캡처할 수 있습니다..

페이지 보기에서 발생하는 Adobe 이미지 요청의 경우, 동적 변수를 사용하여 [!UICONTROL 사용자 지정 트래픽] 값을 [!UICONTROL 사용자 지정 전환]으로 복사하면 `v1=D=c1`1=1이 표시됩니다. eVar1에서 이전에 요청에 있었던 값을 받은 경우 Adobe 서버는 처리 중에 [!UICONTROL 사용자 지정 트래픽 1]의 값을 [!UICONTROL 사용자 지정 전환 1] 값에 동적으로 복사합니다. 그 결과, [!UICONTROL 사용자 지정 트래픽 1]을 사용하여 처음에 전달한 값이 [!UICONTROL 사용자 지정 전환 1] 보고서에도 나타납니다.

변수를 원하는 값으로 설정한 다음 다른 변수를 `D=[variable abbreviation]`로 설정하여 동적 변수를 전달합니다. 각 변수에 대한 약어는 [데이터 수집 쿼리 매개 변수](../../../implement/js-implementation/data-collection/query-parameters.md)를 참조하십시오. 동적 변수는 다음 위치에서 데이터를 가져올 수 있습니다.

* 기타 쿼리-문자열 변수
* HTTP 헤더(쿠키 HTTP 헤더 제외)

동적 변수를 생성하려면 값의 시작 앞부분에 특수한 접두사를 붙입니다. 기본 접두사는 "D="입니다. 동적 변수 플래그 지정에는 두 가지 방법이 있습니다.

* 기본 접두사 D= 사용(예: s.prop1="D=사용자-에이전트")
* JavaScript 구현이 아닌 경우 "D" 쿼리-문자열 매개 변수를 사용하여 사용자 지정 접두사를 정의할 수 있습니다. 예를 들어 쿼리-문자열 매개 변수가 `"&D=$"`인 경우 `s.prop1="$User-Agent"` 명령으로 동적 변수를 만들 수 있습니다.

사용한 변수 약어는 이미지 요청으로 전달되는 변수 매개 변수 이름과 일치해야 합니다. 일부 변수에는 상황에 따라 허용되는 여러 매개 변수가 있을 수 있습니다. 예를 들어 `pageName=`와 `gn=`는 둘 다 페이지 이름을 전달하지만, 뒤의 것이 모바일 및 하드 코드 구현에서 더 많이 사용됩니다. 이미지 요청에서 `pageName=`를 사용하여 페이지 이름을 전달한 경우 `D=pageName`은 사용할 수 있지만 `D=gn`은 사용할 수 없습니다. 이미지 요청에서 `gn=`을 사용하는 경우에는 `D=gn`을 사용할 수 있지만 `D=pageName`은 사용할 수 없습니다.

다음 정보는 동적 변수에 적용됩니다.

* 동적 변수는 모든 버전의 AppMeasurement 코드에서 작동합니다.
* 동적 변수는 대/소문자를 구분합니다.
* 동적 변수는 견적에 포함된 리터럴 문자열을 지원합니다.
* 동적 변수 대체는 처리 규칙, VISTA 및 기타 프로 처리에 앞서 발생합니다.
* 동적 변수 접두사 "D="는 변수 값의 중간이 아닌 맨 앞에 있어야 합니다. 예를 들면 `c2='D="test7"+User-Agent'`를 `c2='"test7"+D=User-Agent'` 대신 사용합니다.

* 모든 구현 기술에서 그렇듯이, Adobe는 프로덕션 환경에 동적 변수를 구현하기 전에 개발 환경에서 충분히 테스트할 것을 권장합니다. 복사되는 전체 문자열이 클라이언트 측 디버깅 도구에 보이지 않으므로 영향을 받는 Analytics 보고서를 검토하여 구현에 성공했는지 확인해야 합니다.
* 최대 길이가 다른 변수 사이에서 값을 복사하는 경우, 대상 변수의 최대 길이를 초과하는 값을 복사하면 값이 잘립니다. 예를 들어 [!UICONTROL 사용자 지정 트래픽] 변수는 100자로 제한되고 [!UICONTROL 사용자 지정 전환] 변수는 255자로 제한됩니다. s.eVar1에서 s.prop1로 150자로 된 값을 복사할 경우 [!UICONTROL 사용자 지정 트래픽] 보고서에서는 이 값이 100자로 잘립니다. 

## 동적 변수 예 {#section_5CE4468D978540FBA384B9D6477C92EC}

<!-- 

dynvars_examples.xml

 -->

Analytics에서 사용할 수 있는 동적 변수의 예입니다.

페이지 보기에서 발생하는 Adobe 이미지 요청의 경우, 동적 변수를 사용하여 [!UICONTROL 사용자 지정 트래픽] 값을 [!UICONTROL 사용자 지정 전환]으로 복사하면 `v1=D=c1`1=1이 표시됩니다. eVar1에서 이전에 요청에 있었던 값을 받은 경우 Adobe 서버는 처리 중에 [!UICONTROL 사용자 지정 트래픽 1]의 값을 [!UICONTROL 사용자 지정 전환 1] 값에 동적으로 복사합니다. 그 결과, [!UICONTROL 사용자 지정 트래픽 1]을 사용하여 처음에 전달한 값이 [!UICONTROL 사용자 지정 전환 1] 보고서에도 나타납니다.

`D=[variable]` 값은 따옴표로 묶어야 합니다. Analytics 코드에서는 이 값을 문자열로 취급합니다. 이 문자열을 Analytics로 전달하면 URL 인코딩됩니다(DigitalPulse Debugger 또는 유사한 유틸리티에서 요청을 볼 때). 이는 정상적인 현상입니다. Adobe 서버에서 `D=[variable]` 구성을 인식하고 이 문자열을 발견하면 적절한 값을 복사합니다.

>[!NOTE]
>
>이미지 요청을 사용하여 링크를 추적할 때 링크 URL/이름(pev2)을 정의하는 것처럼 링크의 유형(다운로드=lnk_d, 종료=lnk_e 또는 사용자 지정 링크=lnk_o)을 정의해야 합니다. 링크는 `<a href>` 태그 내에 코드를 삽입하여 수동으로 구현해야 합니다.

>[!NOTE]
>
>동적 변수는 쿠키(s_cc, s_sq, s_fid, s_vi 및 플러그인으로 설정된 모든 쿠키)와 함께 지원되지 않습니다. `D=<cookie value>`를 사용할 수 없습니다.

<table id="table_A25D5EA2A8C446F5A55AB32955B9848C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> JavaScript 예제 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <code class="syntax javascript">
      s.eVar1="D=pageName" 
    </code> </td> 
   <td colname="col2"> <p>eVar1의 pageName 값을 캡처합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <code class="syntax javascript">
      s.prop1='D=v2+":"+c2'&amp;nbsp; 
    </code> </td> 
   <td colname="col2"> <p>eVar2:prop2를 prop1에 연결합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <code class="syntax javascript">
      s.prop1=s.eVar1="D=g"&amp;nbsp; 
    </code> </td> 
   <td colname="col2"> <p>페이지 URL을 prop1 및 eVar1에 모두 전달합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <code class="syntax javascript">
      s.eVar1="D=v0" 
    </code> </td> 
   <td colname="col2"> <p>eVar 1의 캠페인을 캡처합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <code class="syntax javascript">
      s.prop1='D=User-Agent+" ;- "+Accept-Language' 
    </code> </td> 
   <td colname="col2"> <p>사용자 에이전트를 연결하고 prop1의 언어 헤더를 승인합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <code>
      s.prop1="D=User-Agent" 
    </code> </td> 
   <td colname="col2"> <p>prop1의 사용자 에이전트를 캡처합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_DD0B7F0648054E01A5F98CDF18D745E4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이미지 요청 예제 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <code class="syntax javascript">
      /b/ss/rsid/?gn=Home&amp;D=~~&amp;c1=~~v0 /b/ss/rsid/?gn=Home&amp;D=~~&amp;c1=~~campaign /b/ss/rsid/?gn=Home&amp;c1=D%3dv0%3d is /b/ss/rsid/?gn=Home&amp;c1=%5b%5bv0%5d%5d%5b
    </code> </td> 
   <td colname="col2"> <p>prop1을 캠페인에 설정하는 4가지 방법 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <code>
      /b/ss/rsid/?gn=Home&amp;D=~~&amp;c2=~~x-up-subno 
    </code> </td> 
   <td colname="col2"> <p> x-up-subno 헤더를 prop2에 추가 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <code>
      c1=D%3DUser-Agent 
    </code> </td> 
   <td colname="col2"> <p> prop1을 HTTP 헤더 사용자-에이전트로 채워진 동적 변수로 만듭니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <code class="syntax javascript">
      &amp;c1=D%3D%22test%22 
    </code> </td> 
   <td colname="col2"> <p> prop1을 "test" 문자열로 채워진 동적 변수로 만듭니다. 이는 + 연산자를 활용하는 연결과 함께 사용할 때 유용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <code class="syntax javascript">
      &amp;c1=D%3D%22US%3A%20%22%2BUser-Agent 
    </code> </td> 
   <td colname="col2"> <p> prop1을 접두사가 "UA:"인 사용자-에이전트로 채워진 동적 변수로 만듭니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <code class="syntax javascript">
      &amp;vid=D%3DX-TM-ANTID 
    </code> </td> 
   <td colname="col2"> <p> 이 예제는 이 경우에는 고유한 헤더를 검색합니다. 여기에서는 X-TM-ANTID입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
