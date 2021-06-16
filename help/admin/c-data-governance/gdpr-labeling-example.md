---
description: 히트 데이터, 액세스 요청, 삭제 요청에 대한 데이터에 레이블을 지정하는 방법에 대한 예를 보여줍니다.
title: 레이블 지정 예
uuid: a9a5b937-dbde-4f0f-a171-005ef4c79df9
exl-id: 9bea8636-c79c-4998-8952-7c66d31226e3
source-git-commit: fe277bea867dc67e8693673a547adecccf169332
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 69%

---

# 레이블 지정 예

## 샘플 히트 데이터

다음 히트 데이터가 있다고 가정합니다.

* 첫 번째 행에는 각 변수의 레이블이 포함됩니다.
* 두 번째 행은 변수의 이름입니다. ID 레이블이 있는 경우에는 괄호 안에 지정된 네임스페이스가 포함됩니다.
* 히트 데이터는 세 번째 행에서 시작됩니다.

| 레이블 | I2<br>ID-PERSON<br>DEL-PERSON<br>ACC-PERSON | I2<br>ID-DEVICE<br>DEL-DEVICE<br>ACC-ALL | I2<br>DEL-PERSON<br>ACC-PERSON | I2<br>DEL-DEVICE<br>DEL-PERSON<br>ACC-ALL | I2<br>ID-DEVICE<br>DEL-DEVICE<br>ACC-ALL |
|---|---|---|---|---|---|
| **변수 이름** <br> **(네임스페이스)** | **MyProp1** <br> **(사용자)** | **Visitor ID** <br> **(AAID)** | **MyEvar1** | **MyEvar2** | **MyEvar3** <br> **(xyz)** |
| 히트 데이터 | Mary | 77 | A | M | X |
|  | 메리 | 88 | B | N | Y |
|  | 메리 | 99 | C | O | Z |
|  | John | 77 | D | P | W |
|  | 존 | 88 | E | N | U |
|  | 존 | 44 | F | Q | V |
|  | 존 | 55 | G | R | X |
|  | Alice | 66 | A | N | Z |

## 샘플 액세스 요청

액세스 요청을 제출하면 요약 파일에 아래 표에 표시된 값이 포함됩니다. 요청은 장치 파일만 반환하거나 개인 파일만 반환할 수 있습니다 (즉, 각각에 대해 하나). 개인 ID가 사용되고 expandIds가 true인 경우에만 두 개의 요약 파일이 반환됩니다.

<table>
  <tr>
    <th colspan="2" style="text-align:center">API 값</th>
    <th rowspan="2">반환된<br>파일 형식</th>
    <th colspan="5" style="text-align:center">요약 액세스 파일의 데이터</th>
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
    <td>장치</td>
    <td>없음</td>
    <td>77</td>
    <td>없음</td>
    <td>M, P</td>
    <td>X, W</td>
  </tr>
  <tr>
    <td>AAID=77</td>
    <td>true</td>
    <td>장치</td>
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
    <td>메리</td>
    <td>77, 88, 99</td>
    <td>A, B, C</td>
    <td>M, N, O</td>
    <td>X, Y, Z</td>
  </tr>
  <tr>
    <td rowspan="2">user=Mary</td>
    <td rowspan="2">true</td>
    <td>사람</td>
    <td>메리</td>
    <td>77,88,99</td>
    <td>A, B, C</td>
    <td>M, N, O</td>
    <td>X, Y, Z</td>
  </tr>
  <tr>
    <td>장치</td>
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
    <td>메리</td>
    <td>77,88,99</td>
    <td>A, B, C</td>
    <td>M, N, O</td>
    <td>X, Y, Z</td>
  </tr>
  <tr>
    <td>장치</td>
    <td>없음</td>
    <td>66, 77, 88</td>
    <td>A, B, C</td>
    <td>N, P</td>
    <td>U, W, Z</td>
  </tr>
  <tr>
    <td>xyz=X</td>
    <td>false</td>
    <td>장치</td>
    <td>없음</td>
    <td>55, 77</td>
    <td>없음</td>
    <td>M, R</td>
    <td>X</td>
  </tr>
  <tr>
    <td>xyz=X</td>
    <td>true</td>
    <td>장치</td>
    <td>없음</td>
    <td>55,77</td>
    <td>없음</td>
    <td>M, P, R</td>
    <td>W, X</td>
  </tr>
</table>

expandIDs에 대한 설정은 쿠키 ID를 사용할 때 출력에 영향을 미치지 않습니다.

## 샘플 삭제 요청

삭제 요청에 표의 첫 번째 행에 있는 API 값을 사용하면 히트 표가 다음과 비슷하게 업데이트됩니다.

<table>
  <tr>
    <th colspan="5" style="text-align:center">AAID=77 <br>(expandIDs 값은 중요하지 않음)</th>
  </tr>
  <tr>
    <th>MyProp1</th>
    <th>AAID</th>
    <th>MyEvar1</th>
    <th>MyEvar2</th>
    <th>MyEvar3</th>
  </tr>
  <tr>
    <td>메리</td>
    <td>42</td>
    <td>A</td>
    <td>개인 정보 보호-7398</td>
    <td>개인 정보 보호-9152</td>
  </tr>
  <tr>
    <td>메리</td>
    <td>88</td>
    <td>B</td>
    <td>N</td>
    <td>Y</td>
  </tr>
  <tr>
    <td>메리</td>
    <td>99</td>
    <td>C</td>
    <td>O</td>
    <td>Z</td>
  </tr>
  <tr>
    <td>존</td>
    <td>42</td>
    <td>D</td>
    <td>개인 정보 보호-1866</td>
    <td>개인 정보 보호-8216</td>
  </tr>
  <tr>
    <td>존</td>
    <td>88</td>
    <td>E</td>
    <td>N</td>
    <td>U</td>
  </tr>
  <tr>
    <td>존</td>
    <td>44</td>
    <td>F</td>
    <td>Q</td>
    <td>V</td>
  </tr>
  <tr>
    <td>존</td>
    <td>55</td>
    <td>G</td>
    <td>R</td>
    <td>X</td>
  </tr>
  <tr>
    <td>앨리스</td>
    <td>66</td>
    <td>A</td>
    <td>N</td>
    <td>Z</td>
  </tr>
</table>

>[!NOTE]
>
>AAID = 77 및 DEL-DEVICE 레이블이 있는 행의 셀만 영향을 받습니다.

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
    <td>개인 정보 보호-0523</td>
    <td>77</td>
    <td>개인 정보 보호-1866</td>
    <td>개인 정보 보호-3681</td>
    <td>X</td>
  </tr>
  <tr>
    <td>개인 정보 보호-0523</td>
    <td>88</td>
    <td>개인 정보 보호-2178</td>
    <td>개인 정보 보호-1975</td>
    <td>Y</td>
  </tr>
  <tr>
    <td>개인 정보 보호-0523</td>
    <td>99</td>
    <td>개인 정보 보호-9045</td>
    <td>개인 정보 보호-2864</td>
    <td>Z</td>
  </tr>
  <tr>
    <td>존</td>
    <td>77</td>
    <td>D</td>
    <td>P</td>
    <td>W</td>
  </tr>
  <tr>
    <td>존</td>
    <td>88</td>
    <td>E</td>
    <td>N</td>
    <td>U</td>
  </tr>
  <tr>
    <td>존</td>
    <td>44</td>
    <td>F</td>
    <td>Q</td>
    <td>V</td>
  </tr>
  <tr>
    <td>존</td>
    <td>55</td>
    <td>G</td>
    <td>R</td>
    <td>X</td>
  </tr>
  <tr>
    <td>앨리스</td>
    <td>66</td>
    <td>A</td>
    <td>N</td>
    <td>Z</td>
  </tr>
</table>

>[!NOTE]
>
>user=Mary 및 DEL-PERSON 레이블이 있는 행의 셀만 영향을 받습니다. 또한, 실제로 A_ID를 포함하는 변수는 prop 또는 eVar이 될 수 있습니다. 해당 교체 값은 숫자 값을 임의의 다른 숫자 값으로 대체하지 않고 &quot;개인 정보 보호-&quot;로 시작하는 문자열이며, 그 뒤에는 임의의 숫자(GUID)가 옵니다.

<table>
  <tr>
    <th colspan="5" style="text-align:center">user=Mary<br>expandIDs=true</th>
  </tr>
  <tr>
    <th>MyProp1</th>
    <th>AAID</th>
    <th>MyEvar1</th>
    <th>MyEvar2</th>
    <th>MyEvar3</th>
  </tr>
  <tr>
    <td>개인 정보 보호-5782</td>
    <td>09</td>
    <td>개인 정보 보호-0859</td>
    <td>개인 정보 보호-8183</td>
    <td>개인 정보 보호-9152</td>
  </tr>
  <tr>
    <td>개인 정보 보호-5782</td>
    <td>16</td>
    <td>개인 정보 보호-6104</td>
    <td>개인 정보 보호-2911</td>
    <td>개인 정보 보호-6821</td>
  </tr>
  <tr>
    <td>개인 정보 보호-5782</td>
    <td>83</td>
    <td>개인 정보 보호-2714</td>
    <td>개인 정보 보호-0219</td>
    <td>개인 정보 보호-4395</td>
  </tr>
  <tr>
    <td>존</td>
    <td>09</td>
    <td>D</td>
    <td>개인 정보 보호-8454</td>
    <td>개인 정보 보호-8216</td>
  </tr>
  <tr>
    <td>존</td>
    <td>16</td>
    <td>E</td>
    <td>개인 정보 보호-2911</td>
    <td>개인 정보 보호-2930</td>
  </tr>
  <tr>
    <td>존</td>
    <td>44</td>
    <td>F</td>
    <td>Q</td>
    <td>V</td>
  </tr>
  <tr>
    <td>존</td>
    <td>55</td>
    <td>G</td>
    <td>R</td>
    <td>X</td>
  </tr>
  <tr>
    <td>앨리스</td>
    <td>66</td>
    <td>A</td>
    <td>N</td>
    <td>Z</td>
  </tr>
</table>

다음을 참조하십시오.

* `user=Mary` 및 `DEL-DEVICE` 또는 `DEL-PERSON` 레이블이 있는 행의 셀과 `user=Mary`가 포함된 행에서 발생한 AAID(방문자 ID)가 포함된 행에 `DEL-DEVICE` 레이블이 있는 셀이 영향을 받습니다.
* expandIDs 설정은 `user=Mary` 시 ID-DEVICE 레이블이 있는 MyEvar3에 있는 값을 포함하도록 호출로 확장되지 않습니다. expandID는 `user=Mary`이 있는 행에서 방문자 ID(이 예제의 AAID)뿐만 아니라 ECID도 포함하도록 확장됩니다.
* `MyEvar2` 네 번째 및 다섯 번째 행에는 첫 번째 행과 두 번째 행에 있는 것과 동일한 방문자 ID 값이 포함되어 있으므로 이러한 행의 가 업데이트됩니다. 따라서 ID 확장에는 장치 수준 삭제에 대한 ID 확장이 포함됩니다.
* 두 번째 행과 다섯 번째 행의 `MyEvar2` 값은 삭제 전과 후 모두 일치합니다. 그러나 삭제 후에는 마지막 행이 삭제 요청의 일부로 업데이트되지 않았기 때문에 해당 행에서 발생하는 값 N과 더 이상 일치하지 않습니다.
* `MyEvar3`는 ID 확장을 사용하지 않은 경우와 매우 다르게 작동합니다. ID 확장이 없으므로 일치하는 `ID-DEVICES`가 없습니다. 이제 `AAID`이 처음 다섯 개 행에서 일치합니다.
