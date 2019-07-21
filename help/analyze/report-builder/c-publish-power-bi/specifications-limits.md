---
description: 'null'
seo-description: 'null'
seo-title: 제한 사항 및 사양
title: 제한 사항 및 사양
uuid: 6717 B 6 EA -7 E 01-49 B 8-8 F 6 E-FB 733 A 03 B 687
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 제한 사항 및 사양

## Power BI publishing restrictions {#section_D4BDD70B20F94A0FAE53531CA528AE42}

>[!NOTE]
>
>이러한 제한 사항은 "Power BI 데이터 세트 테이블로 리포트 빌더 요청 게시" 옵션에만 적용됩니다.

* 통합 문서당 최대 100개의 Report Builder 요청을 Power BI에 내보낼 수 있습니다.
* 예약 프로세스에서는 101번째 요청에 도달하면 요청 내보내기가 중단됩니다.
* 한 Report Builder 요청에 대해 Analytics 데이터 중 처음 10,000행만 Power BI에 보내지고, 나머지 행은 무시됩니다.

## Edit a Report Builder request after publishing to Power BI {#section_6989E74F68DD43F08D37C36B6777DB50}

>[!NOTE]
>
>이 사양은 "모든 리포트 빌더 요청을 Power BI 데이터 세트로 게시" 및 "통합 문서에 Power BI 데이터 세트 표로 게시" 옵션 옵션에 적용됩니다.

Report Builder 요청을 Power BI에 게시 후 편집하면 문제가 발생할 수 있습니다.

* **사례 1**: 통합 문서를 Power BI에 게시하고 해당 데이터를 기반으로 시각화를 생성합니다. 다음으로, 통합 문서를 변경하면 이 문서가 참조하는 데이터 세트의 열 중 하나가 사라집니다. 그러면 다시 게시합니다. 이로 인해 Power BI에서 시각화가 손상됩니다.

   **다음은 시각화가 어떻게 손상되는지에 대한 예입니다.**

   1. Report Builder에서 페이지 차원과 페이지 보기 횟수 지표를 사용하여 요청이 하나인 통합 문서를 만듭니다.
   1. Power BI에 게시하도록 [이 요청을 예약](../../../analyze/report-builder/whats-new-arb.md#section_0C26057C7DBB4068A643FDD688F6E463)합니다.
   1. Power BI에서, 페이지 및 페이지 보기 횟수에 대한 시각화를 생성합니다.
   1. 이제 요청에서 페이지 보기 횟수를 제거하여 통합 문서를 편집합니다.
   1. 업데이트된 통합 문서의 일정을 편집하고 요청을 Power BI에 다시 게시합니다.
   1. 새 통합 문서가 Power BI에 전송되면

      1. 처음 게시했을 때 만들어진 기존의 데이터 세트를 덮어쓰는지 확인합니다.
      1. page_1 표의 페이지 및 방문 횟수 열이 제대로 업데이트되었는지 확인합니다.
      1. 시각화가 page_1 표에 더 이상 표시되지 않는 페이지 보기 횟수 열을 참조해서 손상됨을 확인합니다.
   **다음은 시각화가 어떻게 손상되지 않는지에 대한 예입니다.**

   1. Report Builder에서 페이지 차원과 페이지 보기 횟수 지표를 사용하여 요청이 하나인 통합 문서를 만듭니다.
   1. Power BI에 게시하도록 [이 요청을 예약](../../../analyze/report-builder/whats-new-arb.md#section_0C26057C7DBB4068A643FDD688F6E463)합니다.
   1. Power BI에서, 페이지 및 페이지 보기 횟수에 대한 시각화를 생성합니다.
   1. 이제 페이지 및 페이지 보기 횟수를 유지하면서도 방문 지표를 추가하여 Report Builder에서 통합 문서를 편집합니다.
   1. 업데이트된 통합 문서의 일정을 편집하고 요청을 Power BI에 다시 게시합니다.
   1. 새 통합 문서가 Power BI에 전송되면

      1. 처음 게시했을 때 만들어진 기존의 데이터 세트를 덮어쓰는지 확인합니다.
      1. page_1 표의 페이지, 페이지 보기 횟수 및 방문 횟수 열이 제대로 업데이트되었는지 확인합니다.
      1. 시각화가 page_1 표에 여전히 표시되는 두 열을 참조해서 계속 제대로 작동됨을 확인합니다.


* **사례 2**: 통합 문서의 한 부분을 Power BI의 대시보드에 고정했다가 나중에 고정된 해당 부분(차트나 표)을 통합 문서에서 제거합니다. 이로 인해 시각화가 손상됩니다.

## Change the name of a Power BI report {#section_2E7893A78B914EBFACB2B08CBD9E472E}

기본적으로, 공백이 밑줄 문자로 대체된다는 점을 제외하면 보고서 이름은 통합 문서 파일 이름으로 채워집니다(.xlsx 확장명 없이 사용).

주의 사항

* 레이블은 행 및 열 주소용의 틀릴 수 있는 문자와 숫자의 조합일 수 없습니다. 예를 들어, A100은 워크시트에 있는 셀 주소이므로 레이블이 될 수 없습니다.
* 문자 '#', '@', '!', '$', '^', '&amp;', '*', '`', '~', ' '은 유효한 레이블 문자가 아닙니다. 이 문자들은 밑줄 문자로 대체됩니다.
* 유효하지 않은 이름을 입력하면 자동으로 생성된 이름을 제시하는 경고 메시지가 표시됩니다. **[!UICONTROL 예를]**&#x200B;클릭하면 이 이름이 사용됩니다. If you click **[!UICONTROL No]**, the Advanced Wizard UI will let you enter the new name.

