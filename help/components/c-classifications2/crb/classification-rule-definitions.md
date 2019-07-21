---
description: 분류 규칙 빌더에서 페이지의 인터페이스 요소를 정의한 것입니다.
seo-description: 분류 규칙 빌더에서 페이지의 인터페이스 요소를 정의한 것입니다.
seo-title: 분류 규칙 - 정의
solution: Analytics
subtopic: 분류
title: 분류 규칙 - 정의
topic: 관리 도구
uuid: 77 af 8669-6 e 11-435 c -9 cc 3-b 03 eb 627 c 855
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 분류 규칙 - 정의

분류 규칙 빌더에서 페이지의 인터페이스 요소를 정의한 것입니다.

## 규칙 페이지 {#section_4A5BF384EEEE4994B6DC888339833529}

이 페이지에는 규칙 세트의 규칙이 표시됩니다.

![](assets/classification_rules_page.png)

**정의**

<table id="table_2B3A8BB7BDE14836ACA6A1D444B011CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 요소 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>보고서 세트 및 변수 선택 </p> </td> 
   <td colname="col2"> <p><b>보고서 세트</b> </p> <p>규칙 세트가 적용되는 보고서 세트입니다. </p> <p><b>변수</b> </p> <p>분류 규칙 세트를 만들 때 1개의 변수만 적용할 수 있습니다. 1개의 변수에 여러 규칙 세트를 만들려면 각 규칙 세트를 여러 보고서 세트에 적용해야 합니다. </p> <p>참고: 보고서 세트에 대한 액세스 권한이 있는 변수만 사용할 수 있습니다. 변수에 대해 분류가 하나 이상 정의되어 있어야 변수가 <span class="wintitle">새 규칙 세트</span> 패널에 표시됩니다. </p> <p>For example, to make <span class="term"> Pages</span> available as a variable to the rule set, ensure that the report suite has <a href="https://marketing.adobe.com/resources/help/en_US/reference/traffic_classifications.html" format="http" scope="external"> traffic classifications</a> implemented for <span class="term"> Page</span>. </p> <p> <span class="uicontrol">관리</span> &gt; <span class="uicontrol">보고서 세트</span> &gt; <span class="uicontrol">트래픽</span> &gt; <span class="uicontrol">트래픽 분류</span>(또는 <span class="uicontrol">전환</span> &gt; <span class="uicontrol">전환 분류</span>)에서 변수에 대한 분류를 만들 수 있습니다. 그런 다음, 변수를 선택하고 <span class="uicontrol">분류 추가</span>를 클릭합니다. </p> <p>관리 도움말에서 <a href="https://marketing.adobe.com/resources/help/en_US/reference/index.html?f=traffic_classification_admin" format="https" scope="external">트래픽 분류</a> 및 <a href="https://marketing.adobe.com/resources/help/en_US/reference/index.html?f=conversion_classifications" format="https" scope="external">전환 분류</a>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="wintitle"> 활성화</span> </p> </td> 
   <td colname="col2"> <p>규칙의 유효성을 확인하고 활성화합니다. 활성 규칙은 매일 처리되며, 일반적으로 한 달 이전의 분류 데이터를 조사합니다. 이 규칙은 자동으로 새로운 값을 확인하고 분류를 업로드합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="wintitle"> 비활성화</span> </p> </td> 
   <td colname="col2"> <p>규칙을 편집하고 테스트할 수 있도록 규칙을 비활성화합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>보고서 세트 및 변수 구성 </p> </td> 
   <td colname="col2"> <p><span class="wintitle">사용 가능한 보고서 세트</span> 페이지를 표시합니다. 이 페이지에서 모든 규칙 세트에 사용할 하나 이상의 사용 가능한 보고서 세트를 선택할 수 있습니다. (<span class="wintitle">분류 규칙 빌더</span>를 처음 실행할 때에도 이 페이지가 표시됩니다.) </p> <p>사용 가능한 보고서 세트가 수백 개 있을 경우 보고서 세트 로드 시간을 줄이는 데 도움이 되기 위한 기능입니다. </p> <p>The report suites you select here are made available at the rule level, when you click <span class="uicontrol"> Add Suites</span> when creating a rule. </p> <p>Note: A report suite becomes available <span class="term"> only</span> when the report suites have at least one classification defined for the variable in <span class="wintitle"> Admin Tools</span>. <p>(See <span class="term"> Variable</span> in <a href="../../../components/c-classifications2/crb/classification-rule-set.md#concept_CD3D510F5070486584F3BB535AE41524" format="dita" scope="local"> Classification Rule Sets</a> for an explanation about this prerequisite.) </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>규칙은 기존 값을 덮어씁니다. </p> </td> 
   <td colname="col2"> <p> (기본 설정) Importer(SAINT)를 통해 업로드한 분류를 포함한 기존 분류 키들을 항상 덮어씁니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>규칙은 설정이 해제된 값만 덮어씁니다. </p> </td> 
   <td colname="col2"> <p>빈(설정이 해제된) 셀만 채웁니다. 기존 분류는 변경되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>전환 확인 기간 </p> </td> 
   <td colname="col2"> <p>규칙을 활성화하고 유효성을 확인할 때, 영향을 받는 키에 대해 규칙이 기존 분류를 덮어쓰도록 지정할 수 있습니다. 지정한 기간 내에 <span class="keyword">Adobe Analytics</span>로 전달된 적이 있는 분류된 키만 영향을 받습니다. </p> <p><span class="term"> [확인] 창을</span>지정하지 않으면 규칙은 대략 한 달 (현재 날짜에 따라 다름) 에 적용됩니다. 이 옵션을 활성화하지 않으면 기존 분류를 덮어쓰는 일은 없습니다. </p> <p><b>개발 센터</b>: 파트너는 <span class="wintitle">개발 센터</span>에서 분류 규칙을 만들 수 있습니다. 이 규칙은 고객이 통합을 활성화하면 배포됩니다. <span class="wintitle">개발 센터</span>의 <span class="uicontrol">다음 날짜 이후 덮어쓰기</span> 옵션은 고객이 통합을 활성화하거나 편집할 때 덮어쓰기 값을 결정할 수 있는지 여부를 파트너가 지정할 수 있도록 해줍니다. </p> <p>See <a href="../../../components/c-classifications2/crb/classification-quickstart-rules.md#concept_A67A23F523844D37898583C632DB9D25" format="dita" scope="local"> How Rules Are Processed</a> for more information about rule processing. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="../../../components/c-classifications2/crb/classification-quickstart-rules.md#task_86F216DFD2534FA181E64ABDF306782B" format="dita" scope="local"> 규칙 추가 </a> </td> 
   <td colname="col2"> <p>규칙 세트에 규칙을 추가할 수 있습니다. </p> <p>참고: 값이 규칙 세트에서 2회 이상 일치하는 경우, 시스템은 마지막 규칙을 사용하여 값을 분류합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 초안</span> </td> 
   <td colname="col2"> 규칙이 초안 모드가 되도록 지정할 수 있습니다. 초안 상태를 통해 규칙을 실행하기 전에 테스트할 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 복제</span> </td> 
   <td colname="col2"> 규칙 세트를 다른 변수에 적용하거나 다른 보고서 세트의 동일한 변수에 적용할 수 있도록 규칙 세트를 복제(복사)합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../components/c-classifications2/crb/classification-quickstart-rules.md#task_618A1E7CC8664E728F312250E8367158" format="dita" scope="local"> 테스트 규칙 세트 </a> </p> </td> 
   <td colname="col2"> <p>규칙 세트의 유효성을 테스트할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 일치 조건</span> </td> 
   <td colname="col2"> 규칙에 대해 원하는 조건을 지정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 분류 작업</span> </td> 
   <td colname="col2"> <p>일치 조건이 발생하면 수행할 작업을 지정합니다. </p> <p>예를 들면 캠페인 이름을 $2로 설정하면 추적 코드의 위치 2를 캠페인 이름으로 식별합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> #</span> </td> 
   <td colname="col2"> <p>규칙 번호입니다. </p> <p>자세한 내용은 <a href="../../../components/c-classifications2/crb/classification-quickstart-rules.md#concept_A67A23F523844D37898583C632DB9D25" format="dita" scope="local"> 규칙 처리 방법</a>을 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 규칙 유형 선택</span> </td> 
   <td colname="col2"> <p>각 규칙 세트는 특정 변수에 적용됩니다. 유효한 선택은 다음과 같습니다. </p> 
    <ul id="ul_6A8E06BB4AF2402B99C215823CB3D59D"> 
     <li id="li_5C702D4F460841D38A59621A5161A3BC">다음으로 시작 </li> 
     <li id="li_8052A741D9F34A2FBC136C181600193E">종료 문자 </li> 
     <li id="li_D0FA6EA4F09644FFBC9E6BC568BE80AC">포함 </li> 
     <li id="li_48675FE5253942ED887C6A72D1DCEF54"> <a href="../../../components/c-classifications2/crb/classification-quickstart-rules.md#concept_8A63F9BCF9484963962E14E6286D312D" format="dita" scope="local"> 정규 표현식 </a> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 일치 기준 입력</span> </td> 
   <td colname="col2"> 키에서 찾고 있는 텍스트 패턴입니다. 이 기준은 검색어, 문자 또는 정규 표현식이 될 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 분류 설정</span> </td> 
   <td colname="col2"> 일치 기준이 충족되는 경우 설정할 분류 열입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 종료</span> </td> 
   <td colname="col2"> 일치 기준이 충족되는 경우 선택한 분류 열에 대해 지정할 값입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 필터 </td> 
   <td colname="col2"> 규칙을 검색할 수 있습니다. </td> 
  </tr> 
 </tbody> 
</table>

## 정규 표현식 페이지 {#section_C932A5469E774841B2229965A154163C}

[!UICONTROL 정규 표현식] 페이지에서 정규 표현식을 편집할 수 있습니다.

![](assets/regex_tracking_code.png)

**정의**

| 요소 | 설명 |
|---|---|
| 샘플 키 | 사용할 테스트 문자열입니다. 예를 들면 추적 코드의 특정 문자로부터 분류를 만들 수 있습니다. 특정 문자, 단어 또는 문자 패턴을 일치시킬 수 있습니다. |
| 일치 그룹 | 캠페인 ID에서 위치를 분류할 수 있도록 정규 표현식이 캠페인 ID 문자에 대응하는 방식을 표시합니다. |
| 일치 결과 | 정규 표현식과 일치하는 문자열의 각 부분을 표시합니다. |

see [분류 규칙의 정규 표현식](../../../components/c-classifications2/crb/classification-quickstart-rules.md#concept_8A63F9BCF9484963962E14E6286D312D).

## 테스트 페이지 {#section_EC926F97901C4E65901413F9683AA70A}

이 페이지를 통해 세트에서 규칙을 테스트할 수 있습니다.

**정의**

| 요소 | 설명 |
|---|---|
| 테스트 실행 | 규칙 세트를 테스트할 때 보고서의 키를 사용하여 이러한 보고서 키가 규칙 세트에 의해 어떤 영향을 받는지 확인하십시오. |
| 필터 | [!UICONTROL 결과] 패널에서 값을 필터링합니다. |

