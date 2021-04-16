---
description: 'eVar 값을 Prop에 복사하여 경로 지정을 활성화할 수 있습니다. '
subtopic: Processing rules
title: eVar 값을 prop에 복사하여 경로 결정
feature: 관리 도구
uuid: 8d7647c7-aa91-466b-8d31-fb4dce83f04a
exl-id: 23c978b9-a159-4364-9214-561a255d23e4
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 100%

---

# eVar 값을 prop에 복사하여 경로 결정

eVar 값을 Prop에 복사하여 경로 지정을 활성화할 수 있습니다. 

값 설정 시 왼쪽의 변수는 오른쪽의 변수에서 (비어 있는 경우에도)값을 받습니다.

| 규칙 세트 | 값 |
|---|---|
| 조건 | 없음(항상 실행) |
| 작업 | Prop1 값을 eVar1로 덮어쓰기 |

Prop1 값이 아직 다음과 유사한 값을 포함하지 않는 경우에만, 이 규칙을 수정하여 Prop1 값을 설정할 수 있습니다.

| 규칙 세트 | 값 |
|---|---|
| 조건 | Prop1이 설정되지 않은 경우 |
| 작업 | Prop1 값을 eVar1로 덮어쓰기 |

예:

![](assets/overwrite-empty-prop.png)
