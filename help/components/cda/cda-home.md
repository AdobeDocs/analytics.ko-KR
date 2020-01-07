---
title: Cross-Device Analytics
description: Cross-Device Analytics는 장치 데이터를 함께 결합함으로써 데이터를 장치 중심에서 사람 중심으로 변경합니다.
translation-type: ht
source-git-commit: c358df811f23a57441e6f9410c957e34954de712

---


# Cross-Device Analytics

> [!NOTE] Cross-Device Analytics 설명서는 기능이 추가로 개발되면 변경될 수 있습니다. 정기적으로 업데이트를 확인하십시오.

Cross-Device Analytics는 Analytics를 장치 중심 보기에서 사람 중심 보기로 변환하는 기능입니다. 이 기능은 Adobe Experience Platform ID 서비스 Co-op 그래프 또는 Private 그래프를 사용하여 개인에게 속한 장치를 식별하고 함께 결합합니다. 그 결과 분석가는 브라우저, 장치 또는 앱을 넘나드는 사용자 행동을 이해할 수 있습니다. CDA를 사용하여 다음과 같은 질문에 답변할 수 있습니다.

* 얼마나 많은 사람들이 내 브랜드와 상호 작용하고 있습니까? 얼마나 많은 장치와 어떤 유형의 장치를 사용하고 있습니까? 어떻게 중첩됩니까?
* 사람들이 모바일 장치에서 작업을 시작한 다음 나중에 데스크탑 PC로 이동하여 작업을 완료하는 빈도는 얼마나 됩니까? 하나의 장치에 랜딩되는 캠페인 클릭스루가 다른 곳에서 전환을 가져옵니까?
* 장치 간 여정을 고려하면 캠페인 효과에 대한 이해가 어떻게 달라집니까? 단계 분석은 어떻게 변경됩니까?
* 사용자가 하나의 장치에서 다른 장치로 이동하는 가장 일반적인 경로는 무엇입니까? 어디에서 중단됩니까? 어디에서 성공합니까?
* 여러 장치가 있는 사용자의 행동은 단일 장치가 있는 사용자와 어떻게 다릅니까?

장치가 결합되면 변수 지속성이 장치 간에 전달됩니다. 예를 들어 사용자가 먼저 데스크탑 컴퓨터의 광고를 통해 사이트를 방문합니다. 해당 사용자는 모바일 앱을 찾아 설치한 다음 결국 모바일 장치에서 구매합니다. Cross-Device Analytics를 사용하면 수입은 데스크탑 컴퓨터에서 클릭한 광고로 인한 것일 수 있습니다.

Cross-Device Analytics의 기능에 대해 자세히 알려면 [움직임 IQ: Cross-Device Analytics 스파크 페이지](http://adobe.ly/aacda)를 참조하십시오.

## 전제 조건

2019년 9월부로 Cross-Device Analytics를 사용하려면 다음 조건을 충족해야 합니다. 조직 내 팀 및 Adobe 계정 관리자와 함께 다음 사항을 모두 충족하도록 하십시오.

> [!IMPORTANT] 모든 전제 조건을 충족하지 못하면 Cross-Device Analytics를 사용할 수 없거나 데이터 결합이 제대로 되지 않을 수 있습니다.

* 조직의 데이터는 Adobe의 태평양 연안 북서부 데이터 센터 내에 있어야 합니다. 세계의 다른 지역 데이터 센터에 대한 지원이 계획되어 있습니다.
* 조직의 계정 관리자에게 문의하여 다음 주요 사항을 충족하십시오.
   * Adobe Analytics Ultimate가 포함된 계약은 Adobe와 체결해야 합니다.
   * 조직이 Adobe Experience Platform ID 서비스 Co-op 그래프 또는 Private 그래프를 사용해야 합니다. Device Co-op 사용 안내서의 [홈 페이지](https://docs.adobe.com/content/help/ko-KR/device-co-op/using/home.html)를 참조하십시오.
   * 조직은 Adobe가 Microsoft Azure 서버에서 Analytics 데이터를 처리하고 저장하도록 허용하는 데 동의해야 합니다. Adobe는 Azure를 사용하여 장치 그래프 데이터를 저장하고 장치 결합을 수행합니다. 이와 같이 Adobe Analytics 데이터는 Adobe의 데이터 처리 센터와 Microsoft Azure에 있는 Adobe 간에 서로에게 전달됩니다.
* Cross-Device Analytics는 보고서 세트별로 활성화됩니다. CDA에 대해 사용 가능한 보고서 세트는 다음 조건을 충족해야 합니다.
   * 보고서 세트는 하루에 1억 건을 초과할 수 없습니다. 이 임계 값은 앞으로 몇 달 동안 증가할 것입니다.
   * 보고서 세트에는 여러 장치 유형(웹, 앱 등)의 데이터를 의미하는 장치 간 데이터를 포함하는 것이 좋습니다. CDA는 지리적 관점에서 엄격히 말해 전역적일 필요는 없지만, 일부 조직에서는 "전역" 보고서 세트로서 이 개념을 언급하고 있습니다. Cross-Device Analytics는 보고서 세트 간에 작동하지 않으며 여러 보고서 세트의 데이터를 결합하지도 않습니다.
* 구현은 다음 요구 사항을 충족해야 합니다.
   * 최신 버전의 Experience Cloud ID 서비스를 배포해야 합니다. Experience Cloud ID 서비스 사용 안내서의 [홈 페이지](https://docs.adobe.com/content/help/ko-KR/id-service/using/home.html)를 참조하십시오. Adobe Experience Platform Launch를 사용하는 대부분의 구현에 이미 ECID가 배포되어 있을 수 있습니다.
   * 사용자가 로그인하거나 이메일을 여는 경우와 같이 개인을 식별할 수 있을 때마다 이 `setCustomerIDs` 함수를 호출합니다. 이 요구 사항은 모바일 앱(사용하는 경우)을 비롯한 모든 플랫폼에 적용됩니다. Experience Cloud ID 서비스 사용 안내서의 [setCustomerIDs](https://docs.adobe.com/content/help/ko-KR/id-service/using/id-service-api/methods/setcustomerids.html)를 참조하십시오.

## 제한

Cross-Device Analytics는 획기적이고 강력한 기능이지만 사용 방법에 대한 제한이 있습니다.

* CDA는 Analysis Workspace를 통해서만 사용할 수 있습니다.
* 위의 전제 조건에서 설명한 대로 보고서 세트 간에 결합을 수행할 수 없습니다.
* Adobe Analytics 보고서 세트는 둘 이상의 IMS 조직에 매핑할 수 없습니다. CDA는 주어진 보고서 세트 내에서 장치를 결합하기 때문에 여러 IMS 조직 간에 데이터를 결합하는 데에는 CDA를 사용할 수 없습니다.
* CDA는 현재 사용자 특성과 호환되지 않습니다. 장치 간 세그먼트 내에서 또는 CDA 가상 보고서 세트를 기반으로 하는 Analysis Workspace 프로젝트 내에서 보고를 위해 사용자 특성을 사용하여 CDA 가상 보고서 세트를 작성할 수 없습니다.
   > [!TIP] CDA에서 사용자 특성을 사용할 수는 없지만 두 기능은 모두 `setCustomerIDs` 함수에 의존합니다. 이 두 기능은 별도의 (가상) 보고서 세트에서 동시에 실행될 수 있습니다.
* CDA는 Co-op 그래프 또는 Private 그래프를 필요로 합니다. 타사 장치 그래프는 지원되지 않습니다.
* 기존 Analytics ID는 지원되지 않습니다. Experience Cloud ID가 있는 방문자만 결합됩니다.
* 고객 지원 센터는 아직 이 기능을 완전히 지원하지는 않습니다. 이 기능에 대한 지원을 위해 [Cross-Device Analytics 포럼](https://forums.adobe.com/community/experience-cloud/analytics-cloud/analytics/cross-device-analytics/overview)을 이용할 수 있으며 여기에는 Adobe 제품 관리자의 적극적이고 직접적인 참여가 포함됩니다.
* Cross-Device Analytics는 가상 보고서 세트 및 보고서 처리 시간을 사용하는데, 여기에는 자체 제한 사항도 있습니다. 이러한 제한 사항에 대한 자세한 내용은 [가상 보고서 세트](../vrs/vrs-about.md) 및 [보고서 처리 시간](../vrs/vrs-report-time-processing.md)을 참조하십시오.
* 1.4 API가 지원되지 않습니다. Power BI 커넥터와 Report Builder 모두 1.4 API에 의존하며, 따라서 CDA와 호환되지 않습니다.
* 사이트를 방문하는 새 장치는 Co-op 그래프 또는 Private 그래프로 처리하는 데 최대 2주가 소요될 수 있습니다. 가장 최근 2주 동안 CDA의 결합 수준은 일반적으로 그 이전까지 날짜 범위의 수준보다 낮습니다. Adobe에서는 향후 새로운 장치를 실시간으로 결합하기 위해 Adobe Experience Platform ID 서비스를 개선할 계획입니다.
* 가상 보고서 세트의 내역 데이터는 Adobe 인식 및 결합 장치를 기반으로 변경됩니다. 소스 보고서 세트의 데이터는 변경되지 않습니다.

조직이 모든 요구 사항을 충족하고 제한 사항을 이해하면 [Cross-Device Analytics 설정](cda-setup.md)을 시작할 수 있습니다.
