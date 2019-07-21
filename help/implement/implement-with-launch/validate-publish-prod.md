---
title: 개발 환경에 Adobe Analytics 배포
seo-title: 개발 환경에 Adobe Analytics 배포
description: Adobe Experience Platform Launch를 사용하여 개발 환경에 Adobe Analytics를 배포하는 방법을 살펴볼 수 있습니다.
seo-description: Adobe Experience Platform Launch를 사용하여 개발 환경에 Adobe Analytics를 배포하는 방법을 살펴볼 수 있습니다.
translation-type: tm+mt
source-git-commit: d195fb85711f58383577bf1d7b4da4078b909427

---


# 개발 구현 유효성 검사 및 프로덕션에 게시

Adobe Experience Platform Launch 라이브러리가 프로덕션에 푸시되면 조직은 Adobe Analytics를 사용하여 기본 보고서를 가져올 수 있습니다.

## 전제 조건

[Analytics 구현을 개발 환경에 배포합니다](deploy-dev.md). 이 페이지를 팔로우하려면 Analytics 구현을 개발 환경에 게시해야 합니다.

## Experience Cloud 디버거를 사용하여 개발 구현 유효성 검사

Experience Cloud Debugger는 페이지에 있는 모든 Experience Cloud 태그를 보여주는 Chrome 플러그인입니다.

1. [Chrome 웹 브라우저를](https://www.google.com/chrome/) 열고 Chrome 웹 스토어에서 [Adobe Experience Cloud Debugger](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj) 로 이동하여 익스텐션을 설치합니다.
2. 론치를 구현한 개발 웹 사이트로 이동합니다.
3. Chrome 오른쪽 상단에 있는 Adobe Experience Cloud Debugger 아이콘을 클릭합니다.
4. 모든 것이 제대로 구현되면 Adobe Analytics, Adobe Experience Platform Launch 및 Adobe Experience Cloud 방문자 ID 서비스 내의 컨텐츠가 표시됩니다.

![디버거][assets/debugger.png]

## 스테이징/프로덕션에 개발 구현 배포

데이터가 확인되고 있는 경우 구현을 사이트의 라이브 버전으로 푸시할 수 있습니다.

1. [Adobe Experience Platform Launch](https://launch.adobe.com) 로 이동하여 메시지가 표시되면 로그인합니다.
2. 사이트에서 구현할 론치 속성을 클릭합니다.
3. 게시 탭을 클릭하고 개발 열에서 라이브러리를 찾습니다.
4. 라이브러리에서 드롭다운을 클릭한 다음 승인을 위해 제출을 선택합니다. 모달 창에서 제출을 클릭합니다.
5. [제출됨] 열에서 라이브러리 드롭다운을 다시 클릭하고 스테이징용으로 빌드를 선택합니다.
6. 잠시 후 라이브러리의 노란색 색상이 녹색으로 바뀌어 성공적으로 구축되었음을 나타냅니다.
7. 라이브러리의 드롭다운을 다시 클릭하고 [게시 승인] 를 선택합니다.
8. 라이브러리 드롭다운을 다시 클릭하고 (현재 승인된 열에서) 제작 및 프로덕션에 게시를 선택합니다.
9. 환경 탭, 클릭 제작 환경으로 이동합니다.
10. 프로덕션 머리글 + 바닥글 코드를 복사하여 웹 사이트 소유자에게 제공합니다. 사이트 프로덕션 환경에서 이 코드를 구현하도록 요청합니다.

## 프로덕션 구현 유효성 확인

사이트의 라이브 버전에 데이터가 표시되는지 확인하고 Adobe Analytics에 대한 공식적인 데이터 수집을 시작합니다.

1. 웹 사이트 소유자가 론치 코드를 프로덕션에 푸시했음을 확인한 후 Chrome에서 웹 사이트 홈 페이지로 이동하여 Adobe Experience Cloud 디버거를 엽니다.
2. 모든 것이 작동한다면 개발 환경에서 비슷한 데이터를 테스트해야 합니다. 이제 사이트에서 데이터를 수집하고 이제 Adobe Analytics를 사용하여 보고할 수 있습니다.

## 문제 해결

**디버거에 데이터가 나타나지 않습니다.**

사이트에 있는 동안 브라우저의 개발자 콘솔 (일반적으로 F 12) 를 엽니다. 페이지의 소스 코드를 보고 다음을 충족하는지 확인합니다.

* 콘솔에 JavaScript 오류가 없습니다. 조직의 웹 사이트 소유자와 협력하여 모든 JS 오류가 해결되었는지 확인합니다.
* Header code is properly implemented: Make sure the header code is inside the `<head>` tag, and that the file exists.
* Appmeasurement 라이브러리가 존재함: JS 소스로 바로 이동하여 JS 파일에 코드가 들어 있는지 확인합니다. 그렇지 않은 경우 각 환경이 만들어지고 라이브러리가 해당 환경에 게시되는지 확인합니다.
* 간섭 플러그인: 일부 Chrome 플러그인은 이미지 요청이 실행되지 않도록 할 수 있습니다. 데이터를 Adobe 서버로 보내지 못하게 하는 플러그인을 비활성화합니다.

## 다음 단계

기본 구현이 설정되었으므로 조직 내에서 귀하의 역할에 대해 다음과 같이 자세히 알아볼 경로에 영향을 미칠 수 있습니다.

* [솔루션 디자인 문서 만들기](../prepare/solution-design.md): 사용자 지정 변수를 사용하는 방법에 대한 계획을 만든 다음 구현에 포함
* [분석 작업 공간 사용을 시작하십시오](../../analyze/analysis-workspace/home.md). 툴의 주요 기능을 사용하여 Adobe Analytics로 바로 이동할 수 있습니다.
