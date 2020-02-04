---
description: Akamai 호스팅을 사용하는 경우 콘솔에서 게시 취소된 규칙을 테스트합니다.
keywords: Dynamic Tag Management;rule;switcher plug-in;akamai;test akamai;unpublished rules;test unpublished rules;debug rule
solution: Experience Cloud,Analytics,Target,Dynamic Tag Management
title: Akamai 호스팅을 위한 게시되지 않은 규칙 테스트
uuid: 979e3d74-8d96-47d0-b581-cf5371248434
translation-type: tm+mt
source-git-commit: 2ffa989156dd9bc4f6ef9a216e8c06425cc39440

---


# Akamai 호스팅을 위한 게시되지 않은 규칙 테스트

Akamai 호스팅을 사용하는 경우 콘솔에서 게시 취소된 규칙을 테스트합니다.

Switcher 플러그인을 사용하면 손쉽게 테스트할 수 있습니다. See [Search Discovery plug-ins](https://marketing.adobe.com/resources/help/en_US/dtm/search_discovery_plugins.html) in the Dynamic Tag Management Product Documentation for more information.

다음 단계에서는 전환기 플러그인을 사용하지 않고 테스트하는 방법을 보여 줍니다.

1. 사이트에서 웹 콘솔에 액세스하고 `localStorage.setItem('sdsat_stagingLibrary', true)`.
1. **[!UICONTROL Enter]**키를 누릅니다.
1. `_satellite.setDebug(true)`를 입력한 다음 **[!UICONTROL Enter]**키를 누릅니다.
1. 페이지를 새로 고칩니다.

   이 작업으로 스테이징 라이브러리가 로드되고 디버거가 시작되어, 페이지에서 실행되는 모든 사용 가능한 (게시된/게시되지 않은) 규칙에 대한 세부 정보가 표시됩니다.
1. 완료되면 `localStorage.setItem('sdsat_stagingLibrary', false)`를 실행한 다음 **[!UICONTROL Enter]**키를 누릅니다.

   단계 결과
