---
title: Adobe Analytics의 VISTA 규칙
description: VISTA 규칙 및 해당 기능에 대해 자세히 알아보십시오.
source-git-commit: 1e2284fd4a62816b27b33a91f3bee2575a852107
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---


# Adobe Analytics의 VISTA 규칙

VISTA 규칙은 데이터 수집과 처리 사이에 적용할 수 있는 사용자 지정 데이터 수정의 대체 형식입니다. 자세한 내용은 [처리 순서](processing-order.md) vista 규칙이 적용되는 데이터 파이프라인의 정확한 단계에 대한 자세한 정보. VISTA 규칙은 수집된 현재 데이터에만 영향을 줍니다. 기존 데이터는 변경되지 않습니다.

VISTA 규칙의 몇 가지 일반적인 사용 사례는 다음과 같습니다.

* 한 보고서 세트에서 다른 보고서 세트로 Analytics 히트를 복사하고, 선택적으로 복사된 보고서 세트로 데이터를 변경합니다
* 에서 제공하는 사용 사례를 초과하는 사용자 지정 IP 제외 [IP별로 제외](/help/admin/admin/exclude-ip.md)
* 변수 값을 조건부로 또는 전역적으로 수정합니다
* 다른 변수에 변수 값이 중복됨
* 변수 값에 영향을 줄 수 있는 Adobe FTP 사이트에 파일을 업로드합니다

VISTA 규칙에 대한 많은 사용 사례는에서 이미 제공합니다. [처리 규칙](/help/admin/admin/c-processing-rules/processing-rules.md), [보트 규칙](/help/admin/admin/bot-removal/bot-rules.md), [가상 보고서 세트](/help/components/vrs/vrs-about.md)또는 Adobe Analytics 구현을 업데이트하기만 하면 됩니다. Adobe은 VISTA 규칙만 마지막 수단으로 권장합니다.

>[!IMPORTANT]
>
>VISTA 규칙에서는 조직과 Adobe Professional Services 간의 유료 계약이 필요합니다. VISTA 규칙을 만들거나 업데이트하려면 조직의 Adobe 계정 관리자에게 문의하십시오.

## VISTA 규칙 만들기

VISTA 규칙을 만들려면 Adobe Professional Services에서 작업해야 합니다. VISTA 규칙을 만들려면 조직의 Adobe 계정 관리자에게 문의하십시오.

## 기존 VISTA 규칙 참조

Adobe은 기존 VISTA 규칙을 보기 위한 UI를 제공하지 않습니다. 기존 VISTA 규칙 목록을 검색하려면 원하는 보고서 세트를 사용하여 조직의 Adobe 계정 관리자 또는 고객 지원 센터에 문의하십시오.
