---
description: 다중 통화 지원이 작동하도록 대상 통화 코드를 정의하는 방법에 대해 설명합니다.
title: 다중 통화 지원
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 63a6ca92ae5fe103648c74bd16bcdf90858c71f3

---


# 다중 통화 지원

이 문서에서는 다중 통화 지원을 위한 대상 통화 코드를 정의하는 방법에 대해 설명합니다.

타겟 통화 코드는 다음 세 가지 수준에서 정의됩니다.

## 페이지 수준

페이지 수준에서 대상 통화에 대한 JavaScript 변수를 설정할 수 있습니다. 사이트 소유자는 이 변수를 적절한 3자 ISO 4217 통화 코드(이 문서의 아래 참조)로 설정합니다. 이 [수준에서 currencyCode](https://docs.adobe.com/content/help/en/analytics/implementation/vars/config-vars/currencycode.html) 변수가 설정되지 않은 경우 기본 통화는 보고서 세트에 지정된 것과 같습니다. 페이지 수준의 변수가 보고서 세트에 지정된 변수와 충돌하는 경우 보고서 세트의 변수가 우선합니다.


## 보고서 세트 수준

보고서 세트를 **만들 때 기본 통화가** 지정됩니다 [](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/new-report-suite/new-report-suite.html). 이것은 통화에 대한 기본 설정이며 페이지 수준에서 설정된 통화 코드보다 우선합니다. 따라서 보고서 세트에 미국 달러, 유로 및 영국 파운드를 수락하는 주문이 있고 보고서 세트에 기본 통화 코드가 &quot;미국 달러&quot;로 설정된 경우, 보고 백엔드 데이터베이스는 모든 거래를 미국 달러로 변환합니다.

마케팅 보고서는 이미지 요청 발생 시 환율을 사용하여 페이지 수준 통화 값을 기본 보고서 세트 통화 값으로 변환합니다. 보고서 세트는 &quot;미국 달러&quot;를 기본 통화로 사용합니다.


## 보고서 수준

사용자는 사용자 로그인 세션에 대해 보고된 기본 통화를 설정할 수 있습니다. 여기에는 전환 보고서에서 **표시 옵션** 링크를 통해 액세스할 수 있습니다. 마케팅 보고서는 보고서 실행 시 환율을 사용하여 보고서 세트 통화 값을 보고서 지정 통화 값으로 변환합니다.

## 지원되는 통화 코드(ISO 4217)

Analytics는 현재 전환 트랜잭션에 대해 다음 통화 형식을 지원합니다.


&#39;AFA&#39; 아프가니스탄 아프가니 (AFA)

&#39;AFN&#39; 아프가니스탄 아프가니 (AFN)

&#39;ALL&#39; 알바니아 레케(ALL)

&#39;DZD&#39; 알제리 디나르(DZD)

&#39;AOA&#39; 앙골라 크완자(AOA)

&#39;ARS&#39; 아르헨티나 페소 (ARS)

&#39;AMD&#39; 아르메니아 드램(AMD)

&#39;AWG&#39; 아루바 길더(AWG)

&#39;AUD&#39; 오스트레일리아 달러 (AUD)

&#39;AZM&#39; 아제르바이잔 마나트(AZM)

&#39;AZN&#39; 아제르바이잔 뉴 마나트(AZN)

&#39;BSD&#39; 바하마 달러(BSD)

&#39;BHD&#39; 바레인 디나르(BHD)

&#39;BDT&#39; 방글라데시 타카 (BDT)

&#39;BBD&#39; 바베이도스 달러(BBD)

&#39;BYR&#39; 벨라루스 루블 (BYR)

&#39;BZD&#39; 벨리즈 달러(BZD)

&#39;BMD&#39; 버뮤다 달러(BMD)

&#39;BTN&#39; 부탄 굴트럼(BTN)

&#39;BOB&#39; 볼리비아 볼리비아노 (BOB)

&#39;BAM&#39; 보스니아 헤르체고비나 태환 마르카 (BAM)

&#39;BWP&#39; 보츠와나 풀라스(BWP)

&#39;BRL&#39; 브라질 리알(BRL)

&#39;BND&#39; 브루나이 달러 (BND)

&#39;BGN&#39; 불가리아 레바(BGN)

&#39;BIF&#39; 부룬디 프랑 (BIF)

&#39;KHR&#39; 캄보디아 리엘(KHR)

&#39;CAD&#39; 캐나다 달러(CAD)

&#39;CVE&#39; Cape Verde Escudos(CVE)

&#39;KYD&#39; 케이맨 제도 달러(KYD)

&#39;CLP&#39; 칠레 페소 (CLP)

&#39;CNY&#39; 중국 위안 인민폐 (CNY)

&#39;COP&#39; 콜롬비아 페소 (COP)

&#39;XOF&#39; Communauté Financière Africaine Francs BCEAO (XOF)

&#39;XAF&#39; Communauté Financière Africaine Francs BEAC(XAF)

&#39;KMF&#39; 코모로스 프랑 (KMF)

&#39;XPF&#39; Comptoirs Français du Pacifique Francs (XPF)

&#39;CDF&#39; Congo/Kinshasa Francs (CDF)

&#39;CRC&#39; 코스타리카 콜론(CRC)

&#39;HRK&#39; 크로아티아 쿠나(HRK)

&#39;CUC&#39; 쿠바 태환 페소 (CUC)

&#39;CUP&#39; 쿠바 페소 (CUP)

&#39;CYP&#39; 키프로스 파운드(CYP)

&#39;CZK&#39; 체코 공화국 코루니(CZK)

&#39;DKK&#39; 덴마크 크로너(DKK)

&#39;DJF&#39; 지부티 프랑 (DJF)

&#39;DOP&#39; 도미니카 공화국 페소 (DOP)

&#39;XCD&#39; 동카리브 달러(XCD)

&#39;EGP&#39; 이집트 파운드(EGP)

&#39;SVC&#39; 엘살바도르 콜론(SVC)

&#39;ERN&#39; 에리트레아 낙파(ERN)

&#39;XBT&#39; 오류(XBT)

&#39;EEK&#39; 에스토니아 크루니(EEK)

&#39;ETB&#39; ETB(에티오피아 Birr)

&#39;EUR&#39; 유로(EUR)

&#39;FKP&#39; 포클랜드 제도 파운드(FKP)

&#39;FJD&#39; 피지 달러(FJD)

&#39;GMD&#39; 감비아 달라시(GMD)

&#39;GEL&#39; Georgia Lari (GEL)

&#39;GHC&#39; 가나 시디스(GHC)

&#39;GHS&#39; 가나 시디스(GHS)

&#39;GIP&#39; 지브롤터 파운드(GIP)

&#39;XAU&#39; 금 온스(XAU)

&#39;GTQ&#39; Guatemala Quetsales (GTQ)

&#39;GGP&#39; 건지 파운드(GGP)

&#39;GNF&#39; 기니 프랑 (GNF)

&#39;GYD&#39; 가이아나 달러(GYD)

&#39;HTG&#39; 아이티 고르데스(HTG)

&#39;HNL&#39; 온두라스 렘피라스(HNL)

&#39;HKD&#39; 홍콩 달러(HKD)

&#39;HUF&#39; 헝가리 포린트(HUF)

&#39;ISK&#39; 아이슬랜드 크로누(ISK)

&#39;INR&#39; 인도 루페 (INR)

&#39;IDR&#39; 인도네시아 루피아(IDR)

&#39;XDR&#39; 국제 통화 기금 특별 인출권(XDR)

&#39;IRR&#39; 이란 리알(IRR)

&#39;IQD&#39; 이라크 디나르 (IQD)

맨섬 파운드(IMP)

&#39;ILS&#39; 이스라엘 뉴 셰켈 (ILS)

&#39;JMD&#39; 자메이카 달러(JMD)

&#39;JPY&#39; 일본 엔 (JPY)

&#39;JEP&#39; 저지 파운드(JEP)

&#39;JOD&#39; 요르단 디나르(JOD)

&#39;KZT&#39; 카자흐스탄 텐지 (KZT)

&#39;KES&#39; 케냐 실링(KES)

&#39;KWD&#39; 쿠웨이트 디나르(KWD)

&#39;KGS&#39; 키르기스스탄 홈즈(KGS)

&#39;LAK&#39; 라오스 키프(LAK)

&#39;LVL&#39; 라트비아 라티(LVL)

&#39;LBP&#39; 레바논 파운드(LBP)

&#39;LSL&#39; 레소토 말로티(LSL)

&#39;LRD&#39; 라이베리아 달러(LRD)

&#39;LYD&#39; 리비아 디나르(LYD)

&#39;LTL&#39; 리투아니아 리타이(LTL)

&#39;MOP&#39; 마카오 파타카 (MOP)

&#39;MKD&#39; 마케도니아 디나르(MKD)

&#39;MGA&#39; 마다가스카르 아리아리(MGA)

&#39;MWK&#39; 말라위 콰쳐 (MWK)

&#39;MYR&#39; Malaysia Ring (MYR)

&#39;MVR&#39; 몰디브 루피아(MVR)

&#39;MTL&#39; 몰타 리리(MTL)

&#39;MRO&#39; 모리타니아 오우기야(MRO)

&#39;MUR&#39; 모리셔스 루페 (MUR)

&#39;MXN&#39; 멕시코 페소 (MXN)

&#39;MDL&#39; 몰도바 레이(MDL)

&#39;MNT&#39; 몽골 투그릭(MNT)

&#39;MAD&#39; 모로코 디르함 (MAD)

&#39;MZN&#39; 모잠비크 메티카시(MZN)

&#39;MZM&#39; 모잠비크 메티카시(MZM)

&#39;MMK&#39; 미얀마 키아츠(MMK)

&#39;NAD&#39; 나미비아 달러(NAD)

&#39;NPR&#39; 네팔 루페 (NPR)

&#39;ANG&#39; 네덜란드령 앤틸리스 길더(ANG)

&#39;NZD&#39; 뉴질랜드 달러(NZD)

&#39;NIO&#39; 니카라과 코르도바 (NIO)

&#39;NGN&#39; 나이지리아 나이라(NGN)

KPW 북한 원 (KPW)

&#39;NOK&#39; 노르웨이 크로너(NOK)

&#39;OMR&#39; 오만 리알(OMR)

&#39;PKR&#39; 파키스탄 루페 (PKR)

&#39;XPD&#39; Palladium O온스 (XPD)

&#39;PAB&#39; Panama Balboas (PAB)

&#39;PGK&#39; 파푸아뉴기니 키나(PGK)

&#39;PYG&#39; 파라과이 과라니(PYG)

&#39;PEN&#39; 페루 누에보 솔레스(PEN)

&#39;PHP&#39; 필리핀 페소(PHP)

&#39;XPT&#39; 플래티넘 온스(XPT)

&#39;PLN&#39; 폴란드 즐로티(PLN)

&#39;QAR&#39; 카타르 리얄(QAR)

&#39;ROL&#39; 루마니아 레이 (ROL)

&#39;RON&#39; 루마니아 뉴 레이 (RON)

&#39;RUB&#39; 러시아 루블 (RUB)

&#39;RUR&#39; 러시아 루블 (RUR)

&#39;RWF&#39; 르완다 프랑 (RWF)

&#39;SHP&#39; 세인트헬레나 파운드(SHP)

&#39;WST&#39; 사모아 탈라(WST)

&#39;STD&#39; 상투메프린시페 도브라스(STD)

&#39;SAR 파섹&#39; 사우디아라비아 리얄(SAR 파섹)

&#39;SPL&#39; Seborga Luigini(SPL)

&#39;RSD&#39; 세르비아 디나르(RSD)

&#39;CSD&#39; 세르비아 디나르(CSD)

&#39;SCR&#39; 세이셸 루페 (SCR)

&#39;SLL&#39; 시에라리온 레오네(SLL)

&#39;XAG&#39; 은화(XAG)

&#39;SGD&#39; 싱가포르 달러(SGD)

&#39;SKK&#39; 슬로바키아 코루니(SKK)

&#39;SIT&#39; 슬로베니아 톨라스 (SIT)

&#39;SBD&#39; 솔로몬 제도 달러 (SBD)

&#39;SOS&#39; 소말리아 실링(SOS)

ZAR&#39; 남아프리카 랜드 (ZAR 파섹

한국 원(KRW)

&#39;LKR&#39; 스리랑카 루페 (LKR)

&#39;SDD&#39; 수단 디나르(SDD)

&#39;SDG&#39; 수단 파운드(SDG)

&#39;SRD&#39; 수리남 달러(SRD)

&#39;SRG&#39; 수리남 길더(SRG)

&#39;SZL&#39; 스와질란드 에말랑게니(SZL)

&#39;SEK&#39; 스웨덴 크로노(SEK)

&#39;CHF&#39; 스위스 프랑 (CHF)

&#39;SYP&#39; 시리아 파운드(SYP)

&#39;TWD&#39; 대만 뉴 달러(TWD)

&#39;TJS&#39; 타지키스탄 소모니(TJS)

TZS&#39; 탄자니아 실링(TZS)

&#39;THB&#39; 태국 바트 (THB)

&#39;TOP&#39; 통가 파안가(TOP)

&#39;TTD&#39; 트리니다드 토바고 달러(TTD)

&#39;TND&#39; 튀니지 디나르(TND)

&#39;TRY&#39; 터키 리라(TRY)

&#39;TRL&#39; 터키 리라(TRL)

&#39;TMM&#39; 투르크메니스탄 마나트(TMM)

&#39;TMT&#39; 투르크메니스탄 뉴 마나트(TMT)

&#39;TVD&#39; 투발루 달러(TVD)

&#39;UGX&#39; 우간다 실링(UGX)

&#39;UAH&#39; 우크라이나 그리브니아(UAH)

&#39;AED&#39; 아랍에미리트 연합국 디르함(AED)

&#39;GBP&#39; 영국 파운드(GBP)

&#39;USD&#39;가 선택된 미국 달러(USD)

&#39;유유&#39; 우루과이 페소 (UYU)

&#39;UZS&#39; 우즈베키스탄 합계(UZS)

&#39;VUV&#39; 바누아투 바투(VUV)

&#39;VEB&#39; 베네수엘라 볼리바르(VEB)

&#39;VEF&#39; 베네수엘라 볼리바르 푸에르테(VEF)

&#39;VND&#39; 베트남 동(VND)

&#39;YER&#39; 예멘 리알(YER)

&#39;ZMK&#39; 잠비아 콰차 (ZMK)

&#39;ZMW&#39; 잠비아 콰차 (ZMW)

&#39;ZWD&#39; 짐바브웨 달러 (ZWD)


## AppMeasurement.js 예

이 `currencyCode` 변수는 AppMeasurement.js 파일에서 전역적으로 정의할 수 있습니다. 이 파일에서 currencyCode 변수를 정의하면 모든 통화 거래에 동일한 통화 코드가 사용됩니다. 아래 예제는 AppMeasurement.js 파일의 `currencyCode` 변수로 유로를 `CONFIG SECTION` 지정합니다. 모든 구매 이벤트는 &quot;유로&quot; 거래로 보고하여 해석됩니다.

```
/************************** CONFIG SECTION **************************/ 
/* You may add or alter any code config here. */ 
s.account="devnow"
s.currencyCode="EUR"
s.trackInlineStats=true 
s.linkLeaveQueryString=false 
s.linkTrackVars="None" 
s.linkTrackEvents="None" 
***
    
```

AppMeasurement.js 파일 편집에 대한 자세한 내용은 [AppMeasurement.js 파일에](https://docs.adobe.com/content/help/en/analytics/implementation/implement-analytics-with-dtm/analytics-tool/t-appmeasurement-code.html)코드 삽입을 참조하십시오.

## 추가 구현 참고 사항

* 페이지 간에 통화 코드가 변경될 수 있지만, 지정된 페이지 요청에 정의된 모든 전환 라인 항목은 동일한 통화를 사용해야 합니다(예: 동일한 페이지 뷰에서 유로, 영국 파운드 및 미국 달러를 정의할 수 없음). 통화 변환을 하지 않으려면 currencyCode 값을 비워 두어야 합니다. 이렇게 하면 전송된 값이 전환 없이 보고서로 직접 전달됩니다.

* 잘못된 currencyCode(지원되는 통화 코드 목록에 없는 모든 값)를 설정하면 전체 히트가 제외되고 해당 트랜잭션에 대해 데이터가 수집되지 않습니다. 프로덕션에서 설정하기 `currencyCode` 전에 테스트 보고서 세트를 사용하여 데이터가 수집되고 통화 변환이 올바른지 확인하십시오.

* 마침표(.)를 구분 문자로 사용하지 않는 통화는 일반적인 구분 문자 대신 마침표를 사용하도록 수정해야 합니다. 예를 들어 쉼표(,)를 사용하는 스웨덴 크로노는 쉼표 대신 마침표를 사용하도록 수정되어야 합니다. Analytics는 쉼표를 사용하여 값을 구분하며 데이터가 올바르게 전달되지 않습니다. 마침표는 값을 보고서에 올바로 전달합니다.
