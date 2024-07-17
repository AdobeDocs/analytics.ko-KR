---
title: Activity Map FAQ
description: Activity Map 관련 FAQ
feature: Activity Map
role: User, Admin
exl-id: 6b2767cb-6c2c-4bf3-b9a9-a23418624650
source-git-commit: 64964972410911c2bea1460039def39b7c6dfa38
workflow-type: tm+mt
source-wordcount: '1094'
ht-degree: 15%

---

# Activity Map FAQ

Activity Map 관련 FAQ

+++Activity Map에 대한 권한을 부여하려면 어떻게 해야 합니까?

Activity Map 및 관련 차원을 사용할 수 있는 권한은 [Adobe Admin Console](/help/admin/admin-console/home.md)에서 처리됩니다.

Activity Map에 필요한 [권한 항목](/help/admin/admin-console/permissions/product-profile.md)은(는) 다음과 같습니다.

* **[!UICONTROL Analytics 도구]** > **[!UICONTROL Activity Map]**
* **[!UICONTROL Analytics 도구]** > **[!UICONTROL 세그먼트 게시]**
* **[!UICONTROL Dimension]** > **[!UICONTROL Activity Map 스크롤 도달]**
* **[!UICONTROL Dimension]** > **[!UICONTROL 지역별 Activity Map 링크]**
* **[!UICONTROL Dimension]** > **[!UICONTROL Activity Map 지역]**
* **[!UICONTROL Dimension]** > **[!UICONTROL Activity Map 링크]**
* **[!UICONTROL Dimension]** > **[!UICONTROL Activity Map 페이지]**

자세한 내용은 [Analytics 도구에 대한 제품 프로필 권한](/help/admin/admin-console/permissions/analytics-tools.md)을 참조하세요.

+++

+++모든 Analytics 고객이 Activity Map에 액세스할 수 있습니까?

Adobe Analytics Standard, Premium 및 Ultimate 계약을 맺은 조직은 Activity Map에 액세스할 수 있습니다. 이러한 계약 유형은 대부분의 Adobe Analytics 고객을 나타냅니다.

+++

+++Activity Map은 어떻게 단일 페이지 애플리케이션(SPA)을 지원합니까?

Activity Map은 몇 초마다 웹 페이지를 스캔하여 변경 사항을 찾습니다. Activity Map은 다시 로드할 필요 없이 페이지에서 새 컨텐츠를 찾지만 이 새 컨텐츠는 항상 첫 번째 페이지 차원 값에 귀속됩니다.

* Activity Map는 알려진 링크의 가시성이 변경되었는지 확인합니다. 가시성이 바뀐 것이 발견되면 Links On Page 표의 해당 링크에 대한 상태 열이 [!UICONTROL 표시됨] 또는 [!UICONTROL 숨겨짐]으로 업데이트됩니다.

* 사용자 상호 작용에서 새 콘텐츠를 만들면 AppMeasurement이 링크로 결정하는 모든 새 요소가 [!UICONTROL Links On Page] 표에 추가됩니다. Activity Map은 이 새로운 링크를 포함하는 새로운 데이터 요청을 전송합니다. 데이터 요청이 반환되면 [!UICONTROL Links On Page] 표에 새 링크가 나타납니다.

+++

+++Activity Map은 보기는 했지만 클릭하지 않은 링크에 대한 데이터를 제공합니까?

아니요. Adobe은 열람만 한 링크를 자동으로 추적하지 않습니다.

+++

+++Activity Map은 어떤 브라우저와 버전을 지원합니까?

Activity Map은 최신 버전의 가장 현대적인 브라우저를 지원합니다.

+++

+++Activity Map이 서버 호출을 늘립니까?

Activity Map은 자체적으로 서버 호출을 보내지 않습니다. 대신 Activity Map 컨텍스트 데이터 변수가 후속 페이지의 Analytics 페이지 보기 호출에 포함됩니다. 그러나 웹 SDK의 일부 이전 버전의 Activity Map은 Activity Map 데이터에 대한 별도의 호출을 전송합니다. 최신 버전의 Web SDK를 사용하는 경우 Activity Map 데이터가 다음 이벤트와 병합됩니다.

+++

+++왜 오버레이에서 일부 등급 번호가 누락되어 있습니까?

메뉴에 포함된 링크와 같은 일부 링크는 페이지에서 숨겨집니다. 따라서 해당 링크 오버레이가 표시되지 않습니다. 숨겨진 링크를 포함하여 페이지의 모든 링크에 대해 등급이 매겨집니다.

+++

+++모든 링크 보고서에서 링크 등급은 어떻게 결정됩니까?

* **그라데이션 및 버블 모드에서**: 지표 열이 등급을 결정합니다. 동일한 지표 값이 있는 링크의 경우 등급은 추가적으로 링크 ID 알파벳순을 기반으로 합니다.
* **승자 및 패자 모드**: 얻은 비율 열이 등급을 결정합니다. 이득이 동일한 링크의 경우 등급은 추가적으로 링크 ID 알파벳순을 기반으로 합니다.

+++

+++여러 보고서 세트를 사용하는 페이지에서 Activity Map은 어떻게 작동합니까?

기본적으로 Activity Map은 페이지의 첫 번째 태그와 연결된 보고서 세트를 사용합니다. **[!UICONTROL Activity Map 설정]** > **[!UICONTROL 기타]** 탭을 통해 다른 보고서 세트를 선택할 수 있습니다.

+++

+++Activity Map이 페이지에서 Adobe Analytics을 검색하는 데 얼마나 걸립니까?

Activity Map은 페이지 완료 이벤트 후 최대 20초 동안 Adobe Analytics의 존재를 검색합니다.

+++

+++Activity Map은 어떻게 다이내믹 콘텐츠를 처리합니까?

Activity Map은 2초마다 다음과 같은 웹 페이지 상태의 변경 사항을 발견했는지 확인합니다.

* 표시된 HTML 콘텐츠
* 숨겨진 HTML 콘텐츠
* 주입된 새 HTML 콘텐츠

콘텐츠가 숨거나 표시되는 경우, 확장 기능은 영향을 받는 링크 상태를 자동으로 숨김에서 표시로, 또는 표시에서 숨김으로 변경합니다(따라서 오버레이합니다). 새 콘텐츠가 삽입되면 애플리케이션은 연결된 링크를 검색하고 해당 링크에 대한 분석 데이터를 가져온 다음 이러한 링크에 대한 오버레이를 추가합니다.

+++

+++페이지 흐름 보고서는 어떤 지표를 기반으로 합니까?

표시된 모든 데이터는 페이지 보기를 기반으로 합니다.

+++

+++데이터 피드를 통해 Activity Map 데이터를 내보낼 수 있습니까?

예. Activity Map이 사용하는 [데이터 피드 열](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md)은(는) 다음과 같습니다.

* Activity Map 링크: `clickmaplink`
* Activity Map 페이지: `clickmappage`
* Activity Map 영역: `clickmapregion`
* 지역별 Activity Map 링크: `clickmaplinkbyregion`

+++

+++세그먼트는 라이브 모드에서 작동합니까?

아니요. 세그먼트는 라이브 모드에서 작동하지 않습니다.

+++

+++Activity Map이 가상 보고서 세트와 호환합니까?

예. 하지만, 가상 보고서 세트 제한 사항으로 인해 Activity Map의 라이브 모드는 가상 보고서 세트와 호환되지 않습니다.

+++

+++Activity Map을 비활성화하려면 어떻게 해야 합니까?

Activity Map을 비활성화하는 방법은 구현 유형에 따라 다릅니다.

* **Web SDK 확장**: 확장 구성 설정에서 **[!UICONTROL 내부 링크 클릭 수 수집]**, **[!UICONTROL 외부 링크 클릭 수 수집]** 및 **[!UICONTROL 다운로드 링크 클릭 수 수집]** 상자의 선택을 취소합니다.
* **웹 SDK JavaScript 라이브러리**: [`clickCollectionEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled)을(를) `false`(으)로 설정합니다.
* **Analytics 확장**: 확장 구성 설정에서 **[!UICONTROL Activity Map 사용]** 확인란을 선택 취소합니다.
* **AppMeasurement**: `AppMeasurement.js` 내의 Activity Map 모듈을 제거하거나 주석 처리하거나 모듈 함수 호출을 빈 본문으로 덮어씁니다.

  ```js
  function AppMeasurement_Module_ActivityMap() {}
  ```

+++

+++Activity Map 오버레이를 사용하기 위한 시스템 요구 사항은 무엇입니까?

Activity Map 확장 기능으로 최신 버전의 Chrome, Edge 또는 Firefox를 사용할 수 있습니다.

+++

+++개인 식별 정보에 대한 Activity Map을 사용할 때 고려해야 할 사항은 무엇입니까?

Activity Map을 사용하여 개인 식별 가능한 데이터를 수집할 수 있는 다음 시나리오를 고려하십시오.

* **전자 메일 링크**: 전자 메일 주소를 클릭하여 사용자의 메일 클라이언트를 열 수 있는 경우 Activity Map은 클릭한 전자 메일 주소를 수집할 수 있습니다.
* **Activity Map ID 링크**: 방문자가 로그인한 후 방문자의 사용자 ID가 포함된 모든 링크를 기록할 수 있습니다.
* **중요 정보 링크**: 금융 기관의 경우 계정 번호와 같은 중요 정보가 링크이고 방문자가 클릭하는 경우 추적할 수 있습니다.
* **개인 정보가 포함된 링크**: 의료 웹 사이트의 경우 링크에 개인 정보가 포함될 수 있습니다. 방문자가 이러한 링크를 클릭하면 Activity Map이 해당 링크 텍스트를 수집합니다.

+++

+++Activity Map은 기본적으로 어떤 데이터를 추적합니까?

Activity Map은 다음 요소를 추적합니다.

* `href` 속성이 있는 `<a>` 또는 `<area>` 태그입니다. 앵커 태그 링크(`#`)는 기본적으로 추적되지 않습니다.
* `s_objectID` 변수를 설정하는 `onclick` 특성
* 값 또는 자식 텍스트가 있는 `<input>` 태그 또는 `submit` 단추
* 유형 `image` 및 속성 `src`의 `<input>` 태그
* `type="button"` 특성이 없는 `<button>` 태그입니다. `<button>`개의 태그를 추적하려면 `role="button"` 또는 `submit="button"`과(와) 같은 특성을 대신 사용하십시오.

+++

+++Activity Map이 자동으로 추적하는 링크의 예는 무엇입니까?

다음은 Activity Map에 링크를 추적하는 데 필요한 모든 정보가 있는 몇 가지 예입니다.

```html
<a href="home.html">Home</a>

<input type="submit" value="Submit"/>

<input type="image" src="submit-button.png"/>

<p onclick="var s_objectID='Market rates';">
  <span class="title">Current Market Rates</span>
  <span class="subtitle">1.45 USD</span>
</p>

<div onclick="s.tl(true,'o','Chat button')">
  <span class="title">Chat with an agent now</span>
  <span class="subtitle">Current wait: 0 minutes</span>
</div>
```

+++

+++Activity Map이 자동으로 추적하지 않는 링크의 예는 무엇입니까?

다음은 Activity Map이 클릭을 추적하지 않는 몇 가지 예입니다.

```html
<!-- Anchor tag does not have a valid href -->
<a name="innerAnchor">Section header</a>

<!-- Neither s_objectID or tl() method present -->
<p onclick="showPanel('stock price')">
  <span class="title">Current company stock price</span>
  <span class="subtitle">987.65 USD</span>
</p>

<!-- Neither s_objectID or tl() method present -->
<input type="radio" onclick="changeState(this)" name="group1" value="A"/>
<input type="radio" onclick="changeState(this)" name="group1" value="B"/>
<input type="radio" onclick="changeState(this)" name="group1" value="C"/>

<!-- src property missing on a form input element -->
<input type="image"/>
```

+++
