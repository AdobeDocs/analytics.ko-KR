---
title: Cross-Device Analytics
description: 크로스 디바이스 분석은 장치 데이터를 함께 결합함으로써 데이터를 장치 중심의 데이터에서 사람 중심의 데이터로 변경합니다.
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Cross-Device Analytics

> [!NOTE] 크로스 장치 분석 문서는 기능이 추가로 개발되면 변경될 수 있습니다. 정기적으로 업데이트를 확인하십시오.

크로스 디바이스 분석은 Analytics를 장치 중심 보기에서 사람 중심의 보기로 변환하는 기능입니다. 이 기능은 Adobe Experience Platform Identity Service Co-op Graph 또는 Private Graph를 사용하여 개인에게 속한 디바이스를 식별하고 함께 결합합니다. 따라서 애널리스트는 브라우저, 디바이스 또는 앱을 넘나드는 사용자 행동을 이해할 수 있습니다. CDA를 사용하여 다음과 같은 질문에 답변할 수 있습니다.

* 얼마나 많은 사람들이 내 브랜드와 상호 작용하고 있습니까? 얼마나 많은 장치와 어떤 유형의 장치를 사용하고 있습니까? 어떻게 중첩됩니까?
* 사람들이 모바일 장치에서 작업을 시작한 다음 나중에 데스크탑 PC로 이동하여 작업을 완료하는 빈도는 얼마나 됩니까? 하나의 장치에 랜딩되는 캠페인 클릭스루가 다른 곳에서 전환을 가져옵니까?
* 장치 간 여정을 고려하면 캠페인 효과에 대한 이해가 어떻게 달라집니까? 단계 분석은 어떻게 변경됩니까?
* 사용자가 하나의 장치에서 다른 장치로 이동하는 가장 일반적인 경로는 무엇입니까? 어디에서 중단됩니까? 어디에서 성공합니까?
* 여러 장치가 있는 사용자의 행동은 단일 장치가 있는 사용자와 어떻게 다릅니까?

장치가 연결되면 변수 지속성이 장치 간에 전달됩니다. 예를 들어 사용자가 먼저 데스크톱 컴퓨터의 광고를 통해 사이트를 방문합니다. 해당 사용자는 모바일 앱을 찾아 설치한 다음 모바일 디바이스에서 구매합니다. 크로스 디바이스 분석을 사용하면 데스크탑 컴퓨터에서 클릭한 광고로 매출이 달라질 수 있습니다.

Journey [IQ:크로스 디바이스 분석 Spark 페이지에서](http://adobe.ly/aacda) 크로스 디바이스 분석의 기능과 기능에 대해 자세히 알아보십시오.

## 전제 조건

2019년 9월 현재 크로스 디바이스 분석에는 다음이 필요합니다. 조직 내 팀과 Adobe 계정 관리자를 사용하여 다음 사항을 모두 충족할 수 있습니다.

> [!IMPORTANT] 모든 사전 요구 사항을 충족하지 못하면 크로스 장치 분석을 활성화할 수 없거나 데이터를 연결할 때 결과가 좋지 않을 수 있습니다.

* 조직의 데이터는 Adobe의 태평양 연안 북서부 데이터 센터 내에 있어야 합니다. 세계 다른 지역의 데이터 센터에 대한 지원이 예정되어 있습니다.
* 조직의 계정 관리자에게 문의하여 다음 주요 사항을 설정하십시오.
   * 계약은 Adobe Analytics Ultimate가 포함된 Adobe와 체결되어야 합니다.
   * 조직은 Adobe Experience Platform Identity Service Co-op 그래프 또는 Private Graph를 사용해야 합니다. Device [Co](https://docs.adobe.com/content/help/en/device-co-op/using/home.html) -op 사용 안내서의 홈 페이지를 참조하십시오.
   * 조직은 Adobe가 Microsoft Azure 서버에서 Analytics 데이터를 처리하고 저장하도록 허용하기로 동의해야 합니다. Adobe는 Azure를 사용하여 장치 그래프 데이터를 저장하고 장치 스티칭을 수행합니다. 따라서 Adobe Analytics 데이터는 Adobe의 데이터 처리 센터와 Microsoft Azure에서 Adobe의 현재 상태 간에 전달됩니다.
* 장치 간 분석은 보고서 세트별로 활성화됩니다. CDA 파섹
   * 보고서 세트에는 일일 히트 수가 1억 개를 초과할 수 없습니다. 이 임계값은 앞으로 몇 달 동안 증가할 것입니다.
   * Adobe에서는 보고서 세트에 여러 장치 유형(웹, 앱 등)의 데이터를 의미하는 크로스 장치 데이터가 들어 있는 것이 좋습니다. 일부 조직은 이 개념을 "글로벌" 보고서 세트로 언급하지만, CDA는 지리적 관점에서 글로벌화되어야 하는 것은 아닙니다. 장치 간 분석은 보고서 세트 간에 작동하지 않으며 여러 보고서 세트의 데이터를 결합하지 않습니다.
* 구현은 다음 요구 사항을 충족해야 합니다.
   * Experience Cloud ID 서비스의 최신 버전을 배포해야 합니다. Experience [Cloud](https://docs.adobe.com/content/help/en/id-service/using/home.html) Identity Service 사용 안내서의 홈 페이지를 참조하십시오. Adobe Experience Platform Launch를 사용하는 대부분의 구현에 이미 ECID가 배포되어 있을 수 있습니다.
   * 사용자가 로그인하거나 이메일을 여는 경우와 같이 개인을 식별할 수 있을 때마다 이 `setCustomerIDs` 함수를 호출합니다. 이 요구 사항은 모바일 앱을 비롯한 모든 플랫폼에 적용됩니다. Experience [Cloud](https://docs.adobe.com/content/help/en/id-service/using/id-service-api/methods/setcustomerids.html) Identity Service 사용 안내서의 setCustomerIDs를 참조하십시오.

## 제한

Cross-Device Analytics는 혁신적이고 강력한 기능이지만 사용 방법에 대한 제한이 있습니다.

* CDA는 분석 작업 공간을 통해서만 사용할 수 있습니다.
* 위의 사전 요구 사항에 설명된 대로 보고서 세트에서 스티칭을 수행할 수 없습니다.
* Adobe Analytics 보고서 세트는 두 개 이상의 IMS 조직에 매핑할 수 없습니다. 지정된 보고서 세트 내에서 CDA 스티치 장치를 사용하기 때문에 CDA를 사용하여 여러 IMS 조직에서 데이터를 연결할 수 없습니다.
* CDA는 현재 고객 속성과 호환되지 않습니다. 고객 속성은 CDA 가상 보고서 세트를 만들거나, 크로스 장치 세그먼트 내에서 또는 CDA 가상 보고서 세트를 기반으로 하는 분석 작업 공간 프로젝트 내에서 보고하는 데 사용할 수 없습니다.
* CDA에는 Co-op 그래프 또는 Private Graph가 필요합니다. 타사 장치 그래프는 지원되지 않습니다.
* 기존 Analytics ID는 지원되지 않습니다. Experience Cloud ID가 있는 방문자만 스티칭됩니다.
* 고객 지원 센터는 아직 이 기능을 완전히 지원하지 않습니다. 크로스 [디바이스 분석 포럼은](https://forums.adobe.com/community/experience-cloud/analytics-cloud/analytics/cross-device-analytics/overview) Adobe 제품 관리자의 적극적인 직접 참여를 포함하는 이 기능을 지원하기 위해 사용할 수 있습니다.
* 장치 간 분석에서는 가상 보고서 세트와 보고서 시간 처리를 사용하며, 이러한 작업은 고유 제한이 있습니다. 이러한 [제한에 대한 자세한 내용은 가상 보고서 세트](../vrs/vrs-about.md) 및 [보고서 시간 처리를](../vrs/vrs-report-time-processing.md) 참조하십시오.
* 사이트를 방문하는 새 장치는 Co-op Graph 또는 Private 그래프로 처리하는 데 최대 2주가 걸릴 수 있습니다. 최근 2주 동안 CDA의 스티칭 수준은 일반적으로 2주가 지난 날짜 범위에 비해 낮습니다. Adobe는 향후 새로운 디바이스를 실시간으로 연결할 수 있도록 Adobe Experience Platform Identity Service를 개선할 계획입니다.
* 가상 보고서 세트의 내역 데이터는 Adobe가 장치를 인식하고 결합하는 것을 기준으로 변경됩니다. 소스 보고서 세트의 데이터는 변경되지 않습니다.

조직에서 모든 요구 사항을 충족하고 제한 사항을 이해하면 크로스 [장치 분석 설정을 시작할 수 있습니다](cda-setup.md).
