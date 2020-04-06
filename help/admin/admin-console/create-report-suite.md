---
title: 보고서 세트 만들기
description: Adobe Analytics에서 데이터 수집을 위한 기본 컨테이너를 만듭니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 보고서 세트 만들기

보고서 세트는 Adobe Analytics가 보고서를 가져오는 데 사용하는 데이터의 사일로입니다. 조직에는 여러 개의 보고서 세트가 있을 수 있으며, 각 보고서 세트에는 서로 다른 데이터 세트가 포함되어 있습니다. 이전에는 개별 보고서 세트가 중요했지만 단일 보고서 세트가 더 유용해졌습니다. 가상 보고서 세트 및 보고서 처리 시간을 도입하면 사용자가 고유한 데이터 하위 세트를 만들 수 있으므로, 전역 및 사이트별 데이터를 모두 유연하게 얻을 수 있습니다.

이 문서는 시스템 수준 관리자 또는 분석 관리자가 데이터 수집을 준비할 수 있게 설계되었습니다.

## 전제 조건

[Analytics 첫 번째 관리 시작 안내서](first-admin-guide.md): 시스템 수준 관리자가 Experience Cloud Admin Console을 통해 Adobe Analytics에 대한 액세스 권한을 부여했는지 확인

## 보고서 세트 만들기

>[!NOTE] 이전 관리자를 사용하여 Adobe Analytics에서 보고서 세트를 만드는 방법도 있습니다. 여기에 요약된 보고서 세트 설정 마법사를 사용하는 것이 좋습니다.

1. Adobe ID 자격 증명을 사용하여 [experiencecloud.adobe.com](https://experiencecloud.adobe.com)에 로그인합니다.
1. 오른쪽 상단에 있는 9제곱 아이콘을 클릭한 다음 컬러 Analytics 로고를 클릭합니다.
1. 자동으로 &#39;Adobe Analytics에 오신 것을 환영합니다.&#39; 모달 창이 표시되는 것을 볼 수 있습니다. 자동으로 표시되지 않을 경우 오른쪽 상단의 도움말 아이콘을 클릭한 다음 &#39;Adobe Analytics에 오신 것을 환영합니다.&#39;를 선택합니다.
1. 모달 창에서 설정 시작을 클릭합니다.
1. 속성 유형, 업계 및 시간대 등의 기본 사항을 요약한 각 메시지를 따르십시오. 다음을 클릭합니다.
1. 이제 보고서 세트가 생성됩니다. 또한 테스트 시 고객 데이터가 손상되지 않도록 개발 보고서 세트를 갖고 있는 것이 좋습니다. 오른쪽 상단에 있는 도움말 아이콘을 클릭한 다음 &#39;Adobe Analytics에 오신 것을 환영합니다.&#39;를 다시 선택합니다.
1. 모달 창에서 설정 시작을 클릭합니다.
이 보고서 세트의 이름을 동일하게 지정하되, 이름 끝에 &quot;- DEV&quot;를 추가합니다. 이 보고서 세트는 내부 트래픽만 수신하므로 예상 크기가 가장 작을 수 있습니다.
1. 다음을 클릭하여 개발 보고서 세트 만들기를 완료합니다.

이 모달 창의 단계에 대한 자세한 내용은 구현 [사용 안내서의 구현](/help/implement/prepare/implementation-modal.md) 모달을 참조하십시오.

## 문제 해결

**Experience Cloud에 로그인하면 Analytics 아이콘이 회색으로 표시됩니다.**

이는 계정에 Analytics에 대한 올바른 권한이 부여되지 않았음을 의미합니다. 조직의 시스템 수준 관리자와 함께 Adobe Analytics에 액세스할 수 있는 충분한 권한이 있는 프로필에 속해 있는지 확인합니다.

**Adobe Analytics에 로그인하면 &#39;Adobe Analytics에 오신 것을 환영합니다.&#39; 팝업과 드롭다운이 표시되지 않습니다.**

my.omniture.com을 통해서가 아니라 Experience Cloud를 통해 로그인했는지 확인합니다. my.omniture.com을 통해 로그인한 사용자는 보고서 세트 설정 마법사를 사용할 수 없습니다.

## 다음 단계

[Launch에서 Adobe Analytics에 대한 속성 만들기 및 구성](/help/implement/launch/create-analytics-property.md): Analytics 구현을 관리할 영역 만들기
