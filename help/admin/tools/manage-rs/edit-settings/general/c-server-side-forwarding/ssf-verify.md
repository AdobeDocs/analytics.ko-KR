---
description: 서버측 전달이 제대로 활성화되었는지 확인하려면 Analytics 추적 요청에서 HTTP 응답을 검사해야 합니다. 이 지침은 서버측 전달이 제대로 활성화되도록 하기 위해 존재해야 하는 지표를 보여 줍니다.
solution: Analytics
title: 서버측 전달 구현 확인 방법
feature: Report Suite Settings
exl-id: 21db4572-da3c-43aa-a774-86a089656695
role: Admin
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 86%

---

# 서버측 전달 구현 확인 방법

서버측 전달이 제대로 활성화되었는지 확인하려면 Analytics 추적 요청에서 HTTP 응답을 검사해야 합니다. 이 작업은 브라우저의 개발자 도구를 사용하거나 Charles Web Debugger와 같은 프록시 도구를 사용하여 수행할 수 있습니다. 다음 지침은 서버측 전달이 제대로 활성화되도록 하기 위해 존재해야 하는 표시기를 보여 줍니다.

서버측 전달의 상태를 확인하려면 다음 작업을 수행하십시오.

1. 업데이트 된 AppMeasurement 코드가 포함된 테스트 페이지를 로드합니다.
1. 브라우저의 디버깅 도구나 프록시 소프트웨어를 사용하여 Analytics 추적 요청의 HTTP 응답을 검사합니다(&#39;b/ss&#39;가 포함된 경로를 선택하여 쉽게 필터링할 수 있습니다.).
1. HTTP 응답을 검사합니다. 응답에 Audience Manager 데이터가 있으면(아래 그림 참조) 서버측 전달이 작동하고 있습니다.

![](/help/admin/tools/manage-rs/edit-settings/general/c-server-side-forwarding/assets/ssf-succeed.png)

>[!CAUTION]
>
>응답에 키 값 쌍 `"status":"SUCCESS"` 또는 2 x 2 이미지가 있는 경우 서버측 전달이 제대로 구성되지 *않은* 것입니다. ID 서비스가 제대로 배포되었는지, App Measurement 모듈을 배포했는지, 해당 보고서 세트가 올바른 조직 ID에 매핑되었는지, Analytics 관리 도구에서 서버측 전달이 활성화되었는지 확인하십시오.

>[!MORELIKETHIS]
>
>* [Charles Web Debugger](https://www.charlesproxy.com/)
