---
title: 보고서 세트 생성
seo-title: Adobe Analytics에서 보고서 세트 만들기
description: Adobe Analytics에서 데이터 수집을 위한 기본 컨테이너를 만듭니다.
seo-description: Adobe Analytics에서 데이터 수집을 위한 기본 컨테이너를 만듭니다.
translation-type: tm+mt
source-git-commit: d195fb85711f58383577bf1d7b4da4078b909427

---


# 보고서 세트 생성

보고서 세트는 Adobe Analytics가 보고서를 가져오는 데 사용하는 데이터의 일종입니다. 조직에는 각각 다른 데이터 세트를 포함하는 많은 보고서 세트가 있을 수 있습니다. 이전에는 별도의 보고서 세트가 중요했지만, 단일 보고서 세트가 더 유리해졌습니다. 가상 보고서 세트와 보고서 시간 처리 기능에 대한 소개를 통해 사용자는 고유한 데이터 하위 집합을 만들어 글로벌 및 사이트별 데이터를 모두 확보할 수 있습니다.

이 문서는 시스템 수준 관리자 또는 분석 관리자가 데이터 수집을 준비할 수 있도록 설계되었습니다.

## 전제 조건

[Adobe Analytics 첫 번째 관리 안내서](first-admin-guide.md): 시스템 수준 관리자가 Experience Cloud Admin Console를 통해 Adobe Analytics에 대한 액세스 권한을 부여했는지 확인

## 보고서 세트 생성

> [!NOTE]참고: 기존 관리자를 사용하여 Adobe Analytics에서 보고서 세트를 만들 수도 있습니다. Adobe 에서는 여기에 설명된 보고서 세트 설정 마법사를 사용할 것을 권장합니다.

1. Log in to [experiencecloud.adobe.com](https://experiencecloud.adobe.com) using your Adobe ID credentials.
1. 오른쪽 상단의 9 개 사각형 아이콘을 클릭한 다음 컬러 분석 로고를 클릭합니다.
1. ' Adobe Analytics에 오신 것을 환영합니다'모달 창이 자동으로 표시됩니다. 그렇지 않은 경우 오른쪽 상단의 도움말 아이콘을 클릭한 다음'Adobe Analytics에 오신 것을 환영합니다'를 선택합니다.
1. 모달 창에서 [설정 시작] 를 클릭합니다.
1. 속성 유형, 업계 및 표준 시간대와 같은 기본 사항에 대해 설명하는 각 프롬프트를 따릅니다. [다음] 를 클릭합니다.
1. 이제 보고서 세트가 만들어집니다. Adobe 에서는 개발 보고서 세트를 사용할 것을 권장합니다. 따라서 테스트를 통해 고객 데이터를 감염시키지 않습니다. 오른쪽 상단의 도움말 아이콘을 클릭한 다음'Adobe Analytics에 오신 것을 환영합니다'를 다시 선택합니다.
1. 모달 창에서 설정 시작을 클릭합니다.
끝에 "- dev" 를 추가하되 이 보고서 세트의 이름을 동일하게 지정합니다. 이 보고서 세트는 내부 트래픽만 받게 되므로 예상 크기는 가장 작아질 수 있습니다.
1. 다음을 클릭하여 개발 보고서 세트 만들기를 완료합니다.

## 문제 해결

**Experience Cloud에 로그인하면 Analytics 아이콘이 회색으로 표시됩니다.**

이는 계정에 Analytics에 대한 올바른 권한이 부여되지 않았음을 의미합니다. 조직에서 시스템 수준 관리자와 함께 Adobe Analytics에 액세스할 수 있는 적절한 권한이 있는 프로필에 속해 있는지 확인합니다.

**Adobe Analytics에 로그인한 후'Adobe Analytics 시작'팝업 및 드롭다운이 누락되었습니다.**

my. omniture. com 이 아닌 Experience Cloud를 통해 로그인했는지 확인합니다. my.omniture.com를 통해 로그인하는 사용자에게는 보고서 세트 설정 마법사가 없습니다.

## 다음 단계

[Launch에서 Adobe Analytics에 대한 속성을 만들고 구성합니다](../../implement/implement-with-launch/create-analytics-property.md). Analytics 구현을 관리할 영역 만들기
