---
description: 데이터 피드에서 사용된 특수 문자에 대한 정보
keywords: 데이터 피드; 작업; 특수 문자; hit_ data; 다중값 변수; events_ list; products_ list; mvvars
seo-description: 데이터 피드에서 사용된 특수 문자에 대한 정보
seo-title: 특수 문자
solution: Analytics
subtopic: 데이터 피드
title: 특수 문자
topic: Reports & Analytics
uuid: 5 EFE 019 B -39 E 6-4226-A 936-88202 A 02 F 5 E 6
translation-type: tm+mt
source-git-commit: 01a6fc7e44dc71b868bd38a4f6a5a4089eae6349

---


# 특수 문자

데이터 피드에서 사용된 특수 문자에 대한 정보

* [hit_data 파일의 특수 문자](../../../export/analytics-data-feed/c-df-contents/datafeeds-spec-chars.md#section_9759C7A6AE684EB5B4A154FB6A26B39E)
* [여러 값이 있는 변수의 특수 문자(events_list, products_list, mvvars)](../../../export/analytics-data-feed/c-df-contents/datafeeds-spec-chars.md#section_056F8D540FFC4F24A001DC74331C2AAC)
* [샘플 워크플로우](../../../export/analytics-data-feed/c-df-contents/datafeeds-spec-chars.md#section_97F8C2925A35433DA2E7E8BE60037E37)

## hit_data 파일의 특수 문자 {#section_9759C7A6AE684EB5B4A154FB6A26B39E}

다음 문자는 hit_data 파일에서 특별한 의미를 갖습니다.

| 문자 | 의미 | 설명 |
|--- |--- |--- |
| \t(탭 문자) | 열의 끝 | 데이터 필드의 끝을 표시합니다. |
| \n(줄바꿈 문자) | 행의 끝 | 데이터 행의 끝을 표시합니다. |
| \(백슬래시 문자) | 이스케이프 문자 | 문자가 데이터 수집 중 설정된 값의 일부인 경우 탭, 줄바꿈, 백슬래시를 이스케이프 처리합니다. |

특수 문자 앞에 백슬래시가 있으면 문자 그대로를 의미합니다.

| 문자 | 의미 | 설명 |
|--- |--- |--- |
| \\t | 탭 | 문자 그대로의 탭. 이 문자는 데이터 수집 중에 설정된 값의 일부입니다. |
| \\n | 줄바꿈 | 문자 그대로의 줄바꿈. 이 문자는 데이터 수집 중에 설정된 값의 일부입니다. |
| \\ | 백슬래시 | 문자 그대로의 백슬래시. 이 문자는 데이터 수집 중에 설정된 값의 일부입니다. |

## 여러 값이 있는 변수의 특수 문자(events_list, products_list, mvvars) {#section_056F8D540FFC4F24A001DC74331C2AAC}

다음 문자는 여러 값이 있는 변수에서 특별한 의미를 갖습니다.

<table id="table_FDA13DE05A784ED4972C2955BD2642C7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 문자 </th> 
   <th colname="col02" class="entry"> 의미 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <code>,</code>(쉼표 문자) </td> 
   <td colname="col02"> 값의 끝 </td> 
   <td colname="col2"> <p>제품 문자열, 이벤트 ID 또는 기타 값을 여러 값이 있는 변수에서 구분합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code>;</code>(세미콜론 문자) </td> 
   <td colname="col02"> 개별 제품 값 내에서 하위 값의 끝 </td> 
   <td colname="col2"> <p><code>product_list</code>에서 개별 제품과 연결된 값을 구분합니다 . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code>=</code>(등호 문자) </td> 
   <td colname="col02"> 값 할당 </td> 
   <td colname="col2"> <p><code>event_list</code>의 이벤트에 값을 할당합니다 . </p> </td> 
  </tr> 
 </tbody> 
</table>

특수 문자 앞에 삽입 기호가 있으면 문자 그대로를 의미합니다.

| 문자 | 의미 | 설명 |
|--- |--- |--- |
| ^, | 쉼표 | 문자 그대로의 쉼표. 이 문자는 데이터 수집 중에 설정된 값의 일부입니다. |
| ^; | 세미콜론 | 문자 그대로의 세미콜론. 이 문자는 데이터 수집 중에 설정된 값의 일부입니다. |
| ^= | 같음 | 문자 그대로의 등호. 이 문자는 데이터 수집 중에 설정된 값의 일부입니다. |
| ^^ | 삽입 기호 | 문자 그대로의 삽입 기호. 이 문자는 데이터 수집 중에 설정된 값의 일부입니다. |

## 샘플 워크플로우 {#section_97F8C2925A35433DA2E7E8BE60037E37}

데이터 피드의 열에 사용자가 제출한 데이터가 있으면 `split` 또는 `readLine` 등으로 데이터를 구분하기 전에 특수 문자가 있는지 확인해야 합니다.

다음 데이터를 생각해 보십시오.

| 브라우저 너비 | 브라우저 높이 | eVar1 | prop 1 |
|---|---|---|---|
| 1680 | 1050 | search\nstring | en |
| 800 | 600 | search\tstring | en |

내보내기 중에 eVar1의 줄바꿈 및 탭 문자가 이스케이프됩니다. 이 행에 대한 데이터 피드는 다음과 같이 표시됩니다.

```
1680\t1050\tsearch\\nstring\ten\n 
800\t600\tsearch\\tstring\ten\n
```

Calling `readLine()` on the first row returns the following partial string:

```
800\t600\tsearch\
```

Calling `split("\t")` on the second row returns the following string array:

```
800 
600 
search\ 
string 
en
```

이를 방지하려면 다음과 같은 방법을 사용하십시오.

1. 파일 첫 부분부터 탭, 줄바꿈, 백슬래시 또는 삽입 기호 문자를 찾을 때까지 읽어나갑니다.
1. 마주하는 특수 문자를 기준으로 작업을 수행합니다.

   * 탭 - 해당 시점부터 데이터 저장소 셀에 문자열을 삽입하고 계속합니다.
   * 줄바꿈 - 데이터 저장소 행을 완성합니다.
   * 백슬래시 - 다음 문자를 읽고 적절한 문자열을 삽입한 후 계속합니다.
   * 삽입 기호 - 다음 문자를 읽고 적절한 문자열을 삽입한 후 계속합니다.

