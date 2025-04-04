---
title: 필드 기반 결합
description: 필드 기반 결합을 사용하여 데이터 결합의 사전 요구 사항과 제한 사항을 이해합니다.
exl-id: 81f2768c-53c2-40b4-8d3b-8d3b94cd7318
feature: CDA
role: Admin
source-git-commit: 5bf3f561c471410e4ce1ca576ba34ea3849b0325
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 83%

---

# 필드 기반 결합

{{available-existing-customers}}

크로스 디바이스 분석에서는 데이터를 서로 결합하는 두 가지 서로 다른 방법을 제공합니다. 이 방법은 [prop](/help/implement/vars/page-vars/prop.md)이나 [eVar](/help/implement/vars/page-vars/evar.md)과 같은 Analytics 변수를 사용하여 사용 식별자를 포함합니다. 해당 변수는 디바이스를 함께 연결하는 기준으로 사용됩니다. 방문자 추적의 투명성과 예측 가능성을 확보하기 위해 이 결합 옵션을 사용하는 것이 좋습니다.

## 필드 기반 결합에 대한 사전 요구 사항

필드 기반 결합을 사용하여 크로스 디바이스 분석을 구현하려면 다음 조건을 충족해야 합니다. 조직 내의 팀 및 Adobe 계정 팀과 함께 다음 사항을 모두 충족하는지 확인합니다.

>[!WARNING]
>
>모든 사전 요구 사항을 충족하지 못하면 크로스 디바이스 분석을 사용할 수 없거나 데이터 결합이 제대로 되지 않을 수 있습니다.

* [개요 페이지](overview.md)에 나열되어 있는 모든 사전 요구 사항.
* 구현은 가능하다면 항상 사용자가 로그인하거나 이메일을 여는 경우와 같이 개인을 고유하게 식별할 수 있는 prop 또는 eVar을 설정해야 합니다. 이 요구 사항은 모바일 앱(사용하는 경우)을 비롯한 모든 플랫폼에 적용됩니다.<br/>이 prop 또는 eVar에 기본값을 할당하지 마십시오. 2,000개 이상의 서로 다른 장치에 동일한 기본값이 할당되면 해당 사용자가 &#39;잘못된 사용자&#39; 목록에 추가되고 이러한 이벤트가 CDA가 활성화된 가상 보고서 세트에서 삭제되어 잘못된 분석이 발생합니다.
* 필드 기반 결합에 대해 프로비저닝되면 원하는 식별 변수를 Adobe 계정 팀에 전달합니다.

## 필드 기반 결합에 대한 제한 사항

* 필드 기반 결합은 높은 사용자 식별/인증 비율이 있는 보고서 세트에 가장 적합합니다.
* props 및 eVar 각각에는 보고 목적으로 대문자 및 소문자를 처리하는 방법에 대한 규칙이 있지만 필드 기반 결합은 결합에 사용되는 prop 또는 eVar를 어떤 방식으로도 변환하지 않습니다. 필드 기반 결합은 사후 VISTA 규칙 및 사후 처리 규칙이 존재하는 것처럼 지정된 필드의 값을 사용합니다. 결합 프로세스는 대소문자를 구분합니다. 예를 들어 때때로 “Bob”이라는 단어가 prop/eVar에 나타나며, 때로는 “BOB”이라는 단어가 나타나는 경우 이는 결합 과정에서 두 명의 개별적인 사람으로 처리됩니다.
* 필드 기반 결합은 대소문자를 구분하므로 Adobe는 필드 기반 결합에 사용되고 있는 prop 또는 eVar에 적용되는 VISTA 규칙 또는 처리 규칙을 검토할 것을 권장합니다. 이러한 규칙 중 동일한 ID의 새로운 형식을 도입하는 규칙이 없는지 확인하기 위해 검토해야 합니다. 예를 들어 VISTA 또는 처리 규칙이 히트의 일부에서만 prop 또는 eVar에 소문자를 도입하지 않는지 확인해 보아야 합니다.
* 필드 기반 결합은 결합 목적으로 둘 이상의 prop 또는 eVar 사용을 지원하지 않습니다. 예를 들어 eVar12에 로그인 ID가 포함되어 있고 eVar20에 이메일 ID가 포함되어 있는 경우 그 중 하나를 선택해야 합니다.
* 필드 기반 결합은 필드를 결합하거나 연결하지 않습니다(예: eVar10 + prop5).
* prop 또는 eVar에는 단일 유형의 ID를 포함해야 합니다. 예를 들어 prop 또는 eVar는 로그인 ID와 이메일 ID의 조합을 포함해서는 안 됩니다.
* 동일한 방문자에 대해 동일한 타임스탬프를 가진 여러 히트가 발생하지만 결합 prop 또는 eVar에 다른 값이 있는 경우, CDA는 알파벳 순서를 기반으로 선택하게 됩니다. 따라서 방문자 A에 동일한 타임스탬프를 가진 두 개의 히트가 있고 히트 중 하나가 “Bob”을 지정하고 다른 하나는 “Ann”을 지정하는 경우 CDA는 “Ann”을 선택합니다.


## 다음 단계

조직이 모든 요구 사항을 충족하고 제한 사항을 이해하면 [Cross-Device Analytics 설정](setup.md)을 시작할 수 있습니다.

