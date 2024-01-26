---
title: Adobe Experience Platform Edge Network Server API를 사용하여 Adobe Analytics 구현
description: Adobe Experience Platform Edge Network Server API를 사용하여 Adobe Analytics으로 데이터를 전송합니다.
exl-id: 1ede95b7-4f17-4d69-aba6-62b253b6693a
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 33%

---

# Adobe Experience Platform Edge Network Server API를 사용하여 Adobe Analytics 구현

일반적으로 Experience Platform Edge Network Server API를 사용하여 IoT 장치, 셋톱 박스, 데스크탑 애플리케이션과 같은 장치에서 데이터를 수집합니다. 그런 다음 해당 데이터를 Edge 네트워크와 Adobe Analytics 같은 서비스로 전송합니다.

또한 중요한 데이터를 네트워크를 통해 안전하게 수집하고 인증해야 하는 경우 Edge Network Server API를 고려하십시오. 다음을 참조하십시오 [인증](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/authentication.html?lang=en) 추가 정보.

구현 작업에 대한 개략적인 개요:

![Analytics 확장 워크플로를 사용하는 Adobe Analytics](../../assets/edge-network-server-api.png)

<table style="width:100%">

<tr>
<th style="width:5%"></th><th style="width:60%"><b>작업</b></th><th style="width:35%"><b>추가 정보</b></th>
</tr>

<tr>
<td>1</td>
<td><b>보고서 세트를 정의</b>했는지 확인합니다.</td>
<td><a href="../../../admin/admin/c-manage-report-suites/report-suites-admin.md">보고서 세트 관리자</a></td>
</tr>

<tr>
<td>2</td>
<td><b>스키마 설정</b>. Adobe Experience Platform을 활용하는 애플리케이션 전체에서 사용할 데이터 수집을 표준화하기 위해, Adobe는 개방적이고 공개적으로 문서화된 표준인 XDM(경험 데이터 모델)을 만들었습니다.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=ko-KR">스키마 UI 개요</a></td>
</tr>

<tr>
<td>3</td>
<td><b>데이터스트림을 구성합니다</b>. 데이터 스트림은 Adobe Experience Platform Edge Network API의 API를 사용할 때 서버측 구성을 나타냅니다.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=ko-KR">데이터스트림 구성<a></td> 
</tr>

<tr>
<td>4</td>
<td><b>데이터 수집 구현 및 테스트</b> 단일 이벤트 데이터 및 일괄 처리 이벤트 데이터 수집 API 사용.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=en">단일 이벤트 데이터 수집</a><br/><a href="https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/non-interactive-data-collection.html?lang=en">일괄 처리 이벤트 데이터 수집</a>
</tr>

<td>5</td>
<td>데이터스트림에 <b>Adobe Analytics 서비스를 추가</b>합니다. 이 서비스는 데이터가 Adobe Analytics로 전송되는지 여부와 그 방법을 제어합니다.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/interacting-other-adobe-solutions/interacting-adobe-analytics.html?lang=ens">Adobe Analytics과 상호 작용</a></td>
</tr>


</table>

다음을 참조하십시오 [Edge Network Server API 설명서](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=ko-KR)및 예 [Adobe Analytics과 통합](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/interacting-other-adobe-solutions/interacting-adobe-analytics.html?lang=ko-KR) 추가 정보.

