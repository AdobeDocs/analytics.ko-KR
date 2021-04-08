---
description: 디바이스 또는 브라우저에서 필수적이지 않은 쿠키를 저장하거나 읽기 위한 사용자 동의에 대한 가이드라인 및 권장 사항에 대해 살펴보십시오.
title: 사용자 동의 및 쿠키에 대한 CNIL 가이드라인은 무엇입니까
exl-id: 04179e58-dbba-45e2-ba57-7fe5fdedc483
translation-type: tm+mt
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 100%

---

# CNIL 동의 면제

2020년 10월 1일, 프랑스 데이터 보호 당국(이하 “CNIL”)은 사용자 디바이스 또는 브라우저에서 필수적이지 않은 쿠키 및 유사 기술을 저장하거나 읽기 위하여 사용자 동의를 구하는 것에 대한 쿠키 가이드라인(“가이드라인”)의 개정된 버전과 최종 권장 사항(“권장 사항”)을 발표했습니다.

가이드라인은 동의 요구 사항에 대한 제한적인 면제를 규정합니다(“동의 면제”). 동의 면제는 웹 게시자를 대신하여 사이트 또는 앱의 잠재고객만 측정하는 제한적인 용도를 가진 분석 쿠키에 적용됩니다. 가이드라인은 동의 면제를 적용하려면 다음 조건을 구현해야 한다고 규정합니다.

* 최대 25개월 데이터 보존.  분석 > 관리 > 데이터 거버넌스에서 현재 데이터 보존 설정을 검토할 수 있습니다.  [데이터 유지](https://experienceleague.adobe.com/docs/analytics/technotes/data-retention.html?lang=ko-KR)
* ECID에서 서드 파티 쿠키를 비활성화합니다. [disableThirdPartyCalls](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/configurations/disablethirdpartycalls.html?lang=ko-KR#id-service-api), [disableThirdPartyCookies](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/configurations/disable-cookies.html?lang=ko-KR#id-service-api), [disableIdSyncs](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/configurations/disableidsync.html?lang=ko-KR#id-service-api)
* 13개월 쿠키 제한이 고정 날짜로 설정되었으며, 유동적이지 않습니다.  `cookieLifetime` 변수를 사용하여 분석 쿠키 만료를 재정의할 수 있습니다.  [cookieLifetime](https://experienceleague.adobe.com/docs/analytics/implementation/vars/config-vars/cookielifetime.html?lang=ko-KR)
* 제한적 범위. 쿠키의 범위는 단일 사이트 또는 애플리케이션으로 제한되어야 합니다. [브라우저 쿠키](https://experienceleague.adobe.com/docs/analytics/technotes/cookies.html?lang=ko-KR&quot;\l&quot;third-party-cookie-implementations)
* 익명화. IP 주소의 마지막 옥텟을 익명화합니다. [일반 계정 설정](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/general-acct-settings-admin.html?lang=ko-KR)
* 보고에서 방문자 ID를 숨깁니다.  방문자 ID는 기본적으로 Adobe Workspace 및 Adobe Reports &amp; Analytics에 표시되지 않습니다.  방문자 ID는 데이터 피드 및 Data Warehouse에서 제공됩니다.  데이터 피드 및 Data Warehouse에 대한 액세스는 [Admin Console의 액세스 권한](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=ko-KR&quot;\l&quot;task_040673FE3E3E429B9531FBCB8B6A4391)에 의해 제한될 수 있습니다. 및 [데이터 피드 열 참조](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html?lang=en#columns%2C-descriptions%2C-and-data-types)
* 지리적 위치 매개 변수. 지리적 위치는 우편 번호 수준보다 정확할 수 없습니다. [우편 번호 옵션](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/zip.html?lang=ko-KR&quot;\l&quot;zip-in-adobe-experience-platform-launch) 및 [일반 계정 설정](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/general-acct-settings-admin.html?lang=ko-KR&quot;\l&quot;admin-tools)
* 옵트인 옵션 설정.  옵트인 서비스를 사용하면 방문자가 사용자의 사이트를 방문할 때 사용자의 디바이스 또는 브라우저에 쿠키를 설정할 수 있는지 확인할 수 있도록 프로토콜을 설정할 수 있습니다. [옵트인 서비스](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/optin-overview.html?lang=ko-KR)
* 데이터 공유 방지.  Adobe Audience Manager에 대한 데이터 공유를 금지하려면 `opt.dmp` [개인 정보 보고 변수](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/consent-variables.html?lang=ko-KR&quot;\l&quot;variables)에 대해 컨텍스트 변수를 사용하여 히트가 공유되지 않도록 차단합니다.
* 액세스 및 삭제 기능. 액세스 및 삭제 요청을 위해 Privacy Service를 활용하십시오. [Analytics &amp; Privacy Service](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/an-gdpr-overview.html?lang=ko-KR)

## 데이터 수집에 대한 추가 고려 사항

다음과 같은 추가 고려 사항이 적용됩니다.

* 세분화를 위해, 가상 보고서 세트를 위해 또는 별도의 끝점으로 라우팅하기 위해 옵트인 데이터를 옵트아웃 데이터와 분리하려면 Analytics 변수에서 옵트인 상태를 수집하는 것이 좋습니다.
* 사전 동의 없이 사이트 또는 앱 외부에서 측정하지 않습니다. 예를 들어 오프사이트 캠페인, 이메일 캠페인 또는 iFrame이 금지됩니다.
* 사용자 동의 없이는 개인 정보 변수의 수집이 허용되지 않습니다. [사용자 동의에 따라 Experience Cloud 활동 제어](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/use-opt-in-to-control-experience-cloud-activities-based-on-user-consent.html?lang=en%22%20\l%20%22implementation#implementation)
* 데이터는 다른 데이터와 결합하지 않고 익명 통계를 생성하는 데만 사용됩니다.
* 데이터는 상호 참조 작업에 사용되지 않습니다.
* GPS 지리적 위치 데이터는 수집되지 않습니다.
* 최종 사용자 동의가 주어지면 위의 설정을 수정하고 제한을 완화할 수 있습니다.

자세한 내용은 [CNIL 쿠키 면제](https://www.cnil.fr/en/sheet-ndeg16-use-analytics-your-websites-and-applications) 웹 사이트를 참조하십시오.
