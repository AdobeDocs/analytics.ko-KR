---
title: 기존 Report Builder 통합 문서 변환
description: 기존 Report Builder 통합 문서를 마이그레이션하고 새 Report Builder으로 변환하는 방법에 대해 알아봅니다. Adobe Analytics 기반 통합 문서를 원활하게 변환하는 방법에 대한 이 마이그레이션 안내서의 단계별 지침을 따르십시오.
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: ff9011b2-fc18-456f-81dc-151b9e4fccd2
source-git-commit: 9743d7ac2a6c7e63d7a6701e60d05683c5680d36
workflow-type: tm+mt
source-wordcount: '1179'
ht-degree: 0%

---

# 기존 Report Builder 통합 문서 변환

레거시 Report Builder은 2026년 6월에 사용이 종료됩니다. 통합 문서를 기존 Report Builder에서 새 Report Builder으로 마이그레이션해야 합니다. 새 Report Builder은 기존 Report Builder으로 생성된 통합 문서를 신속하게 마이그레이션할 수 있는 편리한 방법을 제공합니다.

>[!IMPORTANT]
>
>각 통합 문서를 복제하고 기존 통합 문서를 변환하기 전에 한 가지 버전의 이름을 변경합니다. 필요한 경우 원본 레거시 통합 문서의 복사본을 항상 유지할 수 있습니다.


>[!BEGINSHADEBOX]

데모 비디오를 보려면 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [통합 문서 변환](https://experienceleague.adobe.com/ko/docs/analytics-learn/tutorials/exporting/report-builder/upgrade-and-reschedule-workbooks){target="_blank"}을 참조하세요.

>[!ENDSHADEBOX]


>[!NOTE]
>
>기존 통합 문서를 변환하려면 먼저 [새 Report Builder을 설정](/help/analyze/report-builder/report-builder-setup.md)해야 합니다.


## 레거시 통합 문서 열기

레거시 통합 문서를 열려면 다음을 수행할 수 있습니다.

* **[!UICONTROL Report Builder 허브]**&#x200B;의 [예약](report-builder-hub.md) 탭에서 예약된 레거시 통합 문서를 엽니다. 이 작업은 예약된 기존 통합 문서에 대해 선호되는 방법입니다. [전환된 레거시 통합 문서를 예약](#schedule-a-converted-legacy-workbook)하는 즉시 레거시 통합 문서와 연결된 일정을 사용할 수 있는 옵션이 제공됩니다.

   1. [!DNL Excel]을(를) 열고 ![&#x200B; 리본 모음에서 &#x200B;](/help/assets/icons/AdobeLogoRedOnWhite.svg)AdobeLogoRedonWhite **&#x200B;**&#x200B;Report Builder[!DNL Excel]을(를) 선택합니다.

   1. **[!UICONTROL 로그인]**&#x200B;을 선택하고 Report Builder에 로그인합니다.

   1. **[!UICONTROL Report Builder 허브]**&#x200B;에서 [예약](report-builder-hub.md)을 선택하세요.
   1. **[!UICONTROL 레거시]** 탭을 선택합니다. 탭에는 사용자가 만든 레거시 Report Builder 기반 예약 통합 문서가 나열됩니다.

      ![레거시 워크플로](assets/upgrade-legacy-schedule.png)

   1. 목록에서 변환할 예약된 통합 문서를 ![SelectBox](/help/assets/icons/SelectBox.svg)을(를) 선택하고 ![다운로드](/help/assets/icons/Download.svg)를 선택합니다. 통합 문서가 다운로드되어 [!DNL Excel]의 새 창에서 열립니다. 이제 [기존 Report Builder 통합 문서를 변환](#convert-a--workbook)할 수 있습니다.


* 로컬 컴퓨터나 네트워크에서 직접 레거시 통합 문서를 엽니다. 이 방법을 사용하면 기존 통합 문서와 연결할 수 있는 일정을 사용할 수 없습니다. <br/>이전 통합 문서가 [!DNL Excel]에 열려 있는 경우:

   1. ![&#x200B; 리본 표시줄에서 &#x200B;](/help/assets/icons/AdobeLogoRedOnWhite.svg)AdobeLogoRedOnWhite **&#x200B;**&#x200B;Report Builder[!DNL Excel]을(를) 선택합니다.
   1. **[!UICONTROL 로그인]**&#x200B;을 선택하고 Report Builder에 로그인합니다.
   1. [기존 통합 문서를 변환](#convert-a-workbook)합니다.


## 레거시 통합 문서 변환

기존 통합 문서를 변환하려면 다음을 수행하십시오.

1. 레거시 통합 문서를 열면 새 Report Builder에서 이 통합 문서에 [레거시 Report Builder](/help/analyze/legacy-report-builder/home.md) 요청이 포함되어 있는지 감지합니다.

   ![마이그레이션 업그레이드를 보여 주는 [!DNL Excel] Report Builder 업그레이드 보고서의 스크린샷](assets/upgrade-workbook.png){zoomable="yes"}

1. 하나 이상의 레거시 요청이 있는 경우 **[!UICONTROL 통합 문서 업그레이드]** 대화 상자에서 **[!UICONTROL 업그레이드]**&#x200B;을 클릭하여 통합 문서를 업그레이드하십시오.

   >[!NOTE]
   >
   >각 요청을 개별적으로 업그레이드해야 합니다. 대량 업그레이드는 지원되지 않습니다.


1. 업그레이드할 경우 통합 문서 변경 내용을 알리는 **[!UICONTROL 경고]** 대화 상자가 나타납니다. 계속하기 전에 이전 통합 문서의 백업을 만들어야 합니다.

   ![마이그레이션 경고를 표시하는 [!DNL Excel] Report Builder 업그레이드 보고서의 스크린샷](assets/upgrade-warning.png){zoomable="yes"}

1. 업그레이드를 계속하려면 **[!UICONTROL 계속 진행]**&#x200B;을 클릭하세요.

   업그레이드에 성공하면 **[!UICONTROL 통합 문서 업그레이드가 완료되었습니다]** 알림이 표시됩니다.

   ![마이그레이션이 완료되었음을 나타내는 [!DNL Excel] Report Builder 업그레이드 보고서의 스크린샷](assets/upgrade-complete.png)

   * 알림을 닫고 새 Report Builder에 대해 업데이트된 요청이 있는 통합 문서에서 계속 작업하려면 **[!UICONTROL 닫기]**&#x200B;를 선택하십시오.

   * **[!UICONTROL 업그레이드 보고서 다운로드]**&#x200B;를 선택하여 업그레이드 결과를 표시하는 새 [!DNL Excel] 통합 문서를 다운로드하고 엽니다. 예를 들어 아래를 참조하십시오.

     마이그레이션 보고서를 표시하는 ![&#x200B; Report Builder 업그레이드 보고서의 [!DNL Excel]스크린샷](assets/upgrade-report.png)

이제 통합 문서에서 [데이터 블록을 관리](/help/analyze/report-builder/manage-reportbuilder.md)할 수 있습니다. 이러한 데이터 블록은 업그레이드 결과이며 기존 Report Builder 요청을 대체합니다.


## 전환된 레거시 통합 문서 예약

Report Builder 허브의 **[!UICONTROL 예약]** 탭에서 다운로드하고 연 기존 통합 문서의 예약 세부 정보를 사용할 수 있는 옵션이 있습니다. 로컬 컴퓨터 또는 네트워크에서 여는 일정 세부 정보가 있는 레거시 통합 문서에는 이 옵션을 사용할 수 없습니다.

1. 변환된 이전 통합 문서를 이전 일정으로 예약하려면 다음과 같이 하십시오.

   * Report Builder 허브에서 **[!UICONTROL 통합 문서 보내기]**&#x200B;를 선택하거나
   * Report Builder의 **[!UICONTROL 일정]** 탭에서 사용할 수 있는 **[!UICONTROL 통합 문서]** 탭에서 **[!UICONTROL 통합 문서 예약]**&#x200B;을 선택합니다.

1. 기존 통합 문서의 일정 세부 정보를 기본 일정 설정으로 사용할 수 있습니다.

   ![Report Builder 레거시 일정 설정 옵션 [!DNL Excel]의 스크린샷](assets/upgrade-legacy-schedule-convert.png)

   * 기존 일정 세부 정보를 사용하려면 **[!UICONTROL 사용]**&#x200B;을 선택하세요. 일정 세부 정보는 [통합 문서 보내기](schedule-reportbuilder.md#schedule-a-workbook) 인터페이스에 미리 채워집니다.
   * 기존 일정 세부 정보를 사용하지 않으려면 **[!UICONTROL 사용하지 않음]**&#x200B;을 선택하십시오.
   * 취소하려면 **[!UICONTROL 취소]**&#x200B;를 선택합니다.

   나중에 이 통합 문서에 대한 레거시 일정 세부 정보를 사용하지 않으려면 **[!UICONTROL 나중에 사용할 레거시 메타데이터 제거]**&#x200B;를 선택하십시오.


## 기존 Report Builder에서 마이그레이션

기존 Report Builder의 일부 기능은 Report Builder에서 지원되지 않거나, 부분적으로 지원되거나, 다르게 구현됩니다.

* **실시간 요청**. 실시간 요청은 지원되지 않으며 변환된 기존 통합 문서에서 제거됩니다.

* **경로/폴아웃 보고**. 폴아웃 요청은 지원되지 않으며 변환된 레거시 통합 문서에서 제거됩니다.

* 예약된 보고서에 대한 **[!DNL FTP]옵션**. 보고서를 [!DNL FTP] 위치로 보내도록 예약하는 옵션을 더 이상 사용할 수 없습니다.

* **예약된 보고서에 대한 [!DNL Power BI] 옵션에 통합 문서 게시**. [!DNL Power BI]에 보고서를 예약하는 옵션을 더 이상 사용할 수 없습니다.

* **방문자 지표**. 보고 결과가 정확히 일치하지 않더라도 다음 지표는 변환된 레거시 통합 문서에서 *고유 방문자*(으)로 변환됩니다. `visitorshourly`, `visitorsdaily`, `visitorsweekly`, `visitorsmonthly`, `visitorsquarterly` 및 `visitorsyearly`. 이 변환은 `mobilevisitorshourly`, `mobilevisitorsdaily`, `mobilevisitorsweekly`, `mobilevisitorsmonthly`, `mobilevisitorsquarterly` 및 `mobilevisitorsyearly`에도 적용됩니다.

* **자동 재인증**. 새 [!DNL Excel] 파일을 열 때 명시적으로 다시 인증해야 합니다. 이 재인증은 [!DNL Office Add-ins] 기능의 보안 기능입니다.

* **데이터 블록 그룹이 있는 워크시트를 복사합니다**. 두 개 이상의 데이터 블록이 포함된 워크시트의 복사를 지원하려면 다음 작업을 수행하십시오.

   1. [!DNL Excel] 통합 문서에서 복사할 워크시트 탭을 선택합니다.
   1. 탭의 컨텍스트 메뉴에서 **[!UICONTROL 이동 또는 복사...]**&#x200B;를 선택합니다.
   1. **[!UICONTROL 이동 또는 복사]** 대화 상자에서:
      1. 복사한 워크시트를 복사할 위치를 선택합니다.
      1. **[!UICONTROL 복사본 만들기]**&#x200B;를 사용하도록 설정해야 합니다.
      1. **[!UICONTROL 확인]**&#x200B;을 선택합니다.
   1. 소스 워크시트에서
      1. 모든 데이터 블록을 포함하는 셀 범위를 선택합니다.
      1. ![Report Builder 허브](/help/assets/icons/Copy.svg)에서 **[!UICONTROL 복사]** [데이터 블록 복사](/help/analyze/report-builder/report-builder-hub.md)를 선택합니다.
   1. 대상 워크시트에서
      1. 복사한 셀 범위를 붙여 넣을 셀을 선택합니다.
      1. ![Report Builder 허브](/help/assets/icons/Paste.svg)에서 **[!UICONTROL 붙여넣기]** [데이터 블록 붙여넣기](/help/analyze/report-builder/report-builder-hub.md)를 선택합니다.

* **날짜 범위**. Report Builder은 기존 Report Builder의 날짜 범위에 대한 행 레이블에 적용된 날짜 범위 서식 옵션 **[!UICONTROL 시작 및 종료 기간을]**(으)로 표시&rbrack;를 마이그레이션하지 않습니다.

* **평균**. Report Builder은 선택한 서식 옵션 **[!UICONTROL 평균 옵션]**(**[!UICONTROL 일별 평균]** ~ **[!UICONTROL 연간 평균]**)을(를) 기존 Report Builder의 지표에 적용하지 않습니다. 계산된 지표를 사용하여 선택한 옵션을 대체합니다.

* **텍스트 앞에 추가/뒤에 추가**. Report Builder은 기존 Report Builder의 지표에 적용된 **[!UICONTROL Prepend/postpend 텍스트]**&#x200B;를 마이그레이션하지 않습니다.

* **소계**. Report Builder은 기존 Report Builder의 지표에 적용된 서식 옵션 **[!UICONTROL SubTotal(이 요청)]**&#x200B;을(를) 마이그레이션하지 않습니다. 이전 통합 문서 요청에서 **[!UICONTROL SubTotal(이 요청)]**&#x200B;을(를) 사용하면 기능이 **[!UICONTROL Total]**(으)로 변환됩니다. 예를 들어 상위 5개 페이지 이름이 있는 레거시 데이터 블록에서 **[!UICONTROL SubTotal(페이지 보기 수)]**&#x200B;을 사용하여 상위 5개 페이지 이름에 대한 페이지 보기 수의 합계를 반환합니다. 마이그레이션 후 상위 5개의 페이지 이름을 가진 동일한 데이터 블록이 *모두*&#x200B;개의 페이지 이름에 대한 페이지 보기 횟수 합계를 반환합니다. 기존 **[!UICONTROL SubTotal]** 기능을 대체하려면 계산된 지표 기능을 사용하십시오.
