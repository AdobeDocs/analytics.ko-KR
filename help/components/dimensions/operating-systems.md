---
title: 운영 체제
description: 방문자의 운영 체제입니다.
feature: Dimensions
exl-id: e3911ae0-d242-4da2-a4bc-b2f4877f9dd2
TQID: https://experienceleague.adobe.com/WM6GQ-AhLmtudRWXF6lOez6DaVxMBU3rSaEb2UdsXdc
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2: id: d2311670-43bd-4c2e-bc98-1da2aaba9cefid: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 178
ht-degree: 45%

---

# 운영 체제

운영 체제 [차원](overview.md)은(는) 방문자가 사용한 운영 체제와 버전을 보여 줍니다. 웹 속성에 OS별 기능이 있는 경우 이 차원을 통해 가장 일반적인 운영 체제를 파악할 수 있습니다.

## 이 차원을 데이터로 채우기

이 차원은 Adobe 내부의 조회 테이블을 참조합니다. 조회 값은 이미지 요청에 있는 `User-Agent` HTTP 헤더를 기반으로 합니다. Adobe은 사용자 에이전트와 운영 체제 간 조회를 유지 관리하기 위해 [DeviceAtlas](https://deviceatlas.com/)와(과) 파트너 관계를 맺고 있습니다.

* AppMeasurement 구현의 경우 이 차원은 즉시 작동합니다.
* 웹 SDK 구현의 경우 [데이터 스트림을 구성](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html)할 때 [!UICONTROL 장치 조회]를 사용하도록 설정하십시오.

## 차원 항목

차원 항목에는 방문자가 사용하는 운영 체제가 포함됩니다. 예로는 `"Windows 10"`, `"OS X 10.15.7"` 및 `"Android 9"`가 있습니다.

## 정확한 OS 버전 추적

업계에서 클라이언트 힌트로 전환함에 따라 일부 운영 체제 버전이 잠재적으로 혼동될 수 있습니다. 예를 들어 높은 엔트로피 클라이언트 힌트를 수집하지 않는 경우 &quot;Windows 10&quot; 및 &quot;Windows 11&quot;을 모두 &quot;Windows 10&quot; 아래에 그룹화할 수 있습니다. 자세한 내용은 기술 정보 안내서의 [클라이언트 힌트](/help/technotes/client-hints.md)를 참조하십시오.
