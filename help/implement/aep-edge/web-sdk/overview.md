---
title: Adobe Experience Platform Web SDK를 사용하여 Adobe Analytics 구현
description: Adobe Experience Platform 데이터 수집에서 Web SDK 확장 기능을 사용하여 Adobe Analytics로 데이터를 전송합니다.
source-git-commit: e6b40881a543b43c03b612c7e7b0d9bd09f44c0d
workflow-type: tm+mt
source-wordcount: '782'
ht-degree: 23%

---

# Adobe Experience Platform Web SDK를 사용하여 Adobe Analytics 구현

[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/sdk/overview.html)를 사용하여 데이터를 Adobe Analytics로 전송할 수 있습니다. 이 구현 방법은 [XDM(경험 데이터 모델)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko-KR)을 Analytics에서 사용하는 형식으로 변환하여 작동합니다.

Web SDK를 사용하여 직접 또는 태그의 Web SDK 확장을 통해 Experience Edge에 데이터를 전송할 수 있습니다.

## Web SDK

구현 작업의 개요:

![웹 SDK 워크플로우를 사용하여 Adobe Analytics 구현](../../assets/websdk-annotated.png)

|<div style="width:20px"></div>| 작업 | 추가 정보 | |-| —|—| | 1 | 다음을 확인하십시오. **보고서 세트 정의**. | [보고서 세트 관리자](../../../admin/admin/c-manage-report-suites/report-suites-admin.md) | | 2 | **스키마 및 데이터 세트 설정**. Adobe Experience Platform을 활용하는 여러 애플리케이션에서 사용할 수 있도록 데이터 수집을 표준화하기 위해 Adobe은 개방적이고 공개적으로 문서화된 표준 XDM(Experience Data Model) 을 만들었습니다. | [스키마 UI 개요](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=ko-KR) 및 [데이터 세트 UI 개요](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=ko) | | 3 | **데이터 레이어 만들기** 를 사용하여 웹 사이트에서 데이터 추적을 관리할 수 있습니다. | [데이터 레이어 만들기](../../prepare/data-layer.md) | | 4 | **사전 빌드된 독립형 버전 설치**. 라이브러리를 참조할 수 있습니다(`alloy.js`)를 페이지에서 직접 CDN에 추가하거나 자체 인프라에서 다운로드하여 호스팅할 수 있습니다. 또는 NPM 패키지를 사용할 수 있습니다. | [사전 빌드된 독립형 버전 설치](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en#option-2%3A-installing-the-prebuilt-standalone-version) 및 [NPM 패키지 사용](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en#option-3%3A-using-the-npm-package)| | 5 | **데이터 스트림 구성**. 데이터 스트림은 Adobe Experience Platform Web SDK를 구현할 때 서버측 구성을 나타냅니다. | [데이터 스트림 구성](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en) | | 6 | **Adobe Analytics 서비스 추가** 데이터 스트림에 추가 이 서비스는 Adobe Analytics으로 데이터를 전송할지 여부와 방법을 제어합니다. | [데이터 스트림에 Adobe Analytics 서비스 추가](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en#analytics) | | 7 | **웹 SDK 구성**. 4단계에서 설치한 라이브러리가 데이터 스트림 ID(이전에 Edge 구성 ID( )로 제대로 구성되었는지 확인합니다`edgeConfigId`), 조직 id ( ))`orgId`) 및 기타 사용 가능한 옵션. | [웹 SDK 구성](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=ko) | | 8 | **명령 실행** 및/또는 **이벤트 추적**. 웹 페이지에 기본 코드가 구현되면 SDK를 사용하여 명령 및 이벤트 추적을 시작할 수 있습니다. | [명령 실행](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/executing-commands.html?lang=en) 및 [이벤트 추적](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html?lang=en) | | 9 | **구현 확장 및 유효성 검사** 프로덕션에 투입하기 전에 | |



## 웹 SDK 확장

구현 작업의 개요:

![웹 SDK 확장 프로그램을 사용하여 Adobe Analytics 구현 워크플로우](../../assets/websdk-extension-annotated.png)

|<div style="width:20px"></div> | 작업 | 추가 정보 | |-| —|—| | 1 | 다음을 확인하십시오. **보고서 세트 정의**. | [보고서 세트 관리자](../../../admin/admin/c-manage-report-suites/report-suites-admin.md) | | 2 | **스키마 및 데이터 세트 설정**. Adobe Experience Platform을 활용하는 여러 애플리케이션에서 사용할 수 있도록 데이터 수집을 표준화하기 위해 Adobe은 개방적이고 공개적으로 문서화된 표준 XDM(Experience Data Model) 을 만들었습니다. | [스키마 UI 개요](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=ko-KR) 및 [데이터 세트 UI 개요](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=ko) | | 3 | **데이터 레이어 만들기** 를 사용하여 웹 사이트에서 데이터 추적을 관리할 수 있습니다. | [데이터 레이어 만들기](../../prepare/data-layer.md) | | 4 | **데이터 스트림 구성**. 데이터 스트림은 Adobe Experience Platform Web SDK를 구현할 때 서버측 구성을 나타냅니다. | [데이터 스트림 구성](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en) | | 5 | **Adobe Analytics 서비스 추가** 데이터 스트림에 추가 이 서비스는 Adobe Analytics으로 데이터를 전송할지 여부와 방법을 제어합니다. | [데이터 스트림에 Adobe Analytics 서비스 추가](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en#analytics) | | 6 | **태그 속성 만들기**. 속성은 태그 관리 데이터를 참조하는 데 사용되는 매우 중요한 컨테이너입니다.| [웹용 태그 속성 만들기 또는 구성](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html?lang=en#for-web) | | 7 | **웹 SDK 확장 설치 및 구성** 태그에 다음 코드를 배치하십시오. 4단계에서 구성된 데이터 스트림으로 데이터를 보내도록 Web SDK 확장을 구성합니다. | [Adobe Experience Platform 웹 SDK 확장 개요](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/sdk/overview.html?lang=en) | | 8 | **반복, 유효성 검사 및 게시** 프로덕션에 추가할 수 있습니다. 웹 사이트에 태그 속성을 추가합니다. 그런 다음 데이터 요소, 규칙 등을 사용하여 구현을 사용자 지정합니다. | [게시 개요](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/overview.html?lang=ko-KR) |



## 추가 리소스

태그는 높은 자유도로 사용자 정의할 수 있습니다. 구현에 적합한 데이터를 포함하여 Adobe Analytics를 최대한 활용할 수 있는 방법에 대해 자세히 알아봅니다.

- [태그 설명서](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html#): 인터페이스의 작동 방식과 이요 가능한 확장 유형에 대해 알아봅니다.

- [Adobe Experience Platform 웹 SDK 설명서](https://experienceleague.adobe.com/docs/web-sdk.html?lang=ko)
