---
title: Cross-Device Analytics 설정
description: 사전 요구 사항을 충족한 후 장치 간 분석을 설정하는 방법을 알아봅니다.
translation-type: tm+mt
source-git-commit: 5d6ff87bd49140a974fcaaeed714d0f0b7d1e58b

---


# Cross-Device Analytics 설정

> [!NOTE] Cross-Device Analytics documentation is subject to change as the feature is further developed. 정기적으로 업데이트를 확인하십시오.

Once all prerequisites are met, use the following steps to enable Cross-Device Analytics. 이 단계를 수행하려면 제품 프로필 관리 그룹에 속해 있거나 Adobe Analytics에서 관리자 권한이 있어야 합니다.

> [!IMPORTANT] 이러한 단계를 수행하기 전에 모든 사전 요구 사항을 충족해야 합니다. If all prerequisites are not met, the feature is not available or will not work. See [Cross-Device Analytics](cda-home.md) for prerequisites and limitations.

## CDA에 대해 활성화될 장치 간 보고서 세트 선택

조직에서 CDA를 사용하도록 프로비저닝되면 사용할 보고서 세트를 선택합니다. 이 선택 사항은 Adobe 계정 관리자를 통해 전달될 수 있습니다. 그러면 Adobe에서 선택한 보고서 세트를 CDA 처리를 활성화합니다.

## 장치 간 보기를 보려면 장치 간 가상 보고서 세트 만들기

가상 보고서 세트를 만들 수 있는 액세스 권한이 있는 관리자는 다음과 같이 CDA 가상 보고서 세트를 만들 수 있습니다.

1. Experiencecloud.adobe.com [으로](https://experiencecloud.adobe.com) 이동하고 AdobeID 자격 증명을 사용하여 로그인합니다.
2. 맨 위에 있는 9개의 격자 아이콘을 클릭한 다음 분석을 클릭합니다.
3. 맨 위에 있는 구성 요소 위로 마우스를 가져간 다음 가상 보고서 세트를 클릭합니다.
4. 추가를 클릭합니다.
5. 가상 보고서 세트의 이름을 입력하고 CDA 사용 보고서 세트가 선택되었는지 확인합니다.
6. 장치 간 분석을 포함한 여러 가지 옵션을 활성화하는 '보고서 시간 처리 활성화' 확인란을 클릭합니다.
7. '장치 간 사용자 방문 연결' 확인란을 클릭합니다.
8. 계속을 클릭하고 가상 보고서 세트 구성을 완료한 다음 저장을 클릭합니다.

![CDA 확인란](assets/cda-checkbox.png)

## 장치 간 가상 보고서 세트에 대한 추가 및 변경 사항

가상 보고서 세트에서 장치 간 분석이 활성화되면 다음 변경 사항을 참고하십시오.

* A new cross-device icon appears next to the virtual report suite name. This icon is exclusive to cross-device virtual report suites.
* '사람' 및 '고유 장치'라는 레이블이 지정된 새 지표를 사용할 수 있습니다.
* The metric 'Unique Visitors' is not available, as it is replaced with People and Unique Devices.
* 세그먼트를 작성할 때 '방문자' 세그먼트 컨테이너는 '사람' 컨테이너로 대체됩니다.

## The Compression calculated metric

장치 간 분석 기능으로 장치를 연결할 수 있는 기능은 다양한 요인에 따라 다릅니다. 이 기능의 데이터 스티치 기능의 효과는 압축이라는 계산된 지표를 사용하여 측정할 수 있습니다. Factors that contribute to compression include:

* Using the Co-op graph or Private graph: Generally speaking, organizations using the device co-op tend to see better compression rates than organizations using the private graph.
* Log in rate: The more users log in on your site, the more Adobe can identify and stitch visitors across devices. Sites with a low log in rate also have low compression rates.
* Experience Cloud ID coverage: Only visitors with an ECID can be stitched. A lower percentage of visitors to your site using an ECID correlates to lower compression rates.
* Multiple device usage: If visitors to your site don't use multiple devices, you can see lower compression rates.
* 세부기간 보고:일별 압축은 일반적으로 월 또는 연도별로 압축하는 것보다 작습니다. 개인이 여러 디바이스를 사용할 수 있는 가능성은 한 달 전보다 하루 안에 더 작아졌습니다. 분류 차원을 세그먼트화, 필터링 또는 사용할 경우 압축률이 낮아질 수 있습니다.

지정된 기간 동안 조직의 압축을 보려면 다음을 수행하십시오.

1. 맨 위에 있는 작업 영역을 클릭한 다음 '새 프로젝트 만들기'를 클릭합니다.
2. 빈 프로젝트로 시작한 다음 만들기를 클릭합니다.
3. Drag the Unique Devices metric onto the canvas area labeled 'Drop a Metric Here'.
4. 사람 지표를 고유 장치 지표 머리글의 오른쪽에 있는 캔버스로 드래그하여 두 지표를 나란히 놓습니다.
5. Click the '' symbol next to available metrics on the left to open the Calculated Metric builder.`+`
6. Give this calculated metric the following settings:
   * 이름:장치 간 압축
   * Format: Percent
   * Decimal Places: 2
   * 정의: `[Static Number: 1] minus [People] divided by [Unique Devices]`
      > [!TIP] 정의 영역의 오른쪽 위 모서리에서 '추가'를 클릭하여 정적 번호를 추가합니다. 왼쪽의 사용 가능한 지표 목록에서 [사람 및 고유 장치]를 드래그합니다.
7. 저장을 클릭합니다.
8. 새 계산된 지표를 사람 지표 머리글의 오른쪽에 있는 캔버스로 드래그하여 세 가지 지표를 나란히 놓습니다.
9. 선택 사항:작업공간은 기본적으로 일 차원을 로드합니다. 다른 시간 세부기간을 원하는 경우 일 차원 위에 주 또는 월과 같은 대체 날짜 차원을 드래그합니다.
