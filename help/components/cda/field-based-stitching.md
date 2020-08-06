---
title: 현장 기반 연결
description: 필드 기반 스티칭을 사용하여 데이터를 결합하는 데 필요한 사전 요구 사항과 제한 사항을 이해합니다.
translation-type: tm+mt
source-git-commit: 763c1b7405c1a1b3d6dbd685ce796911dd4ce78b
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 23%

---


# 현장 기반 연결

장치 간 분석에서는 데이터를 서로 연결하는 두 가지 고유한 방법을 제공합니다. 이 메서드는 [prop](/help/implement/vars/page-vars/prop.md) 또는 [eVar과](/help/implement/vars/page-vars/evar.md)같은 Analytics 변수를 사용하여 사람 식별자를 포함합니다. 이 변수는 장치를 함께 연결하는 기준으로 해당 변수를 사용합니다.

## 필드 기반 스티칭에 대한 사전 요구 사항

필드 기반 스티칭을 사용하여 장치 간 분석을 구현하려면 다음이 필요합니다. 조직 내 팀 및 Adobe 계정 관리자와 함께 다음 사항을 모두 충족하도록 하십시오.

>[!IMPORTANT]
>
>모든 전제 조건을 충족하지 못하면 교차 장치 분석을 사용할 수 없거나 데이터 결합이 제대로 되지 않을 수 있습니다.

* 모든 전제 조건은 [개요 페이지에 나열되어 있습니다](overview.md).
* 사용자가 로그인하거나 이메일을 여는 경우와 같이 가능할 때마다 개인을 고유하게 식별하는 prop 또는 eVar을 설정해야 합니다. 이 요구 사항은 모바일 앱(사용하는 경우)을 비롯한 모든 플랫폼에 적용됩니다. 필드 기반 스티칭에 대해 제공되면 원하는 식별 변수를 계정 관리자에게 알립니다.

## 필드 기반 스티칭에 대한 제한 사항

* 필드 기반 스티칭은 높은 사용자 식별 비율이 있는 보고서 세트에 가장 적합합니다. 보고서 세트에 ID 또는 로그인 비율이 낮은 경우 [Co-op 그래프 사용을 고려하십시오](device-graph.md).

## 다음 단계

Once your organization meets all requirements met and understands the limitations, you can start [Setting up Cross-Device Analytics](setup.md).