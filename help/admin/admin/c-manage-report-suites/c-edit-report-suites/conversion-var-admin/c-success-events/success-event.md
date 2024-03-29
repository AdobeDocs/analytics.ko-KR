---
description: 성공 이벤트는 추적할 수 있는 작업입니다. 성공 이벤트가 무엇인지 결정합니다. 예를 들어 방문자가 품목을 구매하면 구매 이벤트를 성공 이벤트로 간주할 수 있습니다.
keywords: 이벤트
title: 성공 이벤트 개요
feature: Event
role: Admin
exl-id: d52a691a-8124-4601-932f-d6d2d0a7842b
source-git-commit: 429aaa43fdae669350bdb5a5a54a7d4b9b1c65f2
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 100%

---

# 성공 이벤트 개요

성공 이벤트(전환 이벤트 또는 사용자 지정 이벤트라고도 함)는 추적할 수 있는 작업입니다. 성공 이벤트가 무엇인지 결정합니다. 예를 들어 방문자가 품목을 구매하면 구매 이벤트를 성공 이벤트로 간주할 수 있습니다.

다음은 비디오 개요입니다.

>[!VIDEO](https://video.tv.adobe.com/v/28764/?quality=12)

보고서 세트 설정의 성공 이벤트 페이지에 액세스합니다.

1. AdobeID 자격 증명을 사용하여 [experiencecloud.adobe.com](https://experiencecloud.adobe.com)에 로그인합니다.
2. 맨 위에 있는 9격자 버튼을 클릭한 다음 [!UICONTROL Analytics]를 클릭합니다.
3. [!UICONTROL 관리] > [!UICONTROL 보고서 세트]로 이동합니다
4. 원하는 보고서 세트를 선택한 다음 [!UICONTROL 설정 편집] > [!UICONTROL 전환] > [!UICONTROL 성공 이벤트]로 이동합니다.

웹 사이트 유형에 따라 다양한 성공 이벤트가 있습니다. 여기에는 다음과 같은 예가 포함됩니다.

* **소매**: 제품 보기, 체크아웃, 구매
* **미디어**: 구독, 콘테스트 등록, 페이지 보기, 비디오 보기
* **금융**: 신청서 제출, 로그인, 셀프서비스 도구 사용
* **여행**: 예약(구매), 내부 캠페인(클릭스루), 검색(가격 명세서)
* **무선 통신**: 구매, 리드, 셀프서비스 도구 사용
* **첨단 기술**: 백서 다운로드, RFP, 양식 완성, 지원 요청
* **자동차**: 리드 제출, 견적 요청, 브로슈어 다운로드

[s.events](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/events/event-serialization.html?lang=ko-KR) 변수는 성공 이벤트를 정의합니다.

## 성공 이벤트 페이지 - 설명 {#section_681ECEC981694CABBDBF00E18165B447}

**[!UICONTROL Analytics]** > **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]** > **[!UICONTROL 설정 편집]** > **[!UICONTROL 전환]** > **[!UICONTROL 성공 이벤트]**

성공 이벤트 페이지를 사용하여 사이트에서 사용되는 이벤트 변수를 구성할 수 있습니다. 최대 1,000개의 성공 이벤트를 추가할 수 있습니다. H22 이상의 코드에 있는 경우 이벤트 81-1,000만 작동합니다.

| 요소 | 설명 |
|--- |--- |
| Event | 이벤트의 원래 이름. |
| 이름 | 사이트에 사용되는 성공 이벤트에 의미 있는 이름을 부여합니다. 예를 들어 event1이 등록을 추적하는 데 사용되는 경우 event1이 모든 전환 보고서에서 &quot;등록&quot; 지표로 나타나도록 여기에서 이름을 변경합니다. |
| 유형 | 선택된 유형은 이벤트가 카운터(표준), 숫자 또는 통화 이벤트인지 여부를 결정합니다. 숫자 및 통화 이벤트를 사용하여 두 개 이상씩 지표를 증가시킬 수 있습니다.  카운터 이벤트는 이벤트를 시간에 맞춰 기록하는 데 사용되며, 반면에 통화 이벤트는 세금이나 배송과 같은 십진수를 기록합니다. 통화 이벤트로 전달된 값은 받는 즉시 페이지 통화에서 보고서 세트의 기본 통화로 전환됩니다. 통화 이벤트 사용에 대한 자세한 내용은 Adobe 담당자에게 문의하십시오. 숫자 이벤트는 주문에 사용된 쿠폰 수와 같이 통화가 아닌 숫자를 보고하는 데 사용됩니다. 통화 이벤트는 세금과 운송료를 추적하는 데 사용됩니다. 데이터 소스의 표준 유형에 사용되는 이벤트는 숫자 또는 통화 이벤트여야 합니다. |
| 극성 | 지표 극성을 사용하면 지정된 사용자 지정 이벤트(지표)가 상승할 경우 Adobe Analytics에서 이를 좋은 것으로 볼지 나쁜 것으로 볼지 여부를 나타낼 수 있습니다. 이 설정을 사용하면 Adobe Analytics에서 컨텍스트(예: 이전 주 대비)를 추가하기 위해 다양한 지표에 대한 방향 표시기(화살표)를 표시할 수 있습니다.  예: &quot;제출된 버그&quot;가 전주 대비로 증가하는 경우, Adobe Analytics에서 이를 좋은 것으로 봐야 합니까, 나쁜 것으로 봐야 합니까? 이메일 등록 증가는 아마도 좋은 것으로 봐야 할 것입니다. 반면에 양식 제출 오류 증가는 나쁜 것으로 봐야 할 것입니다.  Analysis Workspace에서 극성이 자유 형식 테이블 조건부 서식, 요약 변경 사항 시각화 및 맵 시각화의 양/음 색상 구성표에 적용됩니다. |
| 설명 | 이벤트의 목적 및 용도에 대한 간단한 설명입니다. |
| 고유 이벤트 기록 | **방문당 한 번 기록**: 해당 이벤트를 방문자의 세션에 연결합니다. 동일한 방문에서 해당 이벤트에 대한 후속 카운트는 무시됩니다. 이러한 유형의 이벤트 직렬화에는 구현 변경이 필요하지 않습니다.<br>**이벤트 ID 사용**: 해당 이벤트를 사용자 지정 ID에 연결합니다. 이벤트 ID가 동일한 해당 이벤트에 대한 후속 카운트는 무시됩니다. 이 유형의 이벤트 직렬화를 사용하려면 값의 중복을 제거하기 위해 히트의 사용자 지정 ID가 필요합니다. 구현 사용 안내서에서 [이벤트 ID 직렬화](/help/implement/vars/page-vars/events/event-serialization.md)를 참조하십시오. |
| 기여도 | 방문의 모든 차원 항목에 전체 속성 크레딧을 제공합니다. |
| 경고(통화 이벤트) | 이벤트 유형을 통화 이벤트에서 다른 이벤트로 변경하거나 다른 이벤트에서 통화 이벤트로 변경하면 보고에 내역 데이터를 사용할 수 없다는 메시지가 표시됩니다.  다른 이벤트 유형에서는 별도의 데이터 테이블을 사용하며, 동시에 사용할 수 없습니다. 사용자가 이벤트 유형을 되돌리면 일부 내역 데이터를 복원할 수 있습니다. 하지만 초기 변경 후 수집된 모든 데이터는 사용할 수 없습니다. 따라서 이벤트 유형을 변경할 때는 주의하십시오. |
