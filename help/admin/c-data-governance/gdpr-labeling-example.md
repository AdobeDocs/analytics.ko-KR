---
description: 'null'
seo-description: 'null'
seo-title: 레이블 지정 예
title: 레이블 지정 예
uuid: A 9 A 5 B 937-DBDE -4 F 0 F-A 171-005 EF 4 C 79 DF 9
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 레이블 지정 예

## 샘플 히트 데이터 {#section_94DE6BC0026F46D7AD7061C5625C8D52}

다음 히트 데이터가 있다고 가정합니다.

* 첫 번째 행에는 각 변수의 레이블이 포함됩니다.
* 두 번째 행은 변수의 이름입니다. ID 레이블이 있는 경우에는 괄호 안에 지정된 네임스페이스가 포함됩니다.
* 히트 데이터는 세 번째 행에서 시작됩니다.

<!-- Meike, I converted html tables for fix elusive validation error. Bob -->

| 레이블 | I2<br>id-persondel<br>-personacc<br>-person | I2<br>ID-DEVICE<br>DEL-DEVICE<br>ACC-ALL | I2<br>DEL-PERSON<br>ACC-PERSON | I2<br>DEL-DEVICE<br>DEL-PERSON<br>ACC-ALL | I2<br>ID-DEVICE<br>DEL-DEVICE<br>ACC-ALL |
|:---:|:---:|:---:|:---:|:---:|:---:|
| Variable Name<br>(Namespace) | MyProp1<br>(user) | Visitor ID<br>(AAID) | MyEvar1 | MyEvar2 | MyEvar3<br>(xyz) |
| 히트 데이터 | Mary | 77 | A | M | X |
| Mary | 88 | B | N | Y |
| Mary | 99 | C | O | Z |
| John | 77 | D | P | W |
| John | 88 | E | N | U |
| John | 44 | F | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | Z |


## 샘플 액세스 요청 {#section_BDA817FD2415420DAAC835825484BA9D}

액세스 요청을 제출하면 요약 파일에 아래 표에 표시된 값이 포함됩니다. 요청은 장치 파일만 반환하거나 개인 파일만 반환할 수 있습니다(즉, 각각에 대해 하나). 개인 ID가 사용되고 expandIds가 true인 경우에만 두 개의 요약 파일이 반환됩니다.

| API 값 | 반환된 파일 유형 | 요약 액세스 파일의 데이터 |
|--- |--- |--- |
| 네임스페이스/ID | expandIDs |  | MyProp1 | 방문자 ID | MyEvar1 | MyEvar2 | MyEvar3 |
| AAID=77 | false | 장치 | 변수 없음 | 77 | 변수 없음 | M, P | X, W |
| AAID=77 | true | 장치 | 77 | M, P | X, W |
| user=Mary | false | 사람 | Mary | 77, 88, 99 | A, B, C | M, N, O | X, Y, Z |
| user=Mary | true | 사람 | Mary | 77, 88, 99 | A, B, C | M, N, O | X, Y, Z |
| 장치 | 없음 | 77, 88 | 없음 | N, P | U, W |
| user=Mary AAID=66 | true | 사람 | Mary | 77, 88, 99 | A, B, C | M, N, O | X, Y, Z |
| 장치 | 없음 | 66, 77, 88 | 없음 | N, P | U, W, Z |
| xyz=X | false | 장치 | 없음 | 55, 77 | 없음 | M, R | X |
| xyz=X | true | 장치 | 없음 | 55, 77 | 없음 | M, P, R | W, X |

expandIDs에 대한 설정은 쿠키 ID를 사용할 때 출력에 영향을 미치지 않습니다.

## 샘플 삭제 요청 {#section_6C75F70F5D574BE7AA540981E8B7EA26}

삭제 요청에 표의 첫 번째 행에 있는 API 값을 사용하면 히트 표가 다음과 비슷하게 업데이트됩니다.

| aaid = 77 expandids 값은 문제가 되지 않습니다. |
|--- |
| MyProp1 | AAID | MyEvar1 | MyEvar2 | MyEvar3 |
| Mary | 42 | A | GDPR-7398 | GDPR-9152 |
| Mary | 88 | B | N | Y |
| Mary | 99 | C | O | Z |
| John | 42 | D | GDPR-1866 | GDPR-8216 |
| John | 88 | E | N | U |
| John | 44 | F | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | W |

>[!NOTE]
>
>AAID = 77 및 DEL-DEVICE 레이블이 있는 행의 셀만 영향을 받습니다.

| user = Mary expandids = false |
|--- |
| MyProp1 | AAID | MyEvar1 | MyEvar2 | MyEvar3 |
| GDPR-0523 | 77 | GDPR-1866 | GDPR-3681 | X |
| GDPR-0523 | 88 | GDPR-2178 | GDPR-1975 | Y |
| GDPR-0523 | 99 | GDPR-9045 | GDPR-2864 | Z |
| John | 77 | D | P | W |
| John | 88 | E | N | U |
| John | 44 | F | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | W |

>[!NOTE]
>
>user=Mary 및 DEL-PERSON 레이블이 있는 행의 셀만 영향을 받습니다. 또한 연습에서 A_ID를 포함하는 변수는 prop 또는 eVar이고 해당 교체 값은 "GDPR-"로 시작하는 문자열이며, 그 뒤에는 숫자 값을 임의의 다른 숫자 값으로 대체하지 않고 임의의 숫자(GUID)가 옵니다.

| user=Mary expandIDs=true |
|--- |
| MyProp1 | AAID | MyEvar1 | MyEvar2 | MyEvar3 |
| GDPR-5782 | 09 | GDPR-0859 | GDPR-8183 | GDPR-9152 |
| GDPR-5782 | 16 | GDPR-6104 | GDPR-2911 | GDPR-6821 |
| GDPR-5782 | 83 | GDPR-2714 | GDPR-0219 | GDPR-4395 |
| John | 09 | D | GDPR-8454 | GDPR-8216 |
| John | 16 | E | GDPR-2911 | GDPR-2930 |
| John | 44 | F | Q | V |
| John | 55 | G | R | X |
| Alice | 66 | A | N | W |

다음을 참고하십시오.

* user=Mary 및 DEL-DEVICE 또는 DEL-PERSON 레이블이 포함된 행의 셀과 user=Mary가 포함된 행에서 발생한 방문자 ID를 포함하는 행에 DEL-DEVICE 레이블이 있는 셀이 영향을 받습니다.
* 네 번째 및 다섯 번째 행에는 첫 번째 행과 두 번째 행에 있는 것과 동일한 방문자 ID 값이 포함되어 있으므로 이러한 행의 MyEvar2가 업데이트됩니다. 따라서 ID 확장에는 장치 수준의 삭제에 대한 값이 포함됩니다.
* 두 번째 행과 다섯 번째 행의 MyEvar2 값은 삭제 전과 후 모두 일치하지만, 삭제 후에는 마지막 행이 삭제 요청의 일부로 업데이트되지 않았기 때문에 해당 행에서 발생하는 값 N과 더 이상 일치하지 않습니다.
* MyEvar3은 ID 확장을 사용하지 않은 경우와 매우 다르게 작동합니다. ID 확장이 없으므로 일치하는 ID-DEVICES가 없습니다. 이제 AAID가 처음 다섯 개 행에서 일치합니다.
