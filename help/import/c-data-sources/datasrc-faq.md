---
description: 이 항목에서는 일반적인 질문에 대한 답변을 제공합니다.
subtopic: Data sources
title: Data Sources FAQ
topic-fix: Developer and implementation
feature: Data Sources
exl-id: 2a5d38fe-5c5b-4275-bc44-e9cb02ec2f5d
source-git-commit: 79294cfc6f86e5a41a39504099cd730f53668725
workflow-type: ht
source-wordcount: '1496'
ht-degree: 100%

---

# Data Sources FAQ

이 항목에서는 일반적인 질문에 대한 답변을 제공합니다.

## 오프라인 데이터를 온라인 이벤트에 연결하려면 어떻게 합니까? {#offline}

오프라인 데이터를 온라인 이벤트와 연결하기 위한 거래 ID 데이터 소스의 경우 거래 ID 레코딩을 사용해야 합니다. 자세한 내용은 [거래 ID 기록](/help/import/c-data-sources/datasrc-integrating-offline-data.md#section_30D6D47AEC0F4A36B87EBFE4C858F20C)을 참조하십시오.

## 데이터 소스 기능을 사용하려면 비용이 얼마나 듭니까? {#cost}

데이터 소스는 표준 서버 호출에 대해 추가 요금을 부과하지 않습니다. 서버 호출 요금은 개별 히트가 데이터의 행으로 전송되는 전체 처리 데이터 소스 유형에만 적용됩니다. 트래픽 및 합계 수준 데이터 소스는 추가 비용을 내지 않아도 됩니다.

## 데이터 소스 파일에 주석을 추가하려면 어떻게 합니까? {#comments}

데이터 소스 파일에서 파운드 기호 (#)로 시작하는 각 행은 주석으로 취급됩니다.

## 스프레드시트 데이터에 날짜 열을 포함시켜야 합니까? {#date}

예. 다수의 마케팅 보고서는 날짜 열에서 입력되므로 데이터 소스에는 날짜 열이 필요합니다.

## 이미 사용 중인 기존 변수에 데이터를 저장할 수 있습니까? {#variables}

데이터 소스를 사용하여 데이터를 가져오려면 새로운 미사용 변수를 선택하는 것이 좋습니다. 데이터 파일의 구성에 대해 잘 모르거나 변수 재사용에 따르는 위험을 더욱 잘 이해하려면 고객 지원 센터에 문의하십시오.

## 데이터 소스를 사용하여 가져온 데이터를 삭제할 수 있습니까? {#imported}

아니요. 데이터 소스를 사용하여 보고서로 업로드한 데이터는 가져온 후에는 Adobe 기술자도 삭제할 수 없습니다. 이것은 기존 데이터에 영구적으로 삽입되어 JavaScript, ActionSource, 데이터 삽입 API 등의 기존 데이터 수집 수단을 통해 입력한 데이터와 구별할 수 없게 됩니다. 따라서 생산 환경에 업로드하기 전에 데이터 소스 데이터를 테스트 보고서 세트에 업로드할 것을 적극 권장합니다.

## 한 번에 가져올 수 있는 데이터 양은 어느 정도입니까? {#amount}

크기가 50MB를 초과하는 경우 처리가 일시 중지되며 총 크기가 50MB 아래로 떨어져야 다시 시작됩니다. 보고서 생성에서의 시간 지연을 제한하려면 하루에 90일 분량이 넘는 데이터를 업로드하지 마십시오.

## 데이터 소스를 통해 데이터를 가져오면 기존 데이터가 덮어쓰기됩니까? {#overwrite}

데이터 소스의 데이터는 절대로 기존 보고서 데이터를 덮어쓰지 않습니다. 대신 데이터 소스를 사용하여 업로드한 데이터는 기존 데이터에 추가됩니다.

## 데이터 소스를 통해 데이터를 업로드할 때 지표가 함께 업로드되지 않는 이유는 무엇입니까? {#metrics}

데이터 소스의 데이터를 업로드하면 보고서 인터페이스에서 제공될 지표를 업로드하게 됩니다.

예를 들어 사이트에서 판매하는 제품에 대한 콜 센터 매출을 업로드하면 해당 콜 센터 매출을 온라인 매출과 같은 보고서에서 사용할 수 있게 됩니다. 하지만 이와 함께 방문 횟수를 업로드하지 않았으므로 방문 횟수와 연결하여 사용할 수는 없습니다. Adobe는 일반 마케팅 보고서 지표 외에도 데이터 소스를 통해 업로드한 지표와 요소에 대해서만 보고할 수 있습니다.

## 데이터 소스를 통해 보고에 음수 값을 전달하면 어떻게 됩니까? {#negative}

그에 따라 값이 감소합니다.

## 트래픽과 전환 (범용) 데이터 소스의 차이는 무엇입니까? {#traffic}

트래픽 데이터 소스는 적절한 테이블로 요약 값을 업데이트하므로 훨씬 빠르게 업로드됩니다. 전환 데이터를 포함한 범용 데이터 소스 (이벤트 등)는 열의 모든 값을 처리할 수 있는 히트를 생성합니다.

샘플 파일:

<table id="table_D5408E0BDB984229B4C60A66BB53CEBB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code> Date </code> </p> </td> 
   <td colname="col2"> <p> <code> Event15 </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code> 01/01/2013 </code> </p> </td> 
   <td colname="col2"> <p> <code> 553 </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

위 예는 캐시 시스템에서 처리할 553개의 히트를 생성합니다.

## 데이터 소스는 하위 관계, 상관 관계, 경로 지정을 고려합니까? {#breakdown}

데이터 소스 프로세스 (&quot;범용 DS, 비트래픽&quot;)는 캐시에서 처리되는 개별 히트를 만들기 때문에 하위 관계 프로세스는 사용되지만 상관 관계 프로세스는 사용되지 않습니다. 경로 지정은 처리 가능하지만 각 히트는 자체 방문이 되므로 경로 지정이 생성되지 않습니다. 경로 지정 데이터는 웹 로그 가져오기를 위해 생성됩니다.

## 데이터 소스 업로드 또는 분류 파일에서 파일 확장자는 대소문자를 구분합니까? {#case}

데이터 소스 업로드 파일 또는 분류 파일의 확장자가 대문자인 경우 파일이 처리되지 않습니다. 데이터 소스 업로드 파일 확장자는 소문자여야 합니다. 예를 들어 [!DNL file.TXT]와 [!DNL file.FIN]은 처리되지 않습니다. 마찬가지로 [!DNL .TAB] 및 [!DNL .FIN]도 처리되지 않습니다. 하지만, [!DNL .txt] 및 [!DNL .fin]은 처리됩니다.

## 생성된 템플릿에 이벤트를 추가할 수 있습니까, 아니면 3개로 제한됩니까? {#template}

이벤트는 원하는 만큼 추가할 수 있습니다. 하지만, 마법사에서는 이벤트를 세 개만 허용합니다. 템플릿 파일을 생성한 후에 필요에 따라 더 많은 이벤트를 추가할 수 있습니다.

## 데이터 소스 파일에서 하나 이상의 레코드에 있는 열의 수가 헤더 레코드와 다른 경우 어떻게 됩니까? {#header}

데이터 소스 파일에서 하나 이상의 레코드에 있는 열의 수가 헤더 레코드와 다른 경우 다음이 발생합니다.

* 데이터 소스 작성자에게 오류를 알리는 이메일이 전송됩니다.
* 열 불일치로 인해 파일이 처리되지 않습니다.

## 데이터 소스 정보는 롤업됩니까? {#rollup}

데이터 소스 정보는 롤업될 수 있지만 Adobe 고객 지원 센터에서 기록된 날짜로부터 롤업을 다시 처리하여 내역 데이터를 포함해야 합니다. 예를 들어 현재 날짜가 2015년 10월 31일이며 데이터 소스를 사용하여 2015년 8월 1-15일에 대한 데이터를 업로드하는 경우, 2015년 8월 1일부터 재처리를 시작하도록 롤업을 설정해야 새로 가져온 데이터가 포함됩니다.

또한 데이터 소스를 사용하여 롤업 보고서 세트에 직접 데이터를 업로드해서는 안 됩니다. 이 데이터를 롤업에 포함시켜야 한다면 표준 보고서 세트 ( *`child suite`* 라고도 함)로 가져와야 합니다. 자세한 내용은 Adobe 고객 지원 센터에 문의하십시오.

## 페이지 보기 횟수 보고서에 하루치 데이터 소스 데이터가 표시되지 않지만 일주일에 해당하는 데이터는 바르게 표시되는 이유는 무엇입니까? {#week}

데이터 소스는 시간별로 데이터를 보고하지 않습니다. 특정일에 대한 보고서를 실행하려는 경우 데이터는 시간 기준으로만 분류할 수 있으므로 보고서에는 아무것도 표시되지 않습니다. 주별 보고서 또는 월별 보고서 등 하루 이상의 단위로 분류할 때만 데이터를 볼 수 있습니다.

## 웹 서버 로그 데이터 소스 업로드에서 어떻게 고유 방문자를 계산합니까? {#unique}

웹 서버 로그의 고유 방문자 수는 웹 로그에서 *`IP Address`* 및 *`User Agent`*&#x200B;의 개별적인 조합으로 계산됩니다. 이러한 두 가지 항목의 각 고유한 조합은 고유 방문자로 계산됩니다. [!UICONTROL 사용자 에이전트] 열이 비어 있거나 웹 로그에 포함되지 않은 경우 고유 방문자 수를 식별할 수 없고 IP 주소가 여러 개인 경우에도 전체 업로드가 하나의 고유 방문자로 계산됩니다.

## 데이터 소스에서 특정 로그인이 어떤 보고서 세트에 속하는지 어떻게 알 수 있습니까? {#login}

데이터 소스에서 보고서 세트 ID는 설정된 특정 데이터 소스를 식별하는 난수가 첨부된 로그인의 첫 번째 부분입니다. (예: `RSID-drmossdev5 Login-drmossdev5_0001343430`)

## 버전 15와 세그먼테이션은 어떻게 데이터 소스에 영향을 줍니까? {#segmentation}

버전 15에서는 데이터 소스가 소스 유형에 따라 다르게 동작합니다.

* 전체 처리, 웹 로그 및 거래 ID 데이터 소스가 정상으로 나타납니다. 세그먼트가 적용되는 경우 세그먼트 규칙에 따라 데이터가 필터링됩니다.
* 표준 또는 전환 데이터 소스 (광고 캠페인, CRM, 고객 만족, 사이트 실적, 범용 요약 데이터, 온라인 구매, 리드 및 견적, 오프라인 데이터 채널)가 버전 15에 나타납니다. 하지만 이러한 데이터 소스는 방문이나 방문 횟수에 연결되지 않으므로 세그먼트가 적용될 때 필터링에서 제외됩니다.

## 거래 ID를 사용하여 가져온 지표를 Clickstream 데이터 피드 및 데이터 웨어하우스에서 사용할 수 있습니까? {#clickstream}

데이터 피드에는 받은 거래 ID 지표가 모두 들어 있습니다. 하지만, 과거 날짜에 대해 거래 ID 데이터를 업로드하는 경우 해당 데이터를 얻는 유일한 방법은 데이터 피드를 해당 날에 대해 다시 다운로드하는 것입니다.

## 현재 방문자 프로필에서 지속되고 있는 eVar가 데이터 소스를 사용하여 업로드한 지표에 할당되어 있습니까? {#visitor}

전체 처리에는 아니지만, 거래 ID에 대해서는 할당되어 있습니다. 전체 처리 데이터 소스는 개별 방문자 프로필을 사용하여 처리됩니다. 따라서 방문자 ID가 일치하더라도 eVar 할당 측면에서는 함께 연결되어 있지 않게 됩니다. 거래 ID 데이터 소스는 주 방문자 프로필에 연결되어 있으므로, 지속적인 eVar는 거래 ID를 사용하여 업로드된 이벤트에 할당됩니다.

## 데이터 소스를 사용하여 업로드된 eVar는 나중의 온라인 행동에까지 지속됩니까? {#evars}

아니요. 거래 ID 데이터 소스를 통해 업로드된 eVar는 저장된 프로필 정보에서만 읽히게 되고, 프로필을 업데이트하지는 않습니다.
아니요. eVar은 방문자 프로필의 스냅숏에 저장되는 유일한 변수입니다.

## 숫자 및 통화 이벤트는 데이터 소스에서 어떻게 작동합니까? {#numeric}

전체 처리는 이벤트 목록에서 직접 숫자/통화/카운터 (1개 이상) 이벤트 값을 제외한 레거시 이벤트 목록 형식 (`"eventNN,eventKK"``"eventNN=#.##"`이 아닌)만 지원합니다. 데이터 소스 파일의 이벤트 열에 전달되고 1씩 증가하는 경우에만 카운터 이벤트를 지원한다는 의미입니다.

숫자, 통화 또는 카운터 (1개 이상) 이벤트가 필요한 경우 제품 목록을 사용하십시오.

```js
s.products="Footwear;Running Shoes;1;99.99;event1=4.50";
s.products="Footwear;Running Shoes;1;99.99;event1=4.50|event4=1.99";
```
