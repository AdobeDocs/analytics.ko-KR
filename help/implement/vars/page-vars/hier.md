---
title: hier
description: Adobe Analytics에서 계층 변수를 구현합니다.
feature: Variables
exl-id: 72bdab8f-a001-4ada-b5e2-453a8e3f24a6
source-git-commit: f435453f655caef89460de42ebecf489b021dc47
workflow-type: ht
source-wordcount: '352'
ht-degree: 100%

---

# hier

>[!IMPORTANT]
>
>이 변수는 사용이 중단되었으며 Analysis Workspace에서 사용할 수 있는 차원이 아닙니다. Adobe에서는 대신 [eVar](evar.md) 및 분류를 사용하는 것이 좋습니다.

계층 변수는 사이트의 구조를 볼 수 있도록 해 주는 사용자 정의 변수입니다. Adobe는 구현에서 최대 5개의 계층 변수를 지원합니다.

이 변수는 사이트 구조의 수준이 4 이상인 사이트에 유용합니다. 예를 들어 미디어 사이트의 스포츠 섹션에는 4개 수준 (`Sports`, `Local Sports`, `Baseball`및 `Team name`)이 있을 수 있습니다. 누군가 야구 페이지를 방문하면 스포츠, 해외 스포츠 및 야구가 해당 방문을 모두 반영합니다.

구현에서 계층을 사용하기 전에 보고서 세트 설정에서 각 계층을 구성해야 합니다.

## 웹 SDK를 사용한 계층

계층은 XDM 필드 `_experience.analytics.customDimensions.hierarchies.hier1` 아래에서 `_experience.analytics.customDimensions.hierarchies.hier5`에 [Adobe Analytics에 대해 매핑됩니다](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html).

## Adobe Analytics 확장을 사용한 계층

Analytics 확장(전역 변수)을 구성하는 동안 또는 규칙에서 계층을 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [Adobe Experience Platform 데이터 수집](https://experience.adobe.com/data-collection)에 로그인합니다.
2. 원하는 태그 속성을 클릭합니다.
3. [!UICONTROL 규칙] 탭으로 이동한 다음 원하는 규칙을 클릭하거나 규칙을 만듭니다.
4. [!UICONTROL 작업]에서 기존 [!UICONTROL Adobe Analytics - 변수 설정] 작업을 클릭하거나 &#39;+&#39; 아이콘을 클릭합니다.
5. [!UICONTROL 확장] 드롭다운을 Adobe Analytics로 설정하고 [!UICONTROL 작업 유형]을 [!UICONTROL 변수 설정]으로 설정합니다.
6. [!UICONTROL 계층] 섹션을 찾습니다.

계층 구조 값을 정적 문자열로 설정하거나 데이터 요소를 참조할 수 있습니다. 원하는 구분 기호를 설정할 수도 있습니다. 여기에서 설정한 구분 기호가 보고서 세트 설정에서 설정한 구분 기호와 일치해야 합니다.

## AppMeasurement 및 Analytics 확장 사용자 정의 코드 편집기의 s.hier1 - s.hier5

각 계층은 조직에 관련된 사용자 정의 값을 포함하는 문자열입니다. 최대 길이는 255바이트이고, 255바이트보다 긴 값은 Adobe에 전송될 때 자동으로 잘립니다.

섹션 이름 중에 그 안에 구분 기호가 포함되는 섹션이 없도록 하십시오. 예를 들어 섹션 중 하나를 호출하면 `Coach Griffin, Jim`쉼표가 아닌 구분 기호를 선택합니다. 총 변수 제한은 255바이트입니다. 구분 기호는 `||` 또는 `/|\` 등의 여러 문자로 구성될 수 있으며 변수 값에 표시될 가능성이 줄어듭니다.

```js
s.hier1 = "Toys|Boys 6+|Legos|Super Block Tub";

s.hier3 = "Sports/Local Sports/Baseball";
```
