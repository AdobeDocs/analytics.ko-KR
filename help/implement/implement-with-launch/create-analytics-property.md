---
title: 론치에 Analytics 속성 만들기
seo-title: Adobe Experience Platform Launch에서 Adobe Analytics 속성 만들기
description: Adobe Experience Platform Launch를 사용하여 데이터를 수집하는 방법을 사용자 정의하는 공간을 만듭니다.
seo-description: Adobe Experience Platform Launch를 사용하여 Adobe Analytics에서 데이터가 수집되는 방식을 사용자 정의하는 공간을 만듭니다.
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# Adobe Experience Platform Launch에서 Analytics 속성 만들기

Adobe Experience Platform Launch는 웹 사이트 (분석 포함) 에서 Experience Cloud 솔루션을 통합하는 데 사용할 수 있는 툴입니다. 이 페이지에서는 론치 관리자가 기본적인 Adobe Analytics 구현을 올바르게 구성한 방법을 대략적으로 설명합니다.

## 전제 조건

[보고서 세트 만들기](../../admin/admin-console/create-report-suite.md): 수집할 Analytics 데이터에 대한 분산된 항목 만들기

## 속성 만들기 및 중요 확장 설치

속성은 태그를 관리하는 데 사용하는 중요한 컨테이너입니다. 익스텐션을 사용하면 제품별 태그를 설치하고 구성할 수 있습니다.

1. [launch.adobe.com](https://launch.adobe.com) 로 이동하여 메시지가 표시되면 로그인합니다.
1. ' 새 속성'을 클릭합니다.
1. 속성에 웹 사이트의 제목과 같은 이름을 지정하고 분석을 구현할 도메인을 입력합니다. 저장을 클릭합니다.
1. 새로 만든 속성을 클릭하여 설정을 입력합니다.
1. 확장 탭을 클릭한 다음 카탈로그를 클릭합니다.
1. ID 서비스를 찾은 다음 설치를 클릭합니다.
1. Experience Cloud 조직 ID를 비롯한 모든 설정은 이미 기재되어 있어야 합니다. 저장을 클릭합니다.
1. Extensions Catalog에서 Adobe Analytics를 찾아 설치를 클릭합니다.

## Adobe Analytics 용 데이터 요소 만들기

데이터 요소는 사이트의 특정 부분에 대한 참조로서 변수 값을 수집합니다.

1. [launch.adobe.com](https://launch.adobe.com) 로 이동하여 메시지가 표시되면 로그인합니다.
2. 사이트에서 구현할 론치 속성을 클릭합니다.
3. 데이터 요소 탭을 클릭한 다음 새 데이터 요소 만들기를 클릭합니다.
4. 데이터 요소에 다음 설정을 지정합니다.
   * 이름: 페이지 이름
   * 익스텐션: core
   * 데이터 요소 유형: JavaScript 변수
   * Path to variable: `window.document.title`
      > [!NOTE] 참고: 시작하는 데 도움이 되는 예제 값입니다. 조직에서 데이터 레이어 값과 같은 페이지 이름에 더 나은 값을 정의하는 경우 여기에 입력할 수 있습니다.
   * 깔끔한 텍스트 선택
   * 지속 시간: Pageview
5. 저장을 클릭합니다.

## Adobe Analytics 규칙 만들기

규칙은 데이터 요소를 Analytics 변수 값에 매핑하고 이러한 값이 Adobe 서버로 전송되는 시기를 결정합니다.

1. [launch.adobe.com](https://launch.adobe.com) 로 이동하여 메시지가 표시되면 로그인합니다.
1. 사이트에서 구현할 론치 속성을 클릭합니다.
1. Click Create New Rule and name it `Global Rule`.
1. 이벤트 옆에 있는 추가를 클릭하고 다음 설정을 입력합니다.
   * 익스텐션: core
   * 이벤트 유형: 라이브러리 로드됨 (페이지 상단)
   * 이름: Core - 라이브러리 로드됨 (페이지 상단)
   * 주문: 50
1. 변경 내용 유지를 클릭합니다.
1. [동작] 아래에서 [추가] 를 클릭하고 다음 설정을 입력합니다.
   * 익스텐션: Adobe Analytics
   * 작업 유형: 변수 설정
   * Page Name: click the container icon, and select the `Page Name` data element.
   * Campaign: Query parameter with a value of `cid`
1. 변경 내용 유지를 클릭합니다.
1. 동작 옆에 있는 더하기 기호를 클릭하여 다른 작업을 추가하고 다음 설정을 입력합니다.
   * 익스텐션: Adobe Analytics
   * 작업 유형: 비콘 보내기
   * 이름: Adobe Analytics - 비콘 보내기
   * 추적: s. t ()
1. 변경 내용 유지를 클릭합니다.
1. 이벤트와 두 개의 작업 세트가 있는지 확인한 다음 저장을 클릭합니다.

## 설명서 및 추가 리소스

* [Adobe Analytics 확장 설명서](https://docs.adobelaunch.com/extension-reference/web/adobe-analytics-extension): Adobe Experience Platform Launch의 Adobe Analytics 익스텐션에 특화된 전체 설명서입니다.
* [론치 시작](https://docs.adobelaunch.com/getting-started): 상세한 시작 안내서 포함 Launch에 대한 전체 설명서
* [Adobe Experience Platform, YouTube 채널 출시](https://www.youtube.com/channel/UCa84ntcvYhPArOBsZIRE2Jw/videos?view=0&shelf_id=0&sort=dd): 비디오에 Launch를 사용하는 방법 학습

## 다음 단계

[Analytics 구현을 개발 환경에 배포합니다](deploy-dev.md). 테스트 환경에서 작동하는 Analytics 코드를 가져옵니다.
