---
description: 'null'
title: 통합 배포
uuid: ebb385ca-7bfb-4cd3-9ff6-a5f5a52db5c9
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 통합 배포{#deploying-the-integration}

이 통합 배포는 Adobe 통합 마법사를 완료하고 플러그인 코드(JavaScript)를 배포하고 통합을 확인하는 간단한 과정으로 이루어집니다.

## Adobe 통합 마법사 완료{#complete-the-adobe-integration-wizard}

통합을 활성화하려면 데이터 커넥터 인터페이스에서 구성 마법사를 완료합니다.

1. Adobe Experience Cloud에 로그인합니다.
1. 로 **[!UICONTROL Data Connectors]**&#x200B;이동합니다.
1. Kampyle 통합 마법사를 시작합니다.
1. 원하는 보고서 세트를 선택하고 통합 이름을 제공합니다.
1. 다음 항목을 구성합니다.
   1. **[!UICONTROL Email address]**: 기본 연락처의 이메일 주소.
   1. **[!UICONTROL Description]** (선택 사항):이 통합 설정에 대한 설명입니다.
   1. **[!UICONTROL Kampyle Key]**:> 아래의 Kampyle 애플리케이션에서 이 키를 **[!UICONTROL Feedback Form]** 찾습니다 **[!UICONTROL Feedback Form Customization]**.
   1. **[!UICONTROL Tracking Server]**:Adobe Analytics 데이터를 추적하는 데 사용하는 추적 서버 값입니다.
   1. **[!UICONTROL Tracking Server Secure]**:보안/https 트래픽에 대해 추적 서버가 다른 경우 여기에서 해당 설정을 제공하십시오.
1. Configure the following **[!UICONTROL Variable Mappings]** items:
   1. **[!UICONTROL Kampyle Feedback ID]**: 보고서 세트에서 사용 가능한 eVar 변수를 선택합니다
   1. **[!UICONTROL Feedback Grade]**:보고서 세트에서 사용 가능한 성공 이벤트(&quot;카운터&quot; 유형)를 선택합니다.
   1. **[!UICONTROL Feedback Items]**:보고서 세트에서 사용 가능한 성공 이벤트(&quot;카운터&quot; 유형)를 선택합니다.
   1. **[!UICONTROL Feedback with Grade]**:보고서 세트에서 사용 가능한 성공 이벤트(&quot;카운터&quot; 유형)를 선택합니다.
1. Kampyle 통합 대시보드를 자동으로 만들려면 이 확인란을 선택합니다(권장).
1. Review all configuration items and click **[!UICONTROL Activate Now]**.

## 통합 구성 개체 배포{#deploy-the-integration-configuration-object}

통합 마법사를 완료한 후 통합 구성 개체를 웹 속성에 배포합니다. 대부분의 경우 통합 구성 개체를 배포하는 가장 쉬운 방법은 Adobe Analytics 배포 코드에 통합 구성 개체를 포함하는 것입니다.

>[!NOTE] Adobe Experience Platform Launch를 사용하는 경우 해당 도구를 통해 통합 구성 개체를 쉽게 추가할 수 있습니다.

1. Navigate to the **[!UICONTROL Resources]** > **[!UICONTROL Support]** tab of the integration.
1. 리소스를 다운로드하고 저장합니다. **[!UICONTROL Kampyle Integration Code (JS)]** 코드는 다음과 유사합니다.

   ```
   /* Kampyle:  Integration configuration settings */
     window.k_sc_param = { "version":1.1 }
   ```

1. 다음 방법 중 하나를 사용하여 코드를 배포합니다.

   * Adobe Experience Platform Launch를 사용하십시오.
   * Adobe Analytics 배포를 유지하는 조직 리소스에 코드를 전달할 수 있습니다.

## 통합 확인{#verify-the-integration}

통합이 두 가지 검사를 완료하여 데이터를 성공적으로 전송하는지 확인합니다.

### 통합 활동 로그 {#section-0472df9180db4f218db5f6040cab07af}

View your Kampyle integration setup within the Adobe Experience Cloud by navigating to **[!UICONTROL Support]** > **[!UICONTROL Integration Activity Log]**. Under the **[!UICONTROL Data In]** tab, you should see entries stating that classification data was successfully imported.

>[!NOTE] 로그 항목은 일반적으로 배포 후 24시간 이내에 표시됩니다.

![통합 작업 로그](assets/integration_activity_log.png)

### Adobe 보고 데이터 {#section-1ae9f0a5e6bc40988478ff55aefd56ac}

적절한 메뉴 구조 내에서 Kampyle 보고로 이동하여 Adobe Analytics에서 Kampyle 피드백 보고서를 봅니다.

>[!NOTE] 통합 피드백 양식이 제출물을 적극적으로 수신하고 있다고 가정할 경우 보고 데이터는 성공적인 배포 후 24-48시간 이내에 표시되어야 합니다.

![Adobe 보고 데이터](assets/adobe_reporting_data.png)
