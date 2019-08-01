---
description: Adobe 데이터 커넥터 구성 마법사를 사용하여 통합을 설정합니다.
seo-description: Adobe 데이터 커넥터 구성 마법사를 사용하여 통합을 설정합니다.
seo-title: 통합 활성화
title: 통합 활성화
uuid: 93 c 59 f 8 e -3 cf 5-44 c 1-9 a 04-22460 af 93 d 5 d
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: a3310ec57ce4c68539f07e0d294c8175742c49dc

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
| 클릭함 | 총 이메일 클릭 수. |
| 캠페인 ID | 고유한 메시지 ID를 저장합니다. 종종 캠페인 변수에 저장됩니다. |
| 열림 | 총 이메일 수가 열립니다. |
| 클릭 수 | 클릭한 사람 수입니다. |
| 처리됨 | 처리된 총 이메일 수입니다. |
| Broadlog ID | 이 ID는 Neolane 시스템에서 이메일 주소를 인코딩하거나 숫자 표현으로 표현한 것입니다. 이 "확장 로그 ID" 는 사이트의 다운스트림 방문자 행동과 관련되어 있습니다 (장바구니 확장 로그 ID 포기, 구매 등). Neolane 시스템으로 가져와 리마케팅용으로 활용할 수 있습니다. |
| 예약됨 | 배달할 예약된 이메일 메시지 수. |
| sent | 전송된 이메일 메시지 수. |
| 총 바운스 수 | 배달 문제로 인해 수신자에게 배달되지 않은 이메일 메시지 수입니다. |
| 고유한 클릭 수 | 별개의 클릭 수. |
| 고유 열기 | Distinct의 수가 열립니다. |
| 가입 해지 | 이메일 메시지를 열어본 다음 조직의 향후 이메일 메시지를 옵트아웃하는 구독 취소 링크를 클릭한 방문자 수입니다. |
| 세그먼트 | 이 통합은 파트너 세그먼트 섹션에 표시된 파트너 정의 세그먼트를 만듭니다. 또한, 통합에 포함할 기존 보고서 세트 수준 세그먼트를 선택할 수 있습니다. |
| 액세스 요청 | 권장 액세스 권한을 활성화합니다. |
| 데이터 수집 | Select **JavaScript Plug-in** if you want to use the s_code.js plug-in as the collection model for this integration. Select **Automated Solution** if you want to use an automated collection model for this integration, then specify the unique identifiers used for this integration. 이 옵션을 선택하는 경우 이 통합에 사용되는 고유 식별자를 지정합니다. <ul><li>메시지 ID 쿼리 문자열 매개 변수: 이 값은 이메일 파트너가 랜딩 페이지 URL를 추가하는 메시지 ID를 나타냅니다.</li><li>수신자 ID 쿼리 문자열 매개 변수: 이 값은 이메일 파트너가 랜딩 페이지 URL에 추가하는 수신자 ID를 나타냅니다.</li></ul> |
| 대시보드 및 책갈피 생성 | 통합에 대한 대시보드와 책갈피를 자동으로 생성합니다. |