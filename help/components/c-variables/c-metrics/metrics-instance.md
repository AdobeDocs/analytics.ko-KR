---
description: 변수에 대해 값이 설정된 횟수입니다.
keywords: 인스턴스
seo-description: 변수에 대해 값이 설정된 횟수입니다.
seo-title: 인스턴스
solution: Analytics
title: 인스턴스
topic: 지표
uuid: FEC 94 BDD-A 1 DC -4 CB 0-8983-EA 575 B 69589 F
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 인스턴스

변수에 대해 값이 설정된 횟수입니다.

인스턴스는 모든 히트 유형에 대해 계산되지만, 지속성으로 인해 후속 히트에서 변수에 대한 값이 기록될 때에는 계산되지 않습니다.

예를 들어 사용자가 [!DNL example.com]을 통해 여러분의 사이트에 도착하는 경우, 사이트에 대한 첫 번째 이미지 요청에는 [!DNL example.com]의 참조가 포함되어 있습니다. 이 값이 설정되면, 방문 동안 본 모든 페이지에 대해 이 레퍼러가 기록되더라도 하나의 인스턴스가 [!DNL example.com] 인스턴스로 계산됩니다.

Data Warehouse에서 전환 변수에 대한 인스턴스가 2011년 중반에 추가되어, Data Warehouse 요청이 특정 전환 변수 인스턴스를 지표로 처리할 수 있습니다. 이 지표는 지표를 도입한 시간 이전의 보고에는 사용할 수 없습니다.
