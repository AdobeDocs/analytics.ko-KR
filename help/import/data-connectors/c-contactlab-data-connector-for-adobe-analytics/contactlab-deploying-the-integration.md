---
description: 'null'
title: 통합 배포
uuid: df3f24c9-d2e3-489e-b97e-e1af0d5dd1fa
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# 통합 배포{#deploying-the-integration}

이 통합 배포는 다음 작업이 필요한 간단한 프로세스입니다.

## Adobe 통합 마법사 완료{#completing-the-adobe-integration-wizard}

Data Connectors 인터페이스에서 통합 마법사를 완료하는 절차.

1. Adobe Experience Cloud 내에서 Data Connectors(이전 Genesis) 영역으로 이동합니다.
1. ContactLab 통합 마법사를 시작합니다.
1. 원하는 보고서 세트를 선택하고 통합 이름을 제공합니다.
1. 다음 항목을 구성합니다.

   | 항목 | 설명 |
   |---|---|
   | 이메일 주소 | 기본 연락처의 이메일 주소 |
   | 설명 | (선택 사항) 이 통합 설정에 대한 설명 |

1. 다음 **[!UICONTROL 변수 매핑]** 항목을 구성합니다.

   | 항목 | 설명 |
   |---|---|
   | 링크 ID | 링크 ID를 실시간으로 수집할 eVar를 선택합니다. |
   | 메시지 ID | 메시지 ID를 실시간으로 수집할 eVar를 선택합니다. |
   | 수신자 ID | 수신자 ID를 실시간으로 수집할 eVar를 선택합니다. |
   | 바운스 수 | ContactLab에서 일별 바운스를 받을 숫자 이벤트를 선택합니다. |
   | 보냄 | ContactLab에서 일별 전송 수를 받을 숫자 이벤트를 선택합니다. |
   | 클릭됨 | ContactLab에서 일별 총 클릭 수를 받을 숫자 이벤트를 선택합니다. |
   | 열림 | ContactLab에서 일별 총 열림 수를 받을 숫자 이벤트를 선택합니다. |
   | 가입 해지됨 | ContactLab에서 일별 가입 해지 수를 받을 숫자 이벤트를 선택합니다. |

1. 데이터 액세스를 활성화하고 데이터 수집을 구성합니다.
   1. 필요한 경우 분류 이름을 변경합니다.
   1. **[!UICONTROL 파트너 세그먼트]**&#x200B;는 통합에 포함된 표준 리마케팅 세그먼트입니다.
   1. **[!UICONTROL 세그먼트]** 아래에서 이 통합에 포함할 사용자 지정 세그먼트를 선택합니다. 관리 패널에서 추가 사용자 지정 세그먼트를 만들 수 있습니다.
   1. **[!UICONTROL 액세스 요청]**&#x200B;에서 상자를 선택하여 일별 리마케팅 세그먼트에서 ContactLab으로 제품 정보를 내보낼 수 있습니다.
   1. 필요에 따라 계산된 지표의 이름을 변경합니다.
   1. Analytics 수집 코드를 수동으로 업데이트하거나 자동화된 솔루션을 사용하여 ID를 수집할지 여부를 구성합니다. **[!UICONTROL 자동화된 솔루션]**&#x200B;을 선택하는 경우 이메일 링크에 사용되는 매개 변수를 포함하여 ID를 전달해야 합니다.
1. 모든 구성 항목을 검토하고 **[!UICONTROL 지금 활성화]**&#x200B;를 클릭합니다.

## 통합 확인{#verifying-the-integration}

Adobe Experience Cloud에서 ContactLab 통합 설정 보기

1. 통합 활동 로그를 봅니다.
   1. Adobe Experience Cloud에서 **[!UICONTROL 지원]** > **[!UICONTROL 통합 활동 로그]**&#x200B;로 이동합니다.

      ![](assets/integration_activity_log.png)

   1. **[!UICONTROL 분류 데이터를 가져왔습니다]**, **[!UICONTROL 지표 데이터를 가져왔습니다]** 및 **[!UICONTROL 지표 데이터를 내보냈습니다]**&#x200B;와 같은 항목을 찾습니다. 이러한 항목은 성공적으로 배포한 후 1일 이내에 표시됩니다.
1. Adobe Analytics에서 보고 데이터를 봅니다.
   1. **[!UICONTROL 사용자 지정 전환]** > **[!UICONTROL 사용자 지정 전환 1-10]** > **[!UICONTROL 메시지 ID 보고서]**&#x200B;로 이동합니다.

      ![](assets/reporting.png)

   1. ContactLab 보고를 찾습니다. 이 데이터는 성공적으로 배포한 후 24-48시간 이내에 표시됩니다.
