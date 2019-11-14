---
description: PDF 및 CSV 형식으로 저장된 프로젝트와 저장되지 않은 프로젝트를 다운로드할 수 있습니다.
title: PDF 또는 CSV 파일 다운로드
uuid: 8af5f3d7-5870-4ed6-8a9f-ef290a48ef5f
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# PDF 또는 CSV 파일 다운로드

PDF 및 CSV 형식으로 저장된 프로젝트와 저장되지 않은 프로젝트를 다운로드할 수 있습니다.

PDF 또는 CSV 파일 이름이 프로젝트의 현재 이름과 일치합니다. 저장되지 않은 프로젝트인 경우 프로젝트에 저장되지 않은 변경 사항이 다운로드한 파일에 포함됩니다. PDF 또는 CSV로 저장되지 않은 프로젝트를 예약할 수 없습니다.

> [!NOTE] 또한 CSV 형식으로 폴아웃 시각화도 지원합니다.

> [!NOTE] 프로젝트를 PDF 파섹 프로젝트에 사용자 지정 크기의 시각화 및 패널이 있는 경우, 잘린 컨텐츠가 생기지 않게 시각화 및 패널의 크기가 자동으로 지정(오른쪽 상단 모서리의 단추)되도록 변경해야 합니다.

1. 프로젝트를 만들거나 엽니다.
1. Click **[!UICONTROL Project]** &gt; **[!UICONTROL Download CSV (or Download PDF).]**

On April 11, 2019, several changes were made to **[!CSV downloads]** (and **[!Copy to Clipboard]**) from Analysis Workspace to remove formatting from exported data.
* 천 단위 구분 기호가 더 이상 포함되지 않습니다. (The decimal separator will continue to be included, and will adhere to the format defined under **[!UICONTROL Components &gt; Report Settings &gt; Thousands Separator]**).
* 통화 기호는 표시되지 않습니다.
* 퍼센트 기호가 표시되지 않습니다.
* 백분율은 십진수 형식입니다.예를 들어, 75%는 0.75로 표시됩니다.
* 시간은 초 단위로 표시됩니다.
* 집단 테이블은 원시 값만 표시합니다.백분율이 제거됩니다.
* 숫자가 잘못된 경우 빈 셀이 표시됩니다.

>[!N참고:]
>
> 쉼표를 소수 구분 문자로 사용하는 숫자 값은 내보낸 CSV에서 계속 인용 부호가 됩니다.
