---
title: Launch에서 Analytics 속성 만들기
seo-title: Adobe Experience Platform Launch에서 Adobe Analytics 속성 만들기
description: Adobe Experience Platform Launch를 사용하여 데이터 수집 방법을 사용자 정의할 공간을 만듭니다.
seo-description: Adobe Experience Platform Launch를 사용하여 데이터를 Adobe Analytics에 수집하는 방법을 사용자 정의할 공간을 만듭니다.
translation-type: tm+mt
source-git-commit: 757cea821bae49fabe819a65b921797070d328fc

---


# Adobe Experience Platform Launch에서 Analytics 속성 만들기

Adobe Experience Platform Launch는 웹 사이트(Analytics 포함)에서 Experience Cloud 솔루션을 통합하는 데 사용할 수 있는 도구입니다. 이 페이지에서는 Launch 관리자가 기본 Adobe Analytics 구현을 올바르게 구성하는 방법을 간략하게 설명합니다.

## 전제 조건

[보고서 세트 만들기](/help/admin/admin-console/create-report-suite.md): 수집할 Analytics 데이터에 대한 사일로 만들기

## 속성 만들기 및 중요한 확장 설치

속성은 태그를 관리하는 데 사용하는 중요한 컨테이너입니다. 확장을 사용하면 제품별 태그를 설치하고 구성할 수 있습니다.

1. Go to [launch.adobe.com](https://launch.adobe.com) and log in if prompted.
1. 새 속성을 클릭합니다.
1. 속성 이름을 웹 사이트의 제목 등으로 지정하고 Analytics를 구현할 도메인을 입력합니다. 저장을 클릭합니다.
1. 새로 만든 속성을 클릭하여 해당 설정을 입력합니다.
1. 확장 탭을 클릭한 다음 카탈로그를 클릭합니다.
1. ID 서비스를 찾은 다음 설치를 클릭합니다.
1. Experience Cloud 조직 ID를 비롯한 모든 설정은 이미 작성되어 있어야 합니다. 저장을 클릭합니다.
1. 확장 카탈로그로 돌아가 Adobe Analytics를 찾은 다음 설치를 클릭합니다.

## Adobe Analytics용 데이터 요소 만들기

데이터 요소는 변수 값을 수집하기 위한 사이트의 특정 부분에 대한 참조입니다.

1. Go to [launch.adobe.com](https://launch.adobe.com) and log in if prompted.
2. 사이트에서 구현할 Launch 속성을 클릭합니다.
3. 데이터 요소 탭을 클릭한 다음 새 데이터 요소 만들기를 클릭합니다.
4. 데이터 요소에 다음 설정을 지정합니다.
   * 이름: 페이지 이름
   * 확장: 핵심
   * 데이터 요소 유형: JavaScript 변수
   * 변수 경로: `window.document.title`
      > [!NOTE] 참고: 시작하는 데 도움이 되는 예제 값입니다. 조직에서 페이지 이름에 데이터 계층 값과 같은 값을 정의한 경우 해당 값을 여기에 입력할 수 있습니다.
   * 텍스트 정리 선택
   * 기간: 페이지 보기
5. 저장을 클릭합니다.

## Adobe Analytics에 대한 규칙 만들기

규칙은 데이터 요소를 Analytics 변수 값에 매핑하고, 이러한 값을 언제 Adobe의 서버로 전송해야 하는지를 결정합니다.

1. Go to [launch.adobe.com](https://launch.adobe.com) and log in if prompted.
1. 사이트에서 구현할 Launch 속성을 클릭합니다.
1. 새 규칙 만들기를 클릭하고 이름을 `Global Rule`로 지정합니다.
1. 이벤트 옆에 있는 추가를 클릭하고 다음 설정을 입력합니다.
   * 확장: 핵심
   * 이벤트 유형: 라이브러리가 로드됨(페이지 상단)
   * 이름: 핵심 - 라이브러리가 로드됨(페이지 상단)
   * 주문: 50
1. Keep Changes를 클릭합니다.
1. 작업에서 추가를 클릭하고 다음 설정을 입력합니다.
   * 확장: Adobe Analytics
   * 작업 유형: 변수 설정
   * 페이지 이름: 컨테이너 아이콘을 클릭하고 `Page Name` 데이터 요소를 선택합니다.
   * 캠페인: 값이 `cid`인 쿼리 매개 변수
1. Keep Changes를 클릭합니다.
1. 다른 작업을 추가할 작업 옆에 있는 더하기 기호를 클릭하고 다음 설정을 입력합니다.
   * 확장: Adobe Analytics
   * 작업 유형: 비콘 전송
   * 이름: Adobe Analytics - 비콘 전송
   * 추적: s.t()
1. Keep Changes를 클릭합니다.
1. 이벤트와 두 작업을 설정했는지 확인한 다음 저장을 클릭합니다.

## 문서 및 추가 리소스

* [Adobe Analytics 확장 설명서](https://docs.adobelaunch.com/extension-reference/web/adobe-analytics-extension):Adobe Experience Platform Launch의 Adobe Analytics 확장 기능에 대한 전체 설명서입니다.
* [시작](https://docs.adobelaunch.com/getting-started):자세한 시작 안내서를 포함하여 Launch에 대한 전체 설명서
* [Adobe Experience Platform Launch YouTube 채널](https://www.youtube.com/channel/UCa84ntcvYhPArOBsZIRE2Jw/videos?view=0&shelf_id=0&sort=dd):비디오를 통해 Launch를 사용하는 방법 살펴보기

## 다음 단계

[개발 환경에 Analytics 구현 배포](deploy-dev.md): 테스트 환경에서 작동하는 Analytics 코드를 가져옵니다.
