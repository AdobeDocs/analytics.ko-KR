---
title: 분류 세트 개요
description: 분류 세트를 사용하여 분류 데이터를 관리합니다.
exl-id: a139b298-1188-42ce-b52f-c71e0ff7c4e3
source-git-commit: 05243d37d252274d88650566de049327ff2bd439
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 26%

---

# 분류 세트 개요

분류 세트는 분류 및 규칙을 관리하는 단일 인터페이스를 제공합니다. 이 워크플로는 분류 데이터를 만들고 관리하기 위한 보다 직관적인 인터페이스를 제공하기 위해 보고서 세트 설정에서 분류를 만드는 개념을 분류 가져오기의 개념과 결합합니다.

**[!UICONTROL 구성 요소]** > **[!UICONTROL 분류 세트]**

분류 세트와 함께 릴리스된 백엔드 아키텍처에는 몇 가지 주목할 만한 개선 사항이 포함되어 있습니다.

* 처리 시간 단축(72시간 → 24시간)
* 분류 세트 UI 사용 기능
* [분류 데이터용 Adobe Analytics 소스 커넥터](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/classifications.html)를 통해 향후 Adobe Experience Platform에서 분류 데이터를 사용하는 옵션

분류 세트와 함께 릴리스된 백엔드 아키텍처에는 몇 가지 주목할 만한 변경 사항이 포함됩니다.

* 브라우저 또는 자동화된 가져오기를 사용할 때 &#39;[!UICONTROL 충돌 시 덮어쓰기]&#39; 은 항상 활성화되어 있습니다.
* 브라우저 또는 자동화된 가져오기를 사용하는 경우 가져오기 직후 내보내는 옵션이 더 이상 지원되지 않습니다. 내보내기는 별도로 시작해야 합니다.
* Analytics 2.0 API `GetDimensions` 엔드포인트는 이제 숫자 식별자 대신 분류에 대한 문자열 식별자를 반환합니다. 숫자 식별자를 계속 사용할 수 있지만 가능한 경우 새 문자열 식별자를 사용하는 것이 좋습니다. 숫자 식별자는 `?expansion=hidden` 쿼리 문자열 매개변수를 사용하여 검색할 수 있습니다.

>[!IMPORTANT]
>
>분류 세트의 성능은 주로 데이터가 포함된 고유한 키 값의 수에 따라 다릅니다. Adobe은 고유 값이 많이 포함된 변수를 처리할 때 주의할 것을 권장합니다. 이 주의는 여러 보고서 세트 및 차원의 변수를 단일 분류 세트로 결합할 때 특히 적용됩니다.

분류 세트는 다음 세 가지 주요 영역으로 구성됩니다.

* [**[!UICONTROL 분류 세트 관리자]**](manage/set-manager.md): 분류 세트를 작성, 편집 및 삭제합니다.
* [**[!UICONTROL 분류 세트 작업 관리자]**](job-manager.md): 분류 세트 작업의 상태를 보고 내보내기 파일을 다운로드합니다.
* [**[!UICONTROL 분류 세트 통합]**](consolidations/manage.md): 여러 분류 세트를 하나의 분류 세트로 결합합니다.
