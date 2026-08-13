---
description: Data Warehouse에서 데이터를 검색하는 데 걸리는 시간을 줄이는 데 도움이 되는 지침에 대해 알아봅니다.
keywords: 우수 사례;실패;시간 초과;문제 해결
title: Data Warehouse 우수 사례
feature: Data Warehouse
uuid: d71c9138-22d9-4f92-885e-593f83f2bb59
exl-id: 7e21534b-a7ec-4231-89f1-0ad5013e70cf
TQID: 'https://experienceleague.adobe.com/fWshdRnbrh11kLLT3DiW0a-qMJ13o8v4EMH-t-ceWC8'
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: b3f03848-ae12-48b2-8aab-cad18567eb32id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
subfeature_v2: id: f47edbe0-f963-46ff-a667-71011396f5f3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 235
ht-degree: 27%

---

# Data Warehouse 우수 사례

Data Warehouse는 사용자 지정 보고서를 실행할 수 있는 유연한 인터페이스를 제공합니다. 다음 지침을 사용하여 데이터를 검색하는 데 걸리는 시간을 줄일 수 있습니다.

| 지침 | 설명 |
|--- |--- |
| 요청하는 데이터의 양 이해 | 대규모 보고서 세트에 대한 다년간의 보고서에는 수백억 개의 데이터 행이 포함될 수 있습니다. 이 데이터를 처리하고 평가하는 데 며칠 또는 몇 주가 걸릴 수 있습니다. 보고서 사용 방법을 평가하여 여러 해 데이터 중 일부를 사용할 수 있는지 또는 보고서를 여러 요청으로 나눌 수 있는지 확인합니다. |
| 보고서 기간을 세부기간에 일치 | 보고 세부기간을 사용하려면 추가 처리 시간이 필요합니다. 전체 연도의 월별 세부기간을 보고하는 경우 매월 보고서 요청을 제출하면 보고서가 훨씬 빠르게 처리됩니다. |
| 완료된 데이터 범위에 대한 보고서 | Data Warehouse 보고서는 요청한 데이터 범위가 완료될 때 생성됩니다. 예를 들어 수요일에 현재 주에 대한 보고서를 요청하면 그다음 주의 일요일까지 보고서가 생성되지 않습니다. . |
| Data Warehouse에서 경로 지정 보고서 생성 | 경로 지정 지표(시작, 종료, 바운스 등) 는 data warehouse에서 사용할 수 없습니다. |
| 가상 보고서 세트 | 가상 보고서 세트에 대한 Data Warehouse 보고는 가상 보고서 세트에 구성된 대체 시간대를 지원합니다. |

