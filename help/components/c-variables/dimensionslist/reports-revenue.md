---
description: 특정 기간 동안 모든 제품에서 생성된 수입 금액을 측정합니다.
title: '수입 '
topic: Reports
uuid: e5b72798-f5c7-440d-a62d-376bfd115ac8
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8

---


# 수입 

특정 기간 동안 모든 제품에서 생성된 수입 금액을 측정합니다.

매출을 사용하여 일반 성공과 사이트 트렌드를 볼 수 있습니다. 사이트가 특히 성공적인 기간을 가려내고 소스를 찾아 앞으로의 캠페인에 이용하는 데 사용할 수도 있습니다.

## 보고서의 일반 속성 {#section_97FC92DFB07D45A79F40B452F9AEE57B}

* 이 보고서에서 데이터를 잘 수집하려면 몇 가지 요구 사항을 충족해야 합니다. 다음이 같은 이미지 요청에서 발생해야 합니다.

   * A [!UICONTROL purchase] event must fire in the `s.events` variable.

   * 가격 필드에 숫자가 있는 `products` 변수를 정의해야 합니다.
   * 예를 들어, 다음은 매출 보고서에 $35.99를 전달합니다.

      ```js
       s.products="Mens;Shoes;1;35.99"
      ```

      ```js
       s.events="purchase"
      ```

* [!UICONTROL s.products] 변수에 두 개 이상의 제품이 있는 경우는 모든 제품이 매출 보고서에 계산됩니다. 예를 들어, [!DNL s.products="Mens;Socks;1;4.50,Womens;Socks;1;4.50"]은 수입 $9를 보고 기능으로 전달합니다.

   >[!NOTE]
   >
   >단일 제품에서 수량이 증가한 경우는 수입을 곱하지 않습니다. 예를 들어, [!DNL s.products="Womens;Socks;5;4.50"]는 $22.50를 보고 기능에 전달하지 않고 $4.50를 전달합니다. 구현에서 나열된 수량([!DNL s.products="Womens;Socks;5;22.50"])에 대한 총 수입을 전달하도록 구현하십시오.

* [!UICONTROL Revenue] 기간의 총 금액을 가장 가까운 통화 값으로 반올림합니다. 개별 제품이나 히트를 근사 처리하지 않습니다.
* Analytics는 하루의 값을 가장 가까운 정수 통화 값으로 근사 처리하여 일별 합계와 월별 총액 사이의 차이를 최소화합니다. 월별 합계는 근사 처리된 일별 값을 합한 것이 아니고 전체 합계를 가장 가까운 정수 통화 값으로 근사 처리한 것입니다.
* 매출을 가장 가까운 정수 통화로 근사 처리하지 않은 보고서를 생성하려면 [계산된 지표](https://docs.adobe.com/content/help/ko-KR/analytics/components/calculated-metrics/cm-overview.html)를 사용합니다.
* `purchaseID` 변수를 사용하지 않으면 사용자가 페이지를 새로 고칠 때 데이터를 Adobe로 여러 번 보내기 때문에 수입이 부풀려질 수 있습니다.
* 시간별 분류는 보고서 세트의 시간대를 따릅니다.
* 이 보고서에는 라인 항목이 없습니다. 트렌드 형식으로만 볼 수 있습니다.
* 시간, 일, 주, 월, 분기 및 연도 단위를 적용할 수 있습니다. 이러한 단위는 보고 날짜 범위에 적합하게만 사용할 수 있습니다.
* 이 보고서는 조직과 보고서 세트 설정에 따라 다음 보고서로 상세 분류할 수 있습니다.

   * [!UICONTROL Time Spent per Visit] 보고서.
   * [!UICONTROL Pages and Site Sections] 보고서.
   * [!UICONTROL Videos] 보고서.
   * [!UICONTROL Page Depth and Entry Pages] 보고서.
   * 대부분의 [!UICONTROL Traffic Sources]보고서( [!UICONTROL Search Keywords]보고서, [!UICONTROL Search Engines]보고서 포함)를 [!UICONTROL Referring Domains] 참조하십시오.

   * [!UICONTROL Tracking Code] 보고서 및 모든 관련 분류 보고서.
   * [!UICONTROL Products variable] 보고서 및 모든 관련 분류 보고서. 보고서도 [!UICONTROL Categories] 있습니다.

   * 거의 모든 [!UICONTROL Visitor Profile] 보고서( [!UICONTROL GeoSegmentation] 보고서 제외)

   * 기본 하위 관계가 있는 모든 [!UICONTROL Custom Conversion] 변수 보고서.

* 시간별로는 분류할 수 없습니다.

## 제품별 속성 {#section_ED87FFD020634453AABE86B0248BE69B}

* 이 보고서에 액세스하려면 **[!UICONTROL Conversion]** > **[!UICONTROL Purchases]** > **[!UICONTROL Revenue]**.

* [!UICONTROL Traffic Sources] 분류는 에서 찾을 수 [!UICONTROL Finding Methods]있습니다.

* 이 보고서에 액세스하려면 **[!UICONTROL Site Metrics]** > **[!UICONTROL Purchases]** > **[!UICONTROL Revenue]**.

* 이전에 나열된 모든 분류 외에도 [!UICONTROL First and Last Touch Marketing Channel] 분류를 사용할 수 있습니다.

* 이 보고서에 액세스하려면 **[!UICONTROL Site Metrics]** > **[!UICONTROL Purchases]** > **[!UICONTROL Revenue]**.

* In addition to the previously mentioned breakdowns, [!UICONTROL List]variables and the current [!UICONTROL Video] variables can be used.

* 이 보고서는 세그먼트를 활용할 수 있습니다.

* 다른 모든 보고서 및 변수를 기준으로 이 보고서의 각 항목을 분류하여 원하는 단위로 볼 수 있게 제공합니다.
* 모든 [!UICONTROL conversion] 지표와 [!UICONTROL traffic] 지표를 함께 사용할 수 [!UICONTROL Revenue]있습니다. You can use different allocation for all [!UICONTROL conversion] metrics.

* 이 보고서에는 여러 고급 세그먼트를 활용할 수 있습니다.

지정된 위치에서 이 보고서를 사용할 수 없는 경우는 관리자에게 문의하십시오. 조직 고유의 상황에 맞게 기본 이름이나 메뉴 구조를 변경했을 수도 있습니다.
