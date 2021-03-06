---
title: Adobe Analytics 구현
description: 사이트, 속성 또는 애플리케이션에서 Adobe Analytics를 구현합니다.
feature: Implementation Basics
exl-id: 2b629369-2d69-4dc6-861a-ff21a46d39e0
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: ht
source-wordcount: '430'
ht-degree: 100%

---

# Adobe Analytics 구현

![배너](../../assets/doc_banner_implement.png)

다음은 Adobe Analytics에 대한 비디오 개요입니다.

>[!VIDEO](https://video.tv.adobe.com/v/27429/?quality=12)

Adobe의 데이터를 데이터 수집 서버에 전송하려면 사이트 또는 앱에 코드가 있어야 합니다. 다음 절차는 일반적인 구현의 작동 방식을 나타냅니다.

1. 방문자가 사이트에 도달하면 웹 서버에 요청이 만들어집니다.
2. 사이트의 웹 서버에서는 페이지 코드 정보를 보내고, 브라우저 페이지가 표시됩니다.
3. 페이지가 로드되고, Analytics JavaScript 코드가 실행됩니다.
JavaScript 코드가 이미지 요청을 Adobe 데이터 수집 서버에 전송합니다. 구현에서 정의한 페이지 데이터는 이 이미지 요청에서 쿼리 문자열의 일부로 전송됩니다.

4. Adobe에서 투명한 픽셀 이미지를 반환합니다.
5. Adobe 서버는 수집된 데이터를 하나 이상의 *보고서 세트*&#x200B;에 저장합니다.
6. 보고서 세트 데이터는 웹 브라우저에서 액세스할 수 있는 보고서를 채웁니다.

   JavaScript 코드 실행은 매우 신속하게 수행되며 페이지 로드 시간에 그다지 영향을 주지 않습니다. 이 접근 방식을 사용하면 캐시에서 페이지를 검색했을 때에도 JavaScript가 실행되므로 방문자가 **[!UICONTROL 다시 로드]**&#x200B;나 **[!UICONTROL 뒤로]**&#x200B;를 클릭하여 페이지에 도달했을 때 표시된 페이지를 계산할 수 있습니다.

Adobe Analytics에서 데이터 수집 서버에 데이터를 전송하려면 웹 사이트, 모바일 앱 또는 기타 애플리케이션 내에 코드가 있어야 합니다. 플랫폼과 조직의 요구 사항에 따라 이 코드를 구현하는 방법에는 몇 가지가 있습니다.

* **Web SDK**: Adobe Analytics 구현을 위한 표준화된 권장 방법입니다. Adobe Experience Platform 데이터 수집에 Web SDK 확장을 설치하고, 각 페이지에 로더 태그를 사용하고, 조직에 편리한 형식으로 Adobe Experience Platform Edge에 데이터를 보냅니다. Experience Edge는 들어오는 데이터를 올바른 형식으로 Adobe Analytics에 전달합니다.
* **Adobe Analytics 확장**: Adobe Experience Platform 데이터 수집에서 Adobe Analytics 확장을 설치합니다. 각 페이지에 로더 태그를 배치하고 Analytics 확장을 사용하여 각 변수가 정의되는 방식을 결정합니다.
* **기존 JavaScript**: Adobe Analytics를 구현하는 과거의 수동 방법입니다. 구현에서 사용되는 변수 및 설정을 간략하게 설명합니다. 이는 사용자 정의 코드가 있는 규칙을 사용하는 구현에 유용할 수 있습니다.
* **Mobile SDK**: 모바일 앱 내에서 데이터를 Adobe에 쉽게 전송할 수 있는 전용 라이브러리입니다.

## 주요 Analytics 구현 문서

* [기존 Adobe Analytics 구현 관리](/help/implement/prepare/existing-implementation.md)
* [Adobe Debugger](validate/debugger.md)
* [Experience Platform의 태그 속성 만들기](launch/create-analytics-property.md)
* [AppMeasurement 업데이트](appmeasurement-updates.md)

## 기타 Analytics 사용 안내서

[Analytics 사용자 안내서](https://experienceleague.adobe.com/docs/analytics.html)

## 주요 Analytics 리소스

* [고객 지원 문의](https://experienceleague.adobe.com/?support-solution=Analytics#support)
* [Analytics 포럼](https://forums.adobe.com/community/experience-cloud/analytics-cloud/analytics)
* [Adobe Analytics 리소스](https://forums.adobe.com/message/10660755)
* [Experience League](https://landing.adobe.com/experience-league/)
