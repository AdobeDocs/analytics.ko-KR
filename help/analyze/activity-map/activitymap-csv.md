---
description: 표준 모드에서 Activity Map의 Analytics 데이터를 CSV(쉼표 구분 값) 파일로 내보내십시오.
seo-description: 표준 모드에서 Activity Map의 Analytics 데이터를 CSV(쉼표 구분 값) 파일로 내보내십시오.
seo-title: CSV 파일로 내보내기
solution: Analytics
title: CSV 파일로 내보내기
topic: Activity Map
uuid: dc 6 c 50 c 0-57 f 7-45 b 8-a 4 cb -2092 a 21 da 529
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# CSV 파일로 내보내기

표준 모드에서 Activity Map의 Analytics 데이터를 CSV(쉼표 구분 값) 파일로 내보내십시오.

사용자는 링크 클릭 데이터를 다른 데이터 소스와 병합하거나 다른 분석을 수행(예: Excel)해야 할 수 있습니다. CSV 내보내기를 이용하면 주어진 페이지에 대한 모든 Activity Map 데이터를 소비하기 쉬운 형식으로 얻을 수 있습니다. 또한 페이지에 대해 생성된 분석 데이터를 기본 CSV 파일에 저장하여 Page Report, [Page Flow Report](/help/analyze/activity-map/activitymap-page-flow.md)), and [Links on Page](/help/analyze/activity-map/activitymap-links-report.md) data. 그런 다음 스프레드시트 또는 텍스트 파일로 보거나, 데이터를 다른 시스템으로 가져올 수 있습니다.

Activity Map 도구 모음에서 [내보내기] 아이콘을 클릭합니다.

Activity Map에서는 Adobe Analytics 페이지 이름을 기반으로 파일 이름을 생성하고 여기에 날짜와 타임스탬프를 추가합니다(Pagename_DateTime.csv). 이 파일은 해당 브라우저에 대한 기본 다운로드 디렉토리에 저장됩니다.

| 내보내기 정보 | 설명 |
|---|---|
| 페이지 지표 보고서 | 페이지에서 보낸 시간, 페이지 클릭 수 및 총 페이지 보기 횟수를 포함한 Analytics의 페이지 지표 데이터. |
| 페이지 세부 사항 보고서 | 종료 데이터는 물론, 내부 항목 또는 외부 참조를 위한 이전 페이지를 식별하는 페이지 시작 및 종료 정보. |
| 페이지에 있는 링크 수 보고서 | 표준 또는 라이브 모드의 특정 페이지에 대한 링크 정보. |
