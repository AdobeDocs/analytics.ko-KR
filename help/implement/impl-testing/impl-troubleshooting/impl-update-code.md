---
description: Adobe에서는 Analytics 코드를 업데이트하는 우수 사례를 제공합니다.
keywords: Analytics 구현
seo-description: Adobe에서는 Analytics 코드를 업데이트하는 우수 사례를 제공합니다.
seo-title: Analytics 코드 바꾸기
solution: Analytics
subtopic: 문제 해결
title: Analytics 코드 바꾸기
topic: 개발자 및 구현
uuid: D 3 EA 6585-199 F -4 DBE -9 EE 8-15 B 204689 F 2 F
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Analytics 코드 바꾸기

Adobe에서는 Analytics 코드를 업데이트하는 우수 사례를 제공합니다.

흔히 고객들은 Adobe [!UICONTROL 코드 관리자]를 사용하여 코드를 최신 버전으로 바꿉니다. 이것은 몇 가지 사항을 기억해 두기만 한다면 좋은 방법입니다.

## 잘못된 데이터 수집 서버 ID 사용 {#section_1726CEB1ABEC408492569B06664410C8}

간혹 Adobe 코드 관리자로부터 생성되지 않은 일반적인 [!DNL s_code.js] 파일이 사이트에서 코드를 구현하는 담당자들에게 보내지고, 그로 인해 계좌에 대해 잘못된 데이터 수집 서버 ID([!UICONTROL s.dc] 변수에서 보듯이)가 사용되기도 합니다. 다른 보고서 세트의 코드를 다시 사용하기 보다는, [!UICONTROL 코드 관리자]에서 바로 특정 보고서 세트용의 새로운 코드를 생성하는 것이 가장 좋습니다. 이것이 [!UICONTROL s.dc] 변수를 확실하게 올바로 채우는 가장 좋은 방법입니다.

## 플러그인 {#section_53650E52D6A54A4795F95E491E7548D1}

어떤 고객들은 Adobe 환경을 향상시키고자 플러그인을 구현하기도 합니다. 코드를 바꿀 때는, 해당 코드의 일부로 플러그인을 가지고 있다는 것을 잊지 마십시오. [!UICONTROL 코드 관리자]에서 만들어진 코드에는 플러그인 코드가 들어 있지 않습니다. 따라서 모든 플러그인은 더 최신 코드 기반으로 직접 마이그레이션해야 합니다. 어떤 문제가 발생하여 이전 코드로 돌아가야 하는 경우에 대비하여 기존 코드의 사본을 만드십시오.
