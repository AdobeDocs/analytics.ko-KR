---
description: 중단 없는 일련의 페이지 보기입니다. 방문 지표는 일반적으로 선택된 기간 내의 사용자 세션 수를 표시하는 보고서에 사용됩니다.
keywords: 방문
seo-description: 중단 없는 일련의 페이지 보기입니다. 방문 지표는 일반적으로 선택된 기간 내의 사용자 세션 수를 표시하는 보고서에 사용됩니다.
seo-title: 방문
solution: Analytics
title: 방문
topic: 지표
uuid: 91317487-F 116-4546-8 CD 2-421418 C 49 A 7 A
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 방문

중단 없는 일련의 페이지 보기입니다. 방문 지표는 일반적으로 선택된 기간 내의 사용자 세션 수를 표시하는 보고서에 사용됩니다.

>[!NOTE]
>
>For information about how visits and mobile app launches are calculated, see [Compare Visits and Mobile App Launches](https://helpx.adobe.com/analytics/kb/compare-visits-and-mobile-app-launches.html) in the Knowledge Base.

방문 지표는 항상 기간과 연관되어 있으므로 동일한 방문자가 사이트에 돌아오는 경우 새 방문을 계산할지 여부를 알 수 있습니다. 세션은 사용자가 사이트에 처음 도착하면 시작되고 다음 중 한 가지 시나리오에서 종료됩니다.

* **활동이 없는 상태로 30분:** 거의 모든 세션이 이 방식으로 종료됩니다. 이미지 요청 사이에 30분 이상이 경과하면 새 방문이 시작됩니다.
* **계속 활동하는 상태로 12시간:** 사용자가 30분 이상의 간격 없이 12시간 동안 이미지 요청을 보내면 자동으로 새 방문이 시작됩니다.
* **2500히트:** 사용자가 새 세션을 시작하지 않고 히트를 대량으로 발생시키면 2500개의 이미지 요청 후에 새 방문이 계산됩니다.
* **100초에 100히트**: 방문이 100초 이내에 발생한 100개가 넘는 히트로 구성되는 경우, 방문이 자동으로 끝납니다. 이 동작은 일반적으로 보트 활동을 가리키는데, 이러한 처리 중심 방문이 지연을 증가시키고 보고서를 생성하는 데 드는 시간을 증가시키지 않도록 하기 위해 이러한 제한이 적용됩니다.

>[!NOTE]
>
>보고서 세트에 대한 방문의 정의는 구체적으로 요청할 경우 줄일 수 있지만 연장할 수는 없습니다. 조직에서 지원되는 사용자 중 한 명이 고객 지원 센터에 연락하여 이 변경 사항을 요청하도록 하십시오.

다음 시나리오에서는 새 방문이 시작되지 않습니다.

* 사용자가 탭을 닫았다가 다시 열고 30분 이내에 사이트로 돌아오는 경우. 또한 사용자는 브라우저를 닫거나 컴퓨터를 다시 부팅할 수 있지만, 이 역시 단일 방문으로 계산됩니다(30분 기간 내 해당 사이트로 다시 이동할 경우).
* 여러 탭에서 사이트를 탐색하는 사용자 탐색에서 여러 개의 탭을 사용해도 방문 또는 방문자가 증가하지 않지만 별도의 브라우저를 사용하면 증가합니다. 다른 탭은 같은 쿠키를 참조하지만 다른 브라우저는 그렇지 않기 때문입니다.

방문이 꼭 브라우저 세션과 일치할 필요는 없습니다. 예를 들어 방문자가 브라우저를 닫은 경우 브라우저를 다시 열고 분 후 다시 사이트를 방문하면 동일한 방문의 연속으로 인식됩니다. 또한 방문자가 35분 동안 하나의 페이지에 머무는 경우에는 방문이 종료되고 처리되며 다른 페이지로 클릭하여 이동하면 새로운 방문이 시작됩니다.

방문이 끝나면, 방문 만료가 있는 모든 변수는 만료되고 더 이상 지속되지 않습니다. 방문 번호 지표는 이 방문자에 대해 다음 방문 시 증가합니다.

>[!NOTE]
>
>If you are using Analytics as the reporting source for Adobe Target, refer to [Minimizing Inflated Visit and Visitor Counts in A4T](https://marketing.adobe.com/resources/help/en_US/target/a4t/minimizing-inflated-visit-and-visitor-counts-a4t.html) in the [!DNL Target] documentation.

자세한 내용은 Adobe Analytics 구현 안내서의 [고유 방문자 식별](https://marketing.adobe.com/resources/help/en_US/sc/implement/visid_overview.html)을 참조하십시오.

**기간**

방문은 활동이 발생한 각 기간에서 보고됩니다. 예를 들어 방문이 12월 1일 오후 11시 45분에 시작해서 12월 2일 오전 12시 30분까지 계속된다고 가정합시다. 이 방문은 12월 1일과 12월 2일에 카운트됩니다. 이러한 보고 기능은 주별, 월별, 분기별, 연도별을 포함한 다른 기간에도 적용됩니다.
