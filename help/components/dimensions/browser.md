---
title: 브라우저
description: 사용된 브라우저의 이름 및 버전입니다.
feature: Dimensions
exl-id: 2bdf2a5a-3482-43fa-b2e1-fbea892918fb
TQID: https://experienceleague.adobe.com/J6rDfVwmRZpRLrultdurQkRih2HcPygjcjwO0bkms5E
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: d2311670-43bd-4c2e-bc98-1da2aaba9cef
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: bdd7a704c94394d6f6cedfbc07988bde69993691
workflow-type: tm+mt
source-wordcount: 280
ht-degree: 43%

---

# 브라우저

&#39;[!UICONTROL 브라우저]&#39; [차원](overview.md)에서 히트를 보내는 브라우저의 이름과 버전을 보고합니다. 이 차원은 방문자가 사용하는 가장 일반적인 브라우저를 측정하려는 경우에 유용합니다. 사이트의 새 버전을 테스트할 때 이 차원의 상위 브라우저에서 이러한 테스트를 실행하여 품질 관리 노력을 극대화할 수 있습니다.

## 이 차원을 데이터로 채우기

이 차원은 Adobe 내부의 조회 테이블을 참조합니다. 조회 값은 이미지 요청에 있는 `User-Agent` HTTP 헤더를 기반으로 합니다. Adobe은 사용자 에이전트와 브라우저 간 조회를 유지 관리하기 위해 [DeviceAtlas](https://deviceatlas.com/)와(과) 파트너 관계를 맺고 있습니다.

* AppMeasurement 구현의 경우 이 차원은 즉시 작동합니다.
* 웹 SDK 구현의 경우 [데이터 스트림을 구성](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html)할 때 [!UICONTROL 장치 조회]를 사용하도록 설정하십시오.

## 차원 항목

차원 항목에는 사용된 브라우저 이름과 버전이 포함됩니다. 동일한 브라우저의 다른 버전은 별도의 차원 항목입니다.

일부 차원 항목은 버전 번호 대신 `"(unknown version)"`을 포함합니다. 이 차원 항목은 Adobe이 조회 테이블에 아직 추가하지 않은 최근 브라우저 릴리스를 참조합니다. 브라우저는 자주 업데이트되므로 주어진 브라우저에 대해 `"(unknown version)"`은 일반적이고 일시적입니다. Adobe는 일반적으로 월별 유지 관리 릴리스 동안 조회 테이블을 업데이트합니다.

일부 차원 항목에는 `"Chrome 148.999"`과(와) 같이 `.999`이(가) 부 버전 번호로 포함되어 있습니다. 이 값은 Adobe이 브라우저의 부 버전을 안정적으로 확인할 수 없음을 나타냅니다. Chrome 또는 Edge 브라우저에서 [클라이언트 힌트](/help/technotes/client-hints.md) 없이 요청을 보낼 때 사용자 에이전트 문자열의 부 버전은 신뢰할 수 없는 것으로 간주됩니다. Adobe은 부정확할 수 있는 부 버전으로 차원 항목을 부풀리는 대신 해당 부 버전을 `.999`(으)로 바꿉니다. 마찬가지로, 브라우저가 비정상적으로 높은 버전 번호(99999 이상)를 보고하는 경우 Adobe은 이를 `999.999`(으)로 표준화합니다.
