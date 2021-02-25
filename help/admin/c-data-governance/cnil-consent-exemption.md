---
description: 장치 또는 브라우저에서 중요하지 않은 쿠키를 저장하거나 읽는데 대한 사용자의 동의에 대한 지침 및 권장 사항에 대해 알아보십시오.
title: 사용자의 동의 및 쿠키에 대한 CNIL 가이드라인은 무엇입니까?
translation-type: tm+mt
source-git-commit: c5ebc92622e012699d64c27701b24a88429e9f4f
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 1%

---


# CNIL 동의 면제

2020년 10월 1일, 프랑스 데이터 보호 기관(이하 &quot;CNIL&quot;이라 함)은 쿠키 지침의 개정판(&quot;지침&quot;)과 사용자의 장치 또는 브라우저에 중요하지 않은 쿠키 및 유사한 기술을 저장하거나 읽는데 대한 사용자의 동의를 받는 것에 대한 최종 권장 사항(&quot;Recommendations&quot;)을 게시했습니다.

가이드라인은 동의 요건(&quot;동의 면제&quot;)에 대해 제한된 면제를 제공합니다. 동의 면제는 Web Publisher를 대신하여 사이트 또는 앱의 고객을 측정하는 용도로만 사용되는 분석 쿠키에 적용됩니다. 가이드라인에서는 동의 면제가 적용되려면 다음 조건을 이행해야 합니다.

* 최대 25개월 데이터 유지  Analytics > 관리 > 데이터 거버넌스에서 현재 데이터 유지 설정을 검토할 수 있습니다.  [데이터 유지](https://experienceleague.adobe.com/docs/analytics/technotes/data-retention.html)
* 13개월 쿠키 제한.  `cookieLifetime` 변수를 사용하여 분석 쿠키 만료를 재정의할 수 있습니다.  [cookieLifetime](https://experienceleague.adobe.com/docs/analytics/implementation/vars/config-vars/cookielifetime.html)
* 제한된 범위. 쿠키의 범위는 단일 사이트 또는 애플리케이션으로 제한되어야 합니다. [브라우저 쿠키](https://experienceleague.adobe.com/docs/analytics/technotes/cookies.html?lang=en&quot;\l&quot;타사 쿠키 구현)
* 익명화. IP 주소의 마지막 8진수 이름을 익명화합니다. [일반 계정 설정](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/general-acct-settings-admin.html)
* 방문자 ID를 보고에서 숨깁니다.  방문자 ID는 기본적으로 Adobe 작업 공간 및 Adobe Reports and Analytics에 표시되지 않습니다.  방문자 ID는 데이터 피드 및 Data Warehouse에서 사용할 수 있습니다.  데이터 피드 및 Data Warehouse에 대한 액세스는 [Admin Console의 액세스 권한](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=en&quot;\l&quot;task_040673FE3E3E429B9531FBCB8B6A4391)으로 제한될 수 있습니다.
* 지리적 위치 매개 변수. 지리적 위치는 우편 번호 수준보다 더 정확할 수 없습니다. [우편 ](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/zip.html?lang=en&quot;\l&quot;zip-in-adobe-experience-platform-launch) 옵션 및  [일반 계정 설정](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/general-acct-settings-admin.html?lang=en&quot;\l&quot;admin-tools)
* 옵트인 옵션을 설정합니다.  옵트인 서비스를 사용하면 사이트를 방문할 때 사용자의 장치 또는 브라우저에서 쿠키를 설정할 수 있는지 여부를 확인하기 위해 방문자 프로토콜을 설정할 수 있습니다. [옵트인 서비스](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/optin-overview.html)
* 데이터 공유 방지  Adobe Audience Manager에 대한 데이터 공유를 차단하려면 [개인 정보 보고](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/consent-variables.html?lang=en&quot;\l&quot;변수)에 대해 `opt.dmp` 컨텍스트 변수를 사용하여 히트가 공유되지 않도록 차단하십시오.
* 액세스 및 삭제 기능 Privacy Service을 사용하여 액세스 및 삭제 요청을 수행합니다. [분석 및 Privacy Service](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/an-gdpr-overview.html)

## 데이터 수집을 위한 추가 고려 사항

다음과 같은 추가 고려 사항이 적용됩니다.

* 사전 동의 없이 사이트 또는 앱 외부에서 측정 금지(예: 오프사이트 캠페인, 이메일 캠페인 또는 iFrame 없음).
* 변수의 개인 정보 수집은 동의 없이 허용되지 않습니다.
* 데이터는 다른 데이터와 조합하지 않고 익명의 통계를 작성하는 데만 사용됩니다.
* 데이터는 상호 참조 작업에 사용되지 않습니다.
* GPS 위치 정보 데이터는 수집되지 않습니다.

자세한 내용은 [CNIL 쿠키 면제](https://www.cnil.fr/en/sheet-ndeg16-use-analytics-your-websites-and-applications) 웹 사이트를 참조하십시오.
