---
description: 분류 데이터를 삭제하거나 제거하는 방법을 설명하는 단계입니다.
seo-description: 분류 데이터를 삭제하거나 제거하는 방법을 설명하는 단계입니다.
seo-title: 분류 데이터 삭제
solution: Analytics
subtopic: 분류
title: 분류 데이터 삭제
topic: 관리 도구
uuid: 5b1b0ac7-ee52-4fd8-b98e-25283595cf0c
translation-type: tm+mt
source-git-commit: 8c4c368a84ba5499d85f0b7512c99de47ddb14c2

---


# 분류 데이터 삭제

분류 데이터를 삭제하거나 제거하는 방법을 설명하는 단계입니다.

1. Click **[!UICONTROL Admin]** &gt; **[!UICONTROL Classification Importer]**.
1. Click **[!UICONTROL Browser Export]**.
1. 분류 데이터를 제거할 보고서 세트 및 데이터 세트를 선택합니다.
1. Adjust any optional settings to filter specific data you're looking for, then click **[!UICONTROL Export File]**.
1. Once the file has been downloaded, open the file and replace any classification values you wish to delete with [!DNL ~empty~].

   Alternatively, use [!DNL ~deletekey~]. 이 명령은 분류가 지정된 키에 대해 발생하지 않는 것처럼 분류를 취급합니다. 이렇게 하면 조회 테이블에서 키와 모든 열 데이터가 완벽하게 제거됩니다.

   **Caveat**:deletekey가 포함된 열은 하나만 [!DNL ~있으면 됩니다~]. The [!DNL ~empty~] command works at the cell level (key and column combination), so you need [!DNL ~empty~] in the classification column you want to remove. However, [!DNL ~deletekey~] works at the row level (the key and all associated metadata), so it only needs to appear in one of the columns in the row. 이 명령은 행에서 모든 메타데이터를 제거합니다. Adobe는 이것을 키가 절대로 분류되지 않은 것으로 해석하고 [없음](/help/components/c-classifications2/c-classifications-importer/nonclassified-keys.md#concept_233E51DDF3084FF7B7EA89381C73C5FF) 카테고리에 표시합니다.

1. 파일을 저장하고 [!UICONTROL 파일 가져오기] 탭을 사용하여 파일을 다시 업로드합니다.

   After you upload the file, the system recognizes [!DNL ~empty~] as a command to delete that classification value.

   **이 명령의 속성**

* [!DNL ~비어~] 있는 값은 공백 없이 소문자여야 합니다. 다음 항목은 잘못되었습니다.

   * [!DNL ~EMPTY~]
   * [!DNL ~ empty ~]
   * [!DNL ~Empty~]

* 키 열에서 값을 삭제할 수 없습니다. 이것은 보고 기능으로 바로 전달된 데이터이며 영구적입니다.
* 하위 분류가 있는 분류 값을 제거하는 경우 하위 분류도 함께 제거됩니다. 분류는 키 값 없이 존재할 수 없으며 하위 분류의 상위는 하위 분류의 키 값입니다.
* 상위 분류를 온전한 상태로 두고 하위 분류를 제거할 수 있습니다.

