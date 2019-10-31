---
description: 'null'
seo-description: 'null'
seo-title: 우수 사례
title: 우수 사례
uuid: 6d55a9aa-030e-4e4d-963c-ec9cc38e1731
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# 우수 사례

## Power BI 시각화에서 참조 유지 {#section_7ED14FE64D974681A57EB91EF1B47CB6}

요청을 생성하면 해당 요청에는 항상 Power BI에 동일한 참조가 생깁니다. 하지만, 요청을 삭제하면, 참조는 동일한 차원에 대해 생성한 새 요청이 사용하게 됩니다.

통합 문서에서 요청을 삭제하는 경우, Power BI에서 해당 요청을 가리키는 시각화가 없는지 확인하십시오. 그렇게 하지 않으면 시각화가 손상되기 때문입니다.

* 가능하다면 Report Builder에서 생성한 요청은 삭제하지 마십시오.
* Report Builder에서 요청을 삭제하는 경우에는 Power BI에서 그에 해당하는 시각화도 반드시 삭제하십시오.
* 잘 모를 경우에는, 더 이상 필요하지 않은 요청을 삭제한 후 다시 게시하고 Power BI로 이동하여 손상된 시각화를 확인하십시오.

