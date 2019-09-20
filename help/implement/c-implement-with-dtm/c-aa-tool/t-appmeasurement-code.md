---
description: Adobe Analytics에서 다이내믹 태그 관리를 수동으로 배포할 때 AppMeasurement 코드를 삽입합니다.
keywords: 다이내믹 태그 관리;연결된 계정;계정 연결;코드 편집;appmeasurement;appmeasurement 코드
seo-description: Adobe Analytics에서 다이내믹 태그 관리를 수동으로 배포할 때 AppMeasurement 코드를 삽입합니다.
seo-title: 핵심 AppMeasurement 코드 삽입
solution: Experience Cloud,Analytics,Target,다이내믹 태그 관리
title: 핵심 AppMeasurement 코드 삽입
uuid: 3f83fbb1-3ed5-4e45-888a-0a183aac1a90
translation-type: tm+mt
source-git-commit: e060fb745d611f37f28708b3fe103c1191aa483b

---


# 핵심 AppMeasurement 코드 삽입

Adobe Analytics에서 다이내믹 태그 관리를 수동으로 배포할 때 AppMeasurement 코드를 삽입합니다.

1. On the [!DNL Adobe Analytics] tool page, expand the **[!UICONTROL General]** section, then click **[!UICONTROL Open Editor]**.
1. Unzip the [!DNL AppMeasurement_JavaScript*.zip] file you downloaded in [deploy Adobe Analytics](../../../implement/c-implement-with-dtm/t-analytics-deploy.md#task_3A00639CADF14C9C844F962222077E4E).

   사용자 지정 라이브러리를 선택하고 창을 열면 가장 최신의 코드 버전이 이미 표시되어 나타나므로 관리 콘솔에서 zip 파일을 다운로드하지 않아도 됩니다.
1. Open [!DNL AppMeasurement.js] in a text editor.
1. Copy and paste the contents into the **[!UICONTROL Edit Code]** window.

   ![](assets/edit-code.png)

1. Adobe는 *`Do Not Alter Anything Below This Line`*:

   ```
   var s_account="INSERT-RSID-HERE"
   var s=s_gi(s_account)
   ```

   >[!IMPORTANT]
   >
   >If you add this code, it is recommended that you also select the **[!UICONTROL Set report suites using custom code below]** checkbox in the overall library settings.

1. Click **[!UICONTROL Save and Close]**.

   미디어 모듈, 통합 모듈 또는 구현 플러그인을 사용 중인 경우, 복사하여 코드 섹션에도 붙여넣을 수 있습니다. 다이내믹 태그 관리의 관리되는 코드는 일반적인 구현의 JavaScript 파일처럼 구성할 수 있습니다.

