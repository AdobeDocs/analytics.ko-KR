---
title: transactionID
description: 이 변수를 사용하여 온라인 및 오프라인 데이터를 함께 연결합니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# transactionID

`transactionID` 변수는 Data Sources를 통해 업로드된 데이터에 히트가 연결할 수 있도록 거래를 고유하게 식별합니다. 이 변수는 다른 채널의 데이터를 사용하고 이 데이터를 AppMeasurement로 수집한 데이터에 연결하려는 경우에 유용합니다.

>[!NOTE] 이 변수를 사용하기 전에 보고서 [!UICONTROL Transaction ID Storage] 세트에서 활성화되어 있는지 확인하십시오. 자세한 내용은 관리자 가이드에서 [일반 계정 설정](/help/admin/admin/general-acct-settings-admin.md)을 참조하십시오.

히트에서 `transactionID`를 설정하면 Adobe는 해당 시점에서 설정하거나 지속되는 모든 Analytics 변수의 &quot;스냅샷&quot;을 만듭니다. 일치하는 거래 ID로 Data Sources를 통해 업로드된 데이터는 해당 변수 값에 영구적으로 연결됩니다.

기본적으로 Adobe는 최대 90일 동안 모든 거래 ID 값(연결 및 연결 해제된 값)을 기억합니다. 오프라인 상호 작용 프로세스가 90일 이상인 경우 고객 지원에 요청하여 이 한계를 늘리십시오.

## Adobe Experience Platform Launch의 거래 ID

Analytics 확장(전역 변수)을 구성하는 동안 또는 규칙에서 거래 ID를 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. Go to the [!UICONTROL Rules] tab, then click the desired rule (or create a rule).
4. 아래에서 [!UICONTROL Actions]기존 [!UICONTROL Adobe Analytics - Set Variables] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. 드롭다운을 [!UICONTROL Extension] Adobe Analytics로 설정하고 [!UICONTROL Action Type] 을 [!UICONTROL Set Variables]설정합니다.
6. Locate the [!UICONTROL Transaction ID] section.

거래 ID를, 데이터 요소를 포함한 어떤 문자열 값으로든 설정할 수 있습니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.transactionID

`s.transactionID` 변수는 거래의 고유 식별자를 포함하는 문자열입니다. 유효한 값에는 최대 100바이트 길이의 영숫자 문자가 포함됩니다. 기본값은 빈 문자열입니다.

```js
s.transactionID = "ABC123";
```

히트에 대한 거래 ID가 두 개 이상 있는 경우 각각 쉼표로 구분할 수 있습니다. 여러 거래 ID에도 여전히 100바이트 제한이 적용됩니다.

```js
s.transactionID = "ABC123,XYZ456";
```

>[!NOTE] 이 변수를 사용하여 여러 오프라인 채널을 통합하는 경우 다른 채널이 거래 ID와 겹치지 않도록 하십시오. 예를 들어, `1234`라는 콜 센터 거래 ID 값과 `1234`라는 영업 리드 거래 ID 값이 있는 경우, 이 값들이 충돌하여 예상치 않은 결과가 발생할 수 있습니다. 거래 ID에 각 오프라인 채널에 대해 고유한 형식이 포함되어 있는지 확인하고 필요한 경우 구분해야 합니다. 예를 들어, Data Sources와 AppMeasurement 모두에서 콜 센터 거래 ID를 `call_1234`로 설정하고 영업 리드 거래 ID를 `lead_1234`로 설정합니다.
