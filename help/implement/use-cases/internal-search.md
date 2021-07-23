---
title: 내부 검색어 캡처
description: 사용자 지정 변수를 사용하여 내부 검색어를 캡처합니다.
source-git-commit: 3986084eaab81842b6ea0dbabc7bdb78e39f887a
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 2%

---


# 내부 검색어 캡처

내부 검색 보고는 많은 조직에 중요하며 Adobe Analytics을 사용하는 기본 차원은 아닙니다. 그러나 최소한의 구현 노력으로 내부 검색어 보고를 쉽게 캡처할 수 있습니다.

## 사전 요구 사항

[개발 구현을 확인하고 프로덕션에 게시](../launch/validate-publish-prod.md): 이 페이지에서는 사용자가 기본적인 작업 구현을 가지고 있고 Adobe 디버거에서 Adobe Analytics 이미지 요청을 볼 수 있다고 가정합니다.

## 내부 검색을 수용할 eVar 만들기

[전환 변수 admin](/help/admin/admin/conversion-var-admin/conversion-var-admin.md)에 따라 내부 검색을 위한 새 eVar을 만듭니다. eVar을 쉽게 인식할 수 있는 이름(예: &quot;내부 검색어&quot;)을 지정하고 조직의 [솔루션 디자인 문서](../prepare/solution-design.md)에 새 eVar을 기록합니다.

## 내부 검색 키워드 결정

대부분의 내부 검색은 쿼리 문자열을 사용하여 페이지 간에 키워드 데이터를 전달합니다. 사이트의 내부 검색을 사용하고 검색 결과 페이지에서 URL을 확인합니다.

`https://example.com/search.html?q=kittens`

사이트의 내부 검색에서 URL을 사용하지 않는 경우 데이터 계층이나 쿠키와 같은 다른 위치에서 검색어를 찾습니다. 내부 검색어를 찾을 위치를 모를 경우 사이트 개발 팀과 작업합니다.

## 데이터 요소에 쿼리 문자열 매개 변수 할당

[데이터 레이어 개체를 데이터 요소에 매핑](../launch/layer-to-elements.md)을 따릅니다. **[!UICONTROL 데이터 요소 유형]**&#x200B;을 선택하는 경우 **[!UICONTROL JavaScript 변수]** 대신 **[!UICONTROL 쿼리 문자열 매개 변수]**&#x200B;를 선택합니다. 원하는 쿼리 문자열 매개 변수(일반적으로 `q`)를 텍스트 필드에 입력합니다.

## 데이터 요소를 eVar에 매핑

[데이터 요소를 Analytics 변수에 매핑](../launch/elements-to-variable.md)을 따르십시오. 보고서 세트 설정에서 만든 것과 동일한 eVar을 선택해야 합니다.

## 태그 배포 시작

[개발 환경에 Analytics 구현 배포](../launch/deploy-dev.md)를 따르십시오. 개발 환경에서 작동 중인지 확인했으면 [개발 구현의 유효성을 검사하고 프로덕션](../launch/validate-publish-prod.md)에 게시할 수 있습니다.

## Workspace에서 보고

구현에 데이터를 수집할 시간을 제공한 다음 Analysis Workspace에서 차원 사용을 시작할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [experiencecloud.adobe.com](https://experiencecloud.adobe.com)에 로그인합니다.
2. Adobe Analytics에 자동으로 로그인하지 않은 경우 오른쪽 상단의 9격자 아이콘을 클릭하고 **[!UICONTROL Analytics]**&#x200B;을(를) 선택합니다.
3. **[!UICONTROL 작업 공간]** 탭을 클릭하고 새 프로젝트를 만듭니다.
4. Dimension 아래에서 만든 eVar 이름을 찾아 작업 공간 캔버스로 드래그합니다.
