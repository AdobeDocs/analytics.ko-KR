---
title: 패킷 분석기
description: 패킷 분석기를 사용하여 구현에서 Adobe 데이터 수집 서버로 보낸 데이터를 볼 수 있습니다.
keywords: packet sniffer, http status, 200, 302, charles
translation-type: tm+mt
source-git-commit: b359582fe8ab6ee04bb478825d9989d850390f96
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 58%

---


# 패킷 분석기

패킷 분석기를 사용하여 구현에서 Adobe 데이터 수집 서버로 보낸 데이터를 볼 수 있습니다.

Adobe Experience Cloud Debugger와 마찬가지로 패킷 모니터는 이미지 요청에서 전달되는 데이터 매개 변수를 표시하지만 추가 기능도 제공합니다.

* 사용자 지정 링크 추적 이미지 요청 보기
* 하드 코딩된 이미지 요청이나 [!DNL Appmeasurement]와 같이 JavaScript 외의 구현 방법을 사용하여 이미지 요청 보기

Analytics 요청을 보려면 &quot;b/ss&quot;를 사용하여 발신 요청을 필터링하십시오.

요청이 Adobe의 [!DNL Analytics] 처리 서버에 전달되지 못하는 경우에도 디버거가 이미지 요청을 보고하는 드문 경우가 있습니다. 패킷 모니터는 특정 이미지 요청이 성공적으로 실행되었는지 100% 확신할 수 있는 훌륭한 방법입니다.

Adobe가 정식 패킷 모니터를 제공하지는 않지만 인터넷에서 다양한 패킷 모니터를 찾아볼 수 있습니다. 다음은 다른 사용자가 유용하다고 여기는 일부 패킷 모니터입니다.

>[!TIP]
>
>이러한 목록은 전체 목록이 아니라 자주 사용하는 모니터에 대한 정보입니다.

| Firefox | Internet Explorer | Chrome | 독립 실행형 프로그램 |
|---|---|---|---|
| [Observe Point](https://www.observepoint.com/product#plugin)(태그 뷰어) | [HttpWatch](https://www.httpwatch.com/) | [Observe Point](https://www.observepoint.com/product#plugin)(태그 뷰어) | [Charles](https://www.charlesproxy.com/) |
| [HttpFox](https://addons.thunderbird.net/en-us/firefox/addon/httpfox/) |  | [Chrome Developer Tools](https://code.google.com/chrome/devtools/docs/overview.html) | [Fiddler](https://www.fiddler2.com/fiddler2/) |
| [Tamper Data](https://addons.mozilla.org/en-US/firefox/addon/tamper-data-for-ff-quantum/) |  | [Firebug Lite](https://chrome.google.com/webstore/detail/bmagokdooijbeehmkpknfglimnifench) | [Wireshark](https://www.wireshark.org/) |
| [HttpWatch](https://www.httpwatch.com/) |  |  |  |
| [Firebug](https://getfirebug.com/) |  |  |  |

>[!NOTE]
>
>Adobe은 이러한 패킷 모니터에서 발생하는 문제를 지원하거나 해결하지 않습니다. 패킷 모니터 제공 사이트에서 지원을 참조하십시오.

## 일반적인 HTTP 응답 상태 코드

AppMeasurement가 Adobe 데이터 수집 서버로 데이터를 보내면 서버는 응답 상태 코드로 응답합니다.

* **200 OK**:데이터 수집 서버에서 가장 일반적인 응답 이미지 요청을 수신했으며 투명한 이미지가 반환되었습니다.
* **302 발견됨**:이 응답을 받아야 하는 몇 가지 가능한 이유가 있습니다.
   * 방문자의 첫 번째 이미지 요청:리디렉션은 사용자가 사이트를 처음 방문하는 경우에 발생합니다. 이 리디렉션은 방문자 쿠키를 가져오는 것입니다. 데이터 수집에는 영향을 주지 않습니다.
   * Comscore와 Adobe 간의 통합:조직에서 Comscore/Analytics 통합을 사용하는 경우 각 이미지 요청은 항상 302 응답을 가져옵니다.
* **404 찾을 수 없음**:이 응답은 이미지 요청을 찾을 수 없으며 데이터가 Adobe 데이터 수집 서버로 전송되지 않음을 의미합니다. 이 응답은 하드 코딩된 이미지 요청의 형식이 올바로 지정되지 않은 경우에도 가능합니다. Analytics를 구현한 개인 또는 팀과 함께 이 문제를 해결하십시오.

## 응답 코드의 NS_BINDING_ABORTED

이 메시지는 링크 추적 이미지 요청이 Adobe 데이터 수집 서버의 응답을 기다리기 전에 브라우저를 다음 페이지로 진행할 수 있도록 설계되었기 때문에 발생합니다.

이미지 요청에 대한 Adobe의 응답은 페이지의 컨텐츠와 관계가 없는 1x1 투명 이미지입니다. If you see a line item in your packet monitor from Adobe, either with a **[!UICONTROL 200 OK]** response or an **[!UICONTROL NS_BINDING_ABORTED]** response, the data has reached Adobe&#39;s servers. 더 이상 페이지를 대기시킬 필요가 없습니다.

플러그인으로 통합된 패킷 모니터는 전체 응답을 보는 경우가 흔치 않습니다. 모니터는 전체 응답이 수신되지 않았기 때문에 요청을 취소된 것으로 보는 경향이 있습니다. 이러한 모니터는 또한 취소된 것이 요청과 응답 중 어느 것인지 구분하지 않습니다. 독립형 패킷 모니터는 일반적으로 더 자세한 메시지를 표시하며 상태를 더 정확하게 보고합니다. 예를 들어, 사용자가 *Charles*&#x200B;로부터 &quot;전체 응답을 받기 전에 클라이언트 연결이 끊어졌습니다.&quot;와 같은 메시지를 받을 수 있습니다. 이 메시지는 데이터가 Adobe 서버에 도달했고 1x1 픽셀을 받기 전에 브라우저가 다음 페이지로 이동한 경우를 의미합니다.

외부 패킷 모니터에서 응답 대신 데이터 수집 요청이 중단되었다고 보고하면 우려입니다. Adobe [!DNL Customer Care]에서 문제 해결에 관한 도움말을 제공할 수 있습니다.
