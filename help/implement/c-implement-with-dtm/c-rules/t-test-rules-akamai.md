---
description: Akamai 호스팅을 사용하는 경우 콘솔에서 게시 취소된 규칙을 테스트합니다.
keywords: 다이내믹 태그 관리;규칙;전환기 플러그인;akamai;test akamai;게시 취소된 규칙;테스트 게시 취소된 규칙;디버그 규칙
seo-description: Akamai 호스팅을 사용하는 경우 콘솔에서 게시 취소된 규칙을 테스트합니다.
seo-title: Akamai 호스팅을 위한 게시되지 않은 규칙 테스트
solution: Experience Cloud,Analytics,Target,다이내믹 태그 관리
title: Akamai 호스팅을 위한 게시되지 않은 규칙 테스트
uuid: 979e3d74-8d96-47d0-b581-cf5371248434
translation-type: tm+mt
source-git-commit: e060fb745d611f37f28708b3fe103c1191aa483b

---


# Akamai 호스팅을 위한 게시되지 않은 규칙 테스트

Akamai 호스팅을 사용하는 경우 콘솔에서 게시 취소된 규칙을 테스트합니다.

이때 Switcher 플러그인을 이용하면 가장 쉽게 테스트할 수 있습니다. 자세한 내용은 다이내믹 태그 관리 제품 설명서의 [Search Discovery 플러그인](https://marketing.adobe.com/resources/help/en_US/dtm/search_discovery_plugins.html)을 참조하십시오.

다음 단계는 Switcher 플러그인을 사용하지 않고 테스트하는 방법을 보여 줍니다.

1. 사이트에서 웹 콘솔에 액세스하고 `localStorage.setItem('sdsat_stagingLibrary', true)`.
1. Press **[!UICONTROL Enter]**.
1. 을 `_satellite.setDebug(true)`입력한 다음 Enter 키를 **[!UICONTROL 누릅니다]**.
1. 페이지를 새로 고칩니다.

   이 작업으로 스테이징 라이브러리가 로드되고 디버거가 시작되어, 페이지에서 실행되는 모든 사용 가능한 (게시된 / 게시되지 않은) 규칙에 대한 세부 정보가 표시됩니다.
1. 완료되면 Enter `localStorage.setItem('sdsat_stagingLibrary', false)`키를 **[!UICONTROL 누릅니다]**.

   단계 결과