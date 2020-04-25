---
description: 처리 규칙을 사용하여 컨텍스트 데이터 변수의 값을 props 및 eVars로 이동합니다.
subtopic: Processing rules
title: eVar에 컨텍스트 데이터 변수 복사
topic: Admin tools
uuid: 1beaec4c-71e9-49ce-b154-78408cc532a3
translation-type: tm+mt
source-git-commit: 984d6034d14cc4256d93bd4f7d1a7f01b63b71e9

---


# eVar에 컨텍스트 데이터 변수 복사

처리 규칙을 사용하여 컨텍스트 데이터 변수의 값을 prop 및 eVar로 이동합니다. 처리 규칙이 없으면 컨텍스트 데이터 변수는 의미가 없으며 Analytics에 보고서를 채우지 않습니다.

[!UICONTROL 컨텍스트 변수] 목록은 이전 30일 동안 보고서 세트로 전송된 모든 변수를 포함합니다. 컨텍스트 데이터 변수 이름은 알지만, 현재 보고서 세트로 보내지 않았다면 변수 이름을 입력하고 **[!UICONTROL 변수 이름 컨텍스트 데이터 추가]**&#x200B;를 클릭하여 값을 추가할 수 있습니다.

![추가](assets/add-context-variable.png)

다음 예제에서는 `search_term` 컨텍스트 데이터 변수를 가져와 해당 값을 `eVar3`에 지정합니다.

![설정 ](assets/set-context-data.png)

위의 예제는 채울 eVar가 몇 개만 있을 때 잘 작동합니다. 조직에 각각 고유한 eVar가 필요한 수백 개의 컨텍스트 데이터 변수가 있는 경우 조건문을 사용할 수 있습니다. 십여 개의 조건문을 단일 처리 규칙에 맞게 설정하여 조직에서 150개 처리 규칙 제한을 실행하지 않고도 한 보고서 세트에 모든 eVar를 채울 수 있습니다.

다음 예제는 `prop7`을 컨텍스트 데이터 변수 `testhierarchy`로 채우지만, `testhierarchy`가 설정된 경우만 해당합니다.

![조건부](assets/add-conditional.png)

컨텍스트 데이터 변수 구현에 대한 자세한 내용은 구현 사용 안내서의 [컨텍스트 데이터 변수](/help/implement/vars/page-vars/contextdata.md)를 참조하십시오.
