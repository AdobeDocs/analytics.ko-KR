---
description: Adobe Analytics에서 Dynamic Tag Management를 수동으로 배포할 때 AppMeasurement 코드를 삽입합니다.
keywords: Dynamic Tag Management;linked accounts;linking accounts;edit code;appmeasurement;appmeasurement code
solution: Experience Cloud,Analytics,Target,Dynamic Tag Management
title: 핵심 AppMeasurement 코드 삽입
uuid: 3f83fbb1-3ed5-4e45-888a-0a183aac1a90
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 핵심 AppMeasurement 코드 삽입

Adobe Analytics에서 Dynamic Tag Management를 수동으로 배포할 때 AppMeasurement 코드를 삽입합니다.

1. [!DNL Adobe Analytics] 도구 페이지에서 **[!UICONTROL 일반]** 섹션을 확장한 다음 **[!UICONTROL 편집기 열기]**&#x200B;를 클릭합니다.
1. [!DNL AppMeasurement_JavaScript*.zip]Adobe Analytics 배포[에서 다운로드한 ](/help/implement/c-implement-with-dtm/t-analytics-deploy.md) 파일의 압축을 풉니다.

   사용자 지정 라이브러리를 선택하고 창을 열면 가장 최신의 코드 버전이 이미 표시되어 나타나므로 관리 콘솔에서 zip 파일을 다운로드하지 않아도 됩니다.
1. 텍스트 편집기에서 [!DNL AppMeasurement.js]를 엽니다.
1. 콘텐츠를 복사해 **[!UICONTROL 코드 편집]** 창에 붙여넣습니다.

   ![](assets/edit-code.png)

1. Adobe는 *`Do Not Alter Anything Below This Line`*:

   ```
   var s_account="INSERT-RSID-HERE"
   var s=s_gi(s_account)
   ```

   >[!IMPORTANT]
   >
   >이 코드를 추가할 경우 전체 라이브러리 설정에서 **[!UICONTROL 아래의 사용자 지정 코드를 사용한 보고서 세트 설정]** 확인란도 선택하는 것이 좋습니다.

1. **[!UICONTROL 저장 후 닫기]**&#x200B;를 클릭합니다.

   미디어 모듈, 통합 모듈 또는 구현 플러그인을 사용 중인 경우, 복사하여 코드 섹션에도 붙여넣을 수 있습니다. Dynamic Tag Management의 관리되는 코드는 일반적인 구현의 JavaScript 파일처럼 구성할 수 있습니다.

