---
title: 구현 FAQ
description: 구현에 대한 자주 묻는 질문 및 추가 정보 링크.
exl-id: 4bab6d51-0077-42ce-8091-f75207d4c4db
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '499'
ht-degree: 100%

---

# Analytics 구현에 대한 FAQ

구현에 대한 자주 묻는 질문 및 추가 정보 링크.

## Experience Cloud 방문자 ID와 Analytics 방문자 ID의 차이점은 무엇입니까?

ID 서비스는 Experience Cloud에 있는 다른 솔루션 간에 공유할 수 있는 고유한 영구 식별자를 지정합니다. Analytics 방문자 ID는 Analytics에서만 사용됩니다. 구현에서는 Experience Cloud 방문자 ID 서비스를 사용하는 것이 좋습니다.

## 하트비트 비디오 추적은 어떻게 구현합니까?

[Adobe Analytics에서 오디오 및 비디오 측정](https://docs.adobe.com/content/help/ko-KR/media-analytics/using/media-overview.html)을 참조하십시오.

## Adobe의 서비스 중단이 성능에 영향을 줄 수 있습니까?

아니요. JavaScript 파일은 Adobe 서버에서 호스팅되지 않으므로 Adobe 중단은 AppMeasurement 라이브러리에 영향을 주지 않습니다. Adobe Experience Platform Launch를 사용하는 경우, JavaScript 파일은 Akamai에 의해 호스팅되거나, 조직이 결정한 서버 위치에서 호스팅됩니다.

## 데이터를 브라우저에서 Adobe 서비스로 보내면 성능이 저하될 수 있습니까?

AppMeasurement는 HTML 페이지 내에 이미지 개체를 만들며, 그렇게 되면 브라우저가 Adobe 데이터 수집 서버의 이미지 개체를 요청합니다. 데이터 수집 서버가 느려지거나 응답을 하지 않으면, 이미지가 반환되거나, 시간 초과가 발생할 때까지 해당 요청을 처리하는 스레드가 지연됩니다. 브라우저는 여러 스레드로 이미지를 처리하고, Adobe 중단이 페이지 로드 시간에 미치는 영향은 매우 작으므로, 다른 스레드가 계속 작동하는 동안 한 스레드를 연결 중입니다.

## Analytics 구현을 무효화하거나 제거하려면 어떻게 합니까?

조직이 계약 만료 때문에 또는 서버 호출 수를 줄이기 위해 구현을 제거하려는 경우가 있습니다.

* **Launch를 사용한 구현**: [!UICONTROL 확장] 탭에서 Adobe Analytics 확장 기능을 비활성화하거나 제거한 다음 게시합니다.
* **이전 AppMeasurement 구현**: `s_code.js` 파일의 전체 콘텐츠를 다음 코드 줄로 바꿉니다.

```js
var s = new Object();
```

>[!WARNING]
>
>금지 사항:
>
>* Adobe 서버에서 불필요한 로드를 생성하므로 보고서 세트를 잘못된 값으로 변경하지 마십시오.
>* 각 페이지에서 `s_code.js` 파일에 대한 모든 참조를 제거하지 않는 한 이 파일을 모두 제거하지 마십시오.
>* `trackingServer` 변수를 Adobe에서 멀리 가리키도록 변경하지 마십시오. AppMeasurement가 여전히 404 오류를 반환하는 이미지 요청을 전송합니다.


## 코드 분석기를 통해 AppMeasurement를 실행했으며 AppMeasurement가 `Math.random()` 사용을 잠재적인 보안 위험으로 표시했습니다. 민감한 데이터에 `Math.random()`을 사용합니까?

아니요. `Math.random()`을 사용하는 숫자는 민감한 데이터를 마스킹, 전송 또는 수신하는 데 사용되지 않습니다. Adobe 데이터 수집 서버로 전송되는 데이터는 기본 HTTPS 연결의 보안에 의존합니다. <!-- AN-173590 -->

AppMeasurement는 세 가지 주요 영역에서 `Math.random()` 을 사용합니다.

* **샘플링**: 구현에 따라 일부 정보는 사이트 방문자의 일부에 대해서만 수집될 수 있습니다. `Math.random()`은 특정 방문자가 데이터를 보내야 하는지 여부를 결정하는 데 사용됩니다. 대부분의 구현은 샘플링을 사용하지 않습니다.
* **대체 방문자 ID**: 쿠키에서 방문자 ID를 검색할 수 없는 경우 무작위 방문자 ID가 생성됩니다. AppMeasurement의 이 부분에서는 `Math.random()`에 대한 두 번의 호출을 사용합니다.
* **캐시 무효화**: 브라우저 캐싱을 방지하기 위해 이미지 요청 URL 끝에 임의의 숫자가 추가됩니다.
