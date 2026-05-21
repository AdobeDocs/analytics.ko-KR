---
description: 서버측 전달이 제대로 활성화되었는지 확인하려면 Analytics 추적 요청에서 HTTP 응답을 검사해야 합니다. 이 지침은 서버측 전달이 제대로 활성화되도록 하기 위해 존재해야 하는 지표를 보여 줍니다.
solution: Analytics
title: 서버측 전달 구현 확인 방법
feature: Report Suite Settings
exl-id: 21db4572-da3c-43aa-a774-86a089656695
role: Admin
TQID: https://experienceleague.adobe.com/FpB4dk9D87gc24t5KG6WRJ-r8GFOvOEUlRTTjc6XFYI
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 246
ht-degree: 60%

---

# 서버측 전달 구현 확인 방법

서버측 전달이 제대로 활성화되었는지 확인하려면 Analytics 추적 요청에서 HTTP 응답을 검사해야 합니다. 이 작업은 브라우저의 개발자 도구를 사용하거나 Charles Web Debugger와 같은 프록시 도구를 사용하여 수행할 수 있습니다. 다음 지침은 서버측 전달이 제대로 활성화되도록 하기 위해 존재해야 하는 표시기를 보여 줍니다.

서버측 전달의 상태를 확인하려면 다음 작업을 수행하십시오.

1. 업데이트된 AppMeasurement 코드가 포함된 테스트 페이지를 로드합니다.
1. 브라우저의 디버깅 도구에서 또는 프록시 소프트웨어를 사용하여 Analytics의 추적 요청에서 HTTP 응답을 검사합니다(&quot;b/ss&quot;가 포함된 경로를 선택하여 쉽게 필터링할 수 있음).
1. HTTP 응답을 검사합니다. 응답에 Audience Manager 데이터가 있으면(아래 그림 참조) 서버측 전달이 작동하고 있습니다.

![](/help/admin/tools/manage-rs/edit-settings/general/c-server-side-forwarding/assets/ssf-succeed.png)

>[!CAUTION]
>
>응답에 키 값 쌍 `"status":"SUCCESS"` 또는 2 x 2 이미지가 있는 경우 서버측 전달이 제대로 구성되지 *않은* 것입니다. ID 서비스가 제대로 배포되었는지, App Measurement 모듈을 배포했는지, 해당 보고서 세트가 올바른 조직 ID에 매핑되었는지, Analytics 관리 도구에서 서버측 전달이 활성화되었는지 확인하십시오.

>[!MORELIKETHIS]
>
>* [Charles Web Debugger](https://www.charlesproxy.com/)
