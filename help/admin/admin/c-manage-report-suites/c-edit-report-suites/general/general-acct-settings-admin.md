---
description: 관리 기능의 일반 계정 설정 보고서 세트에 대한 필드 설명입니다.
title: 일반 계정 설정
feature: Admin Tools
uuid: c1ab5c34-2c41-4d12-a706-0e760dff8a95
exl-id: f49babb2-8e26-4cc6-b264-b4d7be93f130
source-git-commit: ac3748826d9907cc68076ad39e865f39ea903cf2
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 100%

---

# 일반 계정 설정

관리 기능의 일반 계정 설정 보고서 세트에 대한 필드 설명입니다.

**[!UICONTROL Analytics]** > **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]** > **[!UICONTROL 설정 편집]** > **[!UICONTROL 일반]** > **[!UICONTROL 일반 계정 설정]**

이러한 설정에는 이름 및 시간대와 같은 기본 보고서 세트 기능의 편집 옵션도 포함되어 있습니다.

다음은 일반 계정 설정 구성에 대한 비디오입니다.

>[!VIDEO](https://video.tv.adobe.com/v/332330/?quality=12)

| 옵션 | 설명 |
|--- |--- |
| 사이트 제목 | 사이트를 식별합니다. 각 보고서 세트에 고유한 사이트 제목을 부여합니다. |
| 기본 URL | 보고서 세트의 주 웹 사이트를 지정합니다. 기본 URL은 참조 필터링에 영향을 주지 않습니다. 대신 [내부 URL 필터](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md)를 사용하십시오. |
| 시간대 | 보고서 데이터와 관련된 날짜와 시간을 결정합니다.  라이브 보고서 세트의 시간대를 변경하면 보고서 데이터에 스파이크나 갭이 만들어집니다. 영향을 최소화하려면 비스파이크 시간 동안 시간대를 변경하여 데이터 왜곡을 방지하는 것이 좋습니다.  예를 들어 보고서 세트 시간대를 오후 3시에 중부 표준시에서 태평양 표준시로 변경하면 보고서 세트의 현재 시각은 오후 1시가 됩니다. 보고 기능은 1시간 동안 이미 데이터를 수집했으므로 보고서는 오후 1시 ~ 오후 3시 사이의 트래픽 스파이크를 표시합니다.  또는 보고서 세트 시간대를 오후 3시에 중부 표준시에서 동부 표준시로 변경하면 보고서 세트의 현재 시간은 오후 4시가 됩니다. 보고서는 시간 변경일의 오후 3시 ~ 오후 4시 사이의 데이터를 표시하지 않습니다. |
| 기본 페이지 | [!UICONTROL 최대 방문 페이지 보고서]가 페이지 이름이 아닌 URL을 포함하는 경우 이 설정은 여러 URL이 동일한 페이지를 나타내지 않게 합니다. 예를 들어 URL `https://example.com` 및 `https://example.com/index.html`은 일반적으로 동일한 페이지입니다. 이러한 두 URL이 모두 `https://example.com`으로 표시되도록 기본 파일 이름을 제거할 수 있습니다. 비어 있는 경우 URL에서 index.htm, index.html, index.cgi, index.asp, default.htm, default.html, default.cgi, default.asp, home.htm, home.html, home.cgi및 home.asp 파일 이름이 제거됩니다.  파일 이름이 모두 제거되지 않도록 하려면 URL에서 절대 나타나지 않을 값을 입력하십시오. |
| IP 주소의 마지막 옥텟을 0으로 바꾸기 | 마지막 옥텟 제거는 IP 필터링/제외 전, 보트 규칙 확인 전, 지리적 세분화 조회 전 등 히트에 대한 처리가 완료되기 전에 수행됩니다. 따라서 마지막 옥텟은 0으로 대체되고, IP 제외 규칙은 끝에 0이 있는 IP 주소와 일치하도록 업데이트해야 합니다. 일치 *는 0과 일치해야 합니다. 예를 들어 IP 주소 11.22.33.44은 11.22.33.0으로 변경됩니다. 지리 특성 데이터는 전체 IP 주소를 사용할 때만큼 정확하지는 않습니다. 특히 도시 정확성은 국가 또는 지역 정확성보다 더 많은 영향을 받습니다. 전체 IP 주소는 봇 규칙과 VISTA 규칙에 사용할 수 없으므로 두 규칙 모두 영향을 받습니다. 또한, 마케팅 채널 규칙과 보고서 세트 처리 규칙을 포함하여 IP 기반의 모든 처리 규칙도 이 설정의 영향을 받습니다. <br> **참고**: 이 설정은 2019년 1월 이후 런던 데이터 센터에서 생성된 새 보고서 세트에 대해 기본적으로 활성화되어 있지만 그러한 보고서 세트의 설정이 Admin Console에 나열된 템플릿에서 복사된 경우에만 가능합니다. 다른 보고서 세트와 중복되는 설정이 있는 보고서 세트는 선택한 보고서 세트에서 모든 설정을 상속합니다. |
| IP 난독화 | IP 주소가 인식할 수 없는 문자열로 바뀌어 결국 Adobe 데이터 저장소에서 제거됩니다. 유사 IP 탐지가 활성화되면 원래 IP 주소는 영구적으로 손실됩니다. <br> **참고**: IP 주소는 Data Warehouse를 포함하여 Analytics의 모든 곳에서 난독화되었습니다. 하지만 Target의 IP 설정은 별도로 제어되므로 이 설정은 Target에 영향을 주지 않습니다.<br> IP 난독화가 활성화된 경우 IP 주소가 난독화되기 전에 IP 필터링/제외, 보트 규칙 및 지리적 세분화 조회를 포함하여 필요한 모든 처리가 수행됩니다. IP 난독화를 활성화할 때 아무 것도 변경할 필요가 없습니다.<ul><li>**비활성화됨**&#x200B;을 선택하면 데이터에 IP 주소가 남습니다.</li><li>**IP 주소 난독화**&#x200B;를 확인하면 IP가 두 개의 콜론 뒤에 해시된 값(예: `::1932023538`)으로 변경됩니다.</li><li>**IP 주소 제거**&#x200B;를 선택하면 지역 조회 후 데이터에서 IP 주소가 `::X.X.X.X`로 변경됩니다.</li></ul>****&#x200B;참고: 이 설정을 사용하려면 사용자 정의 [ 보트 규칙](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md) 또는[ IP 제외를 변경해야 할 수 있습니다](/help/admin/admin/exclude-ip.md). |
| 거래 ID 스토리지 | [거래 ID](/help/import/data-sources/transactionid.md) 데이터 소스를 사용할 수 있습니다. |
| Data Warehouse 활성화 | 도구 > Data Warehouse에서 Data Warehouse UI를 활성화합니다. |
| 우편번호 옵션 | 지역 IP 조회 생성 대신 우편번호를 지정할 수 있습니다. |
| 멀티바이트 문자 지원 | 멀티바이트 문자 지원은 UTF-8을 사용하여 보고서 세트의 문자를 저장합니다. 수신 시 시스템에서는 웹 페이지의 문자 세트 데이터를 UTF-8 문자 세트로 전환하므로 마케팅 보고서에서 모든 언어를 사용할 수 있습니다. 기존 보고서 세트에 대한 멀티바이트 문자 지원을 변경하려면 계정 관리자 또는 고객 지원 센터에 문의하십시오. |
| 활성화됨 | 이 보고서 세트가 활성화되는지 여부를 지정합니다. |
| 기본 통화 | 이 보고서 세트에 대한 기본 [통화](https://experienceleague.adobe.com/docs/analytics/implementation/vars/config-vars/currencycode.html)를 지정할 수 있습니다. |
| 조직 ID | 공급된 Experience Cloud 회사와 연결된 ID입니다. 이 ID는 24자의 영숫자 문자열과 @AdobeOrg(포함 필수)로 구성됩니다. |