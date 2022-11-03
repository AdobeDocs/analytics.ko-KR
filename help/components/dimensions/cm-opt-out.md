---
title: 동의 관리 옵트아웃
description: 방문자가 옵트아웃한 개인 정보 설정을 확인합니다.
source-git-commit: 49b2c144fea5786564ccb6dc70adead3bc669596
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 5%

---

# 동의 관리 옵트아웃

동의 관리 옵트아웃 차원은 방문자가 명시적으로 옵트아웃한 개인 정보 설정을 표시합니다. 이 차원을 사용하여 개인 정보 설정에 따라 데이터를 필터링하거나 가장 일반적인 개인 정보 옵트아웃 이유를 확인할 수 있습니다.

## 이 차원을 데이터로 채우기

이 차원은 다음 항목에서 데이터를 수집합니다 [컨텍스트 데이터 변수](/help/implement/vars/page-vars/contextdata.md):

* `contextData.['cm.ssf']` 설정 `1`. If `cm.ssf` 다음과 같음 `0` 또는 가 비어 있으면 이 변수는 아무 작업도 하지 않습니다.
* `contextData.['opt.dmp']` 설정 `N`. If `opt.dmp` 다음과 같음 `Y`, [동의 관리 옵트인](cm-opt-in.md) 차원이 대신 채워집니다.
* `contextData.['opt.sell']` 설정 `N`. If `opt.sell` 다음과 같음 `Y`, [동의 관리 옵트인](cm-opt-in.md) 차원이 대신 채워집니다.

조직은 이러한 컨텍스트 데이터 변수를 구현하는 논리를 결정합니다. 변수는 설정된 히트 이후에 지속되지 않으므로 각 페이지에서 각 컨텍스트 데이터 변수를 설정해야 합니다.

## 차원 항목

Dimension 항목에는 다음 세 가지 값이 포함됩니다.

* **`SSF`**: 방문자가 옵트아웃했습니다. [서버 측 전달](/help/admin/admin/c-server-side-forwarding/ssf.md). 이 차원 항목은 컨텍스트 데이터 변수가 있을 때 표시됩니다 `cm.ssf` 다음과 같음 `1`. 자세한 내용은 [데이터 개인 정보 보호 개요](https://experienceleague.adobe.com/docs/audience-manager/user-guide/overview/data-privacy/data-privacy.html) 를 참조하십시오.
* **`DMP`**: 방문자가 데이터 관리 플랫폼에 대한 공유를 옵트아웃했습니다. 이 차원 항목은 컨텍스트 데이터 변수가 있을 때 표시됩니다 `opt.dmp` 다음과 같음 `N`. 히트가 Adobe Audience Manager에 전달되지 않습니다.
* **`SELL`**: 방문자가 제3자에게 데이터 공유 또는 판매를 옵트아웃했습니다. 이 차원은 컨텍스트 데이터 변수 `opt.sell` 다음과 같음 `N`.
