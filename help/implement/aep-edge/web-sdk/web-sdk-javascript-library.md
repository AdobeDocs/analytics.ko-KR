---
title: 웹 SDK JavaScript 라이브러리를 사용하여 Adobe Analytics에 데이터 보내기
description: 깔끔한 웹 SDK 구현으로 시작하여 JavaScript 라이브러리를 사용하여 Adobe Analytics으로 데이터를 전송합니다.
exl-id: 593b63ac-e411-4f88-af7e-78f026269ec0
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '1070'
ht-degree: 18%

---

# 웹 SDK JavaScript 라이브러리를 사용하여 Adobe Analytics에 데이터 보내기

이 구현 경로에는 웹 SDK JavaScript 라이브러리를 사용하여 새 웹 SDK 설치가 포함됩니다. 다른 구현 경로는 별도의 페이지에서 다룹니다.

* [Web SDK 태그 확장](web-sdk-tag-extension.md): Web SDK 태그 확장을 사용하여 새로 설치한 웹 SDK입니다. Adobe Experience Platform 데이터 수집의 태그를 사용하여 구현을 관리한다는 점을 제외하면 웹 SDK JavaScript 라이브러리 접근 방식(이 페이지)과 유사합니다. XDM 스키마에 포함할 일반적인 Analytics 변수를 포함하는 Adobe Analytics ExperienceEvent 필드 그룹이 필요합니다.
* [Analytics 확장을 웹 SDK 확장으로](analytics-extension-to-web-sdk.md): Adobe Analytics 태그 확장에서 웹 SDK 태그 확장으로 원활하게 이동합니다. 이 접근 방법에서는 조직에서 Customer Journey Analytics과 같은 Adobe Experience Platform 서비스를 사용할 준비가 될 때까지 XDM을 사용할 필요가 없습니다. `data` 개체 대신 `xdm` 개체를 사용하여 Adobe으로 데이터를 보냅니다.
* [웹 SDK JavaScript 라이브러리로 AppMeasurement](appmeasurement-to-web-sdk.md): 태그를 사용하지 않는 경우를 제외하고 웹 SDK으로 마이그레이션하는 유연하고 체계적인 방법입니다. 대신 수동으로 Adobe Analytics 데이터 수집 라이브러리(`AppMeasurement.js`)를 제거하고 웹 SDK JavaScript 라이브러리(`alloy.js`)로 바꿀 수 있습니다.

## 이 구현 경로의 장단점

웹 SDK JavaScript 라이브러리를 사용하여 Adobe Analytics으로 데이터를 전송하는 데에는 장점과 단점이 모두 있습니다. 각 옵션을 신중히 평가하여 조직에 가장 적합한 접근 방식을 결정하십시오.

| 장점 | 단점 |
| --- | --- |
| <ul><li>**직접 접근 방식**: 이 구현 경로는 기존 Adobe Analytics 구현을 이동하는 접근 방식보다 더 간단합니다. 현재 Adobe Analytics 구현에 대해 걱정할 필요가 없는 경우 해당 웹 SDK XDM 필드를 채웁니다.</li><li>**미리 정의된 스키마**: 조직에 고유한 스키마가 필요하지 않은 경우 Adobe Analytics에 맞게 구성된 스키마를 사용하면 됩니다. 이 개념은 Customer Journey Analytics으로 이동하는 경우에도 적용됩니다. prop 및 eVar의 개념은 Customer Journey Analytics에 적용되지 않지만, prop 및 eVar를 간단한 사용자 지정 차원으로 계속 사용할 수 있습니다.</li></ul> | <ul><li>**구현을 변경하려면 개발자의 개입이 필요합니다**: 웹 SDK 구현을 변경하려면 개발 팀과 함께 사이트에서 코드를 편집해야 합니다. [웹 SDK 태그 확장](web-sdk-tag-extension.md)을 사용하는 방법은 이러한 단점을 방지합니다.</li><li>**특정 스키마를 사용하여 잠김**: 조직이 Customer Journey Analytics으로 이동할 때 Adobe Analytics 스키마를 계속 사용하도록 선택하거나 별도의 데이터 집합인 조직의 스키마로 마이그레이션해야 합니다. 조직에서 Customer Journey Analytics으로 이동할 때 Adobe Analytics 스키마와 별도의 데이터 세트로 마이그레이션하는 것을 모두 방지하려면 Adobe에서 다음 두 가지 방법 중 하나를 권장합니다.</li><ul><li>`data` 개체 사용: `data` 개체를 사용하면 XDM 스키마를 준수하지 않고 Adobe Analytics으로 데이터를 보낼 수 있습니다. 조직의 스키마가 만들어지면 데이터 스트림 매핑을 사용하여 `data` 개체 필드를 XDM에 매핑할 수 있습니다. [Analytics 확장을 Web SDK 확장](analytics-extension-to-web-sdk.md)으로, [AppMeasurement을 Web SDK JavaScript 라이브러리로](appmeasurement-to-web-sdk.md)에서 모두 이 `data` 개체를 사용합니다.</li><li>Adobe Analytics 전체 건너뛰기: 웹 SDK을 구현하는 경우 Customer Journey Analytics에서 사용할 수 있도록 해당 데이터를 Adobe Experience Platform의 데이터 세트로 전송할 수 있습니다. 원하는 스키마를 사용할 수 있습니다. Adobe Analytics은 이 워크플로에 전혀 포함되지 않으므로 Adobe Analytics ExperienceEvent 필드 그룹이 필요하지 않습니다. 이 방법은 기술적인 부채를 최소한으로 발생시키지만 Adobe Analytics을 완전히 배제시킵니다.</li></ul></ul> |

>[!IMPORTANT]
>
>이 구현 방법을 사용하려면 Adobe Analytics에 대해 구성된 스키마를 사용해야 합니다. 향후 조직에서 Customer Journey Analytics을 사용하여 자체 스키마를 사용하려는 경우 Adobe Analytics 스키마를 사용하면 데이터 관리자나 설계자에게 혼란이 발생할 수 있습니다. 이러한 장애를 완화하는 몇 가지 옵션이 있습니다.
>
>* CJA에서 Adobe Analytics 스키마를 사용할 수 있습니다. CJA에는 prop 또는 eVar의 개념이 없으며 다른 스키마 필드로 처리됩니다. 또한 CJA에서 Adobe Analytics 스키마를 사용하면 Adobe Journey Optimizer 또는 Real-Time Customer Data Platform과 같은 다른 플랫폼 서비스를 사용하는 것이 더 어려울 수 있습니다.
>* 마이그레이션 워크플로와 유사한 데이터 개체를 사용할 수 있습니다. 데이터 개체를 사용하려면 각 데이터 개체 필드를 XDM 스키마 필드에 매핑해야 합니다.
>* Adobe Analytics 구현을 완전히 건너뛰고 고유한 스키마를 사용하여 Adobe Experience Platform으로 데이터를 전송할 수 있습니다. 이 접근 방식은 장기적으로 이상적이며 조직에서 Customer Journey Analytics을 사용할 수 있습니다.

## 웹 SDK JavaScript 라이브러리를 구현하는 데 필요한 단계

구현 작업에 대한 개략적인 개요:

![이 섹션에 설명된 대로 Web SDK 워크플로를 사용하여 Adobe Analytics을 구현하는 방법입니다.](../../assets/websdk-annotated.png)

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
<td> 4</td>
<td><b>미리 빌드된 독립형 버전을 설치합니다</b>. 페이지에서 직접 CDN의 라이브러리(<code>alloy.js</code>)를 참조하거나 자체 인프라에서 다운로드하여 호스팅할 수 있습니다. 또는 NPM 패키지를 사용할 수 있습니다.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/web-sdk/install/library.html?lang=ko">미리 빌드된 독립형 버전 설치</a> 및 <a href="https://experienceleague.adobe.com/docs/experience-platform/web-sdk/install/npm.html?lang=ko">NPM 패키지 사용</a></td>
</tr>

<tr>
<td>5</td>
<td><b>데이터스트림을 구성합니다</b>. 데이터스트림은 Adobe Experience Platform Web SDK 구현 시 서버측 구성을 나타냅니다.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=ko">데이터스트림 구성<a></td> 
</tr>

<td>6</td>
<td>데이터스트림에 <b>Adobe Analytics 서비스를 추가</b>합니다. 해당 서비스는 데이터가 Adobe Analytics으로 전송되는지 여부와 전송 방법, 구체적으로 어떤 보고서 세트를 통해 전송되는지 여부를 제어합니다.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=ko#analytics">데이터스트림에 Adobe Analytics 서비스 추가</a></td>
</tr>

<tr>
<td>7</td>
<td><b>Web SDK를 구성합니다</b>. 4단계에서 설치한 라이브러리가 데이터 스트림 ID(이전에는 Edge 구성 ID(<code>datastreamId</code>)라고 함), 조직 ID(<code>orgId</code>) 및 기타 사용 가능한 옵션으로 올바르게 구성되었는지 확인합니다. 변수의 적절한 매핑을 확인합니다. </td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/web-sdk/commands/configure/overview.html?lang=ko">웹 SDK 구성</a><br/><a href="../xdm-var-mapping.md">XDM 개체 변수 매핑</a></td>
</tr>

<tr>
<td>8</td>
<td><b>명령을 실행</b>하거나 <b>이벤트를 추적</b>합니다. 베이스 코드가 웹 페이지에 구현되면 SDK를 사용하여 명령 실행 및 이벤트 추적을 시작할 수 있습니다.
</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/web-sdk/commands/sendevent/overview.html?lang=ko">이벤트 보내기</a></td>
</tr>

<tr>
<td>9</td><td>프로덕션으로 푸시하기 전에 <b>구현을 확장하고 유효성을 검사</b>합니다.</td><td></td> 
</tr>
</table>
