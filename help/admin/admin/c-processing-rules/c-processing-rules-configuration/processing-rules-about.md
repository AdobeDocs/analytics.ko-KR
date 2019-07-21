---
description: 처리 규칙을 사용하여 정의된 조건을 기준으로 데이터를 변경할 수 있습니다. 속성 또는 값이 정의된 조건과 일치하는 경우 값을 설정하고 삭제할 수 있으며 이벤트를 설정할 수 있습니다.
seo-description: 처리 규칙을 사용하여 정의된 조건을 기준으로 데이터를 변경할 수 있습니다. 속성 또는 값이 정의된 조건과 일치하는 경우 값을 설정하고 삭제할 수 있으며 이벤트를 설정할 수 있습니다.
seo-title: 처리 규칙 작동 방식
solution: Analytics
subtopic: 처리 규칙
title: 처리 규칙 작동 방식
topic: 관리 도구
uuid: 19 C 31 F 94-C 8 D 8-47 B 1-97 FA -29 ED 98 C 94 E 87
translation-type: tm+mt
source-git-commit: ad6ba22acf6996aa038c5a3252cae8bddbf0b36a

---


# 처리 규칙 작동 방식

처리 규칙을 사용하여 정의된 조건을 기준으로 데이터를 변경할 수 있습니다. 속성 또는 값이 정의된 조건과 일치하는 경우 값을 설정하고 삭제할 수 있으며 이벤트를 설정할 수 있습니다.

처리 규칙은 데이터가 수집될 때 데이터에 적용되고 AppMeasurement 라이브러리를 통해, 그리고 데이터 삽입 API를 통해 들어오는 모든 데이터에 적용됩니다. 처리 규칙은 전체 및 로그 데이터 소스에도 적용됩니다. 이 소스에는 *`hit`*&#x200B;또는 사용자가 수행할 수 있는 작업을 나타내는 데이터가 들어 있습니다. 처리 규칙은 다른 데이터 소스에는 적용되지 않습니다.

## 중요 개념 {#section_EB138775E7C64C74B0D1D3213F7A823C}

다음 테이블에서는 처리 규칙 사용 시 이해해야 하는 주요 개념을 보여줍니다.

<table id="table_287C606AE26E47AA8F737411990ACEB2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>개념 </p> </th> 
   <th colname="col2" class="entry"> <p>세부 사항 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>규칙이 단일 보고서 세트에 적용됩니다. </p> </td> 
   <td colname="col2"> <p> <a href="../../../../admin/admin/c-processing-rules/c-processing-rules-configuration/t-processing-rules-copy-to-rs.md#task_6E4B82FCA687409B88F17EAFC353755D" type="task" format="dita" scope="local"> 다른 보고서 세트에 처리 규칙 복사 </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>처리 규칙이 나열된 순서대로 적용됩니다. </p> </td> 
   <td colname="col2"> <p>작업이 값을 변경하는 경우 이후 조건은 새 값을 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>처리 규칙은 저장 후 즉시 보고서 세트에 적용됩니다. </p> </td> 
   <td colname="col2"> <p>처리 규칙의 변경 사항은 저장 후 수분 내에 보고서 세트에 표시되어야 합니다. 처리 규칙을 테스트할 때에는 처리 규칙의 결과를 빨리 볼 수 있도록 테스트 보고서 세트에서 <a href="../../../../admin/admin/realtime/t-realtime-admin.md#task_1CD03E9B6BDB48B08E9E612183557F40" format="dita" scope="local"> 테스트 보고서 세트의 실시간 보고서를</a> 사용하여 처리 규칙의 결과를 빠르게 확인할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>처리 규칙은 컨텍스트 데이터 변수에 액세스할 수 있는 유일한 방법입니다. </p> </td> 
   <td colname="col2"> <p> <a href="../../../../admin/admin/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md#concept_43AA4980A2D847D6A3BEC50BCC0780E7" format="dita" scope="local"> Evar에 컨텍스트 데이터 변수 복사 </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>VISTA 규칙 및 마케팅 채널 규칙 이전에 처리 규칙이 적용됩니다. </p> </td> 
   <td colname="col2"> <p> <a href="../../../../admin/admin/c-processing-rules/c-processing-rules-configuration/processing-rule-order.md#concept_8A6BBEA7F50C40C8A8D8755D4F579B1E" type="concept" format="dita" scope="local"> 처리 순서 </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>히트를 제외할 수 없습니다. </p> </td> 
   <td colname="col2"> <p>Vista 규칙을 사용하여 히트를 제외할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>제품 문자열, 참조 및 사용자 에이전트를 변경할 수 없습니다. </p> </td> 
   <td colname="col2"> <p>참조 및 사용자 에이전트는 읽기 전용입니다. 제품 문자열은 사용할 수 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>모바일 장치 속성 및 분류는 사용할 수 없습니다. </p> </td> 
   <td colname="col2"> <p>모바일 장치 조회가 처리 규칙 전에 발생하지만 속성은 처리 규칙에서 사용할 수 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>JavaScript AppMeasurement H.25.2 이전 버전을 실행하는 경우 쿼리 문자열 매개 변수는 URL의 처음 255자 이상을 읽을 수 없습니다. JavaScript appmeasurement H .25 .3 이상에서는 모든 쿼리 문자열 매개 변수를 포함한 전체 URL를 처리 규칙에 제공합니다. </p> </td> 
   <td colname="col2"> <p>H.25.3 이후 버전으로 업그레이드하거나 긴 URL 클라이언트측에서 쿼리 문자열 매개 변수를 읽고 컨텍스트 데이터 변수에 값을 저장하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>쿼리 문자열 값은 처리 규칙에서 읽도록 유니코드 또는 UTF-8로 인코딩해야 합니다. </p> </td> 
   <td colname="col2"> <p>이는 쿼리 문자열을 사용하여 전달된 멀티바이트 문자에 영향을 줄 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>각 보고서 세트에 대해 각각 30개 조건이 있는 150개 규칙으로 제한됩니다. </p> </td> 
   <td colname="col2"> <p>처리 규칙 제한은 회사 기준이 아닌 보고서 세트 기준입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>처리 규칙을 데이터가 전송되기 전에 컨텍스트 데이터 변수를 검색하도록 설정해야 합니다. </p> </td> 
   <td colname="col2"> <p>처리 규칙은 서버 호출이 전송될 때 적용됩니다. 컨텍스트 데이터 변수에 저장된 값은 처리 규칙을 사용하여 복사되지 않으므로 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>UI에서 값 비교는 대/소문자를 구분하지 않습니다. </p> </td> 
   <td colname="col2"> <p> <a href="../../../../admin/admin/c-processing-rules/processing-rules-examples/clean-up-values-in-a-report.md#concept_958E924BCCBB4BBA91CE91C977FE5151" type="concept" format="dita" scope="local"> 보고서에서 값을 정리합니다 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>컨텍스트 데이터 변수 이름에는 영숫자, 밑줄, 점만 포함될 수 있습니다. 추가된 모든 문자는 제거됩니다. </p> </td> 
   <td colname="col2"> <p>예를 들어 컨텍스트 데이터 변수 <code>login_page-home</code>은 자동으로 <code>login_pagehome</code>이 됩니다. <code>login_page-home</code> 변수로 전송된 모든 데이터는 <code>login_pagehome</code>에 할당됩니다. </p> <p>지원되지 않는 문자가 포함된 컨텍스트 데이터 변수는 처리 규칙 인터페이스에 추가될 수 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>삽입 기호(^)는 처리 규칙 시스템에서 특수 문자입니다. </p> </td> 
   <td colname="col2"> <p>하나의 삽입 기호를 대응시키려면, 두 개의 삽입 기호(^^)를 사용하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 처리 규칙 조건 {#section_387390EEE9BA4DA98698522A84326DB4}

조건은 일치 값에 대한 페이지 변수를 확인하거나 값이 있는지 확인합니다. 여러 조건을 추가할 수 있으며 모든 조건이 일치해야 하는지 선택할 수 있습니다.

조건이 없는 규칙을 만들어 정의된 작업을 항상 실행할 수 있습니다.

작업이 발생하기 전에 변수에서 값이 자동으로 확인되지 않습니다. 예를 들어 Prop1에는 "something"의 값이 포함되고, eVar1은 비어 있습니다. Prop1이 eVar1과 동일하도록 설정하는 경우 두 값 모두 비어 있게 됩니다. 이를 방지해야 하는 경우 값의 존재를 확인하기 위한 조건을 추가합니다.

## 처리 규칙 작업 {#section_E2285C9D008442C7BF136E52A9A4CC06}

작업은 페이지 변수를 설정하거나, 페이지 변수를 삭제하거나 이벤트를 트리거합니다. 또한 작업은 보고서에 표시할 값을 연결할 수 있습니다. 

For example, you might want to display `category:product` by concatenating two variables.
