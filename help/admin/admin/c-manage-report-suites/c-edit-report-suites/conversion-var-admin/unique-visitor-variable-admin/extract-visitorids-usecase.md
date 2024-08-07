---
description: Data Warehouse는 방문자 ID 목록을 추출할 수 있는 기능을 제공합니다. 이러한 ID는 쿠키 ID가 아니고 전환 변수 중 하나에서 캡처한 ID입니다. 이 정보를 다른 방법으로 얻을 수도 있지만, 다음 방법을 사용하면 간단하게 Data Warehouse 요청을 생성할 수 있습니다.
title: 사용 사례 - 방문자 ID 추출
feature: Admin Tools
role: Admin
exl-id: b1fc41af-31c7-42cd-aab7-0c659577781d
source-git-commit: 429aaa43fdae669350bdb5a5a54a7d4b9b1c65f2
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 96%

---

# 사용 사례 - 방문자 ID 추출

Data Warehouse는 방문자 ID 목록을 추출할 수 있는 기능을 제공합니다. 이러한 ID는 쿠키 ID가 아니고 전환 변수 중 하나에서 캡처한 ID입니다. 이 정보를 다른 방법으로 얻을 수도 있지만, 다음 방법을 사용하면 간단하게 Data Warehouse 요청을 생성할 수 있습니다.

예를 들어, 비즈니스에서 고객과 잠재고객에게 마케팅 이메일을 보내는 경우를 가정할 수 있습니다. 이 전자 메일 받는 사람 각각에는 전자 메일 시스템(예: *`EMAIL Contact ID`*)에 고유한 ID가 있습니다. 연락처에서 이메일을 받고 링크를 클릭한 방문자는 캠페인 ID와 고유한 이메일 연락처 ID가 지정된 상태로 웹 사이트에 도착합니다. 예를 들어 이메일 링크는 다음과 같이 확인될 수 있습니다.

```js
https://www.test.com/?cid=springmailblast&mid=1363660158
```

전환 변수(eVar)에서 이 값을 설정하면 각 이메일의 수행 방법(캠페인 ID를 통해)과 각 이메일 수신자가 사이트를 방문한 빈도(이메일 연락처 ID를 통해)를 확인할 수 있습니다.

이러한 ID를 캡처하는 경우를 생각해 보십시오. 대부분의 마케터는 웹 사이트 행동을 세그먼트화한 후 특정 기준에 맞는 사람에 대한 재마케팅 여부를 확인하려고 합니다. 예를 들어, 이메일을 통해 사이트에 온 다음 웹 사이트 양식을 보거나 완료한 모든 이메일 수신자에게 재마케팅 이메일을 보낼 수 있습니다. 그러려면 특정 양식을 완료한 이메일 연락처 ID를 식별할 방법이 필요합니다.

한 가지 방법은 전환 하위 관계 보고서를 사용하여 양식 ID eVar 값을 이메일 연락처 ID eVar로 분류하는 것입니다. Data Warehouse를 사용하면 사전 작성된 기능을 여기에 사용할 수 있습니다. 이 기능을 사용하면 고유 사용자 ID(이 경우 이메일 연락처 ID)를 저장하는 eVar를 에 알리고 Data Warehouse를 사용하여 해당 ID를 쉽게 추출할 수 있습니다. 이 기능을 사용하면 관심 있는 고유 방문자 ID를 가져오는 데이터 웨어하우스 요청을 자동으로 생성할 수 있습니다.
