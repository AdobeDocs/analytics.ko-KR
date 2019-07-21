---
title: 솔루션 디자인 문서 만들기
seo-title: 솔루션 디자인 문서 만들기
description: 솔루션 설계 문서의 정의와 조직에서 사용할 수 있는 방법을 알아봅니다.
seo-description: 솔루션 설계 문서의 정의와 조직에서 사용할 수 있는 방법을 알아봅니다.
translation-type: tm+mt
source-git-commit: d195fb85711f58383577bf1d7b4da4078b909427

---


# 솔루션 디자인 문서 만들기

솔루션 디자인 문서 (솔루션 디자인 참조 또는 비즈니스 요구 사항 문서라고도 함) 는 본질적으로 Analytics 구현의 블루프린트입니다. 조직 전체에서 이해 관계자에 의해 식별된 기준을 정의하고 Adobe Analytics 내의 변수로 변환합니다. 따라서 조직은 보고 요구 사항을 조율하는 데 어려움이 있으며 중요한 데이터를 수집하는 데 놓치는 경향이 있습니다.

## 전제 조건

[Analytics 구현을 확인하고 프로덕션에 게시](../implement-with-launch/validate-publish-prod.md) - 직접 필수 사항은 아니지만, 추가 비즈니스 요구 사항을 설정하고 구현하는 동안 중요한 데이터가 수집되도록 기본 구현을 준비하는 것이 좋습니다.

## 디자인 문서의 소유권 및 위치

* **조직 내에서 솔루션 디자인 문서를 유지할 책임이 있는 사람을 결정합니다.** 이 역할은 개인 또는 팀일 수 있습니다. 역할 변경 사항이나 조직의 재구성을 통해서도 솔루션 디자인을 유지할 수 있습니다. 이것은 살아있는 문서이므로 적절하게 유지 관리해야 합니다.
* **솔루션 문서가 위치할 위치를 결정합니다.** 솔루션 디자인 문서를 위한 최고의 위치는 없지만 일반적으로 액세스할 수 있는 내부 위치에 거주합니다. 예를 들어 공유 스프레드시트나 SharePoint 또는 내부 Wiki와 같은 공동 작업 영역이 있습니다. 모든 사람에게 편집할 필요는 없지만 보고 기능을 최소한 볼 수 있도록 보고 기능에 액세스할 수 있는 사용자에게 유용합니다.

## 비즈니스 요구 사항 정의

수집할 데이터를 결정할 때 "모든 것" 는 쉽게 "모든 것" 로 표시되지만, 관리가 쉽고 더 간결한 데이터 양을 수집하는 것보다 더 적은 가치를 제공할 수 있습니다.

1. **주요 성능 지표를 결정합니다.** 방문자가 어떤 작업을 수행하길 원하십니까? 이 질문에 대한 답변은 업계마다 다르며, 여러 가지가 될 수 있습니다. 구매, 등록 또는 광고 클릭이 포함됩니다.
1. **수집할 가장 중요한 데이터를 계산해 보십시오.** 구체적인 답변을 얻을 수 있는 비즈니스 질문을 할 수 있습니다. 이러한 질문에 대한 답변은 KPI를 개선하는 방법에 대한 통찰력을 제공합니다.
1. **이러한 질문을 해결하고 추적 요구 사항을 파악합니다.** 차원 및 지표로 그룹화합니다.
   * 차원은 텍스트를 포함하는 변수입니다. 예에는 내부 검색어, 제품 카테고리 또는 방문자가 클릭한 영역의 이름이 포함됩니다.
   * 지표는 방문자가 원하는 작업을 수행하는 특정 이벤트이며, 원하는 작업을 수행합니다. 예에는 주문 제출, 뉴스레터 가입 또는 설문 조사 응답 제출이 포함됩니다.
1. **차원 및 지표를 페이지 또는 스프레드시트에 매핑합니다.** 이 페이지 또는 표는 궁극적으로 솔루션 디자인 문서가 됩니다. 몇 가지 유용한 열 또는 글머리 기호:
   * 구현 상태: 계획, 활성, 비활성, 문제 등 이 경우, 변수가 구현된 경우, 또는 데이터 수집에 문제가 있는 경우, 해당 변수가 해당 변수의 상태를 알 수 있습니다.
   * 변수 이름: 예: "internal search terms". Analytics 내에서 작업할 때 분석가가 보게 되는 값이 이 값입니다.
   * Analytics 변수가 다음에 매핑됨: 값을 할당할 기본 또는 사용자 지정 Analytics 변수. 지표는 일반적으로 Evar에 속하며 지표는 이벤트 아래에 속합니다.
   * 로직: 변수가 설정된 방법과 값을 결정하는 것에 대한 설명입니다. 예를 들어 "내부 검색 페이지에만 설정됩니다. Q 쿼리 문자열 매개 변수의 값을 가져옵니다. "
   * 변수와 관련된 기타 모든 메모

## 추가 리소스

솔루션 설계 문서를 정의하는 것은 매우 복잡한 프로젝트이며, 특히 이전에 만들지 않은 조직에게는 매우 복잡한 프로젝트입니다. 추가 지원이 필요한 경우 Adobe는 Adobe Analytics를 사용할 수 있도록 전문 컨설팅 서비스를 제공합니다. Adobe의 전문 서비스를 등록하려면 계정 관리자에게 문의하십시오. [기술 사전 구현 설문 조사를](assets/technical-pre-implementation-questionnaire.pdf) 작성하여 Adobe가 조직의 요구 사항을 기반으로 하는 방법을 정확하게 파악할 수 있습니다.

또한 솔루션 디자인 문서 작성을 지원하고 사이트에서 Adobe Analytics를 구현하는 데 도움이 되는 여러 Adobe 파트너가 있습니다.

> [!NOTE] Analytics 커뮤니티 구성원은 다음 링크를 유용하지만 Adobe가 소유하지 않습니다. 컨텐츠를 볼 때 이 메모를 고려하십시오.

* [Observepoint로 웹 분석 솔루션 디자인을](https://resources.observepoint.com/blog/7-steps-solution-design-data-governance) 설정하는 7 단계
* [분석으로 디지털 분석 프로세스를](https://analyticsdemystified.com/analytics-strategy/framework-digital-analytics-process/) 위한 프레임워크
* [솔루션 설계 참조는 실제로 숫자](http://numericanalytics.com/why-a-simple-piece-of-documentation-is-the-key-to-analytics-success-the-solution-design-reference-is-actually-your-bff/) 분석의 BFF 입니다.
* [Antti Koski의 Adobe Analytics Tagging Map](http://www.anttikoski.fi/how-to-make-adobe-analytics-tagging-map-aka-solution-design-requirements-for-sitecatalyst-implementation/) 를 만드는 방법
* [Ebiquity를 통한 솔루션 설계 문서의](https://www.ebiquity.com/news-insights/analytics/the-importance-of-the-solution-design-document) 중요성

## 다음 단계

솔루션 디자인 문서에서 변수를 구현합니다.

* Evar 소개: Evar의 정의와 작동 방식 및 구현에서 사용하는 방법 알아보기
* 이벤트 소개: 성공 이벤트가 무엇인지, 작동 방식, 구현 중 하나를 사용하는 방법 알아보기
