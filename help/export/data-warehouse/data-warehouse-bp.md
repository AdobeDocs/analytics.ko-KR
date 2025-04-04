---
description: Data Warehouse에서 데이터를 검색하는 데 걸리는 시간을 줄이는 데 도움이 되는 지침에 대해 알아봅니다.
keywords: 우수 사례;실패;시간 초과;문제 해결
title: Data Warehouse 우수 사례
feature: Data Warehouse
uuid: d71c9138-22d9-4f92-885e-593f83f2bb59
exl-id: 7e21534b-a7ec-4231-89f1-0ad5013e70cf
source-git-commit: d929e97a9d9623a8255f16729177d812d59cec05
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 79%

---

# Data Warehouse 우수 사례

Data Warehouse는 사용자 지정 보고서를 실행할 수 있는 유연한 인터페이스를 제공합니다. 다음 지침을 사용하여 데이터를 검색하는 데 걸리는 시간을 줄일 수 있습니다.

| 지침 | 설명 |
|--- |--- |
| 요청하려는 데이터의 양 이해 | 큰 보고서 세트에 대한 다년 보고서에는 수백억 개의 데이터 열이 포함될 수 있습니다. 이 데이터를 처리하고 평가하는 데 며칠 또는 몇 주가 걸릴 수 있습니다. 보고서를 어떻게 사용하고 있는지 평가하여 여러 해에 걸친 데이터 중 일부를 사용할 수 있는지 또는 보고서를 여러 개의 요청으로 나눌 수 있는지를 파악해보십시오. |
| 보고서 기간을 세부기간에 일치시킴 | 세부기간별로 보고하려면 추가 처리 시간이 필요합니다. 1년의 월간 세부기간을 보고하는 경우 매달 보고서 요청을 제출하면 보고서가 훨씬 더 빠르게 처리됩니다. |
| 완료된 데이터 범위에 대한 보고서 | Data Warehouse 보고서는 요청한 데이터 범위가 완료될 때 생성됩니다. 예를 들어 수요일에 현재 주에 대한 보고서를 요청하면 그다음 주의 일요일까지 보고서가 생성되지 않습니다. . |
| Data Warehouse에서 경로 지정 보고서 생성 | 경로 지정 지표(시작, 종료, 바운스 등)는 Data Warehouse에서 사용할 수 없습니다. |
| 가상 보고서 세트 | 가상 보고서 세트에 대한 Data Warehouse 보고는 가상 보고서 세트에서 구성된 대체 시간대를 지원합니다. |

