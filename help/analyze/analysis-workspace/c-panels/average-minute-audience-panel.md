---
title: 미디어 평균 시간(분) 대상 패널
description: Analysis Workspace에서 미디어 평균 시간(분) 대상 패널을 사용하고 해석하는 방법
feature: Panels
role: User, Admin
source-git-commit: 3cb991e7f440a72247b7261ad5959e15619e8a76
workflow-type: tm+mt
source-wordcount: '1313'
ht-degree: 10%

---

# 미디어 평균 시간(분) 대상 패널

Media Analytics 고객은 평균 시간(분) 대상 패널을 사용하여 컨텐츠의 평균 소비를 더 잘 이해할 수 있습니다. 대상 평균 시간(분)은 길이나 장르의 프로그래밍을 비교할 수 있도록 해줍니다. 또한 고객은 이 디지털 평균 시간(분) 대상을 선형 TV 평균 시간(분) 지표에 비교하거나 추가할 수 있습니다. 이 패널에서는 사실 후에 기간 분류가 업데이트된 시점과 사용자 지정 기간 동안의 평균 대상을 측정할 수 있는 유연성을 제공합니다. 현재 평균 대상 시간(분) 지표는 처리 시간에 기간을 사용할 수 있는 경우에만 작동합니다.

Analysis Workspace에서 평균 시간(분) 대상은 미디어 스트림을 시청하는 데 걸린 시간을 컨텐츠 지속 시간 또는 기간 및 선택한 세부 기간의 총 선택 기간으로 나눈 시간입니다.

미디어 평균 시간(분) 대상 패널은 분류를 사용하여 지속 시간이 사용 가능한 경우 선택한 특정 컨텐츠별로 평균 시간(분) 대상 분석을 제공합니다.
대상 평균 시간(분) 패널은 선택한 기간 동안 분류를 사용하여 지속 시간을 사용할 수 있는지 여부에 관계없이 특정 콘텐츠로 필터링할 수 있는 분석을 제공합니다. 미디어 평균 시간(분) 대상 패널에 액세스하려면 Media Analytics 구성 요소가 활성화된 보고서 세트로 이동합니다. 그런 다음 맨 왼쪽에 있는 패널 아이콘을 클릭하고 패널을 Analysis Workspace 프로젝트로 끌어옵니다.

<!-- For more information, see the Media Average Minute Audience introduction video:
<< replace with AMA video when available >> -->

<!-- >[!VIDEO](https://video.tv.adobe.com/v/330177/?quality=12) -->

## 패널 입력 {#Input}

다음 입력 설정을 사용하여 미디어 평균 시간(분) 대상 패널을 구성할 수 있습니다.

| 설정 | 설명 |
|---------|------------|
| 패널 날짜 범위 | 패널 날짜 범위 기본값은 오늘입니다. 단 하루 또는 여러 달이 보이도록 편집할 수 있습니다. <br></br> 이 시각화는 1440개의 데이터 행으로 제한됩니다(예: 분 단위 세부 기간에서 24시간). 날짜 범위와 세부 기간 조합의 결과 행이 1440개를 초과하는 경우 전체 날짜 범위를 수용하도록 세부 기간이 자동으로 업데이트됩니다. |
| 여기(또는 기타 구성 요소)로 세그먼트를 드래그합니다. | 다른 패널과 마찬가지로 이 설정은 작성한 세그먼트에 따라 선택 사항을 필터링합니다. 특정 플랫폼, 라이브 스트림 또는 기타 일반적인 미디어 세그먼트를 보는 좋은 방법입니다. |
| 다음에 대한 지표 계산 | 이 설정을 사용하면 을 선택하여 특정 콘텐츠에 대한 평균 시간(분) 대상을 표시할지 여부를 선택할 수 있습니다 *특정 콘텐츠*&#x200B;또는 을 선택하여 특정 기간 동안의 대상 평균 시간(분) 분을 보려면 *사용자 지정 기간*. <br></br>특정 콘텐츠는 분류를 사용하여 기간이 업데이트된 경우에만 작동합니다. 지속 시간을 사용할 수 없거나, 특정 지속 시간(예: 라이브 스트림이나 이벤트 동안)이 없는 컨텐츠나 컨텐츠가 여러 개인 시계열 평균 분 대상을 보려면 사용자 지정 기간을 선택해야 합니다. 이 설정은 워크플로우 및 보고서 출력을 변경합니다. |

### 특정 콘텐츠

| 설정 | 설명 |
|---------|------------|
| 보고 차원 | 특정 컨텐츠를 선택할 때 보고서 출력을 선택하여 비디오 이름 또는 컨텐츠 ID 필드를 사용하여 선택한 기간 동안의 컨텐츠 및 연관된 평균 시간 대상 을 표시할 수 있습니다. |
| 콘텐츠 필터링 기준 (선택 사항) | 원하는 보기 또는 데이터 구성 방식에 따라 특정 콘텐츠를 필터링할 수 있습니다. |
| 쇼, 시즌, 에피소드 | &quot;표시, 시즌, 에피소드&quot;를 선택하면 드롭다운에 사용 가능한 표시가 표시됩니다. 이 프로그램은 검색을 사용하여 필터링하거나 왼쪽 열에서 표시 이름을 드래그하여 놓을 수 있습니다. 선택 사항을 종료하여 쇼의 모든 시즌을 보거나 개별 시즌별로 필터링한 다음 개별 에피소드별로 필터링할 수 있습니다. 이 설정은 선택한 기간 동안의 해당 프로그램, 시즌 또는 에피소드에 대한 데이터를 표시합니다. |
| 사용자 정의 차원 | 표시 이름이 사용자 지정 차원 아래에 있는 경우 차원(선택 사항) 드롭다운에서 검색하거나 왼쪽 열 검색을 사용하여 찾을 수 있습니다. 차원 항목은 해당 선택을 기반으로 자동으로 채워지고 에피소드로 처리됩니다. |
| 없음 | 선택할 수 있습니다 *없음* 선택한 항목에 대한 대상 평균 시간(분) 데이터가 있는 모든 비디오 이름을 표시하기 위해 |

### 특정 컨텐츠 고급 설정

| 설정 | 설명 |
|---------|------------|
| 테이블 설정 | 기본 설정은 테이블의 계산 값을 표시하여 평균 분 대상의 분자와 분모를 테이블의 이전 열로 표시합니다. 이 옵션을 선택 해제하면 해당 두 열이 제거되어 비디오 이름 또는 컨텐츠 ID 옆에 있는 평균 시간(분)만 남습니다. |
| 체류 시간 지표 | 컨텐츠 시간만 포함하는 기본 컨텐츠 체류 시간을 선택하거나, 컨텐츠 및 광고 시간을 포함하여 평균 분 대상 분자 계산으로 포함하는 미디어 체류 시간을 사용하도록 선택할 수 있습니다. |

### 사용자 정의 기간

| 설정 | 설명 |
|---------|------------|
| 세부 기간 | 기본 세부기간은 5분이지만 달력 선택에서 수행된 전체 기간 선택 내에서 시계열의 분모로 사용되는 세부기간을 선택할 수 있습니다. 예를 들어, 5분 세부기간을 사용하여 오후 12:00부터 오후 12:30까지 선택하면 전체 30분 동안 평균 분 대상 및 5분 기간 동안 평균 분 대상(분)이 있는 6개의 행이 반환됩니다. 이러한 행은 시계열 차트의 데이터 포인트로 사용됩니다. |
| 콘텐츠 필터링 기준 (선택 사항) | 원하는 보기 또는 데이터 구성 방식에 따라 특정 콘텐츠를 필터링할 수 있습니다. |
| 쇼, 시즌, 에피소드 | 선택 *보기, 시즌, 에피소드* 검색을 통해 필터링하거나 왼쪽 열에서 표시 이름을 드래그하여 놓을 수 있는 드롭다운에 사용 가능한 표시를 표시합니다. 선택 사항을 종료하여 쇼의 모든 시즌을 보거나 개별 시즌별로 필터링한 다음 개별 에피소드별로 필터링할 수 있습니다. 이 설정은 선택한 기간 동안의 해당 프로그램, 시즌 또는 에피소드에 대한 데이터를 표시합니다. |
| 사용자 정의 차원 | 표시 이름이 사용자 지정 차원 아래에 있는 경우 차원(선택 사항) 드롭다운에서 검색하거나 왼쪽 열 검색을 사용하여 찾을 수 있습니다. 차원 항목은 해당 선택을 기반으로 자동으로 채워지고 에피소드로 처리됩니다. |
| 없음 | 선택할 수 있습니다 *없음* 선택한 기간 동안의 모든 비디오 이름을 표시하도록 했습니다. |

### 사용자 지정 기간 고급 설정

| 설정 | 설명 |
|---------|------------|
| 테이블 설정 | 기본 설정은 테이블에서 평균 분 대상의 분자와 분모를 이전 열로 표시하는 계산 값을 표시합니다. 이 옵션을 선택 해제하면 기간 옆에 있는 평균 시간(분) 대상만 남은 두 열이 제거됩니다. |


## 특정 컨텐츠 패널 출력

미디어 평균 시간(분) 대상 패널은 다음을 반환합니다.

* 전체 선택에 대한 총 평균 시간(분) 대상
* 표에 표시된 개별 비디오의 대상 필터 및 평균 시간(분)
* 고급 설정을 선택한 경우 컨텐츠 체류 시간 및 비디오 길이(기간)가 선택됩니다

언제든지 패널을 편집하고 다시 빌드하려면 오른쪽 상단의 연필 편집을 클릭합니다.

![기본 보기](assets/specific-content-panel-output.png)


### 특정 컨텐츠 데이터 소스

이 패널에서 사용할 수 있는 유일한 지표는 대상 평균 분수입니다.

| 지표 | 설명 |
|--------|-------------|
| Average Minute Audience | 미디어 스트림을 시청하는 데 걸린 시간은 분류를 통해 제공된 비디오 길이(기간)로 나눠집니다. |

## 사용자 지정 기간 패널 출력 {#custom-time-period-output}

미디어 평균 시간(분) 대상 패널은 전체 선택에 대한 총 평균 대상(분), 최대 및 최소 대상(분) 및 전체 선택 항목에서 평균 시간(분) 대상(분)을 나타내는 선 시리즈 그래프를 반환합니다. 아래 표는 세부기간에 대한 필터 및 평균 분 대상자와 고급 설정을 선택한 경우 각 기간의 콘텐츠 체류 시간 및 세부기간을 보여줍니다.

언제든지 패널을 편집하고 다시 빌드하려면 오른쪽 상단의 연필 편집을 클릭합니다.

![동시 뷰어 출력](assets/custom-time-period-panel-output.png)

### 사용자 지정 기간 데이터 소스

이 패널에서 사용할 수 있는 유일한 지표는 대상 평균 시간(분) 뿐입니다.

| 지표 | 설명 |
|---|---|
| 대상 평균 시간(분) | 미디어 스트림을 시청하는 데 걸린 시간(총 선택 시간 또는 선택한 세부기간(분)으로 나눈 시간. |



<!-- For more information about Media Average Minute Audience, visit [MA doc page]( https://url). -->