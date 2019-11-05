---
description: 'null'
seo-description: 'null'
seo-title: Analytics for Digital Assistants 구현
title: Analytics for Digital Assistants 구현
uuid: c61e6a1a-ec08-4936-9053-5f57223f57ff
translation-type: tm+mt
source-git-commit: b7a92c7b7305c5456e6764b4329c51ad13f2609e

---


# 디지털 보조자에 대한 분석 구현

<!-- 
https://wiki.corp.adobe.com/display/mobileanalytics/Analytics+for+Digital+Assistants+Whitepaper
https://marketing.adobe.com/resources/help/en_US/sc/implement/digital-assistants-white-paper.html
Ticket: https://jira.corp.adobe.com/browse/AN-157750
-->

클라우드 컴퓨팅, 머신 러닝 및 자연어 처리 분야의 최근 발전을 통해 디지털 어시스트는 일상생활의 일부가 되고 있습니다. 소비자는 디바이스와 대화를 시작하고 인간과 같은 방식을 이해하고 반응할 수 있기를 기대하고 있습니다. 디지털 도우미 플랫폼이 더욱 확실히 자리를 잡아가면서 관련 서비스 제공업체들은 사실적이며 실제와 같이 서비스를 소비자에게 제공할 수 있게 되었습니다. 예를 들면 소비자는 다음과 같은 작업을 요청할 수 있습니다.

* "Alexa, 자동차 오일을 바꿔야 하는지 확인해 봐."
* "Cortana, 내 결제 계좌의 잔액이 얼마야?"
* "Siri야, 내 뱅킹 앱에서 어제 저녁 값으로 존에게 20달러 보내 줘."

이 페이지에서는 Adobe Analytics를 사용하여 이러한 유형의 경험을 측정하고 최적화하는 방법에 대한 개요를 제공합니다.

## 디지털 경험 아키텍처 개요

![](assets/Digital-Assitants.png)

오늘날 대부분의 Digital Assistant는 다음과 유사한 높은 수준의 아키텍처를 따릅니다.

1. **장치:** 사용자가 질문을 할 수 있는 마이크가 있는 장치(예: Amazon Echo 또는 전화기)가 있습니다.
1. **Digital Assistant:** 이 장치는 Digital Assistant를 구동하는 서비스와 상호 작용합니다. 여기서 음성은 시스템이 이해할 수 있는 의도로 변환되고 요청 세부 사항이 구문 분석됩니다. 사용자의 의도를 이해한 경우 Digital Assistant가 의도 및 요청 세부 사항을 요청을 처리하는 앱에 전달합니다.
1. **"앱":** 앱은 전화기의 앱 또는 음성 앱일 수 있습니다. 앱이 요청에 응답합니다. 앱이 Digital Assistant에 응답하면 Digital Assistant가 사용자에게 응답합니다.

## Analytics 구현 위치

Analytics를 구현하는 가장 적합한 위치 중 하나가 앱입니다. 이 앱은 디지털 도우미로부터 의도와 세부 사항을 받은 다음, 앱이 응답하는 방법을 결정합니다.

요청 중에는 Adobe Analytics로 데이터를 전송하는 데 도움이 될 수 있는 두 번 있습니다.

1. 요청이 앱에 전송되면
1. 앱에서 응답이 반환된 후.

향후 최적화를 위해 고객에게 발생한 사항을 기록하는 데 관심이 있다면 응답이 반환된 후 Adobe Analytics에 요청을 보냅니다. 요청이 무엇이었는지 그리고 시스템이 어떻게 반응했는지 전체 상황을 파악할 수 있습니다.

## 새 설치

일부 디지털 도우미의 경우 누군가 기술을 설치했을 때, 특히 인증이 포함될 때 알림을 받게 됩니다. 컨텍스트 데이터 변수를 설정하여 Install 이벤트를 전송하는 것이 좋습니다 `a.InstallEvent=1`. 이 기능은 일부 디지털 도우미에서는 사용할 수 없지만 고객 유지율을 확인하는 데 도움이 됩니다. 다음 코드 샘플은 Install 이벤트, Install Date 및 AppID 값을 컨텍스트 데이터 변수로 전송합니다.

```text
GET
/b/ss/[rsid]/1?vid=[UserID]&c.a.InstallEvent=1&c.a.InstallDate=2017-04-24&c.a.AppID=Spoofify1.0&c.OSType=Alexa&pageName=install
HTTP/1.1
Host:
<xref href="https://sc.omtrdc.net">
  sc.omtrdc.net
 Cache-Control: no-cache
</xref href="https:>
```

## 여러 보조 또는 여러 앱

조직에서 여러 플랫폼용 앱을 원할 수 있습니다. 가장 좋은 방법은 각 요청에 앱 ID를 포함하는 것입니다. This variable can be set in the `a.AppID` context data variable. Follow the format of `[AppName] [BundleVersion]`, for example, BigMac for Alexa 1.2:

```text
GET /b/ss/[rsid]/1?vid=[UserID]&c.a.AppID=Spoofify1.0&c.a.Launches=1&c.Product=AmazonEcho&c.OSType=Alexa&pageName=install  HTTP/1.1
Host: example.sc.omtrdc.net
Cache-Control: no-cache
```

```text
GET /b/ss/[rsid]/1?vid=[UserID]&c.a.AppID=Spoofify2.0&c.a.Launches=1&c.Product=GoogleHome&c.OSType=Android&pageName=install  HTTP/1.1
Host: example.sc.omtrdc.net
Cache-Control: no-cache
```

## 사용자/방문자 식별

Adobe Analytics는 Adobe [Experience Cloud](https://docs.adobe.com/content/help/en/id-service/using/home.html) Identity Service를 사용하여 시간 경과에 따른 상호 작용을 동일한 사람에게 연결합니다. 대부분의 디지털 도우미는 다른 사용자에 대해 활동을 유지하는 데 사용할 `userID` 수 있는 항목을 반환합니다. 대부분의 경우 이 값은 고유 식별자로 전달할 수 있는 값입니다. 일부 플랫폼은 허용되는 100자보다 긴 식별자를 반환합니다. 이러한 경우 MD5 또는 Sha1과 같은 표준 해싱 알고리즘을 사용하여 고유 식별자를 고정 길이 값으로 해시하는 것이 좋습니다.

ID 서비스를 사용하면 ECID를 다른 장치(예: 웹-디지털 도우미)에 매핑할 때 가장 많은 값을 제공합니다. 앱이 모바일 앱인 경우 Experience Platform SDK를 있는 그대로 사용하고 `setCustomerID` 메서드를 사용하여 사용자 ID를 전송합니다. However, if your app is a service, use the user ID provided by the service as the ECID, as well as setting it in `setCustomerID`.

```text
GET /b/ss/[rsid]/1?vid=[UserID]&pageName=[intent]  HTTP/1.1
Host: example.sc.omtrdc.net
Cache-Control: no-cache
```

## 세션

Digital Assistant는 대화식이므로 세션의 개념이 있습니다. 예:

**소비자:** "Ok Google, 택시를 불러 줘."

**Google:** "예, 몇 시에 불러드릴까요?"

**소비자:** "오후 8시 30분"

**Google:** "좋습니다. 운전사가 오후 8시 30분에 도착할 것입니다."

세션은 컨텍스트를 유지하고 디지털 지원을 보다 자연스럽게 하기 위해 더 자세한 정보를 수집하는 데 도움이 됩니다. 대화에서 Analytics를 구현할 때 새 세션이 시작될 때 수행해야 할 두 가지 사항이 있습니다.

1. **Audience Manager에 연결:** 응답을 사용자 지정할 수 있도록 사용자가 속해 있는 관련 세그먼트를 가져옵니다. (예를 들면 이 사람은 현재 다중 채널 할인에 적격입니다.)
2. **새 세션 또는 실행 이벤트에 보내기:** Analytics에 첫 번째 응답을 보낼 때 실행 이벤트를 포함합니다. 일반적으로 `a.LaunchEvent=1`의 컨텍스트 데이터를 설정하여 보낼 수 있습니다.

```text
GET /b/ss/[rsid]/1?vid=[UserID]&c.a.LaunchEvent=1&c.Intent=[intent]&pageName=[intent]  HTTP/1.1
Host: sc.omtrdc.net
Cache-Control: no-cache
```

## 의도

각 Digital Assistant에는 의도를 감지한 다음 "앱"에 그 의도를 전달하는 알고리즘이 있으므로 앱이 수행할 작업을 알고 있습니다. 이러한 의도는 요청의 간결한 표현입니다.

예를 들어, 사용자가 "Siri야, 내 뱅킹 앱에서 어제 저녁 값으로 존에게 20달러 보내 줘."라고 말하면 의도는 *sendMoney*.

이러한 각 요청을 eVar로 전송하면 전환 앱의 각 인스턴스에 대해 경로 지정 보고서를 실행할 수 있습니다. 앱에서 의도하지 않은 요청도 처리할 수 있습니다. 변수를 전송하는 대신 '지정된 의도 없음'을 의도 컨텍스트 데이터 변수에 전달하는 것이 좋습니다.

```text
GET /b/ss/[rsid]/1?vid=[UserID]&c.a.AppID=Penmo1.0&c.a.LaunchEvent=1&c.Intent=SendPayment&pageName=[intent]  HTTP/1.1
Host: example.sc.omtrdc.net
Cache-Control: no-cache
```

또는

```text
GET /b/ss/[rsid]/1?vid=[UserID]&c.a.AppID=Penmo1.0&c.a.LaunchEvent=1&c.Intent=No_Intent_Specified&pageName=[intent]  HTTP/1.1
Host: sc.omtrdc.net
Cache-Control: no-cache
```

## 매개 변수/슬롯/엔티티

의도 외에 디지털 도우미에는 종종 의도를 세부적으로 표시하는 키/값 쌍의 집합이 있습니다. 이를 슬롯, 엔티티 또는 매개 변수라고 할 수 있습니다. 예를 들어 "Siri, Send John for dinner last night from my banking app"는 다음 매개 변수를 가집니다.

* Who = John
* Amount = 20
* Why = Dinner

일반적으로 앱에는 이러한 값의 수가 제한되어 있습니다. Analytics에서 이러한 값을 추적하려면 컨텍스트 데이터 변수로 보낸 다음 각 매개 변수를 eVar에 매핑합니다.

```text
GET /b/ss/[rsid]/1?vid=[UserID]&c.a.AppID=Penmo1.0=1&c.a.LaunchEvent=1&c.Intent=SendPayment&c.Amount=20.00&c.Reason=Dinner&c.ReceivingPerson=John&c.Intent=SendPayment&pageName=[intent]  HTTP/1.1
Host: example.sc.omtrdc.net
Cache-Control: no-cache
```

## 오류 상태

경우에 따라 디지털 도우미가 앱에 처리하는 방법을 모르는 입력을 제공합니다. 예: "Siri, Send John 20 bag of coal for dinner last night from my banking app"

이러한 상황이 발생하면 앱에 명확히 묻도록 하십시오. 또한 오류가 발생한 유형을 지정하는 eVar와 함께 응용 프로그램에 오류 상태가 있음을 나타내는 데이터를 Adobe로 보냅니다. 입력 내용이 올바르지 않은 오류와 앱에 문제가 있는 오류를 포함해야 합니다.

```text
GET /b/ss/[rsid]/1?vid=[UserID]&c.a.AppID=Penmo1.0&c.Error=1&c.ErrorName=InvalidCurrency&pageName=[intent]  HTTP/1.1
Host: example.sc.omtrdc.net
Cache-Control: no-cache
```

## 디바이스 기능

대부분의 플랫폼은 사용자가 말한 장치를 노출시키지 않지만 장치의 기능은 노출됩니다. 오디오, 화면, 비디오 등과 같이 이 정보는 사용자와 상호 작용할 때 사용할 수 있는 컨텐츠 유형을 정의하므로 유용합니다. 장치 기능을 측정할 때는 이를 알파벳 순서로 연결하는 것이 가장 좋습니다.

예: `":Audio:Camera:Screen:Video:"`

선행 및 후행 콜론 기능은 세그먼트를 만들 때 도움이 됩니다. 예를 들어 `:Audio:` 기능이 있는 모든 히트를 표시합니다.

* [Amazon Alexa를](https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/docs/alexa-skills-kit-interface-reference) 사용한 Amazon 기능
* [Google에서](https://developers.google.com/actions/assistant/surface-capabilities) 동작을 사용하는 Google 기능

## 예

| 사람 | 장치 응답 | 작업/의도 | 요청 받기 |
| --- | --- | --- | --- | ---|
| Spoofify 설치 | 응답 없음 | 설치 | `GET /b/ss/[rsid]/1?vid=[UserID]&c.a.InstallEvent=1&c.a.InstallDate=[currentDate]&c.a.AppID=Spoofify1.0&c.OSType=Alexa&c.Intent=Install&pageName=Install  HTTP/1.1`<br>`Host: example.sc.omtrdc.net`<br>`Cache-Control: no-cache` |
| Spoofify 재생 | "좋아, 스푸피시" | 재생 | `GET /b/ss/[rsid]/1?vid=[UserID]&c.a.AppID=Spoofify1.0&c.a.LaunchEvent=1&c.Intent=Play&pageName=PlayApp  HTTP/1.1`<br>`Host: example.sc.omtrdc.net`<br>`Cache-Control: no-cache` |
| 노래 변경 | "좋아, 어떤 노래를 원하니?" | ChangeSong | `GET /b/ss/[rsid]/1?vid=[UserID]&c.a.AppID=Spoofify1.0&c.Intent=ChangeSong&pageName= Ask%20For%20Song  HTTP/1.1`<br>`Host: example.sc.omtrdc.net`<br>`Cache-Control: no-cache` |
| "Baby Shark" 재생 | "좋아, 핑크퐁의 '아기 상어' 재생" | ChangeSong | `GET /b/ss/[rsid]/1?vid=[UserID]&c.a.AppID=Spoofify1.0&c.Intent=ChangeSong&pageName=Action%20Play%20Song&c.SongID=[012345]  HTTP/1.1`<br>`Host: example.sc.omtrdc.net`<br>`Cache-Control: no-cache` |
| 재생 목록 변경 | "네, 어떤 재생 목록을 원하십니까?" | ChangePlaylist | `GET /b/ss/[rsid]/1?vid=[UserID]&c.a.AppID=Spoofify1.0&c.Intent=ChangePlaylist&pageName=Ask%20For%20Playlist  HTTP/1.1`<br>`Host: example.sc.omtrdc.net`<br>`Cache-Control: no-cache` |
| 좋아하는 노래 재생 목록 | "좋아요, 좋아하는 노래 재생 목록 재생" | ChangePlaylist | `GET /b/ss/[rsid]/1?vid=[UserID]&c.a.AppID=Spoofify1.0&c.Intent=ChangePlaylist&pageName=Action%20Play%20Playlist&c.Playlist=My%20Favorite%20Songs  HTTP/1.1`<br>`Host: example.sc.omtrdc.net`<br>`Cache-Control: no-cache` |
| 음악 끄기 | 반응 없음, 음악 꺼짐 | 꺼짐 | `GET /b/ss/[rsid]/1?vid=[UserID]&c.a.AppID=Spoofify1.0&c.Intent=Off&pageName=Music%20Off  HTTP/1.1`<br>`Host: example.sc.omtrdc.net`<br>`Cache-Control: no-cache` |
