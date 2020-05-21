---
description: 장치의 JavaScript 사용 설정 여부 또는 장치가 "식별되지 않음"으로 카운트되었는지 여부를 기준으로 지표를 표시합니다.
title: JavaScript 지원
topic: Reports
uuid: 7b95001a-cd35-478a-8b24-54d30666110d
translation-type: ht
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# JavaScript 지원

장치의 JavaScript 사용 설정 여부 또는 장치가 &quot;식별되지 않음&quot;으로 카운트되었는지 여부를 기준으로 지표를 표시합니다.

>[!NOTE] 2016년 11월 초에 JavaScript가 모바일 장치에 대해 항상 *`disabled / unidentified`*&#x200B;으로 나열되는 제한을 제거할 계획입니다.

JavaScript 보고서는 원시 데이터에서 javascript 열에 해당합니다.

javascript가 방문 수준 필드이므로 방문의 첫 번째 히트에 있는 값을 유지합니다. (visit_referrer가 방문의 첫 번째 레퍼러만 유지하는 것과 마찬가지로) javascript 열은 j_jscript 열에 있는 첫 번째 값을 기반으로 합니다.

j_jscript는 Adobe Analytics 이미지 요청에서 매개 변수 j로 채워집니다.

다음은 한 예입니다.

| 히트 | j_jscript | javascript |
|---|---|---|
| 1 |  | 0 |
| 2 | 1.6 | 0 |
| 3 | 1.6 | 0 |

따라서 방문에서 특정 시점에 javascript 버전을 지정했는지는 문제가 되지 않습니다. 첫 번째 히트에 j_jscript에 대한 값이 포함되지 않았기 때문에 항상 Javascript 아님으로 표시됩니다.
