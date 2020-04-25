---
title: Adobe Analytics에서 보트 제거
description: Adobe Analytics에서 보트를 제거하는 세 가지 방법
translation-type: tm+mt
source-git-commit: e1cbdf87140b915dccbb8f64694797bb903d8ab8

---


# Adobe Analytics에서 보트 제거

Adobe Analytics에는 보고에서 보트 트래픽을 제거하는 여러 가지 옵션이 있습니다.

## 보트 규칙 사용

표준 및 사용자 지정 보트 필터링 방법은 모두 **[!UICONTROL Analytics]** > **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]** > **[!UICONTROL 설정 편집]** > **[!UICONTROL 일반]** > **[!UICONTROL 보트 규칙]**&#x200B;에서 지원됩니다.

| 규칙 유형 | 설명 |
|--- |--- |
| 표준 IAB 보트 규칙 | **[!UICONTROL IAB 보트 필터링 규칙 사용]**&#x200B;을 선택하면 [IAB](https://www.iab.com/)(International Advertising Bureau) International Spiders &amp; Bots List를 사용하여 보트 트래픽을 제거합니다. 대부분의 고객은 최소한 이 옵션을 선택합니다. |
| 사용자 지정 보트 규칙 | 사용자 에이전트, IP 주소 또는 IP 범위를 기반으로 하여 사용자 지정 보트 규칙을 정의하고 추가할 수 있습니다. |

자세한 내용은 [보트 규칙 개요](/help/admin/admin/bot-removal/bot-rules.md)를 참조하십시오.

## Adobe 도구의 조합 사용

또한 보트가 빠르게 변형되기 때문에 Adobe는 적절하게 정기적으로 조합해서 사용하면 이런 데이터 품질의 장애물을 제거하는 데 도움이 되는 몇 가지 강력한 기능도 제공합니다. 그러한 기능에는 Experience Cloud ID 서비스, 세그먼테이션, Data Warehouse, 사용자 특성 및 가상 보고서 세트가 있습니다. 이러한 도구를 활용하는 방법을 간략하게 살펴보겠습니다.

### 1단계: 방문자의 Experience Cloud ID를 새로 선언된 ID에 전달

시작하려면 [사람 핵심 서비스](https://docs.adobe.com/content/help/en/core-services/interface/audiences/audience-library.html)에서 새로 선언된 ID를 만듭니다. 방문자의 Experience Cloud ID를 새로 선언된 ID로 전달합니다. [Adobe Experience Platform Launch](https://docs.adobe.com/content/help/ko-KR/launch/using/implement/solutions/idservice-save.html)를 사용하면 이 작업을 빠르고 신속하게 할 수 있습니다. 선언된 ID에 &quot;ECID&quot;라는 이름을 사용하겠습니다.

![](assets/bot-cust-attr-setup.png)

다음은 데이터 요소를 통해 이 ID를 캡처하는 방법입니다. Experience Cloud OrgID를 데이터 요소에 올바르게 채워야 합니다.

```return Visitor.getInstance("REPLACE_WITH_YOUR_ECORG_ID@AdobeOrg").getExperienceCloudVisitorID();```

이 데이터 요소가 설정되면 [이 지침](https://docs.adobe.com/content/help/ko-KR/launch/using/implement/solutions/idservice-save.html)에 따라 선언된 ID의 데이터 요소를 Launch의 ECID 도구에 전달합니다.

### 2단계: 세그먼테이션을 사용하여 보트 식별

이제 방문자의 ECID가 선언된 ID에 전달되었으므로 [Analysis Workspace의 세그먼테이션](https://docs.adobe.com/content/help/ko-KR/analytics/analyze/analysis-workspace/components/t-freeform-project-segment.html)을 사용하여 보트처럼 행동하는 방문자를 식별할 수 있습니다. 보트는 단일 액세스 방문, 비정상적인 사용자 에이전트, 알 수 없는 장치/브라우저 정보, 레퍼러 없음, 새 방문자 수, 비정상적인 랜딩 페이지 같은 그들의 행동으로 정의됩니다. 작업 공간 드릴다운 및 세그먼테이션의 기능을 사용하여 IAB 필터링 및 보고서 세트 보트 규칙을 회피하는 보트를 식별합니다. 다음은 사용할 수 있는 세그먼트의 스크린샷의 예입니다.

![](assets/bot-filter-seg1.png)

### 3단계: Data Warehouse를 통해 세그먼트에서 모든 [!DNL Experience Cloud IDs] 내보내기

세그먼트를 사용하여 보트를 식별했으므로 다음 단계는 Data Warehouse를 활용하여 이 세그먼트와 연결된 모든 Experience Cloud ID를 추출하는 것입니다. 다음은 [Data Warehouse](https://docs.adobe.com/content/help/ko-KR/analytics/export/data-warehouse/data-warehouse.html) 요청을 설정하는 방법입니다.

![](assets/bot-dwh-3.png)

Experience Cloud 방문자 ID를 차원으로 사용하고 보트 세그먼트를 적용해야 합니다.

### 4단계: 이 목록을 다시 Adobe에 사용자 특성으로 전달

Data Warehouse 보고서가 도착하면 내역 데이터에서 필터링해야 하는 ECID 목록이 제공됩니다. 이러한 ECID를 복사하여 ECID 열과 보트 플래그 열만 있는 빈 .CSV 파일에 붙여넣습니다.

* **ECID**: 이 열 헤더가 위에서 선언한 새 ID에 제공한 이름과 일치하는지 확인합니다.
* **보트 플래그**: 사용자 특성 스키마 차원으로 추가합니다.

이 .CSV 파일을 사용자 특성 가져오기 파일로 사용한 다음 이 [블로그 게시물](https://theblog.adobe.com/link-digital-behavior-customers)에 설명된 대로 보고서 세트를 사용자 특성에 구독합니다.

![](assets/bot-csv-4.png)

### 5단계: 새 사용자 특성을 활용하는 세그먼트 만들기

데이터 세트가 처리되어 Analysis Workspace에 통합되면 새로운 &quot;보트 플래그&quot; 사용자 특성 차원과 [!UICONTROL 제외] 컨테이너를 활용하는 세그먼트를 한 개 더 만듭니다.

![](assets/bot-filter-seg2.png)

### 6단계: 이 세그먼트를 가상 보고서 세트 필터로 사용

마지막으로 이 세그먼트를 활용하는 [가상 보고서 세트](/help/components/vrs/vrs-about.md)를 만들어 식별된 보트를 필터링해야 합니다.

![](assets/bot-vrs.png)

이렇게 새로 세그먼트화된 가상 보고서 세트는 식별된 보트가 완전히 제거되어 데이터 세트가 완전히 깨끗해집니다.

### 7단계: 2~4단계를 정기적으로 반복 수행

정기적으로 예약된 분석을 수행하기 전에 적어도 월별 미리 알림을 설정하여 새 보트를 식별하고 필터링합니다.
