---
title: 동의 관리 옵트아웃
description: 방문자가 옵트아웃한 개인 정보 설정을 확인합니다.
exl-id: 2bf4d22c-5b24-47fb-b489-49388fcca5b1
source-git-commit: dc9cd6bb45af0c992c37ffe20ea22eab67789ec5
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 100%

---

# 동의 관리 옵트아웃

&#39;동의 관리 옵트아웃&#39; 차원에서는 방문자가 명시적으로 옵트아웃한 개인 정보 설정이 표시됩니다. 이 차원을 사용하여 개인 정보 설정을 기반으로 데이터를 필터링하거나 가장 일반적인 개인 정보 옵트아웃 이유를 확인할 수 있습니다.

## 이 차원을 데이터로 채우기

이 차원은 다음 [컨텍스트 데이터 변수](/help/implement/vars/page-vars/contextdata.md)에서 데이터를 수집합니다.

* `1`로 설정된 경우 `contextData.['cm.ssf']` `cm.ssf`이 `0`이거나 비어 있는 경우 이 변수는 아무 작업도 하지 않습니다.
* `N`으로 설정된 경우 `contextData.['opt.dmp']` `opt.dmp`가 `Y`이면 [동의 관리 옵트인](cm-opt-in.md) 차원이 대신 채워집니다.
* `N`으로 설정된 경우 `contextData.['opt.sell']` `opt.sell`가 `Y`이면 [동의 관리 옵트인](cm-opt-in.md) 차원이 대신 채워집니다.

조직은 이러한 컨텍스트 데이터 변수를 구현하는 논리를 결정합니다. 이러한 데이터는 설정된 히트 이후에 유지되지 않으므로 각 페이지에서 각 컨텍스트 데이터 변수를 설정해야 합니다.

## 차원 항목

차원 항목에는 다음 세 가지 값이 포함됩니다.

* **`SSF`**: 방문자가 [서버측 전달](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf.md)을 옵트아웃했습니다. 이 차원 항목은 컨텍스트 데이터 변수 `cm.ssf`가 `1`인 경우에 존재합니다. 자세한 내용은 Audience Manager 사용 안내서의 [데이터 개인정보 보호 개요](https://experienceleague.adobe.com/docs/audience-manager/user-guide/overview/data-privacy/data-privacy.html)를 참조하십시오. 해당 히트는 Adobe Audience Manager로 전달되지 않습니다.
* **`DMP`**: 방문자가 데이터 관리 플랫폼에 대한 공유를 옵트아웃했습니다. 이 차원 항목은 컨텍스트 데이터 변수 `opt.dmp`가 `N`인 경우에 존재합니다. `SSF`와 마찬가지로, 해당 히트는 Adobe Audience Manager로 전달되지 않습니다.
* **`SELL`**: 방문자가 데이터를 서드파티에 공유하거나 판매하는 것을 옵트아웃했습니다. 이 차원은 컨텍스트 데이터 변수 `opt.sell`가 `N`인 경우에 존재합니다.
