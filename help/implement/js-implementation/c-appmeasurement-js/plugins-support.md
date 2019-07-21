---
description: 새 JavaScript AppMeasurement 버전에서는 플러그인 지원이 변경되었습니다.
keywords: Analytics 구현; Appmeasurement; Javascript; plugin; 플러그인
seo-description: 새 JavaScript AppMeasurement 버전에서는 플러그인 지원이 변경되었습니다.
seo-title: Appmeasurement 플러그인 지원
solution: Analytics
subtopic: JavaScript AppMeasurement
title: Appmeasurement 플러그인 지원
topic: 개발자 및 구현
uuid: E 048 E 16 B -994 A -4079-BDE 4-3 FAA 3 DF 8 C 96 D
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# Appmeasurement 플러그인 지원

현재 버전의 JavaScript appmeasurement에서 플러그인 지원

## 테스트한 플러그인 {#section_48415FB895E6455FAC34B0B96DE6EBE7}

다음 플러그인은 호환 여부에 대한 테스트 및 확인을 완료했습니다.

* [s.abort flag](/help/implement/js-implementation/plugins/abort.md)
* [appendList](/help/implement/js-implementation/plugins/appendlist.md)
* [Doplugins 함수](/help/implement/js-implementation/plugins/function-doplugins.md)
* [getAndPersistValue](/help/implement/js-implementation/plugins/getandpersistvalue.md)
* [getDaysSinceLastVisit](../../../implement/js-implementation/plugins/getdayssincelastvisit.md#concept_E3D0FEC81E1F4987B39CC467F19FFCFF)
* [getLoadTime](/help/implement/js-implementation/plugins/getloadtime.md)
* [getNewRepeat](../../../implement/js-implementation/plugins/getnewrepeat.md#concept_E3D0FEC81E1F4987B39CC467F19FFCFF)
* [getPageVisibility](/help/implement/js-implementation/plugins/pagevisibility.md)
* [getPercentPageViewed](/help/implement/js-implementation/plugins/getpercentpageviewed.md)
* [getPreviousValue](/help/implement/js-implementation/plugins/getpreviousvalue.md)
* [getQueryParam](/help/implement/js-implementation/plugins/getqueryparam.md)
* [getTimeParting](../../../implement/js-implementation/plugins/gettimeparting.md#concept_3746EA1D1EF746049AE84105B911F44A)
* [getValOnce](/help/implement/js-implementation/plugins/getvalonce.md)
* [getVisitNum](/help/implement/js-implementation/plugins/getvisitnum.md)
* [getVisitStart](/help/implement/js-implementation/plugins/getvisitstart.md)가 있어야 합니다
* [hitGovernor](/help/implement/js-implementation/plugins/hitgovernor.md)
* [내부 트래픽](/help/implement/js-implementation/plugins/internal-traffic.md)
* [performanceTiming](/help/implement/js-implementation/plugins/performancetiming.md)
* [trackTNT](/help/implement/js-implementation/plugins/tracktnt.md)

## 테스트하지 않은 플러그인 {#section_32BA7CAB37554A278170A728F1D65CE9}

다음 플러그인은 아직 기본 기능이 지원되므로 계속 작동하지만, 호환 여부에 대한 테스트 및 확인은 이루어지지 않았습니다. 이 플러그인들은 마이그레이션 전에 개발 환경에서 테스트해야 합니다.

* getActionDepth
* getCookiesAccepted
