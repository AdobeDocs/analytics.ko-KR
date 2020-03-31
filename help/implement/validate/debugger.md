---
title: 기존 Adobe Experience Cloud Debugger
description: 기존 Adobe Experience Cloud Debugger를 설치합니다. 이 디버거는 Analytics, Target, Advertising Cloud, Identity Service, DTM 및 Launch용 태그를 검사합니다.
translation-type: ht
source-git-commit: 819f719c4ce131c04916f3b668bcbda1a1b03651

---


# 기존 Adobe Experience Cloud Debugger

> [!IMPORTANT] 이 디버깅 도구는 더 이상 유지 관리되지 않습니다. 대신 [Adobe Experience Cloud Debugger Chrome 확장 프로그램](https://docs.adobe.com/content/help/ko-KR/debugger/using/experience-cloud-debugger.html)을 사용하는 것이 좋습니다.

[!UICONTROL 기존 디버거]는 대부분의 Adobe Experience Cloud 서비스용 태그를 검사합니다. 디버거를 사용하면 사이트의 지정된 페이지에서 어떤 데이터가 Adobe에 전송되는지 볼 수 있습니다. 이 정보를 사용하여 조직의 구현 문제를 해결하거나 유효성을 검사할 수 있습니다.

## 기존 디버거 설치

JavaScript 북마클릿을 만들어 디버거를 설치하십시오.

### 1단계: 북마클릿 코드 복사

다음 코드를 클립보드에 복사합니다.

```JavaScript
javascript:void(window.open("","stats_debugger","width=800,height=800,location=0,menubar=0,status=1,toolbar=0,resizable=1,scrollbars=1").document.write("<script language=\"JavaScript\" id=dbg src=\"https://www.adobetag.com/d1/digitalpulsedebugger/live/DPD.js\"></"+"script>"+"<script language=\"JavaScript\">window.focus();</script>"));
```

### 2단계: 북마클릿 코드를 책갈피에 붙여넣기

각 브라우저의 책갈피 처리 방법은 서로 다르지만 개념은 동일합니다. 책갈피는 URL로서 원하는 이름과 북마클릿 코드를 사용하여 만듭니다.

#### Chrome

[chrome 확장 프로그램](https://docs.adobe.com/content/help/ko-KR/debugger/using/experience-cloud-debugger.html)을 굳이 사용하지 않으면 기존 디버거 북마클릿을 대신 사용할 수 있습니다.

1. 오른쪽 상단에 있는 세 점을 클릭한 다음, 책갈피 > 책갈피 관리자로 이동합니다. `Ctrl` + `Shift` + `O`(Windows) 또는 `Cmd` + `Shift` + `O`(Mac)을 누를 수도 있습니다.
2. 책갈피 관리자의 오른쪽 상단에서 세 점을 클릭한 다음, &#39;새 책갈피 추가&#39;를 클릭합니다.
3. 이름 필드에서 &quot;Adobe Experience Cloud Debugger&quot;로 레이블을 지정하고 코드 조각을 URL 필드에 붙여 넣습니다.
4. 책갈피 관리자를 사용하여 새 북마클릿을 원하는 위치에 배치합니다.

#### Firefox

1. 오른쪽 상단에 있는 세 줄을 클릭한 다음, 라이브러리 > 책갈피 > 모든 책갈피 표시로 이동합니다. `Ctrl` + `Shift` + `B`(Windows) 또는 `Cmd` + `Shift` + `B`(Mac)을 누를 수도 있습니다.
2. 구성 > 새 책갈피를 클릭합니다.
3. 이름 필드에서 &quot;Adobe Experience Cloud Debugger&quot;로 레이블을 지정하고 코드 조각을 위치 필드에 붙여 넣습니다. 태그 및 키워드 필드는 필수가 아닙니다.
4. 라이브러리 창을 사용하여 새 북마클릿을 원하는 위치에 배치합니다.

#### Edge

Edge에서는 북마클릿을 수동으로 만들 수 없지만 책갈피 URL을 편집하여 북마클릿에 포함할 수는 있습니다.

1. URL 필드의 오른쪽에 있는 별 아이콘을 클릭하여 현재 페이지를 책갈피로 지정합니다.
2. 책갈피 이름을 &quot;Adobe Experience Cloud Debugger&quot;로 지정하고 원하는 위치에 저장합니다.
3. 줄이 있는 별 아이콘을 클릭하여 즐겨찾기 막대를 엽니다.
4. 새로 만든 책갈피를 마우스 오른쪽 단추로 클릭하고 &#39;URL 편집&#39;을 선택합니다.
5. 코드 조각을 텍스트 필드에 붙여 넣은 다음, Enter 키를 누릅니다.

#### Safari

Safari에서는 북마클릿을 수동으로 만들 수 없지만 책갈피 URL을 편집하여 북마클릿에 포함할 수는 있습니다.

1. 오른쪽 상단의 공유 아이콘을 클릭하여 책갈피 모달 창을 엽니다.
2. 책갈피 이름을 &quot;Adobe Experience Cloud Debugger&quot;로 지정하고 원하는 위치에 저장합니다.
3. 책갈피 > 책갈피 편집을 클릭하고 새로 만든 책갈피를 찾습니다.
4. 마우스 오른쪽 단추 > 주소 편집을 클릭한 다음, 코드 조각을 텍스트 필드에 붙여 넣습니다.

## 기존 디버거 사용

사이트에서 원하는 페이지로 이동한 다음, 북마클릿을 클릭하십시오. Adobe에 전송된 데이터를 보여주는 팝업 창이 나타납니다.

> [!NOTE] 특정 광고 차단 플러그인과 팝업 차단기가 디버거 창의 로드를 방해할 수 있습니다. 브라우저에서 차단된 팝업이 있는지 확인하고 팝업을 허용하여 디버거가 제대로 작동할 수 있도록 하십시오.

디버거에는 데이터 표시 방식을 사용자 지정하는 몇 가지 옵션이 있습니다. 이 옵션들은 데이터 수집에 영향을 주지 않습니다.

* **표시된 Experience Cloud 제품:** 각각의 Experience Cloud 제품에 대한 이미지 요청을 표시하거나 숨깁니다.
* **URL 디코딩:** URL은 이미지 요청을 보고에 표시되는 내용과 일치하도록 디코딩합니다. 이 상자는 선택된 채로 두는 것이 좋습니다.
* **자동 새로 고침:** 팝업을 몇 초마다 자동으로 새로 고쳐 페이지에서 더 많은 이미지 요청을 확인합니다. 디버거에서 컨텐츠를 복사하거나 붙여 넣으려면 선택 내용이 유지되도록 자동 새로 고침을 비활성화하십시오.
* **친숙한 형식:** 이미지 요청에서 유용한 레이블과 원시 쿼리 문자열 간 표시 형식을 전환합니다. 자세한 내용은 [데이터 수집 쿼리 매개 변수](query-parameters.md)를 참조하십시오.

디버거에 대한 기본 표시 옵션을 저장하려면 오른쪽 상단에 있는 &#39;Adobe Debugger&#39; 링크를 마우스 오른쪽 단추로 클릭한 다음, 링크 주소를 복사합니다. 현재 디버거 북마클릿을 편집하고 업데이트된 코드 조각을 URL 필드에 붙여 넣으십시오.
