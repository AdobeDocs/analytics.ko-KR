---
title: 데이터 계층 만들기
description: Analytics 구현에서 데이터 계층이 무엇이고 Adobe Analytics에서 이 데이터 계층을 사용하여 변수를 매핑하는 방법을 알아봅니다.
feature: Implementation Basics
exl-id: 271dd8fa-3ba1-4a7f-b16a-c48a736a5bb5
role: Admin, Developer, Leader
source-git-commit: 5ef8ba686a13f8b4ab592c0b48a9c074b0477fcf
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 97%

---

# 데이터 계층 만들기

데이터 계층은 Analytics 구현에 사용된 변수 값을 포함하는 사이트의 JavaScript 오브젝트의 프레임워크로서, Analytics 변수에 값을 할당할 때 보다 세밀하게 제어하고 쉽게 유지 관리할 수 있습니다.

## 전제 조건

[솔루션 디자인 문서 만들기](solution-design.md) - 조직이 추적 요구 사항을 충족시키는 것이 중요합니다. 조직의 개발 팀에 접촉하기 전에 솔루션 디자인 문서를 준비했는지 확인하십시오.

## 워크플로

데이터 계층을 사용하여 Adobe Analytics를 구현하는 절차는 일반적으로 다음과 같습니다.

1. **사이트 개발 팀과 협력하여 데이터 계층 구현**: 사이트 개발 팀은 데이터 계층 개체가 올바른 값으로 채워지는지 확인하는 작업을 주로 수행합니다. 사이트 개발 팀과 함께 이 페이지를 검토하여 팀 간의 기대 내용이 일치하는지 확인합니다.

   >[!NOTE]
   >
   >다음의 Adobe 권장 데이터 계층 사양은 선택 사항입니다. 이미 데이터 계층이 있거나 Adobe의 사양을 따르지 않기로 선택하는 경우, 따로 따라야 할 사양을 조직이 충족하도록 해야 합니다.

1. **브라우저 콘솔을 사용하여 데이터 계층의 유효성 검사**: 데이터 계층이 만들어지면 브라우저의 개발자 콘솔을 사용하여 데이터 계층이 작동하는지 확인할 수 있습니다. `F12` 키를 사용하면 대부분의 브라우저에서 개발자 콘솔을 열 수 있습니다. 변수 값의 예는 `adobeDataLayer.page.title`입니다.
1. **Adobe Experience Platform 데이터 수집을 사용하여 데이터 레이어 오브젝트를 데이터 요소에 매핑**: 이 단계는 조직의 구현 방법에 따라 다릅니다.
   * **웹 SDK를 사용하는 경우**: 원하는 데이터 레이어 오브젝트를 Adobe Experience Platform Edge의 원하는 XDM 필드에 매핑합니다. 원하는 데이터 레이어 매핑을 확인하려면 [Analytics XDM 변수 매핑](../aep-edge/xdm-var-mapping.md)을 참조하십시오.
   * **Analytics 확장을 사용하는 경우**: Adobe Experience Platform 데이터 수집의 태그 아래에 데이터 요소를 만들고 원하는 데이터 레이어 오브젝트에 할당합니다. 그런 다음 Analytics 확장 내에서 각 데이터 요소를 적절한 Analytics 변수에 할당합니다.

## 사양

새 구현 또는 재구성된 구현에는 [Adobe 클라이언트 데이터 레이어](https://github.com/adobe/adobe-client-data-layer/wiki)를 사용하는 것이 좋습니다.

조직은 [고객 경험 디지털 데이터 레이어](https://www.w3.org/2013/12/ceddl-201312.pdf) 또는 완전히 다른 사용자 정의 사양과 같이 다른 데이터 레이어 사양을 자유롭게 사용할 수 있습니다. 조직의 요구 사항을 충족하는 일관된 데이터 레이어에 맞추는 것이 가장 중요합니다.

데이터 계층은 확장 가능합니다. 조직만의 고유한 요구 사항이 있다면 해당 요구 사항에 맞게 데이터 계층에 개체를 포함할 수 있습니다.

## 데이터 계층 값 설정

데이터 계층은 일반적으로 서버측을 생성하며 사이트 콘텐츠를 작성하는 데 사용되는 것과 동일한 개체를 참조합니다. 조직의 [솔루션 디자인 문서](solution-design.md)에 설정된 추적 요구 사항을 기반으로 사이트의 데이터 계층을 설정하십시오.

## 다음 단계

[데이터 레이어 개체를 데이터 요소에 매핑](../launch/layer-to-elements.md): Adobe Experience Platform에서 사이트의 데이터 레이어를 사용합니다.
