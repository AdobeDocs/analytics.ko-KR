---
description: Power BI 모범 사례입니다.
title: 모범 사례
feature: Report Builder
role: User, Admin
exl-id: 2d9447f4-77ac-465b-af93-206dc3ea80f7
source-git-commit: 12d048b42c6a61e03dbbe73acb9d34df3e37693c
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 100%

---

# 모범 사례

## Power BI 시각화에서 참조 유지

요청을 생성하면 해당 요청에는 항상 Power BI에 동일한 참조가 생깁니다. 단, 요청을 삭제하면 참조는 동일한 차원에 대해 생성한 새 요청을 사용하게 됩니다.

통합 문서에서 요청을 삭제하는 경우, Power BI에서 해당 요청을 가리키는 시각화가 없는지 확인하십시오. 그렇게 하지 않으면 시각화가 손상되기 때문입니다.

* 가능하다면 Report Builder에서 생성한 요청은 삭제하지 마십시오.
* Report Builder에서 요청을 삭제하는 경우에는 Power BI에서 그에 해당하는 시각화도 반드시 삭제하십시오.
* 잘 모를 경우에는, 더 이상 필요하지 않은 요청을 삭제한 후 다시 게시하고 Power BI로 이동하여 손상된 시각화를 확인하십시오.
