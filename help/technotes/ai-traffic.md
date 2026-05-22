---
description: AI 챗봇의 트래픽을 보고하는 방법을 이해할 수 있습니다
title: AI 챗봇의 트래픽 분석
feature: Metrics, Data Configuration and Collection
exl-id: 0b013b7d-02a2-405d-bdd6-c991f0baac8e
TQID: https://experienceleague.adobe.com/lyzSP-7iZ8Y5XiTG1t7Axsg1f5AJf6BbcZbu7MmkwWU
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: b7156124-d291-4de4-ac0c-ed17d8078449
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
subfeature_v2:
  - id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 643
ht-degree: 2%

---

# 대화형 AI 도구에서 트래픽 분석

Adobe Analytics은 웹 사이트에서 AI 트래픽을 분석하는 도구를 제공합니다.

AI 트래픽을 분석할 때 먼저 발생할 수 있는 AI 트래픽 유형과 어떤 유형이 히트를 생성하는지 이해해야 합니다. 그런 다음 Analysis Workspace에서 트래픽을 분석할 수 있습니다.

## AI 트래픽 이해

### AI 트래픽 유형 이해

웹 사이트의 AI 트래픽은 다음 상황 중 하나에서 발생할 수 있습니다.

* **사전 교육 중**: 웹 사이트의 콘텐츠가 스크랩되어 AI 교육 데이터에 수집될 때 드물게 발생합니다.

* **온디맨드 프롬프트에 응답할 때**: 사용자가 AI에 질문을 묻고 AI 챗봇이 응답하는 동안 발생합니다. AI 챗봇이 웹 검색을 수행하고 해당 웹 사이트의 콘텐츠가 응답에 포함됩니다. (이러한 유형의 상호 작용을 RAG(Retrieval-Augmented Generation)라고도 합니다.)

  일부 AI 챗봇 응답에는 사이트의 소스 자료에 대한 링크가 포함되어 있으며 일부는 포함되어 있지 않습니다.

* **에이전트 워크플로우를 실행할 때**: 사용자 요청에 응답하기 위해 브라우저에서 일련의 웹 페이지를 클릭할 때 AI 에이전트가 웹 사이트를 방문할 때마다 발생합니다. 이 경우 AI는 요청을 한 사용자의 에이전트 역할을 합니다.

### AI 트래픽에 대한 히트가 생성되는 시점을 이해합니다

히트는 페이지에서 JavaScript이 실행될 때 웹 페이지에 생성됩니다. 사이트에서 발생하는 AI 트래픽 유형에 따라 JavaScript이 실행될 수도 있고 실행되지 않을 수도 있습니다.

| AI 트래픽 유형 | 히트 생성 | 고려 사항 |
|---------|----------|---------|
| **사전 교육** | 예 | 히트는 웹 사이트의 콘텐츠가 AI에 수집될 때 사전 교육 중에 생성됩니다. 그러나 사전 교육은 드물게 발생하며 AI의 사전 교육에 포함된 콘텐츠는 웹 사이트에서 추가 히트를 생성하지 않고 향후 응답에서 반복해서 재사용할 수 있습니다. <p>즉, AI의 사전 교육 중에 발생하는 단일 히트는 웹 사이트에서 추가 히트를 생성하지 않고 여러 온디맨드 응답에 대해 반복해서 재사용할 수 있습니다.</p><p>Analysis Workspace에서 이러한 유형의 AI 트래픽을 분석하는 방법에 대한 자세한 내용은 [봇 탐지를 사용하여 AI 트래픽 분석](#analyze-ai-traffic-using-bot-detection)을 참조하십시오.</p> |
| **요청 시 프롬프트** | 아니요 | 응답은 다음을 조합하여 사용하므로 AI 응답은 히트를 생성하지 않습니다.<ul><li>사전 훈련된 데이터 <br/>정보는 이미 AI의 사전 훈련된 지식에 포함되어 있으므로 AI가 페이지에서 JavaScript을 실행하지 않습니다.</li><li>온디맨드 웹 검색 <br/>웹 검색 중에 웹 페이지의 원시 HTML만 가져오므로 AI가 페이지에서 JavaScript을 실행하지 않습니다.</li></ul> |
| AI 응답의 **Source 자료 링크** | 예 | 히트는 사용자가 AI 응답에 포함된 소스 자료에 대한 링크를 클릭할 때 생성됩니다. 링크에 응답도 포함되어 있고 링크를 사용자가 클릭하지 않은 경우에는 히트가 생성되지 않습니다. <p>일부 AI 챗봇 응답에는 소스 자료에 대한 링크가 포함되고 일부는 그렇지 않다. </p><p>Analysis Workspace에서 이러한 유형의 AI 트래픽을 분석하는 방법에 대한 자세한 내용은 [레퍼러 유형별 AI 트래픽 분석](#analyze-ai-traffic-by-referrer-type)을 참조하십시오.</p> |
| **에이전트 워크플로** | 예 | AI 에이전트가 사용자를 대신하여 워크플로를 클릭할 때 각 페이지에 히트가 생성됩니다. <p>Analysis Workspace에서 이러한 유형의 AI 트래픽을 분석하는 방법에 대한 자세한 내용은 [레퍼러 유형별 AI 트래픽 분석](#analyze-ai-traffic-by-referrer-type)을 참조하십시오.</p> |

## Analysis Workspace에서 AI 트래픽 분석

### 레퍼러 유형별 AI 트래픽 분석

Analysis Workspace의 레퍼러 유형 차원을 사용하여 다음 유형의 AI 트래픽을 분석할 수 있습니다.

* AI 응답의 Source 자료 링크

* 에이전트 워크플로

레퍼러 유형 차원에는 [대화형 AI 도구 차원 항목](/help/components/dimensions/referrer-type.md#conversational-ai-tools)이 포함됩니다. 이 차원 항목에는 사전 정의된 AI 챗봇 목록이 포함됩니다.

자세한 내용은 [레퍼러 유형](/help/components/dimensions/referrer-type.md)을 참조하세요.

### 보트 감지를 사용하여 AI 트래픽 분석

Analysis Workspace에서 보트 감지를 사용하여 사전 교육에서 발생하는 AI 트래픽을 분석할 수 있습니다.
