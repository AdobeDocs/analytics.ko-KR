---
title: 레퍼러
description: 해당 히트가 사이트 외부에 있는 경우 이전 히트의 URL을 표시합니다.
translation-type: tm+mt
source-git-commit: f18fbd091333523cd9351bfa461a11f0c3f17bef

---


# 레퍼러

&#39;레퍼러&#39; 차원은 방문자가 사이트에 오기 전에 있었던 URL을 보여줍니다. For example, if a visitor clicks a link from `example.com/example-page.html` and arrives on your site, `example.com/example-page.html` is the referrer if it is not defined as part of your domain.

이 차원을 사용하려면 보고서 세트의 내부 URL [필터를](/help/admin/admin/internal-url-filter-admin.md)구성해야 합니다. 내부 URL 필터를 구성하지 않으면 Adobe Analytics는 모든 도메인을 사이트의 내부 도메인으로 간주합니다.

## 차원 속성

* 이 차원은 기본적으로 최신 할당을 사용합니다.
* 이 차원은 기본적으로 방문 후 만료됩니다.
* 이 차원은 (낮은 트래픽) 아래의 차원 값을 그룹화하기 전에 500k 고유 제한을 받습니다. 데이터 웨어하우스에는 고유한 제한이 없습니다.
* 지표에 대한 레퍼러 값이 없는 경우, 이 값은 `Typed/Bookmarked`아래에 그룹화됩니다.
* 이 차원은 일반적으로 방문의 첫 번째 히트에서 설정되지만 중간 방문으로 설정할 수 있습니다.

## 문제 해결

**Q:차원 값으로 표시되는`googleusercontent.com`이유는 무엇입니까?**

A:Google [](https://about.google/) 은 호스팅된 컨텐츠에 `googleusercontent.com` 도메인을 사용합니다. 호스팅된 컨텐츠에는 다음이 포함됩니다.

* **캐시된 페이지**:Google의 스파이더는 오프라인이거나 다른 방법으로 사용할 수 없는 경우 웹 페이지를 지속적으로 크롤링 및 저장합니다. 이러한 캐시된 페이지는 Google의 검색 결과 페이지 중 하나에서 &quot;캐시됨&quot; 링크를 클릭하여 모든 검색 결과 옆에 있습니다. 사용자가 이 링크를 클릭하면 사이트의 원래 컨텐츠를 보면 참조 도메인으로 `googleusercontent.com` 표시됩니다. 이러한 페이지에는 하위 도메인이 `webcache.googleusercontent.com`있습니다.
* **번역된 페이지**:Google은 강력하고 편리한 번역 서비스를 제공합니다. 이 서비스를 사용하여 사이트를 보는 경우 이 서비스가 `googleusercontent.com`시작됩니다. 사용자가 링크를 클릭하여 원래 컨텐츠로 돌아가는 경우 레퍼러 차원은 이 도메인의 URL을 표시합니다. 이러한 페이지에는 하위 도메인이 `translate.googleusercontent.com`있습니다.
