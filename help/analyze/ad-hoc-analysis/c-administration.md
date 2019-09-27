---
description: 사용자를 구성하고 데이터 샘플링에 대해 알 수 있습니다.
seo-description: 사용자를 구성하고 데이터 샘플링에 대해 알 수 있습니다.
seo-title: 관리
title: 관리
uuid: 12f90223-139f-4a8d-bfd3-5cd9af7489d2
translation-type: tm+mt
source-git-commit: 0dbc8ac9b416ce50f197a884bb71c6cd389cd0bb

---


# 관리

사용자를 구성하고 데이터 샘플링에 대해 알 수 있습니다.

For [!DNL Admin Console] help, see the [Analytics Reference](https://marketing.adobe.com/resources/help/en_US/reference/index.html).

## 사용자 라이센스 {#concept_C1440741C77C471EB38A243B013EA620}

사용자 라이센스가 부여된 사용자만 로그인할 수 있습니다. 사용자 라이센스는 동시 사용 라이센스입니다. 사용자 라이선스는 공유할 수 있지만 주어진 시간의 사용자 수는 구입한 사용자 라이선스의 수로 제한됩니다.

<!-- 

c_user_license.html

 -->

로그인한 사용자 수가 사용 가능한 라이선스 수를 초과하면 대화 상자는 사용 가능한 모든 라이선스를 사용 중이라고 알려줍니다. 큐에서 사용자의 위치는 큐 위치를 다시 확인하도록 링크와 함께 표시됩니다. 라이센스를 사용할 수 있게 되면 사용자에게 이메일이 전송되고 Ad Hoc Analysis에 액세스할 수 있다는 내용의 팝업 대화 상자가 표시됩니다. 사용자는 15분 내에 응답할 수 있으며 그 시간이 지나면 큐에서의 위치를 잃게 됩니다.

## 사용자 라이센스 부여 {#task_22AE669703EC48BA9685414538D8B1FA}

Reports &amp; Analytics 로컬 관리자가 권한 시스템을 통해 사용자 라이센스를 부여할 수 있는 방법을 설명하는 단계입니다.

<!-- 

t_user_licenses.xml

 -->

1. 에 [!DNL Experience Cloud]로그인합니다.
1. Click **[!UICONTROL Admin]** &gt; **[!UICONTROL User Management]**.
1. Click **[!UICONTROL Edit Groups]**.

   회사에서 사용자 라이센스를 구입한 경우 [!UICONTROL Ad Hoc Analysis 라이센스 사용자] 그룹이 [!UICONTROL 그룹 이름] 열에 나타납니다. 사용자 로그인에 대한 사용 가능한 라이센스 수도 표시됩니다.

1. Click **[!UICONTROL Edit]**.
1. [!UICONTROL 사용자 로그인 지정]**에서 그룹에 추가할 사용자를 선택하고[!UICONTROL 추가]를 클릭합니다.**
1. Click **[!UICONTROL Save Group]**.

   라이선스 시스템은 그룹에 추가되는 사용자 수를 제한하지 않습니다. 구입한 사용자 라이센스 수는 동시 사용을 제한합니다.

## 사용자 세션 관리 {#task_868C3DD9CB3F45D19B98EEF60F5E0B32}

관리자가 사용자의 세션을 종료할 수 있는 방법을 설명하는 단계입니다. 이 기능은 종료된 사용자가 다시 로그인하는 것을 막지 않습니다.

<!-- 

t_managing_users.xml

 -->

1. Click Adobe Analytics &gt; Admin &gt; User Management, then click Manage Users.****************
1. 사용자를 찾은 다음 **[!UICONTROL 종료]를 클릭합니다.**

   [!UICONTROL 활성 Ad Hoc Analysis 세션] 페이지에서, 유휴 상태였던 사용자가 목록의 맨 위에 가장 오래 표시됩니다.

## 권한 {#concept_A7F2A7600BFF47C38D7C980E08D395B8}

<!-- 

c_permissions.xml

 -->

You set up access to report suites in the [!DNL Administration Console]. 보고서 세트 수준에서 권한을 구성할 수 있습니다. 예를 들어, 활성화된 보고서 세트가 여러 개 있지만 모든 사용자에게 모든 보고서 세트에 대한 액세스 권한을 주고 싶지 않을 경우에는 특정 보고서 세트로 그룹을 만들어 해당 사용자를 해당 그룹에 지정할 수 있습니다.

## 모든 보고서 액세스 그룹에 사용자 추가 {#task_E821BF3B4FDB434D844A98AAB15487A9}

모든 보고서 세트에 대한 액세스 권한을 비관리 사용자에게 부여하는 방법을 설명하는 단계입니다.

<!-- 

t_permissions.xml

 -->

1. Log in to the **[!UICONTROL Experience Cloud]**.
1. Click **[!UICONTROL Adobe Analytics &gt; Admin]** &gt; **[!UICONTROL User Management]** &gt; **[!UICONTROL Edit Groups]**.
1. Click **[!UICONTROL All Report Access]**.
1. [!UICONTROL 사용 가능한 사용자]**에서 사용자를 선택한 다음[!UICONTROL 추가]를 클릭합니다.**
1. Click **[!UICONTROL Save Group]**.

## 권한 그룹 만들기 {#task_65A4C2E58B13475B9B2606CEB93B7CBD}

특정 보고서 세트에 대해 비관리 사용자를 위한 권한 그룹을 만듭니다.

<!-- 

t_permission_groups.xml

 -->

1. Log in to the **[!UICONTROL Experience Cloud]**.
1. Click **[!UICONTROL Adobe Analytics &gt; Admin]** &gt; **[!UICONTROL User Management]** &gt; **[!UICONTROL Edit Groups]**.
1. 액세스를 허용할 비관리 사용자에 대해 Ad Hoc Analysis이 활성화된 보고서 세트를 포함하는 권한 그룹을 만듭니다.

   사용자가 사용할 수 있는 보고서 세트는 새 프로젝트를 만들 때 [!UICONTROL 보고서 클라우드] 메뉴에 표시됩니다.

## Java로 프록시 정책 설정 {#task_3B03F58519544025B55CF54FACF8F4F5}

서버 연결 오류를 받을 경우 프록시 정책을 설정하는 방법을 설명하는 단계입니다.

<!-- 

t_proxy_policies.xml

 -->

Ad Hoc Analysis에서는 HTTP를 사용하여 서버와 통신합니다. 이것은 다른 HTTP 트래픽과 동일한 프록시 정책을 따릅니다.

1. 에서 [!DNL Windows Control Panel]Java [!UICONTROL 제어판을 시작합니다].
1. **일반** 탭에서 **[!UICONTROL 네트워크 설정을 클릭합니다]**.
1. Select **[!UICONTROL Use browser settings]**, or manually configure the proxy settings.
1. Click **[!UICONTROL OK]**, then click **[!UICONTROL OK]** on the [!UICONTROL Java Control Panel].

## 데이터 샘플링 방식 {#concept_8433CFD38E0243849E92DF4F1E743AC3}

방문자 데이터 샘플을 가져와 정확하고 의미 있는 보고를 생성합니다. 날짜 범위는 로드된 프로젝트의 데이터 구획으로 사용됩니다. 슬라이스는 일반적으로 현재 월과 이전 두 개의 월을 나타냅니다.

<!-- 

c_overview_data_sampling.xml

 -->

최적의 처리를 위해 Ad Hoc Analysis은 구획당 최대 히트 수로 약 750,000,000개의 히트를 사용합니다. (히트 수 = 페이지 보기 횟수 + 이벤트 수)

예상 샘플 비율에 도달하기 위해 데이터 세트당 예상 히트 수를 계산한 다음 750,000,000으로 나눕니다.

* (평균 일일 히트 수 x 슬라이스의 일 수) / 750,000,000

예를 들어 일일 히트 수가 1,000만 개이고 데이터 슬라이스 기간이 90일인 경우:

* (10,000,000 x 90) / 750,000,000 = 1.2

따라서 이 90일 동안의 히트 수를 750,000,000개 미만으로 유지하기 위해 데이터를 1.2:1 비율로 샘플링할 수 있지만, 정수에 대해 샘플링하므로 샘플링 비율은 2:1이 됩니다.

또 다른 예로 일일 히트 수가 1,000만 개이고 데이터 슬라이스 기간이 365일인 경우:

* (10,000,000 x 365) / 750,000,000 = 4.8

따라서 이 365일 동안의 히트 수를 750,000,000개 미만으로 유지하기 위해 데이터를 4.8:1 비율로 샘플링할 수 있습니다. 정수를 사용하여 샘플링 비율은 5:1이 됩니다.

>[!MORE_LIKE_THIS]
>
>* [사용자 ](https://marketing.adobe.com/resources/help/en_US/reference/users.html)
>* [그룹 ](https://marketing.adobe.com/resources/help/en_US/reference/groups.html)

