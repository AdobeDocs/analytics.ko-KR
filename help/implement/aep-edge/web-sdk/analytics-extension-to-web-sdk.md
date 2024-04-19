---
title: Adobe Analytics 태그 확장에서 웹 SDK 태그 확장으로 마이그레이션
description: 웹 SDK 확장을 사용하도록 Adobe Experience Platform 데이터 수집 태그에서 Analytics 구현을 업데이트합니다.
exl-id: 691c29ca-d169-4ef8-9f91-d0375166796d
source-git-commit: 7bd4a188e5a2171260f1f0696d8bebad854dba4a
workflow-type: tm+mt
source-wordcount: '1706'
ht-degree: 1%

---

# Adobe Analytics 태그 확장에서 웹 SDK 태그 확장으로 마이그레이션

이 구현 경로에는 Adobe Analytics 태그 확장에서 웹 SDK 태그 확장으로 이동하는 메소드 마이그레이션 접근 방식이 포함됩니다. 다른 구현 경로는 별도의 페이지에서 다룹니다.

* [웹 SDK JavaScript 라이브러리에 AppMeasurement](appmeasurement-to-web-sdk.md): 태그를 사용하지 않는 경우를 제외하고 웹 SDK로 마이그레이션하는 유연하고 체계적인 방법입니다. 대신 수동으로 Adobe Analytics 데이터 수집 라이브러리(`AppMeasurement.js`) 웹 SDK JavaScript 라이브러리( )로 대체합니다`alloy.js`).
* [Web SDK 태그 확장](web-sdk-tag-extension.md): Adobe Experience Platform 데이터 수집의 태그를 사용하여 구현을 관리하는 새로운 웹 SDK 설치. XDM 스키마에 포함할 일반적인 Analytics 변수를 포함하는 Adobe Analytics ExperienceEvent 필드 그룹이 필요합니다.
* [웹 SDK JavaScript 라이브러리](web-sdk-javascript-library.md): Web SDK JavaScript 라이브러리를 사용한 새로운 웹 SDK 설치(`alloy.js`). 태그 UI를 사용하는 대신 구현을 직접 관리합니다. XDM 스키마에 포함할 일반적인 Analytics 변수를 포함하는 Adobe Analytics ExperienceEvent 필드 그룹이 필요합니다.

## 이 구현 경로의 장단점

이러한 마이그레이션 접근 방식을 사용하면 장점과 단점이 모두 있습니다. 각 옵션을 신중히 평가하여 조직에 가장 적합한 접근 방식을 결정하십시오.

| 장점 | 단점 |
| --- | --- |
| <ul><li>**사이트에 코드 변경 없음**: 구현에 이미 태그가 설치되어 있으므로 태그 인터페이스에서 모든 마이그레이션 업데이트를 수행할 수 있습니다.</li><li>**기존 구현 사용**: 이 접근 방식에서는 완전히 새로운 구현이 필요하지 않습니다. 새로운 규칙 작업이 필요하지만 최소한의 변경으로 기존 데이터 요소와 규칙 조건을 재사용할 수 있습니다.</li><li>**스키마가 필요하지 않음**: Web SDK로 마이그레이션하는 이 단계에서는 XDM 스키마가 필요하지 않습니다. 대신 `data` 개체 - Adobe Analytics으로 데이터를 직접 전송합니다. 웹 SDK로의 마이그레이션이 완료되면 조직에 대한 스키마를 만들고 데이터스트림 매핑을 사용하여 적용 가능한 XDM 필드를 채울 수 있습니다. 마이그레이션 프로세스의 이 단계에서 스키마가 필요한 경우 조직에서 Adobe Analytics XDM 스키마를 사용해야 합니다. 이 스키마를 사용하면 향후 조직에서 자체 스키마를 사용하는 것이 더 어려워집니다.</li></ul> | <ul><li>**구현 기술 부채**: 이 방법은 기존 구현의 수정된 형식을 사용하므로 구현 논리를 추적하고 필요한 경우 변경을 수행하는 것이 더 어려울 수 있습니다. 사용자 지정 코드는 특히 디버깅하기 어려울 수 있습니다.</li><li>**데이터를 플랫폼으로 전송하기 위한 매핑 필요**: 조직에서 Customer Journey Analytics을 사용할 준비가 되면 Adobe Experience Platform의 데이터 세트로 데이터를 보내야 합니다. 이 작업을 수행하려면 의 모든 필드가 `data` 객체는 XDM 스키마 필드에 할당하는 데이터 스트림 매핑 도구의 항목입니다. 매핑은 이 워크플로우에 대해 한 번만 수행하면 되며 구현 변경을 수반하지 않습니다. 그러나 XDM 개체에서 데이터를 전송할 때는 필요하지 않은 추가 단계입니다.</li></ul> |

Adobe은 다음 시나리오에서 이 구현 경로를 따를 것을 권장합니다.

* Adobe Analytics 태그 확장을 사용하는 기존 구현이 있습니다. AppMeasurement을 사용하는 구현이 있는 경우 다음을 수행하십시오 [AppMeasurement에서 웹 SDK로 마이그레이션](appmeasurement-to-web-sdk.md) 대신,
* 나중에 Customer Journey Analytics을 사용할 계획이지만 Analytics 구현을 처음부터 웹 SDK 구현으로 바꾸지는 않을 것입니다. 웹 SDK에서 구현을 처음부터 교체하려면 가장 많은 노력이 필요하지만 가장 실행 가능한 장기 구현 아키텍처도 제공합니다. 조직에서 깔끔한 웹 SDK 구현을 수행하려는 경우 다음을 참조하십시오. [Adobe Experience Platform Web SDK를 통해 데이터 수집](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/edge-network/aepwebsdk) Customer Journey Analytics 사용 안내서에서 확인할 수 있습니다.

## 웹 SDK로 마이그레이션하는 데 필요한 단계

다음 단계에는 구체적인 작업 목표가 포함되어 있습니다. 각 단계를 클릭하여 수행 방법에 대한 자세한 지침을 확인하십시오.

+++**1. 데이터 스트림 만들기 및 구성**

Adobe Experience Platform 데이터 수집에서 데이터 스트림을 만듭니다. 이 데이터 스트림으로 데이터를 전송하면 데이터가 Adobe Analytics으로 전달됩니다. 향후에 이와 동일한 데이터스트림이 데이터를 Customer Journey Analytics에 전달합니다.

1. 다음으로 이동 [experience.adobe.com](https://experience.adobe.com) 자격 증명을 사용하여 로그인합니다.
1. 오른쪽 상단의 홈 페이지 또는 제품 선택기를 사용하여 다음 위치로 이동합니다. **[!UICONTROL 데이터 수집]**.
1. 왼쪽 탐색에서 을 선택합니다. **[!UICONTROL 데이터스트림]**.
1. **[!UICONTROL 새 데이터스트림]**&#x200B;을 선택합니다.
1. 원하는 이름을 입력한 다음 을 선택합니다 **[!UICONTROL 저장]**.
1. 데이터 스트림이 생성되면 다음을 선택합니다. **[!UICONTROL 서비스 추가]**.
1. 서비스 드롭다운 메뉴에서 다음을 선택합니다. **[!UICONTROL Adobe Analytics]**.
1. 현재 분석 데이터를 보내는 사이트와 동일한 보고서 세트 ID를 입력합니다. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

![Adobe Analytics 서비스 추가](assets/datastream-rsid.png) {style="border:1px solid lightslategray"}

이제 데이터 스트림이 데이터를 받아서 Adobe Analytics에 전달할 준비가 되었습니다.

+++

+++**2. 태그 속성에 Web SDK 확장 추가**

이 섹션에서는 다음 단계에서 수행되는 대량의 마이그레이션 작업에 대해 태그를 준비합니다.

1. Adobe Experience Platform 인터페이스 왼쪽 상단의 햄버거 아이콘을 클릭한 다음 을 선택합니다 **[!UICONTROL 태그]**.
1. 원하는 태그 속성을 선택합니다.
1. 태그 속성의 왼쪽 탐색에서 을 선택합니다 **[!UICONTROL 확장]**.
1. 선택 **[!UICONTROL 카탈로그]** 사용 가능한 모든 확장 목록을 보려면 상단 근처에 있습니다.
1. 을(를) 검색하고 선택합니다 **[!UICONTROL Adobe Experience Platform 웹 SDK]** 확장을 클릭한 다음 를 클릭합니다 **[!UICONTROL 설치]** 오른쪽.

   ![카탈로그](assets/catalog.png) {style="border:1px solid lightslategray"}

1. 확장 구성 설정이 나타납니다. [데이터스트림] 섹션을 찾아 이전 단계에서 생성한 데이터스트림을 선택합니다.

   ![데이터 스트림 선택](assets/datastream-select.png) {style="border:1px solid lightslategray"}

1. **[!UICONTROL 저장]**&#x200B;을 선택합니다.

이제 태그 속성에 웹 SDK가 설치됩니다.

+++

+++**3. 데이터 개체 데이터 요소 만들기**

데이터 개체 데이터 요소는 Web SDK가 데이터 스트림으로 전송하는 데 사용하는 페이로드를 구성하는 직관적인 프레임워크를 제공합니다. 다음 단계에서 업데이트하는 대부분의 규칙은 이 데이터 요소와 상호 작용합니다.

1. 태그 인터페이스의 왼쪽 탐색에서 을 선택합니다. **[!UICONTROL 데이터 요소]**.
1. 선택 **[!UICONTROL 데이터 요소 추가]**
1. 데이터 요소에 다음 설정을 지정합니다.
   * [!UICONTROL 이름]: &quot;데이터 레이어&quot; 또는 &quot;데이터 개체&quot;와 같이 원하는 모든 항목
   * [!UICONTROL 확장]: [!UICONTROL Adobe Experience Platform 웹 SDK]
   * [!UICONTROL 데이터 요소 유형]: [!UICONTROL 변수]
   * 확인란은 그대로 남아 있을 수 있습니다
1. 오른쪽에서 다음 설정을 선택합니다.
   * 속성 라디오 단추: [!UICONTROL 데이터]
   * 해결 방법: [!UICONTROL Adobe Analytics]
1. **[!UICONTROL 저장]**&#x200B;을 선택합니다.

![데이터 요소 만들기](assets/create-data-element.png) {style="border:1px solid lightslategray"}

이제 태그 속성에 각 규칙을 업데이트하는 데 필요한 모든 것이 있습니다.

+++

+++**4. Analytics 확장 대신 Web SDK 확장을 사용하도록 규칙 업데이트**

이 단계에는 Web SDK로 마이그레이션하는 데 필요한 많은 작업이 포함되어 있으며 구현 작동 방식에 대한 지식이 필요합니다. 다음은 일반적인 태그 규칙을 편집하는 방법의 예입니다. 구현의 모든 태그 규칙을 업데이트하여 Adobe Analytics 확장에 대한 모든 참조를 웹 SDK 확장으로 바꿉니다.

1. 태그 인터페이스의 왼쪽 탐색에서 을 선택합니다. **[!UICONTROL 규칙]**.
1. 편집할 규칙을 선택합니다.
1. 작업 선택 **[!UICONTROL Adobe Analytics - 변수 설정]**
1. 이 규칙 내에 설정된 모든 Analytics 변수를 확인합니다. 드롭다운 메뉴에 설정된 변수와 사용자 지정 코드 내에 설정된 변수를 모두 포함합니다.
1. 변경 [!UICONTROL 작업 구성] 다음 설정으로 이동하십시오.
   * [!UICONTROL 확장]: [!UICONTROL Adobe Experience Platform 웹 SDK]
   * [!UICONTROL 작업 유형]: 변수 업데이트
1. 오른쪽 드롭다운에서 데이터 개체가 선택되었는지 확인합니다.
1. Analytics 변수를 Analytics 확장에서 구성된 것과 동일한 해당 값으로 설정합니다.
   * 태그 인터페이스 내에 설정된 변수는 동일한 값으로 직접 변환할 수 있습니다.
   * 사용자 지정 코드 내에 설정된 문자열 변수는 최소한의 조정이 필요합니다. 를 사용하지 않고 `s` 개체, 사용 `data.__adobe.analytics` 대신, 예를 들어, `s.eVar1` 을(를) (으)로 번역 `data.__adobe.analytics.eVar1`.
   * 사용자 지정 코드의 Analytics 구성 변수 및 메서드 호출에는 수정된 구현 논리가 필요할 수 있습니다. 각각 보기 [변수](/help/implement/vars/overview.md) 을 클릭하여 Web SDK를 사용하여 동일한 기능을 구현하는 방법을 알아봅니다.
1. 웹 SDK 확장을 사용하여 모든 규칙 논리가 복제되면 다음을 선택합니다. **[!UICONTROL 변경 내용 유지]**.
1. Adobe Analytics 확장을 사용하여 값을 설정하는 모든 작업 구성에 대해 이 단계를 반복합니다. 이 단계에는 태그 인터페이스를 사용하여 설정된 변수와 사용자 지정 코드를 사용하여 설정된 변수가 모두 포함됩니다. 사용자 지정 코드 블록은 `s` 아무 곳에나 삽입할 수 있으며

위의 단계는 값을 설정하는 규칙에만 적용됩니다. 다음 단계는 를 사용하는 모든 작업을 대체합니다. [!UICONTROL 작업 구성] [!UICONTROL 비콘 보내기].

1. 비콘을 보내는 규칙을 선택합니다.
1. 작업 선택 **[!UICONTROL Adobe Analytics - 비콘 보내기]**.
1. 의 현재 값을 확인합니다. [!UICONTROL 추적] 오른쪽에 있는 라디오 버튼([`s.t()`](../../vars/functions/t-method.md) 또는 [`s.tl()`](../../vars/functions/tl-method.md)).
1. 변경 [!UICONTROL 작업 구성] 다음 설정으로 이동하십시오.
   * [!UICONTROL 확장]: [!UICONTROL Adobe Experience Platform 웹 SDK]
   * [!UICONTROL 작업 유형]: [!UICONTROL 이벤트 보내기]
1. 오른쪽에서 작업 설정을 다음과 같이 변경합니다.
   * [!UICONTROL 유형]: 대상 `s.t()`, 사용 **[!UICONTROL 웹 웹 페이지 세부 정보 페이지 보기 수]**. 대상 `s.tl()`, 사용 **[!UICONTROL 웹 웹 인터랙션 링크 클릭 수]**. 를 사용하는 경우 [`s.tl()`](../../vars/functions/tl-method.md), 데이터 개체에 다음 필드도 포함해야 합니다. 이들 필드는 아래에 나열되어 있습니다. [!UICONTROL 추가 속성] 다음을 수행할 때 [!UICONTROL 변수 업데이트] 작업 구성:
      * [링크 이름](../../vars/functions/tl-method.md)
      * [링크 유형](../../vars/functions/tl-method.md)
      * [링크 URL](../../vars/config-vars/linkurl.md)
1. **[!UICONTROL 변경사항 유지]**&#x200B;를 선택합니다.
1. Adobe Analytics을 사용하여 비콘을 전송하는 모든 작업 구성에 대해 이 단계를 반복합니다.

+++

+++**5. 업데이트된 규칙 게시**

업데이트된 규칙을 게시하는 것은 태그 구성에 대한 다른 변경 사항과 동일한 워크플로우를 따릅니다.

1. 태그 인터페이스의 왼쪽 탐색에서 을 선택합니다. **[!UICONTROL 게시 플로우]**.
1. 선택 **[!UICONTROL 라이브러리 추가]**.
1. 이 태그 커밋에 &quot;Web SDK로 업그레이드&quot;와 같은 이름을 지정합니다.
1. 선택 **[!UICONTROL 변경된 모든 리소스 추가]**.
1. **[!UICONTROL 저장]**&#x200B;을 선택합니다.
1. 게시 작업 과정에는 작성 중임을 나타내는 주황색 점이 표시됩니다. 점이 녹색으로 바뀌면 개발 환경에서 변경 사항을 사용할 수 있습니다.
1. 개발 환경에서 변경 사항을 테스트하여 모든 규칙이 올바르게 실행되는지, 그리고 데이터 개체가 예상 값으로 채워지는지 확인합니다.
1. 준비가 되면 승인을 위해 라이브러리를 제출하고 스테이징으로 빌드한 다음 최종적으로 승인하고 프로덕션에 게시합니다.

![게시 플로우](assets/publishing-flow.png) {style="border:1px solid lightslategray"}

+++

+++**6. Analytics 확장 비활성화**

태그 구현이 웹 SDK에서 완전히 실행되면 Adobe Analytics 확장을 비활성화할 수 있습니다.

1. 태그 인터페이스의 왼쪽 탐색에서 을 선택합니다. **[!UICONTROL 확장]**.
1. 을(를) 찾아 선택합니다 [!UICONTROL Adobe Analytics] 확장명. 오른쪽에서 을 선택합니다. **[!UICONTROL 사용 안 함]**.
1. 위의 동일한 게시 작업 과정을 따라 의 제거를 게시하십시오. [!UICONTROL Adobe Analytics] 확장명.
1. 프로덕션에서 확장이 비활성화되면 완전히 제거할 수 있습니다. 확장을 선택하고 오른쪽에 있는 세 점 메뉴를 선택한 다음 를 선택합니다 **[!UICONTROL 제거]**.
1. 위의 동일한 게시 작업 과정을 따라 이러한 변경 사항을 프로덕션에 게시하십시오.

+++

이 시점에서 Analytics 구현은 완전히 웹 SDK에 있으며 향후 Customer Journey Analytics으로 이동할 준비가 되어 있습니다.
