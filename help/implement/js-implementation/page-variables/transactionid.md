---
description: 페이지 변수는 pageName, List Props, List Variables 등과 같이, 보고서를 직접 채웁니다.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: 페이지 변수
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 45642bdbe18627caa20b1def6443f1e596a41f52

---


# transactionID

[!UICONTROL 통합 데이터 소스는 트랜잭션 ID를 사용하여 오프라인 데이터를 온라인 트랜잭션(예: 온라인에서 생성된 리드 또는 구매)에 연결합니다.]

<!-- 

transactionID.xml

 -->

Adobe에 전송된 각각의 고유한 *`transactionID`*&#x200B;는 해당 트랜잭션에 대한 오프라인 정보의 [!UICONTROL 데이터 소스] 업로드 준비 시 기록됩니다. [ 데이터 소스](https://marketing.adobe.com/resources/help/en_US/sc/datasources/)를 참조하십시오.

| 최대 크기 | 디버거 매개 변수 | 채워진 보고서 | 기본값 |
|---|---|---|---|
| 100바이트 | xact | n/a | "" |

**트랜잭션 ID 저장 공간 활성화** {#section_3EA2C9DC9D4C4F0FBE4AB67981BCB52E}

*`transactionID`* 값을 기록하려면 보고서 세트 관리자에서 선택한 보고서 세트에 대해 [!UICONTROL 트랜잭션 ID 저장 공간]을 활성화해야 합니다. 이 설정은 다음 위치에 있습니다.

```
Analytics > Admin > Report Suites > Edit Settings > General > General Account Settings.
```

보고서 세트에 *`transactionID Storage`* 대해 활성화되었는지 확인하려면

```
Analytics > Admin > Data Sources > Manage
```

**구문 및 가능한 값** {#section_0C18329203DC45E989DBAE70C0FB4801}

```js
s.transactionID="unique_id"
```

*`transactionID`*&#x200B;에는 영숫자만 사용할 수 있습니다. 여러 [!UICONTROL transactionID]를 한 번의 히트에 기록해야 할 경우, 쉼표를 사용하여 여러 값을 구분하면 됩니다.

**예** {#section_A4C1F0E54CB54AD7B86A22147E9B5FEF}

```js
s.transactionID="11123456"
```

```js
s.transactionID="lead_12345xyz"
```

```js
s.transactionID=s.purchaseID
```

**함정, 질문 및 팁** {#section_4299BAD5D0154DBC88A9EF0E2C252BB4}

* *`transactionID`* 기록을 활성화하지 않은 경우 *`transactionID`* 값이 삭제되고 [!UICONTROL 통합 데이터 소스]에서 사용할 수 없습니다. *`transactionID`*&#x200B;가 설정된 페이지에서 전환 변수 또는 이벤트(eVar 또는 event 변수)를 설정해야 합니다. 설정되지 않으면 *`transactionID`*.

* 구매 및 리드와 같은 여러 시스템에 대해 [!UICONTROL transactionIDs]를 기록하는 경우 *`transactionID`*&#x200B;의 값이 항상 고유한지 확인합니다. lead_1234 및 purchase_1234와 같이 ID에 접두사를 추가하면 됩니다. [!UICONTROL 통합 데이터 소스]는 고유한 *`transactionID`*&#x200B;가 두 번 표시되면 예외로 작동하지 않습니다([!UICONTROL 데이터 소스] 데이터가 잘못된 데이터에 연결됨).

* 기본적으로 *`transactionID`* 값은 90일 동안 기억됩니다. 오프라인 상호 작용 프로세스가 90일 이상인 경우 고객 지원에 요청하여 한계를 늘리십시오.

> [!NOTE]*`transactionID`* 변수에는 쉼표를 제외한 모든 문자를 사용할 수 있습니다. 이 변수는 문자 제한(100바이트)이 지정된 동일한 위치에 있어야 합니다. 멀티바이트 문자를 사용하는 경우, 멀티바이트 문자 지원을 활성화해야 *`transactionID`*.
