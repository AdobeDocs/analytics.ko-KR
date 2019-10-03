---
description: 기존 Adobe Experience Cloud Debugger를 설치합니다. 이 디버거는 Analytics, Target, Advertising Cloud, Identity Service, DTM 및 Launch에 대한 태그를 검사합니다.
seo-description: 기존 Adobe Experience Cloud Debugger를 설치합니다. 이 디버거는 Analytics, Target, Advertising Cloud, Identity Service, DTM 및 Launch에 대한 태그를 검사합니다.
seo-title: 기존 Adobe Experience Cloud 디버거
title: 기존 Adobe Experience Cloud 디버거
translation-type: tm+mt
source-git-commit: 2ea071c4d4f675c74770396610219d405a07a0e1

---


# Legacy Adobe Experience Cloud Debugger

> [!IMPORTANT] 이 디버깅 도구는 더 이상 유지 관리되지 않습니다. Adobe에서는 대신 Adobe Experience Cloud 디버거 [Chrome 확장을 사용하는 것이 좋습니다](https://docs.adobe.com/content/help/en/debugger/using/experience-cloud-debugger.html).

레거시 [!UICONTROL 디버거는] 대부분의 Adobe Experience Cloud 서비스에 대한 태그를 검사합니다. 디버거를 사용하면 사이트에서 지정된 페이지에서 Adobe로 전송되는 데이터를 볼 수 있습니다. 이 정보를 사용하여 조직의 구현 문제를 해결하거나 유효성을 확인할 수 있습니다.

## 레거시 디버거 설치

JavaScript 북마클릿을 만들어 디버거를 설치합니다.

### 1단계:북마클릿 코드 복사

다음 코드를 클립보드에 복사합니다.

```JavaScript
javascript:void(window.open("","stats_debugger","width=800,height=800,location=0,menubar=0,status=1,toolbar=0,resizable=1,scrollbars=1").document.write("<script language=\"JavaScript\" id=dbg src=\"https://www.adobetag.com/d1/digitalpulsedebugger/live/DPD.js\"></"+"script>"+"<script language=\"JavaScript\">window.focus();</script>"));
```

### 2단계:북마클릿 코드를 책갈피에 붙여넣기

각 브라우저에는 책갈피를 처리하는 방법이 다르지만 개념은 동일합니다. 책갈피는 원하는 이름과 북마클릿 코드를 URL로 만듭니다.

#### Chrome

반드시 [크롬 확장을](https://docs.adobe.com/content/help/en/debugger/using/experience-cloud-debugger.html)사용하지 않으면 기존 디버거 북마클릿을 대신 사용할 수 있습니다.

1. 오른쪽 상단에 있는 세 개의 점을 클릭한 다음 책갈피 &gt; 책갈피 관리자로 이동합니다. + `Ctrl` + `Shift` + `O` (Windows) `Cmd` 또는 `Shift` + `O` +(Mac)를 누를 수도 있습니다.
2. 책갈피 관리자의 오른쪽 상단에서 세 개의 점을 클릭한 다음 '새 책갈피 추가'를 클릭합니다.
3. In the Name field, label it "Adobe Experience Cloud Debugger", and paste the code snippet into the URL field.
4. Use the bookmark manager to place your new bookmarklet in the desired location.

#### Firefox

1. 오른쪽 상단의 세 줄을 클릭한 다음 라이브러리 &gt; 책갈피 &gt; 모든 책갈피 표시로 이동합니다. + `Ctrl` + `Shift` + `B` (Windows) `Cmd` 또는 `Shift` + `B` +(Mac)를 누를 수도 있습니다.
2. 구성 &gt; 새 책갈피를 클릭합니다.
3. 이름 필드에서 "Adobe Experience Cloud Debugger"로 레이블을 지정하고 코드 조각을 위치 필드에 붙여 넣습니다. 태그 및 키워드 필드는 필수가 아닙니다.
4. 라이브러리 창을 사용하여 새 북마클릿을 원하는 위치에 배치합니다.

#### Edge

Edge에서는 북마클릿을 수동으로 만들 수 없지만 책갈피 URL을 편집할 수 있습니다.

1. URL 필드 오른쪽에 있는 별 아이콘을 클릭하여 현재 페이지를 책갈피로 지정합니다.
2. 책갈피 이름을 "Adobe Experience Cloud Debugger"로 지정하고 원하는 위치에 저장합니다.
3. 선이 있는 별 아이콘을 클릭하여 즐겨찾기 막대를 엽니다.
4. 새로 만든 책갈피를 마우스 오른쪽 단추로 클릭하고 'URL 편집'을 선택합니다.
5. Paste the code snippet in the text field, then hit Enter.

#### Safari

Safari does not have the ability to manually create a bookmarklet, but a bookmark URL can be edited.

1. Click the Share icon in the top right, which opens a bookmark modal window.
2. Name the bookmark "Adobe Experience Cloud Debugger", and save it in the desired location.
3. Click Bookmarks &gt; Edit Bookmarks, and locate the newly created bookmark.
4. Right click &gt; Edit Address, then paste the code snippet into text field.

## Using the legacy debugger

디버거를 사용하려면 사이트에서 원하는 페이지로 이동한 다음 북마클릿을 클릭합니다. Adobe로 전송된 데이터를 보여주는 팝업 창이 나타납니다.

> [!NOTE] Certain ad-blocking plug-ins and pop-up blockers can interfere with the loading of the debugger window. Check for blocked pop-ups in your browser, and allow them so the debugger can work correctly.

The debugger has several options available, all of which customize how data is displayed. None of these options affect data collection.

* **Displayed Experience Cloud products:** Shows or hides image requests for each respective Experience Cloud product.
* **** URL 디코드:URL 파섹 이 상자를 선택된 상태로 두는 것이 좋습니다.
* **** 자동 새로 고침:몇 초마다 자동으로 팝업을 새로 고쳐 페이지에서 더 많은 이미지 요청을 확인합니다. If you need to copy/paste content in the debugger, disable auto-refresh so your selection stays.
* **** 친숙한 형식:이미지 요청의 유용한 레이블과 원시 쿼리 문자열 간에 표시 형식을 전환합니다. 자세한 [내용은 데이터 수집 쿼리 매개](../js-implementation/data-collection/query-parameters.md) 변수를 참조하십시오.

디버거에 대한 기본 표시 옵션을 저장하려면 오른쪽 위 모서리에 있는 'Adobe Debugger' 링크를 마우스 오른쪽 단추로 클릭한 다음 링크 주소를 복사합니다. 현재 디버거 북마클릿을 편집하고 업데이트된 코드 조각을 URL 필드에 붙여 넣습니다.
