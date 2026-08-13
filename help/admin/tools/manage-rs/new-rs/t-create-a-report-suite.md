---
description: Adobe Analytics에서 데이터 수집을 위한 기본 컨테이너를 만듭니다
title: 보고서 세트 만들기
feature: Report Suite Settings
exl-id: 255ae051-d993-41a5-8cf3-819a54c17e34
TQID: https://experienceleague.adobe.com/ZmPcYHvXOhaXXnqsSVUh1bpvignxomS3d4S76iMCAa4
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
subfeature_v2:
  - id: c4cb071e-4667-4fb1-b1f1-d8994549cfb2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: c2ae876122715b4fa6367326dc23479dd9648021
workflow-type: tm+mt
source-wordcount: 312
ht-degree: 87%

---

# 보고서 세트 만들기

보고서 세트는 Adobe Analytics가 보고서를 가져오는 데 사용하는 데이터의 사일로입니다. 조직에는 여러 개의 보고서 세트가 있을 수 있으며, 각 보고서 세트에는 서로 다른 데이터 세트가 포함되어 있습니다. 이전에는 개별 보고서 세트가 중요했지만 단일 보고서 세트가 더 유용해졌습니다. [가상 보고서 세트](/help/components/vrs/vrs-about.md#virtual-report-suites)및 보고서 처리 시간을 도입하면 관리자가 고유한 데이터 하위 집합을 만들 수 있으므로 전역 데이터와 사이트별 데이터를 모두 유연하게 얻을 수 있습니다.

이 문서는 시스템 수준 관리자 또는 Adobe Analytics 관리자가 데이터 수집을 준비할 수 있도록 설계되었습니다.

## 사전 요구 사항

[Adobe Analytics 첫 번째 관리 안내서](/help/admin/admin-console/first-admin-guide.md): 시스템 수준 관리자가 CX 엔터프라이즈 Admin Console을 통해 Adobe Analytics에 대한 액세스 권한을 부여했는지 확인하십시오.

## 보고서 세트 만들기 {#create-report-suite}

1. **[!UICONTROL Analytics]** > **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]**&#x200B;를 클릭합니다.
1. **[!UICONTROL 보고서 세트 추가]**&#x200B;를 클릭합니다.
1. 미리 정의된 템플릿이나 [템플릿](/help/admin/tools/manage-rs/rs-templates/report-suite-templates.md)으로 사용할 기존 보고서 세트를 선택합니다.

   >[!NOTE]
   >
   >설정만 복사할 수 있고 데이터는 복사할 수 없습니다. 고객 지원 센터에서 설정을 복사하는 경우 관련된 위험에 대해 고객 지원 센터에서 제공하는 면책조항에 대한 서면 확인서를 제공해야 합니다. 자세한 내용은 [소스 보고서 세트에서 복사되지 않은 설정](/help/admin/tools/manage-rs/new-rs/settings-not-copied-from-rs.md)을 참조하십시오.

1. [새 보고서 세트](/help/admin/tools/manage-rs/new-rs/new-report-suite.md)에 설명된 필드를 채웁니다.
1. **[!UICONTROL 보고서 세트 만들기]**&#x200B;를 클릭합니다.

보고서 세트 ID의 최대 길이는 40바이트입니다. 보고서 세트 이름의 최대 길이는 255바이트입니다.

## 문제 해결

**CX Enterprise에 로그인하면 Analytics 아이콘이 회색으로 표시됩니다.**

이는 계정에 Analytics에 대한 올바른 권한이 부여되지 않았음을 의미합니다. 조직의 시스템 수준 관리자와 함께 Adobe Analytics에 액세스할 수 있는 충분한 권한이 있는 프로필에 속해 있는지 확인합니다.

## 다음 단계

[Adobe Analytics 태그 속성 만들기](/help/implement/launch/create-analytics-property.md): Analytics 구현을 관리할 영역을 만듭니다.
