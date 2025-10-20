---
title: Adobe Analytics 태그 확장을 사용한 방문자 식별
description: Adobe Analytics 태그 확장을 구현할 때 방문자를 올바르게 식별합니다.
source-git-commit: 779ba5b0a1d71467aaaf3872fd707cc323ae8af2
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# Adobe Analytics 태그 확장을 사용한 방문자 식별

Adobe Analytics 태그 확장 기능에서는 태그 관리 인터페이스를 사용하여 AppMeasurement을 구현할 수 있습니다. 이 태그 확장은 기본적으로 AppMeasurement 후드이므로 방문자를 식별하는 유사한 방법을 제공하며 방문자 ID 서비스에 대해 별도의 태그 확장이 필요합니다.

## 방문자 ID 서비스를 사용한 방문자 식별(권장)

Adobe Analytics 태그 확장을 사용하여 방문자 ID 서비스를 사용하려면 태그 속성에 Experience Cloud ID 서비스 태그 확장을 포함하십시오.

1. Adobe ID 자격 증명을 사용하여 [experience.adobe.com](https://experience.adobe.com)에 로그인합니다.
1. **[!UICONTROL 데이터 수집]** > **[!UICONTROL 태그]**(으)로 이동합니다.
1. 원하는 태그 속성을 찾습니다.
1. **[!UICONTROL 확장]**(으)로 이동한 다음 **[!UICONTROL 카탈로그]** 탭을 선택합니다.
1. **[!UICONTROL Experience Cloud ID 서비스]** 확장을 찾은 다음 **[!UICONTROL 설치]**&#x200B;를 선택합니다.

태그 확장은 IMS 조직 ID를 자동으로 가져오므로 추가 구성이 필요하지 않습니다.

## `s_vi` 쿠키를 사용하여 방문자 식별(권장되지 않음)

>[!IMPORTANT]
>
>Adobe에서는 방문자를 식별하기 위해 이 방법을 사용하지 않는 것이 좋습니다.

조직에서 방문자 ID 서비스 태그 확장을 사용하지 않는 경우 Adobe Analytics 태그 확장은 자체 방문자 ID 양식을 사용합니다. 방문자가 사이트에 처음 도착하면 확장 프로그램이 [`s_vi`](https://experienceleague.adobe.com/ko/docs/core-services/interface/data-collection/cookies/analytics) 쿠키를 확인합니다. 이 쿠키는 **[!UICONTROL 태그 확장을 구성]**&#x200B;할 때 **[!UICONTROL SSL 추적 서버]**(HTTPS용) 또는 [추적 서버](https://experienceleague.adobe.com/ko/docs/experience-platform/tags/extensions/client/analytics/overview)&#x200B;(HTTP용)와 일치하는 도메인에 설정됩니다.

* [관리 인증서 프로그램](https://experienceleague.adobe.com/ko/docs/core-services/interface/data-collection/adobe-managed-cert)에 참여하는 경우 추적 서버는 일반적으로 자사 도메인이므로 `s_vi` 쿠키를 자사 쿠키로 만듭니다.
* 관리 인증서 프로그램에 참여하지 않는 경우 추적 서버는 일반적으로 `adobedc.net`, `omtrdc.net` 또는 `2o7.net`의 하위 도메인이며 `s_vi` 쿠키를 타사 쿠키로 만듭니다. 최신 브라우저 개인 정보 보호 표준으로 인해 서드파티 쿠키는 대부분의 브라우저에서 거부됩니다. 거부되면 AppMeasurement은 대신 자사 대체 쿠키(`fid`)를 설정하려고 합니다.

[!UICONTROL SSL 추적 서버]를 올바르게 설정하면 추가 방문자 식별 조치가 필요하지 않습니다.

## `visitorID`을(를) 사용하여 방문자 식별(권장되지 않음)

>[!IMPORTANT]
>
>Adobe에서는 방문자를 식별하기 위해 이 방법을 사용하지 않는 것이 좋습니다.

**[!UICONTROL 방문자 ID]** 변수를 사용하면 조직에서 방문자를 식별하는 독립적인 제어를 완료할 수 있습니다. 데이터 요소를 사용하여 [!UICONTROL 방문자 ID]을(를) 설정하는 경우 다음 제한 사항에 유의하십시오.

* 모든 히트에는 단일 방문자로 계산되려면 동일한 [!UICONTROL 방문자 ID] 값이 있어야 합니다.
   * [!UICONTROL 방문자 ID] 데이터 요소를 생략한 모든 히트는 자동으로 다른 방문자 식별 방법을 사용하려고 시도하여 별도의 방문자로 취급됩니다.
   * 이전 히트와 다른 [!UICONTROL 방문자 ID] 값을 포함하는 모든 히트는 별도의 방문자로 처리됩니다.
   * Adobe에서는 서로 다른 방문자 ID를 함께 사용하여 히트를 연결하는 방법을 제공하지 않습니다.
* 공유 대상, Analytics for Target 및 고객 특성은 [!UICONTROL 방문자 ID]를 사용하여 식별된 방문자에서 지원되지 않습니다.

이 변수를 사용하는 구현 지침은 [`visitorID`](/help/implement/vars/config-vars/visitorid.md)을(를) 참조하십시오.
