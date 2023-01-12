---
description: 보고 데이터에 대한 액세스를 제어할 수 있도록 해 줍니다. 강력한 암호, 암호 만료일, IP 로그인 제한 및 이메일 도메인 제한 옵션이 제공됩니다.
title: 보안 관리자
feature: Company Settings
exl-id: 6dcf0354-4b4a-4bd5-ba6c-ae42c7b9e4df
source-git-commit: 0017a6657e4de6206cf97dc6cf6f2b132b50b50f
workflow-type: ht
source-wordcount: '489'
ht-degree: 100%

---

# 보안 관리자

보안 관리자를 사용하여 보고 데이터에 대한 액세스를 제어할 수 있습니다. 강력한 암호, 암호 만료일, IP 로그인 제한 및 이메일 도메인 제한 옵션이 제공됩니다.

## 설정

**[!UICONTROL Analytics]** > **[!UICONTROL 관리자]** > **[!UICONTROL 모든 관리자]** > **[!UICONTROL 회사 설정]** > **[!UICONTROL 보안]**

| 설정 | 설명 |
| --- | --- |
| 강력한 암호 필요 | 다음 규칙을 준수하는 것보다 안전한 암호를 사용하도록 강제로 설정합니다. <ul><li>최소 8자 길이여야 합니다.</li><li>첫 문자와 마지막 문자 사이에 기호나 숫자가 한 개 이상 있어야 합니다.</li><li>하나 이상의 알파벳 문자가 있어야 합니다.</li><li>사전에서 찾을 수 없거나 사전의 단어(영어)를 포함하지 않아야 합니다.</li><li>로그인 사용자 이름에 있는 연속하는 세 개의 문자를 포함할 수 없습니다.</li><li>이전 10개 암호와 달라야 합니다.</li></ul>**참고**: 이 기능은 앞으로 새 암호로 시행됩니다. 이것은 기존 암호를 확인하거나 사용자가 기존 암호를 변경하게 하지 않습니다. 따라서 암호 만료일을 활성화하여 사용자가 암호를 변경하고 강력한 암호 규칙을 따르게 하십시오. |
| 암호 만료일 | 사용자가 계정 암호를 정기적으로 변경하도록 강제로 설정합니다. 암호를 만료할 간격을 지정하고, 즉각 암호 만료를 시행할 수 있습니다. |
| IP 로그인 제한 적용 | (이 기능은 2021년 1월부터 더 이상 사용할 수 없습니다.)<br> 특정 IP 주소 또는 IP 주소 범위에 대한 보고서 액세스를 제한합니다. IP 주소 필터 목록에서 최대 100개의 항목을 추가할 수 있으며 각 항목은 특정 주소 또는 주소 범위일 수 있습니다. IP 주소 필터 목록에 하나 이상의 항목이 있을 때까지 IP 로그인 제한 적용이 적용되지 않습니다. 허가한 IP 주소: IP 주소 범위를 지정하려면 대괄호로 범위를 묶습니다(예: `192.168.10.[20-240]`). 또한 와일드카드를 사용하여 0에서 255 사이의 숫자를 지정할 수 있습니다(예: `192.168.[10-14].*8`) 실패한 로그인이 기록되고 [사용 및 액세스 로그](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/logs.html#section_6FBAF92D9EA244809C45A78A2F0A7232)에서 볼 수 있습니다. |
| 이메일 도메인 제한 적용 | Analytics가 책갈피, 다운로드 가능한 보고서 및 경고를 보내는 이메일 주소 및 도메인을 필터링합니다. 이메일 필터 목록은 최대 100개의 항목을 지원하며, 각 항목은 이메일 주소 또는 전체 이메일 도메인일 수 있습니다. 예약된 보고서에 승인되지 않은 이메일 대상이 있는 경우 Analytics는 해당 문제에 대한 이메일 알림 및 이 보고서의 예약을 취소할 수 있는 링크를 보냅니다. ****&#x200B;허가한 이메일 도메인 필터 목록에 하나 이상의 항목이 있을 때까지 이메일 도메인 제한 적용은 적용되지 않습니다. **[!UICONTROL 허가한 이메일 주소 및 도메인]**: IP 주소 범위를 지정하려면 대괄호로 범위를 묶습니다(예: `192.168.10.[20-240]`). 와일드카드를 사용하여 0에서 255 사이의 숫자를 지정할 수도 있습니다(예: `192.168.[10-14].*`) |
| 암호 복구 알림 | 사용자가 사용자 계정 암호를 재설정하려고 할 때 지정된 관리자에게 알립니다. **[!UICONTROL 사용 가능한 관리자]**: 모든 관리자를 표시합니다. Ctrl 키 및 Shift 키를 누른 상태로 여러 관리자를 선택할 수 있습니다. **[!UICONTROL 이메일 구성원]**: 현재 정의된 이메일 그룹을 표시합니다. |