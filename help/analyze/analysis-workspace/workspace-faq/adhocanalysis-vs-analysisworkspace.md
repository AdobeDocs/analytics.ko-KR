---
description: Ad Hoc Analysis 용어와 작업을 Analysis Workspace와 비교합니다.
title: Ad Hoc Analysis와 비교한 Analysis Workspace
uuid: e4b3e40f-2b08-49a0-95f1-384d85c1640d
translation-type: tm+mt
source-git-commit: 5d96a2868bee48e2294ec2fb27e0340a3bcc50ae
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 85%

---


# Ad Hoc Analysis와 비교한 Analysis Workspace

>[!IMPORTANT]
>
>Adobe은 2021년 3월 1일, Ad Hoc Analysis을 종신형으로 전환할 예정이다. [추가 정보](https://adobe.ly/discoverworkspace)

Ad Hoc Analysis 용어와 작업을 Analysis Workspace와 비교합니다.

Analysis Workspace는 여러 가지 Ad Hoc Analysis 기능을 브라우저 워크플로우에 제공합니다. 두 제품의 일부 용어와 기능은 같지만, 분석에 대한 몇 가지 새로운 용어와 접근 방식이 Analysis Workspace에 도입되었습니다.

이 두 제품의 주요 기능과 시스템 요구 사항에 대한 기술 비교는 [여기](https://docs.adobe.com/content/help/ko-KR/analytics/admin/admin-overview/analytics-product-comparison.html)에서 확인하십시오.

## 주요 용어 비교 {#section_6109406B83B043A18E46D38F130B1D2E}

| Ad Hoc Analysis | Analysis Workspace |
|--- |--- |
| 프로젝트 | 작업 공간 또는 프로젝트 |
| 작업 공간 | 패널 |
| 보고서 | 자유 형식 테이블 |
| 차트/그래프 | 시각화 |
| 계층: 프로젝트 > 작업 공간 > 보고서 | 계층: 프로젝트 > 패널 > 테이블 |
| 등급, 트렌드, 합계 보고서 템플릿 | 자유 형식 테이블 시각화 |
| 플로우 템플릿 | 플로우 시각화 |
| 폴아웃 | 폴아웃 시각화 |

## 주요 작업 비교 {#section_F31446F1DFA742D794A30D713E223440}

<table id="table_90D4461F04F34D70844C5E3FBB0BBE44"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Ad Hoc Analysis 작업 </th> 
   <th colname="col2" class="entry"> Analysis Workspace 작업 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>지표 열에 차원 및 세그먼트 추가 </p> </td> 
   <td colname="col2"> <p>차원 항목 또는 세그먼트를 열 헤더로 가져와 지표 비교 보기를 쉽게 만들 수 있습니다. <a href="https://www.youtube.com/watch?v=P9W0hhIHhCs"  > 비디오: 차원 작업</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>세그먼트 적용 </p> </td> 
   <td colname="col2"> <p>세그먼트는 세그먼트 구성 요소 메뉴에서 사용할 수 있으며, Analysis Workspace의 다음 세 위치에서 적용할 수 있습니다. </p> 
    <ol id="ol_800D81FE2C84459B94B085C51E140330"> 
     <li id="li_F2E050902F9A4831BBA57F466E07DEAE"><b>패널 수준</b>에서. 패널에서 여러 가지 시각화에 적용합니다. Ad Hoc의 작업 공간에 세그먼트를 적용하는 것과 비슷합니다. </li> 
     <li id="li_2D88E43E0161485C95B08DC3C593EFD9"><b>테이블의 행</b>으로. Ad Hoc의 테이블 빌더 '행/분류' 섹션에 세그먼트를 추가하는 것과 비슷합니다. </li> 
     <li id="li_102E1A1DAA9247C08FC46C5AB3D78113"><b>테이블의 열</b>로. Ad Hoc Analysis의 테이블 빌더 '열' 섹션에 세그먼트를 추가하거나 Ad Hoc Analysis의 보고서 수준에서 세그먼트를 적용하는 것과 비슷합니다. </li> 
    </ol> <p><a href="https://www.youtube.com/watch?v=QlUCdQDnni4"  > 비디오: 작업 공간에서 세그먼트 사용</a> </p> <p><a href="https://www.youtube.com/watch?v=YjaRlJoQqRA"  > 비디오: 패널에 세그먼트 적용</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>임시("임시") 세그먼트 만들기 </p> </td> 
   <td colname="col2"> <p>You can <a href="/help/analyze/analysis-workspace/components/t-freeform-project-segment.md"  > create instant, temporary ("ad-hoc") segments</a> in Analysis Workspace by dragging dimension items into the segment drop zone at the top of the panel. 또한 패널 드롭 영역에 드롭다운 필터를 추가하여 여러 개의 임시 세그먼트를 한 번에 만들 수 있으므로 제어된 프로젝트 상호 작용을 구현할 수 있습니다. </p> <p><a href="https://www.youtube.com/watch?v=NKm7Rj23TtE"  > 비디오: Analysis Workspace의 Ad Hoc 세그먼트</a> </p> <p><a href="https://www.youtube.com/watch?v=vpJywtsFVPI"  > 비디오:Analysis Workspace의 드롭다운 필터</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>날짜 범위 및 세부기간 선택 </p> </td> 
   <td colname="col2"> <p>날짜 범위 및 세부기간은 시간 구성 요소 메뉴에서 사용할 수 있으며, 다음 세 가지 방법으로 사용할 수 있습니다. </p> 
    <ol id="ol_8B57C8A840694A879B22B809C58E7482"> 
     <li id="li_58FAE6A87B494A5C9007CD35BB101608">날짜 범위는 열/행에 적용할 수 있고 선택한 패널 날짜 범위를 재정의합니다. 보고서 수준 날짜 범위와 비슷합니다. </li> 
     <li id="li_85BB89EFF9C8466A992815BB7804EA37">'적용'은 패널 내에 있는 모든 시각화에 날짜 범위를 적용합니다. Ad Hoc Analysis의 작업 공간 날짜 범위와 비슷합니다. </li> 
     <li id="li_BC18564A8FBB48F4A522BCAC60838759">'모든 패널에 적용'은 작업 공간 프로젝트 내에 있는 모든 패널에 날짜 범위를 적용합니다. Ad Hoc Analysis의 프로젝트 날짜 범위와 비슷합니다. </li> 
    </ol> <p><a href="https://www.youtube.com/watch?v=ybmv6EBmhn0"  > 비디오: Analysis Workspace에서 날짜 작업</a> </p> <p><a href="https://www.youtube.com/watch?v=L4FSrxr3SDA"  > 비디오: 날짜 범위 사용자 지정</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>폴아웃 및 전환 단계 유도 사용 </p> </td> 
   <td colname="col2"> <p><a href="/help/analyze/analysis-workspace/visualizations/fallout/fallout-flow.md"  > 폴아웃 시각화</a>는 시각화 구성 요소 메뉴 아래에 있는 Analysis Workspace에서 사용할 수 있습니다. Ad Hoc Analysis과 비슷합니다. </p> 
    <ol id="ol_625FF45AED4E403DBEE1A906282E8531"> 
     <li id="li_7B6C5F2682774641B82D2021786AE5C4">폴아웃은 방문 또는 방문자를 확장할 수 있고 "모든 방문"을 선택적으로 포함할 수 있습니다. 폴아웃은 마우스 오른쪽 단추 클릭 메뉴를 통해 빠르게 추적할 수 있습니다. </li> 
     <li id="li_CFBDDAB8E96A445DB0624640AEB25994">차원 항목은 OR 연산자(그룹과 비슷함)로 연결할 수 있고 이벤트는 단계에서 사용할 수 있습니다. </li> 
     <li id="li_6638E6A62C744A27B2C066E5F9EC62C0">폴스루 및 폴아웃 다음 단계는 마우스 오른쪽 단추 클릭 메뉴를 통해 렌더링될 수도 있습니다. </li> 
    </ol> <p>또한 Analysis Workspace의 폴아웃은 <a href="/help/analyze/analysis-workspace/visualizations/fallout/configuring-interdimensional-fallout.md"  >혼합 차원</a>을 단계 내에서 사용할 수 있습니다. Ad Hoc Analysis보다 개선된 기능입니다. 단계 내에 있는 혼합 차원은 AND 연산자로 처리됩니다. </p> <p><a href="https://www.youtube.com/watch?v=VcrfHSyIoj8"  > 비디오: 폴아웃 및 단계</a> </p> <p><a href="https://www.youtube.com/watch?v=EeLV366pQag"  > 비디오: 여러 폴아웃 차원 사용</a> </p> <p><a href="https://www.youtube.com/watch?v=H-oT3QZlyZQ"  > 비디오: 폴아웃의 세그먼트 비교</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>흐름 검사(경로 지정) </p> </td> 
   <td colname="col2"> <p><a href="/help/analyze/analysis-workspace/visualizations/c-flow/flow.md"  > 폴아웃 시각화</a>는 시각화 구성 요소 메뉴 아래에 있는 Analysis Workspace에서 사용할 수 있습니다. Ad Hoc Analysis과 비슷합니다. </p> 
    <ul id="ul_42D259310823496499F7D1474E1639AF"> 
     <li id="li_5DE6980EF66A49E58B8946A0422BC02C">플로우는 방문 또는 방문자를 확장할 수 있습니다. </li> 
     <li id="li_70A692266D32416BA3D70C1F8999F837">키 통계가 % 경로 보기 측면에서 표시됩니다. </li> 
    </ul> <p>또한 플로우는 Ad Hoc Analysis에 대한 개선 사항인 <a href="/help/analyze/analysis-workspace/visualizations/c-flow/multi-dimensional-flow.md"  > 혼합 차원</a>과 마우스 오른쪽 단추로 클릭하여 세그먼트를 생성할 수 있는 기능을 사용할 수 있습니다. Ad Hoc Analysis보다 개선된 기능입니다. </p> <p>현재 Analysis Workspace의 흐름에서는 사용자가 성공 이벤트를 선택할 수 <b>없습니다</b> . </li> 
    </ul> <p><a href="https://www.youtube.com/watch?v=3R1HTM7y_RM"  > 비디오: 플로우 시각화 개요</a> </p> <p><a href="https://www.youtube.com/watch?v=m1Wa6inC1rQ"  > 비디오: 다차원 플로우</a> </p> <p><a href="https://www.youtube.com/watch?v=XrJoNQy6RaQ"  > 비디오: 플로우에서 세그먼트 만들기</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>무한 분류 수행 </p> </td> 
   <td colname="col2"> <p>Analysis Workspace를 사용하여 브라우저 내에서 무한 수준으로 드릴다운할 수 있습니다. 세그먼트와 차원을 혼합할 수 없습니다. 여러 차원 항목은 여러 번 선택하고 분류 차원으로 드래그하여 한 번에 분석할 수 있습니다. </p> <p><a href="https://www.youtube.com/watch?v=3mQ2HN7-lIc"  > 비디오: 향상된 분류</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>데이터 트렌드 빨리 표시 </p> </td> 
   <td colname="col2"> <p>보고서 행 내에 있는 그래프 아이콘을 클릭하여 데이터를 빠르게 시각화할 수 있습니다. 또한 이러한 빠른 시각화는 소스 테이블에 연결되므로 테이블에서 옆의 값 하나를 클릭하여 그래프가 자동으로 업데이트되는 것을 볼 수 있습니다. </p> <p><a href="https://www.youtube.com/watch?v=kzlPjsBVYFQ"  > 비디오: 차원-그래프 라이브 연결</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>보고서 세트 선택 </p> </td> 
   <td colname="col2"> <p>여러 보고서 세트를 Analysis Workspace의 단일 프로젝트에 추가할 수 있습니다.  </p> <p><a href="https://www.youtube.com/watch?v=kRPTBDNLJKk"  > 비디오:작업 공간의 여러 보고서 세트</a> </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>속성 IQ </p> </td> 
   <td colname="col2"> <p>Analysis Workspace의 <a href="/help/analyze/analysis-workspace/attribution/overview.md"  >속성 IQ</a>에서는 자유 형식 테이블, 시각화 및 계산된 지표에 다양한 새로운 속성 모델 유형을 추가할 수 있습니다. 10개 이상의 규칙 기반 및 알고리즘 모델이 포함되어 있습니다. </p>  <p><a href="https://www.youtube.com/watch?v=aYbGcQvAN1E"  > 비디오:자유 형식 테이블의 Attribution IQ</a> </p> </td> 
  </tr>  
 </tbody> 
</table>

