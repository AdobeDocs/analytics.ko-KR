---
title: Analytics 확장을 사용하여 Adobe Analytics 구현
description: 태그 및 Analytics 확장을 사용하여 Adobe Analytics을 구현하는 방법을 알아봅니다.
feature: Launch Implementation
source-git-commit: e6b40881a543b43c03b612c7e7b0d9bd09f44c0d
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 48%

---

# Analytics 확장을 사용하여 Adobe Analytics 구현

Adobe Analytics의 서비스 제공 기간 동안 Adobe는 데이터 수집을 위해 사이트에서 코드를 구현하는 여러 가지 방법을 제공했습니다. Adobe의 현재 권장 방법은 Adobe Experience Platform에서 태그를 사용하는 것입니다.

Adobe Experience Platform의 태그는 다른 태그 지정 요구 사항과 함께 Analytics 코드를 배포할 수 있도록 해 주는 태그 관리 솔루션입니다. Adobe는 다른 솔루션 및 제품과의 통합을 제공하며 사용자 정의 코드를 배포할 수 있도록 해 줍니다. 따라서 사이트에서 코드를 업데이트하기 위해 조직의 개발 팀에 의존하지 않고도 이러한 모든 작업을 수행할 수 있습니다.

활성 Adobe Experience Cloud 계약을 보유한 모든 고객은 태그를 사용할 수 있습니다. 액세스 권한이 있는지 확실하지 않은 경우 조직의 Experience Cloud 시스템 관리자에게 문의하십시오.

구현 작업의 개요:

![Analytics 확장 워크플로우를 사용한 Adobe Analytics](../assets/analytics-extension-annotated.png)

|<div style="width:20px"></div>| 작업 | 추가 정보 | |-| —|—| | 1 | 다음을 확인하십시오. **보고서 세트 정의**. | [보고서 세트 관리자](../../admin/admin/c-manage-report-suites/report-suites-admin.md) | | 2 | **데이터 레이어 만들기** 를 사용하여 웹 사이트에서 데이터 추적을 관리할 수 있습니다. | [데이터 레이어 만들기](../prepare/data-layer.md) | | 3 | **태그 속성 만들기**. 속성은 태그 관리 데이터를 참조하는 데 사용되는 매우 중요한 컨테이너입니다.| [Adobe Analytics 태그 속성 만들기](../launch/create-analytics-property.md) | | 4 | **Analytics 확장 설치** 를 입력합니다. Adobe Analytics으로 데이터를 보내도록 Analytics 확장을 구성합니다. | [Adobe Analytics 확장 개요](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/analytics/overview.html?lang=en) | | 5 | **개발 환경에 배포**. 태그 개발을 반복적으로 수행할 수 있는 환경을 마련합니다. | [개발 환경에 Analytics 구현 배포](./deploy-dev.md) | | 6 | **유효성 검사 및 프로덕션에 게시**. 웹 사이트에 태그 속성을 추가합니다. 그런 다음 데이터 요소, 규칙 등을 사용하여 구현을 사용자 지정합니다.| [개발 구현 유효성 검사 및 프로덕션에 게시](./validate-publish-prod.md) |

## 추가 리소스

태그는 높은 자유도로 사용자 정의할 수 있습니다. 구현에 적합한 데이터를 포함하여 Adobe Analytics를 최대한 활용할 수 있는 방법에 대해 자세히 알아봅니다.

- [태그 설명서](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html#): 인터페이스의 작동 방식과 이요 가능한 확장 유형에 대해 알아봅니다.

- [구현 변수](../vars/overview.md): 데이터 수집 서버에 전송할 변수를 결정합니다.
