---
title: 차원 개요
description: 차원이 무엇이고 Adobe Analytics에서 차원이 어떻게 사용되는지 알아봅니다.
feature: Dimensions
exl-id: dc00e06a-fdb5-40e3-82e2-269bad3b3677
TQID: https://experienceleague.adobe.com/WypIneraYlrSyIpXv3UQWIFn42A-Dxi0SxeJ2VbeubQ
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7
subfeature_v2: id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: d4db20e3498d54162806b3fdef0b34f45c93a6ff
workflow-type: tm+mt
source-wordcount: 436
ht-degree: 37%

---

# 차원 개요

차원은 일반적으로 문자열 값을 포함하는 Adobe Analytics의 변수입니다. 일반적인 차원은 [페이지](page.md), [참조 도메인](referring-domain.md) 또는 [eVar](evar.md)를 포함합니다. 반면에, [지표](../metrics/overview.md)는 차원에 연결된 숫자 값을 포함합니다. 기본 보고서는 숫자 값 (지표) 열에 대해 문자열 값 (차원) 행을 보여 줍니다.

예를 들어 **[!UICONTROL 페이지]** 차원을 **[!UICONTROL 방문 횟수]** 지표와 결합하면 방문 횟수가 가장 많은 페이지를 보여 주는 등급 보고서가 만들어집니다.

| 페이지 | 방문 횟수 |
| --- | ---: |
| 홈 페이지 | 800 |
| 제품 페이지 | 500 |
| 구매 페이지 | 100 |

{style="table-layout:fixed"}

각 차원은 사이트의 다른 부분 또는 측면을 나타냅니다. 이러한 차원 중 하나 이상을 하나 이상의 지표와 결합하여 원하는 보고서를 만들 수 있습니다.

## 차원 설명 추가

Analytics 관리자는 보고서 세트 내에서 또는 Analysis Workspace 내에서 직접 차원 및 기타 구성 요소에 대한 설명을 추가할 수 있습니다. 차원에 설명을 추가하는 방법에 대한 자세한 내용은 [구성 요소 설명 추가](/help/analyze/analysis-workspace/components/add-component-descriptions.md)를 참조하십시오.

## 폐기된 차원

다음 차원이 중단되었습니다. 대부분의 보고서는 Analysis Workspace에서 사용할 수 없는 Reports &amp; Analytics 보고서였습니다. 기존 보고 또는 이전 데이터에서 이러한 정보가 발견되는 경우 참조용으로 여기에 문서화됩니다.

* **계층**: 보고를 위해 사이트의 계층 구조를 캡처하는 데 사용되는 사용자 지정 차원(`hier1`-`hier5`)입니다. 사용이 중단되었으며 Analysis Workspace에서 사용할 수 없습니다. 대신 [eVars](evar.md) 및 분류를 사용하십시오.
* **홈 페이지**: 현재 페이지가 방문자의 브라우저 홈 페이지인지 여부를 나타내는 플래그입니다. 최신 브라우저 개인 정보 보호 정책으로 인해 현대적인 것과 동등한 요소가 없는 레거시 차원입니다.
* **JavaScript 지원**: 방문자의 브라우저에서 JavaScript을 지원하는지 여부를 나타냈습니다. 최신 측정에는 더 이상 의미가 없는 레거시 차원입니다.
* **JavaScript 버전**: 방문자의 브라우저가 지원하는 JavaScript 버전을 보고했습니다. 더 이상 수집되지 않는 이전 차원입니다.
* **다음 페이지**: 방문자가 본 다음 페이지를 표시하는 경로 지정 차원입니다. 현재 경로 지정 차원에는 Analysis Workspace의 [흐름 시각화](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md)를 사용하십시오.
* **이전 페이지**: 방문자가 본 이전 페이지를 표시하는 경로 지정 차원입니다. 현재 경로 지정 차원에는 Analysis Workspace의 [흐름 시각화](/help/analyze/analysis-workspace/visualizations/c-flow/flow.md)를 사용하십시오.
* **시간대**: AppMeasurement 이미지 요청의 타임스탬프 오프셋에서 파생된 방문자의 시간대입니다. 웹 SDK에서 [`placeContext`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/context)을(를) 사용하여 시간대를 수집합니다.
* **최상위 도메인**: 방문자 액세스 지점의 최상위 도메인입니다. 기존 Reports &amp; Analytics 보고서입니다. 대신 [도메인](domain.md) 차원을 사용하십시오.
* **방문 페이지 번호**: 방문 내의 페이지 번호입니다. 기존 Reports &amp; Analytics 보고서입니다. 대신 [히트 깊이](hit-depth.md) 차원을 사용하십시오.
* **방문자 상태**: `s.state` 변수에서 미국 상태를 보고했습니다. 지리 특성을 사용하는 [미국 주](us-states.md) 차원을 위해 사용이 중단됩니다.
