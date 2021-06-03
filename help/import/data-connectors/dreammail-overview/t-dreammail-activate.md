---
description: Adobe Data Connectors 구성 마법사를 사용하여 통합을 설정합니다.
title: 통합 활성화
uuid: 9084b691-291d-49f7-9fa4-abda507e060d
exl-id: b0d6849b-975a-4476-a2d3-36abeee12273
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 96%

---

# 통합 활성화{#activate-the-integration}

Adobe Data Connectors 구성 마법사를 사용하여 통합을 설정합니다.

1. [Data Connectors](https://experienceleague.adobe.com/docs/analytics/import/dataconnectors/getting-started-data-connectors.html)를 시작하고 **[!UICONTROL + 새로 추가]**&#x200B;를 클릭하여 [새 통합을 추가할 수 있습니다](https://experienceleague.adobe.com/docs/analytics/import/dataconnectors/getting-started-data-connectors.html).
1. **[!UICONTROL 표시]** 목록에서 **[!UICONTROL 이름별]**&#x200B;을 선택하고 [!DNL ~Partner~] 통합을 빈 플러그인 슬롯으로 드래그합니다.
1. 다음 표의 정보를 사용하여 통합 마법사를 완료합니다.

| 필드 | 설명 |
|--- |--- |
| 보고서 세트 | 이 통합에서 데이터를 수신하는 보고서 세트입니다. |
| 통합 이름 | Data Connectors가 보고서 세트의 활성 통합 목록에 표시하는 통합 이름을 지정합니다. |
| 통합 UUID | DreamMail 통합 UUID를 지정합니다. |
| 클라이언트 이름 | DreamMail 클라이언트 이름을 지정합니다. |
| 사이트 이름 | DreamMail 사이트 이름을 지정합니다. |
| 바운스백 | 전송 문제로 인해 수신자에게 전달되지 않은 이메일 메시지 수입니다. |
| 배달됨 | 배달에 성공한 메시지 수입니다. |
| 배달 오류 | 메시지 배달이 실패했습니다. |
| HTML 열기 | 이메일 메시지를 연 방문자 수입니다. |
| 유효하지 않음 | 잘못된 이메일 주소 수입니다. |
| 캠페인 | 마케팅 캠페인 ID. |
| 전달 | 클릭됨 이벤트를 사용하면 이메일 메시지를 클릭한 방문자 수를 볼 수 있습니다. |
| Email eVar | DreamMail 시스템의 이메일 주소입니다. 이 &quot;이메일 eVar&quot;는 사이트의 다운스트림 방문자 행동(장바구니 포기, 구매 등)과 관련되어 있어 DreamMail 시스템으로 다시 가져와 리마케팅 용도로 활용할 수 있습니다. |
| Spotlight 이벤트 | 리마케팅 세그먼트에서 내보낼 수 있는 이벤트입니다. |
| Spotlight 구매 | 리마케팅 세그먼트에서 내보낼 수 있는 이벤트입니다. |
| Spotlight 값 | 리마케팅 세그먼트에서 내보낼 수 있는 매출 이벤트입니다. |
| 총 클릭 수 | 클릭됨 이벤트를 사용하면 이메일 메시지를 클릭한 방문자 수를 볼 수 있습니다. |
| 세그먼트 | 이 통합은 파트너 세그먼트 섹션에 표시되는 파트너 정의 세그먼트를 만듭니다. 또한 통합에 포함할 기존 보고서 세트 수준 세그먼트를 선택할 수 있습니다. |
| 액세스 요청 | 권장 액세스 권한을 활성화합니다. |
| 데이터 수집 | s_code.js 플러그인을 이 통합에 대한 수집 모델로 사용하려면 **JavaScript 플러그인**&#x200B;을 선택합니다(참조). 이 통합에 자동화된 수집 모델을 사용하려면 **자동화된 솔루션**&#x200B;을 선택한 다음 이 통합에 사용되는 고유 식별자를 지정합니다. 이 옵션을 선택하는 경우 이 통합에 사용되는 고유 식별자를 지정합니다.<ul><li>메시지 ID 쿼리 문자열 매개 변수: 이 값은 이메일 파트너가 랜딩 페이지 URL에 추가한 메시지 ID를 나타냅니다.</li><li>수신인 ID 쿼리 문자열 매개 변수: 이 값은 이메일 파트너가 랜딩 페이지 URL에 추가한 수신인 ID를 나타냅니다.</li></ul> |
| 대시보드 및 책갈피 생성 | 통합에 사용할 대시보드 및 책갈피를 자동으로 생성합니다. |
