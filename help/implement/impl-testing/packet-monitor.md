---
description: 패킷 분석기를 사용하여 구현에서 Adobe 데이터 수집 서버로 보낸 데이터를 볼 수 있습니다.
keywords: Analytics 구현
seo-description: 패킷 분석기를 사용하여 구현에서 Adobe 데이터 수집 서버로 보낸 데이터를 볼 수 있습니다.
seo-title: 패킷 분석기
solution: Analytics
subtopic: 디버거
title: 패킷 분석기
topic: 개발자 및 구현
uuid: 3597 C 23 A -1 C 72-46 E 6-909 D-F 861 Cbeef 490
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 패킷 분석기

패킷 분석기를 사용하여 구현에서 Adobe 데이터 수집 서버로 보낸 데이터를 볼 수 있습니다.

[!DNL DigitalPulse Debugger]와 마찬가지로 패킷 모니터는 이미지 요청에서 전달되는 데이터 매개 변수를 표시하지만 추가 기능도 제공합니다.

* 사용자 지정 링크 추적 이미지 요청 보기
* 하드 코딩된 이미지 요청이나 [!DNL Appmeasurement]와 같이 JavaScript 외의 구현 방법을 사용하여 이미지 요청 보기

Analytics 요청을 보려면 "b/ss"를 사용하여 발신 요청을 필터링하십시오.

요청이 Adobe의 [!DNL Analytics] 처리 서버에 전달되지 못하는 경우에도 디버거가 이미지 요청을 보고하는 드문 경우가 있습니다. 패킷 모니터는 특정 이미지 요청이 성공적으로 실행되었는지 100% 확신할 수 있는 훌륭한 방법입니다.

Adobe가 정식 패킷 모니터를 제공하지는 않지만 인터넷에서 다양한 패킷 모니터를 찾아볼 수 있습니다. 다음은 다른 사용자가 유용하다고 여기는 일부 패킷 모니터입니다.

>[!NOTE]
>
>이러한 목록은 포괄적이 아니라 자주 사용하는 모니터에 대한 정보입니다. 성공적으로 사용하고 있는 유용한 패킷 모니터가 있는 경우 이 창 오른쪽에 있는 [!UICONTROL 피드백] 단추를 사용하여 피드백을 제공해 주십시오.

| Firefox | Internet Explorer | Chrome | 독립 실행형 프로그램 |
|---|---|---|---|
| [Observe Point](https://www.observepoint.com/product#plugin)(태그 뷰어) | [HttpWatch](https://www.httpwatch.com/) | [Observe Point](https://www.observepoint.com/product#plugin)(태그 뷰어) | [Charles](https://www.charlesproxy.com/) |
| [HttpFox](https://addons.mozilla.org/en-US/firefox/addon/httpfox/) |  | [Chrome Developer Tools](https://code.google.com/chrome/devtools/docs/overview.html) | [Fiddler](https://www.fiddler2.com/fiddler2/) |
| [Tamper Data](https://addons.mozilla.org/en-us/firefox/addon/tamper-data/) |  | [Firebug Lite](https://chrome.google.com/webstore/detail/bmagokdooijbeehmkpknfglimnifench) | [Wireshark](https://www.wireshark.org/) |
| [HttpWatch](https://www.httpwatch.com/) |  |  |  |
| [Firebug](https://getfirebug.com/) |  |  |  |

>[!NOTE]
>
>Adobe는 이러한 패킷 모니터에서 발생할 수 있는 문제를 지원하거나 해결하지 않습니다. 대신 패킷 모니터 제공 사이트에서 지원을 문의하십시오.

<!-- 

debugger_ns_binding.xml

 -->

이 오류는 링크 추적 이미지 요청이 Adobe의 데이터 수집 서버에서 오는 응답을 기다리기 전에 브라우저를 다음 페이지로 진행할 수 있게 디자인되었기 때문에 발생합니다.

이미지 요청에 대한 Adobe의 응답은 페이지의 컨텐츠와 관계가 없는 1x1 투명 이미지입니다. Adobe의 패킷 모니터에 **[!UICONTROL 200 OK]** 응답이나 **NS_BINDING_ABORTED]응답이 있는 라인 항목이 표시되면 데이터가 서버에 도착한 것이므로,[!UICONTROL ** 더 이상 페이지를 대기시킬 필요가 없습니다.

플러그인으로 통합된 패킷 모니터는 전체 응답을 보는 경우가 흔치 않습니다. 모니터는 전체 응답이 수신되지 않았기 때문에 요청을 취소된 것으로 보는 경향이 있습니다. 이러한 모니터는 또한 취소된 것이 요청과 응답 중 어느 것인지 구분하지 않습니다. 독립형 패킷 모니터는 일반적으로 더 자세한 메시지를 표시하며 상태를 더 정확하게 보고합니다. 예를 들어, 사용자가 *Charles*&#x200B;로부터 "전체 응답을 받기 전에 클라이언트 연결이 끊어졌습니다."와 같은 메시지를 받을 수 있습니다. 이 메시지는 데이터가 Adobe 서버에 도달했고 1x1 픽셀을 받기 전에 브라우저가 다음 페이지로 이동한 경우를 의미합니다.

외부 패킷 스니퍼가 응답 대신 데이터 수집 요청의 취소를 보고하면 심각한 문제일 수도 있습니다. Adobe [!DNL Customer Care]에서 문제 해결에 관한 도움말을 제공할 수 있습니다.
