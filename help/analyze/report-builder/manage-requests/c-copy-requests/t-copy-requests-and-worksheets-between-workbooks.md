---
description: 한 소스 통합 문서의 한 스프레드시트 전체를 하나 이상의 대상 통합 문서에 있는 한 스프레드시트에 복사합니다.
seo-description: 한 소스 통합 문서의 한 스프레드시트 전체를 하나 이상의 대상 통합 문서에 있는 한 스프레드시트에 복사합니다.
seo-title: 통합 문서 간 요청 및 워크시트 복사
solution: Analytics
title: 통합 문서 간 요청 및 워크시트 복사
topic: Report Builder
uuid: 6 B 2 C 4259-D 8 CB -430 E -819 F -38 E 213 DD 2661
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 통합 문서 간 요청 및 워크시트 복사

한 소스 통합 문서의 한 스프레드시트 전체를 하나 이상의 대상 통합 문서에 있는 한 스프레드시트에 복사합니다.

이렇게 하려면 동일한 Excel 인스턴스에서 열린 통합 문서가 두 개 이상 있어야 합니다. 첫 번째 소스 통합 문서에는 셀에 매핑된 요청이 있는 스프레드시트(워크시트)가 들어 있는 반면 다른 대상 통합 문서들은 대상(목적지)입니다. 각각의 새로운 대상 통합 문서에 대해 요청이 포함된 스프레드시트를 붙여넣으려면 먼저 소스 통합 문서와 동일한 보고서 세트에 로그인해야 합니다.
1. Right-click the spreadsheet in the source workbook and select **[!UICONTROL Copy Worksheet w/Requests]**.
1. In the destination workbook, right-click the spreadsheet and select **[!UICONTROL Paste Worksheet w/Requests]**.

   동일한 Excel 인스턴스는 사용자의 컴퓨터에서 한 번에 하나의 Excel 프로세스([!DNL excel.exe])가 실행되고 있음을 의미합니다. Excel 인스턴스 두 개를 실행시키고 첫 번째 Excel 인스턴스에 있는 통합 문서의 워크시트를 두 번째 Excel 인스턴스에 있는 통합 문서에 복사하려 시도하는 경우 Report Builder에서는 워크시트를 붙여넣는 옵션을 두 번째 Excel 인스턴스의 바로 가기 메뉴에 표시하지 않습니다.

   서로 다른 보고서 세트를 사용하여 소스 및 대상 통합 문서에 로그인하는 경우 붙여넣기 작업을 하면 대상 통합 문서의 서식에 영향을 주는 것들만 확인할 수 있습니다. Report Builder에는 지정된 보고서 세트(소스 통합 문서 내)에서 나온 요청에 대한 정보를 대상 통합 문서에 사용할 수 없음을 설명하는 메시지가 표시됩니다. 대상 통합 문서에 붙여넣은 요청이 표시되도록 하려면 소스 통합 문서와 동일한 보고서 세트를 사용하여 대상 통합 문서에 로그인해야 합니다.

   다른 통합 문서가 동일한 Excel 인스턴스에서 다른 문서로 열려 있기만 하면 하나의 통합 문서에 있는 스프레드시트에서 하나 이상의 요청을 복사하여 그 다른 통합 문서의 스프레드시트에 붙여넣을 수 있습니다. 두 통합 문서 모두에서 요청은 동일한 보고서 세트 로그인을 사용하여 만들어야 합니다.
