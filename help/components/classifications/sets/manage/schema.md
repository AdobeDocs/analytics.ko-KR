---
title: 분류 세트 스키마
description: 개별 분류 세트에 대한 스키마를 보고 편집합니다.
exl-id: 0fc12a0c-c1cf-4159-9d8b-492ebcaa8ea1
feature: Classifications
source-git-commit: 6cc7f491340ec7c36252f7ae53de07b0ab8f3b6f
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 42%

---

# 스키마

이 분류 세트에 대해 현재 구성된 분류 차원을 봅니다.

**[!UICONTROL 구성 요소]** > **[!UICONTROL 분류 세트]** > **[!UICONTROL 세트]** > 원하는 분류 세트 이름을 클릭합니다. > **[!UICONTROL 스키마]**

다음 버튼을 사용할 수 있습니다.

<!--* **[!UICONTROL Add]**: Adds an empty row so that you can add a classification dimension to the schema.-->
* **[!UICONTROL 업로드]**: 하나 이상의 분류 차원에 대한 분류 데이터를 수동으로 업로드합니다. `JSON`, `CSV`, `TSV`, 및 `TAB` 파일이 지원됩니다. 유효한 파일을 업로드하면 분류할 데이터의 테이블 미리보기가 표시됩니다.
   * **[!UICONTROL 파일 인코딩]**: 이 드롭다운을 사용하여 올바른 파일 인코딩을 선택합니다. 유효한 옵션에는 [!UICONTROL UTF-8] 및 [!UICONTROL Latin1]이 포함됩니다.
   * **[!UICONTROL 목록 구분 기호]**: 올바른 목록 구분 기호를 선택합니다. 다운로드한 파일 또는 템플릿 파일을 사용하는 경우, [!UICONTROL 목록 구분 기호]가 파일을 다운로드할 때의 [!UICONTROL 목록 구분 기호]와 일치하는지 확인하십시오.
   * **[!UICONTROL 적용]**: 업로드한 분류 데이터를 분류 세트에 저장합니다.

  ![분류 세트 업로드](../../assets/classification-set-upload.png)

* **[!UICONTROL 다운로드]**: 키 값과 해당 분류 열을 다운로드합니다.
   * **[!UICONTROL 행]**: 다운로드 파일에 포함할 최대 행 수입니다.
   * **[!UICONTROL 다음 기간 동안 받은 행 다운로드]**: 보고에 나타나는 시점을 기준으로 키 값을 필터링할 수 있는 캘린더 날짜 선택기입니다. 이 날짜 범위에서 키 값이 수집되지 않은 경우 다운로드한 파일에 키 값이 나타나지 않습니다.
   * **[!UICONTROL 데이터 반환됨]**: 연결된 분류 데이터를 기반으로 다운로드한 파일에 포함된 키 값을 필터링할 수 있는 드롭다운 목록입니다.
      * **[!UICONTROL 모든 분류된 값]**: 하나 이상의 열에 분류 데이터가 포함된 행을 포함합니다.
      * **[!UICONTROL 모든 분류되지 않은 값]**: 하나 이상의 열에 분류 데이터가 누락된 행을 포함합니다.
   * **[!UICONTROL 파일 형식]**: 다운로드 파일이 있는 파일 형식을 결정하는 드롭다운 목록입니다. 옵션에는 [!UICONTROL JSON], [!UICONTROL 쉼표로 구분된 값] 및 [!UICONTROL Excel 탭으로 구분된 값]이 포함됩니다.
   * **[!UICONTROL 파일 인코딩]**: 파일 인코딩을 결정하는 드롭다운 목록입니다. 옵션에는 [!UICONTROL UTF-8] 및 [!UICONTROL Latin1]이 포함됩니다. UTF-8이 권장됩니다.

  ![분류 세트 다운로드](../../assets/classification-set-download.png)

* **[!UICONTROL 템플릿]**: 템플릿 파일을 다운로드합니다. 이 파일은 분류 데이터나 키 값을 포함하지 않는다는 점을 제외하면 [!UICONTROL 다운로드] 버튼과 유사합니다.
   * **[!UICONTROL 파일 형식]**: 템플릿 파일이 있는 파일 형식을 결정하는 드롭다운 목록입니다. 옵션에는 [!UICONTROL 쉼표로 구분된 값] 및 [!UICONTROL Excel 탭으로 구분된 값]이 포함됩니다.
   * **[!UICONTROL 파일 인코딩]**: 파일 인코딩을 결정하는 드롭다운 목록입니다. 옵션에는 [!UICONTROL UTF-8] 및 [!UICONTROL Latin1]이 포함됩니다. UTF-8이 권장됩니다.
   * **[!UICONTROL 목록 구분 기호]**: 각 행에서 분류 열을 구분하는 목록 구분 기호를 결정하는 드롭다운 목록입니다.

  ![분류 세트 템플릿](../../assets/classification-set-template.png)

* **[!UICONTROL 작업 내역]**: 로 이동하는 바로 가기 링크 [작업 관리자](../job-manager.md), 이 분류 세트에 대한 작업만 표시합니다.
* **[!UICONTROL 자동화]**: 외부 스토리지 위치에서 데이터를 자동으로 수집합니다.
   * **[!UICONTROL 위치 계정]**: 조직에서 구성한 기존 위치 계정을 표시하는 드롭다운 목록입니다. 조직에서 아직 위치 계정을 구성하지 않은 경우 다음을 선택하여 구성할 수 있습니다. [!UICONTROL **새 계정 만들기**].

     위치 계정 구성에 대한 자세한 내용은 [클라우드 가져오기 위치 구성](/help/components/classifications/importer/configure-import-accounts.md).

   * **[!UICONTROL 위치]**: 조직에서 구성한 기존 위치를 보여 주는 드롭다운 목록입니다. 조직에서 위치를 아직 구성하지 않은 경우 다음을 선택하여 위치를 구성할 수 있습니다. [!UICONTROL **새 위치 만들기**].

     위치 구성에 대한 자세한 내용은 [클라우드 가져오기 위치 구성](/help/components/classifications/importer/configure-import-accounts.md).

   * **[!UICONTROL 구분 기호]**: 업로드된 파일의 열 구분 기호입니다. 옵션은 다음과 같습니다 [!UICONTROL 쉼표], [!UICONTROL 세미콜론], [!UICONTROL 콜론], [!UICONTROL 세로 막대], [!UICONTROL 공간], [!UICONTROL 슬래시], [!UICONTROL 백슬래시], [!UICONTROL 대시], 또는 [!UICONTROL 밑줄].

   * **[!UICONTROL 인코딩]**: 파일 인코딩을 결정하는 드롭다운 목록입니다. 옵션에는 [!UICONTROL UTF-8] 및 [!UICONTROL Latin1]이 포함됩니다. UTF-8이 권장됩니다.
