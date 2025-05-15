---
description: 히트 데이터, 액세스 요청, 삭제 요청에 대한 데이터에 레이블을 지정하는 방법에 대한 예를 보여 줍니다.
title: 레이블 지정의 예
feature: Data Governance
role: Admin
exl-id: 9bea8636-c79c-4998-8952-7c66d31226e3
source-git-commit: 3e87d420591405e57e57e18fda4287d5fbd3bf1b
workflow-type: ht
source-wordcount: '723'
ht-degree: 100%

---

# 레이블 지정의 예

## 샘플 히트 데이터 {#hit}

다음 히트 데이터가 있다고 가정합니다.

* 첫 번째 행에는 각 변수의 레이블이 포함됩니다.
* 두 번째 행은 변수의 이름입니다. ID 레이블이 있는 경우에는 괄호 안에 지정된 네임스페이스가 포함됩니다.
* 히트 데이터는 세 번째 행에서 시작됩니다.

| 레이블 | I2<br>ID-PERSON<br>DEL-PERSON<br>ACC-PERSON | I2<br>ID-DEVICE<br>DEL-DEVICE<br>ACC-ALL | I2<br>DEL-PERSON<br>ACC-PERSON | I2<br>DEL-DEVICE<br>DEL-PERSON<br>ACC-ALL | I2<br>ID-DEVICE<br>DEL-DEVICE<br>ACC-ALL |
|---|---|---|---|---|---|
| **변수 이름** <br> **(네임스페이스)** | **MyProp1** <br> **(사용자)** | **방문자 ID** <br> **(AAID)** | **MyEvar1** | **MyEvar2** | **MyEvar3** <br> **(xyz)** |
| 히트 데이터 | Mary | 77 | A | M | X |
| | Mary | 88 | B | N | Y |
| | Mary | 99 | C | O | Z |
| | John | 77 | D | P | W |
| | John | 88 | E | N | U |
| | John | 44 | F | Q | V |
| | John | 55 | G | R | X |
| | Alice | 66 | A | N | Z |

## 샘플 액세스 요청 {#access}

액세스 요청을 제출하면 데이터 주체에게 반환할 수 있는 두 개의 파일을 받게 됩니다. 한 파일은 데이터 주체에 대해 수신된 각 히트에 대한 행과 각 변수에 대해 적절한 액세스 레이블이 포함된 열을 가진 CSV 파일입니다. 다른 파일은 각 변수를 나열하고, 해당 변수에 대해 데이터 주체의 고유 값과 각 고유 값이 나타난 횟수를 포함하는 요약 HTML 파일입니다.

예를 들어 요약 파일에는 아래 표에 표시된 값이 포함되어 있습니다. 요청은 디바이스 파일만 반환하거나 개인 파일만 반환할 수 있습니다(즉, 각각에 대해 하나). 개인 ID가 사용되고 `expandIds`가 true인 경우에만 두 개의 요약 파일이 반환됩니다.

<table>
  <tr>
    <th colspan="2" style="text-align:center">API 값</th>
    <th rowspan="2">반환된<br/>파일<br/>유형</th>
    <th colspan="5" style="text-align:center">요약 액세스 파일 데이터</th>
  </tr>
  <tr>
    <th>네임스페이스/ID</th>
    <th>expandIDs</th>
    <th>MyProp1</th>
    <th>방문자 ID</th>
    <th>MyEvar1</th>
    <th>MyEvar2</th>
    <th>MyEvar3</th>
  </tr>
  <tr>
    <td>AAID=77</td>
    <td>false</td>
    <td>디바이스</td>
    <td>없음</td>
    <td>77</td>
    <td>없음</td>
    <td>M, P</td>
    <td>X, W</td>
  </tr>
  <tr>
    <td>AAID=77</td>
    <td>true</td>
    <td>디바이스</td>
    <td>없음</td>
    <td>77</td>
    <td>없음</td>
    <td>M, P</td>
    <td>X, W</td>
  </tr>
  <tr>
    <td>user=Mary</td>
    <td>false</td>
    <td>사람</td>
    <td>Mary</td>
    <td>77, 88, 99</td>
    <td>A, B, C</td>
    <td>M, N, O</td>
    <td>X, Y, Z</td>
  </tr>
  <tr>
    <td rowspan="2">user=Mary</td>
    <td rowspan="2">true</td>
    <td>사람</td>
    <td>Mary</td>
    <td>77, 88, 99</td>
    <td>A, B, C</td>
    <td>M, N, O</td>
    <td>X, Y, Z</td>
  </tr>
  <tr>
    <td>디바이스</td>
    <td>없음</td>
    <td>77, 88</td>
    <td>A, B, C</td>
    <td>N, P</td>
    <td>U, W</td>
  </tr>
  <tr>
    <td rowspan="2">user=Mary<br>AAID=66</td>
    <td rowspan="2">true</td>
    <td>사람</td>
    <td>Mary</td>
    <td>77, 88, 99</td>
    <td>A, B, C</td>
    <td>M, N, O</td>
    <td>X, Y, Z</td>
  </tr>
  <tr>
    <td>디바이스</td>
    <td>없음</td>
    <td>66, 77, 88</td>
    <td>A, B, C</td>
    <td>N, P</td>
    <td>U, W, Z</td>
  </tr>
  <tr>
    <td>xyz=X</td>
    <td>false</td>
    <td>디바이스</td>
    <td>없음</td>
    <td>55, 77</td>
    <td>없음</td>
    <td>M, R</td>
    <td>X</td>
  </tr>
  <tr>
    <td>xyz=X</td>
    <td>true</td>
    <td>디바이스</td>
    <td>없음</td>
    <td>55, 77</td>
    <td>없음</td>
    <td>M, P, R</td>
    <td>W, X</td>
  </tr>
</table>

`expandIDs`에 대한 설정은 쿠키 ID를 사용할 때 출력에 영향을 미치지 않습니다.

## 샘플 삭제 요청 {#delete}

삭제 요청에 테이블의 첫 번째 행에 있는 API 값을 사용하면 히트 테이블이 다음과 같이 업데이트됩니다.

<table>
  <tr>
    <th colspan="5" style="text-align:center">AAID=77 <br>(expandIDs 값은 상관없음)</th>
  </tr>
  <tr>
    <th>MyProp1</th>
    <th>AAID</th>
    <th>MyEvar1</th>
    <th>MyEvar2</th>
    <th>MyEvar3</th>
  </tr>
  <tr>
    <td>Mary</td>
    <td>42</td>
    <td>A</td>
    <td>개인정보 보호-7398</td>
    <td>개인정보 보호-9152</td>
  </tr>
  <tr>
    <td>Mary</td>
    <td>88</td>
    <td>B</td>
    <td>N</td>
    <td>Y</td>
  </tr>
  <tr>
    <td>Mary</td>
    <td>99</td>
    <td>C</td>
    <td>O</td>
    <td>Z</td>
  </tr>
  <tr>
    <td>John</td>
    <td>42</td>
    <td>D</td>
    <td>개인정보 보호-1866</td>
    <td>개인정보 보호-8216</td>
  </tr>
  <tr>
    <td>John</td>
    <td>88</td>
    <td>E</td>
    <td>N</td>
    <td>U</td>
  </tr>
  <tr>
    <td>John</td>
    <td>44</td>
    <td>F</td>
    <td>Q</td>
    <td>V</td>
  </tr>
  <tr>
    <td>John</td>
    <td>55</td>
    <td>G</td>
    <td>R</td>
    <td>X</td>
  </tr>
  <tr>
    <td>Alice</td>
    <td>66</td>
    <td>A</td>
    <td>N</td>
    <td>Z</td>
  </tr>
</table>

>[!NOTE]
>
>`AAID=77` 및 `DEL-DEVICE` 레이블이 있는 행의 열만 영향을 받습니다.

<table>
  <tr>
    <th colspan="5" style="text-align:center">user=Mary <br> expandIDs=false</th>
  </tr>
  <tr>
    <th>MyProp1</th>
    <th>AAID</th>
    <th>MyEvar1</th>
    <th>MyEvar2</th>
    <th>MyEvar3</th>
  </tr>
  <tr>
    <td>개인정보 보호-0523</td>
    <td>77</td>
    <td>개인정보 보호-1866</td>
    <td>개인정보 보호-3681</td>
    <td>X</td>
  </tr>
  <tr>
    <td>개인정보 보호-0523</td>
    <td>88</td>
    <td>개인정보 보호-2178</td>
    <td>개인정보 보호-1975</td>
    <td>Y</td>
  </tr>
  <tr>
    <td>개인정보 보호-0523</td>
    <td>99</td>
    <td>개인정보 보호-9045</td>
    <td>개인정보 보호-2864</td>
    <td>Z</td>
  </tr>
  <tr>
    <td>John</td>
    <td>77</td>
    <td>D</td>
    <td>P</td>
    <td>W</td>
  </tr>
  <tr>
    <td>John</td>
    <td>88</td>
    <td>E</td>
    <td>N</td>
    <td>U</td>
  </tr>
  <tr>
    <td>John</td>
    <td>44</td>
    <td>F</td>
    <td>Q</td>
    <td>V</td>
  </tr>
  <tr>
    <td>John</td>
    <td>55</td>
    <td>G</td>
    <td>R</td>
    <td>X</td>
  </tr>
  <tr>
    <td>Alice</td>
    <td>66</td>
    <td>A</td>
    <td>N</td>
    <td>Z</td>
  </tr>
</table>

>[!NOTE]
>
>`user=Mary` 및 `DEL-PERSON` 레이블이 있는 행의 열만 영향을 받습니다. 또한 `A_ID`를 포함하는 변수는 prop 또는 eVar일 수 있습니다. 대체 값은 다른 임의의 숫자 값이 아닌 `Privacy-`로 시작하는 문자열 뒤에 난수(GUID)가 결합한 값이 됩니다.

<table>
  <tr>
    <th colspan="5" style="text-align:center">user=Mary <br> expandIDs=true</th>
  </tr>
  <tr>
    <th>MyProp1</th>
    <th>AAID</th>
    <th>MyEvar1</th>
    <th>MyEvar2</th>
    <th>MyEvar3</th>
  </tr>
  <tr>
    <td>개인정보 보호-5782</td>
    <td>09</td>
    <td>개인정보 보호-0859</td>
    <td>개인정보 보호-8183</td>
    <td>개인정보 보호-9152</td>
  </tr>
  <tr>
    <td>개인정보 보호-5782</td>
    <td>16</td>
    <td>개인정보 보호-6104</td>
    <td>개인정보 보호-2911</td>
    <td>개인정보 보호-6821</td>
  </tr>
  <tr>
    <td>개인정보 보호-5782</td>
    <td>83</td>
    <td>개인정보 보호-2714</td>
    <td>개인정보 보호-0219</td>
    <td>개인정보 보호-4395</td>
  </tr>
  <tr>
    <td>John</td>
    <td>09</td>
    <td>D</td>
    <td>개인정보 보호-8454</td>
    <td>개인정보 보호-8216</td>
  </tr>
  <tr>
    <td>John</td>
    <td>16</td>
    <td>E</td>
    <td>개인정보 보호-2911</td>
    <td>개인정보 보호-2930</td>
  </tr>
  <tr>
    <td>John</td>
    <td>44</td>
    <td>F</td>
    <td>Q</td>
    <td>V</td>
  </tr>
  <tr>
    <td>John</td>
    <td>55</td>
    <td>G</td>
    <td>R</td>
    <td>X</td>
  </tr>
  <tr>
    <td>Alice</td>
    <td>66</td>
    <td>A</td>
    <td>N</td>
    <td>Z</td>
  </tr>
</table>

다음 사항을 참고하십시오.

* `user=Mary`과 `DEL-PERSON` 레이블을 포함하는 행의 셀만 영향을 받습니다.

