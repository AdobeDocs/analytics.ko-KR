---
description: Data Warehouse 요청을 만드는 방법을 설명하는 단계입니다.
title: Data Warehouse 요청에 대한 보고서 옵션 구성
feature: Data Warehouse
exl-id: b273bddb-431c-44d9-82a5-cb088829b3a3
source-git-commit: 1bd46f104c5ebcca78d624b49c56b2992c3d62cb
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 9%

---

# Data Warehouse 요청에 대한 보고서 옵션 구성

Data Warehouse 요청을 만들 때 사용할 수 있는 구성 옵션은 다양합니다. 다음 정보는 요청에 대한 보고서 옵션을 구성하는 방법을 설명합니다.

요청 만들기를 시작하는 방법과 기타 중요한 구성 옵션에 대한 링크에 대한 자세한 내용은 을 참조하십시오. [Data Warehouse 요청 만들기](/help/export/data-warehouse/create-request/t-dw-create-request.md).

Data Warehouse 요청에 대한 보고서 옵션을 구성하려면 다음 작업을 수행하십시오.

1. 다음을 선택하여 Adobe Analytics에서 요청 만들기 시작 **[!UICONTROL 도구]** > **[!UICONTROL Data Warehouse]** > [!UICONTROL **추가**].

   자세한 내용은 [Data Warehouse 요청 만들기](/help/export/data-warehouse/create-request/t-dw-create-request.md).

1. 새 Data Warehouse 요청 페이지에서 [!UICONTROL **보고서 옵션**] 탭.

   ![보고서 대상 탭](assets/dw-report-options.png) <!-- update screenshot to include Sort by metrics -->

1. 다음 필드를 완료합니다. 

   | 옵션 | 함수 |
   |---------|----------|
   | [!UICONTROL **파일 이름**] | 보고서를 식별합니다. <p>파일 이름에 다음 특수 문자가 사용되는 경우 요청을 저장할 수 없습니다. <code>! &quot; # $ &amp; &#39; ( ) * + , / : ; > = &lt; ? @ [ ] \ ^ ` { } \| ~</code> </p><p>% 문자 뒤에는 다음과 같이 &quot;R&quot;, &quot;rsid&quot; 또는 &quot;id&quot;가 와야 사용할 수 있습니다. <code>%R</code>, <code>%rsid</code>, 및 <code>%id</code>.</p> |
   | [!UICONTROL **파일 이름에 보고서 날짜 범위 추가**] | 보고서 파일 이름에 날짜 범위를 추가합니다. <p>예를 들어 2024년 5월 1일부터 2024년 5월 7일까지의 데이터를 요청하는 경우 파일 이름에 20240501 - 20240507 날짜 범위가 포함됩니다.</p> |
   | [!UICONTROL **CSV**] | 스프레드시트에서 데이터를 보기 위해 보고서를 CSV 파일 형식으로 전달합니다. |
   | [!UICONTROL **타블로(TDE)**] | 보고서를 TDE(타블로 데이터 추출) 파일 형식으로 전달합니다. 이 파일 형식은 타블로 내에서 추가 데이터로 데이터와 레이어를 시각화하는 데 사용할 수 있습니다. |
   | [!UICONTROL **보고서를 압축 파일(ZIP)로 보내기**] | 보고서를 압축(ZIP) 파일 형식으로 전달합니다. 이메일을 로 사용할 때는 이 옵션을 활성화하는 것이 좋습니다. [보고서 대상](/help/export/data-warehouse/create-request/dw-request-report-destinations.md). |
   | [!UICONTROL **모든 행 반환**] | 활성화되면 모든 행이 보고서에 포함됩니다. 포함할 행 수를 지정하려면 이 옵션을 비활성화합니다. |
   | [!UICONTROL **보고서 주석 시작**] | 보고서에 포함할 주석을 추가합니다. 주석은 보고서 시작 부분에 나타납니다. |
   | [!UICONTROL **지표로 정렬**] | 내림차순 지표 값으로 정렬된 Data Warehouse의 등급 분류 보고서를 제공합니다. 지표로 정렬하면 Data Warehouse 보고서를 해석하기가 더 쉬워지고, 이 보고서를 다른 Analytics 분류 보고 보기와 더 쉽게 비교할 수 있게 됩니다.<p>자세한 내용은 [지표로 정렬](/help/export/data-warehouse/sorting-by-metric.md).</p> |
   | [!UICONTROL **매니페스트 파일 보내기**] | 보고서에 포함된 파일에 대한 메타데이터를 포함합니다.<!-- What kind of metadata is included in the manifest file? --> |
   | [!UICONTROL **디지털 서명 파일 보내기**] | 보고서 수신자는 Adobe에서 파일을 받았으며 변경되지 않았는지 확인할 수 있습니다. |
   | [!UICONTROL **보고서에 데이터가 없으면 빈 파일을 보냅니다.**] | 보고서에 데이터가 포함되지 않은 경우에도 보고서를 보냅니다. |

   {style="table-layout:auto"}

1. 에서 Data Warehouse 요청 구성 계속 [!UICONTROL **예약 옵션**] 탭. 자세한 내용은 [Data Warehouse 요청에 대한 예약 옵션 구성](/help/export/data-warehouse/create-request/dw-request-scheduling.md).
