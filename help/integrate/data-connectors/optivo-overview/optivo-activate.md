---
description: Adobe 데이터 커넥터 구성 마법사를 사용하여 통합을 설정합니다.
seo-description: Adobe 데이터 커넥터 구성 마법사를 사용하여 통합을 설정합니다.
seo-title: 통합 활성화
title: 통합 활성화
uuid: 3 B 2 ACDB 8-9 A 1 F -4 F 17-92 F 2-6 A 3780 A 8 F 626
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: d10546972c03efae1bc365b7391000a40a79b0a4

---


# Activate the Integration{#activate-the-integration}

Adobe 데이터 커넥터 구성 마법사를 사용하여 통합을 설정합니다.

1. [데이터 커넥터를](https://marketing.adobe.com/resources/help/en_US/genesis/c_overview.html) 시작하고 **[!UICONTROL + 새로]** 추가를 클릭하여 새 통합을 [추가합니다](https://marketing.adobe.com/resources/help/en_US/genesis/t_add_integration.html).
1. **[!UICONTROL [표시]** ] 목록에서 **[!UICONTROL 이름별로]** 선택하고 [!DNL ~파트너~] 통합을 빈 플러그인 슬롯으로 끕니다.
1. 다음 표의 정보를 사용하여 통합 마법사를 완료합니다.

| 필드 | 설명 |
|--- |--- |
| 보고서 세트 | 이 통합에서 데이터를 받는 보고서 세트입니다. |
| 통합 이름 | 보고서 세트의 활성 통합 목록에 데이터 커넥터가 표시되는 통합 이름을 지정합니다. |
| 이메일 주소 | 통합 관련 정보를 수신할 이메일 주소를 입력합니다. |
| 계정 ID | 이메일 서비스 공급자가 조직에 할당하는 고유 식별자입니다. 이메일 캠페인 데이터를 요청할 때 사용됩니다 (예: # sent, # opened, # clicked 등). 방문자 세그먼트를 이메일 서비스 공급자에게 보내는 방법 |
| Recipient ID | 이 ID는 optivo® broadmail 시스템의 이메일 주소를 인코딩된 또는 숫자 표현으로 표현한 것입니다. 이 "수신자 ID" 는 사이트의 다운스트림 방문자 행동과 관련이 있습니다 (장바구니 포기, 구매 등). Optivo® broadmail 시스템으로 가져와 리마케팅용으로 활용할 수 있습니다. |
| 메시지 ID | (필수) 고유한 메일링 ID를 저장합니다. These classification dimensions are created by the Data Connectors wizard for the Message ID: a)**Campaigns**: Campaigns associated with the message. b)**Channel**: The channel of transmission, this is constantly "optivo broadmail". c)**Country Code**: This field contains the country code of the origin sender country. 상수 "de" 입니다. d) **Delivery Tool**: Method of transmission, always "Email". e) **Message Name**: The name of the mailing, as it is configured in optivo® broadmail. f) **Start Date**: Timestamp of the start of this mailing. |
| 게시물 클릭 시간 | (필수) 수신자가 메일링에서 링크를 클릭한 후 수신자 동작에 대한 정보를 Optivo® Broadmail로 전송하는 데 필요합니다. |
| 게시물 클릭 제품 | (필수) 수신자가 메일링에서 링크를 클릭한 후 수신자 동작에 대한 정보를 Optivo® Broadmail로 전송하는 데 필요합니다. |
| 게시물 클릭 동작 | (필수) 수신자가 메일링에서 링크를 클릭한 후 수신자 동작에 대한 정보를 Optivo® Broadmail로 전송하는 데 필요합니다. |
| 하드 바운스 | (필수) 이메일 시스템에서 가져온 하드 바운스 데이터를 저장하는 Adobe Analytics 이벤트를 지정합니다. 받는 사람에게 배달되지 않고 영구적으로 배달되지 않는 이메일 메시지 수. |
| 부드러운 바운스 | (필수) 이메일 시스템에서 가져온 소프트 바운스 데이터를 저장하는 Adobe Analytics 이벤트를 지정합니다. 배달 문제로 인해 수신자에게 배달되지 않은 이메일 메시지 수입니다. |
| 클릭함 | (필수) 이메일 시스템에서 가져온 이메일 클릭 데이터를 저장하는 Adobe Analytics 이벤트를 지정합니다. 클릭한 이벤트를 통해 이메일 메시지를 클릭한 방문자 수를 확인할 수 있습니다. |
| 열림 | (필수) 이메일 시스템에서 가져온 데이터를 이메일로 저장하는 Adobe Analytics 이벤트를 지정합니다. 열린 이벤트를 통해 이메일 메시지를 연 방문자 수를 볼 수 있습니다. |
| sent | (필수) 이메일 시스템에서 가져온 이메일 데이터를 저장하는 Adobe Analytics 이벤트를 지정합니다. 보낸 이벤트를 사용하여 전송된 이메일 메시지 수를 볼 수 있습니다. |
| 가입 해지 | (필수) 이메일 시스템에서 가져온 구독 취소 데이터를 저장하는 Adobe Analytics 이벤트를 지정합니다. 가입 취소된 이벤트는 이메일 메시지를 연 다음, 조직의 향후 이메일 메시지를 옵트아웃하는 구독 취소 링크를 클릭한 방문자 수를 볼 수 있도록 해줍니다. |
| 세그먼트 | 기존 세그먼트를 이 통합과 함께 사용할 수 있습니다 (선택 사항). |
| 액세스 요청 | 권장 액세스 권한을 활성화합니다. |
| 데이터 수집 | Select **JavaScript Plug-in** if you want to use the s_code.js plug-in as the collection model for this integration. Select **Automated Solution** if you want to use an automated collection model for this integration, then specify the unique identifiers used for this integration. 이 옵션을 선택하는 경우 이 통합에 사용되는 고유 식별자를 지정합니다.<ul><li>메시지 ID 쿼리 문자열 매개 변수: 이 값은 이메일 파트너가 랜딩 페이지 URL에 첨부한 메시지 ID를 나타냅니다.</li><li>수신자 ID 쿼리 문자열 매개 변수: 이 값은 이메일 파트너가 랜딩 페이지 URL에 추가하는 수신자 ID를 나타냅니다.</li></ul> |
| 대시보드 및 책갈피 생성 | 통합에 대한 대시보드와 책갈피를 자동으로 생성합니다. |