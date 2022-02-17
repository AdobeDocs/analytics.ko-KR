---
title: 거래 ID 데이터 소스
description: 거래 ID 데이터 소스를 사용하는 일반적인 워크플로우에 대해 알아봅니다.
feature: Data Sources
exl-id: 5f26b15c-8d9c-46d5-860f-13fdfa21af2e
source-git-commit: 79294cfc6f86e5a41a39504099cd730f53668725
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 45%

---

# 거래 ID 데이터 소스

거래 ID 데이터 소스를 사용하면 온라인 및 오프라인 데이터를 나란히 볼 수 있을 뿐만 아니라 데이터를 함께 연결할 수 있습니다. Analytics 구현에서 [`transactionID`](/help/implement/vars/page-vars/transactionid.md) 변수를 사용해야 합니다.

`transactionID` 값이 포함된 온라인 히트를 전송하는 경우 Adobe는 모든 변수 집합의 &quot;스냅샷&quot;을 취하거나 해당 시점에 지속됩니다. Data Sources를 통해 업로드된 일치하는 거래 ID가 발견되면 오프라인 및 온라인 데이터가 함께 연결됩니다.

트랜잭션을 사용하려면, 해당 거래 ID를 가진 거래 데이터 소스 데이터가 전송되기 전에 거래 ID가 있는 온라인 히트가 전송되고 처리되어야 합니다. 온라인 히트에는 거래 ID 정보와 함께 저장된 온라인 히트에 있는 변수(eVar 등)가 있지만, 이벤트는 포함되지 않습니다.

거래 데이터 소스 히트가 전송되면 데이터 소스 거래 히트의 거래 ID가 변수 등을 조회합니다. (이벤트가 아님) 트랜잭션 ID가 있는 원래의 온라인 히트와 연결되어 있습니다. 데이터 소스 트랜잭션 히트에서 전달된 변수에 대한 값이 없으면 데이터 소스 트랜잭션 히트에서 이러한 변수를 사용합니다.

## 예

거래 ID 1256인 온라인 히트가 이 히트에 전달되면 해당 히트가 전달됩니다 `evar1=blue`, `evar2=water` 및 `event1` 가 설정된 경우 거래 ID 1256에 대한 거래 데이터가 `evar1=blue`, `evar2=water`. 트랜잭션 정보의 일부로 저장된 이벤트 값은 없습니다.

이제 데이터 소스 트랜잭션 히트가 트랜잭션 ID 1256과 함께 시스템을 통해 전달된다고 가정해 보겠습니다 `evar1=yellow`, `evar3=mountain` 및 `event2` 설정합니다. 시스템은 저장된 트랜잭션 데이터와 데이터 소스 트랜잭션 히트 세트에서 찾습니다 `evar2=water` (원래 히트에서 설정된 대로) 설정되지 않음 `evar1=blue` (원래 히트에 있었을 때) `evar1` (노란색)가 이미 데이터 소스 트랜잭션 히트에 설정되어 있습니다.  따라서 데이터 소스 트랜잭션 히트는 `evar1=yellow`, `evar2=water` (원본 온라인 히트에서) 및 `evar3=mountain`. 이러한 3개의 eVar 값은 `event2` 설정 - 데이터 소스 트랜잭션 히트의 이벤트입니다.

데이터 소스 트랜잭션 히트에서 가져올 값이 없습니다. `event1` 데이터 소스 트랜잭션 히트가 처리될 때 설정합니다.

## 거래 ID 데이터 소스의 전체 워크플로우

다음 일반 워크플로우를 사용하여 거래 ID 데이터 소스 사용을 시작합니다.

1. 데이터 소스(&#39;일반&#39; 카테고리와 &#39;일반 데이터 소스(거래 ID)&#39; 유형)를 만듭니다.
1. 데이터 소스 설정 마법사에 따라 데이터를 업로드하고 데이터 소스 템플릿 파일을 다운로드할 FTP 위치를 가져옵니다.
1. `transactionID` 변수를 포함하도록 구현을 업데이트합니다.
1. `.fin` 파일을 사용하여 데이터 소스 파일을 FTP 사이트로 업로드합니다.

## 업로드 파일 및 구현 코드 예

다음 데이터 소스 파일을 업로드하고 사이트에서 다음 코드를 구현하면 보고에 연결된 데이터가 표시됩니다. 데이터 소스 파일은 eVar1 및 event1을 사용하는 반면, 온라인 구현에서는 eVar2 및 event2를 사용합니다. 거래 ID가 일치하므로 eVar1에 대한 event2 데이터와 eVar2에 대한 event1 데이터를 볼 수 있습니다.

### 예제 파일

템플릿을 다운로드하고 값을 업데이트한 다음 데이터 소스 FTP 위치에 업로드합니다.

| `#` | `Example eVar1 name` | `Example event 1 name` | `1` |
|---|---|---|---|
| `Date` | `Evar 1` | `Event 1` | `transactionID` |
| `01/01/2020/12/00/00` | `Example eVar1 value` | `1` | `1234` |

### 예제 구현 코드

거래 ID에 대한 자세한 내용은 구현 사용 안내서에서 [`transactionID`](/help/implement/vars/page-vars/transactionid.md)를 참조하십시오.

```js
var s = s_gi("examplersid");
s.eVar2 = "Example eVar2 value";
s.events = "event2";
s.transactionID = "1234";
s.t();
```
