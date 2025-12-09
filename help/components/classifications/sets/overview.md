---
title: 분류 세트 개요
description: 분류 세트를 사용하여 분류 데이터를 관리하는 방법을 알아봅니다. 분류 세트가 기존 분류와 어떻게 다른지 이해합니다.
exl-id: a139b298-1188-42ce-b52f-c71e0ff7c4e3
feature: Classifications
source-git-commit: 5256319752fb6521ef86c1dde9d3624689879ecb
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 9%

---

# 분류 세트 개요

분류 세트는 분류 및 규칙을 관리할 수 있는 단일 인터페이스를 제공합니다. 이 워크플로는 보고서 세트 설정의 분류 만들기를 [분류 가져오기](/help/components/classifications/sets/manage/set-manager.md)와 결합합니다. 따라서 분류 데이터를 만들고 관리할 수 있는 직관적인 단일 인터페이스가 제공됩니다.


## 분류 세트 대 기존 분류

분류 세트와 레거시 분류 간의 주요 차이점은 레거시 분류가 세 가지 인터페이스에 의존하는 한 인터페이스에서 분류 세트가 모든 기능을 결합한다는 것입니다.

### 레거시 분류

![기존 분류](/help/components/classifications/sets/assets/classifications-legacy.svg)

기존 분류에서 분류 ![스키마](/help/assets/icons2/Schema.svg)(트래픽, 전환, 마케팅 채널 등)에는 각각 고유한 차원(키 ![키](/help/assets/icons2/Key.svg))이 있습니다. 이러한 분류를 [보고서 세트 설정](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/conversion-classifications.md)의 일부로 정의합니다.

![BidRule](/help/assets/icons/BidRule.svg) 규칙을 [분류 규칙 빌더](/help/components/classifications/crb/classification-rule-builder.md) 인터페이스의 일부로 규칙 집합에 별도로 정의합니다. 해당 인터페이스에서 규칙 세트를 하나 이상의 보고서 세트와 연결합니다.

[분류 가져오기](/help/components/classifications/importer/c-working-with-saint.md)를 사용하여 템플릿 ![DocumentFragment](/help/assets/icons/DocumentFragment.svg)을(를) 다운로드하거나, ![UploadToCloud](/help/assets/icons/UploadToCloud.svg) 분류를 보고서 세트 - 키(데이터 세트) 조합으로 가져오거나, ![Download](/help/assets/icons/Download.svg) 분류를 내보냅니다.



### 분류 설정

![분류 집합](./assets/classifications-sets.svg)

분류 세트는 모든 기존 분류 인터페이스를 하나로 결합합니다. 각 분류 세트는 다음을 정의합니다.

* 분류할 보고서 세트 ![데이터](/help/assets/icons2/Data.svg)와(과) 차원 ![키](/help/assets/icons2/Key.svg)(키)의 조합인 하나 이상의 구독입니다. 제품 SKU를 기반으로 제품을 분류하려면 적용 가능한 제품 SKU 차원으로 모든 보고서 세트를 정의할 수 있습니다. 또한 기존 분류 인터페이스처럼 보고서 세트 간에 분류를 복제할 필요가 없습니다.
* 키에 대한 분류 ![스키마](/help/assets/icons2/Schema.svg)(스키마) 목록입니다. 예를 들어 제품 분류의 경우 카테고리, 색상, 크기, 성별 등을 지정할 수 있습니다. 분류를 정의하면 템플릿 ![DocumentFragment](/help/assets/icons/DocumentFragment.svg)을(를) 다운로드하고, 분류 데이터를 ![UploadToCloud](/help/assets/icons/UploadToCloud.svg)업로드하고, 분류 데이터를 ![다운로드](/help/assets/icons/Download.svg)하는 등의 작업을 수행할 수 있습니다.
* 분류를 지원하는 하나 이상의 규칙 ![BidRule](/help/assets/icons/BidRule.svg).


Adobe Analytics 인터페이스의 **[!UICONTROL 구성 요소]** 메뉴에서 **[!UICONTROL 분류 세트]**&#x200B;에 액세스하려면 제품 관리자이거나 권한 항목 [!UICONTROL 보고서 세트 도구] > [!UICONTROL 분류]를 포함하는 제품 프로필에 속해 있어야 합니다. 레거시 분류 관리 인터페이스는 **[!UICONTROL 관리자]** 메뉴에서 사용할 수 있습니다.

분류 세트는 세 가지 기능 영역으로 구성됩니다.

* [**[!UICONTROL 분류 세트]**](manage/set-manager.md): 분류 세트를 만들고, 편집하고, 삭제합니다.
* [**[!UICONTROL 작업]**](job-manager.md): 분류 세트 작업의 상태를 봅니다.
* [**[!UICONTROL 통합]**](consolidations/manage.md): 여러 분류 세트를 하나의 분류 세트로 결합합니다.


## 워크플로

분류 세트에 대한 워크플로우는 일반적으로 다음 단계를 포함합니다.

1. 분류 세트를 생성할 보고서 세트 및 차원 조합을 고려합니다. 예를 들어, 더 자세한 정보를 사용하여 제품을 분류할 보고서 세트에 대해 생성하는 제품 분류 세트를 정의할 수 있습니다. 예를 들어 카테고리와 색상 등의 세부 사항이 있습니다.
1. 제품을 식별하는 하나 이상의 보고서 세트 및 키 차원 조합에 대한 구독이 있는 [분류 세트를 만듭니다](/help/components/classifications/sets/manage/create.md). 예:

   | 보고서 세트 | 주요 차원 |
   |---|---|
   | 보고서 세트 1 | 제품 ID |
   | 보고서 세트 2 | 제품 SKU |

1. [식별한 분류를 &#x200B;](/help/components/classifications/sets/manage/schema.md#add) 분류 집합 스키마에 추가합니다. 예:

   | 분류 이름 | ID 이름 |
   |---|---|
   | 카테고리 | 범주 |
   | 색상 | 색상 |

1. 분류 데이터가 포함된 파일을 수동으로 만듭니다. [템플릿을 사용](/help/components/classifications/sets/manage/schema.md#template)하여 [지원되는 파일 형식](data-files.md#classification-set-file-formats) 및 파일의 열을 사용하도록 하세요. 그런 다음 템플릿 파일에 데이터를 추가합니다.

   또는 제품 카탈로그에서 템플릿을 준수하는 열을 사용하여 [지원되는 파일 형식](data-files.md#classification-set-file-formats)으로 직접 데이터를 내보낼 수 있습니다. 예를 들어 다음과 같은 CSV 파일:

   ```
   Key,Category,Color
   Adobe Nike Tech Fleece Full-Zip Hoodie - Men's,Men,Black
   Adobe Nike Tech Fleece Full-Zip Hoodie - Women's,Women,Black
   Men's North Face Adobe Jacket,Men,Black
   Nike Air Hybrid 2 Golf Bag,Equipment,Blue
   STITCH&reg; Ultimate Garment Bag,Equipment,Brown
   Adobe Analytics Training Tee - Navy,Men,Navy
   AirPods Pro 2,Electronics,White
   Adobe Analytics Training Tee - Green,Men,Green
   Women's North Face Adobe Jacket,Women,Blue
   Adobe Analytics Training Tee - Grey,Men,Gray
   Adobe Analytics One Million Views - Grey,Equipment,Grey
   Adobe and MGM Tee - White,Women,White
   Adobe and MGM Tee - Charcoal,Women,Charcoal
   ```

   분류 데이터 파일에서 **[!UICONTROL 을(를) 사용하는 각 보고서 세트(예:]**&#x200B;제품 ID **[!UICONTROL 및]**&#x200B;제품 SKU`Key`)의 키 차원을 참조합니다. **[!UICONTROL 분류 이름]**(예: `Category` 또는 `Color`)을 사용하여 각 분류를 참조합니다.

1. 분류 데이터가 포함된 파일을 분류 집합 스키마에 [업로드](/help/components/classifications/sets/manage/schema.md#upload)합니다.

1. [규칙](manage/rules.md)을(를) 설정하여 과거의 수신 데이터와 데이터를 자동으로 분류합니다.

1. 클라우드 위치를 사용하여 분류 데이터에 반영하려는 제품 카탈로그 업데이트 프로세스를 [자동화](/help/components/classifications/sets/manage/schema.md#automate)합니다.

1. 콘텐츠의 유효성을 검사하려면 분류 데이터를 [다운로드](/help/components/classifications/sets/manage/schema.md#download)하십시오.

1. 분류에 대한 작업(업로드, 다운로드, 템플릿 등)의 결과를 확인하려면 [작업 기록을 검사하십시오](/help/components/classifications/sets/job-manager.md).
1. 기존 분류 기능에서 마이그레이션한 결과로 유사한 분류 세트가 여러 개 있는 경우 이러한 분류 세트를 [통합](consolidations/manage.md)합니다.



## 개선 사항

분류 세트와 함께 릴리스된 백엔드 아키텍처에는 몇 가지 개선 사항이 포함됩니다.

* 처리 시간이 72시간에서 24시간으로 단축되었습니다.
* 분류를 관리하기 위해 다시 설계된 사용자 인터페이스입니다.
* 분류 데이터에 대한 [Adobe Experience Platform 소스 커넥터](https://experienceleague.adobe.com/ko/docs/experience-platform/sources/connectors/adobe-applications/classifications)를 통해 Adobe Analytics에서 분류 데이터를 사용하는 옵션입니다.

분류 세트와 함께 릴리스된 백엔드 아키텍처에는 다음과 같은 몇 가지 변경 사항도 포함됩니다.

* 브라우저 또는 자동 가져오기를 사용하는 경우 **[!UICONTROL 충돌 시 덮어쓰기]**&#x200B;가 항상 활성화되어 있습니다.
* 브라우저 또는 자동화된 가져오기를 사용할 때 가져오기 직후 내보내기 옵션은 더 이상 지원되지 않습니다. 내보내기는 별도로 시작해야 합니다.
* 이제 Analytics 2.0 `GetDimensions` API 끝점이 숫자 식별자 대신 분류에 대한 문자열 식별자를 반환합니다. 숫자 식별자는 계속 사용할 수 있지만 가능하면 새 문자열 식별자를 사용하는 것이 좋습니다. 숫자 식별자는 `?expansion=hidden` 쿼리 문자열 매개변수를 사용하여 검색할 수 있습니다.

>[!IMPORTANT]
>
>분류 세트 성능은 주로 데이터가 포함된 고유 키 값의 수에 따라 달라집니다. 고유 값이 많이 포함된 변수가 있을 때는 주의하십시오. 특히 여러 보고서 세트 및 차원의 이러한 변수를 단일 분류 세트로 결합할 때 유용합니다.

## 제한 사항

* 분류 세트는 아직 규칙을 지원하지 않습니다. [레거시 규칙 빌더](/help/components/classifications/crb/classification-rule-builder.md) 기능을 사용할 수 없게 되기 전에 규칙 기능이 분류 세트 인터페이스에 추가됩니다.
* 이전 분류 규칙 및 구성을 분류 세트로 마이그레이션하지 않습니다. 이전 분류 기능을 사용할 수 없게 되기 전에 마이그레이션 유틸리티가 분류 세트 인터페이스에 추가됩니다.
