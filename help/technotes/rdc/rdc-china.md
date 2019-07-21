---
title: 중국의 지역 데이터 수집
seo-title: Adobe Analytics China RDC
description: null
seo-description: null
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# 중국의 지역 데이터 수집

중국의 Adobe RDC(지역 데이터 수집)를 사용하여 중국에 있는 고객이 다른 국가가 아닌 중국의 DCC(데이터 수집 센터)로 직접 데이터를 보낼 수 있습니다. 이렇게 하면 중국 외부에 있는 DCC로 데이터를 전송하는 것보다 페이지 로드 시간 및 데이터 정확성이 향상됩니다.

> [!IMPORTANT] 중국 RDC 노드의 사용과 관련된 추가 비용이 있습니다. 이 문서에 설명된 RDC 노드를 사용하여 중국에서 데이터 수집을 구현하기 전에 조직의 계정 관리자에게 연락하여 이 기능을 사용할 수 있는지 확인하십시오.

## 중국 추적 서버 설정

편리한 서비스 시점에서 중국 RDC로 추적을 가져올 수 있습니다. 중국 RDC로 라우팅하려는 디지털 속성 (예: 모바일 앱 또는 웹 페이지) 의 경우 추적 서버를 다음으로 변경하십시오.

`<namespace>.sc.adobedc.cn`

적절한 네임스페이스를 삽입해야 합니다. 네임스페이스는 일반적으로 기존 추적 서버의 시작 부분에 있습니다. For example: `<namespace>.sc.adobedc.cn` - although any namespace value will work. SSL 외 퍼스트 파티 [CNAME](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/fpcookies_cname.html) 레코드로 이 새 위치를 가리킬 수 있습니다.

고객 기반이 중국 외부에 있는 경우 모든 속성 및 지역에 대해 Trackingserver 값을 중국 RDC로 전역적으로 설정하지 마십시오. trackingServer는 중국에 있는 고객에 관해서만 중국 RDC 값으로 설정해야 합니다. 그러지 않으면 강제로 데이터 수집이 중국으로 이동되고, 응답을 받기 위해 다시 이동되므로 중국 이외의 국가에 있는 사용자의 속도가 느려집니다.

## 중국에서 사용자 식별

디지털 속성이 호스팅되는 위치 또는 사용하는 언어와 관계없이 중국에 있는 사용자가 중국의 RDC 노드를 사용하면 환경이 개선됩니다. 따라서 권장되는 방법은 사용자가 중국에 있는지 확인한 다음 해당 사용자에 대해 중국 RDC를 사용하는 것입니다. 이 사용자를 식별하는 데 다음과 같은 방법이 도움이 됩니다.

* 신뢰할 수 있는 Geoip 솔루션 사용 서버측 솔루션을 사용하여 Adobe Experience Platform Launch (또는 데이터 태그 관리) 와 쉽게 통합할 수 있습니다. 이 경우, Experience Platform Launch 또는 DTM 개체에 표준 데이터 요소를 포함하여 위치를 결정할 수 있습니다. 또는 클라이언트 측 GeoIP 솔루션을 사용할 수 있습니다. 이 경우 Experience Platform Launch를 클라이언트측 코드에 연결할 수 있습니다. 이 솔루션을 통해 사용자에게 현지화된 사이트로 이동하라는 메시지를 표시할 수 있습니다. 이것은 첫 번째 페이지가 글로벌 추적 서버에 의해 카운트되고 중국 내 두 번째 페이지가 카운트되는 위험을 나타내며, 이것은 두 번 카운트된 방문으로 이어질 수 있습니다. GeoIP 솔루션에 관한 권장 지침을 따르십시오. Adobe는 사용하는 GeoIP 솔루션의 정확성에 대해 책임을 지지 않습니다.

* Using site structure or the browser language (the `navigator.language / accept-language` header). 이 방법은 비용이 저렴하며 성능을 향상할 수 있습니다. 하지만 중국 이외의 국가를 방문하는 중국어 사용 방문자의 속도는 느려질 수 있습니다.
* 중국에 기반을 둔 호스팅 솔루션을 사용하고 호스트에 따라 Trackingserver를 중국 RDC로 설정합니다. 또한 속도가 크게 향상됩니다.

## 현재 제한 사항

중국 RDC의 현재 제한 사항:

1. China RDC does not support first party SSL ([s.trackingServerSecure](https://helpx.adobe.com/analytics/kb/determining-data-center.html) in your JavaScript), or [Server-Side Forwarding](https://marketing.adobe.com/resources/help/en_US/reference/ssf.html) to Adobe Audience Manager.
2. [A4T](https://marketing.adobe.com/resources/help/en_US/target/a4t/a4t.html) 및 [ECID](https://marketing.adobe.com/resources/help/en_US/mcvid/)가 지원되지만, Target 및 Demdex 도메인은 현재 중국 본토에 있지 않으며, 속도나 안정성이 중국 RDC에 있는 것과 동일하지 않습니다.

## 중국에 대한 Adobe의 노력

Adobe는 중국 RDC 진행을 영구적으로 유지할 계획이며, 퍼스트 파티 SSL 및 서버 측 전달과 같은 기능을 추가로 지원할 예정입니다. 또한 중국에서 ECID 및 Audience Manager 수집을 완벽하게 지원할 demdex(또는 그와 동등한) 도메인을 중국에 제공할 계획입니다. Adobe의 중국 RDC를 사용하기 시작한 고객은 이 데이터 수집 종단점을 무한하게 계속 사용할 수 있습니다.
