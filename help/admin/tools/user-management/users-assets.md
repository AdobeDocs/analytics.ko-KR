---
description: Adobe Admin Console에서 Analytics 사용자 및 해당 에셋을 관리합니다.
title: Analytics 사용자 및 자산 관리
feature: Admin Tools
exl-id: 849a8279-4850-4458-bdd2-85052a17ee21
role: Admin
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 4%

---

# 기존 사용자 계정, 자산, 만료 관리

**[!UICONTROL 관리자] > [!UICONTROL 모든 관리자] > [!UICONTROL Analytics 사용자 및 관리자]**&#x200B;를 사용하여 이전 사용자 계정, 마이그레이션 상태, 만료 데이터, 다른 사용자로의 자산 전송 등을 관리할 수 있습니다.

사용자 화면에는 현재 Adobe Analytics 사용자 목록과 함께 다음 열이 표시됩니다.

| 열 | 설명 |
|---|---|
| [!UICONTROL 사용자 ID] | 사용자가 Adobe Analytics에 로그인하는 데 사용하는 사용자 ID입니다. |
| [!UICONTROL 이름] | 사용자의 이름입니다. |
| [!UICONTROL 마이그레이션 상태] | 기존 사용자 계정에서 Enterprise ID 또는 Adobe ID으로의 마이그레이션 상태입니다.  상태가 시작되지 않음, 큐에 있음 또는 마이그레이션됨일 수 있습니다. |
| [!UICONTROL 이메일] | 사용자의 이메일입니다. |
| [!UICONTROL 기존 로그인] | 활성화 또는 비활성화가 가능한 기존 로그인의 상태입니다. |
| [!UICONTROL 생성된 일자] | Adobe Analytics에서 사용자 계정이 생성된 타임스탬프. |
| [!UICONTROL 마지막 Analytics 액세스] | Adobe Analytics에 대한 사용자 계정의 최신 액세스 타임스탬프 |
| [!UICONTROL 만료] | 사용자 계정의 만료 날짜 또는 사용자 계정이 만료되지 않는 경우 없음. |

![사용자](assets/users.png) 참조

- 특정 사용자를 검색하려면 ![검색](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Search_18_N.svg) *제목별 검색* 필드를 사용하십시오.
- 마이그레이션 상태에서 목록을 필터링하려면 ![V자형 화살표](https://spectrum.adobe.com/static/icons/ui_18/ChevronSize100.svg) **[!UICONTROL 마이그레이션 상태]**&#x200B;를 선택하십시오.
- 기존 로그인 상태에서 목록을 필터링하려면 ![V자형 화살표](https://spectrum.adobe.com/static/icons/ui_18/ChevronSize100.svg) **[!UICONTROL 기존 로그인]**&#x200B;을 선택하십시오.
- 열 표시를 변경하려면 ![열 설정](https://spectrum.adobe.com/static/icons/workflow_18/Smock_ColumnSettings_18_N.svg)을 선택하고 팝업에서 열을 선택합니다.

목록에서 사용자를 한 명 이상 선택할 때 다양한 작업을 적용할 수 있습니다.

| 액션 | 설명 |
|---|---|
| ![마이그레이션](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Briefcase_18_N.svg) **[!UICONTROL 마이그레이션]** | 한 명 이상의 사용자를 Enterprise ID 또는 Adobe ID로 마이그레이션할 수 있습니다. |
| ![일정 잠김](https://spectrum.adobe.com/static/icons/workflow_18/Smock_CalendarLocked_18_N.svg) **[!UICONTROL 만료 설정]** | 선택한 사용자의 기존 Adobe Analytics 로그인을 사용하기 위한 만료 날짜를 설정할 수 있습니다.  달력 팝업을 사용할 날짜를 선택하여 날짜를 지정합니다. **[!UICONTROL 완료]**&#x200B;를 선택하여 만료를 확인합니다. |
| ![자산 전송](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Switch_18_N.svg) **[!UICONTROL 자산 전송]** | 이 작업은 한 명의 사용자를 선택하는 경우에만 사용할 수 있습니다. 사용자에게 양도 가능한 에셋이 있는 경우 계정 항목(예: 책갈피, 대시보드 등)을 선택할 수 있습니다. 전송을 완료하려면 **[!UICONTROL 전송]**&#x200B;을 선택하십시오.<br/>![자산 전송](assets/transfer-assets.png) |
| ![계정 삭제](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Delete_18_N.svg) **[!UICONTROL 계정 삭제]** | 선택한 계정의 삭제를 확인하는 대화 상자가 표시됩니다. 계정을 삭제하려면 **[!UICONTROL 확인]**&#x200B;을 선택하세요. 취소하려면 **[!UICONTROL 취소]**&#x200B;를 선택합니다. |
| ![CSV로 내보내기](https://spectrum.adobe.com/static/icons/workflow_18/Smock_FileCSV_18_N.svg) **[!UICONTROL CSV로 내보내기]** | 이 작업은 선택한 사용자의 세부 사항(이름, 마이그레이션 상태, 이메일 등)을 쉼표로 구분한 값 목록이 포함된 파일을 즉시 다운로드합니다. |

