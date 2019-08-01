---
description: 데이터 커넥터 인터페이스에서 통합 마법사를 완료하는 절차.
seo-description: 데이터 커넥터 인터페이스에서 통합 마법사를 완료하는 절차.
seo-title: Adobe 통합 마법사 완료
solution: Analytics
title: Adobe 통합 마법사 완료
uuid: fb 106251-78 cf -4 a 2 a -8 ba 2-2 a 39188 ba 910
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Completing the Adobe Integration Wizard{#completing-the-adobe-integration-wizard}

데이터 커넥터 인터페이스에서 통합 마법사를 완료하는 절차.

1. Adobe Marketing Cloud 내의 데이터 커넥터 (이전 Genesis) 영역으로 이동합니다.
1. Responsys 통합 마법사를 시작합니다.
1. 원하는 보고서 세트를 선택하고 통합 이름을 제공합니다.
1. 다음 항목을 구성합니다.

   | 항목 | 설명 |
   |---|---|
   | 이메일 주소 | 기본 연락처의 이메일 주소 |
   | 설명 | (선택 사항) 이 통합 설정에 대한 설명 |
   | 계정 ID | support@responsys.com의 Responsys 지원 팀에 문의하여 얻을 수 있습니다. |

1. Configure the following **[!UICONTROL Variable Mappings]** items:

   | 항목 | 설명 |
   |---|---|
   | 메시지 ID | 실시간으로 메시지 ID 수집을 위한 evar를 선택합니다. |
   | Recipient ID | 받는 사람 ID를 실시간으로 수집할 evar를 선택합니다. |
   | 총 바운스 수 | Responsys에서 일별 바운스를 받을 숫자 이벤트를 선택합니다. |
   | 보낸 이메일 | Responsys에서 일별 전송을 수신할 숫자 이벤트를 선택합니다. |
   | 클릭함 | Responsys에서 일별 총 클릭 수를 받을 숫자 이벤트를 선택합니다. |
   | 열림 | Responsys에서 일별 총계를 받는 숫자 이벤트를 선택합니다. |
   | 가입 해지 | Responsys에서 일별 가입을 해지하려면 숫자 이벤트를 선택합니다. |
   | 배달됨 | Responsys에서 일별 배달을 받을 숫자 이벤트를 선택합니다. |

1. 데이터 액세스 권한을 활성화하고 데이터 수집을 구성합니다.
   1. 필요에 따라 분류 이름을 변경합니다.
   1. **[!UICONTROL 파트너 세그먼트는]** 통합에 포함된 표준 리마케팅 세그먼트입니다.
   1. **[!UICONTROL 액세스 요청에서]**&#x200B;일별 리마케팅 세그먼트의 응답으로 제품 정보를 내보낼 수 있게 하려면 상자를 선택합니다.
   1. Analytics 수집 코드를 수동으로 업데이트하거나 자동화된 솔루션을 사용하여 ID를 수집할지 여부를 구성합니다. **[!UICONTROL 자동화된 솔루션을]**&#x200B;선택하는 경우 ID의 전달을 위해 이메일 링크에 사용되는 매개 변수를 포함해야 합니다.
1. Review all configuration items and click **[!UICONTROL Activate Now]**.
