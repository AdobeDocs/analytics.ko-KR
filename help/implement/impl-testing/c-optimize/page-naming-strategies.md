---
description: pageName는 읽기 쉽고 직관적인 페이지 식별자와 함께 채워야 합니다.
keywords: Analytics 구현
seo-description: pageName는 읽기 쉽고 직관적인 페이지 식별자와 함께 채워야 합니다.
seo-title: 페이지 이름 지정 전략
solution: Analytics
title: 페이지 이름 지정 전략
topic: 개발자 및 구현
uuid: A 829 D 0 C 7-6 EBF -459 A-B 403-5 E 9 C 05161 E 5 C
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 페이지 이름 지정 전략

pageName는 읽기 쉽고 직관적인 페이지 식별자와 함께 채워야 합니다.

You can determine the best way of populating the *`pageName`* variable by looking at the structure of your website. The methods listed below outline various ways of populating the *`pageName`* variable.

*`pageName`* 변수가 사용자 동작을 식별하는 데 중요하지만, Adobe 에서는 여러 변수를 사용하여 페이지 정보를 표시할 것을 권장합니다. 아래에서 보듯이 가장 좋은 페이지 이름 지정 전략은 사이트 내에서 각 계층에 서로 다른 변수를 사용하는 방법입니다.

* *`channel`* 이 변수를 사용하여 사이트 섹션을 나타낼 수 있습니다.
* *`pageName`* 이 변수를 사용하여 컨텐츠 유형을 표시할 수 있습니다.
* [!UICONTROL 사용자 지정 인사이트] 변수(prop1)는 상세한 컨텐츠에 사용할 수 있습니다.

아래에서 보듯이 상세함의 수준은 속성에 따라 다양합니다.

| 변수 | 상세 수준 | 예 |
|---|---|---|
| Channel | 일반 섹션 | 전자 |
| Prop1 | 하위 섹션 | 스포츠 : 해외 스포츠 |
| PageName | 일반 컨텐츠 설명 | 대출 : 주택 담보 대출 : 이자율 비교 |
| Prop2 | 세부 컨텐츠 설명 | 전자 : 노트북 PC : 상세 사양 : IBM Thinkpad T20 |

사이트의 계층이 많을수록 더 많은 변수를 사용하여 페이지 컨텐츠를 식별해야 합니다. 회사들은 변수 구간을 겹치게 하면 유용한 경우도 있음을 알게 됩니다. 예를 들어 더 자세한 변수에는 보고 있는 제품에 관한 정보 외에도 사이트 섹션 및 하위 섹션에 대한 정보를 포함할 수 있습니다. 이것은 제품 또는 기사가 사이트의 섹션 두 개 이상에 나타나는 경우에 특히 유용합니다.

다음의 페이지 이름 지정 전략에서 *`pageName`* 변수. 구현하기 쉬운 페이지 이름 지정 전략을 선택하기가 쉽지만, 페이지 명명 전략은 모든 [!UICONTROL 경로] 및 [!UICONTROL 페이지] 보고서의 유용성을 결정한다는 점에 주의해야 합니다. 페이지의 이름 지정 방법을 결정할 때는 현명하게 판단하십시오.

## 페이지마다 고유한 이름 {#section_24704CA39E2F4C00ACEAFF39CA0A921B}

가장 좋은 페이지 이름 지정 방법은 조직의 모든 [!DNL Analytics] 사용자가 쉽게 이해할 수 있는 고유한 ID를 각 페이지에 지정하는 것입니다. 페이지 이름의 예에는 홈 페이지, 전자 부서 홈 및 스포츠 : 지역 스포츠 : 고등학교가 있습니다.

대부분의 [!DNL Analytics] 사용자는 사이트에서 페이지가 발견되는 위치와 페이지 용도를 모두 식별하는 데 계층적 페이지 이름이 유용하다는 것을 알게 됩니다. 다음 표에서 다양한 산업 분야에서 사용되는 몇 가지 샘플 페이지 이름을 볼 수 있습니다.

| 전환 | 미디어 | 재무 |
|---|---|---|
| 홈 페이지 | 홈 페이지 | 홈 페이지 |
| 전자 | 기술 | 가계 대출 |
| 전자 : 노트북 PC | 기술: 신제품 | 가계 대출: 이자율 비교 |
| 전자 : 노트북 PC : 제품 페이지 | 기술 : 신제품 : 기사 페이지 | 가계 대출: 이자율 비교 : 10년 고정 |

## 파일 경로(전체 URL이 아님) {#section_37FDCDA00DA84B3D9B8AB4290555FF34}

일부 사이트의 경우 파일 경로가 분명하고 알아보기 쉽습니다. 모든 비즈니스 사용자가 URL을 읽고 파일 경로가 참조하는 페이지를 판단할 수 있습니다. 이와 같은 사이트인 경우, 아래와 같이 서버 측 변수를 사용하여 파일 경로를 *`pageName`*&#x200B;변수에 채울 수 있습니다.

```js
s.pageName="<%= file_path %>"
```

Adobe does not recommend leaving the *`pageName`* blank, (which results in using the full URL of the page) even though you may be tempted to do so. *`pageName`* 변수를 공백으로 두고를 페이지 식별자로 사용하여 다음과 같은 부작용이 *`pageURL`* 발생합니다.

* 페이지의 도메인 및 경로가 동일하게 표시되지 않을 때가 있습니다. 예를 들어 다음 네 가지 URL이 하나의 페이지를 반환합니다.

   * `https://www.mysite.com/index.jsp`
   * `https://www.mysite.com`
   * `https://mysite.com/index.jsp`
   * `https://mysite.com/`
   If the *`pageName`* is left blank, each of these page names would occupy a separate entry in reports.

* 일부 페이지(예: 양식)가 자체에 게시되므로 원래 양식과 결과 출력 간에 구분이 없어집니다.
* 검색 엔진이나 그 밖의 온라인 도구에 의해 페이지가 다른 언어로 변환될 때 페이지의 URL은 검색 엔진의 URL(사이트의 URL이 아님)입니다.

## HTML(document.title) {#section_B99B8F66B0E2410FA7BFE44E6851EB3F}

If you have invested time into making your HTML titles readable and intuitive, you might consider using the same title as the value in the *`pageName`* variable. Adobe recommends using a server-side variable to populate the *`pageName`* rather than using JavaScript's [!DNL document.title]. 일부 브라우저에서는 HTML 제목을 다른 브라우저와 다르게 해석하므로, [!DNL Analytics]가 다른 브라우저에서 다른 페이지 이름을 받을 수 있습니다.

HTML 제목을 사용하는 가장 좋은 방법은 각 페이지의 기존 제목을 별도 변수 또는 컨텐츠 관리 요소로 복사하는 것입니다. 검색 엔진 최적화 또는 다른 목적으로 HTML 제목을 변경하기로 결정하는 경우 [!DNL Analytics] 페이지 이름에 미치는 영향이 없습니다. [!DNL Analytics]에서 페이지 이름을 변경할 경우, 새 페이지가 되므로 연관된 URL과 관계없이 기존 페이지 이름과 연결되지 않습니다.
