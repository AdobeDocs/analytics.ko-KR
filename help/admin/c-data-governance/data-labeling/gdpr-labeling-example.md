---
description: 히트 데이터, 액세스 요청, 삭제 요청에 대한 데이터에 레이블을 지정하는 방법에 대한 예를 보여 줍니다.
title: 레이블 지정의 예
feature: Data Governance
exl-id: 9bea8636-c79c-4998-8952-7c66d31226e3
source-git-commit: b0716d9a4ea51dc0e1e6fc024f3de6b01a9ccfd8
workflow-type: tm+mt
source-wordcount: '814'
ht-degree: 100%

---

# 레이블 지정의 예

## 샘플 히트 데이터

다음 히트 데이터가 있다고 가정합니다.

* 첫 번째 행에는 각 변수의 레이블이 포함됩니다.
* 두 번째 행은 변수의 이름입니다. ID 레이블이 있는 경우에는 괄호 안에 지정된 네임스페이스가 포함됩니다.
* 히트 데이터는 세 번째 행에서 시작됩니다.

| 레이블 | I2<br>ID-PERSON<br>DEL-PERSON<br>ACC-PERSON | I2<br>ID-DEVICE<br>DEL-DEVICE<br>ACC-ALL | I2<br>DEL-PERSON<br>ACC-PERSON | I2<br>DEL-DEVICE<br>DEL-PERSON<br>ACC-ALL | I2<br>ID-DEVICE<br>DEL-DEVICE<br>ACC-ALL |
|---|---|---|---|---|---|
| **변수 이름** <br> **(네임스페이스)** | **MyProp1** <br> **(사용자)** | **방문자 ID** <br> **(AAID)** | **MyEvar1** | **MyEvar2** | **MyEvar3** <br> **(xyz)** |
| 히트 데이터 | Mary | 77 | A | M | X |
|  | Mary | 88 | B | N | Y |
|  | Mary | 99 | C | O | Z |
|  | John | 77 | D | P | W |
|  | John | 88 | E | N | U |
|  | John | 44 | F | Q | V |
|  | John | 55 | G | R | X |
|  | Alice | 66 | A | N | Z |

## 샘플 액세스 요청

액세스 요청을 제출하면 요약 파일에 아래 표에 표시된 값이 포함됩니다. 요청은 디바이스 파일만 반환하거나 개인 파일만 반환할 수 있습니다 (즉, 각각에 대해 하나). 개인 ID가 사용되고 expandIds가 true인 경우에만 두 개의 요약 파일이 반환됩니다.

<table>
  <tr>
    <th colspan="2" style="text-align:center">API 값</th>
    <th rowspan="2">반환된<br>파일 유형</th>
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

expandIDs에 대한 설정은 쿠키 ID를 사용할 때 출력에 영향을 미치지 않습니다.

## 샘플 삭제 요청

삭제 요청에 표의 첫 번째 행에 있는 API 값을 사용하면 히트 표가 다음과 같이 업데이트됩니다.

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
>AAID = 77 레이블 및 DEL-DEVICE 레이블을 포함하는 행의 셀만 영향을 받습니다.

<table>
  <tr>
    <th colspan="5" style="text-align:center">user=Mary<br>expandIDs=false</th>
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
>user=Mary 레이블 및 DEL-PERSON 레이블을 포함하는 행의 셀만 영향을 받습니다. 또한 A_ID를 포함하는 변수는 prop 또는 eVar일 수 있습니다. 대체 값은 다른 임의의 숫자 값이 아닌 “개인정보 보호-”로 시작하는 문자열 뒤에 난수(GUID)가 결합한 값이 됩니다.

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
* ID 확장 때문에 `AAID=77`, `AAID=88` 또는 `AAID=99`(이는 `user=Mary`를 포함하는 행의 AAID 값) 그리고 `DEL-DEVICE` 레이블을 포함하는 행의 셀이 영향을 받습니다. 여기에는 `user=Mary`인 행에서 `DEL-DEVICE` 레이블을 갖는 셀이 포함됩니다. 이 때문에 `DEL-DEVICE` 레이블(AAID, MyEvar2 및 MyEvar3)을 갖는 4와 5행(그리고 1-3행)의 셀은 난독화됩니다.
* expandID 설정은 `user=Mary`일 때 ID-DEVICE 레이블이 있는 MyEvar3(`X`, `Y` 그리고 `Z`)에 있는 값을 포함하는 호출까지 확장되지 않습니다. ExpandID는 `user=Mary`인 행의 방문자 ID(이 예에서는 AAID이지만 ECID도 포함)만 포함하도록 확장됩니다. 따라서 MyEvar3 값 `X`과 `Z`를 포함하는 마지막 두 행은 영향을 받지 않습니다.
* 이들 행에는 첫 번째 및 두 번째 행과 같은 방문자 ID 값(`77`와 `88`)이 포함되어 있기 때문에 네 번째 및 다섯 번째 행의 `MyEvar2`이 업데이트됩니다. 따라서 ID 확장에는 디바이스 수준의 삭제에 대한 값이 포함됩니다.
* 2행과 5행의 `MyEvar2` 값은 삭제 전과 후 모두 일치합니다. 단, 해당 행은 삭제 요청의 일부로 업데이트된 행이 아니기 때문에 일단 삭제가 되면 마지막 행에 발생한 값 `N`과 더 이상 일치하지 않습니다.
* `MyEvar3`는 ID 확장을 하지 않은 경우와는 전혀 다르게 작동합니다. ID 확장을 하지 않으면 일치하는 `ID-DEVICES`가 없기 때문입니다. 이제 `AAID`는 첫 5행과 일치합니다.
