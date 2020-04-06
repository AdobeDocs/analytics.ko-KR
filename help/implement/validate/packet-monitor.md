---
title: 패킷 분석기
description: 패킷 분석기를 사용하여 구현에서 Adobe 데이터 수집 서버로 보낸 데이터를 볼 수 있습니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 패킷 분석기

패킷 분석기를 사용하여 구현에서 Adobe 데이터 수집 서버로 보낸 데이터를 볼 수 있습니다.

Adobe Experience Cloud Debugger와 마찬가지로 패킷 모니터는 이미지 요청에서 전달되는 데이터 매개 변수를 표시하지만 추가 기능도 제공합니다.

* 사용자 지정 링크 추적 이미지 요청 보기
* 하드 코딩된 이미지 요청이나 [!DNL Appmeasurement]와 같이 JavaScript 외의 구현 방법을 사용하여 이미지 요청 보기

Analytics 요청을 보려면 &quot;b/ss&quot;를 사용하여 발신 요청을 필터링하십시오.

요청이 Adobe의 [!DNL Analytics] 처리 서버에 전달되지 못하는 경우에도 디버거가 이미지 요청을 보고하는 드문 경우가 있습니다. 패킷 모니터를 사용하면 특정 이미지 요청이 성공적으로 실행되는지 100% 확신할 수 있습니다.

Adobe는 공식적인 패킷 모니터를 제공하지 않지만 인터넷에는 다양한 패킷 모니터가 있습니다. 다음은 다른 사용자가 유용하다고 인정한 일부 패킷 모니터입니다.

>[!NOTE] 이러한 목록은 전체 목록이 아니라 자주 사용하는 모니터에 대한 정보입니다. 성공적으로 사용하고 유용한 패킷 모니터가 있는 경우 이 창 오른쪽의 [!UICONTROL Feedback] 단추를 사용하여 피드백을 제공해 주십시오.

| Firefox | Internet Explorer | Chrome | 독립 실행형 프로그램 |
|---|---|---|---|
| [관찰점](https://www.observepoint.com/product#plugin) (태그 뷰어) | [HttpWatch](https://www.httpwatch.com/) | [관찰점](https://www.observepoint.com/product#plugin) (태그 뷰어) | [찰스](https://www.charlesproxy.com/) |
| [HttpFox](https://addons.mozilla.org/ko-KR/firefox/addon/httpfox/) |  | [Chrome Developer Tools](https://code.google.com/chrome/devtools/docs/overview.html) | [Fiddler](https://www.fiddler2.com/fiddler2/) |
| [Tamper Data](https://addons.mozilla.org/ko-kr/firefox/addon/tamper-data/) |  | [Firebug Lite](https://chrome.google.com/webstore/detail/bmagokdooijbeehmkpknfglimnifench) | [Wireshark](https://www.wireshark.org/) |
| [HttpWatch](https://www.httpwatch.com/) |  |  |  |
| [Firebug](https://getfirebug.com/) |  |  |  |

>[!NOTE] Adobe는 이러한 패킷 모니터와 관련하여 발생할 수 있는 문제를 지원하거나 해결하지 않습니다. 대신 패킷 모니터 제공 사이트에서 지원을 문의하십시오.

## 응답 코드의 NS_BINDING_ABORTED

이 오류는 링크 추적 이미지 요청이 Adobe 데이터 수집 서버의 응답을 기다리기 전에 브라우저를 다음 페이지로 진행할 수 있도록 설계되었기 때문에 발생합니다.

이미지 요청에 대한 Adobe의 응답은 단순히 빈 1x1 투명 이미지이며, 이는 페이지의 컨텐츠와 관련이 없습니다. Adobe의 패킷 모니터에 **[!UICONTROL 200 OK]** 응답이나 **[!UICONTROL NS_BINDING_ABORTED]** 응답이 있는 라인 항목이 표시되면 데이터가 서버에 도착한 것이므로, 페이지를 더 이상 기다릴 필요가 없습니다.

플러그인으로 통합된 패킷 모니터는 전체 응답을 거의 볼 수 없습니다. 전체 응답이 수신되지 않았기 때문에 요청이 취소된 것으로 보는 경향이 있습니다. 이러한 모니터는 또한 중단된 요청인지 응답인지 구분하지 않습니다. 독립형 패킷 모니터는 일반적으로 더 자세한 메시지를 표시하며 상태를 보다 정확하게 보고합니다. 예를 들어, 사용자는 Charles에서 &quot;전체 응답을 *받기 전에 클라이언트* 연결 차단&quot;이라는 메시지를 받을 수 있습니다. 즉, 데이터가 서버에 도달했고 1x1 픽셀을 받기 전에 브라우저가 다음 페이지로 이동했습니다.

외부 패킷 스니퍼가 응답 대신 데이터 수집 요청이 중단되었다고 보고하는 경우, 이는 우려입니다. Adobe [!DNL Customer Care]에서 문제 해결에 관한 도움말을 제공할 수 있습니다.
