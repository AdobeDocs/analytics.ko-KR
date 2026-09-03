---
description: Report Builder에서 게시한 자산을 Power BI Desktop에 가져오는 방법을 설명합니다.
title: 게시된 자산을 Power BI Desktop에 가져오기
feature: Report Builder
role: User, Admin
exl-id: ce6020df-caf4-4cd2-8086-4357309e5bbb
TQID: https://experienceleague.adobe.com/fS1xnUciNh8LdPw2ENYMJTDGLqo3C8u4lu39X-GYuZE
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
subfeature_v2: id: ac8a38fa-dec3-4581-8f64-178fde9f64e8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 222
ht-degree: 60%

---

# 게시된 자산을 Power BI Desktop에 가져오기

{{legacy-arb}}

Report Builder에서 게시한 자산을 Power BI Desktop에 가져오는 방법을 설명합니다.

## 사전 요구 사항 {#section_BDFDAE1E300B429FB6EBCB21AD1383A0}

* 최신 Power BI 데스크탑 버전(2017년 4월 릴리스)이 설치되어 있어야 합니다
* 이 프로세스에서는 사용자가 이미 Report Builder 형식의 테이블 또는 요청을 Power BI 서비스에 게시했다고 가정합니다.

## 프로세스 {#section_CB03E6E1B066457EA0F6FC08FFF5EFDD}

Microsoft은 2017년 4월 Power BI 데스크탑 업데이트에서 Power BI 서비스의 데이터 세트에 연결하는 기능을 발표했습니다. 이 기능을 사용하면 이미 클라우드에 게시한 기존 데이터 세트에서 새 보고서를 만들 수 있습니다. 이 기능을 사용하면 팀 전체에서 더 효과적으로 공동 작업을 수행하고 중복 작업을 줄일 수 있습니다.

1. Power BI Desktop에서 **[!UICONTROL 파일]** > **[!UICONTROL 옵션 및 설정]** > **[!UICONTROL 옵션]** > **[!UICONTROL 기능 미리보기]**&#x200B;로 이동합니다.
1. **[!UICONTROL Power BI 서비스 라이브 연결]**&#x200B;을 활성화하고 **[!UICONTROL 확인]**&#x200B;을 클릭합니다. ![Power BI 서비스 라이브 연결을 클릭한 다음 확인을 클릭합니다. ](assets/bi-preview-features.png)

1. Power BI Desktop을 시작합니다.
1. 데스크탑을 시작한 후 **[!UICONTROL 홈]** > **[!UICONTROL 데이터 가져오기]** > **[!UICONTROL 더 보기]**&#x200B;로 이동합니다.
1. **[!UICONTROL Power BI 서비스]**&#x200B;를 검색하여 선택합니다.
1. **[!UICONTROL Microsoft Power BI 서비스]** > **[!UICONTROL 내 작업 영역]** 아래에서 이전에 Report Builder에서 게시한 데이터 세트를 선택합니다.

자세한 내용은 [Microsoft 블로그 게시물](https://powerbi.microsoft.com/ko-kr/blog/connecting-to-datasets-in-the-power-bi-service-from-desktop/)을 참조하십시오.
