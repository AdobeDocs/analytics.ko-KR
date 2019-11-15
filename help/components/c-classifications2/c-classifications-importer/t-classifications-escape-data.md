---
description: 분류 파일에 있는 분류 데이터를 이스케이프 처리하는 방법을 설명하는 절차입니다.
solution: Analytics
subtopic: Classifications
title: 분류 데이터 이스케이프 처리
topic: Admin tools
uuid: 724edcc5-4990-4f24-afbb-9aef301791a7
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 분류 데이터 이스케이프 처리

분류 파일에 있는 분류 데이터를 이스케이프 처리하는 방법을 설명하는 절차입니다.

<!--Meike, please check this page against orginal. It might be missing information. -->

1. 분류 파일 형식이 v2.1인지 확인합니다.

   v2.1이 활성화되어 있으면 다음과 유사한 라인이 표시됩니다.

   >[!NOTE]
   >
   >To specify a format of v2.1, enable **[!UICONTROL Quoted Output]** when exporting the file on the [!UICONTROL Classification Importer] page ( [!UICONTROL Browser Export] or [!UICONTROL FTP Export]).

1. Surround the field containing special characters in double quotes (`"`).

A double quote character can appear in an escaped cell by replacing it with two double quote characters (`" "`). 예:

```
My String "of data"
```

이스케이프 처리된 셀:

```
"My String ""of data"""
```
