---
description: 사전 정의된 템플릿을 선택하거나 기존 보고서 세트 중 하나를 모델로 사용하여 새 보고서 세트를 생성할 수 있습니다.
title: 새 보고서 세트 - 설정
feature: Report Suite Settings
uuid: 3508f684-11a3-4c8f-a233-bea6bafd57c0
exl-id: ea5f8543-058d-4e08-bc66-575e3a7460c2
source-git-commit: 8c0e88a22928d79599ab0a0ad3efc8159712d739
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 94%

---

# 새 보고서 세트 - 설정

사전 정의된 템플릿을 선택하거나 기존 보고서 세트 중 하나를 모델로 사용하여 새 보고서 세트를 생성할 수 있습니다.

[보고서 세트를 만들](/help/admin/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md) 때 사용되는 요소에 대한 설명입니다.

>[!NOTE]
>
>[가상 보고서 세트 설명서](/help/components/vrs/c-workflow-vrs/vrs-create.md)는 가상 보고서 세트를 생성하는 방법을 보여 줍니다.

| 요소 | 설명 |
| --- | --- |
| 보고서 세트 ID | 영숫자만 포함한 고유 ID를 지정합니다. 이 ID는 생성하고 나면 변경할 수 없습니다. Adobe가 필수 ID 접두사를 설정하므로 어느 것도 변경할 수 없습니다.  여러 보고서 세트를 생성할 경우, 고유한 보고서 세트 ID를 보장할 수 있는 이름 지정 규칙을 사용해야 합니다. |
| 사이트 제목 | 관리 도구에서 보고서 세트를 식별합니다. 이 제목은 세트 헤더의 보고서 세트 드롭다운 목록에서도 사용됩니다. |
| 시간대 | 이벤트 및 타임스탬프 데이터를 예약합니다. |
| 기본 URL | (선택 사항) 보고서 세트에 대한 기준 도메인을 정의합니다. 보고서 세트의 내부 URL 필터를 명시적으로 정의하지 않는 경우 이 URL은 내부 URL 필터로 작동합니다. |
| 기본 페이지 | (선택 사항) 기본 페이지 값이 발생하는 URL에서 해당 값을 제거합니다. 가장 방문 빈도가 높은 페이지 보고서가 페이지 이름이 아닌 URL을 포함하는 경우 이 설정은 동일한 웹 페이지에 대한 여러 URL을 방지합니다.  예를 들어 URL `https://example.com` 및 `https://example.com/index.html`은 일반적으로 동일한 페이지입니다.<p> 불필요한 파일 이름을 제거하여 보고서에서 이러한 URL을 모두 `https://example.com`으로 표시되도록 할 수 있습니다. 이 값을 설정하지 않으면 Analytics는 URL에서 파일 이름 `index.htm`, `index.html`, `index.cgi`, `index.asp`, `default.htm`, `default.html`, `default.cgi`, `default.asp`, `home.htm`, `home.html`, `home.cgi` 및 `home.asp`를 자동으로 제거합니다. 파일 이름 제거를 비활성화하려면 URL에서 발생하지 않는 기본 페이지 값을 지정합니다. |
| Go-Live 날짜 | 이 보고서 세트가 활성화될 것으로 예상하는 날짜를 Adobe에 알려 줍니다. 배포 일정이 변경되면 트래픽 관리에서 영구적인 예상 트래픽 도구를 사용하여 업데이트된 예상 트래픽을 제공합니다. |
| 일별 예상 페이지 조회수 | 이 보고서 세트가 하루에 지원할 수 있을 것으로 예상되는 페이지 조회수를 식별합니다. 트래픽 볼륨이 크면 승인 프로세스에 더 오랜 시간이 걸립니다. 처리 지연을 방지하기 위해 가능한 정확하게 이 수를 예상하십시오. |
| 기본 통화 | 모든 통화 데이터를 저장하는 데 사용되는 기본 통화를 지정합니다. Analytics는 데이터를 받을 때 현재 전환율을 사용하여 다른 통화의 거래를 기본 통화로 전환합니다. Analytics 보고는 currencyCode JavaScript 변수를 사용하여 주어진 거래 통화를 확인합니다. |
| 일본어 키워드 처리 활성화 | 보고서 세트에 대한 멀티바이트 문자 지원을 활성화합니다. 멀티바이트 문자 지원을 비활성화하면 시스템에서는 데이터를 `ISO-8859-1` 형식으로 간주합니다. 웹 페이지는 charSet JavaScript 변수에서 해당 문자 세트를 지정해야 합니다. <p>멀티바이트 문자 지원은 UTF-8을 사용하여 보고서 세트의 문자를 저장합니다. 수신 시 시스템에서는 웹 페이지의 문자 세트 데이터를 UTF-8 문자 세트로 전환하므로 마케팅 보고서에서 모든 언어를 사용할 수 있습니다.  기존 보고서 세트에 대한 멀티바이트 문자 지원을 변경하려면 Adobe 계정 팀 또는 고객 지원 센터에 문의하십시오. |
| 간소화된 탐색 메뉴 사용 | 이 기능은 더 이상 지원되지 않는 [Reports &amp; Analytics](https://new.express.adobe.com/webpage/WFCyq7w8kijmB?)의 일부입니다. |

{style="table-layout:auto"}
