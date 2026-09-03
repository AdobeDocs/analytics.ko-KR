---
description: (선택 사항) 분류를 마케팅 보고서로 가져오기 전에 분류 데이터 파일을 만드는 데 도움이 되는 템플릿을 다운로드할 수 있습니다. 데이터 파일은 원하는 분류를 열 머리글로 사용한 다음, 적합한 분류 머리글 아래에 보고 데이터 세트를 구성합니다.
title: 분류 템플릿
feature: Classifications
exl-id: e299509a-0c4f-4ba8-9e91-96356c386054
TQID: https://experienceleague.adobe.com/OR9THCLd93iUl58npPiinO4yAsK8KG3FU8qmBILHioY
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
subfeature_v2:
  - id: c80b99d6-98b9-4aeb-b5c4-933ef2ef705c
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 355
ht-degree: 66%

---

# 분류 템플릿(이전)

{{classification-importer-deprecation}}

(선택 사항) 분류를 보고서 및 프로젝트로 가져오기 전에, 분류 데이터 파일을 만드는 데 도움이 되는 템플릿을 다운로드할 수 있습니다. 데이터 파일은 원하는 분류를 열 머리글로 사용한 다음, 적합한 분류 머리글 아래에 보고 데이터 세트를 구성합니다.

## 분류 템플릿 {#concept_0F06847AD8D042F5BA818AE3C37E2417}

(선택 사항) 분류를 마케팅 보고서로 가져오기 전에 분류 데이터 파일을 만드는 데 도움이 되는 템플릿을 다운로드할 수 있습니다. 데이터 파일은 원하는 분류를 열 머리글로 사용한 다음, 적합한 분류 머리글 아래에 보고 데이터 세트를 구성합니다.

**[!UICONTROL 관리자]** > **[!UICONTROL 분류 가져오기]**.

| 요소 | 설명 |
| --- | ---|
| 보고서 세트 선택 | 템플릿에서 사용할 보고서 세트를 선택합니다. 보고서 세트와 데이터 세트가 일치해야 합니다. |
| 분류할 데이터 세트 | 데이터 파일에 맞는 데이터 유형을 선택합니다. 메뉴에는 분류용으로 구성된 보고서 세트의 모든 보고서가 포함됩니다. |
| Numeric 2 내보내기 | **중요**: 새 분류 아키텍처에 대해 활성화된 보고서 세트에는 이 옵션을 사용할 수 없습니다. |
| 인코딩 | 데이터 파일에 필요한 문자 인코딩을 선택합니다. 기본 인코딩 형식은 UTF-8입니다.<br>**중요**: 새 분류 아키텍처에 대해 활성화된 보고서 세트에는 이 옵션을 사용할 수 없습니다. |
| 다운로드 | 템플릿 파일을 다운로드합니다. |

템플릿에는 각 분류와 연관된 데이터를 포함하지 않고 특정 데이터 세트의 현재 정의된 분류 (열 머리글)가 포함됩니다.

>[!NOTE]
>
>템플릿 메서드는 분류 데이터 다운로드를 단일 보고서 세트로 제한합니다.

데이터 파일 구조에 대한 자세한 내용은 [분류 데이터 파일 정보](/help/components/classifications/importer/c-saint-data-files.md)를 참조하십시오.

## 분류 데이터 템플릿 다운로드(옵션) {#task_8DFCF309B6FD43ABB1D6FEE9AFAEC596}

이 템플릿은 분류에 대해 따라야 할 파일 형식을 제공합니다.

>[!NOTE]
>
>템플릿 메서드는 데이터 다운로드를 단일 보고서 세트로 제한합니다.

1. **[!UICONTROL 관리자]** > **[!UICONTROL 분류 가져오기]**&#x200B;를 클릭합니다.
1. **[!UICONTROL 템플릿 다운로드]** 탭에서 [데이터 템플릿 구성](/help/components/classifications/importer/c-download-saint-data.md)을 지정합니다.
1. **[!UICONTROL 다운로드]**&#x200B;를 클릭합니다.
1. 템플릿 파일을 로컬 시스템에 저장합니다.

   템플릿 파일은 탭으로 구분된 데이터 파일([!DNL .tab] 파일 확장명)이며 대부분의 스프레드시트 애플리케이션에서 지원합니다.
