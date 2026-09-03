---
description: Report Builder 옵션에 대해 알아봅니다.
title: Report Builder 옵션
uuid: f2920dee-4245-4617-a02e-03726dde2bb5
feature: Report Builder
role: User, Admin
exl-id: d3388990-7919-461d-a96e-4c996b8bdb8b
TQID: https://experienceleague.adobe.com/56Wyy-f9kDXxFSanTNILr4rNQ0OB3YtbIFPcRT082sc
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: c153fd90-23e1-4614-81d3-3cc7571227f7id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 474
ht-degree: 39%

---

# Report Builder 옵션

{{legacy-arb}}

옵션 패널에서는 날짜 설정, 지연 설정(현재 데이터), 로그 정보를 지정하고, 업데이트를 구성할 수 있습니다.

1. 추가 기능 도구 모음에서 **[!UICONTROL 옵션]** ![](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Settings_18_N.svg)을 클릭합니다.

| 요소 | 설명 |
|--- |--- |
| [!UICONTROL 기준 날짜] |  |
| 현재 날짜로 설정 | Report Builder에서 현재 날짜를 사용하거나 새로 고침 시 사용할 날짜를 묻도록 [!UICONTROL 기준 날짜]를 지정하거나 재설정할 수 있도록 해 줍니다. |
| 새로 고칠 때마다 설정 여부 묻기 | 요청을 새로 고칠 때 [!UICONTROL 기준 날짜]를 설정할 수 있도록 해줍니다. |
| [!UICONTROL 최근 데이터] |  |
| [!UICONTROL 현재 데이터 포함] | Adobe Analytics에서 이 데이터가 처리되기 전이라도 보고 시 세부적인 부분까지 잠재 데이터([!UICONTROL 최근 데이터]라고도 함)를 볼 수 있도록 해 줍니다.<br>이 옵션을 사용하지 않으면 종결 모드(처리됨)가 사용되어 일반적으로 더 지연 상태가 됩니다.<br>이 설정은 호환하는 현재 데이터인 통합 문서의 모든 요청에 적용됩니다. 요청이 호환하지 않는 경우, 종결 모드가 적용됩니다.<br>현재 데이터 포함] 모드를 사용하려면 다음 상황을 참고하십시오.<br>**서식 옵션**: [표시 머리글 서식을 지정](/help/analyze/legacy-report-builder/layout/t-format-display-headers.md)할 때 이 정보([!UICONTROL 최근 데이터])를 표시할지 여부를 지정할 수 있습니다.<br>**분류**: 지원되지 않습니다. [!UICONTROL [!UICONTROL 최근 데이터] 모드가 현재 데이터로 설정되어 있고, 요청 중 하나에 분류 요소가 들어 있을 경우, 이 요청은 현재가 아닌 데이터 모드로 되돌아갑니다. 그러나 다른 요청은 현재 데이터 모드를 계속 사용합니다.<br>**요청 관리자**: 설정이 예약된 요청에 적용되었는지 확인할 수 있도록 요청 관리자에서 현재 데이터 열을 볼 수 있습니다.<br>**예약된 통합 문서**: 이 모드는 통합 문서 수준에서 예약 프로세스 중에 저장됩니다. 완료된 데이터를 사용하고 있는 예약된 통합 문서를 열고 [!UICONTROL 현재 데이터 포함]을 적용하면 그 후에 현재 모드가 사용됩니다.<br>**권한**: 현재 데이터에 액세스할 수 없는 사용자의 경우 이 옵션은 숨겨집니다.  이 옵션을 활성화하면 하나 이상의 요청을 적용할 수 없는 경우 경고가 표시됩니다. |
| 호환되지 않는 현재 데이터 요청 경고 비활성화 | [!UICONTROL 현재 데이터 포함] 모드를 선택했지만, 데이터를 편집된 요청에 적용할 수 없는 경우 경고를 표시합니다.  예를 들어, [!UICONTROL 현재 데이터 포함]을 설정한 다음, 세그먼트가 선택된 요청을 편집하는 경우, 경고가 표시됩니다. |
| 로컬 파일에 Report Builder 요청 기록(문제 해결) | 요청을 로컬 파일에 기록할 수 있습니다. 이 로그 파일을 사용하여 문제를 해결하십시오. |
| 입력된 값 해석... | 필터 컨트롤의 형식화된 값을 필터 식으로 간주하기 전에 셀 위치로 해석합니다.<br>예를 들어 필터 shoes를 사용하여 상위 10개 페이지 요청을 만드는 경우 다음과 유사한 항목이 들어 있는 셀이 요청에 표시됩니다.  필터: 상위 1-10페이지, 페이지에 Shoes 포함 |
| 새 버전을 사용할 수 있을 때 업데이트 | 시스템에 새 버전을 설치할 수 있는지 여부를 알려줍니다. |
