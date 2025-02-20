---
description: 세그먼트 빌더에서 선택한 연산자를 사용하여 값을 비교하고 제한할 수 있습니다.
title: 세그먼트의 비교 연산자
feature: Segmentation
exl-id: 1ec1ff05-03a9-4151-8fcb-a72ebbce87dd
source-git-commit: 08e29da4847e8ef70bd4435949e26265d770f557
workflow-type: tm+mt
source-wordcount: '1104'
ht-degree: 94%

---

# 세그먼트의 비교 연산자

세그먼트 빌더에서 선택한 연산자를 사용하여 값을 비교하고 제한할 수 있습니다. 연산자 범주로는 표준, Data Warehouse 및 고유 개수, 이렇게 세 가지가 있습니다.

유일하게 지원되는 와일드카드 문자는 별표(&#42;)입니다. &#42;을(를) 검색해야 하는 경우 백슬래시로 이스케이프할 수 있습니다.

**예**: &quot;My cool product&quot;라는 페이지 이름이 있다고 가정해 봅시다. 세그먼트 규칙 &quot;페이지 이름 일치 My&#42;product&quot;는 위의 페이지 이름과 일치합니다. 그러나 &quot;페이지 이름 일치 My\\&#42;product&quot; 규칙은 &quot;My&#42;Product&quot; 페이지 이름만 일치합니다.

## 표준 연산자

| 연산자 | 선택한 차원, 세그먼트 또는 지표 이벤트... |
|--- |--- |
| 다음과 같음 | 숫자나 문자열 값에 대해 정확히 일치하는 항목을 반환합니다. 참고: 와일드카드 문자를 사용하는 경우 &quot;일치&quot; 연산자를 사용하십시오. |
| 다음과 같지 않음 | 입력한 값의 정확한 일치를 포함하지 않는 모든 항목을 반환합니다.  참고: 와일드카드 문자를 사용하는 경우 &quot;일치하지 않음&quot; 연산자를 사용하십시오. |
| 다음 중 1개 이상의 항목과 같음 | 입력 필드의 값 (최대 500개 항목)에 대해 정확히 일치하는 항목을 반환합니다. 예를 들어 이 연산자와 함께 &quot;검색 결과, 홈 페이지&quot;를 입력하면 &quot;검색 결과&quot; 및 &quot;홈 페이지&quot;가 일치하고 2개 항목으로 계산됩니다. 이 연산자의 입력 필드는 쉼표로 구분됩니다. |
| 다음 중 같은 항목 없음 | 입력 필드의 값 (최대 500개 항목)에 대해 정확히 일치하는 항목을 식별한 다음 이러한 값이 없는 항목만 반환합니다. 예를 들어 이 연산자와 함께 &quot;검색 결과, 홈 페이지&quot;를 입력하면 &quot;검색 결과&quot; 및 &quot;홈 페이지&quot;를 식별한 다음 반환된 항목에서 이 항목들을 제외합니다. 이 예는 2개 항목으로 카운트됩니다. 이 연산자의 입력 필드는 쉼표로 구분됩니다. |
| 다음 포함 | 입력한 값의 하위 문자열에 해당하는 항목을 반환합니다. 예를 들어 &quot;Page&quot;에 대한 규칙에 &quot;Search&quot;가 포함되어 있으면 &quot;Search Results&quot;, &quot;Search&quot; 및 &quot;Searching&quot;을 비롯하여 하위 문자열 &quot;Search&quot;가 포함된 모든 페이지가 검색됩니다. &quot;포함&quot; 조항은 Adobe Analytics에서 대소문자를 구분하지 않지만, Customer Journey Analytics에서는 대소문자를 구분합니다. |
| 다음을 포함하지 않음 | &quot;포함&quot; 규칙의 반대 경우를 반환합니다. 구체적으로 말하면 입력한 값과 일치하는 모든 항목이 입력된 값에서 제외됩니다. 예를 들어 &quot;Page&quot;에 대한 규칙에 &quot;Search&quot;가 포함되어 있지 않으면 &quot;Search Results&quot;, &quot;Search&quot; 및 &quot;Searching&quot;을 비롯하여 하위 문자열 &quot;Search&quot;가 포함된 모든 페이지가 검색되지 않습니다. 이러한 값은 결과에서 제외됩니다. |
| 모두 포함 | 여러 값이 함께 연결된 경우를 비롯하여 하위 문자열에 해당하는 항목을 반환합니다. 예를 들어 이 연산자를 사용하여 &quot;Search Results&quot;를 입력하면 &quot;Search Results&quot; 및 &quot;Results of Search&quot;는 검색되지만 &quot;Search&quot; 또는 &quot;Results&quot;만 따로 나오는 경우는 검색되지 않습니다. Search와 Results가 함께 나오는 경우가 검색됩니다. 이 연산자의 입력 필드는 공백으로 구분합니다 (100단어). |
| 다음을 모두 포함하지 않음 | 부분 문자열과 비교하여 항목을 식별하고 (함께 결합된 여러 값 포함) 이 값이 없는 항목만 반환합니다. 예를 들어 이 연산자와 함께 &quot;Search Results&quot;를 입력하면 &quot;Search Results&quot; 및 &quot;Results of Search&quot;를 찾아 (하지만 &quot;Search&quot; 또는 &quot;Results&quot;만 따로 나오는 경우는 찾지 않음) 이 항목들을 제외합니다. 이 연산자의 입력 필드는 공백으로 구분합니다 (100단어). |
| 하나로도 포함 | 여러 값이 함께 연결되거나 개별적으로 식별되는 경우를 비롯하여 하위 문자열에 해당하는 항목을 반환합니다. 예를 들어 이 연산자를 사용하여 &quot;Search Results&quot;를 입력하면 &quot;Search Results&quot;, &quot;Results of Search&quot;, &quot;Search&quot; 및 &quot;Results&quot;는 일치하는 것으로 검색됩니다. Search 또는 Results가 함께 나오거나 따로 나오는 경우 모두 일치하는 것으로 검색됩니다. 이 연산자의 입력 필드는 공백으로 구분합니다 (100단어). |
| 하나도 포함 안 함 | 부분 문자열을 기반으로 항목을 식별한 다음 이 하위 문자열이 없는 값을 반환합니다. 여러 개의 결합된 값이나 독립적으로 식별되는 값이 있을 수 있습니다. 예를 들어 &quot;Search Results&quot;를 입력하면 &quot;Search&quot; 또는 &quot;Results&quot; 중 하나가 각각 독립적으로 일치하거나 둘 다가 일치하는 &quot;Search Results&quot;, &quot;Results of Search&quot;, &quot;Search&quot;, &quot;Results&quot;를 찾습니다. 그런 다음 이 부분 문자열이 들어 있는 항목을 제외합니다. 이 연산자의 입력 필드는 공백으로 구분합니다 (100단어). |
| 다음으로 시작 | 입력한 값의 문자 또는 문자열로 시작되는 항목을 반환합니다. |
| 다음으로 시작하지 않음 | 입력한 값의 문자 또는 문자열로 시작하지 않는 모든 항목을 반환합니다. &quot;다음으로 시작&quot; 연산자의 역입니다. |
| 다음으로 끝남 | 입력한 값의 문자 또는 문자열로 끝나는 항목을 반환합니다. |
| 다음으로 끝나지 않음 | 입력한 값의 문자 또는 문자열로 끝나지 않는 모든 항목을 반환합니다. &quot;다음으로 끝남&quot; 연산자의 역입니다. |
| matches | 지정된 숫자나 문자열 값을 기반으로 정확히 일치하는 항목을 반환합니다. &quot;일치&quot; 조항은 Adobe Analytics 및 Customer Journey Analytics에서 대소문자를 구분합니다. **참고**: 와일드카드(globbing) 기능 사용 시 이 연산자를 사용하십시오. &quot;globbing&quot; 예시:<ul><li>`a*e`는 `ae`, `abcde`, `adobe`, `a whole sentence`와 일치합니다</li><li>`adob*`는 `adobe`, `adobe analytics`, `adobo recipe`와 일치합니다</li><li>`*dobe`는 `dobe`, `adobe`, `cute little dobe`와 일치합니다</li></ul> |
| 일치하지 않음 | 입력한 값의 정확한 일치를 포함하지 않는 모든 항목을 반환합니다. 참고: 와일드카드 (globbing) 기능 사용 시 이 연산자를 사용하십시오. |
| 존재 | 존재하는 항목의 수를 반환합니다. 예를 들어 &quot;존재&quot; 연산자를 사용하여 페이지를 찾을 수 없음 차원을 평가하는 경우, 존재하는 오류 페이지 수가 반환됩니다. |
| 존재하지 않음 | 존재하지 않는 모든 항목을 반환합니다. 예를 들어 &quot;존재하지 않음&quot; 연산자를 사용하여 페이지를 찾을 수 없음 차원을 평가하는 경우, 이 오류 페이지가 존재하지 않았던 페이지의 수가 반환됩니다. |

## Data Warehouse 연산자

| 연산자 | 선택한 차원, 세그먼트 또는 지표 이벤트... |
| --- | --- |
| 보다 작음 | 숫자 값이 입력한 값보다 작은 항목을 반환합니다. |
| 다음보다 작거나 같음 | 숫자 값이 입력한 값보다 작거나 같은 항목을 반환합니다. |
| 보다 큼 | 숫자 값이 입력한 값보다 큰 항목을 반환합니다. |
| 다음보다 크거나 같음 | 숫자 값이 입력한 값보다 크거나 같은 항목을 반환합니다. |

## 고유 개수 연산자

차원 내에서 항목의 고유 개수를 세그먼트화할 수 있습니다. 예: &quot;5개 이상의 고유 제품을 본 방문자&quot; 또는 &quot;5개 이상의 고유 페이지를 본 방문 위치&quot;

| 연산자 | 선택한 차원, 세그먼트 또는 지표 이벤트... |
| --- | --- |
| 다음과 같음 | 고유 카운트가 입력한 값과 같은 차원 항목을 반환합니다. |
| 다음과 같지 않음 | 고유 카운트가 입력한 값과 같지 않은 차원 항목을 반환합니다. |
| 보다 큼 | 고유 카운트가 입력한 값보다 큰 차원 항목을 반환합니다. |
| 보다 작음 | 고유 카운트가 입력한 값보다 작은 차원 항목을 반환합니다. |
| 다음보다 크거나 같음 | 고유 카운트가 입력한 값보다 크거나 같은 차원 항목을 반환합니다. |
| 다음보다 작거나 같음 | 고유 카운트가 입력한 값보다 작거나 같은 차원 항목을 반환합니다. |


>[!BEGINSHADEBOX]

데모 비디오는 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [개별 차원 개수](https://video.tv.adobe.com/v/27257?quality=12&learn=on){target="_blank"}를 참조하십시오.

>[!ENDSHADEBOX]
