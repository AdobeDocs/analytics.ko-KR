---
description: Analysis Workspace에서 데이터를 복사하거나 PDF 및 CSV 형식으로 다운로드할 수 있습니다.
title: PDF 또는 CSV 파일 다운로드
feature: Curate and Share
role: User, Admin
exl-id: 085013dc-8263-4fc8-9492-99f0ecadf14b
source-git-commit: 04c588cbe8cd4cc9b8d6fe162e3623c2be076325
workflow-type: tm+mt
source-wordcount: '1044'
ht-degree: 89%

---

# PDF 또는 CSV 파일 다운로드

Analysis Workspace에서 데이터를 내보내는 방법에는 여러 가지가 있습니다. 선택할 방법은 분석하려는 데이터 세트와 해당 데이터에 액세스해야 하는 사람에 따라 다릅니다.

내보낸 데이터는 복사한 데이터, CSV 또는 PDF 형식일 수 있습니다. 파일에 시각화를 포함하려는 경우 일반적으로 PDF가 선호됩니다. 단순히 일반 텍스트 데이터를 원하는 경우 CSV 및 복사한 데이터가 선호됩니다.

## 프로젝트를 CSV 또는 PDF로 다운로드 {#download-project}

프로젝트를 다운로드할 때는 다음 사항을 고려하십시오.

* 프로젝트를 CSV 또는 PDF으로 다운로드할 때 프로젝트 다운로드를 요청할 때 프로젝트를 저장하거나 저장 취소할 수 있습니다. 그러나 저장된 프로젝트만 [예약](/help/analyze/analysis-workspace/curate-share/t-schedule-report.md)할 수 있습니다.

* 프로젝트를 PDF으로 다운로드할 때:
   * PDF 형식으로 렌더링하기 전에 프로젝트가 Adobe 서버에서 다시 실행되므로 다운로드를 내보내는 데 몇 분이 걸릴 수 있습니다. 브라우저에서 PDF를 다운로드할 때까지 프로젝트를 종료하지 않는 것이 좋습니다. 하지만 기다리는 동안 프로젝트를 계속 변경할 수 있습니다. 5분 이상 소요되는 경우 PDF를 렌더링하는 대신에 이메일로 보내라는 메시지가 표시됩니다.
   * 다운로드는 페이지 매김이 적용되지 않은 단일 페이지로 렌더링됩니다.
   * PDF 렌더링에는 Workspace의 페이지에 있는 내용이 포함됩니다. 프로젝트에 사용자 정의 크기의 시각화 및 패널이 있는 경우, 잘린 콘텐츠가 생기지 않게 시각화 및 패널의 크기가 자동으로 지정(오른쪽 상단의 버튼)되도록 변경해야 합니다.
   * 자유 형식 테이블 내에 있는 [하이퍼링크](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table-hyperlinks.md)는 다운로드한 PDF에서 작동하지 않습니다.

프로젝트를 CSV 또는 PDF 파일로 다운로드하려면 다음 작업을 수행하십시오.

1. 프로젝트를 다운로드하려는 포맷에 따라 다음 중 하나를 수행하십시오.

   * **PDF:** **[!UICONTROL 프로젝트]** > **[!UICONTROL PDF 다운로드]**&#x200B;를 선택합니다.

     다운로드한 파일에 프로젝트에 표시된(표시되는) 테이블과 시각화가 모두 포함되도록 하려면 이 옵션을 선택합니다.

   * **CSV:** **[!UICONTROL 프로젝트]** > **[!UICONTROL CSV 다운로드]**&#x200B;를 선택합니다.

     일반 텍스트 데이터를 원하는 경우 이 옵션을 선택합니다.

   ![](assets/download-project.png)

1. (조건부) PDF 다운로드를 선택한 경우 프로젝트를 다운로드할 준비가 되면 메시지가 표시됩니다. [!UICONTROL **다운로드**]&#x200B;를 클릭합니다.
1. **[!UICONTROL 이 파일 다운로드]** 아이콘을 클릭하고 원하는 폴더에 파일을 저장합니다.

## 클립보드에 데이터 복사(핫키: Ctrl + C) {#copy-data}

마우스 오른쪽 버튼 클릭 옵션 **[!UICONTROL 클립보드에 복사]**&#x200B;를 사용하면 작업 영역에서 데이터를 빠르게 복사하여 서드파티 도구에 붙여넣을 수 있습니다.

* 표시된 테이블을 복사하려면 테이블 헤더를 마우스 오른쪽 버튼으로 클릭하고 **클립보드에 데이터 복사**&#x200B;를 선택합니다.
* 데이터의 일부를 복사하려면 테이블에서 선택한 다음 > **클립보드에 데이터 복사**&#x200B;를 마우스 오른쪽 버튼으로 클릭합니다.

>[!TIP]
>
>`Ctrl+C` 단축키를 사용하여 선택 항목을 클립보드에 복사한 다음 `Ctrl+V`를 사용하여 서드파티 도구에 붙여넣을 수 있습니다.

![](assets/copy-selection.png)

## 데이터를 CSV로 다운로드 {#download-data}

마우스 오른쪽 버튼 클릭 옵션 **[!UICONTROL CSV로 데이터 다운로드]**&#x200B;를 사용하면 데이터 테이블 또는 시각화의 데이터 소스를 CSV로 다운로드할 수 있습니다.

* 테이블 또는 시각화의 헤더에서 마우스 오른쪽 버튼을 클릭하고 **[!UICONTROL CSV로 데이터 다운로드]**&#x200B;를 선택합니다. 이렇게 하면 테이블에 표시된 데이터 또는 시각화를 위한 기본 데이터 소스가 CSV로 다운로드됩니다.

  >[!NOTE]
  >
  >  참고: 맵 시각화는 이 옵션을 지원하지 않습니다.

* 테이블 내에서 마우스 오른쪽 버튼을 클릭하고 **[!UICONTROL 선택 항목을 CSV로 다운로드]**&#x200B;를 선택합니다. 전체 표시된 테이블과는 대조적으로 이 옵션을 사용하면 선택 항목만 다운로드됩니다.

![](assets/download-data-viz.png)

## CSV로 항목 다운로드 {#download-items}

테이블에 있는 400개 이상의 데이터 행을 분석하려면 테이블 헤더 또는 행을 마우스 오른쪽 버튼으로 클릭하고 **CSV로 항목 다운로드(_차원 이름_)**&#x200B;를 선택합니다. 이 옵션은 필터와 세그먼트가 적용된 상태에서 선택한 차원에 대해 최대 50,000개의 차원 항목(테이블 정렬 기준)을 내보냅니다. 테이블의 상단에서 이 옵션을 선택한 경우 테이블의 첫 번째 차원이 내보내집니다. 자유 형식 테이블에는 제한이 적용되지 않지만 최적의 성능을 보장하려면 열이 20개 미만인 테이블에서 항목 다운로드 옵션을 사용하는 것이 좋습니다.

>[!TIP]
>
> 차원이 50,000개 항목을 초과하는 경우 다른 정렬 지표가 적용된 파일을 다운로드하거나 필터를 적용합니다. 예를 들어 한 번의 다운로드에서 방문 횟수를 기준으로 내림차순으로 정렬한 다음 두 번째 다운로드에서 방문 횟수를 기준으로 오름차순으로 정렬합니다. 이 팁은 롱테일 항목을 검색하는 데 도움이 될 수 있습니다.

프로젝트 내에서 멀티태스킹을 할 수 있으며 다운로드가 진행되는 동안 동일한 탭에서 새 Workspace 프로젝트로 이동할 수도 있습니다. 새 브라우저 탭을 열면 다운로드가 일시 중지됩니다. Workspace를 완전히 종료하거나 브라우저 탭을 닫으면 다운로드가 취소됩니다.

![](assets/download-items.png)

### 다운로드한 항목 파일

다음과 같이 테이블의 기능이 다운로드된 파일에 적용됩니다.

* 모든 패널 세그먼트가 필터로 적용됩니다.
* 표에서 선택한 차원 **위** 분류는 각 열 위에 필터로 적용됩니다.
* 표에서 선택한 차원 **아래** 분류는 제거됩니다.

위의 예에서 페이지 항목은 패널 세그먼트(신규 방문자 고객) 및 위의 구성 요소(마케팅 채널 = 이메일)가 필터로 적용된 상태로 다운로드되고 아래 구성 요소(모바일 디바이스 유형)는 다운로드된 CSV에서 제거됩니다.

![](assets/downloaded-file.png)

### 다운로드 알림

파일이 다운로드되면 진행 상황에 대한 정보 알림이 표시됩니다. 언제든지 **[!UICONTROL 다운로드 취소]**&#x200B;를 클릭하여 다운로드를 취소할 수 있습니다. 알림을 닫아도 다운로드가 취소되지&#x200B;**않습니다**.

파일이 완료되면 완료 알림이 표시되고 파일이 브라우저에 다운로드됩니다.

한 번에 두 개 이상의 다운로드를 요청하면 이전 다운로드가 완료될 때까지 각 추가 다운로드가 대기열에 있음을 알리는 알림을 받게 됩니다.

![](assets/toast.png)

## FAQ {#faq}

| 질문 | 답변 |
| --- | --- |
| 다운로드한 PDF가 한 페이지인 이유는 무엇입니까? | 현재 Workspace는 다운로드한 PDF에 페이지를 매기지 않습니다. |
| “CSV로 항목 다운로드” 옵션을 사용하여 50,000개 이상의 항목을 내보낼 수 있습니까? | 각 다운로드에는 최대 50,000개의 차원 항목이 포함될 수 있지만 표의 정렬을 변경하여 롱테일 항목을 검색하거나 필터를 적용하여 더 많은 특정 항목을 다운로드할 수 있습니다. |
| **[!UICONTROL 시각화 복사]**&#x200B;의 기능은 무엇입니까? | [!UICONTROL **클립보드에 데이터 복사**] 또는 [!UICONTROL **선택 항목을 클립보드로 복사**]&#x200B;와 달리 **[!UICONTROL 시각화 복사]** 마우스 오른쪽 버튼 클릭 옵션은 내보내기 옵션이 아닙니다. Workspace의 한 위치에서 다른 위치로 시각화 또는 패널을 복사할 수 있습니다. 예를 들어 동일한 프로젝트의 한 패널에서 다른 패널로 또는 한 프로젝트에서 다른 프로젝트로 복사할 수 있습니다. [인트라 링크 비디오](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/visualizations/intra-linking-in-analysis-workspace.html?lang=ko-KR) |
