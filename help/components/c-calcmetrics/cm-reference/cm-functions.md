---
description: '[계산된 지표 빌더]를 사용하면 [고급 계산 지표]에 통계 및 수학 함수를 적용할 수 있습니다.'
title: 참조  기본 함수
uuid: 5c2b4a0e-613c-4b27-95b8-01d480aeab78
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 참조: 기본 함수

[계산된 지표 빌더]를 사용하면 [고급 계산 지표]에 통계 및 수학 함수를 적용할 수 있습니다.

다음은 함수 및 그 정의를 알파벳 순서로 나열한 것입니다.

>[!NOTE] [!DNL metric]가 함수에서 인수로 식별되는 경우, 지표의 다른 표현식도 허용됩니다. 예를 들어 [!DNL MAXV(metrics)]는 [!DNL MAXV(PageViews + Visits).]에도 허용됩니다.

## 테이블 함수 대 행 함수 {#section_8977BE40A47E4ED79EB543A9703A4905}

테이블 함수는 출력이 표의 모든 행에 대해 동일한 함수입니다. 행 함수는 출력이 표의 모든 행에 대해 다른 함수입니다.

## 절대값(행) {#concept_4CC47884F7CA49D5B84AC898EA596673}

숫자의 절대값을 반환합니다. 숫자의 절대값은 양의 값을 갖는 숫자입니다.

```
ABS(metric)
```

| 인수 | 설명 |
|---|---|
| *metric* | 절대값이 필요한 지표. |

## 열 최대값 {#concept_B25518D717D24F82B65CDE49A153D3A3}

지표 열의 차원 요소 세트에서 가장 큰 값을 반환합니다. MAXV는 차원 요소 간의 단일 열(지표) 내에서 수직으로 평가합니다.

```
MAXV(metric)
```

| 인수 | 설명 |
|---|---|
| *metric* | 평가할 지표. |

## 열 최소값 {#concept_5B1033F8ACE9485F9AD3CDC0D146391B}

지표 열의 차원 요소 세트에서 가장 작은 값을 반환합니다. MINV는 차원 요소 간의 단일 열(지표) 내에서 수직으로 평가합니다.

```
MINV(metric)
```

| 인수 | 설명 |
|---|---|
| *metric* | 평가할 지표. |

## 열 합계 {#concept_391F04FBC3CC43368CA0C5AACE74D4B1}

열 내의 한 지표에 대한 모든 숫자 값을 추가합니다(차원의 요소들에 대해).

```
SUM(metric)
```

| 인수 | 설명 |
|---|---|
| *metric* | 합계 값 또는 합계가 필요한 지표. |

## 카운트(테이블) {#concept_2C6ED2B88AB74481BD130969FB071A41}

열 내의 지표에 대해 0이 아닌 값의 숫자 또는 개수를 반환합니다(차원 내에서 보고된 고유 요소 수).

```
COUNT(metric)
```

| 인수 | 설명 |
|---|---|
| *metric* | 카운트할 지표. |

## 지수(행) {#concept_17554F9D234449FB8DDEE895816B3FF1}

Returns *e* raised to the power of a given number. The constant *e* equals 2.71828182845904, the base of the natural logarithm. EXP is the inverse of LN, the natural logarithm of a number.

```
EXP(metric)
```

| 인수 | 설명 |
|---|---|
| *metric* | The exponent applied to the base *e*. |

## 거듭제곱 {#concept_941578534F1E4583B1BEB067C8113A21}

거듭제곱 연산자

<pre>
pow(x,y) = x<sup>y</sup> = x*x*x*… (y회)
</pre>

## 평균(테이블) {#concept_F4FF950580304D0B99DA7FBB5DB8730A}

열의 지표에 대해 산술 평균 또는 평균을 반환합니다.

```
MEAN(metric)
```

| 인수 | 설명 |
|---|---|
| *metric* | 평균이 필요한 지표. |

## 중간값(테이블) {#concept_183EC31208524EDB8463D986DE2E895F}

열의 지표에 대해 중간값을 반환합니다. 중간값은 숫자 집합의 중간에 있는 숫자입니다. 즉, 숫자의 절반은 중간값보다 크거나 같고, 나머지 절반은 중간값보다 작거나 같습니다.

```
MEDIAN(metric)
```

| 인수 | 설명 |
|---|---|
| *metric* | 중간값이 필요한 지표. |

## 모듈로 {#concept_DE0825D7A51643219CB01F59667EA352}

Euclidean 부서를 사용하여 col1 / col2의 나머지를 사용합니다.

x를 y로 나눈 후 나머지를 반환합니다.

```
x = floor(x/y) + modulo(x,y)
```

반환 값의 기호는 입력과 같습니다(또는 0임).

```
modulo(4,3) = 1 
modulo(-4,3) = -1 
modulo(-3,3) = 0
```

항상 양수를 얻으려면

```
modulo(modulo(x,y)+y,y)
```

## 백분위수(테이블) {#concept_51DF57B606D14F898E5010DBA61CA979}

지표에 대한 값의 k-번째 백분위수를 반환합니다. 이 함수를 사용하여 수락 임계값을 설정할 수 있습니다. 예를 들어 스코어가 90번째 백분위수를 넘는 차원 요소를 검사하기로 결정할 수 있습니다.

```
PERCENTILE(metric,k)
```

<table id="table_35CD840ACFB44CD9979881DB8823CC53"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 인수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <i>metric</i> </td> 
   <td colname="col2"> 상대적 순위를 정의하는 지표 열. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>k </p> </td> 
   <td colname="col2"> 0에서 100까지 범위의 백분위수 값. </td> 
  </tr> 
 </tbody> 
</table>

## 사분위수(테이블) {#concept_BFD37F0F23A24AD181407142233FA151}

지표 값 중 사분위수를 반환합니다. 예를 들어, 사분위수를 사용하면 수익이 가장 많은 제품의 상위 25%를 찾을 수 있습니다. MINV, MEDIAN 및 MAXV는 쿼트가 각각 0, 2 및 4일 때 QUARTILE와 동일한 값을 반환합니다.

```
QUARTILE(metric,quart)
```

<table id="table_64EA3DAAE77541439D59FAF0353F83A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 인수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <i>metric</i> </td> 
   <td colname="col2"> 사분위수 값이 필요한 지표. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>quart </p> </td> 
   <td colname="col2"> 반환할 *값을 나타냅니다. </td> 
  </tr> 
 </tbody> 
</table>

*If *quart* = 0, QUARTILE returns the minimum value. *quart* = 1일 경우, QUARTILE은 첫 번째 사분위수(25번째 백분위수)를 반환합니다. *quart* = 2일 경우, QUARTILE은 첫 번째 사분위수(50번째 백분위수)를 반환합니다. *quart* = 3일 경우, QUARTILE은 첫 번째 사분위수(75번째 백분위수)를 반환합니다. *quart* = 4일 경우에는, QUARTILE이 최대값을 반환합니다.

## 라운드 {#concept_2F12F2A6ACD445A0A8FF648AE4D4CB9E}

주어진 값에 가장 가까운 정수를 반환합니다. 예를 들어, 수입에 대해 소수 통화를 보고하지 않으려 하고, 제품에 $569.34가 있을 경우, 공식 Round(*수입*)을 사용하여 수입을 가장 근접한 달러 또는 $569로 반올림하십시오. $569.51로 보고되는 제품은 가장 가까운 달러 또는 $570로 반올림됩니다.

```
ROUND(metric)
```

| 인수 | 설명 |
|---|---|
| *수* | 반올림할 지표. |

숫자 매개 변수가 없는 반올림은 숫자 매개 변수가 0인 반올림과 같습니다. 즉, 가장 가까운 정수로 반올림하는 것과 같습니다. 숫자 매개 변수를 사용하면 소숫점 오른쪽에 그만큼 많은 숫자를 반환합니다. 숫자가 음수이면, 소숫점 왼쪽에 0들을 반환합니다.

```
round( 314.15, 0) = 314 
round( 314.15, 1) = 314.1 
round( 314.15, -1) = 310 
round( 314.15, -2) = 300
```

## 행 수 {#concept_0DBF5995881C47CF95F793125F3A0E2B}

주어진 열에 대한 행 수(차원 내에서 보고된 고유 요소 수)를 반환합니다. &quot;고유 수 초과&quot;는 1로 집계됩니다.

## 행 최대값 {#concept_984D045D7EDD4A1ABED454CDF2EC23C5}

각 행의 최대 열 수.

## 행 최소값 {#concept_A6FB9E72C70A43D0B31565E70B8122BD}

각 행의 최소 열 수.

## 행 합계 {#concept_E9EAB0FC5233498F907E7A078698A98E}

각 행의 열 합계.

## 제곱근(행) {#concept_6460DFA51EC24527A2317970FB76D404}

숫자의 양수 제곱근을 반환합니다. 숫자의 제곱근은 해당 숫자의 1/2승(거듭제곱) 값입니다.

```
SQRT(metric)
```

| 인수 | 설명 |
|---|---|
| *수* | 제곱근이 필요한 지표. |

## 표준 편차(테이블) {#concept_A383A8BCC6FA42D7B73F7C83997D782A}

샘플 데이터 채우기를 기준으로 표준 편차 또는 분산의 제곱근을 반환합니다.

STDEV의 방정식은 다음과 같습니다.

![](assets/std_dev.png)

여기서 x는 샘플 평균(*지표*)이고 *n* 은 샘플 크기입니다.

```
STDEV(metric)
```

<table id="table_8BCF2E4B02434AABAAD026FB3C4E8B2F"> 
 <tbody> 
  <tr> 
   <td> <b> 인수</b> </td> 
   <td> <b> 설명</b> </td> 
  </tr> 
  <tr> 
   <td> <b> <i> 지표</i></b> </td> 
   <td> <p> 표준 편차에 필요한 지표. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 분산(테이블) {#concept_269751EDC5A34E689112AE16E04A11B0}

샘플 데이터 채우기를 기준으로 분산을 반환합니다.

VARIANCE 방정식은 다음과 같습니다.

![](assets/variance_eq.png)

여기서 x는 샘플 평균(MEAN(*지표*)이고 *n* 은 샘플 크기입니다.

```
VARIANCE(metric)
```

| 인수 | 설명 |
|---|---|
| *metric* | 분산이 필요한 지표. |

분산을 계산하기 위해 전체 숫자 열을 봅니다. 그 숫자 목록에서 먼저 평균을 계산합니다. 평균을 얻으면 각 항목을 살펴보고 다음을 수행합니다.

1. 숫자에서 평균을 뺍니다.

2. 계산 결과를 제곱합니다.

3. 그 값을 총계에 더합니다.

전체 열에 대해 반복하면 하나의 합계가 있습니다. 그런 다음 해당 합계를 열의 항목 수로 나눕니다. 이 숫자는 열의 변화입니다. 그것은 하나의 숫자입니다. 그러나 숫자 열로 표시됩니다.

예를 들어 3개 항목 열이 있다고 가정해 보겠습니다.

1

2

3

이 열의 평균은 2입니다. 열의 변량은 (1 - 2)² + (2 - 2)² + (3 - 2)²/3 = 2/3입니다. 애드혹 분석에서는 다음과 같습니다.

1 2/3

2 2/3

3 2/3
