---
title: 분류 세트 개요
description: 분류 세트를 사용하여 분류 데이터를 관리합니다.
exl-id: a139b298-1188-42ce-b52f-c71e0ff7c4e3
source-git-commit: 4824170ae2465f3fa04ee588d9571e1cc73d11fc
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 46%

---

# 분류 세트 개요

분류 세트는 분류 및 규칙을 관리할 수 있는 단일 인터페이스를 제공합니다. 이 워크플로는 분류 데이터를 만들고 관리하기 위한 보다 직관적인 인터페이스를 제공하기 위해 보고서 세트 설정에서 분류를 만드는 개념을 분류 가져오기의 개념과 결합합니다.

**[!UICONTROL 구성 요소]** > **[!UICONTROL 분류 세트]**

>[!NOTE]
>
>분류 세트는 보고서 세트를 새로운 분류 아키텍처로 마이그레이션한 모든 고객이 사용할 수 있습니다. 자세한 내용은 Adobe 고객 지원 센터나 귀사의 계정 관리자에게 문의해 주십시오.

분류 세트와 함께 릴리스된 백엔드 아키텍처에는 몇 가지 주목할 만한 개선 사항이 포함되어 있습니다.

* 처리 시간이 크게 단축되었습니다(72시간 → 24시간).
* 분류 세트 UI 사용 기능
* 을 통해 향후에 Adobe Experience Platform에서 분류 데이터를 사용하는 옵션 [분류 데이터를 위한 Adobe Analytics 소스 커넥터](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/classifications.html)

분류 세트와 함께 릴리스된 백엔드 아키텍처에는 몇 가지 주목할 만한 변경 사항이 포함되어 있습니다.

* 브라우저 가져오기를 사용할 때 &#39;[!UICONTROL 충돌 시 덮어쓰기]&#39;은(는) 항상 활성화되어 있습니다.
* 브라우저 가져오기를 사용하는 경우 가져오기 바로 후에 내보내는 옵션이 더 이상 지원되지 않습니다. 내보내기는 별도로 시작해야 합니다.
* Analytics 2.0 API `GetDimensions` 이제 종단점은 숫자 식별자 대신 분류에 대한 문자열 식별자를 반환합니다. 숫자 식별자는 계속 사용할 수 있지만 Adobe은 가능한 경우 새 문자열 식별자를 사용하는 것이 좋습니다. 숫자 식별자는 `?expansion=hidden` 쿼리 문자열 매개 변수가 포함된 랜딩 페이지 URL이 있는지 확인합니다.


분류 세트는 두 가지 주요 영역으로 구성됩니다.

* [**[!UICONTROL 분류 세트 관리자]**](set-manager.md): 분류 세트를 작성, 편집 및 삭제합니다.
* [**[!UICONTROL 분류 세트 작업 관리자]**](job-manager.md): 분류 세트 작업의 상태를 보고 내보내기 파일을 다운로드합니다.
