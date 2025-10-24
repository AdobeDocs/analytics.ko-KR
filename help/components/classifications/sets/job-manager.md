---
title: 분류 작업 관리자
description: 분류 세트에서 생성된 현재 및 완료된 분류 작업을 보는 방법에 대해 알아봅니다.
exl-id: 0470e131-79c6-4906-85f0-530d360ac227
feature: Classifications
source-git-commit: 77599d015ba227be25b7ebff82ecd609fa45a756
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 2%

---

# 분류 작업 보기 및 조치

분류 작업 관리자에는 분류 세트에 대해 생성된 현재 및 완료된 분류 작업이 표시됩니다. 관리자를 사용하여 특정 작업에 대한 분류 데이터 또는 템플릿을 다운로드할 수도 있습니다.

분류 작업을 보고 작업하려면

1. 기본 인터페이스에서 **[!UICONTROL 구성 요소]**&#x200B;를 선택한 다음 **[!UICONTROL 분류 집합]**&#x200B;을 선택하십시오.
1. **[!UICONTROL 분류 세트]**&#x200B;에서 **[!UICONTROL 작업]** 탭을 선택합니다.

## 분류 작업 관리자

**[!UICONTROL 분류 집합 - 작업]** 관리자에 다음 인터페이스 요소가 있습니다.

![분류 세트 - 작업 관리자](manage/assets/classifications-sets-jobs.png)



### 분류 작업 목록

**[!UICONTROL 분류 작업]** 목록 ➊에 분류 작업이 표시됩니다. 목록은 다음과 같습니다.

| 열 | 설명 |
|---|---|
| **[!UICONTROL 작업 ID]** | 분류 작업의 식별자입니다. |
| **[!UICONTROL 분류 집합]** | 분류 작업과 연결된 분류 세트입니다. |
| **[!UICONTROL 크기]** | 분류 작업의 일부로 내보내거나 가져온 파일의 크기입니다. |
| **[!UICONTROL 상태]** | 분류 작업의 상태입니다. 가능한 값은 **[!UICONTROL 생성됨]**, **[!UICONTROL 큐에 있음]**, **[!UICONTROL 확인됨]**, **[!UICONTROL 유효성 검사 실패]**, **[!UICONTROL 처리]**, **[!UICONTROL 처리 완료]**, **[!UICONTROL 처리 실패]**, **[!UICONTROL 완료됨]** 또는 **[!UICONTROL 진행]**&#x200B;입니다. |
| **[!UICONTROL 파일 이름]** | 분류 작업의 일부로 파일을 가져오거나 내보내는 데 사용되는 이름 또는 기능을 식별합니다. 가능한 값은 다음과 같습니다. <ul><li>*값 없음*</li><li>분류 작업의 일부로 처리되는 파일의 이름입니다.</li><li>**[!UICONTROL SAINT 내보내기]**: 작업은 [레거시 분류 인터페이스](/help/components/classifications/importer/c-working-with-saint.md)에서 내보내는 작업입니다.</li><li>**[!UICONTROL timestamp _에_분류 집합&#x200B;_에 대한_]**&#x200B;내보내기: 작업은 [스키마](manage/schema.md#download) 인터페이스에서 다운로드한 작업입니다.</li></ul> |
| **[!UICONTROL 작업 유형]** | 분류 작업 유형. 가능한 값은 **[!UICONTROL 가져오기]** 또는 **[!UICONTROL 내보내기]**&#x200B;입니다. |
| **[!UICONTROL 소스]** | 분류 작업의 소스. 가능한 값은 **[!UICONTROL 웹 API]**, **[!UICONTROL 직접 API 업로드]**, **[!UICONTROL Adobe]**, **[!UICONTROL SAINT]** 또는 **[!UICONTROL 알 수 없음]**&#x200B;입니다. |
| **[!UICONTROL 수정된 줄]** | 분류 작업이 수정한 수정된 라인 수. |
| **[!UICONTROL 총 줄 수]** | 분류 작업이 처리한 총 라인 수입니다. |
| **[!UICONTROL 완료 시간]** | 분류 작업의 완료 시간입니다. |
| **[!UICONTROL 파일 다운로드]** | ![다운로드](/help/assets/icons/Download.svg)를 사용하여 분류 작업과 연결된 파일(템플릿 또는 데이터)을 다운로드합니다. |

분류 작업 목록에서 열의 크기를 조정하려면 다음을 수행할 수 있습니다.

* 열 구분자 위로 마우스를 가져간 후 열 구분자를 원하는 열 너비로 드래그합니다.
* ![V자형 화살표](/help/assets/icons/ChevronDown.svg)를 선택하고 **[!UICONTROL 열 크기 조정]**&#x200B;을 선택합니다. [크기 조정] 단추가 있는 세로줄을 사용하면 원하는 로 열 크기를 조정할 수 있습니다.

분류 작업 목록에서 열을 정렬하려면

* ![V자형 화살표](/help/assets/icons/ChevronDown.svg)를 선택하고 **[!UICONTROL 오름차순 정렬]** 또는 **[!UICONTROL 내림차순 정렬]**&#x200B;을 선택합니다. 화살표(↑↓)는 열과 열이 정렬되는 방식을 나타냅니다.


### 검색 및 단추

분류 작업 목록의 맨 위에 있는 ➋ 영역에서 다음을 수행할 수 있습니다.

* 분류 작업을 ![검색](/help/assets/icons/Search.svg)합니다. 결과는 분류 작업 목록에 표시됩니다. 검색을 지우려면 ![CrossSize200](/help/assets/icons/CrossSize200.svg)을(를) 선택하십시오.
* 분류 작업 목록에 적용된 필터를 제거합니다. 필터를 제거하려면 ![CrossSize100](/help/assets/icons/CrossSize100.svg)을(를) 선택하십시오.
* 1000개의 분류 작업을 추가로 로드하려면 ![MoreCircle](/help/assets/icons/MoreCircle.svg)을(를) 선택하십시오. 처음에는 분류 세트 목록에 최대 1000개의 분류 작업이 표시됩니다.
* 분류 세트 작업 목록의 열을 정의합니다. ![ColumnSetting](/help/assets/icons/ColumnSetting.svg)을(를) 선택하고 **[!UICONTROL 테이블 사용자 지정]** 대화 상자에서 **[!UICONTROL 표시할 열 선택]** 아래에 표시할 열을 선택합니다. 열 설정을 적용하려면 **[!UICONTROL 적용]**&#x200B;을 선택하세요.



### 필터 패널

분류 작업 목록을 필터링할 수 있는 필터 패널 ![을(를) 표시하려면 &#x200B;](/help/assets/icons/Filter.svg)필터➌을(를) 선택하십시오. 다음을 필터링할 수 있습니다.

* **[!UICONTROL 분류 집합]**. 하나 이상의 분류 세트를 선택하여 분류 작업 목록을 필터링합니다.
* **[!UICONTROL 완료 시간]**. 가능한 값 중 하나를 선택하여 완료 시간에 분류 작업 목록을 필터링합니다.
* **[!UICONTROL 상태]**. 가능한 값 중 하나를 선택하여 상태의 분류 작업 목록을 필터링합니다.
* **[!UICONTROL 작업 유형]**. 가능한 값 중 하나를 선택하여 작업 유형에 대한 분류 작업 목록을 필터링합니다.
* **[!UICONTROL Source]**. 가능한 값 중 하나를 선택하여 소스의 분류 작업 목록을 필터링합니다.


필터 패널을 숨기려면 ![필터](/help/assets/icons/Filter.svg) **[!UICONTROL 필터 숨기기]**&#x200B;를 선택하십시오.

필터 패널에 표시된 필터는 미리 로드된 분류 작업에 대한 옵션을 반영합니다.


<!--

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Jobs]**

You cannot create jobs from this interface. Create jobs by uploading data to a classification set (either manually or through a configured external location), requesting a download file, or requesting a template file.

## Filter classification sets

The left side of the Classification set job manager provides filter settings to locate the desired job. Clicking the filter icon toggles the filter settings visibility. You can filter Classification sets by **[!UICONTROL Classification set]**, **[!UICONTROL Completion time]**, **[!UICONTROL Status]**, **[!UICONTROL Job Type]**, or **[!UICONTROL Source]**.

![Classification set job filters](../assets/classification-set-job-filters.png)

Additional filter options are available above the Classification set job manager columns:

* **[!UICONTROL Search by title]**: Search for jobs by filename.
* **[!UICONTROL Load more]**: The Classification set job manager initially displays up to 1000 jobs. If more jobs exist, click this button to load 1000 more jobs.
* **Show/Hide columns**: Toggle visibility for any column besides [!UICONTROL Filename] and [!UICONTROL Completion time].

## Classification set job manager columns

The following columns are available in the Classification set job manager:

* **[!UICONTROL Filename]**: The name of the upload or download file.
* **[!UICONTROL Classification set]**: The name of the Classification set that the file applies to. You can click the Classification set name to reach the Classification set's [Settings](manage/settings.md).
* **[!UICONTROL Size]**: The size of the file.
* **[!UICONTROL Status]**: The status of the job processing the file.
  * **[!UICONTROL Created]**: The job was submitted.
  * **[!UICONTROL Queued]**: The file is ready to be processed, and is waiting for a classification server to process the file.
  * **[!UICONTROL Validated]**: The file is valid and is waiting to be processed.
  * **[!UICONTROL Failed validation]**: The file is formatted incorrectly or otherwise invalid. The file does not go through processing.
  * **[!UICONTROL Processing]**: The file is actively being processed by Adobe.
  * **[!UICONTROL Failed processing]**: The file failed processing.
  * **[!UICONTROL Complete]**: Processing is complete. Classification data is visible in reporting.
  * **[!UICONTROL Failed]**: Generic failure not related to validation or processing.
* **[!UICONTROL Job type]**: The type of job.
* **[!UICONTROL Source]**: The job source.
* **[!UICONTROL File download]**: Only applies to download jobs, such as downloading classification data or downloading templates. When a download is ready, this column provides a download link.
* **[!UICONTROL Modified lines]**: The number of modified lines.
* **[!UICONTROL Completed lines]**: The number of completed lines.
* **[!UICONTROL Completion time]**: The date and time that the job completed (or failed).
-->