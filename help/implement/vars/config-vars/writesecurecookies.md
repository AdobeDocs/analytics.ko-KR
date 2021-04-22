---
title: writeSecureCookies
description: AppMeasurement가 Secure 속성을 사용하여 쿠키를 설정할 수 있도록 허용합니다.
exl-id: 0e03d621-5770-4c25-981d-e4af1431ec69
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '200'
ht-degree: 100%

---

# writeSecureCookies

`writeSecureCookies` 변수를 사용하면 AppMeasurement가 Analytics에 대한 [보안 쿠키](https://en.wikipedia.org/wiki/Secure_cookie)를 설정할 수 있습니다. 이 설정은 AppMeasurement에서 설정한 방문자 ID 쿠키와 `Util.CookieWrite()` 메서드를 사용하여 설정한 쿠키에 모두 적용됩니다. 이렇게 하려면 AppMeasurement 2.18.0 이상이 필요합니다.

>[!IMPORTANT]
>
> `writeSecureCookies` 변수를 활성화하면 사이트의 모든 콘텐츠가 HTTPS에서 안전하게 제공되는지 확인하십시오. 이 변수가 활성화되어 있고 페이지에 안전하지 않은 콘텐츠가 있는 경우 AppMeasurement가 작동하지 않습니다.

## Adobe Experience Platform Launch에서 보안 쿠키 작성

[!UICONTROL 보안 쿠키 작성]은 Adobe Analytics 확장을 구성할 때 [!UICONTROL 쿠키] 아코디언 아래의 확인란입니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 확장] 탭으로 이동한 다음, Adobe Analytics 아래의 [!UICONTROL 구성] 버튼을 클릭합니다.
4. [!UICONTROL 쿠키] 아코디언을 확장하면 [!UICONTROL 보안 쿠키 작성] 확인란이 표시됩니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.writeSecureCookies

`s.writeSecureCookies` 변수는 쿠키를 만들 때 AppMeasurement가 보안 속성을 설정하는지 여부를 결정하는 부울입니다. 기본값은 `false`입니다. 사이트의 모든 콘텐츠가 안전하며 AppMeasurement에서 설정한 쿠키가 보안 속성을 갖도록 하려는 경우 이 변수를 `true`로 설정합니다.

```js
s.writeSecureCookies = true;
```
