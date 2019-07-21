---
source-git-commit: d8f2458e7bae596dbabc8dab33ea5d2881047566
translation-type: tm+mt

---
# Adobe Analytics의 제품 프로필

제품 프로필은 제품 관리자가 조직 내에서 사용자에게 할당할 수 있는 권한 사전 설정입니다. 제품 프로필을 만들고 Experience Cloud 사용자를 해당 제품 프로필에 지정하는 경우 제품 프로필에 포함된 권한 항목이 상속됩니다.

See [Manage products and profiles](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html) in the Enterprise user guide for general information on product profiles.

## 제품 프로필 관리자

제품 프로필 관리자는 해당 제품 프로필에 사용자를 추가하거나 제거할 수 있는 선택 그룹입니다. 제품 프로필 관리자는 제품 관리자와 다릅니다.

* 제품 프로필 관리자는 제품 프로필의 사용자 목록에 대한 책임을 집니다.
* 제품 프로필 관리자는 Adobe Analytics에 대한 전체 액세스 권한이 없습니다. Adobe Analytics에 대한 전체 액세스는 제품 관리자용으로 예약되어 있습니다.
* 제품 프로필 관리자는 제품 프로필에서 권한 항목을 조정할 수 없습니다. 제품 관리자가 권한 항목을 조정해야 합니다.
* 제품 프로필 관리자는 팀을 위한 Adobe Analytics에 대한 액세스 권한을 부여 받고 관리하는 팀 리드의 경우 이상적입니다. 개인 사용자는 시스템 관리자나 제품 관리자에게 Adobe Analytics에 대한 액세스 권한을 부여할 필요가 없습니다.

## Adobe Analytics 권한 항목

Adobe Analytics에 액세스하기 위해 제품 프로필에서 필요한 최소 권한은 다음과 같습니다.

* 제품 프로필에 하나 이상의 보고서 세트에 대한 액세스 권한이 있어야 합니다.
* The product profile must belong to the Analytics Tools permission item **Analysis Workspace Access** (or **Reports &amp; Analytics Access**)

### 보고서 세트

Analytics 조직에 속한 보고서 세트에 대한 액세스 권한을 부여합니다. 사용자는 Adobe Analytics를 사용할 수 있는 액세스 권한이 있는 보고서 세트에 속해 있어야 합니다.

### 지표

보고서 세트의 지표에 대한 액세스 권한을 부여합니다. 지표는 분석 작업 공간에 해당 구성 요소로 나열되거나, 지표가 보고 및 분석에서 사용할 수 있으며 사이트 지표 아래의 메뉴 항목으로 사용할 수 있습니다.

사용자 지정 지표는 보고서 세트와 독립적으로 유지하려면'사용자 지정 이벤트 1-1000 ' 레이블이 지정되어 있어야 합니다. ' 사용자 지정 이벤트 1 ' 이 활성화된 권한 항목인 경우 해당 사용자는 제품 프로필에 있는 모든 보고서 세트의 이벤트 1에 액세스할 수 있습니다.

### 차원

보고서 세트의 차원에 대한 액세스 권한을 부여합니다. 차원은 분석 작업 공간에 해당 구성 요소로 나열되거나, 차원을 메뉴 항목으로 사용할 수 있는 보고 및 분석에서 사용할 수 있습니다.

Evar와 같은 사용자 지정 변수는 보고서 세트와 독립적으로 유지하기 위해'사용자 지정 전환 1-250 ' 레이블이 지정됩니다. ' 사용자 지정 전환 1 ' 이 활성화된 권한 항목인 경우 해당 사용자는 제품 프로필에 있는 모든 보고서 세트의 Evar 1에 액세스할 수 있습니다.

### 보고서 세트 도구

보고서 세트 도구 권한 항목은 사용자가 액세스할 수 있는 보고서 세트에 대한 기능에 대한 액세스 권한을 부여합니다. See [Report Suite Tools](report-suite-tools.md) for a full list of permission items and descriptions.

### Analytics 도구

Analytics 도구 권한 항목은 보고서 세트 설정과 독립적인 기능에 대한 액세스 권한을 부여합니다. See [Analytics Tools](analytics-tools.md) for a full list of permission items and descriptions.

## 제품 프로파일 개발자

Developers are similar to users, except they are granted the ability to use the Experience Cloud API on Adobe I/O. See [Manage Developers](https://helpx.adobe.com/enterprise/using/manage-developers.html) in the Enterprise user guide for more information.
