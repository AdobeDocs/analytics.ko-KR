---
description: 'null'
seo-description: 'null'
seo-title: 통합 배포
solution: Analytics
title: 통합 배포
uuid: 5abf6d49-b05b-4e0f-8d9b-bb02d8f1c84a
translation-type: tm+mt
source-git-commit: a31f25e8a4681cf34525a7994b00580aa3aac15d

---


# 통합 배포{#deploying-the-integration}

이 통합 배포는 다음 작업이 필요한 간단한 프로세스입니다.

## Adobe 통합 마법사 완료{#completing-the-adobe-integration-wizard}

데이터 커넥터 인터페이스에서 통합 마법사를 완료하는 절차.

1. Adobe Experience Cloud 내에서 데이터 커넥터(이전 Genesis) 영역으로 이동합니다.
1. Responsys 통합 마법사를 시작합니다.
1. 원하는 보고서 세트를 선택하고 통합 이름을 제공합니다.
1. 다음 항목을 구성합니다.

   | 항목 | 설명 |
   |---|---|
   | 이메일 주소 | 기본 연락처의 이메일 주소 |
   | 설명 | (선택 사항) 이 통합 설정에 대한 설명 |
   | 계정 ID | support@responsys.com에서 Responsys 지원 팀에 연락하여 얻습니다. |

1. 다음 변수 **[!UICONTROL 매핑]** 항목을 구성합니다.

   | 항목 | 설명 |
   |---|---|
   | 메시지 ID | 메시지 ID를 실시간으로 수집할 eVar를 선택합니다. |
   | Recipient ID | 수신자 ID를 실시간으로 수집할 eVar를 선택합니다. |
   | 총 바운스 수 | Responsys에서 일별 바운스를 받을 숫자 이벤트를 선택합니다. |
   | 이메일 전송 | Responsys에서 일별 전송을 수신할 숫자 이벤트를 선택합니다. |
   | 클릭됨 | Responsys에서 일일 총 클릭 수를 수신할 숫자 이벤트를 선택합니다. |
   | 열림 | Responsys에서 일별 합계를 받을 숫자 이벤트를 선택합니다. |
   | 구독 취소 | Responsys에서 일일 구독 취소를 받을 숫자 이벤트를 선택합니다. |
   | 배달됨 | Responsys에서 일별 전달을 받을 숫자 이벤트를 선택합니다. |

1. 데이터 액세스 활성화 및 데이터 수집 구성
   1. 필요에 따라 분류 이름을 변경합니다.
   1. **[!UICONTROL 파트너 세그먼트는]** 통합에 포함된 표준 리마케팅 세그먼트입니다.
   1. 액세스 **[!UICONTROL 요청에서]**&#x200B;상자를 선택하여 일일 리마케팅 세그먼트에서 Responsys로 제품 정보를 내보낼 수 있습니다.
   1. Analytics 수집 코드를 수동으로 업데이트하거나 자동화된 솔루션을 사용하여 ID를 수집할지 여부를 구성합니다. 자동화된 솔루션을 **[!UICONTROL 선택하는]**&#x200B;경우 이메일 링크에 사용되는 매개 변수를 포함하여 ID를 전달해야 합니다.
1. 모든 구성 항목을 검토하고 지금 **[!UICONTROL 활성화를 클릭합니다]**.

## Responsys 시스템 내에서 구성{#configuring-within-the-responsys-system}

통합을 활성화하면 Responsys 지원에 문의해야 합니다.

통합 마법사를 완료한 후 Responsys 내에서 통합을 활성화해야 합니다.

이렇게 하려면 Responsys 지원 팀(support@responsys.com)에 문의하십시오.