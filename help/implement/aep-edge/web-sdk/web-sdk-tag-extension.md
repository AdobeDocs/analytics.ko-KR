---
title: 웹 SDK 태그 확장을 사용하여 Adobe Analytics에 데이터 보내기
description: XDM 및 Adobe Experience Platform ExperienceEvent 필드 그룹을 사용하여 Adobe Analytics에 데이터를 전송하기 위한 Adobe Analytics 데이터 수집의 깔끔한 구현으로 시작합니다.
exl-id: 235b3d68-92dd-4ca4-8889-1e1f2d83f47e
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '1040'
ht-degree: 16%

---

# 웹 SDK 태그 확장을 사용하여 Adobe Analytics에 데이터 보내기

이 구현 경로에는 Adobe Experience Platform 데이터 수집의 태그를 사용하는 새로운 웹 SDK 설치가 포함됩니다. 다른 구현 경로는 별도의 페이지에서 다룹니다.

* [웹 SDK JavaScript 라이브러리](web-sdk-javascript-library.md): 웹 SDK JavaScript 라이브러리(`alloy.js`)를 사용하여 새로 설치한 웹 SDK 설치입니다. 태그 UI를 사용하는 대신 구현을 직접 관리한다는 점을 제외하면 웹 SDK 태그 확장 접근 방식 (이 페이지)과 유사합니다. XDM 스키마에 포함할 일반적인 Analytics 변수를 포함하는 Adobe Analytics ExperienceEvent 필드 그룹이 필요합니다.
* [Analytics 확장을 웹 SDK 확장으로](analytics-extension-to-web-sdk.md): Adobe Analytics 태그 확장에서 웹 SDK 태그 확장으로 원활하게 이동합니다. 이 접근 방법에서는 조직에서 Customer Journey Analytics과 같은 Adobe Experience Platform 서비스를 사용할 준비가 될 때까지 XDM을 사용할 필요가 없습니다. `data` 개체 대신 `xdm` 개체를 사용하여 Adobe으로 데이터를 보냅니다.
* [웹 SDK JavaScript 라이브러리로 AppMeasurement](appmeasurement-to-web-sdk.md): 태그를 사용하지 않는 경우를 제외하고 웹 SDK으로 마이그레이션하는 유연하고 체계적인 방법입니다. 대신 수동으로 Adobe Analytics 데이터 수집 라이브러리(`AppMeasurement.js`)를 제거하고 웹 SDK JavaScript 라이브러리(`alloy.js`)로 바꿉니다.

## 이 구현 경로의 장단점

Web SDK 확장을 사용하여 Adobe Analytics에 데이터를 전송하는 데에는 장점과 단점이 모두 있습니다. 각 옵션을 신중히 평가하여 조직에 가장 적합한 접근 방식을 결정하십시오.

| 장점 | 단점 |
| --- | --- |
| <ul><li>**가장 직접적인 방법**: 이 구현 경로는 가장 간단하며 일반적으로 새 웹 SDK 구현에 권장되는 경로입니다. 현재 Adobe Analytics 구현에 대해 걱정할 필요가 없는 경우 해당 웹 SDK XDM 필드를 채웁니다.</li><li>**미리 정의된 스키마**: 조직에 고유한 스키마가 필요하지 않은 경우 Adobe Analytics에 맞게 구성된 스키마를 사용하면 됩니다. 이 개념은 Customer Journey Analytics으로 이동하는 경우에도 적용됩니다. prop 및 eVar의 개념은 Customer Journey Analytics에 적용되지 않지만, prop 및 eVar를 간단한 사용자 지정 차원으로 계속 사용할 수 있습니다.</li><li>**개발자 개입 없이 태그 관리**: 태그를 사용하면 개발자에게 구현에 대한 코드 변경을 요청하지 않고도 구현을 관리할 수 있습니다. 개발자가 태그 로더 스크립트를 설치하고 데이터 수집 방법에 대한 모든 권한을 갖습니다.</li></ul> | <ul><li>**특정 스키마를 사용하여 잠김**: 조직이 Customer Journey Analytics으로 이동할 때 Adobe Analytics 스키마를 계속 사용하도록 선택하거나 별도의 데이터 집합인 조직의 스키마로 마이그레이션해야 합니다. 조직에서 Customer Journey Analytics으로 이동할 때 Adobe Analytics 스키마와 별도의 데이터 세트로 마이그레이션하는 것을 모두 방지하려면 Adobe에서 다음 두 가지 방법 중 하나를 권장합니다.<ul><li>`data` 개체 사용: `data` 개체를 사용하면 XDM 스키마를 준수하지 않고 Adobe Analytics으로 데이터를 보낼 수 있습니다. 조직의 스키마가 만들어지면 데이터 스트림 매핑을 사용하여 `data` 개체 필드를 XDM에 매핑할 수 있습니다. [Analytics 확장을 Web SDK 확장](analytics-extension-to-web-sdk.md)으로, [AppMeasurement을 Web SDK JavaScript 라이브러리로](appmeasurement-to-web-sdk.md)에서 모두 이 `data` 개체를 사용합니다.</li><li>Adobe Analytics 전체 건너뛰기: 웹 SDK을 구현하는 경우 Customer Journey Analytics에서 사용할 수 있도록 해당 데이터를 Adobe Experience Platform의 데이터 세트로 전송할 수 있습니다. 원하는 스키마를 사용할 수 있습니다. Adobe Analytics은 이 워크플로에 전혀 포함되지 않으므로 Adobe Analytics ExperienceEvent 필드 그룹이 필요하지 않습니다. 이 방법은 기술적인 부채를 최소한으로 발생시키지만 Adobe Analytics을 완전히 배제시킵니다.</li></ul></ul> |

>[!IMPORTANT]
>
>이 구현 방법을 사용하려면 Adobe Analytics에 대해 구성된 스키마를 사용해야 합니다. 향후 조직에서 Customer Journey Analytics을 사용하여 자체 스키마를 사용하려는 경우 Adobe Analytics 스키마를 사용하면 데이터 관리자나 설계자에게 혼란이 발생할 수 있습니다. 이러한 장애를 완화하는 몇 가지 옵션이 있습니다.
>
>* CJA에서 Adobe Analytics 스키마를 사용할 수 있습니다. CJA에는 prop 또는 eVar의 개념이 없으며 다른 스키마 필드로 처리됩니다. 또한 CJA에서 Adobe Analytics 스키마를 사용하면 Adobe Journey Optimizer 또는 Real-Time Customer Data Platform과 같은 다른 플랫폼 서비스를 사용하는 것이 더 어려울 수 있습니다.
>* 마이그레이션 워크플로와 유사한 데이터 개체를 사용할 수 있습니다. 데이터 개체를 사용하려면 각 데이터 개체 필드를 XDM 스키마 필드에 매핑해야 합니다.
>* Adobe Analytics 구현을 완전히 건너뛰고 고유한 스키마를 사용하여 Adobe Experience Platform으로 데이터를 전송할 수 있습니다. 이 접근 방식은 장기적으로 이상적이며 조직에서 Customer Journey Analytics을 사용할 수 있습니다.

## 웹 SDK 태그 확장을 구현하는 데 필요한 단계

구현 작업에 대한 개략적인 개요:

![이 섹션에 설명된 대로 Web SDK 확장 워크플로를 사용하여 Adobe Analytics을 구현하는 방법입니다.](../../assets/websdk-extension-annotated.png)

<table style="width:100%">

<tr>
<th style="width:5%"></th><th style="width:60%"><b>작업</b></th><th style="width:35%"><b>추가 정보</b></th>
</tr>

<tr>
<td>1</td>
<td><b>보고서 세트를 정의</b>했는지 확인합니다.</td>
<td><a href="/help/admin/tools/manage-rs/report-suites-admin.md">보고서 세트 관리자</a></td>
</tr>

<tr>
<td>2</td>
<td><b>스키마를 설정합니다</b>. Adobe Experience Platform을 활용하는 애플리케이션 전체에서 사용할 데이터 수집을 표준화하기 위해, Adobe는 개방적이고 공개적으로 문서화된 표준인 XDM(경험 데이터 모델)을 만들었습니다.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=ko">스키마 UI 개요</a></td>
</tr>

<tr>
<td>3</td>
<td>웹 사이트의 데이터 추적을 관리할 <b>데이터 계층을 만듭니다</b>.</td>
<td><a href="../../prepare/data-layer.md">데이터 계층 만들기</a></td>
</tr>

<tr>
<td>4</td>
<td><b>데이터스트림을 구성합니다</b>. 데이터스트림은 Adobe Experience Platform Web SDK 구현 시 서버측 구성을 나타냅니다.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=ko">데이터스트림 구성<a></td> 
</tr>

<tr>
<td>5</td> 
<td>데이터스트림에 <b>Adobe Analytics 서비스를 추가</b>합니다. 해당 서비스는 데이터가 Adobe Analytics으로 전송되는지 여부와 전송 방법, 구체적으로 어떤 보고서 세트를 통해 전송되는지 여부를 제어합니다.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=ko#analytics">데이터스트림에 Adobe Analytics 서비스 추가</a></td>
</tr>

<tr>
<td>6</td>
<td><b>태그 속성을 만듭니다</b>. 속성은 태그 관리 데이터를 참조하는 데 사용하는 중요한 컨테이너입니다.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html?lang=ko#for-web">웹용 태그 속성 만들기 또는 구성</a></td>
</tr>

<tr>
<td>7</td> 
<td>태그 속성에서 <b>Web SDK 확장을 설치하고 구성</b>합니다. 4단계에서 구성한 데이터스트림으로 데이터를 전송하도록 Web SDK 확장을 구성합니다.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/sdk/overview.html?lang=ko-KR">Adobe Experience Platform Web SDK 확장 개요</a></td>
</tr>

<tr>
<td>8</td>
<td><b>반복하고, 유효성을 검사하고, 프로덕션에 게시합니다</b>. 웹 사이트 페이지에 태그 속성을 포함하는 코드를 포함합니다. 그런 다음 데이터 요소, 규칙 등을 사용하여 구현을 사용자 정의하십시오.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/publish/environments/environments.html?lang=ko#embed-code">포함 코드</a><br/><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/publish/overview.html?lang=ko">게시 개요</a></td>
</tr>

</table>
