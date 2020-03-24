---
description: 이 통합을 활성화하기 전에 Adobe Analytics® 및 이메일 소프트웨어 배포에 대해 다음 항목을 검토하십시오.
title: 이 통합을 활성화하기 전에
uuid: b911edc6-2265-48ed-9e3c-c79cc20dd9b2
translation-type: ht
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 이 통합을 활성화하기 전에{#before-you-activate-this-integration}

이 통합을 활성화하기 전에 Adobe Analytics® 및 이메일 소프트웨어 배포에 대해 다음 항목을 검토하십시오.

이렇게 하면 활성화 전에 적절한 우수 사례와 사전 요구 사항이 준비되므로 최적화되고 성공적인 통합이 이루어지도록 할 수 있습니다.

## Adobe Analytics{#adobe-analytics}

Adobe Analytics와 관련된 이 Data Connectors 통합에 대한 다음 정보를 검토하십시오.

* **보고서 세트별**: 이 통합은 보고서 세트별로 다르므로 주의하십시오. 통합을 활성화하기 전에 원하는 보고서 세트를 선택했는지 확인합니다.
* **사용 가능하고 구성된 Analytics 변수**: 이 통합에는 사용자 지정 이벤트 5개 및 사용자 지정 eVar 2개, 선택적 추가 이벤트 3개 및 추가 eVar 3개가 필요합니다. [Analytics 통합 변수](/help/import/data-connectors/silverpop-overview/silverpop-variables.md)를 참조하십시오.

* **승인된 담당자**: 이 통합을 활성화하면 Adobe, Inc.와의 서비스 계약 또는 Adobe의 신뢰할 수 있는 파트너 중 하나와의 서비스 계약에 따라 귀사에 비용이 발생할 수 있습니다. 이러한 통합을 활성화함으로써 귀하는 귀사의 권한을 부여받은 대표자임을 명시하며, 이에 따라 귀사는 상기에 제시된 서비스 계약에 명시된 요금을 지불해야 합니다.
* **Data Warehouse™**: 이 통합을 사용하려면 리마케팅 세그먼트를 생성하기 위해 Data Warehouse를 활성화해야 합니다. Data Warehouse를 활성화하지 않은 경우 Adobe에 자세한 내용을 문의하십시오.
* **수신자 ID**: 통합하려면 Analytics 변수(eVar) 내에서 &quot;방문자 ID&quot;를 캡처하고 저장해야 합니다. 방문자 ID(종종 &quot;수신자 ID&quot;라고도 함)는 Silverpop 시스템의 이메일 주소를 인코딩하거나 숫자로 표현한 것입니다. 이 &quot;수신자 ID&quot;는 사이트의 다운스트림 방문자 행동(장바구니 포기, 구매 등)과 관련되어 있어 Silverpop 시스템으로 다시 가져와 리마케팅 용도로 활용할 수 있습니다. 설정 프로세스의 일부로 마법사에서 메시지가 표시되면 이 용도를 위해 eVar를 식별해야 합니다.
* **외부 추적**: 현재 전송하는 각 이메일 캠페인에 대해 외부 추적을 활성화하는 우수 사례를 따르고 있지 않다면, 성공적인 통합을 위해 우수 사례를 따라야 합니다. 자세한 내용은 아래 Silverpop 섹션을 참조하십시오.
* **개인정보 규정 준수**: 수신자 또는 방문자 ID 추적을 활성화하면 이 기능이 사이트 방문자의 개인 식별 정보를 추적할 수 있음을 이해해야 합니다. 따라서 조직에서는 사이트 방문자에게 통지하고 동의를 구하는 등과 같이 개인정보 보호를 위한 적절한 절차를 구현해야 합니다.

## Silverpop Data Connector 통합{#silverpop-data-connector-integration}

Silverpop과 관련된 이 Data Connector 통합에 대한 다음 정보를 검토하십시오.

* **유효한 Silverpop 계정:** Data Connectors 이메일 통합을 사용하려면 클라이언트에 이메일이 설정된 활성 Silverpop 계정과 활성 사용자 자격 증명이 있어야 합니다.
* **Silverpop 담당자에게 문의하십시오**. 이 통합은 Silverpop에서 자동으로 활성화되지 않습니다. Analytics에서 데이터를 가져오거나 내보내려면 먼저 Silverpop 담당자에게 연락하여 Silverpop 설정을 시작해야 합니다.

> [!NOTE] 이 통합은 Engage 조직(Transact가 아님)에서만 작동합니다.

## 가격 책정{#pricing}

이 Data Connectors 통합에는 활성화 전에 고려해야 하는 가격 고려사항이 포함되어 있습니다.

### Adobe 가격 고려사항 {#section-2d1c79c895a5479bad8fdd97961ba6a3}

이 통합과 관련된 반복 및 구현 비용이 있을 수 있습니다. 자세한 가격 정보는 Adobe 계정 담당자에게 문의하십시오.

### 파트너 가격 고려사항 {#section-c6afad08c34b43e3a7a3637eea3328c3}

이 통합과 관련된 비용이 있을 수 있습니다. 가격 정보는 관계 관리자에게 문의하십시오.
