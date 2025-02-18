---
description: Analysis Workspace에서 경고를 사용합니다.
title: 경고 빌더 개요
feature: Alerts
exl-id: 82e51357-4a32-4db1-bc56-95a72dbaa1be
source-git-commit: 966bd9a05e6c344a62ce3f0b12df8a99ff3d7ece
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 25%

---

# 경고 만들기 {#create-alerts}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_alerts_timegranularity"
>title="시간 세부 기간"
>abstract="시간 세부 기간은 경고를 확인하는 빈도와 포함 항목 모두를 나타냅니다."

<!-- markdownlint-enable MD034 -->

>[!NOTE]
>
>예외 항목 탐지를 사용하는 경고(_지능형 경고_)는 Adobe Analytics Prime 또는 Ultimate 패키지를 사용하는 조직에서만 사용할 수 있습니다.

Adobe Analytics의 경고를 사용하면 변경된 백분율이나 특정 데이터 포인트에 따라 알림을 받을 수 있습니다. Adobe Analytics 패키지에 따라 예외 항목 임계값에 따라 경고를 트리거할 수도 있습니다. 서버 호출 사용량 경고는 Analytics 관리자만 사용할 수 있는 다른 종류의 경고입니다. 이러한 경고는 서버 호출 사용량 및 약정 데이터의 초과 위험이나 발생을 알려줍니다. 자세한 내용은 [서버 호출 사용량 경고](/help/admin/admin/c-server-call-usage/scu-alerts.md)를 참조하십시오.

경고에 대한 자세한 개요 정보는 [경고 개요](/help/components/c-alerts/intellligent-alerts.md)를 참조하십시오.

경고를 만들려면 다음 작업을 수행하십시오.

1. 경고 빌더에 액세스하여 경고 만들기를 시작합니다. 다음 방법 중 하나로 경고 빌더에 액세스할 수 있습니다.

   * Analysis Workspace에서 프로젝트를 연 다음 **[!UICONTROL 구성 요소]** > **[!UICONTROL 경고 만들기]**&#x200B;를 선택합니다.
   * Analysis Workspace에서 프로젝트를 연 다음 ***ctrl(또는 cmd) + shift + a*** 단축키를 사용합니다.
   * Analysis Workspace에서 프로젝트를 열고 자유 형식 테이블에서 하나 이상의 라인 항목을 선택한 다음 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL 선택 항목으로 경고 만들기]**&#x200B;를 선택합니다. 이 작업을 수행하면 즉시 경고 빌더가 미리 채워져서 올바른 지표와 필터로 경고가 만들어집니다.
   * 경고 관리자](/help/components/c-alerts/alert-manager.md#create-alerts)에서 경고 [을(를) 만듭니다.

   경고 빌더가 표시됩니다. 이 인터페이스는 Analytics에서 세그먼트 또는 계산된 지표를 작성하는 인터페이스에 익숙합니다.

   ![](assets/alert-builder.png)

1. 다음 옵션을 지정하여 경고를 구성합니다.

   | 옵션 | 설명 |
   |---------|----------|
   | [!UICONTROL **제목**] | 경고 이름을 지정합니다. 경고 이름에는 보고서 또는 지표 임계값 이름이 포함될 수 있습니다. |
   | [!UICONTROL **설명(선택 사항)**] | 경고에 대한 설명을 지정합니다. |
   | [!UICONTROL **시간 세부기간**] | 지표를 확인할 빈도를 시간별, 일별, 주별 또는 월별 중에서 선택합니다.<p><b>참고:</b> 사용자 지정 달력이 있는 보고서 세트의 경우 경고 빌더에서 월별 세부기간을 지원하지 않습니다.<!--true?--></p> |
   | [!UICONTROL **수신자**] | 경고를 전송할 대상을 지정합니다. 경고는 Analytics 사용자, Analytics 그룹, 원시 이메일 주소 또는 전화번호에 보낼 수 있습니다.<p><b>중요:</b> 전화 번호 앞에는 `+`과(와) [국가 코드](https://countrycode.org/)가 있어야 합니다.</p><p>경고가 트리거되면 사용자가 받게 되는 이메일은 다음과 유사합니다.</p><p>![](assets/alerts-email.PNG)</p> |
   | [!UICONTROL **만료 날짜**] | 경고가 만료될 날짜 및 시간을 설정합니다. |
   | [!UICONTROL **다음 경우에 경고 보내기**] | [!UICONTROL **다음 지표 트리거 중 하나**]: 여기에 지표(계산된 지표 포함)를 끌어다 놓아 경고에 대한 트리거를 만듭니다.<p>경고에 있는 일부 지표, 차원 또는 세그먼트가 현재 선택한 데이터 보기와 호환하지 않을 경우 **&quot;호환되지 않는 구성 요소&quot;** 메시지가 표시됩니다.</p><p>경고를 설정하기 전에 지표가 초과되는 임계값을 결정합니다. 이 값을 임계값으로 설정한 후 다음 조건 중 하나로 설정할 수 있습니다.</p><ul><li>예외 항목이 있음</li><li>예외 항목이 예상 이상임</li><li>예외 항목이 예상 미만임</li><li>위 또는 같음</li><li>아래 또는 같음</li><li>변경</li><li>90%, 95%, 99%, 99.75% 및 99.9%의 임계값을 설정할 수 있습니다.</li></ul><p>[!UICONTROL **다음 필터 사용**]: 세그먼트 또는 차원을 끌어서 놓아 필터를 추가합니다. 예를 들어 &quot;모바일 디바이스만&quot; 세그먼트를 추가한다는 것은 모바일 디바이스에 대해서만 규칙이 트리거됨을 의미합니다. AND 문을 사용하여 필터를 추가할 수 있습니다. 톱니바퀴 아이콘을 클릭하여 AND 또는 OR 규칙을 추가할 수 있습니다.</p><p>예를 들어 [경고 - 사용 사례](/help/components/c-alerts/alerts-use-cases.md)를 참조하십시오.</p> |
   | [!UICONTROL **미리보기**] | 대화형 경고 미리보기에서는 경고가 과거의 경험을 기반으로 얼마나 자주 표시되는지를 근사적으로 보여 줍니다.<p>예를 들어 시간 세부기간을 매일로 설정하는 경우, 미리보기에서는 경고가 지난 30 또는 31일 동안 특정 지표 x 배수에 대해 트리거됨을 알 수 있습니다. 미리보기 근사화 윈도우는 경고 주파수 설정에 의해 설정된다. 일별 경고 빈도의 경우 미리보기 창은 이전 30일과 비슷합니다. 주별 경고 빈도의 경우 미리보기 창은 지난 12주와 비슷합니다. 월별 경고 빈도의 경우 미리보기 창은 이전 12개월과 비슷합니다.</p><p>너무 많은 경고가 트리거되는 경우 [경고 관리자](/help/components/c-alerts/alert-manager.md)에서 임계값을 조정할 수 있습니다.</p><p>![](assets/alert_preview.png)</p> |

1. [!UICONTROL **저장**]&#x200B;을 선택합니다.
