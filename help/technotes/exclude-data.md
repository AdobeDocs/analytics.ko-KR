---
title: Adobe Analytics에서 데이터 제외
description: 데이터 수집 전후에 데이터를 제외하는 것과 관련한 다양한 방법에 대해 알아봅니다.
exl-id: dee5bf3b-8bb3-48eb-908d-b4a981f17bfb
feature: Data Configuration and Collection
source-git-commit: c697530103ea7cd279cc3560c1daec796759e7a1
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 96%

---

# Adobe Analytics에서 데이터 제외

데이터 제외는 일반적으로 조직의 테스트 작업이 프로덕션 데이터를 채우는 것을 방지하거나 원하지 않는 데이터가 보고서를 잘못 부풀리는 것을 방지하는 데 사용됩니다. 사용 사례에 따라 Adobe Analytics에서 데이터를 제외하려면 다음 방법 중 하나를 사용하십시오.

## 데이터 수집 후 데이터 제외

다음 방법은 Adobe 데이터 수집 서버가 이미지 요청을 받은 후 Analytics 보고에서 데이터를 제외하는 방법입니다. 이러한 방법을 사용하여 제외된 데이터는 여전히 청구 가능한 서버 호출에 포함됩니다.

* **IP로 제외**: Adobe Analytics는 보고서 세트에서 IP 주소 또는 범위에 대한 데이터를 제외하는 기본 기능을 제공합니다. 관리자 사용 안내서의 [IP로 제외](/help/admin/admin/exclude-ip.md)를 참조하십시오.
* **봇 규칙**: 봇 규칙은 알려진 봇 사용자 에이전트 문자열에서 트래픽을 가져와 Analytics 보고서에서 제외합니다. 봇 규칙을 통해 제외된 데이터는 봇 보고서에 배치됩니다. 추가 데이터를 제외하기 위해 사용자 지정 봇 규칙을 만들 수 있습니다. 관리자 사용 안내서의 [봇 규칙](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md)을 참조하십시오.
* **VISTA 규칙**: 조직의 필요에 따라 사용자의 요구 사항과 일치하는 히트는 제외된 데이터 수신 전용의 다른 보고서 세트로 전송됩니다. VISTA 규칙은 일반적으로 IP 주소에 대해 사용되지만 이에 국한되지는 않습니다. 모든 차원을 사용하여 보고서 세트에 데이터를 포함하거나 제외할 수 있습니다. VISTA 규칙에는 추가 비용이 적용됩니다. 자세한 내용은 Adobe 계정 팀에 문의하십시오.
* **옵트아웃 쿠키**: 귀하의 사이트에 대한 모든 방문자는 귀하의 추적 서버와 관련된 페이지를 방문하여 Adobe Analytics에서 추적되는 것을 자발적으로 거부할 수 있습니다. 구현 사용 안내서의 [옵트아웃 링크 구현](/help/implement/js/opt-out.md)을 참조하십시오.

>[!TIP]
>
>처리 규칙은 데이터를 제외하거나 다른 보고서 세트로 데이터를 보낼 수 없습니다. 그러나 특정 변수는 조건부로 설정할 수 있으며 세그먼트를 사용하여 해당 데이터를 보고에서 제외할 수 있습니다.

## 데이터 수집 전 데이터 제외

특정 히트가 Analytics 데이터 수집 서버에 도달하지 못하도록 하려면 [`abort`](/help/implement/vars/config-vars/abort.md) 변수를 사용하십시오. 이 플래그는 이미지 요청이 전송되지 않도록 합니다. 중단된 이미지 요청은 Adobe 데이터 수집 서버에 도달하지 않으므로 청구 가능한 서버 호출은 증가하지 않습니다.
