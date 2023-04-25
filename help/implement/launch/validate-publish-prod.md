---
title: 개발 구현 유효성 검사 및 프로덕션에 퍼블리싱
description: Adobe Experience Platform 태그를 사용하여 Adobe Analytics를 프로덕션 환경에 배포하는 방법에 대해 알아봅니다.
feature: Launch Implementation
exl-id: 2f5bcfee-d75e-4dac-bea9-91c6cc545173
source-git-commit: 78cfb1f3c4d45fc983982a8da11b66f2b2c9ecbc
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 91%

---

# 개발 구현 유효성 검사 및 프로덕션에 퍼블리싱

태그 라이브러리를 프로덕션에 푸시하고 나면 조직에서 Adobe Analytics를 사용하여 기본 보고서를 가져올 수 있습니다.

## 사전 요구 사항

[개발 환경에 Adobe Analytics 배포](deploy-dev.md): 이 페이지를 따라 진행하려면 개발 환경에 Analytics 구현을 게시해야 합니다.

## Experience Cloud 디버거를 사용하여 개발 구현 확인

Experience Cloud 디버거는 페이지에 있는 모든 Experience Cloud 태그를 표시하는 확장 프로그램입니다.

1. [Chrome](https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob) 또는 [Firefox](https://addons.mozilla.org/ko-KR/firefox/addon/adobe-experience-platform-dbg/)용 확장 프로그램을 설치합니다.
2. 태그를 구현한 개발 웹 사이트로 이동합니다.
3. 브라우저에 있는 Adobe Experience Cloud 디버거 아이콘을 클릭합니다.
4. 모든 항목이 올바르게 구현되면 Adobe Analytics 내 콘텐츠, 태그 및 Adobe Experience Cloud 방문자 ID 서비스가 표시됩니다.

## 스테이징/프로덕션에 개발 구현 배포

데이터가 표시되는지 확인했으면 구현을 사이트의 라이브 버전에 푸시할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 사이트에서 구현할 태그 속성을 클릭합니다.
1. **[!UICONTROL 퍼블리싱]** 탭을 클릭하고 개발 열에서 라이브러리를 찾습니다.
1. 라이브러리에서 드롭다운 목록을 클릭한 다음 을 선택합니다 **[!UICONTROL 승인을 위한 제출]**. 모달 창에서 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.
1. 라이브러리의 드롭다운 목록을 다시 클릭하고(이제 제출됨 열에서) 을 선택합니다 **[!UICONTROL 스테이징용 빌드]**.
1. 잠시 후에 라이브러리의 노란색 색상 표시등이 빌드가 성공했음을 나타내는 녹색으로 바뀝니다.
1. 라이브러리의 드롭다운 목록을 다시 클릭하고 을 선택합니다 **[!UICONTROL 게시 승인]**.
1. 라이브러리의 드롭다운 목록을 다시 클릭합니다(이제 [!UICONTROL 승인됨] 열), **[!UICONTROL 빌드 및 프로덕션에 게시]**.
1. 환경 탭으로 이동한 다음 **[!UICONTROL 프로덕션 환경]**&#x200B;을 클릭합니다.
1. 프로덕션 설치 코드를 복사하여 웹 사이트 소유자에게 제공합니다. 사이트의 프로덕션 환경에서 이 코드를 구현하도록 요청합니다.

## 프로덕션 구현 확인

사이트의 라이브 버전에서 데이터가 표시되는지 확인하고 Adobe Analytics에 대한 공식 데이터 수집을 시작합니다.

1. 웹 사이트 소유자가 프로덕션에 태그 코드를 푸시했음을 확인한 후, Chrome에서 웹 사이트 홈페이지로 이동하고 [!UICONTROL Adobe Experience Cloud Debugger]를 엽니다.
2. 모든 기능이 작동하면 개발 환경의 테스트와 유사한 데이터가 표시됩니다. 이제 사이트에서 데이터를 수집하고 있으므로 Adobe Analytics를 사용하여 보고를 시작할 수 있습니다.

## 문제 해결

**디버거에 데이터가 표시되지 않습니다.**

사이트에서 브라우저의 개발자 콘솔을 엽니다(일반적으로 F12). 페이지의 소스 코드에서 다음을 충족하는지 확인합니다.

* 콘솔에 JavaScript 오류가 없습니다. 조직의 웹 사이트 소유자와 함께 모든 JS 오류가 해결되었는지 확인합니다.
* 헤더 코드가 올바르게 구현됨: 헤더 코드가 `<head>` 태그 내에 있고 파일이 있는지 확인합니다.
* AppMeasurement 라이브러리가 있음: JS 소스로 직접 이동하여 JS 파일에 코드가 포함되어 있는지 확인합니다. 코드가 포함되어 있지 않으면 각 환경이 만들어졌는지, 라이브러리가 각각의 환경에 게시되었는지 확인합니다.
* 확장 프로그램 방해: 광고 차단기와 같은 일부 확장 프로그램으로 인해 이미지 요청이 실행되지 않을 수 있습니다. Adobe로 데이터가 전송되지 않도록 하는 확장 프로그램을 비활성화합니다.

## 다음 단계

이제 기본 구현이 설정되었으므로 다음 경로 중에서 어떤 것에 대해 자세히 알아볼 것 인지에는 조직 내 역할이 영향을 줄 수 있습니다.

* [솔루션 디자인 문서 만들기](../prepare/solution-design.md): 사용자 정의 변수를 사용할 방법을 계획한 다음 구현에 포함시킵니다.
* [Analysis Workspace 사용하기](/help/analyze/analysis-workspace/home.md): 도구의 주요 기능을 사용하여 Adobe Analytics를 바로 사용하여 보십시오.
