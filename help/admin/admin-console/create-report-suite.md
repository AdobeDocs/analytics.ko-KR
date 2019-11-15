---
title: 보고서 세트 만들기
description: Adobe Analytics에서 데이터 수집에 대한 기본 컨테이너를 만듭니다.
translation-type: tm+mt
source-git-commit: 6c57780d0ecf65669c1a5306dde267f6e48f1cc4

---


# 보고서 세트 만들기

보고서 세트는 Adobe Analytics에서 보고서를 가져오는 데 사용하는 데이터의 사일로입니다. 조직에는 여러 보고서 세트가 있을 수 있으며 각 보고서 세트는 서로 다른 데이터 세트를 포함합니다. 이전에는 개별 보고서 세트가 중요했지만 단일 보고서 세트가 더 유리해졌습니다. 가상 보고서 세트 및 보고서 시간 처리를 도입하면 사용자가 고유한 데이터 하위 세트를 만들어 글로벌 및 사이트별 데이터를 모두 유연하게 얻을 수 있습니다.

이 문서는 시스템 수준 관리자 또는 분석 관리자가 데이터 수집을 준비할 수 있도록 만들어졌습니다.

## 전제 조건

[Adobe Analytics 첫 번째 관리 안내서](first-admin-guide.md):시스템 수준 관리자가 Experience Cloud 관리 콘솔을 통해 Adobe Analytics에 대한 액세스 권한을 부여했는지 확인

## 보고서 세트 만들기

> [!NOTE] 이전 관리자를 사용하여 Adobe Analytics에서 보고서 세트를 만드는 방법도 있습니다. 여기에 설명된 보고서 세트 설정 마법사를 사용하는 것이 좋습니다.

1. Adobe ID 자격 증명을 사용하여 [experiencecloud.adobe.com](https://experiencecloud.adobe.com)에 로그인합니다.
1. 오른쪽 상단에 있는 9제곱 아이콘을 클릭한 다음 컬러 Analytics 로고를 클릭합니다.
1. 'Adobe Analytics 시작' 모달 창이 자동으로 표시됩니다. 그렇지 않은 경우 오른쪽 상단의 도움말 아이콘을 클릭한 다음 'Adobe Analytics에 오신 것을 환영합니다'를 선택합니다.
1. 모달 창에서 설정 시작을 클릭합니다.
1. 속성 유형, 산업 분야 및 표준 시간대 등의 기본 사항을 대략적으로 설명하는 각 지침을 따르십시오. 다음을 클릭합니다.
1. 이제 보고서 세트가 생성됩니다. 또한 개발 보고서 세트를 사용하는 것이 좋습니다. 따라서 테스트에 고객 데이터가 포함되지 않습니다. 오른쪽 상단에 있는 도움말 아이콘을 클릭한 다음 'Adobe Analytics에 오신 것을 환영합니다'를 다시 선택합니다.
1. 모달 창에서 설정 시작을 클릭합니다.
끝에 "- DEV"를 추가하는 것을 제외하고 이 보고서 세트의 이름을 동일하게 지정합니다. 이 보고서 세트는 내부 트래픽만 수신하므로 예상 크기는 가장 작을 수 있습니다.
1. 다음을 클릭하여 개발 보고서 세트 만들기를 완료합니다.

## 문제 해결

**Experience Cloud에 로그인한 후 Analytics 아이콘이 회색으로 표시됩니다.**

이는 계정에 Analytics에 대한 올바른 권한이 부여되지 않았음을 의미합니다. 조직의 시스템 수준 관리자와 함께 작업하여 Adobe Analytics에 액세스할 수 있는 권한이 있는 프로필에 속해 있는지 확인합니다.

**Adobe Analytics에 로그인한 후 'Adobe Analytics 시작' 팝업과 드롭다운이 없습니다.**

my.omniture.com을 통해서가 아니라 Experience Cloud를 통해 로그인했는지 확인하십시오. my.omniture.com을 통해 로그인한 사용자는 보고서 세트 설정 마법사를 사용할 수 없습니다.

## 다음 단계

[Launch에서 Adobe Analytics에 대한 속성 만들기 및 구성](/help/implement/implement-with-launch/create-analytics-property.md):Analytics 구현을 관리할 영역 만들기
