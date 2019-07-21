---
description: 숫자 2 분류 가져오기 지침을 제공하기 위한 예입니다.
seo-description: 숫자 2 분류 가져오기 지침을 제공하기 위한 예입니다.
seo-title: 예
solution: Analytics
subtopic: 분류
title: 예
topic: 관리 도구
uuid: 0553 D 07 F -87 C 1-4372-90 CE -7118 A 6393 A 01
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 예

숫자 2 분류 가져오기 지침을 제공하기 위한 예입니다.

<!-- 

c_example_1__rate.xml

 -->

이 경우에는 [!UICONTROL 분류 전환] 관리자에서 분류를 만들고 다음 1월의 값을 가져오려고 합니다.

| 키 | MyText | `~MyCost` | `~MyCost^~id~` | `~MyCost^~value~` |
|---|---|---|---|---|
| Product1 | Text1 | `Cost1_jan_var` |  | `.2` |
| Product2 | Text2 | `Cost2_jan_var` |  | `.3` |

| `~MyCost^~period~` | `~MyCost^~rate~` | `~MyCost^~hinge~` |
|---|---|---|
| 2010/01/01 - 2010/01/31 | revenue | revenue |
| 2010/01/01 - 2010/01/31 | revenue | revenue |

In January, Product1 had a cost of 20% of its revenue (shown in `~MyCost^~value~`) and Product2 had a cost of 30% of its revenue. Because you are importing a new row, `~MyCost^~id~` is blank.

## 결과 {#section_E0569289C9B34C479C7D2CD9ECBF866E}

보고서의 출력 예는 다음과 같습니다.

기간: 2010년 1월

보고서: 제품

| 제품 | Revenue | MyCost |
|---|---|---|
| Product1 | $10,000.23 | $2000.05 |
| Product2 | $9,000.04 | $2700.01 |

<!-- 

c_example_2__rate.xml

 -->

| 키 | MyText | `~MyCost` | `~MyCost^~id~` | `~MyCost^~value~` |
|---|---|---|---|---|
| Product1 | Text1 | `Cost1_jan_var` | 1 | .2 |
| Product2 | Text2 | `Cost2_jan_var` | 2 | .3 |
| Product1 | Text1 | `Cost1_feb_var` |  | .15 |
| Product2 | Text2 | `Cost2_feb_var` |  | .25 |

| `~MyCost^~period~` | `~MyCost^~rate~` | `~MyCost^~hinge~` |
|---|---|---|
| 2010/01/01 - 2010/01/31 | revenue | revenue |
| 2010/01/01 - 2010/01/31 | revenue | revenue |
| 2010/02/01 - 2010/02/28 | revenue | revenue |
| 2010/02/01 - 2010/02/28 | revenue | revenue |

2월에 Product1의 사용자 비용은 매출의 15%까지 감소했으며 Product2는 매출의 25%까지 감소했습니다.

## 결과 {#section_23DF5353AC1B478C88647F222703352C}

보고서의 출력 예는 다음과 같습니다.

기간: 2010년 1월

보고서: 제품

| 제품 | Revenue | MyCost |
|---|---|---|
| Product1 | $10,000.23 | $2000.05 |
| Product2 | $9,000.04 | $2700.01 |

기간: 2010년 2월

보고서: 제품

| 제품 | Revenue | MyCost |
|---|---|---|
| Product1 | $15,500.75 | $2325.11 |
| Product2 | $12,300.52 | $3075.13 |

기간: 2010년 1월 1일 - 2010년 2월 28일

보고서: 제품

| 제품 | Revenue | MyCost |
|---|---|---|
| Product1 | $25,500.98 | $4325.16 |
| Product2 | $21,300.56 | $5,775.14 |

<!-- 

c_example_3__fixed.xml

 -->

다음 데이터를 가져옵니다.

| 키 | MyText | `~MyCost` | `~MyCost^~id~` | `~MyCost^~value~` |
|---|---|---|---|---|
| Product1 | Text1 | `Cost1_mar_fixed` |  | 3000.00 |
| Product2 | Text2 | `Cost2_jan_fixed` |  | 2000.00 |

| `~MyCost^~period~` | `~MyCost^~rate~` | `~MyCost^~hinge~` |
|---|---|---|
| 2010/03/01 - 2010/03/31 | fixed | none |
| 2010/03/01 - 2010/03/31 | fixed | none |

## Result {#section_674B57ADB8284B878F9E670038C31464}

보고서의 출력 예는 다음과 같습니다.

기간: 2010년 3월

보고서: 제품

| 제품 | Revenue | MyCost |
|---|---|---|
| Product1 | $11,023.75 | $3000.00 |
| Product2 | $8,000.12 | $2000.00 |

<!-- 

c_example_4__(advanced)_multiple_row_per_time_period.xml

 -->

이 예에서는 1월에 배송 비용 500달러를 추가했으며 2월에 600달러를 추가했습니다.

| 키 | MyText | `~MyCost` | `~MyCost^~id~` | `~MyCost^~value~` |
|---|---|---|---|---|
| Product1 | Text1 | `Cost1_jan_var` | 1 | .2 |
| Product1 | Text1 | `Cost2_jan_fixed` |  | 500 |
| Product1 | Text1 | `Cost1_feb_var` | 2 | .15 |
| Product1 | Text1 | `Cost2_feb_fixed` |  | 600 |

| `~MyCost^~period~` | `~MyCost^~rate~` | `~MyCost^~hinge~` |
|---|---|---|
| 2010/01/01 - 2010/01/31 | revenue | revenue |
| 2010/01/01 - 2010/01/31 | fixed | none |
| 2010/02/01 - 2010/01/31 | revenue | revenue |
| 2010/02/01 - 2010/01/31 | fixed | none |

이전에 가져온 행에는 ID가 있는데, 이것은 새로운 비용이 아님을 나타냅니다.

## 결과 {#section_2096084176614B9AA60F97D5853CB9EA}

보고서의 출력 예는 다음과 같습니다.

기간: 2010년 1월

보고서: 제품

| 제품 | Revenue | MyCost |
|---|---|---|
| Product1 | $10,000.23 | $2500.05 |

>[!NOTE]
>
>이 기능은 고급 사용자가 값을 근사화하는 데 사용됩니다. 결과 정보는 정확한 값으로 간주할 수 없습니다.

<!-- 

c_example_5__identical_rate_hinge.xml

 -->

다음은 이 예를 보여 줍니다.

| 키 | MyText | `~MyCost` | `~MyCost^~id~` | `~MyCost^~value~` |
|---|---|---|---|---|
| Product1 | Text1 | `Cost1_mar_var` |  | 1 |

| `~MyCost^~period~` | `~MyCost^~rate~` | `~MyCost^~hinge~` |
|---|---|---|
| 2010/03/01 - 2010/03/31 | order | order |

## 결과 {#section_39E24ECCC3B34C9AADC25572662750E5}

보고서의 출력 예는 다음과 같습니다.

기간: 2010년 3월

보고서: 페이지별 제품

| 페이지별 제품 | 주문 | MyCost |
|---|---|---|
| Product1 | 1000 | $1000.00 |
| 홈 페이지 | 600 | $600 |
| 장바구니 | 400 | $400 |

<!-- 

c_example_5__fixed_no_hinge.xml

 -->

| 키 | MyText | `~MyCost` | `~MyCost^~id~` | `~MyCost^~value~` |
|---|---|---|---|---|
| Product1 | Text1 | `Cost1_mar_fixed` |  | 3000.00 |
| Product2 | Text2 | `Cost2_mar_fixed` |  | 2000.00 |

| `~MyCost^~period~` | `~MyCost^~rate~` | `~MyCost^~hinge~` |
|---|---|---|
| 2010/03/01 - 2010/03/31 | fixed | none |
| 2010/03/01 - 2010/03/31 | fixed | none |

## Result {#section_7F5F5970077D4E14A5DC91495E23540D}

보고서의 출력 예는 다음과 같습니다.

기간: 2010년 3월

보고서: 페이지별 제품

| 페이지별 제품 | 주문 | MyCost |
|---|---|---|
| Product1 | 1000 | $3000.00 |
| 홈 페이지 | 600 | 0 |
| 장바구니 | 400 | 0 |

<!-- 

c_example_7__fixed_hinge.xml

 -->

이 경우 다음 데이터를 가져옵니다.

| 키 | MyText | `~MyCost` | `~MyCost^~id~` | `~MyCost^~value~` |
|---|---|---|---|---|
| Product1 | Text1 | `Cost1_mar_fixed` |  | 3000.00 |
| Product2 | Text2 | `Cost2_mar_fixed` |  | 2000.00 |

| `~MyCost^~period~` | `~MyCost^~rate~` | `~MyCost^~hinge~` |
|---|---|---|
| 2010/03/01 - 2010/03/31 | fixed | revenue |
| 2010/03/01 - 2010/03/31 | fixed | revenue |

## 결과 {#section_5953BB6FD0CE4EF69D1D60B8B1203431}

보고서의 출력 예는 다음과 같습니다.

기간: 2010년 3월

보고서: 페이지별 제품

| 페이지별 제품 | 주문 | MyCost |
|---|---|---|
| Product1 | 1000 | $3000.00 |
| 홈 페이지 | 600 | $1800.00 |
| 장바구니 | 400 | $1200.00 |

<!-- 

c_example_7_continued__different_rate_hinge.xml

 -->

이 경우 다음 파일 데이터를 가져옵니다.

| 키 | MyText | `~MyCost` | `~MyCost^~id~` | `~MyCost^~value~` |
|---|---|---|---|---|
| Product1 | Text1 | Cost1_mar_fixed |  | 3 |

| `~MyCost^~period~` | `~MyCost^~rate~` | `~MyCost^~hinge~` |
|---|---|---|
| 2010/03/01 - 2010/03/31 | order | revenue |

## 결과 {#section_6E2604D9A3B0455585EFF0F80FF54127}

보고서의 출력 예는 다음과 같습니다.

기간: 2010년 3월

보고서: 페이지별 제품

| 페이지별 제품 | 주문 | MyCost |
|---|---|---|
| Product1 | 1000 | $3000.00 |
| 홈 페이지 | 600 | $1,000.00 |
| 장바구니 | 400 | $2,000.00 |

