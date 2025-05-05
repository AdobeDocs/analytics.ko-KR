---
title: Report Builder의 제한된 레이블은 무엇입니까
description: Report Builder의 제한된 레이블을 설명합니다.
role: User
feature: Report Builder
type: Documentation
solution: Analytics
source-git-commit: eedabc6295f9b918e1e00b93993680e676c216c3
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 49%

---

# Report Builder의 제한된 레이블

일반적으로 Adobe Analytics의 데이터 거버넌스 관련 설정은 Adobe Experience Platform에서 상속됩니다. Adobe Analytics과 Adobe Experience Platform 데이터 거버넌스 간의 통합을 통해 민감한 Adobe Analytics 데이터의 레이블 지정 및 개인정보 처리방침 시행을 수행할 수 있습니다.

Experience Platform에서 사용하는 데이터 세트에 생성된 개인정보 보호 레이블 및 정책은 Adobe Analytics 보고서 세트 워크플로에 표시될 수 있습니다. 이러한 레이블은 중요한 필드에서 지표 및/또는 차원을 생성하는 사용자를 중단 또는 경고합니다. 데이터 세트에 대한 자세한 내용은 [데이터 세트 개요](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=ko)를 참조하십시오.

또한 보고, 내보내기, API 등을 통해 Adobe Analytics에서 데이터를 내보낼 경우, 보고서에 특정 방식으로 처리해야 하는 기밀 정보가 포함되어 있음을 사용자에게 통지하기 위해 경고 또는 레이블이 추가됩니다.

이 통합을 통해 규정 준수를 보다 쉽게 관리할 수 있습니다. 조직의 데이터 관리자는 사용을 제한하는 정책을 설정할 수 있습니다. 그 결과, Adobe Analytics 사용자는 데이터 관리자에 의해 정의된 정책을 준수함을 알고 보다 자신 있게 데이터를 사용할 수 있습니다.

자세한 내용은 [Adobe Analytics 및 데이터 거버넌스](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-privacy/privacy-overview.html?lang=ko)를 참조하십시오.

## Report Builder의 제한된 레이블 보기

보고, 다운로드 및 공유에 영향을 주는 두 가지 Adobe 정의 정책이 Adobe Analytics에 표시됩니다.

* Analytics 시행 정책
* 다운로드 시행 정책

이 정책에 영향을 받는 구성 요소는 회색으로 표시됩니다. 정책이 적용되는 구성 요소에 마우스를 가져다 대면, 다음이 표시됩니다. **이 데이터 사용을 금지하는 정책이 이 필드에 적용됩니다.**&#x200B;자세한 내용은 [레이블 및 정책](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/data-governance.html?lang=ko)을 참조하십시오.

![금지된 데이터 사용을 나타내는 정책 참고입니다.](assets/rb-restricted-label.png)

## 제한된 데이터가 포함된 보고서 업데이트

사용자가 나중에 제한되는 데이터 요소로 Report Builder 보고서를 생성하면 보고서를 새로 고침할 때 오류 메시지가 표시됩니다.

![데이터 요소가 나중에 제한된 후에 표시되는 오류 메시지입니다.](assets/error-restricted-data.png)
