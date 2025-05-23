---
title: 태그에 Analytics 속성 만들기
description: 태그를 사용하여 데이터 수집 방법을 사용자 정의할 공간을 만듭니다.
feature: Tags
exl-id: ffcd8e97-4d29-489e-bc2b-88805400dad5
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 100%

---

# Adobe Analytics 태그 속성 만들기

Adobe Experience Platform의 태그를 사용하면 웹 사이트에서 Experience Cloud 솔루션(Analytics 포함)을 통합할 수 있습니다. 이 페이지에서는 태그 관리자가 기본 Adobe Analytics 구현을 올바르게 구성하는 방법을 간략하게 설명합니다.

## 사전 요구 사항

[보고서 세트 만들기](/help/admin/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md): 수집할 Analytics 데이터에 대한 사일로 만들기.

## 태그 속성 만들기 및 중요한 확장 설치

속성은 태그를 관리하는 데 사용하는 중요한 컨테이너입니다. 확장을 사용하면 제품별 태그를 설치하고 구성할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. **[!UICONTROL 새 속성]**&#x200B;을 클릭합니다.
1. 속성 이름을 웹 사이트의 제목 등으로 지정하고 Analytics를 구현할 도메인을 입력합니다. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.
1. 새로 만든 태그 속성을 클릭하여 해당 설정을 입력합니다.
1. **[!UICONTROL 확장]** 탭을 클릭한 다음 **[!UICONTROL 카탈로그]**&#x200B;를 클릭합니다.
1. “Experience Cloud ID 서비스”를 찾은 다음 **[!UICONTROL 설치]**&#x200B;를 클릭합니다.
1. Experience Cloud 조직 ID를 비롯한 모든 설정은 이미 작성되어 있어야 합니다. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.
1. 확장 카탈로그로 돌아가 Adobe Analytics를 찾은 다음 **[!UICONTROL 설치]**&#x200B;를 클릭합니다.

자세한 내용은 [Adobe Analytics 확장](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html?lang=ko)에 대한 모든 내용이 들어 있는 문서를 참조하십시오.

## Adobe Analytics용 데이터 요소 만들기

데이터 요소는 변수 값을 수집하기 위한 사이트의 특정 부분에 대한 참조입니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 사이트에서 구현할 태그 속성을 클릭합니다.
1. **[!UICONTROL 데이터 요소]** 탭을 클릭한 다음 **[!UICONTROL 데이터 요소 추가]**&#x200B;를 클릭합니다.
1. 데이터 요소에 다음 설정을 지정합니다.

   * 이름: 페이지 이름
   * 확장: 핵심
   * 데이터 요소 유형: JavaScript 변수
   * JavaScript 변수 이름: `window.document.title`

     >[!NOTE]
     >
     >이 값은 시작하는 데 도움이 되는 예제입니다. 조직에서 페이지 이름에 데이터 계층 값과 같은 값을 정의한 경우 해당 값을 여기에 입력할 수 있습니다.
   * 텍스트 정리 선택
   * 저장소 유지 시간: 없음
1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## Adobe Analytics에 대한 규칙 만들기

규칙은 데이터 요소를 Analytics 변수 값에 매핑하고, 이러한 값을 언제 Adobe의 서버로 전송해야 하는지를 결정합니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
1. 사이트에서 구현할 태그 속성을 클릭합니다.
1. **[!UICONTROL 규칙]** 탭을 클릭한 다음 **[!UICONTROL 규칙 추가]**&#x200B;를 클릭합니다. 이름을 `Global Rule`로 지정합니다.
1. 이벤트 옆에 있는 **[!UICONTROL 추가]**&#x200B;를 클릭하고 다음 설정을 입력합니다.
   * 확장: 핵심
   * 이벤트 유형: 라이브러리가 로드됨 (페이지 상단)
   * 이름: 핵심 - 라이브러리가 로드됨 (페이지 상단)
1. **[!UICONTROL 변경사항 유지]**&#x200B;를 클릭합니다.
1. **[!UICONTROL 작업]**&#x200B;에서 **[!UICONTROL 추가]**&#x200B;를 클릭하고 다음 설정을 입력합니다.
   * 확장: Adobe Analytics
   * 작업 유형: 변수 설정
   * 페이지 이름: 컨테이너 아이콘을 클릭하고 `Page Name` 데이터 요소를 선택합니다.
   * 캠페인: 값이 `cid`인 쿼리 매개변수
1. **[!UICONTROL 변경사항 유지]**&#x200B;를 클릭합니다.
1. 다른 작업을 추가할 작업 옆에 있는 더하기 기호를 클릭하고 다음 설정을 입력합니다.
   * 확장: Adobe Analytics
   * 작업 유형: 비콘 전송
   * 이름: Adobe Analytics - 비콘 전송
   * 추적: s.t ()
1. **[!UICONTROL 변경사항 유지]**&#x200B;를 클릭합니다.
1. 이벤트와 두 작업을 설정했는지 확인한 다음 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## 다음 단계

[개발 환경에 Analytics 구현 배포](deploy-dev.md): 테스트 환경에서 작동하는 Analytics 코드를 가져옵니다.
