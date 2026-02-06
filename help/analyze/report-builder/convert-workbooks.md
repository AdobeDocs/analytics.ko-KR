---
title: 기존 Report Builder 통합 문서 변환
description: 기존 Report Builder 기반 통합 문서를 새 Report Builder을 사용하도록 변환하는 방법을 이해합니다.
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: ff9011b2-fc18-456f-81dc-151b9e4fccd2
source-git-commit: 504cce24babdd8aefa5f819433139671904f2e1e
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 0%

---

# 기존 Report Builder 통합 문서 변환

새 Report Builder 기능으로 이동하는 과정의 일부로 현재 레거시 Report Builder 기반 통합 문서(레거시 통합 문서)를 새 Report Builder [데이터 블록](create-a-data-block.md) 기능을 사용하도록 빠르게 변환할 수 있습니다.

>[!IMPORTANT]
>
>각 통합 문서를 복제하고 기존 통합 문서를 변환하기 전에 한 가지 버전의 이름을 변경합니다. 필요한 경우 원본 레거시 통합 문서의 복사본을 항상 유지할 수 있습니다.


>[!BEGINSHADEBOX]

데모 비디오를 보려면 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [통합 문서 변환](https://video.tv.adobe.com/v/3434957?quality=12&learn=on){target="_blank"}을 참조하세요.

>[!ENDSHADEBOX]


>[!NOTE]
>
>기존 통합 문서를 변환하려면 먼저 [새 Report Builder을 설정](/help/analyze/report-builder/report-builder-setup.md)해야 합니다.


## 레거시 통합 문서 열기

레거시 통합 문서를 열려면 다음을 수행할 수 있습니다.

* **[!UICONTROL Report Builder 허브]**&#x200B;의 [예약](report-builder-hub.md) 탭에서 예약된 레거시 통합 문서를 엽니다. 예약된 기존 통합 문서에 대해 선호되는 방법입니다. [전환된 레거시 통합 문서를 예약](#schedule-a-converted-legacy-workbook)하는 즉시 레거시 통합 문서와 연결된 일정을 사용할 수 있는 옵션이 제공됩니다.

   1. Excel을 열고 Excel 리본 표시줄에서 ![AdobeLogoRedonWhite](/help/assets/icons/AdobeLogoRedOnWhite.svg) **[!UICONTROL Report Builder]**&#x200B;을(를) 선택합니다.

   1. **[!UICONTROL 로그인]**&#x200B;을 선택하고 Report Builder에 로그인합니다.

   1. **[!UICONTROL Report Builder 허브]**&#x200B;에서 [예약](report-builder-hub.md)을 선택하세요.
   1. **[!UICONTROL 레거시]** 탭을 선택합니다. 탭에는 기존 Report Builder 기반 예약된 통합 문서가 나열됩니다.

      ![레거시 워크플로](assets/upgrade-legacy-schedule.png)

   1. 목록에서 변환할 예약된 통합 문서를 ![SelectBox](/help/assets/icons/SelectBox.svg)을(를) 선택하고 ![다운로드](/help/assets/icons/Download.svg)를 선택합니다. 통합 문서가 다운로드되어 Excel의 새 창에 열립니다. 이제 [기존 Report Builder 통합 문서를 변환](#convert-a--workbook)할 수 있습니다.


* 로컬 컴퓨터나 네트워크에서 직접 레거시 통합 문서를 엽니다. 이 방법을 사용하면 기존 통합 문서와 연결할 수 있는 일정을 사용할 수 없습니다. <br/>이전 통합 문서가 Excel에 열려 있는 경우:

   1. Excel 리본 표시줄에서 ![AdobeLogoRedonWhite](/help/assets/icons/AdobeLogoRedOnWhite.svg) **[!UICONTROL Report Builder]**&#x200B;을(를) 선택합니다.
   1. **[!UICONTROL 로그인]**&#x200B;을 선택하고 Report Builder에 로그인합니다.
   1. [기존 통합 문서를 변환](#convert-a-workbook)합니다.


## 레거시 통합 문서 변환

기존 통합 문서를 변환하려면 다음을 수행하십시오.

1. 레거시 통합 문서를 열면 새 Report Builder에서 이 통합 문서에 [레거시 Report Builder](/help/analyze/legacy-report-builder/home.md) 요청이 포함되어 있는지 감지합니다.

   ![통합 문서 업그레이드 프롬프트](assets/upgrade-workbook.png){zoomable="yes"}

1. 하나 이상의 레거시 요청이 있는 경우 **[!UICONTROL 통합 문서 업그레이드]** 대화 상자에서 **[!UICONTROL 업그레이드]**&#x200B;을 클릭하여 통합 문서를 업그레이드하십시오.

   >[!NOTE]
   >
   >각 요청을 개별적으로 업그레이드해야 합니다. 대량 업그레이드는 지원되지 않습니다.


1. 업그레이드할 경우 통합 문서 변경 내용을 알리는 **[!UICONTROL 경고]** 대화 상자가 나타납니다. 계속하기 전에 이전 통합 문서의 백업을 만들어야 합니다.

   ![업그레이드 경고](assets/upgrade-warning.png){zoomable="yes"}

1. 업그레이드를 계속하려면 **[!UICONTROL 계속 진행]**&#x200B;을 클릭하세요.

   업그레이드에 성공하면 **[!UICONTROL 통합 문서 업그레이드가 완료되었습니다]** 알림이 표시됩니다.

   ![업그레이드 완료](assets/upgrade-complete.png)

   * 알림을 닫고 새 Report Builder에 대해 업데이트된 요청이 있는 통합 문서에서 계속 작업하려면 **[!UICONTROL 닫기]**&#x200B;를 선택하십시오.

   * 업그레이드 결과를 표시하는 새 Excel 통합 문서를 다운로드하여 열려면 **[!UICONTROL 업그레이드 보고서 다운로드]**&#x200B;를 선택하십시오. 예를 들어 아래를 참조하십시오.

     ![Excel Report Builder 업그레이드 보고서 통합 문서](assets/upgrade-report.png)

이제 통합 문서에서 [데이터 블록을 관리](/help/analyze/report-builder/manage-reportbuilder.md)할 수 있습니다. 이러한 데이터 블록은 업그레이드 결과이며 기존 Report Builder 요청을 대체합니다.


## 전환된 레거시 통합 문서 예약

Report Builder 허브의 **[!UICONTROL 예약]** 탭에서 다운로드하고 연 기존 통합 문서의 예약 세부 정보를 사용할 수 있는 옵션이 있습니다. 로컬 컴퓨터 또는 네트워크에서 여는 일정 세부 정보가 있는 레거시 통합 문서에는 이 옵션을 사용할 수 없습니다.

1. 변환된 이전 통합 문서를 이전 일정으로 예약하려면 다음과 같이 하십시오.

   * Report Builder 허브에서 **[!UICONTROL 통합 문서 보내기]**&#x200B;를 선택하거나
   * Report Builder의 **[!UICONTROL 일정]** 탭에서 사용할 수 있는 **[!UICONTROL 통합 문서]** 탭에서 **[!UICONTROL 통합 문서 예약]**&#x200B;을 선택합니다.

1. 기존 통합 문서의 일정 세부 정보를 기본 일정 설정으로 사용할 수 있습니다.

   ![이전 통합 문서 일정 마이그레이션](assets/upgrade-legacy-schedule-convert.png)

   * 기존 일정 세부 정보를 사용하려면 **[!UICONTROL 사용]**&#x200B;을 선택하세요. 일정 세부 정보는 [통합 문서 보내기](schedule-reportbuilder.md#schedule-a-workbook) 인터페이스에 미리 채워집니다.
   * 기존 일정 세부 정보를 사용하지 않으려면 **[!UICONTROL 사용하지 않음]**&#x200B;을 선택하십시오.
   * 취소하려면 **[!UICONTROL 취소]**&#x200B;를 선택합니다.

   나중에 이 통합 문서에 대한 레거시 일정 세부 정보를 사용하지 않으려면 **[!UICONTROL 나중에 사용할 레거시 메타데이터 제거]**&#x200B;를 선택하십시오.


## 레거시 Report Builder 기능은 지원되지 않음 {#unsupported}

일부 이전 Report Builder 기능은 새 Report Builder에서 더 이상 사용할 수 없습니다

* 실시간 요청.

* 경로/폴아웃 보고.

* 예약된 보고서에 대한 FTP 옵션

* 방문자 지표. 보고 결과가 정확히 일치하지 않더라도 다음 지표가 *고유 방문자 수*(으)로 변환됩니다. `visitorshourly`, `visitorsdaily`, `visitorsweekly`, `visitorsmonthly`, `visitorsquarterly` 및 `visitorsyearly`. 이 변환은 `mobilevisitorshourly`, `mobilevisitorsdaily`, `mobilevisitorsweekly`, `mobilevisitorsmonthly`, `mobilevisitorsquarterly` 및 `mobilevisitorsyearly`에도 적용됩니다.
