---
description: 표준 모드에서 분석 데이터를 [!DNL Activity Map]에서 CSV(쉼표로 구분된 값) 파일로 내보냅니다.
seo-description: 표준 모드에서 분석 데이터를 [!DNL Activity Map]에서 CSV(쉼표로 구분된 값) 파일로 내보냅니다.
seo-title: CSV 파일로 내보내기
solution: Analytics
title: CSV 파일로 내보내기
topic: Activity Map
uuid: dc6c50c0-57f7-45b8-a4cb-2092a21da529
translation-type: tm+mt
source-git-commit: 36637b76b8026fbf87ad48adcfa47386c530e732

---


# CSV 파일로 내보내기

In Standard Mode, export Analytics data from [!DNL Activity Map] to a Comma Separated Values (CSV) file.

사용자는 링크 클릭 데이터를 다른 데이터 소스와 병합하거나 다른 분석을 수행(예: Excel)해야 할 수 있습니다. CSV export allows you to obtain all of your [!DNL Activity Map] data for a given page in an easy-to-consume format. 페이지에 대해 생성된 분석 데이터를 플랫 CSV 파일로 저장하여 페이지 보고서, 페이지 흐름 보고서) 및 [페이지의](/help/analyze/activity-map/activitymap-page-flow.md)링크를 내보낼 수 [있습니다](/help/analyze/activity-map/activitymap-links-report.md) . 그런 다음 스프레드시트 또는 텍스트 파일로 보거나, 데이터를 다른 시스템으로 가져올 수 있습니다.

Click the Export icon on the [!DNL Activity Map] toolbar.

[!DNL Activity Map] adobe Analytics 페이지 이름을 기반으로 파일 이름을 생성하고 여기에 날짜 및 타임스탬프를 추가합니다.Pagename_DateTime.csv. 이 파일은 해당 브라우저에 대한 기본 다운로드 디렉토리에 저장됩니다.

| 내보내기 정보 | 설명 |
|---|---|
| 페이지 지표 보고서 | 페이지에서 보낸 시간, 페이지 클릭 수 및 총 페이지 보기 횟수를 포함한 Analytics의 페이지 지표 데이터. |
| 페이지 세부 사항 보고서 | 종료 데이터는 물론, 내부 항목 또는 외부 참조를 위한 이전 페이지를 식별하는 페이지 시작 및 종료 정보. |
| 페이지에 있는 링크 수 보고서 | 표준 또는 라이브 모드의 특정 페이지에 대한 링크 정보. |
