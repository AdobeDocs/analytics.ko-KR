---
title: IP 주소로 제외
description: 특정 IP 주소에서 생성된 데이터가 보고서에 표시되지 않도록 합니다.
exl-id: 315a3000-f043-434b-a677-d111aeed7971
feature: Admin Tools
role: Admin
source-git-commit: d642bf8703d7c4c1545bfd9763c70ed8b1237eac
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 62%

---

# IP 주소로 제외

보고서에서 내부 웹 사이트 활동, 사이트 테스트 및 직원 사용과 같은 특정 IP 주소의 데이터를 제거할 수 있습니다. IP 주소 데이터를 제외하여 데이터를 제외하면 보고서 정확도가 향상됩니다. 또한 보고서 데이터를 왜곡할 수 있는 서비스 거부나 기타 악의적인 이벤트의 데이터를 제거할 수 있습니다.

IP 주소별로 데이터를 제외하려면 아래 설명에 따라 제외를 구성하거나 [방화벽을 구성](/help/technotes/ip-addresses.md)할 수 있습니다.

## IP 주소별 제외 구성

>[!NOTE]
>
>IP 주소별로 제외를 구성할 때는 다음 사항을 고려하십시오.
>
>* IP별로 제외된 히트는 [서버 호출](https://experienceleague.adobe.com/docs/analytics/technotes/terms.html?lang=ko)로 청구됩니다.
>* 비공개 IP 주소는 제외할 필요가 없습니다. 외부 IP 주소만 Adobe 데이터 수집 서버에 연결됩니다. 비공개 주소에는 `10.*.*.*`, `192.168.*.*`, `172.[16-31].*.*`, `169.254.*.*`가 포함됩니다.
>* 와일드카드 표시기(&#42;)를 사용하여 주소 범위를 제외할 수 있습니다. 예를 들어 `[!DNL 0.0.*.0]`은 `[!DNL 0.0.0.0]`과 `[!DNL 0.0.255.0]` 사이의 모든 IP 주소를 제외합니다. 최대 50개의 다른 IP 주소를 제외할 수 있습니다.
>* 제외가 설정된 후 5분 내에 시스템으로 들어오는 모든 새 히트에 대해 제외된 IP 주소의 데이터는 제외됩니다.
>* IP 주소가 변경되기 전에 캡처된 히트의 데이터는 영향을 받지 않습니다.
>

IP 주소별 제외를 구성하려면 다음 작업을 수행하십시오.

1. Adobe Analytics에서 **[!UICONTROL 관리자]** > **[!UICONTROL 모든 관리자]**&#x200B;를 선택합니다.

1. 관리 페이지에서 **[!UICONTROL IP별로 제외]**&#x200B;를 선택합니다.




## IP 난독화의 영향 {#section_51B7529FFF16449CA016FDC51D87E2CA}

IP 난독화가 활성화되어 있으면 IP 주소가 난독화되기 전에 IP 제외가 발생하므로 고객은 IP 난독화를 활성화할 때 아무것도 변경할 필요가 없습니다.

마지막 옥텟이 제거되면 IP 필터링 전에 변경이 수행됩니다. 따라서 마지막 옥텟은 0으로 대체되고, IP 제외 규칙은 끝에 0이 있는 IP 주소와 일치하도록 업데이트해야 합니다. 일치 &#42;는 0과 일치해야 합니다.
