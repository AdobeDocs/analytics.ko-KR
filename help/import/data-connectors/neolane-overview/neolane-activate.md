---
description: Adobe Data Connectors 구성 마법사를 사용하여 통합을 설정합니다.
title: 통합 활성화
uuid: 93c59f8e-3cf5-44c1-9a04-22460af93d5d
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8

---


# 통합 활성화{#activate-the-integration}

Adobe Data Connectors 구성 마법사를 사용하여 통합을 설정합니다.

1. Start [Data Connectors](https://docs.adobe.com/content/help/en/analytics/import/dataconnectors/getting-started-data-connectors.html) and click **[!UICONTROL + Add New]** to [add a new integration](https://docs.adobe.com/content/help/en/analytics/import/dataconnectors/getting-started-data-connectors.html).
1. In the **[!UICONTROL Show]** list, select **[!UICONTROL By Name]** and drag the [!DNL ~Partner~] integration to an empty plug-in slot.
1. 다음 표의 정보를 사용하여 통합 마법사를 완료합니다.

| 필드 | 설명 |
|--- |--- |
| 보고서 세트 | 이 통합에서 데이터를 수신하는 보고서 세트입니다. |
| 통합 이름 | Data Connectors가 보고서 세트의 활성 통합 목록에 표시하는 통합 이름을 지정합니다. |
| 클릭됨 | 이메일을 클릭한 총 횟수입니다. |
| 캠페인 ID | 고유한 메시지 ID를 저장합니다. 캠페인 변수에 저장되는 경우가 많습니다. |
| 열림 | 열린 총 이메일 수입니다. |
| 사용자 클릭 수 | 클릭한 사용자 수입니다. |
| 처리됨 | 처리된 총 이메일 수입니다. |
| Broadlog ID | 이 ID는 Neolane 시스템의 이메일 주소를 인코딩하거나 숫자로 표시한 것입니다. 이 &quot;Broadlog ID&quot;는 사이트의 다운스트림 방문자 행동(장바구니 Broadlog ID 포기, 구매 등)과 관련되어 있어 Neolane 시스템으로 다시 가져와 리마케팅 용도로 활용할 수 있습니다. |
| 예약됨 | 전송을 위해 예약된 이메일 메시지 수입니다. |
| 보냄 | 전송된 이메일 메시지 수입니다. |
| 총 바운스 수 | 전송 문제로 인해 수신자에게 전달되지 않은 이메일 메시지 수입니다. |
| 고유 클릭 수 | 개별적인 클릭 수입니다. |
| 고유 열기 수 | 개별적인 열기 수입니다. |
| 가입 해지됨 | 이메일 메시지를 열었지만 나중에 가입 해지 링크를 클릭하여 조직에서 발송하는 향후 이메일 메시지를 거부한 방문자 수입니다. |
| 세그먼트 | 이 통합은 파트너 세그먼트 섹션에 표시되는 파트너 정의 세그먼트를 만듭니다. 또한 통합에 포함할 기존 보고서 세트 수준 세그먼트를 선택할 수 있습니다. |
| 액세스 요청 | 권장 액세스 권한을 활성화합니다. |
| 데이터 수집 | s_code.js 플러그인을 이 통합에 대한 수집 모델로 사용하려면 **JavaScript 플러그인**&#x200B;을 선택합니다. 이 통합에 자동화된 수집 모델을 사용하려면 **자동화된 솔루션**&#x200B;을 선택한 다음 이 통합에 사용되는 고유 식별자를 지정합니다. 이 옵션을 선택하는 경우 이 통합에 사용되는 고유 식별자를 지정합니다. <ul><li>메시지 ID 쿼리 문자열 매개 변수: 이 값은 이메일 파트너가 랜딩 페이지 URL에 추가한 메시지 ID를 나타냅니다.</li><li>수신인 ID 쿼리 문자열 매개 변수: 이 값은 이메일 파트너가 랜딩 페이지 URL에 추가한 수신인 ID를 나타냅니다.</li></ul> |
| 대시보드 및 책갈피 생성 | 통합에 사용할 대시보드 및 책갈피를 자동으로 생성합니다. |
