---
description: 'null'
seo-description: 'null'
seo-title: 통합 배포
solution: Analytics
title: 통합 배포
uuid: df3f24c9-d2e3-489e-b97e-e1af0d5dd1fa
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# 통합 배포{#deploying-the-integration}

이 통합 배포는 다음 작업이 필요한 간단한 프로세스입니다.

## Adobe 통합 마법사 완료{#completing-the-adobe-integration-wizard}

데이터 커넥터 인터페이스에서 통합 마법사를 완료하는 절차.

1. Adobe Experience Cloud 내에서 데이터 커넥터(이전 Genesis) 영역으로 이동합니다.
1. ContactLab 통합 마법사를 시작합니다.
1. 원하는 보고서 세트를 선택하고 통합 이름을 제공합니다.
1. 다음 항목을 구성합니다.

   | 항목 | 설명 |
   |---|---|
   | 이메일 주소 | 기본 연락처의 이메일 주소 |
   | 설명 | (선택 사항) 이 통합 설정에 대한 설명 |

1. 다음 변수 **[!UICONTROL 매핑]** 항목을 구성합니다.

   | 항목 | 설명 |
   |---|---|
   | 링크 ID | 실시간으로 링크 ID를 수집할 eVar를 선택합니다. |
   | 메시지 ID | 메시지 ID를 실시간으로 수집할 eVar를 선택합니다. |
   | Recipient ID | 수신자 ID를 실시간으로 수집할 eVar를 선택합니다. |
   | 바운스 수 | ContactLab에서 일별 바운스를 받을 숫자 이벤트를 선택합니다. |
   | 전송 | ContactLab에서 일별 전송을 수신할 숫자 이벤트를 선택합니다. |
   | 클릭됨 | ContactLab에서 일일 총 클릭을 수신할 숫자 이벤트를 선택합니다. |
   | 열림 | ContactLab에서 일별 총계를 받을 숫자 이벤트를 선택합니다. |
   | 구독 취소 | ContactLab에서 일별 미가입자를 받을 숫자 이벤트를 선택합니다. |

1. 데이터 액세스 활성화 및 데이터 수집 구성
   1. 필요에 따라 분류 이름을 변경합니다.
   1. **[!UICONTROL 파트너 세그먼트는]** 통합에 포함된 표준 리마케팅 세그먼트입니다.
   1. 세그먼트 **[!UICONTROL 아래에서]**&#x200B;이 통합에 포함할 사용자 지정 세그먼트를 선택합니다. 관리 패널에서 추가 사용자 지정 세그먼트를 만들 수 있습니다.
   1. 액세스 **[!UICONTROL 요청]**&#x200B;아래에서, 제품 정보를 일일 리마케팅 세그먼트에서 ContactLab으로 내보내도록 허용하려면 이 확인란을 선택합니다.
   1. 필요에 따라 계산된 지표의 이름을 변경합니다.
   1. Analytics 수집 코드를 수동으로 업데이트하거나 자동화된 솔루션을 사용하여 ID를 수집할지 여부를 구성합니다. 자동화된 솔루션을 **[!UICONTROL 선택하는]**&#x200B;경우 이메일 링크에 사용되는 매개 변수를 포함하여 ID를 전달해야 합니다.
1. 모든 구성 항목을 검토하고 지금 **[!UICONTROL 활성화를 클릭합니다]**.

## 통합 확인{#verifying-the-integration}

Adobe Experience Cloud에서 ContactLab 통합 설정 보기

1. 통합 작업 로그를 봅니다.
   1. Adobe Experience Cloud에서 지원 &gt; **[!UICONTROL 통합]** 활동 **[!UICONTROL 로그로 이동합니다]**.

      ![](assets/integration_activity_log.png)

   1. 성공적으로 **[!UICONTROL 가져온 분류 데이터,]**&#x200B;성공적으로 **[!UICONTROL 가져온 지표]**&#x200B;데이터 및 지표 데이터를 성공적으로 ****&#x200B;내보낸 지표 데이터와 같은 항목을찾습니다. 이러한 항목은 배포가 성공한 후 1일 이내에 표시됩니다.
1. Adobe Analytics에서 보고 데이터를 봅니다.
   1. 사용자 지정 **[!UICONTROL 전환]** &gt; **[!UICONTROL 사용자 지정 전환 1-10]** &gt; 메시지 ID **[!UICONTROL 보고서로 이동합니다]**.

      ![](assets/reporting.png)

   1. ContactLab 보고를 찾습니다. 이 데이터는 성공적인 배포 후 24-48시간 이내에 나타나야 합니다.