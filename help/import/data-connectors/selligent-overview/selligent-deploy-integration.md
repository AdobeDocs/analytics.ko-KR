---
description: 이 통합 배포는 간단한 3단계 프로세스입니다.
title: 통합 배포
uuid: c578bf26-34c2-44ea-8e60-2990273f8659
translation-type: ht
source-git-commit: a02fb674ea71a05e085c8e9b2dc4460f62f2cd51

---


# 통합 배포{#deploying-the-integration}

이 통합 배포는 간단한 3단계 프로세스입니다.

## 통합 마법사 완료{#completing-the-integration-wizard}

통합을 활성화하려면 Data Connectors 인터페이스 내에서 Selligent 통합 마법사를 완료해야 합니다.

1. Adobe Experience Cloud 내에서 Data Connectors 영역으로 이동합니다.

   ![](assets/selligent-data_connectors.png)

1. **[!UICONTROL 통합 추가]**&#x200B;에서 Selligent 플러그인을 Adobe Experience Cloud에 끌어다 놓습니다.

   ![](assets/selligent-add_integration.png)

   그러면 Selligent Data Connector 통합이 열립니다.

1. **통합 설정**: 원하는 보고서 세트를 선택하고 **[!UICONTROL 통합 설정]**&#x200B;에서 통합 이름을 제공합니다.

1. **[!UICONTROL 사용자 지정 값]**&#x200B;에서 모든 Selligent 계정 관련 정보를 입력합니다.

   ![](assets/selligent-general_settings.png)

1. **변수 매핑**: 드롭다운 메뉴에서 적절하게 예약된 eVar 및 이벤트를 선택합니다.

   ![](assets/selligent-variables.png)

1. **데이터 설정**: 3개의 자동화된 **[!UICONTROL 파트너]** 세그먼트와 별도로 **[!UICONTROL 사용자 세그먼트]** 아래에서 고유한 세그먼트를 선택할 수 있습니다 .

1. 이 통합을 위해서 Selligent 계정에 몇 개의 데이터 포인트를 다운로드해야 할 수 있습니다. **[!UICONTROL 액세스 요청]**&#x200B;에서 동일한 항목에 대한 액세스 권한을 부여할 수 있습니다.
1. **[!UICONTROL 데이터 수집]**&#x200B;에서 자동화된 솔루션 또는 수동 솔루션(JavaScript 플러그인)을 선택하여 랜딩 페이지 URL에서 쿼리 문자열 매개 변수를 수집할 수 있습니다. 자동화된 솔루션을 선택하는 경우 메시지 ID(MID)와 수신자 ID(RID)에 대한 쿼리 문자열 매개 변수를 각각 입력합니다. JavaScript 플러그인은 Adobe 컨설턴트에게 문의하십시오.
1. **보고서 설정**: **[!UICONTROL 대시보드 생성]**&#x200B;에서 이 상자를 선택하면 Selligent 대시보드가 자동으로 생성됩니다.

   ![](assets/selligent-report_settings.png)

1. 통합 요약을 검토하고 **[!UICONTROL 활성화]**&#x200B;를 클릭합니다.

## Selligent의 구성{#configuration-within-selligent}

Adobe Analytics 내에서 통합이 활성화되는 즉시 Selligent 측에서 자동 구성이 활성화됩니다.

모든 이메일을 추적하는 추적기가 생성되었습니다. 특정 도메인으로 제한하려면 추적기 구성을 업데이트하십시오.

URL에서 Adobe Analytics의 추적 매개 변수를 맨 앞으로 이동하는 것이 좋습니다. 이렇게 하면 Adobe 처리 규칙이 랜딩 페이지 URL에서 매개 변수를 선택하게 됩니다. 아래 표시된 확인란을 선택하여 추적을 활성화합니다.

![](assets/selligent-tracker.png)

## 통합 확인{#verifying-the-integration}

모든 배포 단계가 완료되면 통합이 성공적으로 데이터를 전송하고 있는지 확인할 수 있습니다.

 데이터 교환을 시작하려면 며칠이 걸립니다. 통합을 활성화한 후 Selligent에 문의하십시오.

### 통합 활동 로그 {#section-927e270495db479fba9578915d9ae9c9}

Data Connectors 내에서 Selligent 통합으로 이동합니다. **[!UICONTROL 지원]** 탭에 지표 데이터를 가져왔습니다 및/또는 분류 데이터를 가져왔습니다와 같은 이벤트가 표시되어야 합니다.

![](assets/selligent-verifying.png)

### 보고 데이터 {#section-ebd481a162324e66bd6dc8cb4b8d2424}

적절한 지표를 사용하여 Selligent 메시지 보고서를 봅니다.

1. Adobe Experience Cloud의 Report &amp; Analytics로 이동합니다.
1. 적절한 보고서 세트를 선택합니다.
1. **[!UICONTROL 사용자 지정 전환]**&#x200B;에서 **[!UICONTROL 메시지 ID 보고서]**&#x200B;를 선택하고 **[!UICONTROL 메시지 ID/메시지 이름]**&#x200B;을 선택합니다.
