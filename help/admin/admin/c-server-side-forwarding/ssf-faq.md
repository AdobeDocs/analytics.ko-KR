---
description: 서버 측 전달과 관련된 기능과 문제점에 대한 FAQ.
seo-description: 서버 측 전달과 관련된 기능과 문제점에 대한 FAQ.
seo-title: 서버측 전달 FAQ
title: 서버측 전달 FAQ
uuid: ECD 0 bc 9 b-ebf 7-414 e -88 a 2-ebba 3 fd 75 c 92
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# 서버측 전달 FAQ

서버 측 전달과 관련된 기능과 문제점에 대한 FAQ.

## 추적 서버 {#section_28E5BECC2034484AB9726E513F2CCFB7}

| 질문 | 답변 |
|--- |--- |
| Q: 현재 이전의 추적 서버 기반 서버 측 전달을 사용하고 있다면 어떻게 합니까? | 이전 추적 서버 기반의 서버 측 전달 방법은 Analytics에서 Audience Manager로 데이터를 계속 전달하지만 Audience Manager 세그먼트를 Analytics로 보내려는 경우에는, 새 보고서 세트 기반의 서버 측 전달이 필요합니다. 또한 추적 서버 구성 위에 서버 측 전달을 위한 보고서 세트를 활성화해도 아무런 해가 없습니다. 충돌이 있을 때마다 새로운 보고서 세트 서버 측 전달 설정이 사용됩니다. |
| Q: 이전 추적 서버 기반의 서버 측 전달을 새 보고서 세트 기반의 서버 측 전달으로 마이그레이션해야 합니까? | 당분간 추적 서버 기반의 서버 측 전달을 계속 지원할 예정이지만, Audience Manager에서 Analytics로의 통합(Analytics에 세그먼트 공유)을 활용하려면 적용 가능한 모든 보고서 세트에 대해 새로운 보고서 세트 기반의 서버 측 전달을 제공해야 합니다. 그러나 이전 추적 서버 기반의 서버 측 전달을 비활성화할 긴급한 이유는 없습니다. |

## 태깅 및 보고 {#section_71391BA901AC47B9A2286281644FF281}

| 질문 | 답변 |
|--- |--- |
| Q: 내 사이트에 다중 세트 태깅이 있다면 어떻게 합니까? 서버 측 전달로 인해 Audience Manager에 대한 내 서버 호출이 두 배가 됩니까? | 아니요. Analytics에서 Audience Manager로 전달되는 조회는 조회에 포함된 보고서 세트의 수에 관계없이 Audience Manager에게 한 번만 전달됩니다. 조회에 있는 각 보고서 세트에 대해 Audience Manager에 해당 데이터 소스가 있는 경우 각 보고서 세트는 해당 단일 조회로부터 적절하게 채워집니다.  그러나 현재 클라이언트 측 데이터 수집(DIL)을 사용하고 고객 관리 모듈을 설치하지 않고 서버 측 전달을 활성화하는 경우에는 Analytics 조회에 있는 보고서 세트의 수에 관계없이 Audience Manager에 대한 서버 호출을 두 배로 늘릴 수 있습니다. |
| Q: 별도의 Experience Cloud Orgs에 매핑된 다중 세트 태그 지정 보고서 세트가 있는 경우 어떻게 합니까? | 단일 Analytics 히트에서 별도의 Experience Cloud Orgs에 속하는 두 개의 보고서 세트로 데이터를 보내면 안 됩니다. 그러나 이러한 경우, 페이지에서 ID 서비스 설정과 일치하는 Experience Cloud 조직으로만 히트를 전달합니다. |
| Q: 다중 세트 태깅이 있고 내 보고서 세트 중 하나만 Experience Cloud 조직에 매핑되고 다른 보고서 세트가 아닌 경우 어떻게 해야 합니까? | 매핑된 보고서 세트의 Experience Cloud 조직에 대한 해당 데이터 수집 서버로 히트를 전달하지만 매핑되지 않은 보고서 세트에 Audience Manager에서 연관된 데이터 소스가 없으므로 Audience Manager에서 매핑되지 않은 보고서 세트에 대해 데이터가 기록되지 않습니다. |
| Q: 여러 Experience Cloud Orgs에 매핑된 보고서 세트가 있는 경우 어떻게 합니까? | Analytics는 이 보고서 세트를 매핑되지 않은 것으로 간주하므로 이 보고서 세트에 대해서는 서버 측 전달 기능을 활성화할 수 없습니다. 이러한 매핑 문제를 해결하려면 고객 지원 센터에 문의하십시오. |
| Q: 보고서 세트 기반의 서버 측 전달 방법이 추적 서버 기반의 서버 측 전달보다 느립니까? | 아니요. 응답 시간은 동일합니다. |
| Q: 두 개의 Experience Cloud Orgs (또는 AAM 인스턴스) 가 있고 두 Experience Cloud Orgs 간에 데이터를 공유하려는 경우 어떻게 해야 합니까? 하나의 Analytics 히트를 여러 Experience Cloud Orgs에 전달할 수 있습니까? | 아니요. 하나의 Experience Cloud Org에 수집된 데이터를 다른 Experience Cloud 조직에 공유해야 하는 경우, Audience Marketplace를 사용하여 하나의 Audience Manager 인스턴스에서 다른 Audience Manager 인스턴스로 해당 대상을 보내는 것이 좋습니다. |
| Q: 서버 측 전달로 인해 Audience Manager 또는 Analytics에서 추가적인 청구가 발생합니까? | Analytics에서는 추가적인 청구가 발생하지 않습니다. Audience Manager에서 전달된 조회는 다른 조회와 동일하게 처리되며 청구됩니다.  이것이 DIL과 서버 측 전달을 동시에 활성화하지 않도록 하는 것이 중요한 이유입니다. 동시에 활성화하면 이중 청구와 데이터 중복이 발생할 수 있습니다. |

>[!MORE_LIKE_THIS]
>
>* [서버 측 전달](ssf.md#concept_9563FCADF29748928E770EC5221B2685)

