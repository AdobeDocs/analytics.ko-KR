---
description: 프로젝트 구성 요소가 특정 임계값에 도달하면 경고를 받습니다.
title: 경고 빌더 (Analysis Workspace)
feature: Alerts
role: User, Admin
exl-id: aae28c90-bfdf-49ff-bd38-c9ef63880bf4
source-git-commit: d48f74d4fa642e34de601466737f16fc228a8199
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 43%

---

# 경고 만들기

>[!NOTE]
>
>지능형 경고는 Adobe Analytics Prime 및 Adobe Analytics Ultimate 고객만 사용할 수 있습니다.

Adobe Analytics의 지능형 경고(또는 &quot;경고&quot;)를 사용하면 데이터에서 비정상 이벤트가 발생할 때 즉시 알림을 받을 수 있습니다.

지능형 경고에 대한 자세한 개요 정보는 다음을 참조하십시오. [지능형 경고 개요](/help/analyze/analysis-workspace/c-intelligent-alerts/intellligent-alerts.md).

경고를 만들려면 다음 작업을 수행하십시오.

1. 경고 빌더에 액세스하여 경고 만들기를 시작합니다. 다음 방법 중 하나로 경고 빌더에 액세스할 수 있습니다.

   * Analysis Workspace에서 프로젝트를 연 다음 을 선택합니다. **[!UICONTROL 구성 요소]** > **[!UICONTROL 경고 만들기]**.
   * Analysis Workspace에서 프로젝트를 연 다음 다음 단축키를 사용합니다.

     `ctrl (or cmd) + shift + a`
   * Analysis Workspace에서 프로젝트를 열고 자유 형식 테이블에서 하나 이상의 라인 항목을 선택한 다음 마우스 오른쪽 단추를 클릭하고 을 선택합니다 **[!UICONTROL 선택 항목으로 경고 만들기]**.

     이렇게 하면 즉시 경고 빌더가 미리 채워져서 올바른 지표와 필터로 경고를 만듭니다.
   * Adobe Analytics에서 **[!UICONTROL 구성 요소]** > [!UICONTROL **경고**] > **[!UICONTROL 새 경고 만들기]**.

   경고 빌더가 표시됩니다. 이 인터페이스는 Analytics에 세그먼트 또는 계산된 지표를 만든 사용자에게 익숙합니다.

   ![](assets/alert-builder.png)

1. 다음 옵션을 지정하여 경고를 구성합니다.

   | 옵션 | 설명 |
   |---------|----------|
   | [!UICONTROL **제목**] | 경고 이름을 지정합니다. 경고 이름에는 보고서 또는 지표 임계값 이름이 포함될 수 있습니다. |
   | [!UICONTROL **설명(선택 사항)**] | 경고에 대한 설명을 지정합니다. |
   | [!UICONTROL **시간 세부 기간**] | 지표를 확인할 빈도(일별, 주별 또는 월별)를 선택합니다.<p><b>참고:</b>사용자 지정 달력이 있는 데이터 보기의 경우 경고 빌더에서 월별 세부기간을 지원하지 않습니다.<!--true?--></p> |
   | [!UICONTROL **수신자**] | 경고를 전송할 대상을 지정합니다. 경고는 Analytics 사용자, Analytics 그룹, 원시 이메일 주소 또는 전화번호에 보낼 수 있습니다.<p><b>중요 사항:</b>전화번호 앞에는 &quot;+&quot;와(과) [국가 코드](https://countrycode.org/).</p><p>경고가 트리거되면 사용자가 받게 되는 이메일은 다음과 유사합니다.</p><p>![](assets/alerts-email.PNG)</p> |
   | [!UICONTROL **만료 날짜**] | 경고가 만료될 날짜 및 시간을 설정합니다. |
   | [!UICONTROL **다음의 경우에 경고 보내기**] | [!UICONTROL **다음 지표 중 하나 이상의 트리거**]: 여기에 지표(계산된 지표 포함)를 끌어다 놓아 경고에 대한 트리거를 만듭니다.<p>An **&quot;호환되지 않는 구성 요소&quot;** 경고에 뜬 모든 지표, 차원 또는 세그먼트가 현재 선택된 데이터 보기와 호환하지 않을 경우 메시지가 표시됩니다.</p><p>경고를 설정하기 전에 지표가 초과되는 임계값을 결정합니다. 이 값을 임계값으로 설정한 후 다음 조건 중 하나로 설정할 수 있습니다.</p><ul><li>예외 항목이 있음</li><li>예외 항목이 예상 이상임</li><li>예외 항목이 예상 미만임</li><li>위 또는 같음</li><li>아래 또는 같음</li><li>변경</li><li>90%, 95%, 99%, 99.75% 및 99.9%의 임계값을 설정할 수 있습니다.</li></ul><p>[!UICONTROL **이 모든 필터 사용**]: 세그먼트 또는 차원을 드래그하여 놓아 필터를 추가합니다. 예를 들어 &quot;모바일 디바이스만&quot; 세그먼트를 추가한다는 것은 모바일 디바이스에 대해서만 규칙이 트리거됨을 의미합니다. AND 문을 사용하여 필터를 추가할 수 있습니다. 톱니바퀴 아이콘을 클릭하여 AND 또는 OR 규칙을 추가할 수 있습니다.</p><p>다음을 참조하십시오 [지능형 경고 - 활용 사례](/help/analyze/analysis-workspace/c-intelligent-alerts/alerts-use-cases.md) 예를 들어 사용 사례를 들 수 있습니다.</p> |
   | [!UICONTROL **미리보기**] | 대화형 경고 미리보기에서는 경고가 과거의 경험을 기반으로 얼마나 자주 표시되는지를 근사적으로 보여 줍니다.<p>예를 들어 시간 세부 기간을 매일로 설정하는 경우, 미리보기에서는 경고가 지난 30 또는 31일 동안 특정 지표 x 배수에 대해 트리거됨을 알 수 있습니다.</p><p>너무 많은 경고가 트리거될 것 같으면 [경고 관리자](/help/analyze/analysis-workspace/c-intelligent-alerts/alert-manager.md)에서 임계값을 조정할 수 있습니다.</p><p>![](assets/alert_preview.png)</p> |

1. [!UICONTROL **저장**]&#x200B;을 선택합니다.
