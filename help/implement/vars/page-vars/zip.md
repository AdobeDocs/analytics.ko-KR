---
title: zip
description: 보고서 세트 설정이 허용하는 경우 '우편번호' 차원을 수동으로 채웁니다.
translation-type: tm+mt
source-git-commit: f75c6759feb6576017733f1aac5bff2e21d4b0af

---


# zip

이 `zip` 변수를 사용하면 보고서 세트 설정의 Zip [!UICONTROL 옵션을] 사용하여 &#39;Zip 코드&#39; 차원을 수동으로 채울 수 있습니다. 이전 버전의 Adobe Analytics에서는 일반적으로 소매 사이트에 배송 정보를 입력할 때만 이 변수를 수동으로 설정할 수 있습니다. Adobe Analytics의 향상된 기능을 사용하면 지리적 위치 데이터를 사용하여 이 변수를 자동으로 설정할 수 있습니다. 이 변수는 설정된 히트 이후로 지속되지 않습니다.

> [!IMPORTANT] 보고서 세트 [!UICONTROL 설정의] Zip 옵션이 원하는 값으로 설정되어 있는지 확인합니다. 이 변수는 [!UICONTROL 지역 zip] 이 항상 사용되는 경우 사용할 수 없습니다. See [General Account Settings](/help/admin/admin/general-acct-settings-admin.md) in the Admin user guide for more information.

## Adobe Experience Platform Launch에 압축

Analytics 확장 기능(전역 변수)을 구성하는 동안 또는 규칙에서 우편번호를 설정할 수 있습니다.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. 원하는 속성을 클릭합니다.
3. 규칙 [!UICONTROL 탭으로 이동한] 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [ [!UICONTROL 동작]]에서 기존 Adobe Analytics - [!UICONTROL 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. 확장 [!UICONTROL 프로그램 드롭다운을 Adobe] Analytics로 설정하고 작업 [!UICONTROL 유형을 변수][!UICONTROL 설정으로]설정합니다.
6. Zip [!UICONTROL 섹션을] 찾습니다.

우편 번호를 데이터 요소를 포함한 모든 문자열 값으로 설정할 수 있습니다.

## s.zip in AppMeasurement and Launch custom code editor

이 `s.zip` 변수는 일반적으로 우편번호를 포함하는 문자열이지만 원하는 값을 최대 50바이트로 포함할 수 있습니다.

```js
s.zip = "84043";
```
