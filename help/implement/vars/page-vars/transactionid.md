---
title: transactionID
description: 이 변수를 사용하여 온라인 및 오프라인 데이터를 함께 연결하십시오.
translation-type: tm+mt
source-git-commit: f75c6759feb6576017733f1aac5bff2e21d4b0af

---


# transactionID

이 `transactionID` 변수는 Data Sources를 통해 업로드된 데이터에 히트를 연결할 수 있도록 트랜잭션을 고유하게 식별합니다. 이 변수는 다른 채널의 데이터를 사용하고 AppMeasurement로 수집한 데이터에 연결하려는 경우에 유용합니다.

> [!NOTE] 이 변수를 사용하기 전에 [!UICONTROL 보고서] 세트에서 트랜잭션 ID 저장소가 활성화되어 있는지 확인합니다. See [General Account Settings](/help/admin/admin/general-acct-settings-admin.md) in the Admin user guide for more information.

히트를 `transactionID` 설정하면 Adobe는 모든 Analytics 변수의 &quot;스냅숏&quot;을 설정하거나 해당 시점에 지속합니다. 거래 ID와 일치하는 Data Sources를 통해 업로드된 데이터는 해당 변수 값에 영구적으로 연결됩니다.

기본적으로 Adobe는 최대 90일 동안 모든 거래 ID 값(연결 및 연결 해제)을 기억합니다. 오프라인 상호 작용 프로세스가 90일 이상인 경우 고객 지원 센터에 문의하여 이 제한을 연장하십시오.

## Adobe Experience Platform Launch의 거래 ID

Analytics 확장(전역 변수)을 구성하는 동안 또는 규칙에서 거래 ID를 설정할 수 있습니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 규칙 [!UICONTROL 탭으로 이동한] 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [ [!UICONTROL 동작]]에서 기존 Adobe Analytics - [!UICONTROL 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. 확장 [!UICONTROL 프로그램 드롭다운을 Adobe] Analytics로 설정하고 작업 [!UICONTROL 유형을 변수][!UICONTROL 설정으로]설정합니다.
6. 거래 ID [!UICONTROL 섹션을] 찾습니다.

거래 ID를 데이터 요소를 포함한 모든 문자열 값으로 설정할 수 있습니다.

## s.transactionID in AppMeasurement and Launch 사용자 지정 코드 편집기

이 `s.transactionID` 변수는 트랜잭션의 고유 식별자를 포함하는 문자열입니다. 유효한 값에는 최대 100바이트의 영숫자 문자가 포함됩니다. 기본값은 빈 문자열입니다.

```js
s.transactionID = "ABC123";
```

히트에 대한 거래 ID가 두 개 이상 있는 경우 쉼표로 구분하여 각각 지정할 수 있습니다. 여러 거래 ID는 여전히 100바이트 제한을 받습니다.

```js
s.transactionID = "ABC123,XYZ456";
```

> [!NOTE] 이 변수를 사용하여 여러 오프라인 채널을 통합하는 경우 다른 채널이 거래 ID와 겹치지 않도록 하십시오. 예를 들어, 에 대한 콜 센터 거래 ID 값과 `1234` 에 대한 판매 리드 거래 ID 값이 있는 경우, 이러한 값이 충돌하여 예상치 않은 결과가 발생할 수 `1234`있습니다. 거래 ID에 오프라인 채널당 고유한 형식이 포함되어 있는지 확인하고 필요한 경우 구분해야 합니다. 예를 들어, 콜 센터 거래 ID를 Data Sources와 AppMeasurement에서 `call_1234` 및 판매 리드 거래 ID로 `lead_1234` 설정합니다.
