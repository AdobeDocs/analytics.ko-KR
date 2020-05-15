---
description: 이 섹션은 데이터 피드 배달에서 발견되는 파일을 설명합니다.
keywords: Data Feed;job;contents;manifest;file;lookup;hit data;delivery contents
subtopic: data feeds
title: 데이터 피드 콘텐츠 - 개요
topic: Reports and analytics
uuid: 82a86314-4841-4133-a0dc-4e7c6cd14fc1
translation-type: ht
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# 데이터 피드 콘텐츠 - 개요

이 섹션은 데이터 피드 배달에서 발견되는 파일을 설명합니다.

## 매니페스트 파일

매니페스트 파일에는 업로드된 데이터 세트의 일부인 각 파일에 대한 다음 정보가 있습니다.

* 파일 이름
* 파일 크기
* MD5 해시
* 파일에 포함된 레코드 수

매니페스트 파일은 Java JAR 매니페스트 파일과 같은 형식을 따릅니다.

매니페스트 파일은 항상 별도의 `.txt` 파일로 마지막에 제공되므로 그 존재는 요청 기간에 대한 완전한 데이터 세트가 이미 배달되었음을 의미합니다. 매니페스트 파일은 다음에 따라 명명됩니다.

```text
[rsid]_[YYYY-mm-dd].txt
```

일반적인 매니페스트 파일에는 다음과 비슷한 데이터가 포함됩니다.

```text
Datafeed-Manifest-Version: 1.0
 Lookup-Files: 1
 Data-Files: 1
 Total-Records: 611

 Lookup-File: rsid_date-lookup_data.tar.gz
 MD5-Digest: af6de42d8b945d4ec1cf28360085308
 File-Size: 63750

 Data-File: 01-rsid_date.tsv.gz
 MD5-Digest: 9c70bf783cb3d0095a4836904b72c991
 File-Size: 122534
 Record-Count: 611
```

모든 매니페스트 파일에는 조회 파일, 데이터 파일의 총 수, 모든 데이터 파일의 총 레코드 수를 나타내는 헤더가 있습니다. 이 헤더 뒤에는 데이터 피드 배달에 포함된 각 파일에 대한 정보를 포함하는 여러 개의 섹션이 옵니다.

일부 피드는 `.fin` 매니페스트 대신 `.txt` 파일을 받도록 구성되어 있습니다. `.fin`은 업로드가 완료되었으나 업로드에 대한 메타데이터가 없음을 의미합니다.

## 조회 파일

일부 데이터 피드 열은 실제 값에 해당하는 숫자를 출력합니다. 조회 파일은 데이터 피드 열의 숫자를 연결하고 실제 값과 연결하는 데 사용됩니다. 예를 들어 `browser` 히트 데이터 열의 값 &#39;497&#39;은 `browser.tsv` 조회 시 히트가 &quot;Microsoft Internet Explorer 8&quot;에서 왔음을 나타냅니다.

`column_headers.tsv`와 `event_list.tsv`는 데이터 피드와 보고서 세트에 한정됩니다. `browser.tsv`와 같은 다른 파일은 일반적입니다.

조회 파일은 다음에 따라 명명된 zip 압축 파일로 배달됩니다.

```text
[rsid]_[YYYY-mm-dd]-lookup_data.[compression_suffix]
```

* [!DNL column_headers.tsv](이 데이터 피드에 대해 사용자 정의됨)
* [!DNL browser.tsv]
* [!DNL browser_type.tsv]
* [!DNL color_depth.tsv]
* [!DNL connection_type.tsv]
* [!DNL country.tsv]
* [!DNL javascript_version.tsv]
* [!DNL languages.tsv]
* [!DNL operating_systems.tsv]
* [!DNL plugins.tsv]
* [!DNL resolution.tsv]
* [!DNL referrer_type.tsv]
* [!DNL search_engines.tsv]
* [!DNL event_lookup.tsv](이 데이터 피드에 대해 사용자 정의됨)

## 히트 데이터 파일

히트 데이터 파일은 [!DNL hit_data.tsv] 파일에 제공됩니다. 이 파일의 데이터 양은 배달 형식(시간별 또는 일별, 단일 파일 또는 여러 파일)에 따라 결정됩니다. 이 파일은 히트 데이터만 포함합니다. 열 헤더는 조회 파일과 별도로 배달됩니다. 이 파일의 각 행은 하나의 서버 호출을 포함합니다.

Adobe가 배달하는 파일은 사용자가 구성한 데이터 피드 유형에 따라 달라집니다. 모든 파일은 ISO-8859-1을 사용하여 인코딩됩니다.

* `[rsid]`는 데이터 피드를 가져온 보고서 세트 ID를 나타냅니다.
* `[index]`는 여러 파일 피드에서만 사용되며 페이지 번호를 매긴 파일의 올바른 순서를 나타냅니다.
* `[YYYY-mm-dd]`는 데이터 피드가 사용되는 시작일을 나타냅니다.
* `[HHMMSS]`는 시간별 피드에서만 사용되며 데이터 피드가 사용되는 시작 시간을 나타냅니다.
* `[compression_suffix]`는 사용된 압축 유형을 나타냅니다. 일반적으로 데이터 피드는 `tar.gz` 또는 `zip` 파일로 압축됩니다.

### 일별, 단일 파일

하루 동안 데이터가 수집되면 압축된 한 개의 데이터 파일과 매니페스트 파일을 받게 됩니다. 데이터 파일의 이름은 다음과 같습니다.

`[rsid]_[YYYY-mm-dd].[compression_suffix]`

데이터 파일의 압축을 해제하면 해당 날짜의 모든 데이터가 포함된 단일 `hit_data.tsv` 파일과 필요한 열에 대한 조회 파일이 포함됩니다.

### 일별, 여러 파일

하루 동안 데이터가 수집되면 압축된 한 개 이상의 데이터 파일과 매니페스트 파일을 받게 됩니다. 데이터 파일의 이름은 다음과 같습니다.

`[index]-[rsid]_[YYYY-mm-dd].[compression_suffix]`

각 데이터 파일의 압축을 해제하면 약 2GB의 압축되지 않은 데이터가 포함된 단일 `hit_data.tsv` 파일과 필요한 열에 대한 조회 파일이 포함됩니다.

### 시간별, 단일 파일

한 시간 동안 데이터가 수집되면 압축된 한 개의 데이터 파일과 매니페스트 파일을 받게 됩니다. 데이터 파일의 이름은 다음과 같습니다.

`[rsid]_[YYYY-mm-dd]-[HHMMSS].[compression_suffix]`

데이터 파일의 압축을 해제하면 해당 시간의 모든 데이터가 포함된 단일 `hit_data.tsv` 파일과 필요한 열에 대한 조회 파일이 포함됩니다.

### 시간별, 여러 파일

한 시간 동안 데이터가 수집되면 압축된 한 개 이상의 데이터 파일과 매니페스트 파일을 받게 됩니다. 데이터 파일의 이름은 다음과 같습니다.

`[index]-[rsid]_[YYYY-mm-dd]-[HHMMSS].[compression_suffix]`

각 데이터 파일의 압축을 해제하면 약 2GB의 압축되지 않은 데이터가 포함된 단일 `hit_data.tsv` 파일과 필요한 열에 대한 조회 파일이 포함됩니다.

## 데이터 파일 크기

히트 데이터 파일 크기는 능동적으로 사용되는 변수 개수와 보고서 세트에 전송된 트래픽양에 따라 크게 달라집니다. 하지만 평균적으로 데이터 행은 500B(압축) 또는 2KB(비압축)입니다. 여기에 서버 호출 횟수를 곱하면 데이터 피드의 크기를 대략 예상할 수 있습니다. 조직에서 데이터 피드 파일을 받기 시작하면 `hit_data.tsv`의 행 수를 총 파일 크기로 나누어 더 정확한 숫자를 찾을 수 있습니다.
