---
title: Adobe Experience Platform Mobile SDK를 사용하여 Adobe Analytics 구현
description: Adobe Experience Platform 데이터 수집에서 Mobile SDK 확장 기능을 사용하여 Adobe Analytics로 데이터를 전송합니다.
source-git-commit: e6b40881a543b43c03b612c7e7b0d9bd09f44c0d
workflow-type: tm+mt
source-wordcount: '579'
ht-degree: 20%

---

# Adobe Experience Platform Mobile SDK를 사용하여 Adobe Analytics 구현

Adobe Experience Platform Mobile SDK는 모바일 앱에서 Adobe의 Experience Cloud 솔루션 및 서비스를 강화하는 데 도움이 됩니다. Android™, iOS 및 다양한 교차 플랫폼 개발 프레임워크에서 사용할 수 있습니다. 구성은 Adobe Experience Platform 데이터 수집을 통해 처리됩니다.
>[!IMPORTANT]
>
>Adobe Analytics 확장은 Adobe Experience Platform 데이터 수집 UI에서도 사용할 수 있습니다. 이 확장을 설치하는 경우 XDM 또는 Edge Network를 사용하지 않습니다.

## Adobe Experience Platform SDK

구현 작업의 개요:

![Analytics 확장 워크플로우를 사용한 Adobe Analytics](../../assets/mobilesdk-annotated.png)

|<div style="width:20px"></div>| 작업 | 추가 정보 | |-| —|—| | 1 | 다음을 확인하십시오. **보고서 세트 정의**. | [보고서 세트 관리자](../../../admin/admin/c-manage-report-suites/report-suites-admin.md) | | 2 | **스키마 및 데이터 세트 설정**. Adobe Experience Platform을 활용하는 여러 애플리케이션에서 사용할 수 있도록 데이터 수집을 표준화하기 위해 Adobe은 개방적이고 공개적으로 문서화된 표준 XDM(Experience Data Model) 을 만들었습니다. | [스키마 및 데이터 세트 설정](https://developer.adobe.com/client-sdks/documentation/getting-started/set-up-schemas-and-datasets/) | | 3 | **데이터 스트림 구성**. 데이터 스트림은 Adobe Experience Platform Web SDK를 구현할 때 서버측 구성을 나타냅니다. | [데이터 스트림 구성](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en) | | 4 | **Adobe Analytics 서비스 추가** 데이터 스트림에 추가 이 서비스는 Adobe Analytics으로 데이터를 전송할지 여부와 방법을 제어합니다. | [데이터 스트림에 Adobe Analytics 서비스 추가](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en#analytics) | | 5 | **모바일 속성 만들기**. 속성은 확장, 규칙, 데이터 요소 및 라이브러리로 채우는 컨테이너입니다. | [모바일 속성 설정](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/) | | 6 | **Adobe Experience Platform Edge Network 확장 설치** 모바일 태그 속성에서 데이터 스트림을 구성하고 확장에서 데이터 스트림을 구성합니다. | [Adobe Experience Platform Edge Network](https://developer.adobe.com/client-sdks/documentation/edge-network/) | | 7 | **앱에서 코드 사용** 필요한 확장을 등록하고 태그 구성을 로드합니다. | [구성 설정](https://developer.adobe.com/client-sdks/documentation/user-guides/getting-started-with-platform/overview/#set-up-the-configuration) | | 8 | **구현 및 테스트 기능** 앱에서 태그의 데이터 요소, 규칙, 추가 확장 및 SDK API 호출 조합을 사용합니다. 모바일 애플리케이션에 대한 데이터 수집 및 경험을 Inspect, 유효성 검사 및 디버깅합니다. | [샘플 애플리케이션 사용](https://developer.adobe.com/client-sdks/documentation/user-guides/getting-started-with-platform/overview/#use-the-sample-application) | | 9 | **모바일 앱 구현 확장 및 유효성 검사** 프로덕션에 투입하기 전에 | |


## Adobe Analytics 확장.

구현 작업의 개요:

![Analytics 확장 워크플로우를 사용한 Adobe Analytics](../../assets/mobilesdk-analytics-annotated.png)

|<div style="width:20px"></div> | 작업 | 추가 정보 | |-| —|—| | 1 | 다음을 확인하십시오. **보고서 세트 정의**. | [보고서 세트 관리자](../../../admin/admin/c-manage-report-suites/report-suites-admin.md) | | 2 | **모바일 속성 만들기**. 속성은 확장, 규칙, 데이터 요소 및 라이브러리로 채우는 컨테이너입니다. | [모바일 속성 설정](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/) | | 3 | **Adobe Analytics 확장 설치** 모바일 태그 속성에서 보고서 세트를 가리키도록 확장을 구성합니다. | [모바일 속성에 대한 Adobe Analytics 확장](https://developer.adobe.com/client-sdks/documentation/adobe-analytics/) | | 4 | **앱에서 코드 사용** 필요한 확장을 등록하고 태그 구성을 로드합니다. | [구성 설정](https://developer.adobe.com/client-sdks/documentation/user-guides/getting-started-with-platform/overview/#set-up-the-configuration) | | 5 | **구현 및 테스트 기능** 앱에서 태그의 데이터 요소, 규칙, 추가 확장 및 SDK API 호출 조합을 사용합니다. 모바일 애플리케이션에 대한 데이터 수집 및 경험을 Inspect, 유효성 검사 및 디버깅합니다. | [샘플 애플리케이션 사용](https://developer.adobe.com/client-sdks/documentation/user-guides/getting-started-with-platform/overview/#use-the-sample-application) | | 6 | **모바일 앱 구현 확장 및 유효성 검사** 프로덕션에 투입하기 전에 | |

## 추가 리소스

- [태그 설명서](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html#)

- [Mobile SDK 설명서](https://developer.adobe.com/client-sdks/documentation/)



