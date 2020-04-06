---
description: 타사 애플리케이션에서 Analytics로 추적 데이터를 가져옵니다.
title: Analytics Data Connectors 시작하기
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Data Connectors 개요

Adobe는 조직의 디지털 전략 및 마케팅 이니셔티브에 대한 실행 가능한 실시간 인텔리전스를 제공합니다. 데이터 커넥터를 사용하면 타사 애플리케이션의 추적 데이터를 Analytics로 가져올 수 있으므로 한 곳에서 데이터를 수집하고 사용할 수 있습니다. 파트너 제품 중 하나를 사용하는 경우 애플리케이션 데이터를 마케팅 보고서로 가져오는 통합을 만들 수 있습니다. 통합되면 애플리케이션에서 데이터를 포함하는 보고서를 생성할 수 있습니다.

예를 들어 이메일 통합은 이메일 파트너를 사용하여 이메일 캠페인을 배포해야 할 수 있습니다. 방문자가 웹 사이트를 방문하면 이메일 캠페인에 대한 응답으로 들어온 방문자를 알 수 있습니다. 데이터 커넥터는 이메일 파트너의 데이터를 마케팅 보고서에 통합하므로 이 정보를 확인하여 이메일 캠페인의 효과를 측정할 수 있습니다.

**시스템 요구 사항**

데이터 커넥터는 가장 널리 사용되는 브라우저와 적절히 통합되어야 합니다. 그러나 보고서는 다음 권장 사항을 충족하는 시스템에서 가장 잘 보이고 작동합니다.

* 브라우저:Microsoft Internet Explorer 버전 6 이상
* 쿠키: 필수
* JavaScript:활성화됨
* 운영 체제:Windows 기반
* Macromedia Flash Player:버전 6 이상
* 모니터 해상도:1024x768(800x600이 작동함)
* 색상 깊이:16비트 이상

또한 데이터 수집은 웹 브라우저에서 JavaScript가 사용 가능하게 설정되어 있을 때 개선됩니다.

**전제 조건**

제품에 대한 데이터 커넥터 통합을 구성하기 전에 다음을 수행하십시오.

* 마케팅 보고서와 통합하려는 모든 데이터에 액세스할 수 있는 권한과 함께 파트너 제품 계정에 필요한 액세스 자격 증명을 보유합니다. 보고서 배포자에 대한 특별 이메일 계정을 만들고 통합 작업에 대한 알림을 받을 수 있습니다.
* 캠페인 정보를 포함하는 사용자 지정 변수를 식별합니다. 이를 일반적으로 캠페인 추적 코드라고 하지만 조직에서 다른 용어를 사용할 수 있습니다.
* 노출 횟수를 수신할 이벤트를 확인하고 데이터를 클릭합니다. 이벤트의 이름을 적절하게 변경할 수 있습니다.
* Analytics가 파트너 제품에서 생성된 데이터로 적절한 모델링을 수행할 수 있도록 랜딩 페이지에 적절한 코드를 배치합니다. 각 파트너 제품에 대한 특정 지침은 Data Connectors 쇼케이스의 리소스 탭에서 찾을 수 있습니다.

## 통합 추가

[!UICONTROL Data Connectors] 랜딩 페이지(콘솔)에 액세스하려면 현재 계정이 있어야 합니다. 또한 Adobe Analytics에 익숙해지는 것이 좋습니다.

1. Adobe Experience Cloud에 로그인합니다.
1. Click **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Data Connectors]**.
1. 클릭 **[!UICONTROL Add New]**.
1. 인터페이스를 **[!UICONTROL Add Integration]** 단계별로 진행합니다.

   개별 제품 통합에 따라, 통합 프로세스의 일부로 특정 구성 정보를 제공해야 할 수 있습니다.

   통합이 완료되면 파트너 제품 아이콘이 Data Connectors 네트워크 페이지에 표시되고 메뉴에서 사용할 수 있습니다.

## Data Connectors 콘솔

통합을 활성화하면 [!UICONTROL Data Connectors] 페이지에 표시됩니다. 콘솔에서 세부 사항을 보고 구성을 변경할 수 있습니다. 회사의 모든 보고서 세트에서 활성 통합 및 통합을 볼 수 있습니다. 활동 로그를 보고 통합을 대시보드로 설정하고 통합을 구성하고 도움말을 찾을 수도 있습니다.

![Data Connectors 콘솔](assets/data-connectors-console.png)

## Data Connectors의 리마케팅 세그먼트

리마케팅 세그먼트는 Data Connectors 통합에 사용된 변수를 기반으로 하여 생성되는 데이터 파일입니다.

Adobe Analytics는 이 파일을 별도의 일별 파일로 데이터 웨어하우스를 통해 Adobe가 타사를 위해 만든 FTP로 보냅니다. 그런 다음 제3자가 이러한 파일을 클라이언트에 배포합니다. 일반적으로 기업은 사이트를 방문하여 제품을 살펴보았지만 구매하지 않은 방문자에게 리마케팅하기 위해 이 기능을 사용합니다. (예를 들어 고객이 본 제품에 대해 할인 혜택을 제공하지만 구매로 끝나지 않은 고객에게 도달합니다.)

**세그먼트**

* [!UICONTROL Cart Abandonment]:방문자가 장바구니에 품목을 추가했지만 구매하지 않은 비율 기술적으로 장바구니 추가로 나누어진 주문으로 구성된 계산된 지표입니다.
* [!UICONTROL Purchases]:특정 제품의 메시지 ID를 기반으로 구매를 수행한 수신자 ID(또는 방문자 ID).
* [!UICONTROL Product Views]:이와 [!UICONTROL Cart Abandonment]유사하게, 계산된 지표이기도 합니다. It reports [!UICONTROL Product Views] divided by Orders, because customers&#39; viewing the product shows some interest.

**구현 예제**

리마케팅 세그먼트를 성공적으로 구현하려면 다음 조건을 충족해야 합니다.

* 데이터 커넥터 계약이 체결되었으며 조직이 Adobe 컨설턴트와 구현 단계를 완료했습니다.
* 해당 이벤트는 products 변수와 동시에 실행됩니다.
   * 장바구니 포기: `scAdd` 이벤트
   * 구매: `purchase` 이벤트
   * 제품 보기: `prodView` 이벤트

>[!NOTE] 연결된 이벤트 없이 제품이 정의된 경우 prodView 이벤트가 자동으로 실행됩니다.
위의 요구 사항을 충족하지 않으면 해당 리마케팅 세그먼트가 올바르게 보고되지 않습니다.

[!UICONTROL Cart Abandonment]:사용자가 장바구니에 제품을 추가한 후 실행됩니다.

```
s.products=";cat";
s.events="scAdd";
```

[!UICONTROL Purchases]:구매 확인 페이지에서 실행됩니다.

```
s.products=";
cat;1;50";
s.events="purchase";
//Note: Though optional, adding the purchaseID variable increases accuracy by preventing duplicate purchases
```

**일반적인 문제**

| 문제 | 설명 |
| -----------| ---------- |  
| 리마케팅 세그먼트 파일에 제품 ID 정보가 표시되지 않습니다. | 이 문제는 올바른 이벤트가 실행되었지만, 같은 이미지 요청에 제품 변수가 없는 경우 발생합니다. 이 문제를 해결하려면 위의 구현 예에서 보듯이 products 변수와 해당 이벤트가 동일한 페이지에서 실행되는지 확인하십시오. |
| 리마케팅 세그먼트 파일을 받지 못했습니다. | 파일을 수신하지 않는 경우 조직에서 지원되는 사용자 중 한 명이 ClientCare에 연락하여 보고서가 성공적으로 수신되지 않은 원인을 조사하도록 하십시오. |


>[!IMPORTANT] 일반적으로 컨설턴트는 표준 Data Connectors 통합 리마케팅 세그먼트 파일 외에 매일 예약된 보고서로 데이터 웨어하우스 요청을 설정합니다. 이 데이터 웨어하우스 요청에는 데이터 커넥터 변수 및 데이터 커넥터 변수가 포함되며, 요청은 조직의 특정 요청만을 기준으로 예약할 수 있습니다. 문제 해결 시 혼동을 방지하려면 해당 파일이 실제 리마케팅 세그먼트 파일인지, 비genesis 변수가 들어 있는 데이터 웨어하우스 요청인지 지정하십시오.
