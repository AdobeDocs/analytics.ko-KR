---
description: 미리 정의한 필터로 경로 보고서를 만드는 방법을 설명합니다.
solution: Analytics
title: 종속 요청을 추가하여 경로 보고서 필터링
topic: Report builder
uuid: dd1294f8-a26b-4254-a9f6-1365b2912adf
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 종속 요청을 추가하여 경로 보고서 필터링

미리 정의한 필터로 경로 보고서를 만드는 방법을 설명합니다.

마케팅 Reports &amp; Analytics은 [!UICONTROL 다음] 및 [!UICONTROL 이전 사이트 섹션] 보고서, 시작 및 [!UICONTROL 종료 사이트 섹션] 보고서, [!UICONTROL 단일 사이트 섹션] 보고서와 같이 미리 정의된 필터가 있는 상위 경로 보고서에 해당하는 일부 독립 실행형 보고서를 제공합니다.

Report Builder does not offer these as standalone reports, but you can create them through the **[!UICONTROL Add dependent request]** &gt; **[!UICONTROL Path]** context menus. 다음 보고서를 사용할 수 있습니다.

* 경로 &gt; 페이지 폴아웃
* 경로 &gt; 시작 경로
* 경로 &gt; 종료 경로
* 경로 &gt; 다음 페이지
* 경로 &gt; 시작 페이지 &gt; 다음 페이지
* 경로 &gt; 이전 페이지
* 경로 &gt; 종료 경로 &gt; 이전 페이지
* 경로 &gt; 시작 경로 &gt; 시작 페이지로
* 경로 &gt; 종료 경로 &gt; 종료 페이지로

1. Select multiple rows from an existing request, then right-click **[!UICONTROL Add Dependent Request]** &gt; **[!UICONTROL Path]**.

   (**[!UICONTROL 페이지 폴아웃]메뉴 항목을 표시하려면 3개 이상의 행을 선택해야 합니다.)**

   ![](assets/dependen_request.png)

1. Select the predefined filter, for example **[!UICONTROL Previous Page]**.

   이전 페이지 지표가 이미 선택된 상태로 요청 마법사가 나타납니다. 1.요청 마법사에서 요청을 계속 세분화하고 요청을 생성합니다.
