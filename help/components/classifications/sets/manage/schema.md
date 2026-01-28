---
title: 분류 세트 스키마
description: 개별 분류 세트에 대한 스키마를 보고 편집하는 방법을 알아봅니다.
exl-id: 4a7c5bfe-ff2b-4380-af46-435801d73c1e
feature: Classifications
source-git-commit: cfa8335008548254786e46dfe634229edad5bd54
workflow-type: tm+mt
source-wordcount: '1494'
ht-degree: 4%

---

# 분류 세트 스키마

스키마는 분류 세트에 대해 정의한 주요 차원에 적용할 분류 목록입니다. 예를 들어, 제품을 키 차원으로 정의했으며 이 필드에 제품 SKU가 포함되어 있는 경우 스키마를 사용하여 제품 이름, 제품 색상, 제품 크기 등과 같은 분류를 추가합니다.

분류 세트에 대한 스키마를 편집하려면 다음을 수행하십시오.


1. Adobe Analytics 상단 메뉴 모음에서 **[!UICONTROL 구성 요소]**&#x200B;를 선택한 다음 **[!UICONTROL 분류 세트]**&#x200B;를 선택합니다.
1. **[!UICONTROL 분류 세트]**&#x200B;에서 **[!UICONTROL 분류 세트]** 탭을 선택합니다.
1. **[!UICONTROL 분류 세트]** 관리자에서 스키마를 편집할 분류 세트를 선택합니다.
1. **[!UICONTROL 분류 집합: _분류 집합 이름_]**&#x200B;대화 상자에서&#x200B;**[!UICONTROL 스키마]**&#x200B;탭을 선택합니다. 해당 탭은 다음 인터페이스 요소로 구성됩니다.

   ![분류 집합 - 스키마](assets/classification-sets-schema.png)

   * [분류 목록](#classification-list)
   * [검색](#search)
   * [액션](#actions)
   * [작업 표시줄](#action-bar)

## 분류 목록

분류 목록에는 다음 열이 있습니다.

| 열 | 설명 |
|---|---|
| **[!UICONTROL 분류 이름]** | 분류에 제공한 이름입니다. |
| **[!UICONTROL ID 이름]** | 시스템에서 분류에 대해 파생된 이름입니다. 이 이름은 읽기 전용 값이며 ID 이름을 사용할 수 있습니다 |
| **[!UICONTROL 분류자]** | 사용하는 경우 이 분류를 분류하는 데 사용되는 조회 분류 세트에 대한 링크입니다. |


## 검색

![검색](/help/assets/icons/Search.svg)에서 하나 이상의 분류를 빠르게 검색할 수 있습니다. ![CrossSize100](/help/assets/icons/CrossSize100.svg)을(를) 사용하여 검색을 지웁니다.

## 액션

다음 작업은 분류 목록 맨 위에 있는 버튼으로 사용할 수 있습니다.

| 아이콘 | 액션 | 설명 |
|---|---|---|
| ![추가](/help/assets/icons/Add.svg) | **[!UICONTROL 추가]** | 목록에 [분류를 추가](#add)합니다. |
| ![UploadToCloud](/help/assets/icons/UploadToCloud.svg) | **[!UICONTROL 업로드]** | [JSON, CSV, TSV 또는 TAB 파일 업로드](#upload). |
| ![다운로드](/help/assets/icons/Download.svg) | **[!UICONTROL 다운로드]** | [분류 데이터를 다운로드합니다](#download). |
| ![문서 단편](/help/assets/icons/DocumentFragment.svg) | **[!UICONTROL 템플릿]** | 분류 데이터에 대해 [템플릿을 다운로드합니다](#template). |
| ![기록](/help/assets/icons/History.svg) | **[!UICONTROL 작업 기록]** | 선택한 분류 세트에 대해 필터링된 [분류 세트 작업 관리자](/help/components/classifications/sets/job-manager.md)를 표시합니다. |
| ![톱니바퀴](/help/assets/icons/Gear.svg) | **[!UICONTROL 자동화]** | 클라우드 위치를 사용하여 [분류 데이터 수집 자동화](#automate). |


### 추가

새 분류를 추가하려면 ![추가](/help/assets/icons/Add.svg) **[!UICONTROL 추가]**&#x200B;를 선택하십시오.

![분류 세트 - 스키마에 분류 추가](assets/classification-sets-schema-add-classification.png)

**[!UICONTROL _분류 집합 이름_]**&#x200B;에 대한 새 분류 추가 대화 상자에서&#x200B;**[!UICONTROL 분류 이름]**&#x200B;을 입력하고&#x200B;**[!UICONTROL 추가]**&#x200B;를 선택합니다. 분류가 목록에 추가됩니다.



### 업로드

분류를 위해 스키마로 분류 데이터를 가져오려면 ![UploadToCloud](/help/assets/icons/UploadToCloud.svg) **[!UICONTROL Upload]**&#x200B;을(를) 선택하십시오.


![분류 세트 - 스키마 파일 업로드](assets/classification-sets-schema-upload-file.png)

1. **[!UICONTROL 새 분류 추가]** 대화 상자에서:

   * 분류 데이터가 포함된 파일을 **[!UICONTROL 여기에 끌어다 놓기]**(으)로 끌어다 놓습니다.
   * **[!UICONTROL 찾아보기]**&#x200B;를 선택하고 컴퓨터 또는 네트워크에서 파일을 선택하십시오.

   파일 내용 중 **[!UICONTROL 스키마 미리 보기]**&#x200B;가 표시됩니다. 미리 보기에는 파일의 데이터 열이 표시됩니다. 열 크기를 조정하려면 ![V자 크기 조정](/help/assets/icons2/ChevronDownSize300.svg)을 선택하고 **[!UICONTROL 열 크기 조정]**&#x200B;을 선택합니다. 열 크기를 조정할 수 있는 핸들이 나타납니다.

   열에 대한 분류 집합에 분류가 정의되지 않은 경우 경고 ![Alert](/help/assets/icons/Alert.svg)이(가) 표시됩니다. 기존 분류 스키마 세트에 분류가 없고 가져올 때 생성된다는 경고가 표시됩니다.

1. **[!UICONTROL 충돌 시 데이터 덮어쓰기를 선택하시겠습니까?현재 분류 데이터를 가져온 새 데이터로 덮어쓰려는 경우]**. 예:

   | | 키 | 현재 제품 색상 | 파일 가져오기 | 새 제품 색상 |
   |---|---|---|---|---|
   | ![SelectBox](/help/assets/icons/SelectBox.svg) **[!UICONTROL 충돌 시 데이터를 덮어쓰시겠습니까?]** | 1234 | 녹색 | 파랑 | 파랑 |
   | ![정사각형](/help/assets/icons2/Square.svg) **[!UICONTROL 충돌 시 데이터를 덮어쓰시겠습니까?]** | 1234 | 녹색 | 파랑 | 녹색 |

1. **[!UICONTROL 적용]**&#x200B;을 선택합니다. 열이 기존 스키마 세트에 분류로 존재하지 않으면 경고가 표시됩니다. 이러한 열은 업로드를 확인할 때 새 분류로 추가됩니다.

   ![분류 집합 - 분류 경고 업로드](assets/classification-sets-schema-upload-file-preview-alert.png)

   업로드를 확인하려면 **[!UICONTROL 업로드 확인]**&#x200B;을 선택하십시오. 업로드를 취소하려면 **[!UICONTROL 업로드 취소]**&#x200B;를 선택하십시오.


### 다운로드

분류 데이터를 다운로드하려면 ![다운로드](/help/assets/icons/Download.svg) **[!UICONTROL 다운로드]**&#x200B;를 선택하십시오.

![분류 세트 - 스키마 분류 데이터 다운로드](assets/classification-sets-schema-download-file.png)

**[!UICONTROL _분류 집합 이름_]**&#x200B;에 대한 데이터 다운로드 대화 상자에서:

1. 다운로드할 **[!UICONTROL 행]**&#x200B;의 수를 입력하십시오. 예: `10000`.
1. 분류 데이터 행을 다운로드할 기간을 선택하려면 **[!UICONTROL 다음 기간 사이에 받은 행 다운로드]**&#x200B;에 대한 시작 및 종료 데이터를 입력하십시오. 또는 ![달력](/help/assets/icons/Calendar.svg)을 사용하여 기간을 선택하는 달력 팝업을 사용합니다.
1. 반환할 데이터를 선택하려면 **[!UICONTROL 반환된 데이터]**&#x200B;에서 옵션을 선택하십시오.

   * **[!UICONTROL 모든 값]**&#x200B;은(는) 현재 분류 데이터에 대한 모든 값을 반환합니다.
   * **[!UICONTROL 비어 있는 모든 열]**&#x200B;은(는) 기존 분류 데이터에 대한 키 값이 있는 열을 반환합니다. 값이 없는 분류 데이터에 대해 값이 없는 열.
   * **[!UICONTROL 모든 열이 비어 있음]**&#x200B;은(는) 기존 분류 데이터에 대한 값이 있는 키 열을 반환합니다. 분류 데이터에 대한 값이 없는 열입니다.
1. 다운로드한 분류 데이터의 [파일 형식](/help/components/classifications/sets/data-files.md#general-file-requirements)을(를) 선택하려면 **[!UICONTROL 파일 형식]** 드롭다운 메뉴에서 옵션을 선택하십시오. 사용 가능한 옵션은 다음과 같습니다.

   * **[!UICONTROL JSON]**
   * **[!UICONTROL 쉼표로 구분된 값]**(CSV).
   * **[!UICONTROL Excel 탭으로 구분된 값]**(TSV 또는 TAB).

1. 파일을 다운로드할 때 [파일 인코딩](/help/components/classifications/sets/data-files.md#general-file-requirements)을 선택하려면 [파일 인코딩] 드롭다운 메뉴에서 옵션을 선택하십시오. 사용 가능한 옵션은 다음과 같습니다.

   * **[!UICONTROL UTF-8]**.
   * **[!UICONTROL Latin-1]**.


1. 분류 데이터를 다운로드하려면 **[!UICONTROL 다운로드]**&#x200B;를 선택하십시오. 다운로드한 파일은 브라우저의 기본 다운로드 디렉터리에 있으며 제목은 <code><i>분류 세트</i>입니다.<i>json</i>|<i>csv</i>|<i>tsv</i></code>. 파일이 이미 있는 경우 시퀀스 번호 <code>(<i>x</i>)</code> 가 파일 이름에 추가됩니다.<br/>데이터를 반환하지 않는 옵션을 지정한 경우 반환된 날짜 범위 및 데이터에 대한 옵션을 변경하도록 알리는 **[!UICONTROL 알림]** 대화 상자가 표시됩니다.


### 템플릿

분류 데이터용 템플릿을 다운로드하려면 ![문서 단편](/help/assets/icons/DocumentFragment.svg) **[!UICONTROL 템플릿]**&#x200B;을 선택하세요.

![분류 세트 스키마 - 템플릿 다운로드](assets/classification-sets-schema-download-template.png)

**[!UICONTROL 분류 세트 이름&#x200B;_에 대한_]**&#x200B;템플릿 다운로드 대화 상자에서:

1. 다운로드한 분류 데이터의 [파일 형식](/help/components/classifications/sets/data-files.md#general-file-requirements)을(를) 선택하려면 **[!UICONTROL 파일 형식]** 드롭다운 메뉴에서 옵션을 선택하십시오. 사용 가능한 옵션은 다음과 같습니다.

   * **[!UICONTROL 쉼표로 구분된 값]**&#x200B;입니다.
   * **[!UICONTROL Excel 탭으로 구분된 값]**.

1. 파일을 다운로드할 때 [파일 인코딩](/help/components/classifications/sets/data-files.md#general-file-requirements)을 선택하려면 [파일 인코딩] 드롭다운 메뉴에서 옵션을 선택하십시오. 사용 가능한 옵션은 다음과 같습니다.

   * **[!UICONTROL UTF-8]**.
   * **[!UICONTROL Latin-1]**.

1. 분류 데이터 템플릿을 다운로드하려면 **[!UICONTROL 다운로드]**&#x200B;를 선택하십시오. 다운로드한 파일은 브라우저의 기본 다운로드 디렉터리에 있으며 제목이 <code><i>분류 세트</i>입니다.<i>csv</i>|<i>tsv</i></code>. 파일이 이미 있는 경우 시퀀스 번호 <code>(<i>x</i>)</code> 가 파일 이름에 추가됩니다.


### 자동화 {#automate}


>[!CONTEXTUALHELP]
>id="classificationsets_schema_automate_locationaccount"
>title="위치 계정"
>abstract="분류 데이터 가져오기를 지원하는 계정 유형의 위치 계정 목록입니다. 새 위치 계정을 만들려면 **[!UICONTROL 새 계정]**&#x200B;을 선택하세요."
>additional-url="https://experienceleague.adobe.com/docs/analytics/components/locations/configure-import-accounts.html?lang=ko" text="클라우드 가져오기 및 내보내기 계정 구성"


>[!CONTEXTUALHELP]
>id="classificationsets_schema_automate_location"
>title="위치"
>abstract="분류 데이터 가져오기를 지원하는 선택한 위치 계정의 위치 목록입니다. 새 위치를 만들려면 **[!UICONTROL 새 위치]**&#x200B;를 선택하십시오."
>additional-url="https://experienceleague.adobe.com/docs/analytics/components/locations/configure-import-locations.html?lang=ko" text="클라우드 가져오기 및 내보내기 위치 구성"


분류 수집을 자동화하려면 ![톱니바퀴](/help/assets/icons/Gear.svg) **[!UICONTROL 자동화]**&#x200B;를 선택하십시오.

![분류 세트 스키마 - 자동화](assets/classification-sets-schema-automate.png)

**[!UICONTROL _분류 집합 이름_]**&#x200B;에 대한 수집 위치 연결/업데이트 대화 상자에서:

1. 클라우드 위치를 선택하려면 **[!UICONTROL 위치 계정]**&#x200B;에서 옵션을 선택하십시오. 분류 데이터를 가져올 수 있는 [지원되는 계정 유형의 위치 계정](https://experienceleague.adobe.com/ko/docs/analytics/components/locations/configure-import-accounts)만 표시됩니다. 새 계정을 만들려면 **[!UICONTROL 새 계정]**&#x200B;을 선택하세요.
1. 위치를 선택하려면 **[!UICONTROL 위치]**&#x200B;에서 옵션을 선택하십시오. 분류 데이터를 가져오기 위해 선택한 계정 유형의 위치만 표시됩니다. 새 위치를 만들려면 **[!UICONTROL 새 위치]**&#x200B;를 선택하세요.

   >[!IMPORTANT]
   >
   >만들거나 선택한 위치에 분류 데이터 파일을 호스팅하려면 **[!UICONTROL 버킷]** 내에 **[!UICONTROL 접두사]**(폴더)가 있어야 합니다. 예를 들어 폴더 이름이 `files`입니다. 버킷 루트의 호스팅 파일은 대부분의 클라우드 위치에서 작동하지 않습니다.
   >

1. 구분 기호를 선택하려면 **[!UICONTROL 목록 구분 기호]** 드롭다운 메뉴에서 옵션을 선택하십시오. 옵션은 다음과 같습니다.
   * **[!UICONTROL 쉼표 ,]**
   * **[!UICONTROL 세미콜론 ;]**
   * **[!UICONTROL 콜론:]**
   * **[!UICONTROL 세로 막대 |]**
   * **[!UICONTROL 스페이스]**
   * **[!UICONTROL 탭]**
1. 파일을 다운로드할 때 [파일 인코딩](/help/components/classifications/sets/data-files.md#general-file-requirements)을 선택하려면 **[!UICONTROL 파일 인코딩]** 드롭다운 메뉴에서 옵션을 선택하십시오. 사용 가능한 옵션은 다음과 같습니다.

   * **[!UICONTROL UTF-8]**.
   * **[!UICONTROL Latin-1]**.

1. 수집 작업이 완료되었음을 사용자에게 알리려면 **[!UICONTROL 수집 작업이 완료되었을 때 알릴 전자 메일(쉼표로 구분)]**&#x200B;에 대한 전자 메일 주소를 쉼표로 구분하여 입력하십시오.
1. **[!UICONTROL 유효성 검사]**&#x200B;를 선택합니다. 클라우드 위치에 대한 연결이 확인되었습니다.
1. 유효성 검사가 성공하면 ![CheckmarkCircle](/help/assets/icons/CheckmarkCircle.svg) **[!UICONTROL 위치 유효성 검사가 성공했음을 보여 주는 toast 메시지가 표시됩니다. 클라우드 스토리지에 대한 연결이 확인되었습니다.클라우드 연결에 대한 연결을 만든 경우 &#x200B;]**<br/>**[!UICONTROL &#x200B;저장&#x200B;]**&#x200B;을 선택합니다. 그렇지 않으면&#x200B;**[!UICONTROL &#x200B;업데이트&#x200B;]**&#x200B;를 선택하십시오. 또는&#x200B;**[!UICONTROL &#x200B;취소&#x200B;]**&#x200B;를 선택하여 클라우드 위치 구성을 취소하세요.

파일을 클라우드 위치에 업로드할 때 15분 이내에 파일이 검색되어 가져오기 작업으로 제출됩니다. 가져오기 작업의 결과는 [분류 작업 관리자](/help/components/classifications/sets/job-manager.md)에 보고됩니다. 수집 작업 완료를 알릴 사용자 목록에 추가되면 이메일 메시지도 수신하게 됩니다.

예:

![분류 세트 - 작업 확인 전자 메일](assets/job-failed-validation.png){width="400"}


## 작업 표시줄

작업 표시줄에는 선택한 분류에 사용할 수 있는 작업이 표시됩니다. 사용 가능한 옵션은 다음과 같습니다.

| 아이콘 | 액션 | 설명 |
|---|---|---|
| ![찾아보기](/help/assets/icons/Browse.svg) | **[!UICONTROL 조회 추가]** | 분류 세트를 조회(하위 분류)로 추가합니다.<br/>조회 첨부&#x200B;**[!UICONTROL 테이블의]**: <ol><li>**[!UICONTROL 분류 이름]** 드롭다운 메뉴에서 조회 분류를 선택합니다.</li><li>**[!UICONTROL 추가]**&#x200B;를 선택합니다.</li></ol>조회 분류가 분류에 추가되고 내부 ID를 사용하여 **[!UICONTROL 분류자]** 열에 나열됩니다. |
| ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) | **[!UICONTROL 조회 제거]** | 조회로 분류 세트를 제거합니다. 분류에서 조회를 영구적으로 삭제하려면 **[!UICONTROL 분류&#x200B;_확인 대화 상자에서__분류 세트 제거_]**&#x200B;에서&#x200B;**[!UICONTROL 삭제]**&#x200B;를 선택합니다. |
| ![이름 바꾸기](/help/assets/icons/Rename.svg) | **[!UICONTROL 이름 바꾸기]** | 분류의 **[!UICONTROL 분류 이름]** 이름을 바꾸십시오. **[!UICONTROL 이름 바꾸기: _분류 이름_]**&#x200B;대화 상자에서 새 이름을 입력하고&#x200B;**[!UICONTROL 이름 바꾸기]**&#x200B;를 선택합니다. |
| ![삭제](/help/assets/icons/Delete.svg) | **[!UICONTROL 삭제]** | 분류를 삭제합니다. **[!UICONTROL _분류 이름 삭제_]**&#x200B;대화 상자가 나타납니다. 분류를 삭제하려면&#x200B;**[!UICONTROL 삭제]**&#x200B;를 선택하십시오. |
