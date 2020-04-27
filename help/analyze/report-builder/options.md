---
description: 옵션 패널에서는 날짜 설정, 지연 설정(현재 데이터), 로그 정보를 지정하고, 업데이트를 구성할 수 있습니다.
title: Report Builder 옵션
topic: Report builder
uuid: f2920dee-4245-4617-a02e-03726dde2bb5
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Report Builder 옵션

옵션 패널에서는 날짜 설정, 지연 설정(현재 데이터), 로그 정보를 지정하고, 업데이트를 구성할 수 있습니다.

1. In the Add-Ins toolbar, click **[!UICONTROL Options]** ![](assets/options_icon.png):

| 요소 | 설명 |
|--- |--- |
| [!UICONTROL As Of Date] |  |
| 현재 날짜로 설정 | Lets you specify or reset the  [!UICONTROL As Of Date] so that report builder uses the current date or asks you which date to use upon refresh. |
| 새로 고칠 때마다 설정 여부 묻기 | 요청을 새로 고칠 [!UICONTROL As Of Date] 때 을 설정할 수 있습니다. |
| [!UICONTROL Data Recency] |  |
| [!UICONTROL Include Current Data] | Lets you view data latency (also known as  [!UICONTROL Data Recency]) down to the minute in reporting, occasionally even before this data has been processed by  Adobe Analytics.<br>이 선택 사항을 사용하지 않으면 종결 모드(처리됨)가 사용되어 일반적으로 더 [지연](https://marketing.adobe.com/resources/help/ko_KR/reference/data_latency.html)됩니다.<br>이 설정은 호환하는 현재 데이터인 통합 문서의 모든 요청에 적용됩니다. 요청이 호환하지 않는 경우, 종결 모드가 적용됩니다.<br>모드 사용에 대한 다음 상황에 유의하십시오 [!UICONTROL Include Current Data] :<br>**형식 옵션&#x200B;**:표시 헤더의[!UICONTROL Data Recency]서식을 지정할 때 이 정보([](/help/analyze/report-builder/layout/t-format-display-headers.md))를 표시할지 여부를 지정할 수 있습니다.<br>**분류**: 지원되지 않습니다. If the  [!UICONTROL Data Recency] mode is set to the Current Data, and one of the requests contains a break-down element, this request reverts to non-current data mode. 하지만 다른 요청은 계속 현재 데이터 모드를 사용합니다.<br>**요청 관리자&#x200B;**: 설정이 예약된 요청에 적용되는지 확인할 수 있는 요청 관리자의 현재 데이터 열을 볼 수 있습니다.<br>**예약된 통합 문서**: 이 모드는 통합 문서 수준에서 예약 프로세스 동안 저장됩니다. If you open a scheduled workbook that is using finalized data, and apply [!UICONTROL Include Current Data], current mode is used thereafter.<br>**권한&#x200B;**: 현재 데이터에 액세스할 수 없는 사용자에게는 이 옵션이 표시되지 않습니다.  이 옵션을 활성화하면, 하나 이상의 요청을 적용할 수 없는 경우 경고가 표시됩니다. |
| 요청과 호환되지 않는 현재 데이터 비활성화 경고 | Displays warnings if the  [!UICONTROL Include Current Data] mode is selected but the data mode cannot be applied to the edited request.  For example, if you set [!UICONTROL Include Current Data], and then edit a request that has a segment selected, a warning is issued. |
| Report Builder 요청을 로컬 파일에 기록(문제 해결용) | 요청을 로컬 파일에 기록할 수 있도록 해줍니다. 문제 해결에 이 로그 파일을 사용합니다. |
| 입력된 값 해석... | 필터 컨트롤에 입력된 값을 필터 표현식으로 간주하기 전에 셀 위치로 해석합니다.<br>예를 들어 필터 shoes를 사용하여 상위 10개 페이지 요청을 만드는 경우 다음과 유사한 항목이 들어 있는 셀이 요청에 표시됩니다.  필터: 상위 1-10페이지, 페이지에 Shoes 포함 |
| 새 버전을 사용할 수 있으면 업데이트 | 새 버전을 설치할 수 있으면 사용자에게 알리도록 합니다. |
