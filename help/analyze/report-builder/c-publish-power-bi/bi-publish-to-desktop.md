---
description: Report Builder에서 게시한 자산을 Power BI Desktop에 가져오는 방법을 설명합니다.
title: 게시된 자산을 Power BI Desktop에 가져오기
uuid: ef47d5c7-31e0-44fc-a792-bc9d12bb089e
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 게시된 자산을 Power BI Desktop에 가져오기

Report Builder에서 게시한 자산을 Power BI Desktop에 가져오는 방법을 설명합니다.

## 전제 조건 {#section_BDFDAE1E300B429FB6EBCB21AD1383A0}

* 최신 Power BI Desktop 버전이 설치되어 있어야 합니다(2017년 4월 릴리스).
* 이 프로세스에서는 이미 Report Builder에서 형식을 지정한 표나 요청을 Power BI 서비스에 게시했다고 가정합니다.

## 프로세스 {#section_CB03E6E1B066457EA0F6FC08FFF5EFDD}

Microsoft는 Power BI Desktop의 2017년 4월 업데이트에서 Power BI 서비스의 데이터 세트에 연결하는 기능을 발표했습니다. 이 기능을 사용하면 이미 클라우드에 게시한 기존의 데이터 세트에서 새 보고서를 생성할 수 있고, 팀에서 공동 작업을 더 잘 수행하고 중복되는 노력을 줄일 수 있습니다.

1. In Power BI Desktop, go to **[!UICONTROL File]** &gt; **[!UICONTROL Options and settings]** &gt; **[!UICONTROL Options]** &gt; **[!UICONTROL Preview features.]**
1. Enable **[!UICONTROL Power BI Service Live Connection]** and click **[!UICONTROL OK]**. ![](assets/bi-preview-features.png)

1. Power BI Desktop을 시작합니다.
1. **[!UICONTROL 데스크탑을 다시 시작한 후 홈 &gt;]**&#x200B;데이터&#x200B;**[!UICONTROL 가져오기]**&gt;**[!UICONTROL 자세히]**...로 이동합니다..
1. **[!UICONTROL Power BI 서비스를 검색하여 선택합니다]**.
1. Under **[!UICONTROL Microsoft Power BI service]** &gt; **[!UICONTROL My Workspace]**, select the dataset that you had previously published from Report Builder.

자세한 내용은 이 [Microsoft 블로그 게시물](https://powerbi.microsoft.com/en-us/blog/connecting-to-datasets-in-the-power-bi-service-from-desktop/)을 참조하십시오.
