---
description: Power BI 모범 사례입니다.
title: 모범 사례
feature: Report Builder
role: User, Admin
exl-id: 2d9447f4-77ac-465b-af93-206dc3ea80f7
TQID: https://experienceleague.adobe.com/WXvRDft1TRz5qM9R8Psz-Yp2qY-AL-SrrXgXWRx55N0
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: c153fd90-23e1-4614-81d3-3cc7571227f7
  - id: f73667dc-d296-4875-8975-ac3fdc3adc42
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 139
ht-degree: 46%

---

# 모범 사례

{{legacy-arb}}

## Power BI 시각화에서 참조 유지

요청을 만들면 해당 요청에 Power BI에서 항상 동일한 참조가 생깁니다. 단, 요청을 삭제하면 참조는 동일한 차원에 대해 생성한 새 요청을 사용하게 됩니다.

통합 문서에서 요청을 삭제하는 경우, Power BI에서 해당 요청을 가리키는 시각화가 없는지 확인하십시오. 그렇게 하지 않으면 시각화가 손상되기 때문입니다.

* 가능하면 Report Builder에서 만든 요청을 삭제하지 마십시오
* Report Builder에서 요청을 삭제하는 경우 Power BI에서도 해당 시각화를 삭제하도록 하십시오.
* 확실하지 않은 경우: 더 이상 필요하지 않은 요청을 삭제한 다음 다시 게시하고 Power BI으로 이동하여 어떤 시각화가 손상되었는지 확인합니다
