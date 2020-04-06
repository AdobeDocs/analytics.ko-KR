---
description: (선택 사항) 분류를 마케팅 보고서로 가져오기 전에 분류 데이터 파일을 만드는 데 도움이 되는 템플릿을 다운로드할 수 있습니다. 데이터 파일은 원하는 분류를 열 머리글로 사용한 다음 해당 분류 머리글 아래에 보고 데이터 세트를 구성합니다.
subtopic: Classifications
title: 분류 템플릿
topic: Admin tools
uuid: 4edd411b-164c-4b4d-a872-b57a3163ca72
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 분류 템플릿

(선택 사항) 분류를 마케팅 보고서로 가져오기 전에 분류 데이터 파일을 만드는 데 도움이 되는 템플릿을 다운로드할 수 있습니다. 데이터 파일은 원하는 분류를 열 머리글로 사용한 다음 해당 분류 머리글 아래에 보고 데이터 세트를 구성합니다.

## 분류 템플릿 {#concept_0F06847AD8D042F5BA818AE3C37E2417}

(선택 사항) 분류를 마케팅 보고서로 가져오기 전에 분류 데이터 파일을 만드는 데 도움이 되는 템플릿을 다운로드할 수 있습니다. 데이터 파일은 원하는 분류를 열 머리글로 사용한 다음 해당 분류 머리글 아래에 보고 데이터 세트를 구성합니다.

**[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.

| 요소 | 설명 |
|---|---|
| 보고서 세트 선택 | 템플릿에서 사용할 보고서 세트를 선택합니다. 보고서 세트와 데이터 세트가 일치해야 합니다. |
| 분류할 데이터 세트 | 데이터 파일의 데이터 유형을 선택합니다. 메뉴에는 분류에 대해 구성된 보고서 세트의 모든 보고서가 포함됩니다. |
| Numeric 2 내보내기 | 가져오기를 통해 Numeric 2 분류를 시스템으로 가져올 수 있습니다. 숫자 2 분류는 [!UICONTROL Marketing Channel] 보고서의 비용 및 예산 값과 같이 시간에 따라 다른 항목에 대해 변경되는 변수에 유용합니다. Numeric 2 분류를 사용한 데이터 업로드에 대한 내용은 [Numeric 2 분류](/help/components/c-classifications2/c-numeric-2/c-numeric-2-classifications.md)를 참조하십시오. |
| 인코딩 | 데이터 파일의 문자 인코딩을 선택합니다. 기본 인코딩 형식은 UTF-8입니다. |
| 다운로드 | 템플릿 파일을 다운로드합니다. |

템플릿에는 각 분류와 연관된 데이터를 포함하지 않고 특정 데이터 세트의 현재 정의된 분류(열 머리글)가 포함되어 있습니다.

>[!NOTE] 템플릿 메서드는 분류 데이터 다운로드를 단일 보고서 세트로 제한합니다.

데이터 파일 구조에 대한 자세한 내용은 [분류 데이터 파일 정보](/help/components/c-classifications2/c-classifications-importer/c-saint-data-files.md)를 참조하십시오.

## 분류 데이터 템플릿 다운로드(옵션) {#task_8DFCF309B6FD43ABB1D6FEE9AFAEC596}

이 템플릿은 분류에 대해 따라야 할 파일 형식을 제공합니다.

>[!NOTE] 템플릿 메서드는 데이터 다운로드를 단일 보고서 세트로 제한합니다.

1. 클릭 **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. On the **[!UICONTROL Download Template]** tab, specify the [data template configuration](/help/components/c-classifications2/c-classifications-importer/c-download-saint-data.md).
1. 클릭 **[!UICONTROL Download]**.
1.  템플릿 파일을 로컬 시스템에 저장합니다. 

   템플릿 파일은 탭으로 구분된 데이터 파일([!DNL .tab] 파일 확장명)이며 대부분의 스프레드시트 애플리케이션에서 지원합니다.

