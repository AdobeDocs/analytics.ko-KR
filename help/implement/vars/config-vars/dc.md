---
title: dc
description: 사용할 데이터 센터를 결정할 수 있도록 해주는 폐기된 변수입니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# dc

>[!IMPORTANT] 이 변수는 사용이 중단되었습니다. 대신 [`trackingServer`](trackingserver.md)를 사용하십시오.

이전 버전의 Adobe Analytics에서는 보낸 데이터를 받을 데이터 센터를 지정해야 했습니다. 히트를 잘못된 데이터 센터에 보내는 경우에는 데이터 손실도 발생했습니다.

Adobe는 모든 구현에서 히트를 `sc.omtrdc.net`에 보낼 수 있도록 함으로써 이 환경을 개선했습니다. 따라서 더 이상 데이터 센터를 지정할 필요가 없습니다.
