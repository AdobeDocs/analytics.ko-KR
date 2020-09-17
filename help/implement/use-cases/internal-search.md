---
title: 내부 검색어 캡처
description: 사용자 지정 변수를 사용하여 내부 검색어를 캡처합니다.
translation-type: tm+mt
source-git-commit: a94b8e090b9a3c75a57fd396cac8486bba2e5d79
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 2%

---


# 내부 검색어 캡처

내부 검색 보고는 많은 조직에 없어서는 안 될 사항이며, Adobe Analytics과 함께 사용해서는 안 되는 차원이 아닙니다. 그러나 구현 작업을 최소화하면 내부 검색어 보고를 손쉽게 캡처할 수 있습니다.

## 전제 조건

[개발 구현 유효성을 확인하고 프로덕션에 게시](../launch/validate-publish-prod.md):이 페이지에서는 기본적인 작업 구현을 가지고 있고 Adobe 디버거에서 Adobe Analytics 이미지 요청을 볼 수 있다고 가정합니다.

## 내부 검색을 수용할 eVar 만들기

전환 [변수 관리에](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) 따라 내부 검색을 위한 새 eVar을 만듭니다. 쉽게 인식할 수 있는 이름(예: &quot;내부 검색어&quot;)을 eVar에 지정하고 조직의 [솔루션 디자인 문서에 새 eVar을 기록합니다](../prepare/solution-design.md).

## 내부 검색 키워드 결정

대부분의 내부 검색은 쿼리 문자열을 사용하여 페이지 간에 키워드 데이터를 전달합니다. 사이트의 내부 검색을 사용하고 검색 결과 페이지의 URL을 확인합니다.

`https://example.com/search.html?q=kittens`

사이트의 내부 검색에서 URL을 사용하지 않는 경우 데이터 레이어 또는 쿠키와 같은 다른 위치에서 검색어를 찾습니다. 내부 검색어를 찾을 위치를 잘 모르는 경우 사이트 개발 팀과 함께 작업할 수 있습니다.

## 데이터 요소에 쿼리 문자열 매개 변수 지정

Follow [Map data layer objects to data elements](../launch/layer-to-elements.md). 데이터 요소 **[!UICONTROL 유형을]**&#x200B;선택할 때 **[!UICONTROL JavaScript 변수]** 대신 **[!UICONTROL 쿼리 문자열 매개 변수]**&#x200B;를선택합니다. 텍스트 필드에 원하는 쿼리 문자열 매개 변수(일반적으로 `q`)를 입력합니다.

## 데이터 요소를 eVar에 매핑

Follow [Map Launch data elements to Analytics variables](../launch/elements-to-variable.md). 보고서 세트 설정에서 만든 것과 동일한 eVar을 선택해야 합니다.

## 시작 배포 프로세스 시작

Follow [Deploy an Analytics implementation to a development environment](../launch/deploy-dev.md). 개발 환경에서 작동 중임을 확인한 후 개발 구현 [의 유효성을 확인하고 프로덕션에 게시할 수 있습니다](../launch/validate-publish-prod.md).

## 작업 공간에서 보고

구현을 통해 데이터를 수집하는 시간을 지정한 다음 Analysis Workspace에서 차원 사용을 시작할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [experiencecloud.adobe.com](https://experiencecloud.adobe.com)에 로그인합니다.
2. Adobe Analytics에 자동으로 로그인하지 않은 경우 오른쪽 상단의 9 그리드 아이콘을 클릭하고 **[!UICONTROL 분석을 선택합니다]**.
3. 작업 **[!UICONTROL 공간]** 탭을 클릭하고 새 프로젝트를 만듭니다.
4. Dimension 아래에 만든 eVar 이름을 찾아 작업 영역 캔버스로 드래그합니다.
