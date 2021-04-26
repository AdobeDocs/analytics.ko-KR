---
title: 교차 디바이스 분석
description: 디바이스 데이터를 함께 결합함으로써 데이터를 디바이스 중심에서 사람 중심으로 변경합니다.
exl-id: e1c0d1e5-399d-45c2-864c-50ef93a77449
translation-type: tm+mt
source-git-commit: 99fea634dafc5d0992898f8f9f89471b51191fc6
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 85%

---

# 교차 디바이스 분석

교차 디바이스 분석은 Analytics를 디바이스 중심 보기에서 사람 중심 보기로 변환하는 기능입니다. 그 결과 분석가는 브라우저, 디바이스 또는 앱을 넘나드는 사용자 행동을 이해할 수 있습니다. Adobe에서는 디바이스 데이터를 함께 연결하는 두 가지 매우 중요한 워크플로를 지원합니다.

* [**필드 기반 결합**](field-based-stitching.md): 가상 보고서 세트에서 크로스 디바이스 결합의 기반으로 Analytics 변수를 선택할 수 있습니다. 결정론적 일치를 사용하여 디바이스를 함께 연결합니다. 가장 결정론적 일치 사용 사례가 필요하면 필드 기반 결합을 사용하는 것이 좋습니다.
* [**Device Graph**](device-graph.md): CDA는 Device Graph와의 의사 소통을 통해 디바이스를 함께 결합합니다. 공동 작업 그래프는 결정론적 일치와 확률론적 일치를 모두 사용합니다.

CDA를 사용하여 다음과 같은 질문에 답변할 수 있습니다.

* 얼마나 많은 사람들이 내 브랜드와 상호 작용합니까? 얼마나 많은 디바이스와 어떤 유형의 디바이스를 사용하고 있습니까? 어떻게 중첩됩니까?
* 사람들이 모바일 디바이스에서 작업을 시작한 다음 나중에 데스크탑 PC로 이동하여 작업을 완료하는 빈도는 얼마나 됩니까? 하나의 디바이스에 랜딩되는 캠페인 클릭스루가 다른 곳에서 전환을 가져옵니까?
* 디바이스 간 여정을 고려하면 캠페인 효과에 대한 이해가 어떻게 달라집니까? 단계 분석은 어떻게 변경됩니까?
* 사용자가 하나의 디바이스에서 다른 디바이스로 이동하는 가장 일반적인 경로는 무엇입니까? 어디에서 중단됩니까? 어디로 이어집니까?
* 여러 디바이스가 있는 사용자의 행동은 단일 디바이스가 있는 사용자와 어떻게 다릅니까?

디바이스가 결합되면 변수 지속성이 디바이스 간에 전달됩니다. 예를 들어 사용자가 먼저 데스크탑 컴퓨터의 광고를 통해 사이트를 방문합니다. 해당 사용자는 모바일 앱을 찾아 설치한 다음 결국 모바일 디바이스에서 구매합니다. Cross-Device Analytics를 사용하면 모바일 디바이스의 매출을 데스크탑 컴퓨터에서 클릭한 광고에 연결할 수 있습니다.

Adobe는 파트너십과 투명성 측면에서 Microsoft Azure를 교차 디바이스 분석과 연계하여 사용하고 있다는 점을 고객에게 알리고자 합니다. Adobe는 Azure를 사용하여 디바이스 그래프 데이터를 저장하고 크로스 디바이스 결합을 수행합니다. 이와 같이 Adobe Analytics 데이터는 Adobe의 데이터 처리 센터와 Microsoft Azure에 있는 Adobe의 프로비저닝된 인스턴스 간에 서로 전달됩니다.

크로스 디바이스 분석의 기능에 대해 자세히 알려면 [여정 IQ: Cross-크로스 디바이스 분석 스파크 페이지](http://adobe.ly/aacda)를 참조하십시오.

## 전제 조건

CDA를 사용하려면 다음 조건을 모두 충족해야 합니다. [필드 기반 결합](field-based-stitching.md)과 [Device Graph](device-graph.md) 방법에는 특정한 자체 사전 요구 사항도 있습니다.

* Adobe Analytics Ultimate가 포함된 계약은 Adobe와 체결해야 합니다.
* 장치 간 분석은 보고서 세트별로 활성화됩니다. 여러 디바이스 유형 (웹, 앱 등)의 데이터를 의미하는 디바이스 간 데이터를 포함하는 보고서 세트를 사용하는 것이 좋습니다. CDA는 지리적 관점에서 엄격히 말해 전역적일 필요는 없지만 일부 조직에서는 &quot;전역&quot; 보고서 세트로서 이 개념을 언급하고 있습니다.

## 제한 사항

교차 디바이스 분석은 획기적이고 강력한 기능이지만 사용 방법에 대한 제한이 있습니다. [필드 기반 결합](field-based-stitching.md)과 [Device Graph](device-graph.md) 방법에는 특정한 자체 제한 사항도 있습니다.

* CDA는 Analysis Workspace를 통해서만 사용할 수 있습니다.
* 교차 디바이스 분석은 보고서 세트 간에 작동하지 않으며 여러 보고서 세트의 데이터를 결합하지도 않습니다.
* Adobe Analytics 보고서 세트는 둘 이상의 IMS 조직에 매핑할 수 없습니다. CDA는 주어진 보고서 세트 내에서 디바이스를 결합하기 때문에 여러 IMS 조직 간에 데이터를 결합하는 데에는 CDA를 사용할 수 없습니다.
* 비공개 그래프는 Experience Cloud 및 Adobe Analytics 내에 있는 [고객 속성](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html?lang=en#customer-attributes) 기능에 사용되는 것과 동일한 ID 동기화를 활용합니다. 그러나 CDA 가상 보고서 세트(개인 그래프 또는 필드 기반 스티칭에 따라 관계 없음)는 나머지 고객 속성 기능과 호환되지 않습니다. 즉, 고객 속성 기반 차원은 CDA 가상 보고서 세트 내에서 사용할 수 없습니다.
* CDA는 현재 A4T와 호환되지 않습니다.
* 교차 디바이스 분석은 가상 보고서 세트 및 보고서 처리 시간을 사용하는데, 여기에는 자체 제한 사항도 있습니다. 이러한 제한 사항에 대한 자세한 내용은 [가상 보고서 세트](../vrs/vrs-about.md) 및 [보고서 처리 시간](../vrs/vrs-report-time-processing.md)을 참조하십시오.
* 1.4 API가 지원되지 않습니다. Power BI 커넥터와 Report Builder 모두 1.4 API에 의존하며, 따라서 CDA와 호환되지 않습니다.
* 가상 보고서 세트의 내역 데이터는 Adobe 인식 및 결합 디바이스를 기반으로 변경됩니다. 소스 보고서 세트의 데이터는 변경되지 않습니다.
* Adobe에 의한 CDA 스티칭 프로세스의 활성 모니터링은 프로덕션 보고서 세트로만 제한됩니다.
* CDA는 현재 Adobe Analytics [데이터 복구 API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/data-repair.md)와 호환되지 않습니다.
