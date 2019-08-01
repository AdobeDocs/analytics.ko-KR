---
description: 통합을 활성화하려면 데이터 커넥터 인터페이스 내에서 Qualtrics 통합 마법사를 완료해야 합니다.
seo-description: 통합을 활성화하려면 데이터 커넥터 인터페이스 내에서 Qualtrics 통합 마법사를 완료해야 합니다.
seo-title: Adobe 통합 마법사 완료
solution: Analytics
subtopic: Qualtrics
title: Adobe 통합 마법사 완료
topic: Data connectors
uuid: e 065 fba 4-1 fe 1-4 e 25-9 c 45-6 c 52 dc 20 f 81 e
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Completing the Adobe Integration Wizard{#completing-the-adobe-integration-wizard}

통합을 활성화하려면 데이터 커넥터 인터페이스 내에서 Qualtrics 통합 마법사를 완료해야 합니다.

1. 데이터 커넥터로 이동하여 Qualtrics 통합 마법사를 실행합니다. ([Data Connectors 도움말](http://microsite.omniture.com/t2/help/en_US/genesis/)).
1. 이 통합에 사용할 보고서 세트를 선택하고 이름을 입력합니다.

   다음 단계에 설명된 정보를 제공하는 통합 마법사를 완료합니다. 1. **Wizard Step 1**

   | Email Address | 기본 연락처 이메일 주소입니다. |
   |---|---|
   | 설명 | (선택 사항) 이 통합 설정에 대한 설명입니다. |
   | Qualtrics 조직 ID | [Qualtrics 조직 ID 조회](../../qualtrics-overview/qualtrics-org-id.md#task-47ea30d6dcd24893986a5e5b8dcf5e96) |
   | Adobe sitecatalyst 토큰 | [Qualtrics Adobe Analytics 토큰 생성](../../qualtrics-overview/qualtrics-token.md#task-e32eacbc91614008b84e6b2f0b92d372) |

1. ** 마법사 2 단계 - 변수 매핑**

   | Qualtrics 응답 목록 | 보고서 세트에서 사용 가능한 목록 변수를 선택합니다. (보고서 세트 관리자에서 새 Listvar를 활성화해야 할 수 있습니다.) |
   |---|---|
   | Qualtrics 응답 ID | 보고서 세트에서 사용 가능한 Evar 또는 prop를 선택합니다. (보고서 세트 관리자에서 새 Listvar를 활성화해야 할 수 있습니다.) |
   | 추적 서버 | Adobe Analytics 데이터를 추적하는 데 사용하는 추적 서버 (도메인) 설정을 제공합니다. `trackingServerSecure` 추적 서버를 표준 추적 서버 설정과 다른 경우 사용합니다. |
   | Qualtrics 설문조사 제출 | 보고서 세트에서 사용 가능한 이벤트를 선택합니다 (보고서 세트 관리자에서 새 이벤트를 활성화해야 할 수 있음). |

1. **마법사 3 단계**: 필수 사항 없음, 정보용으로만 제공됩니다.

   단계 결과 1. ** 마법사 4 단계 - 내보내기 설정**

   | eVar | Qualtrics로 내보낼 때 표시할 evar 중 최대 5 개를 선택합니다. |
   |---|---|
   | 이벤트 | Qualtrics로 내보낼 때 표시할 사용자 지정 이벤트 최대 5 개 선택 |
   | Prop | Qualtrics로 내보낼 때 표시할 Prop 최대 5 개 선택 |
   | 액세스 요청 | Qualtrics로 내보낼 표준 지표 및 차원에 대한 상자를 선택합니다. The `visitor_id` is required to allow the export to function properly. |

1. **마법사 5 단계**: 구성을 검토하고 지금 **[!UICONTROL 활성화를 클릭합니다]**.
