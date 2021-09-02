---
title: 내부 검색어 캡처
description: 사용자 지정 변수를 사용하여 내부 검색어를 캡처합니다.
source-git-commit: 3986084eaab81842b6ea0dbabc7bdb78e39f887a
workflow-type: ht
source-wordcount: '372'
ht-degree: 100%

---


# 내부 검색어 캡처

내부 검색 보고는 많은 조직에 필수적이며 Adobe Analytics에서 기본 차원이 아닙니다. 그러나 최소한의 구현 노력으로 내부 검색어 보고를 쉽게 캡처할 수 있습니다.

## 전제 조건

[개발 구현 유효성 검사 및 프로덕션에 퍼블리싱](../launch/validate-publish-prod.md): 이 페이지는 기본 작업 구현이 있고 Adobe 디버거에서 Adobe Analytics 이미지 요청을 본다고 가정한 내용입니다.

## 내부 검색에 맞는 eVar 만들기

새로운 내부 검색 전용 eVar을 만들려면 [전환 변수 관리](/help/admin/admin/conversion-var-admin/conversion-var-admin.md)를 따르십시오. eVar에 쉽게 인식 가능한 이름(예: &quot;내부 검색어&quot;)을 지정하고 새로운 eVar을 조직의 [솔루션 디자인 문서](../prepare/solution-design.md)에 기록하십시오.

## 내부 검색 키워드 결정

대부분의 내부 검색은 쿼리 문자열을 사용하여 페이지 간 키워드 데이터를 전달합니다. 사이트의 내부 검색을 사용하고 검색 결과 페이지의 URL을 확인합니다.

`https://example.com/search.html?q=kittens`

사이트의 내부 검색에서 URL을 사용하지 않는 경우 데이터 레이어 또는 쿠키 등 다른 위치에서 검색어를 찾아봅니다. 내부 검색어를 어디에서 찾아야 할지 모르겠는 경우 사이트 개발 팀의 도움을 구합니다.

## 쿼리 문자열 매개 변수를 데이터 요소에 할당합니다.

Follow [데이터 레이어 개체를 데이터 요소에 매핑합니다](../launch/layer-to-elements.md). **[!UICONTROL 데이터 요소 유형]**&#x200B;을 선택할 때 **[!UICONTROL JavaScript 변수]**&#x200B;가 아닌 **[!UICONTROL 쿼리 문자열 매개 변수]**&#x200B;를 선택합니다. 원하는 쿼리 문자열 매개 변수(일반적으로 `q`)를 텍스트 필드에 넣습니다.

## eVar에 데이터 요소 매핑

[Analytics 변수에 데이터 요소 매핑](../launch/elements-to-variable.md)을 따르십시오. 이때, 보고서 세트 설정에서 만든 동일한 eVar을 선택해야 합니다.

## 태그 배포 시작

[개발 환경에 Analytics 구현 배포](../launch/deploy-dev.md)를 따르십시오. 개발에서 구현이 작동하는 것을 확인했으면 [개발 구현 유효성 검사 및 프로덕션에 퍼블리싱](../launch/validate-publish-prod.md)을 수행할 수 있습니다.

## Workspace에서 보고

구현이 데이터를 수집하는 동안 잠시 기다린 뒤, Analysis Workspace에서 차원 사용을 시작할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [experiencecloud.adobe.com](https://experiencecloud.adobe.com)에 로그인합니다.
2. 자동으로 Adobe Analytics에 로그인되지 않는 경우 오른쪽 상단의 9 그리드 아이콘을 클릭한 다음 **[!UICONTROL Analytics]**&#x200B;를 선택합니다.
3. **[!UICONTROL Workspace]** 탭을 클릭하고 새 프로젝트를 만듭니다.
4. 차원에서 만든 eVar의 이름을 찾아 작업 영역 캔버스로 드래그합니다.
