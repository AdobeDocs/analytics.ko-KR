---
title: 거래 ID 데이터 소스
description: 거래 ID 데이터 소스를 사용하는 일반적인 워크플로에 대해 알아봅니다.
feature: Data Sources
exl-id: 5f26b15c-8d9c-46d5-860f-13fdfa21af2e
role: Admin
source-git-commit: 1d905aa47b4573a35012d56c0cf70fbc944bc972
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 7%

---

# 거래 ID 데이터 소스

거래 ID 데이터 소스는 온라인 및 오프라인 데이터를 함께 연결할 수 있는 요약 데이터 소스의 변형입니다. Analytics 구현에서 [`transactionID`](/help/implement/vars/page-vars/transactionid.md) 변수를 사용해야 합니다.

* 데이터 소스 파일의 행에 AppMeasurement에서 이미 수집한 거래 ID와 일치하는 거래 ID가 포함되어 있는 경우 차원 및 지표가 온라인 히트에 추가됩니다.
* 데이터 소스 파일의 행에 일치하는 항목이 포함되지 않은 거래 ID가 포함된 경우 해당 행은 요약 데이터 소스와 유사하게 처리됩니다.

>[!NOTE]
>
>거래 ID 데이터 소스를 사용하기 전에 먼저 원하는 보고서 세트에 대해 [일반 계정 설정](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md)에서 활성화해야 합니다.

[`transactionID`](/help/implement/vars/page-vars/transactionid.md) 값이 포함된 온라인 히트를 보낼 때 Adobe은 모든 변수 집합의 &quot;스냅샷&quot;을 취하거나 지속됩니다. 데이터 소스를 통해 업로드된 일치하는 거래 ID가 발견되면 오프라인 데이터와 온라인 데이터가 함께 연결됩니다.

거래 ID 데이터 소스에는 다음 속성이 있습니다.

* 온라인 데이터를 먼저 수집하고 처리해야 합니다. 보고서 세트가 해당 거래 ID와 일치하는 히트를 처리하기 전에 거래 ID 데이터 소스가 업로드되는 경우 데이터가 연결되지 않습니다.
* AppMeasurement을 통해 수집된 거래 ID는 25개월 후에 만료됩니다.
* 만료된 거래 ID로 업로드된 데이터 소스는 거래 ID 없이 업로드된 데이터와 유사하게 처리됩니다.
* 동일한 변수가 온라인 히트와 거래 ID 데이터 소스에 모두 포함된 경우 거래 ID 데이터 소스의 값이 거래 데이터 소스 히트에 사용됩니다.
* 변수가 온라인 히트에 포함되어 있지만 일치하는 거래 ID 데이터 소스 히트에 포함되어 있지 않으면 온라인 히트 변수가 유지됩니다.
* 여러 온라인 히트에 대해 동일한 거래 ID를 설정하면 첫 번째 발생만 일치하는 거래 ID 데이터 소스의 데이터로 변경됩니다.

예:

1. AppMeasurement의 페이지 보기에서 다음 위치를 보냅니다.
   * `eVar1`이(가) `blue`과(와) 같음
   * `eVar2`이(가) `water`과(와) 같음
   * `events`이(가) `event1`과(와) 같음
   * `transactionID`이(가) `1256`과(와) 같음
2. 히트가 수집되고 처리된 후 다음과 같은 거래 ID 데이터 소스를 업로드합니다.
   * `eVar1`이(가) `yellow`과(와) 같음
   * `eVar3`이(가) `bird`과(와) 같음
   * `events`이(가) `event2`과(와) 같음
   * `transactionID`이(가) `1256`과(와) 같음
3. 데이터 소스 히트가 처리되면 작업 영역에서 보고서를 볼 수 있습니다. 데이터에는 다음이 표시됩니다.
   * `eVar1`이(가) `yellow`과(와) 같음
   * `eVar2`이(가) `water`과(와) 같음
   * `eVar3`이(가) `bird`과(와) 같음
   * `events`이(가) `event2`과(와) 같음

트랜잭션 ID 히트가 해당 값을 덮어썼으므로 eVar1 값 `blue` 및 `event1` 지표가 보고에 없습니다.
