---
description: Adobe Analytics에서 Document Cloud 데이터를 볼 수 있습니다.
title: Document Cloud 보고 구성
feature: Admin Tools
exl-id: eb58d011-c4b0-4c0c-9241-83b2bccc2c77
TQID: 'https://experienceleague.adobe.com/2X5YQxmTsMYdnwSWVL4EMr1K1aV9UM6FRMHa2P--Xuc'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
subfeature_v2:
  - id: fab61dd8-112a-4e5e-ad5f-fb0240b7a60b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 140
ht-degree: 100%

---

# Document Cloud 보고 구성

Adobe Analytics에서 사용할 수 있도록 PDF 관련 차원 및 지표를 구성할 수 있습니다.

## PDF 보고 활성화 시 추가되는 구성 요소

PDF 보고를 올바르게 구성한 경우 Adobe Analytics에서 다음과 같은 차원 및 지표를 사용할 수 있습니다.

**차원:**

* PDF 검색어

* PDF 확대/축소 레벨

* PDF 작업

* PDF 페이지 번호

* PDF 파일 이름

**지표:**

* PDF 조회수

* PDF 페이지 조회수

* PDF 다운로드

* PDF 검색

* 사용된 PDF 책갈피

* PDF 텍스트 복사

* PDF 인쇄

## Adobe Analytics에서 PDF 보고 활성화

1. **[!UICONTROL Analytics]** > **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]** > **`<select report suite>`** > **[!UICONTROL 설정 편집]** > **[!UICONTROL Document Cloud 관리]** > [!UICONTROL **Document Cloud 보고**]&#x200B;로 이동합니다.

1. Adobe Document Cloud 관리 페이지에서 [!UICONTROL **PDF 보고서 활성화**]&#x200B;를 선택합니다.

1. Adobe Analytics로 데이터를 전송하도록 Adobe Document Cloud를 구성하려면 [Adobe Document Cloud Javascript SDK](https://www.adobe.io/apis/documentcloud/dcsdk.html)를 사용하십시오.
