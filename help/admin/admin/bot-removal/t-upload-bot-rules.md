---
description: 보트 규칙 일괄 가져오기를 수행하기 위해 규칙을 정의하는 CSV 파일을 업로드할 수 있습니다.
seo-description: 보트 규칙 일괄 가져오기를 수행하기 위해 규칙을 정의하는 CSV 파일을 업로드할 수 있습니다.
seo-title: 보트 규칙 업로드
solution: Analytics
subtopic: 보트 규칙
title: 보트 규칙 업로드
topic: 관리 도구
uuid: BD 70 C 199-5817-437 E -980 D -6 D 8 F 95 D 82 F 2 C
translation-type: tm+mt
source-git-commit: 4a627e268994d0152a19fb44e9bc06ea7ebc64c6

---


# 보트 규칙 업로드

보트 규칙 일괄 가져오기를 수행하기 위해 규칙을 정의하는 CSV 파일을 업로드할 수 있습니다.

다음 열을 나타난 순서대로 포함하는 CSV 파일을 만듭니다.

<table id="table_770891EF9E4A49F695977BB6446736B5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code> 보트 이름</code> </p> </td> 
   <td colname="col2"> <p> <code> IP 시작 </code> </p> </td> 
   <td colname="col3"> <p> <code> IP 끝 </code> </p> </td> 
   <td colname="col4"> <p> <code> 에이전트 일치 규칙(포함 또는 다음으로 시작)</code> </p> </td> 
   <td colname="col5"> <p> <code> 에이전트 포함(100자 제한)</code> </p> </td> 
   <td colname="col6"> <p> <code> 에이전트 제외(255자 제한)</code> </p> </td> 
  </tr> 
 </tbody> 
</table>

세 가지 유형의 보트 규칙을 정의할 수 있습니다.

* 사용자 에이전트 포함 또는 다음으로 시작
* 단일 IP 주소 또는 와일드카드 일치
* IP 범위 일치

가져오기 파일의 각 행은 다음 보트 정의 중 하나만 포함할 수 있습니다.

* **사용자 에이전트 포함 또는 다음으로 시작**: [에이전트 포함] 열에 일치시킬 단일 사용자 에이전트 문자열을 입력합니다. [에이전트 일치 규칙] 필드에 *포함* 또는 *다음으로 시작*&#x200B;을 배치하여 수행할 일치 유형을 지정합니다. An optional value can be included in the Agent Exclude column that defines one or more pipe-delimited ( `|` ) strings that the Agent does not contain. 문자열 일치는 대/소문자를 구분하지 않습니다. IP 시작 열과 IP 끝 열은 모두 비어 있어야 합니다.

* **단일 IP 주소 또는 와일드카드 일치**: 단일 IP 주소 ( `10.10.10.1`) 또는 와일드카드 IP 주소 ( `10.10.*.*`) 와 일치시키려면 IP 시작 열과 IP 종료 열 모두에 동일한 값을 배치합니다. [일치 규칙], [에이전트 포함] 및 [에이전트 제외]는 비어 있어야 합니다.

* **IP 범위 일치**: IP 시작 및 IP 종료 열을 사용하여 IP 주소 범위를 정의합니다. Wildcards can be used to match IP ranges, for example `10.10.10.*` to `10.10.20.*`. [일치 규칙], [에이전트 포함] 및 [에이전트 제외]는 비어 있어야 합니다.

## OR로 결합된 다중 규칙

OR로 결합된 규칙의 조합을 사용하여 보트를 일치시키려면(예: 사용자 에이전트 또는 IP 주소) 보트 이름 필드에 결합할 모든 규칙에 대한 동일한 이름을 제공하십시오. AND 일치는 지원되지 않습니다.

## 업로드 파일로 모든 규칙 덮어쓰기

모든 기존 규칙을 삭제하고 업로드 파일에 정의된 규칙으로 대체하려면 **[!UICONTROL 기존 규칙 덮어쓰기]확인란을 선택하십시오.**

## 내보내기 규칙

**[!UICONTROL 업로드된 보트 파일 내보내기]버튼을 누르면 UI에 정의된 모든 규칙을 CSV 형식으로 내보냅니다.**
