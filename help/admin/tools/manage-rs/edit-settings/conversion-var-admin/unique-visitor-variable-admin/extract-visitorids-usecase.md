---
description: Data Warehouse에서는 방문자 ID 목록을 추출할 수 있는 기능을 제공합니다. 이러한 ID는 쿠키 ID가 아니라 전환 변수 중 하나에서 캡처하는 ID입니다. 이 정보를 가져오는 다른 방법이 있지만 다음 예제는 Data Warehouse 요청을 생성하는 바로 가기입니다.
title: 사용 사례 - 방문자 ID 추출
feature: Admin Tools
role: Admin
exl-id: b1fc41af-31c7-42cd-aab7-0c659577781d
TQID: 'https://experienceleague.adobe.com/CUpKcu-jVNn77bkWM2mJvlLxYMyvfpRt4o-maC7tUBA'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
subfeature_v2:
  - id: f47edbe0-f963-46ff-a667-71011396f5f3
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 399
ht-degree: 2%

---

# 사용 사례 - 방문자 ID 추출

Data Warehouse에서는 방문자 ID 목록을 추출할 수 있는 기능을 제공합니다. 이러한 ID는 쿠키 ID가 아니라 전환 변수 중 하나에서 캡처하는 ID입니다. 이 정보를 가져오는 다른 방법이 있지만 다음 예제는 Data Warehouse 요청을 생성하는 바로 가기입니다.

예를 들어, 비즈니스에서 고객 및 잠재 고객에게 마케팅 이메일을 전송한다고 가정해 보겠습니다. 이 전자 메일 받는 사람 각각에는 전자 메일 시스템(예: *`EMAIL Contact ID`*)에 고유한 ID가 있습니다. 연락처가 전자 메일을 받고 링크 중 하나를 클릭하면 방문자가 캠페인 ID와 고유 전자 메일 연락처 ID를 사용하여 웹 사이트에 도착하도록 전자 메일을 설정합니다. 예를 들어 이메일 링크가 다음으로 확인될 수 있습니다.

```js
https://www.example.com/?cid=springmailblast&mid=1363660158
```

전환 변수(eVar)에 이러한 매개 변수를 설정하면 각 전자 메일이 수행된 방법(캠페인 ID를 통해)과 각 전자 메일 수신자가 사이트를 방문한 빈도(전자 메일 연락처 ID를 통해)를 확인할 수 있습니다.

이러한 ID를 캡처하고 있다고 가정합니다. 대부분의 마케터는 웹 사이트 동작을 세그먼트화한 후 특정 기준을 충족하는 사람에게 다시 마케팅할 수 있는지 확인하고 싶어합니다. 예를 들어 이메일을 통해 사이트로 이동하여 웹 사이트 양식을 보거나 완료한 모든 이메일 수신자에게 리마케팅 이메일을 보낼 수 있습니다. 이렇게 하려면 특정 양식을 완료하는 사용자의 이메일 연락처 ID를 식별하는 방법을 찾으십시오.

이렇게 하는 한 가지 방법은 전환 하위 관계 보고서를 사용하여 양식 ID eVar 값을 이메일 연락처 ID eVar으로 분류하는 것입니다. 하지만 Data Warehouse을 사용하여 이를 수행하는 데에는 사전 빌드된 기능을 사용할 수 있습니다. 이 기능을 사용하면 고유한 사용자 ID(이 경우 이메일 연락처 ID)를 저장하는 eVar을 구별할 수 있으며 Data Warehouse를 사용하여 해당 ID를 쉽게 추출할 수 있습니다. 이 기능을 사용하면 관심 있는 고유 방문자 ID를 가져오는 데이터 웨어하우스 요청을 자동으로 만들 수 있습니다.
