---
title: 데이터 소스 FAQ
description: 데이터 소스에 대한 FAQ.
exl-id: a948dfe9-289f-43e2-a9e7-7990cf609f5c
feature: Data Sources
role: Admin
source-git-commit: f7d07525c97f4aa145dc46198f883a37cde80158
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 5%

---

# 데이터 소스 FAQ

데이터 소스에 대한 FAQ.

+++데이터 소스 사용 비용은 얼마입니까?
데이터 소스는 요금이 발생하지 않으며 서버 호출 사용량에 계산되지 않습니다. [전체 처리 데이터 원본](full-processing-eol.md)은(는) 사용 중지 전 서버 호출에 계산되었습니다.
+++

+++데이터 소스는 eVar의 속성 및 만료에 어떤 영향을 줍니까?
transactionID가 데이터 소스와 온라인 히트 간에 일치하는 경우, 연결된 eVar 값은 온라인 히트에 설정된 것처럼 동일한 속성 및 만료를 가정합니다.

데이터 소스를 통해 업로드된 다른 모든 데이터에는 어떤 종류의 기여도 또는 만료도 없습니다.
+++

+++데이터 소스는 페이지 보기 수, 방문 횟수 또는 고유 방문자 수와 같은 기본 지표에 어떤 영향을 줍니까?
데이터 소스를 통해 업로드된 데이터는 어떤 식으로든 [페이지 보기 수](/help/components/metrics/page-views.md), [방문 수](/help/components/metrics/visits.md) 또는 [고유 방문자 수](/help/components/metrics/unique-visitors.md)에 영향을 주지 않습니다. 영향을 미치는 유일한 기본 지표에는 [발생 횟수](/help/components/metrics/occurrences.md)가 포함됩니다.
+++

+++데이터 소스를 사용하여 가져온 데이터를 삭제할 수 있습니까?

예. [데이터 복구 API](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/data-repair/)를 사용하여 이 데이터를 삭제할 수 있습니다. Adobe 또한 데이터 소스 데이터를 프로덕션 보고서 세트에 업로드하기 전에 테스트 보고서 세트에 업로드하는 것이 좋습니다.
+++

+++한 번에 얼마나 많은 데이터를 가져올 수 있습니까?

크기가 50MB를 초과하는 경우 처리가 일시 중지되며 총 크기가 50MB 아래로 떨어져야 다시 시작됩니다. FTP 사이트에 있는 모든 파일의 총 크기가 50MB 미만인지 확인하십시오.
+++

+++데이터 소스를 통해 음수 값을 보고에 전달하면 어떻게 됩니까?

그에 따라 값이 감소합니다. 일부 조직에서는 데이터를 수정하기 위해 음수 데이터 소스 값을 사용합니다. 음수 데이터 소스 값은 잠재적으로 원치 않거나 예기치 않은 방식으로 보고서에 영향을 줄 수 있습니다. Adobe은 부정적인 데이터 소스를 마지막 수단으로만 사용할 것을 권장합니다.
+++

+++파일 확장자는 대/소문자를 구분합니까?
예. 확장명이 `.TXT` 또는 `.FIN`인 파일은 처리되지 않습니다. 파일 확장명이 모두 소문자인지 확인하십시오.
+++

+++데이터 소스 파일에 몇 개의 열을 추가할 수 있습니까?
모든 열이 유효한 열이면 원하는 수만큼 데이터 소스 파일에 열을 포함할 수 있습니다. 올바른 변수/열 이름 목록은 [파일 형식](file-format.md)을 참조하세요.
+++

+++Adobe이 제공한 FTP 위치를 사용하지 않고 데이터 소스를 사용할 수 있습니까?
Adobe에 직접 API 호출을 보낼 수 있는 [데이터 원본 API](https://developer.adobe.com/analytics-apis/docs/1.4/guides/data-sources/)를 사용할 수 있습니다. 이러한 API 호출에는 JSON 개체 페이로드로 데이터를 보낼 수 있는 `UploadData` 메서드가 포함되어 있습니다.
+++
