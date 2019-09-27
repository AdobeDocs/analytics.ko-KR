---
description: '[옵션] 패널에서는 날짜 설정, 지연 설정(현재 데이터), 로그 정보를 지정하고, 업데이트를 구성할 수 있습니다.'
seo-description: '[옵션] 패널에서는 날짜 설정, 지연 설정(현재 데이터), 로그 정보를 지정하고, 업데이트를 구성할 수 있습니다.'
seo-title: Report Builder 옵션
solution: Analytics
title: Report Builder 옵션
topic: Report Builder
uuid: f2920dee-4245-4617-a02e-03726dde2bb5
translation-type: tm+mt
source-git-commit: 0dbc8ac9b416ce50f197a884bb71c6cd389cd0bb

---


# Report Builder 옵션

[옵션] 패널에서는 날짜 설정, 지연 설정(현재 데이터), 로그 정보를 지정하고, 업데이트를 구성할 수 있습니다.

1. 추가 기능 도구 모음에서 **[!UICONTROL 선택 사항을 클릭합니다]** ![](assets/options_icon.png):

| 요소 | 설명 |
|--- |--- |
| [!UICONTROL 기준 날짜] |  |
| 현재 날짜로 설정 | Report Builder가 현재 날짜를 사용하거나 새로 고침 시 사용할 날짜를 묻도록 [!UICONTROL 기준 날짜]를 지정하거나 재설정할 수 있도록 해줍니다. |
| 새로 고칠 때마다 설정 여부 묻기 | 요청을 새로 고칠 때 [!UICONTROL 기준 날짜]를 설정할 수 있도록 해줍니다. |
| [!UICONTROL 최근 데이터] |  |
| [!UICONTROL 현재 데이터 포함] | Adobe Analytics에서 이 데이터가 처리 완료되기 전이라도, 경우에 따라 보고를 통해 세부적인 부분까지 잠재 데이터([!UICONTROL 최근 데이터]라고도 함)를 조회할 수 있게 해 줍니다.<br>이 옵션을 사용하지 않으면 종결 모드(처리됨)가 사용되어 일반적으로 더 [지연됩니다](https://marketing.adobe.com/resources/help/en_US/reference/data_latency.html).<br>이 설정은 호환하는 현재 데이터인 통합 문서의 모든 요청에 적용됩니다. 요청이 호환하지 않는 경우, 종결 모드가 적용됩니다.<br>현재 데이터 포함 모드: [!UICONTROL 형식] 옵션을 사용하기 위한 다음 상황을<br>**참고하십시오**.표시 헤더의서식을 지정할 때 이 정보( [최근](../../analyze/report-builder/layout/t-format-display-headers.md)데이터)를 표시할지 여부를 지정할 수 있습니다.<br>**분류**: 지원되지 않습니다. [!UICONTROL 최근 데이터] 모드가 [현재 데이터]로 설정되어 있고, 요청 중 하나에 분류 요소가 들어 있을 경우, 이 요청은 현재가 아닌 데이터 모드로 되돌아갑니다. 하지만 다른 요청은 계속 현재 데이터 모드를 사용합니다.<br>**요청 관리자**: 설정이 예약된 요청에 적용되는지 확인할 수 있는 요청 관리자의 현재 데이터 열을 볼 수 있습니다.<br>**예약된 통합 문서**: 이 모드는 통합 문서 수준에서 예약 프로세스 동안 저장됩니다. If you open a scheduled workbook that is using finalized data, and apply [!UICONTROL Include Current Data], current mode is used thereafter.<br>**권한**: 현재 데이터에 액세스할 수 없는 사용자에게는 이 옵션이 표시되지 않습니다.  이 옵션을 활성화하면, 하나 이상의 요청을 적용할 수 없는 경우 경고가 표시됩니다. |
| 요청과 호환되지 않는 현재 데이터 비활성화 경고 | [!UICONTROL 현재 데이터 포함] 모드를 선택했지만 데이터를 편집된 요청에 적용할 수 없는 경우 경고를 표시합니다.  예를 들어, [!UICONTROL 현재 데이터 포함]을 설정한 다음, 세그먼트가 선택되어 있는 요청을 편집하는 경우, 경고가 표시됩니다. |
| Report Builder 요청을 로컬 파일에 기록(문제 해결용) | 요청을 로컬 파일에 기록할 수 있도록 해줍니다. 문제 해결에 이 로그 파일을 사용합니다. |
| 입력된 값 해석... | 필터 컨트롤에 입력된 값을 필터 표현식으로 간주하기 전에 셀 위치로 해석합니다.<br>예를 들어 필터 shoes를 사용하여 상위 10개 페이지 요청을 만드는 경우 다음과 유사한 항목이 들어 있는 셀이 요청에 표시됩니다.  필터:Top 1-10 Page, Page contains Shoes |
| 새 버전을 사용할 수 있으면 업데이트 | 새 버전을 설치할 수 있으면 사용자에게 알리도록 합니다. |
