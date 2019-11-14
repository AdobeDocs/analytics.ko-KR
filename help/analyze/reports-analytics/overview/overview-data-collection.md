---
description: Adobe Analytics에 대한 데이터를 수집하는 방법에 대해 알아봅니다.
solution: Analytics
subtopic: Get started
title: 데이터 수집 정보
topic: Reports and analytics
uuid: 4dd9a23d-ad49-4841-8f4c-32c3993851f2
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 데이터 수집 정보

Adobe Analytics에 대한 데이터를 수집하는 방법에 대해 알아봅니다.

Adobe가 추적하는 모든 페이지에는 작은 Adobe 공인 JavaScript 코드가 있습니다. 계정 관리자가 이 코드를 제공합니다.

상위 수준의 데이터 수집 프로세스는 다음과 같이 진행됩니다.

![](assets/data_collection.png)

1. 방문자가 데이터 수집 코드가 들어 있는 웹 페이지를 방문합니다.
1. 페이지가 로드됨에 따라 데이터 수집 코드가 이미지 요청(웹 비콘이라고 함)을 Adobe 데이터 수집 서버에 전송합니다. 이미지 요청에는 웹 사이트와 방문자의 상호 작용에 대해 수집할 데이터가 들어 있습니다.
1. Adobe는 보고서 세트에 데이터를 저장합니다. 로그인하여 보고서 세트 데이터에 액세스하고 웹 사이트에서의 방문자 활동과 관련된 보고서를 생성할 수 있습니다.

데이터 수집은 매우 신속하며 페이지 로드 시간에 그다지 영향을 주지 않습니다. 수집된 데이터는 브라우저 **다시 로드** 또는 **뒤로** 단추를 클릭하여 계산된 페이지 보기 횟수를 포함합니다. JavaScript 코드는 캐시에서 페이지를 검색할 때도 실행됩니다.

Analytics [에서 데이터 수집을 참조하십시오.](/help/import/home.md)
