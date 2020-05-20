---
title: zip
description: 보고서 세트 설정이 허용하는 경우 '우편번호' 차원을 수동으로 채웁니다.
translation-type: ht
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# zip

보고서 세트 설정의 [!UICONTROL Zip 옵션]이 허용하는 경우 `zip` 변수를 사용하여 &#39;우편번호&#39; 차원을 수동으로 채울 수 있습니다. 이전 버전의 Adobe Analytics에서는 일반적으로 소매 사이트에 배송 정보를 입력할 때 이 변수를 수동으로만 설정할 수 있었습니다. Adobe Analytics의 개선된 기능을 사용하면 지리적 위치 데이터를 사용하여 이 변수를 자동으로 설정할 수 있습니다. 이 변수는 이 변수가 설정된 히트 이후로 지속되지 않습니다.

>[!IMPORTANT] 보고서 세트 설정의 [!UICONTROL Zip 옵션]이 원하는 값으로 설정되어 있는지 확인하십시오. 이 변수는 [!UICONTROL geo zip](지리적 우편번호) 이 항상 사용되는 경우에는 사용할 수 없습니다. 자세한 내용은 관리자 가이드에서 [일반 계정 설정](/help/admin/admin/general-acct-settings-admin.md)을 참조하십시오.

## Adobe Experience Platform Launch의 우편번호

Analytics 확장(전역 변수)을 구성하는 동안 또는 규칙에서 우편번호를 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [launch.adobe.com](https://launch.adobe.com)에 로그인합니다.
2. 원하는 속성을 클릭합니다.
3. [!UICONTROL 규칙] 탭으로 이동한 다음, 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [!UICONTROL 작업]에서 기존 [!UICONTROL Adobe Analytics - 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. [!UICONTROL 확장] 드롭다운을 Adobe Analytics로 설정하고 [!UICONTROL 작업 유형]을 [!UICONTROL 변수 설정]으로 설정합니다.
6. [!UICONTROL Zip] 섹션을 찾습니다.

우편번호를, 데이터 요소를 포함한 어떤 문자열 값으로든 설정할 수 있습니다.

## AppMeasurement 및 Launch 사용자 지정 코드 편집기의 s.zip

`s.zip` 변수는 일반적으로 우편번호를 포함하는 문자열이지만 최대 50바이트 길이이면 어떤 값이든 원하는 값을 포함할 수 있습니다.

```js
s.zip = "84043";
```
