---
description: 특정 기간 동안 모든 제품에서 생성된 수입 금액을 측정합니다.
seo-description: 특정 기간 동안 모든 제품에서 생성된 수입 금액을 측정합니다.
seo-title: 수입
solution: Analytics
title: 수입
topic: 보고서
uuid: E 5 B 72798-F 5 C 7-440 D-A 62 D -376 BFD 115 AC 8
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 매출

특정 기간 동안 모든 제품에서 생성된 수입 금액을 측정합니다.

매출을 사용하여 일반 성공과 사이트 트렌드를 볼 수 있습니다. 사이트가 특히 성공적인 기간을 가려내고 소스를 찾아 앞으로의 캠페인에 이용하는 데 사용할 수도 있습니다.

## 보고서의 일반 속성 {#section_97FC92DFB07D45A79F40B452F9AEE57B}

* 이 보고서에서 데이터를 잘 수집하려면 몇 가지 요구 사항을 충족해야 합니다. 다음이 같은 이미지 요청에서 발생해야 합니다.

   * [!UICONTROL purchase] 이벤트가 `s.events` 변수에 설정된 ID.

   * 가격 필드에 숫자가 있는 `products` 변수를 정의해야 합니다.
   * 예를 들어, 다음은 매출 보고서에 $35.99를 전달합니다.

      ```js
       s.products="Mens;Shoes;1;35.99"
      ```

      ```js
       s.events="purchase"
      ```

* [!UICONTROL s.products] 변수에 두 개 이상의 제품이 있는 경우는 모든 제품이 매출 보고서에 계산됩니다. For example, [!DNL s.products="Mens;Socks;1;4.50,Womens;Socks;1;4.50"] would pass $9 in revenue to reporting.

   >[!NOTE]
   >
   >단일 제품에서 수량이 증가하면 매출이 곱해지지 않습니다. For example, [!DNL s.products="Womens;Socks;5;4.50"] does not pass $22.50 into reporting, it passes $4.50. Make sure your implementation passes the total revenue for the quantity listed ( [!DNL s.products="Womens;Socks;5;22.50"]).

* [!UICONTROL 매출]은 기간에 대한 총액을 가장 가까운 통화 값으로 근사 처리합니다. 개별 제품이나 히트를 근사 처리하지 않습니다.
* Analytics는 하루의 값을 가장 가까운 정수 통화 값으로 근사 처리하여 일별 합계와 월별 총액 사이의 차이를 최소화합니다. 월별 합계는 근사 처리된 일별 값을 합한 것이 아니고 전체 합계를 가장 가까운 정수 통화 값으로 근사 처리한 것입니다.
* 매출을 가장 가까운 정수 통화로 근사 처리하지 않은 보고서를 생성하려면 [계산된 지표](https://marketing.adobe.com/resources/help/en_US/analytics/calcmetrics/)를 사용합니다.
* `purchaseID` 변수를 사용하지 않으면 사용자가 페이지를 새로 고칠 때 데이터를 Adobe로 여러 번 보내기 때문에 수익이 부풀려질 수 있습니다.
* 시간별 분류는 보고서 세트의 시간대를 따릅니다.
* 이 보고서에는 라인 항목이 없습니다. 트렌드 형식으로만 볼 수 있습니다.
* 시간, 일, 주, 월, 분기 및 연도 단위를 적용할 수 있습니다. 이러한 단위는 보고 날짜 범위에 적합하게만 사용할 수 있습니다.
* 이 보고서는 조직과 보고서 세트 설정에 따라 다음 보고서로 상세 분류할 수 있습니다.

   * [!UICONTROL 방문당 체류 시간] 보고서.
   * [!UICONTROL 페이지 및 사이트 섹션] 보고서.
   * [!UICONTROL 비디오] 보고서.
   * [!UICONTROL 페이지 깊이 및 시작 페이지] 보고서.
   * 대부분의 [!UICONTROL 트래픽 소스] 보고서([!UICONTROL 검색 키워드], [!UICONTROL 검색 엔진], 및 [!UICONTROL 참조 도메인] 보고서 포함).

   * [!UICONTROL 추적 코드] 보고서와 모든 관련 분류 보고서.
   * [!UICONTROL 제품 변수] 보고서와 모든 관련 분류 보고서. 그리고 [!UICONTROL 카테고리] 보고서.

   * 거의 모든 [!UICONTROL 방문자 프로필] 보고서([!UICONTROL 지리 특성] 보고서 제외).

   * 모든 [!UICONTROL 사용자 지정 전환] 변수 보고서와 기본 하위 관계.

* 시간별로는 분류할 수 없습니다.

## 제품별 속성 {#section_ED87FFD020634453AABE86B0248BE69B}

* **[!UICONTROL 전환]** &gt; **[!UICONTROL 구매]** &gt; **[!UICONTROL 매출로 이동하여 이 보고서에 액세스할]**&#x200B;수 있습니다.

* [!UICONTROL 트래픽 소스] 분류는 [!UICONTROL 검색 방법]에서 찾을 수 있습니다.

* **[!UICONTROL 사이트 지표]** &gt; **[!UICONTROL 구매]** &gt; **[!UICONTROL 매출로 이동하여 이 보고서에 액세스할]**&#x200B;수 있습니다.

* 이전에 나열된 모든 분류 외에도 [!UICONTROL 첫 번째 및 마지막 터치 마케팅 채널] 분류를 사용할 수 있습니다.

* **[!UICONTROL 사이트 지표]** &gt; **[!UICONTROL 구매]** &gt; **[!UICONTROL 매출로 이동하여 이 보고서에 액세스할]**&#x200B;수도 있습니다.

* 이전에 언급된 분류 외에도 [!UICONTROL 목록] 변수와 현재 ]비디오[!UICONTROL  변수를 사용할 수 있습니다.

* 이 보고서는 세그먼트를 활용할 수 있습니다.

* 다른 모든 보고서 및 변수를 기준으로 이 보고서의 각 항목을 분류하여 원하는 단위로 볼 수 있게 제공합니다.
* 모든 [!UICONTROL 전환] 및 [!UICONTROL 트래픽] 지표를 [!UICONTROL 매출]과 함께 사용할 수 있습니다. 모든 [!UICONTROL 전환] 지표에 대해 다른 할당을 사용할 수 있습니다.

* 이 보고서에는 여러 고급 세그먼트를 활용할 수 있습니다.

지정된 위치에서 이 보고서를 사용할 수 없는 경우는 관리자에게 문의하십시오. 조직 고유의 상황에 맞게 기본 이름이나 메뉴 구조를 변경했을 수도 있습니다.
