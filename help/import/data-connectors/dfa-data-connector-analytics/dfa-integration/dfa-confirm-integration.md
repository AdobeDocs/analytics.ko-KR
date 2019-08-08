---
description: 필요한 웹 사이트 업데이트를 모두 완료한 후 Charles*, Chrome Developer Tools 또는 Firebug*와 같은 네트워크 트래픽 뷰어를 사용하여 DFA가 Adobe 수집 서버와 통신하는지 확인할 수 있습니다.
keywords: DFA
seo-description: 필요한 웹 사이트 업데이트를 모두 완료한 후 Charles*, Chrome Developer Tools 또는 Firebug*와 같은 네트워크 트래픽 뷰어를 사용하여 DFA가 Adobe 수집 서버와 통신하는지 확인할 수 있습니다.
seo-title: 성공적인 DFA 통합 확인
solution: Analytics
title: 성공적인 DFA 통합 확인
topic: Data connectors
uuid: D 658 CD 7 C -6377-439 A -850 C-ECEA 8 C 41 F 970
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# 성공적인 DFA 통합 확인{#confirming-a-successful-dfa-integration}의 단계에 따라 작동 중인 통합이 있는지 확인합니다

필요한 웹 사이트 업데이트를 모두 완료한 후 Charles*, Chrome Developer Tools 또는 Firebug*와 같은 네트워크 트래픽 뷰어를 사용하여 DFA가 Adobe 수집 서버와 통신하는지 확인할 수 있습니다.

DFA 지원 `s_code.js` 파일을 배포한 후 네트워크 트래픽 뷰어를 사용하여 DFA와 Adobe 데이터 수집 서버 간 요청을 확인하여 다음을 찾을 수 있습니다.

* A request to DFA's `fls.doubleclick.net/json` service. 이 서비스는 사용하는 DFA의 버전에 따라 다르게 응답할 수 있습니다. DFA 통합 버전 1.5를 사용하여 다음을 수행하십시오.

   * HTTP 302에서 [!DNL ad.doubleclick.net]으로 리디렉션합니다. 이 경우 광고 방문자에 대한 정보가 들어 있는 위치: 태그를 응답에 보냅니다.
   * This Location tag causes a redirect to [!DNL integrate.112.2o7.net/dfa_echo]. 이 서비스는 광고 방문자에 대한 정보를 JSON(JavaScript Object Notati on) 인코딩 문자열로 변환합니다. 이 데이터는 200 OK HTTP 응답과 함께 반환됩니다.

* DFA 통합 버전 2.0(고급 광고 제공 기능)을 사용하여 다음을 수행하십시오.

   * [!DNL fls.doubleclick.net]이 200 OK로 직접 응답합니다.

어느 경우든지 요청이 성공하면 vX 매개 변수(여기서 X는 뷰스루 eVar 번호)가 있는 Adobe 데이터 수집 서버로 요청이 전달됩니다. 이 매개 변수 값은 DFA-XXXX-XXXX- XXXX-XXXX-XXXX-XXXX-XXXX-XXXX-XXXX 형식을 사용합니다. 이 문자열에는 마지막 클릭 및 현재 방문자의 마지막 노출에 대한 정보가 들어 있습니다.
