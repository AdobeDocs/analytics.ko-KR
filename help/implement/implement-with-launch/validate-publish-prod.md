---
title: 개발 환경에 Adobe Analytics 배포
seo-title: 개발 환경에 Adobe Analytics 배포
description: Adobe Experience Platform Launch를 사용하여 Adobe Analytics를 개발 환경에 배포하는 방법에 대해 알아봅니다.
seo-description: Adobe Experience Platform Launch를 사용하여 Adobe Analytics를 개발 환경에 배포하는 방법에 대해 알아봅니다.
translation-type: ht
source-git-commit: d195fb85711f58383577bf1d7b4da4078b909427

---


# 개발 구현 유효성 검사 및 프로덕션에 게시

Adobe Experience Platform Launch 라이브러리가 프로덕션에 푸시되면 조직은 Adobe Analytics를 사용하여 기본 보고서를 가져오기를 시작할 수 있습니다.

## 전제 조건

[개발 환경에 Adobe Analytics 배포](deploy-dev.md): 이 페이지를 따라 진행하려면 개발 환경에 Analytics 구현을 게시해야 합니다.

## Experience Cloud 디버거를 사용하여 개발 구현 확인

Experience Cloud 디버거는 페이지에 있는 모든 Experience Cloud 태그를 표시하는 Chrome 플러그인입니다.

1. [Chrome 웹 브라우저](https://www.google.com/chrome/)를 열고 Chrome 웹 사이트에서 [Adobe Experience Cloud 디버거](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj)로 이동하여 확장을 설치합니다.
2. Launch를 구현한 개발 웹 사이트로 이동합니다.
3. Chrome의 오른쪽 위에 있는 Adobe Experience Cloud 디버거 아이콘을 클릭합니다.
4. 모든 것이 제대로 구현된 경우 Adobe Analytics, Adobe Experience Platform Launch 및 Adobe Experience Cloud 방문자 ID 서비스 내에 다음과 같은 콘텐츠가 표시됩니다.

![디버거][assets/debugger.png]

## 스테이징/프로덕션에 개발 구현 배포

데이터가 표시되는지 확인했으면 구현을 사이트의 라이브 버전에 푸시할 수 있습니다.

1. [Adobe Experience Platform Launch](https://launch.adobe.com)로 이동한 후 메시지가 표시되면 로그인합니다.
2. 사이트에서 구현할 Launch 속성을 클릭합니다.
3. 게시 탭을 클릭하고 개발 열에서 라이브러리를 찾습니다.
4. 라이브러리의 드롭다운을 클릭한 다음 승인을 위해 제출을 선택합니다. 모달 창에서 제출을 클릭합니다.
5. 라이브러리의 드롭다운을 다시 클릭하고(이제 제출됨 열에서) 스테이징을 위해 빌드를 선택합니다.
6. 잠시 후에 라이브러리의 노란색 색상 표시등이 빌드가 성공했음을 나타내는 녹색으로 바뀝니다.
7. 라이브러리의 드롭다운을 다시 클릭하고 게시를 위해 승인을 선택합니다.
8. 라이브러리의 드롭다운을 다시 클릭하고(이제 승인됨 열에서) 프로덕션에 빌드 및 게시를 선택합니다.
9. 환경 탭으로 이동하여 프로덕션 환경을 클릭합니다.
10. 프로덕션 머리글 + 바닥글 코드를 복사하여 웹 사이트 소유자에게 제공합니다. 사이트의 프로덕션 환경에서 이 코드를 구현하도록 요청합니다.

## 프로덕션 구현 확인

사이트의 라이브 버전에서 데이터가 표시되는지 확인하고 Adobe Analytics에 대한 공식 데이터 수집을 시작합니다.

1. 웹 사이트 소유자로부터 Launch 코드를 프로덕션에 푸시했다는 확인을 받으면 Chrome에서 웹 사이트의 홈 페이지로 이동하여 Adobe Experience Cloud 디버거를 엽니다.
2. 모든 기능이 작동하면 개발 환경의 테스트와 유사한 데이터가 표시됩니다. 이제 사이트에서 데이터를 수집하고 있으므로 Adobe Analytics를 사용하여 보고를 시작할 수 있습니다.

## 문제 해결

**디버거에 데이터가 표시되지 않습니다.**

사이트에서 브라우저의 개발자 콘솔을 엽니다(일반적으로 F12). 페이지의 소스 코드에서 다음을 충족하는지 확인합니다.

* 콘솔에 JavaScript 오류가 없습니다. 조직의 웹 사이트 소유자와 함께 모든 JS 오류가 해결되었는지 확인합니다.
* 헤더 코드가 올바르게 구현됨: 헤더 코드가 `<head>` 태그 내에 있고 파일이 있는지 확인합니다.
* AppMeasurement 라이브러리가 있음: JS 소스로 직접 이동하여 JS 파일에 코드가 포함되어 있는지 확인합니다. 코드가 포함되어 있지 않으면 각 환경이 만들어졌는지, 라이브러리가 각각의 환경에 게시되었는지 확인합니다.
* 플러그인 방해: 일부 Chrome 플러그인으로 인해 이미지 요청이 실행되지 않을 수도 있습니다. Adobe 서버로 데이터가 전송되지 않도록 하는 플러그인을 비활성화합니다.

## 다음 단계

기본 구현이 설정되었으므로 조직 내에서 귀하의 역할이 다음 사항에 대해 학습할 경로에 영향을 줄 수 있습니다.

* [솔루션 디자인 문서 만들기](../prepare/solution-design.md): 사용자 지정 변수를 사용할 방법을 계획한 다음 구현에 포함시킵니다.
* [Analysis Workspace 사용하기](../../analyze/analysis-workspace/home.md): 도구의 주요 기능을 사용하여 Adobe Analytics를 바로 사용해 보십시오.
