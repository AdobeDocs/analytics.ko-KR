---
title: currencyCode 변수는 무엇이며 어떻게 사용할 수 있습니까?
description: 전자 상거래 사이트의 경우 페이지에서 취급하는 통화를 설정합니다.
feature: Variables
exl-id: 3332c366-c472-4778-96c8-ef0aa756cca8
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '862'
ht-degree: 93%

---

# currencyCode

상거래를 사용하는 사이트의 경우 매출 및 통화는 Analytics의 중요한 부분입니다. 많은 사이트, 특히 여러 국가를 아우르는 사이트는 다양한 통화를 사용합니다. 매출 기여도 분석이 올바른 통화로 표시되게 하려면 `currencyCode` 변수를 사용하십시오.

`currencyCode`가 정의되지 않으면 [`products`](../page-vars/products.md) 변수로 정의된 통화 값과 통화 이벤트가 보고서 세트의 통화와 동일한 것처럼 처리됩니다. 보고서 세트의 통화를 확인하려면 관리자 안내서에서 [일반 계정 설정](/help/admin/admin/general-acct-settings-admin.md)을 참조하십시오.

`currencyCode`가 정의되어 있고 보고서 세트의 통화와 일치하는 경우 통화 전환이 적용되지 않습니다.

`currencyCode`가 정의되어 있고 보고서 세트의 통화와 다른 경우에는 Adobe가 현재 날짜의 환율을 기준으로 통화 변환을 적용합니다. Adobe는 [XE](https://xe.com)와 협력하여 매일 통화를 변환합니다. 데이터 수집 서버에 저장된 모든 값은 궁극적으로 보고서 세트의 통화로 저장됩니다.

>[!WARNING]
>
>`currencyCode`에 잘못된 값이 포함되어 있으면 전체 히트가 삭제되어 데이터 손실이 발생합니다. 구현에서 이 변수를 사용하는 경우 이 변수가 올바르게 정의되어 있는지 확인하십시오.

이 변수는 히트 간에 지속되지 않습니다. 이 변수가 매출 또는 통화 이벤트를 포함하는 모든 페이지에서 정의되었는지 확인하십시오.

## 웹 SDK를 사용한 통화 코드

통화 코드는 다음과 같습니다 [Adobe Analytics용 매핑](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) XDM 필드 아래 `commerce.order.currencyCode`.

## Adobe Analytics 확장을 사용한 통화 코드

통화 코드는 Adobe Analytics 확장을 구성할 때 [!UICONTROL 일반] 아코디언 아래의 필드입니다.

1. 에 로그인합니다. [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection) adobeID 자격 증명 사용.
1. 원하는 태그 속성을 클릭합니다.
1. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 **[!UICONTROL 구성]** 버튼을 클릭합니다.
1. [!UICONTROL 일반] 아코디언을 확장합니다. 그러면 [!UICONTROL 통화 코드] 필드가 표시됩니다.

사전 설정된 통화 코드나 사용자 지정 통화 코드를 사용할 수 있습니다. 사용자 지정 통화 코드를 사용하는 경우 코드가 유효한지 확인하십시오.

## Adobe Experience Platform Mobile SDK의 통화 코드

통화 코드는 Adobe Analytics 확장의 컨텍스트 데이터 변수를 통해 Adobe Experience Platform Mobile SDK에 전달됩니다.

1. `trackState` 또는 `trackAction` 동안 컨텍스트 데이터 변수에 통화 코드를 설정합니다.
1. 보고서 세트에 대한 Adobe Analytics Admin Console에서 처리 규칙을 만듭니다. 통화 코드 변수를 덮어쓰는 규칙을 설정합니다.
1. 통화 코드를 `trackState` 또는 `trackAction` 호출에서 `products` 변수에 전달합니다.

사전 설정된 통화 코드나 사용자 지정 통화 코드를 사용할 수 있습니다. 사용자 지정 통화 코드를 사용하는 경우 코드가 유효한지 확인하십시오.

## AppMeasurement 및 Analytics 확장 사용자 지정 코드 편집기의 s.currencyCode

`s.currencyCode` 변수는 페이지의 통화를 나타내는 3자로 된 대문자 코드를 포함하는 문자열입니다.

```js
s.currencyCode = "USD";
```

다음 통화 코드가 유효합니다.

| 통화 코드 | 통화 설명 |
| --- | --- |
| `AED` | 아랍에미리트 연합국 디르함 |
| `AFA` | 아프카니스탄 아프가니 |
| `ALL` | 알바니아 레케 |
| `AMD` | 아르메니아 드램 |
| `ANG` | 네덜란드령 앤틸리스 길더 |
| `AOA` | 앙골라 크완자 |
| `ARS` | 아르헨티나 페소 |
| `AUD` | 오스트레일리아 달러 |
| `AWG` | 아루바 길더 |
| `AZM` | 아제르바이잔 마나트 |
| `BAM` | 보스니아 헤르체코비나 태환 마르크 |
| `BBD` | 바베이도스 달러 |
| `BDT` | 방글라데시 타카 |
| `BGN` | 불가리아 레바 |
| `BHD` | 바레인 디나르 |
| `BIF` | 부룬디 프랑 |
| `BMD` | 버뮤다 달러 |
| `BND` | 브루나이 달러 |
| `BOB` | 볼리비아 볼리비아노스 |
| `BRL` | 브라질 리알 |
| `BSD` | 바하마 달러 |
| `BTN` | 부탄 눌트눔 |
| `BWP` | 보츠와나 풀라스 |
| `BYR` | 벨라루스 루블 |
| `BZD` | 벨리즈 달러 |
| `CAD` | 캐나다 달러 |
| `CDF` | 콩고/킨샤사 프랑 |
| `CHF` | 스위스 프랑 |
| `CLP` | 칠레 페소 |
| `CNY` | 중국 위안 인민폐 |
| `COP` | 콜롬비아 페소 |
| `CRC` | 코스타리카 콜론 |
| `CSD` | 세르비아 디나르 |
| `CUP` | 쿠바 페소 |
| `CVE` | 케이프베르데 에스쿠도 |
| `CYP` | 시프러스 파운드 |
| `CZK` | 체코 코루니 |
| `DJF` | 지부티 프랑 |
| `DKK` | 덴마크 크로너 |
| `DOP` | 도미니카 공화국 페소 |
| `DZD` | 알제리 디나르 |
| `EEK` | 에스토니아 크루니 |
| `EGP` | 이집트 파운드 |
| `ERN` | 에리트레아 낙파 |
| `ETB` | 에디오피아 비르 |
| `EUR` | 유로 |
| `FJD` | 피지 달러 |
| `FKP` | 포클랜드 제도 파운드 |
| `GBP` | 영국 파운드 |
| `GEL` | 조지아 라리 |
| `GGP` | 건지 파운드 |
| `GHC` | 가나 세디스 |
| `GIP` | 지브롤터 파운드 |
| `GMD` | 잠비아 달라시 |
| `GNF` | 기니아 프랑 |
| `GTQ` | 과테말라 쿼잘레 |
| `GYD` | 가이아나 달러 |
| `HKD` | 홍콩 달러 |
| `HNL` | 온두라스 렘피라스 |
| `HRK` | 크로아티아 쿠나 |
| `HTG` | 아이티 고르데스 |
| `HUF` | 헝가리 포린트 |
| `IDR` | 인도네시아 루피아 |
| `ILS` | 이스라엘 뉴 셰켈 |
| `IMP` | 맨섬 파운드 |
| `INR` | 인도 루페 |
| `IQD` | 이라크 디나르 |
| `IRR` | 이란 리알 |
| `ISK` | 아이슬랜드 크로누 |
| `JEP` | 저지 파운드 |
| `JMD` | 자메이카 달러 |
| `JOD` | 요르단 디나르 |
| `JPY` | 일본 엔 |
| `KES` | 케냐 실링 |
| `KGS` | 키르기스탄 솜 |
| `KHR` | 캄보디아 리엘 |
| `KMF` | 코모로스 프랑 |
| `KPW` | 북한 원 |
| `KRW` | 한국 원 |
| `KWD` | 쿠웨이트 디나르 |
| `KYD` | 케이맨 제도 달러 |
| `KZT` | 카자흐스탄 텐게 |
| `LAK` | 라오스 키프 |
| `LBP` | 레바논 파운드 |
| `LKR` | 스리랑카 루페 |
| `LRD` | 라이베리아 달러 |
| `LSL` | 레소토 말로티 |
| `LTL` | 리투아니아 리타이 |
| `LVL` | 라트비아 라티 |
| `LYD` | 리비아 디나르 |
| `MAD` | 모로코 디르함 |
| `MDL` | 몰도바 레이 |
| `MGA` | 마다가스카르 아리아리 |
| `MKD` | 마케도니아 디나르 |
| `MMK` | 미얀마 키아츠 |
| `MNT` | 몽골 터그리크 |
| `MOP` | 마카오 파타카 |
| `MRO` | 모리타니아 오우기야 |
| `MTL` | 몰타 리리 |
| `MUR` | 모리셔스 루페 |
| `MVR` | 몰디브 루피아 |
| `MWK` | 말라위 콰차 |
| `MXN` | 멕시코 페소 |
| `MYR` | 말레이시아 링깃 |
| `MZM` | 모잠비크 메티카시 |
| `NAD` | 나미비아 달러 |
| `NGN` | 나이지리아 나이라 |
| `NIO` | 니카라과 골드 코르도바 |
| `NOK` | 노르웨이 크로너 |
| `NPR` | 네팔 루페 |
| `NZD` | 뉴질랜드 달러 |
| `OMR` | 오만 리알 |
| `PAB` | 파나마 발보아 |
| `PEN` | 페루 누에보 솔레스 |
| `PGK` | 파푸아뉴기니 키나 |
| `PHP` | 필리핀 페소 |
| `PKR` | 파키스탄 루페 |
| `PLN` | 폴란드 즐로티 |
| `PYG` | 파라과이 과라니 |
| `QAR` | 카타르 리알 |
| `ROL` | 루마니아 레이 |
| `RUR` | 러시아 루블 |
| `RWF` | 르완다 프랑 |
| `SAR` | 사우디아라비아 리알 |
| `SBD` | 솔로몬 제도 달러 |
| `SCR` | 세이셸 루페 |
| `SDD` | 수단 디나르 |
| `SEK` | 스웨덴 크로노 |
| `SGD` | 싱가폴 달러 |
| `SHP` | 세인트헬레나 파운드 |
| `SIT` | 슬로베니아 톨라르 |
| `SKK` | 슬로바키아 로루니 |
| `SLL` | 시에라리온 레오네 |
| `SOS` | 소말리아 실링 |
| `SPL` | 세보르가 루이기니 |
| `SRD` | 수리남 달러 |
| `SRG` | 수리남 길더 |
| `STD` | 상투메프린시페 도브라스 |
| `SVC` | 엘살바도르 콜론 |
| `SYP` | 시리아 파운드 |
| `SZL` | 스와질란드 에말란게니 |
| `THB` | 타이 바트 |
| `TJS` | 타지키스탄 소모니 |
| `TMM` | 투르크메니스탄 마나트 |
| `TND` | 튀니지 디나르 |
| `TOP` | 통가 파안가 |
| `TRL` | 터키 리라 |
| `TTD` | 트리니다드 토바고 달러 |
| `TVD` | 투발루 달러 |
| `TWD` | 대만 뉴 달러 |
| `TZS` | 탄자니아 실링 |
| `UAH` | 우크라이나 그리브니아 |
| `UGX` | 우간다 실링 |
| `USD` | 미국 달러 |
| `UYU` | 우루과이 페소 |
| `UZS` | 우즈베키스탄 솜 |
| `VEB` | 베네수엘라 볼리바레 |
| `VND` | 베트남 동 |
| `VUV` | 바누아투 바투 |
| `WST` | 사모아 탈라 |
| `XAF` | Communauté Financière Africaine Francs B |
| `XAG` | 은 (온스) |
| `XAU` | 금 (온스) |
| `XCD` | 동캐리비안 달러 |
| `XDR` | 국제 통화 기금의 특별 인출 |
| `XOF` | Communauté Financière Africaine Francs B |
| `XPD` | 팔라듐 (온) |
| `XPF` | CFP 프랑 |
| `XPT` | 백금 (온스) |
| `YER` | 예멘 리알 |
| `ZAR` | 남아프리카 랜드 |
| `ZMK` | 잠비아 콰차 |
| `ZWD` | 짐바브웨 달러 |
