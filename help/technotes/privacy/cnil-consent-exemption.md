---
description: 디바이스 또는 브라우저에서 필수적이지 않은 쿠키를 저장하거나 읽기 위한 사용자 동의에 대한 가이드라인 및 권장 사항에 대해 알아보십시오.
title: 사용자 동의 및 쿠키에 대한 CNIL 가이드라인은 무엇입니까
feature: Data Governance
role: Admin
exl-id: 04179e58-dbba-45e2-ba57-7fe5fdedc483
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 100%

---

# CNIL 동의 면제

2020년 10월 1일, 프랑스 데이터 보호 당국(이하 “CNIL”)은 사용자 디바이스 또는 브라우저에서 필수가 아닌 쿠키 및 유사 기술을 저장하거나 읽기 위해 사용자 동의를 구하는 것에 대한 쿠키 가이드라인(“가이드라인”)의 개정된 버전과 최종 권장 사항(“권장 사항”)을 발표했습니다.

가이드라인은 동의 요구 사항에 대한 제한적인 면제를 규정합니다(“동의 면제”). 동의 면제는 웹 게시자를 대신하여 사이트 또는 앱의 대상자만 측정하는 제한적인 용도를 가진 분석 쿠키에 적용됩니다. 가이드라인은 동의 면제를 적용하려면 다음 조건을 구현해야 한다고 규정합니다.

* 최대 25개월 데이터 보존.  현재 데이터 보존 설정은 [!UICONTROL 분석] > [!UICONTROL 관리] > [!UICONTROL 데이터 거버넌스]에서 검토할 수 있습니다.  [데이터 보존](/help/technotes/data-retention.md)
* ECID에서 서드파티 쿠키를 비활성화합니다. [disableThirdPartyCalls](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/configurations/disablethirdpartycalls.html?lang=ko-KR#id-service-api), [disableThirdPartyCookies](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/configurations/disable-cookies.html?lang=ko-KR#id-service-api), [disableIdSyncs](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/configurations/disableidsync.html?lang=ko-KR#id-service-api)
* 13개월 쿠키 제한.  `cookieLifetime` 변수를 사용하여 분석 쿠키 만료를 재정의할 수 있습니다. Analytics, ECID가 포함된 Experience Cloud 쿠키로 인해 방문할 때마다 쿠키 만료일이 연장됩니다.  고정적이고 비순환하는 쿠키 만료일을 설정하려면 (1) 사용자 정의 코드를 작성하여 쿠키를 삭제할 날짜를 설정하거나 (2) CMP를 시용하여 쿠키 재설정 날짜를 제어합니다.   [cookieLifetime](/help/implement/vars/config-vars/cookielifetime.md) 및 [Experience Cloud 쿠키](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-privacy.html?lang=ko-KR#ec-cookies)
* 제한적 범위. 쿠키의 범위는 단일 사이트 또는 애플리케이션으로 제한되어야 합니다. [브라우저 쿠키](/help/technotes/cookies/cookies.md#third-party-cookie-limitations)
* 익명화. IP 주소의 마지막 옥텟을 익명화합니다. [일반 계정 설정](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md)
* 보고에서 방문자 ID를 숨깁니다.  방문자 ID는 기본적으로 Adobe Workspace 및 Adobe Reports &amp; Analytics에 표시되지 않습니다.  방문자 ID는 데이터 피드 및 Data Warehouse에서 제공됩니다.  데이터 피드 및 Data Warehouse에 대한 액세스는 [Admin Console의 액세스 권한](https://experienceleague.adobe.com/docs/core-services/interface/administration/admin-getting-started.html) 및 [데이터 피드 열 참조](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md)에 의해 제한될 수 있습니다.
* 지리적 위치 매개변수. 지리적 위치는 우편번호 수준보다 정확할 수 없습니다. [우편번호 옵션](/help/implement/vars/page-vars/zip.md) 및 [일반 계정 설정](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md)
* 옵트인 옵션 설정.  옵트인 서비스를 사용하면 방문자가 사용자의 사이트를 방문할 때 사용자의 디바이스 또는 브라우저에 쿠키를 설정할 수 있는지 확인할 수 있도록 프로토콜을 설정할 수 있습니다. [옵트인 서비스](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/optin-overview.html?lang=ko-KR)
* 데이터 공유 방지.  Adobe Audience Manager에 대한 데이터 공유를 금지하려면 `opt.dmp` [개인정보 보고 변수](/help/admin/tools/manage-rs/edit-settings/privacy-reporting.md)에 대해 컨텍스트 변수를 사용하여 히트가 공유되지 않도록 차단합니다.
* 액세스 및 삭제 기능. 액세스 및 삭제 요청을 위해 Privacy Service를 활용하십시오. [Analytics &amp; Privacy Service](gdpr.md)

## 데이터 수집에 대한 추가 고려 사항

다음과 같은 추가 고려 사항이 적용됩니다.

* Adobe Analytics는 미국, 영국 및 싱가포르에서 데이터 처리 센터를 운영하여 모든 고객에게 데이터를 지역적으로 수집하고, 처리하고, 저장할 수 있는 유연성을 제공합니다. 고객은 Adobe Analytics의 초기 설정 구성 시 원하는 데이터 처리 센터 위치를 선택할 수 있습니다. 고객 데이터는 최종적으로 핵심 Analytics 제품에 대해 고객이 선택한 지역 내에 저장됩니다.
* 세분화를 위해, 가상 보고서 세트를 위해 또는 별도의 엔드포인트로 라우팅하기 위해 옵트인 데이터를 옵트아웃 데이터와 분리하려면 Analytics 변수에서 옵트인 상태를 수집하는 것이 좋습니다.
* 사전 동의 없이 사이트 또는 앱 외부에서 측정하지 않습니다. 예를 들어 오프사이트 캠페인, 이메일 캠페인 또는 iFrame이 금지됩니다.
* 사용자 동의 없이는 개인정보 변수의 수집이 허용되지 않습니다. [사용자 동의에 따라 Experience Cloud 활동 제어](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/use-opt-in-to-control-experience-cloud-activities-based-on-user-consent.html?lang=ko-KR#implementing-opt-in-on-the-page)
* 데이터는 다른 데이터와 결합하지 않고 익명 통계를 생성하는 데만 사용됩니다.
* 데이터는 상호 참조 작업에 사용되지 않습니다.
* GPS 지리적 위치 데이터는 수집되지 않습니다.
* 최종 사용자 동의가 주어지면 위의 설정을 수정하고 제한을 완화할 수 있습니다.

>[!IMPORTANT]
>
>이 문서는 법률 또는 규정에 대한 조언을 제공하기 위한 것이 아니며, Adobe의 보증 또는 계약상 약속이 아닙니다. 고객이 이 주제와 관련된 문제에 대한 고객의 법적 및 규제 의무에 대해 독립적인 법률 자문을 구할 것을 권장합니다.

자세한 내용은 [CNIL 쿠키 면제](https://www.cnil.fr/en/sheet-ndeg16-use-analytics-your-websites-and-applications) 웹 사이트를 참조하십시오.
