---
title: zip
description: 보고서 세트 설정이 허용하는 경우 '우편번호' 차원을 수동으로 채웁니다.
feature: Appmeasurement Implementation
exl-id: 1acf4bf7-3788-46bd-bcdb-9885c7b93b59
role: Admin, Developer
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 75%

---

# zip

보고서 세트 설정의 [!UICONTROL Zip 옵션]이 허용하는 경우 `zip` 변수를 사용하여 &#39;우편번호&#39; 차원을 수동으로 채울 수 있습니다. 이전 버전의 Adobe Analytics에서는 일반적으로 리테일 사이트에 배송 정보를 입력할 때 이 변수를 수동으로만 설정할 수 있었습니다. Adobe Analytics의 개선된 기능을 사용하면 지리적 위치 데이터를 사용하여 이 변수를 자동으로 설정할 수 있습니다. 이 변수는 이 변수가 설정된 히트 이후로 지속되지 않습니다.

>[!IMPORTANT]
>
>보고서 세트 설정의 [!UICONTROL Zip 옵션]이 원하는 값으로 설정되어 있는지 확인하십시오. [!UICONTROL 지역 zip]이 항상 사용되는 경우에는 이 변수를 사용할 수 없습니다. 자세한 내용은 관리자 안내서에서 [일반 계정 설정](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md)을 참조하십시오.

## 웹 SDK을 사용하는 우편번호

우편 번호는 다음 변수에 매핑됩니다.

* [XDM 개체](/help/implement/aep-edge/xdm-var-mapping.md): `xdm.placeContext.geo.postalCode`
* [데이터 개체](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.zip`

## Adobe Analytics 확장을 사용한 우편번호

Analytics 확장(전역 변수)을 구성하는 동안 또는 규칙에서 우편번호를 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
2. 원하는 태그 속성을 클릭합니다.
3. [!UICONTROL 규칙] 탭으로 이동한 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [!UICONTROL 작업]에서 기존 [!UICONTROL Adobe Analytics - 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. [!UICONTROL 확장] 드롭다운 목록을 Adobe Analytics으로 설정하고 [!UICONTROL 작업 유형]을(를) [!UICONTROL 변수 설정]&#x200B;(으)로 설정합니다.
6. [!UICONTROL Zip] 섹션을 찾습니다.

우편번호를, 데이터 요소를 포함한 어떤 문자열 값으로든 설정할 수 있습니다.

## AppMeasurement 및 Analytics 확장 사용자 정의 코드 편집기의 s.zip

`s.zip` 변수는 일반적으로 우편번호를 포함하는 문자열이지만 최대 50바이트 길이이면 어떤 값이든 원하는 값을 포함할 수 있습니다.

```js
s.zip = "84043";
```
