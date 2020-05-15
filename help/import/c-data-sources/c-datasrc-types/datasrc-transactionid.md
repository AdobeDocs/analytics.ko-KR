---
title: 거래 ID 데이터 소스
description: 거래 ID 데이터 소스를 사용하는 일반적인 워크플로우에 대해 알아봅니다.
translation-type: ht
source-git-commit: c6f84f470dcf97f49ce7dc9d2c5dd8c65cc6cf67

---


# 거래 ID 데이터 소스

거래 ID 데이터 소스를 사용하면 온라인 및 오프라인 데이터를 나란히 볼 수 있을 뿐만 아니라 데이터를 함께 연결할 수 있습니다. Analytics 구현에서 [`transactionID`](/help/implement/vars/page-vars/transactionid.md) 변수를 사용해야 합니다.

`transactionID` 값이 포함된 온라인 히트를 전송하는 경우 Adobe는 모든 변수 집합의 &quot;스냅샷&quot;을 취하거나 해당 시점에 지속됩니다. Data Sources를 통해 업로드된 일치하는 거래 ID가 발견되면 오프라인 및 온라인 데이터가 함께 연결됩니다. 어떤 데이터 소스가 먼저 표시되는지는 중요하지 않습니다.

## 거래 ID 데이터 소스의 전체 워크플로우

다음 일반 워크플로우를 사용하여 거래 ID 데이터 소스 사용을 시작합니다.

1. 데이터 소스(&#39;일반&#39; 카테고리와 &#39;일반 데이터 소스(거래 ID)&#39; 유형)를 만듭니다.
1. 데이터 피드 설정 마법사에 따라 데이터를 업로드하고 데이터 소스 템플릿 파일을 다운로드할 FTP 위치를 가져옵니다.
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
