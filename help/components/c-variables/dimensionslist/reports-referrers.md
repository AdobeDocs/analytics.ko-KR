---
title: 레퍼러
description: 이전 히트가 사이트 외부에 있는 경우 해당 히트의 URL을 표시합니다.
translation-type: ht
source-git-commit: f18fbd091333523cd9351bfa461a11f0c3f17bef

---


# 레퍼러

&#39;레퍼러&#39; 차원은 방문자가 사이트를 방문하기 전에 있었던 URL을 표시합니다. 예를 들어 방문자가 `example.com/example-page.html`에서 링크를 클릭하여 사이트를 방문하는 경우 `example.com/example-page.html`가 도메인의 일부로 정의되어 있지 않으면 레퍼러입니다.

이 차원을 사용하려면 보고서 세트의 [내부 URL 필터](/help/admin/admin/internal-url-filter-admin.md)를 구성해야 합니다. 내부 URL 필터를 구성하지 않으면 Adobe Analytics는 모든 도메인을 사이트의 내부로 간주합니다.

## 차원 속성

* 이 차원은 기본적으로 가장 최근 할당을 사용합니다.
* 이 차원은 기본적으로 방문 후 만료됩니다.
* 이 차원은 차원 값을 (낮은 트래픽)에 그룹화하기 전에 500k의 고유 제한을 따릅니다. Data Warehouse에는 고유한 제한이 없습니다.
* 지표에 대한 레퍼러 값이 없는 경우 `Typed/Bookmarked` 아래에 그룹화됩니다.
* 이 차원은 일반적으로 첫 번째 방문 히트에서 설정되지만 중간 방문에서 설정할 수 있습니다.

## 문제 해결

**Q:`googleusercontent.com`이 차원 값으로 표시되는 이유는 무엇입니까?**

A: [Google](https://about.google/)은 호스팅된 해당 컨텐츠에 `googleusercontent.com` 도메인을 사용합니다. 호스팅된 컨텐츠에 포함된 내용은 다음과 같습니다.

* **캐시된 페이지**: Google의 스파이더는 웹을 지속적으로 크롤링하고 웹 페이지를 오프라인으로 가져오는 경우 해당 페이지를 저장하고, 그렇지 않은 경우 저장할 수 없습니다. 이렇게 캐시된 페이지는 Google의 검색 결과 페이지 중 하나에서 &quot;캐시됨&quot; 링크를 클릭하여 모든 검색 결과 옆에 표시됩니다. 사용자가 이 링크를 클릭하여 사이트에서 원래 컨텐츠를 볼 때 참조 도메인으로 `googleusercontent.com`이 나열됩니다. 이러한 페이지에는 하위 도메인 `webcache.googleusercontent.com`이 있습니다.
* **번역된 페이지**: Google은 강력하고 편리한 번역 서비스를 제공합니다. 이 서비스를 사용하여 사이트를 보는 경우 `googleusercontent.com`에서 사이트가 전송됩니다. 사용자가 링크를 클릭하여 원래 컨텐츠로 돌아가는 경우 레퍼러 차원은 이 도메인의 URL을 표시합니다. 이러한 페이지에는 하위 도메인 `translate.googleusercontent.com`이 있습니다.
