---
description: 서버 측 전달은 Analytics의 데이터를 다른 Experience Cloud 솔루션에 실시간으로 공유하려는 고객을 위해 설계되었습니다. 이 기능이 활성화되어 있을 때 서버 측 전달을 사용하면 Analytics에서 데이터를 다른 Experience Cloud 솔루션에 푸시하고 데이터 수집 프로세스 중에 해당 솔루션으로 데이터를 Analytics에 푸시할 수 있습니다.
solution: Audience Manager
title: 서버 측 전달 개요
uuid: 22ddbde5-6805-4eba-8f82-62772644dcaa
translation-type: ht
source-git-commit: 327fdfd6a6d6bfe1c7bae9825fc8812b5ac7d095

---


# 서버 측 전달 개요

서버 측 전달은 Analytics의 데이터를 다른 Experience Cloud 솔루션에 실시간으로 공유하려는 고객을 위해 설계되었습니다. 이 기능이 활성화되어 있을 때 서버 측 전달을 사용하면 Analytics에서 데이터를 다른 Experience Cloud 솔루션에 푸시하고 데이터 수집 프로세스 중에 해당 솔루션으로 데이터를 Analytics에 푸시할 수 있습니다.

다음과 같은 이유로 데이터 수집 시 서버 측 전달이 향상됩니다.

* 페이지 호출이 줄어듭니다. 서버 측 전달을 사용하면 DIL이 Analytics에서 전달되므로 [!DNL Audience Manager] 고객은 더 이상 데이터 수집에 DIL을 사용할 필요가 없습니다. DIL을 제거하면 `"/event"` 호출이 제거됩니다. 호출이 줄어들면 페이지 로딩 시간이 단축되므로 고객은 사이트에서 더 나은 경험을 하게 됩니다.
* Experience Cloud 솔루션 간 데이터 공유를 활용할 수 있습니다.
* Audience Manager 코드 구현 및 배포에 대한 우수 사례를 준수합니다.

>[!TIP]
>
>Analytics를 사용하는 현재의 Audience Manager 고객은 서버 측 전달로 마이그레이션해야 합니다. 새로운 Adobe Analytics 및 Audience Manager 고객은 기본 데이터 수집 및 전송 방법으로 서버 측 전달(DIL 대신)을 구현해야 합니다.

>[!IMPORTANT]
>EU 쿠키 준수 규정에 따라, 데이터 컨트롤러(Analytics 고객)에게는 사전 동의한 데이터를 Adobe Analytics로 제한하여 서버 측에서 AAM(Adobe Audience Manager)으로 전달되지 않도록 하는 옵션이 제공됩니다. 새 구현 컨텍스트 변수를 사용하여 동의를 받지 못한 히트에 플래그를 지정할 수 있습니다. 변수를 설정하면 동의를 받을 때까지 이러한 히트가 AAM에 전송되지 않습니다. 자세한 내용은 [GDPR_ePrivacy 준수 및 서버 측 전달](/help/admin/admin/c-server-side-forwarding/ssf-gdpr.md)을 참조하십시오.

서버측 전달을 구현하는 측면에서 조직의 위치를 이해하려면 다음 유효성 검사 절차를 수행하십시오.

## ![step1_icon.png 이미지](assets/step1_icon.png) ECID 서비스 구현 확인

[Analytics 추적 요청](https://docs.adobe.com/content/help/ko-KR/id-service/using/implementation/test-verify.html)을 검사하여 Experience Cloud ID(ECID) 서비스가 구현되었는지 확인합니다.

요청 탭에서 ECID 값이 설정되어 있는지 확인하십시오. 이는 ID 서비스가 올바르게 구현되었음을 나타내며, 서버측 전달의 필수 조건입니다.

* ECID 값이 표시되면 2단계로 진행합니다.
* ECID 값이 표시되지 않으면 2단계로 진행하기 전에 [ID 서비스를 구현](https://docs.adobe.com/content/help/ko-KR/id-service/using/implementation/implementation-guides.html)합니다.

## ![step2_icon.png 이미지](assets/step2_icon.png) 서버 측 전달 구현 버전 확인

[Analytics 추적 요청을 검사](/help/admin/admin/c-server-side-forwarding/ssf-verify.md)하여 이미 구현된 서버 측 전달 버전이 있는지 확인합니다.

응답에 Audience Manager 데이터가 포함되어 있는지 &quot;응답&quot; 탭에서 확인합니다. 만약

* **&quot;postbacks&quot; 또는 &quot;dcs_region&quot;과 같은 항목을 포함하는 Audience Manager의 JSON 응답**&#x200B;이 표시된다면 이미 어떤 형태의 서버 측 전달이 활성화되어 있는 것입니다. 3단계로 진행합니다.
* **&quot;status&quot;:&quot;SUCCESS&quot;**&#x200B;가 표시된다면, 고객 관리 모듈이 구현되어 있지만 서버 측 전달이 제대로 구성되지 않은 것입니다. 3단계로 진행합니다.
* **2 x 2 이미지**&#x200B;가 표시된다면, 서버 측 전달 또는 고객 관리 모듈이 구현되어 있지 않습니다. 이 문제를 해결하려면 다음을 수행하십시오.

   * **DIL이 있는 AAM 고객**: 다음 두 항목을 긴밀하게 편성하십시오.

      1. DIL 코드를 제거하고 [고객 관리 모듈](https://docs.adobe.com/content/help/ko-KR/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/audience-management-module.html) 페이지 코드를 설치합니다.
      1. 3단계에서 설명한 대로 Analytics 관리 UI에서 서버 측 전달을 활성화합니다. DIL 코드를 제거하기 전에 이 설정을 활성화하면 데이터가 중복되고 Audience Manager에 대해 추가 청구된 서버 호출이 생성됩니다.
   * **새 AAM 고객** - [고객 관리 모듈](https://docs.adobe.com/content/help/ko-KR/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/audience-management-module.html) 페이지 코드를 설치하고 3단계로 진행합니다. 3단계에서 서버 측 전달 기능이 켜지기 전까지는 데이터가 Audience Manager에게 전송되지 않습니다.


## ![step3_icon.png 이미지](assets/step3_icon.png) 보고서 세트의 서버 측 전달 구현 확인

이전 추적 서버 접근 방식이 아니라, 보고서 세트 수준에서 서버 측 전달을 구현했는지 확인하십시오.

Analytics에서 어떤 데이터가 공유되는지를 더 세부적으로 제어할 수 있으므로 이전 추적 서버 접근 방식보다 보고서 세트 수준의 서버 측 전달이 권장됩니다. 이것은 이 Audience Analytics 통합을 위한 선행 조건이기도 합니다.

**Analytics** > **관리자** > **보고서 세트** > (**보고서 세트** 선택) > **설정 편집** > **일반** > **서버 측 전달**&#x200B;로 이동합니다. 확인란이

* **비활성**(선택을 할 수 없거나 메뉴가 존재하지 않음): 선택한 보고서 세트가 IMS 조직에 매핑되어 있지 않습니다. 해당 보고서 세트가 [보고서 세트 매핑 UI](https://docs.adobe.com/content/help/ko-KR/core-services/interface/about-core-services/report-suite-mapping.html)를 사용하여 적절한 Experience Cloud 조직에 매핑되어 있는지 확인하십시오.
* **비활성화됨** 상태라면, 새 서버 측 전달이 설정되어 있지 않았습니다. 페이지의 컨텐츠를 읽은 다음, 기능을 활성화하십시오.
* **활성화됨** 상태라면, 사용자는 새 서버 측 전달을 위해 프로비저닝되었습니다. 이 Audience Analytics 통합을 설정할 수도 있습니다.

>[!NOTE] 3개의 단계가 모두 완료되기 전까지는 [Audience Manager](https://docs.adobe.com/content/help/ko-KR/audience-manager/user-guide/aam-home.html) 또는 [Audiences](https://docs.adobe.com/content/help/ko-KR/core-services/interface/audiences/audience-library.html)와 같은 다른 Experience Cloud 솔루션에 데이터가 표시되지 않습니다. 활성화한 후 이 설정이 적용되는 데에는 몇 시간이 걸립니다.

