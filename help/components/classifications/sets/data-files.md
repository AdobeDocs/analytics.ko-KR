---
description: 분류 세트에서 지원하는 파일 형식
title: 분류 세트 파일 형식
feature: Classifications
exl-id: f3d429be-99d5-449e-952e-56043b109411
source-git-commit: c642664ecca24d9fc555944fb2b449f30eac879d
workflow-type: tm+mt
source-wordcount: '1023'
ht-degree: 0%

---

# 분류 세트 파일 형식

분류 세트는 분류 데이터를 대량으로 업로드하기 위해 여러 파일 형식을 지원합니다. 각 형식에는 성공적인 데이터 업로드를 위한 특정 요구 사항이 있습니다.

이러한 사양에 따라 파일의 형식이 올바르게 지정되면 분류 세트 인터페이스 또는 API를 통해 업로드할 수 있습니다. 자세한 업로드 지침은 다음과 같습니다.

* **브라우저 업로드**: [스키마](manage/schema.md) 참조
* **API 업로드**: [Analytics 분류 API](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/classifications/) 참조

분류 세트는 다음 파일 형식을 지원합니다.

* **JSON**: 구조화된 데이터가 있는 JavaScript 개체 표기법 파일
* **CSV**: 쉼표로 구분된 값 파일
* **TSV/TAB**: 탭으로 구분된 값 파일

## 일반 파일 요구 사항

모든 파일 형식은 다음 요구 사항을 준수해야 합니다.

* **파일 인코딩**: 바이트 순서 표시 없이 UTF-8을 사용합니다. Latin1 인코딩도 지원됩니다.
* **문자 제한**: 개별 분류 값의 최대 제한은 255바이트입니다.
* **키 요구 사항**: 키 값은 비워 두거나 공백만 포함할 수 없습니다. 중복 키가 있는 경우 마지막 항목이 사용됩니다.

+++**JSON 형식 세부 정보**

JSON 파일 형식은 JSON 라인(JSONL)에 대한 규칙을 따릅니다. 파일에는 라인당 하나의 JSON 오브젝트가 포함되어야 하며, 여기서 각 오브젝트는 단일 분류 레코드를 나타냅니다.

>[!NOTE]
>
>다음 JSON 줄 규칙에도 불구하고 모든 업로드에 `.json` 파일 확장명을 사용합니다. `.jsonl` 확장을 사용하면 오류가 발생할 수 있습니다.

### JSON 구조

각 JSON 개체에는 다음이 포함되어야 합니다.

* `key`(필수): 분류 레코드에 대한 고유 식별자
* `data`(업데이트에 필요): 분류 열 이름 및 해당 값이 포함된 개체
* `action`(선택 사항): 수행할 작업입니다. 지원되는 값은 다음과 같습니다.
   * `update`(기본값)
   * `delete-field`
   * `delete-key`
* `enc`(선택 사항): 데이터 인코딩 사양입니다. 지원되는 값은 다음과 같습니다.
   * `utf8` 또는 `UTF8`(기본값)
   * `latin1` 또는 `LATIN1`

모든 JSON 필드 이름(`key`, `data`, `action`, `enc`)은 대/소문자를 구분하며 소문자여야 합니다.

### JSON 예

**기본 업데이트 레코드:**

```json
{"key": "product123", "data": {"Product Name": "Basketball Shoes", "Brand": "Brand A", "Category": "Sports"}}
```

**지정된 인코딩으로 업데이트:**

```json
{"key": "product456", "enc": "utf8", "data": {"Product Name": "Running Shoes", "Brand": "Brand B"}}
```

**특정 필드 삭제:**

```json
{"key": "product789", "action": "delete-field", "data": {"Brand": null, "Category": null}}
```

**전체 키 삭제:**

```json
{"key": "product999", "action": "delete-key"}
```

### JSON 유효성 검사 규칙

* `key` 필드는 필수이며 null이거나 비워 둘 수 없습니다.
* `update` 작업의 경우 `data` 필드는 필수이며 비워 둘 수 없습니다.
* `delete-field` 작업의 경우 `data` 필드에 삭제할 필드가 있어야 합니다.
* `delete-key` 작업의 경우 `data` 필드가 없어야 합니다.
* 지원되는 인코딩 값은 대소문자를 구분하지 않으며 표준 문자 세트 이름을 포함합니다.

+++

+++**CSV 형식 세부 정보**

CSV(쉼표로 구분된 값) 파일은 쉼표를 사용하여 분류 데이터 필드를 구분합니다.

### CSV 구조

* **머리글 행**: 첫 번째 행에는 열 머리글이 포함되어야 하며 첫 번째 열은 키 열이어야 합니다. 후속 열은 분류 세트 스키마의 이름과 일치해야 합니다.
* **데이터 행**: 각 후속 행에 분류 데이터가 포함되어 있습니다.
* **구분 기호**: 필드는 쉼표로 구분됩니다.
* **Quoting**: 쉼표, 따옴표 또는 줄바꿈을 포함하는 필드는 큰따옴표로 묶어야 합니다.

### CSV 예

**기본 분류 데이터:**

```csv
Key,Product Name,Brand,Category,Price
product123,"Basketball Shoes",Brand A,Sports,89.99
product456,"Running Shoes",Brand B,Sports,79.99
product789,"Winter Jacket",Brand C,Clothing,149.99
```

**전체 키 삭제:**

```csv
Key,Product Name,Brand,Category,Price
product999,~deletekey~,,,
```

**특정 필드 삭제(업데이트와 혼합):**

```csv
Key,Product Name,Brand,Category,Price
product123,"Updated Product Name",Brand A,Sports,89.99
product456,,~empty~,~empty~,79.99
```

### CSV 형식 규칙

* 쉼표를 포함하는 필드는 큰따옴표로 묶어야 합니다.
* 큰따옴표가 포함된 필드는 큰따옴표를 두 배로 늘려 이스케이프 처리를 해야 합니다(`""`).
* 빈 필드는 해당 분류에 대한 null 값을 나타냅니다.
* 필드 주위의 선행 및 후행 공백은 자동으로 트리밍됩니다
* 따옴표 붙은 필드 내의 특수 문자(탭, 줄바꿈)는 보존됩니다

**삭제 작업:**
* 모든 필드에서 `~deletekey~`을(를) 사용하여 전체 키와 모든 해당 분류 데이터를 삭제합니다.
* 특정 필드에서 `~empty~`을(를) 사용하여 해당 분류 값만 삭제합니다(다른 필드는 그대로 유지).
* `~empty~`을(를) 사용하는 경우 같은 파일의 업데이트와 함께 삭제를 혼합할 수 있습니다

+++

+++**TSV/탭 형식 세부 정보**

TSV(탭으로 구분된 값) 및 TAB 파일은 탭 문자를 사용하여 분류 데이터 필드를 구분합니다.

### TSV/탭 구조

* **머리글 행**: 첫 번째 행에는 열 머리글이 포함되어야 하며 첫 번째 열은 키 열이어야 합니다. 후속 열은 분류 세트 스키마의 이름과 일치해야 합니다.
* **데이터 행**: 각 후속 행에 분류 데이터가 포함되어 있습니다.
* **구분 기호**: 필드가 탭 문자(`\t`)로 구분됩니다.
* **따옴표**: 일반적으로 따옴표는 필요하지 않지만 일부 구현은 따옴표 붙은 필드를 지원합니다.

### TSV/탭 예

**기본 분류 데이터:**

```tsv
Key    Product Name    Brand    Category    Price
product123    Basketball Shoes    Brand A    Sports    89.99
product456    Running Shoes    Brand B    Sports    79.99
product789    Winter Jacket    Brand C    Clothing    149.99
```

**전체 키 삭제:**

```tsv
Key    Product Name    Brand    Category    Price
product999    ~deletekey~            
```

**특정 필드 삭제(업데이트와 혼합):**

```tsv
Key    Product Name    Brand    Category    Price
product123    Updated Product Name    Brand A    Sports    89.99
product456        ~empty~    ~empty~    79.99
```

### TSV/탭 서식 규칙

* 필드는 단일 탭 문자로 구분됩니다
* 빈 필드(연속 탭)는 null 값을 나타냅니다.
* 일반적으로 특별한 견적은 필요하지 않습니다
* 선행 및 후행 공백은 그대로 유지됩니다
* 필드 내의 줄바꿈 문자는 사용하지 않아야 합니다.

**삭제 작업:**
* 모든 필드에서 `~deletekey~`을(를) 사용하여 전체 키와 모든 해당 분류 데이터를 삭제합니다.
* 특정 필드에서 `~empty~`을(를) 사용하여 해당 분류 값만 삭제합니다(다른 필드는 그대로 유지).
* `~empty~`을(를) 사용하는 경우 같은 파일의 업데이트와 함께 삭제를 혼합할 수 있습니다

+++

## 오류 처리

일반적인 업로드 문제 및 솔루션:

### 일반 파일 형식 오류

* **잘못된 파일 형식**: 파일 확장명이 콘텐츠 형식(.json, .csv, .tsv 또는 .tab)과 일치하는지 확인하십시오.
* **&quot;알 수 없는 헤더&quot;**: 열 이름은 분류 세트 스키마와 일치해야 합니다(모든 형식에 적용).

### CSV/TSV 관련 오류

* **&quot;첫 번째 열은 키여야 합니다.&quot;**: CSV/TSV 파일에 먼저 키 열과 함께 적절한 머리글 행이 있는지 확인하십시오.
* **&quot;최소 두 개의 헤더 항목이 필요합니다.&quot;**: CSV/TSV 파일에는 적어도 &quot;키&quot; 열과 하나의 분류 열이 있어야 합니다.
* **&quot;첫 번째 헤더 열은 &#39;Key&#39;&quot;**&#x200B;이어야 합니다. 첫 번째 열 헤더는 정확히 &#39;Key&#39;(대문자 K, 대/소문자 구분)여야 합니다.
* **&quot;빈 헤더가 허용되지 않음&quot;**: 모든 CSV/TSV 열 헤더에 이름이 있어야 합니다.
* **&quot;열 수가 헤더와 일치하지 않습니다.&quot;**: 각 CSV/TSV 데이터 행의 필드 수가 헤더 행과 같아야 합니다.
* **&quot;잘못된 형식의 문서&quot;**: CSV 따옴표, TSV 파일에서 적절한 탭 구분 등을 확인하십시오.

### JSON 관련 오류

* **&quot;키는 필수 필드입니다&quot;**: 모든 JSON 레코드에는 비어 있지 않은 `"key"` 필드가 있어야 합니다(소문자, 대/소문자 구분).
* **&quot;action=update&quot;**&#x200B;를 사용할 때 데이터는 필수 필드입니다. JSON 업데이트 작업에는 `"data"` 필드가 포함되어야 합니다.
* **&quot;action=delete-field&quot;**&#x200B;을(를) 사용할 때 데이터는 필수 필드입니다. JSON delete-field 작업은 `"data"` 필드에서 삭제할 필드를 지정해야 합니다.
* **&quot;action=delete-key&quot;**&#x200B;을(를) 사용할 때 데이터가 없어야 합니다. JSON delete-key 작업에는 `"data"` 필드가 포함될 수 없습니다.
* **&quot;지원되지 않는 인코딩&quot;**: `"enc"` 필드의 지원되는 인코딩 값(utf8, UTF8, latin1, LATIN1)만 사용합니다.
* **잘못된 JSON 구문**: JSON 파일의 형식이 JSONL 규칙에 따라 올바르게 지정되었는지 확인하십시오. 또한 일반적인 JSON 형식, 누락된 따옴표, 쉼표, 대괄호 등을 확인합니다.

### 크기 제한 오류

* **&quot;키가 최대 크기를 초과합니다.&quot;**: 개별 키는 255바이트를 초과할 수 없습니다.
* **&quot;열 값이 최대 크기&quot;를 초과합니다.**: 개별 분류 값은 255바이트를 초과할 수 없습니다.

## 모범 사례

* **파일 크기**: 50MB는 브라우저 및 API 업로드의 최대 파일 크기입니다.
* **일괄 처리**: 대용량 데이터 세트의 경우 더 작은 파일로 분할하는 것이 좋습니다.
* **데이터 유효성 검사**: 큰 데이터 세트를 업로드하기 전에 작은 샘플 파일로 테스트합니다.
* **백업**: 원본 데이터 파일의 복사본을 보관합니다.
* **증분 업데이트**: 개별 레코드 업데이트 및 삭제를 정확하게 제어하려면 JSON 형식을 사용하십시오.
