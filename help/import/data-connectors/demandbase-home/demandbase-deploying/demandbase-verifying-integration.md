---
description: 라이브 추적 및 보고를 확인하여 통합이 데이터를 캡처하는지 확인합니다.
seo-description: 라이브 추적 및 보고를 확인하여 통합이 데이터를 캡처하는지 확인합니다.
seo-title: 통합 확인
title: 통합 확인
uuid: A 9 A 0746 A -4845-41 AE -919 E-E 85 D 95 C 305 BE
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# 통합 확인{#verifying-the-integration}

라이브 추적 및 보고를 확인하여 통합이 데이터를 캡처하는지 확인합니다.

## 라이브 추적 {#section-9c20e8ff6b404ae09387ee07d675c9e2}

Digitalpulse Debugger 도구를 사용하여 Demandbase 차원 데이터가 Adobe Analytics로 전송되고 있는지 확인합니다. 쿠키를 삭제한 후 통합 코드가 배포된 웹 사이트의 페이지를 다시 로드하십시오. 현재 IP 맵이 Demandbase에서 인증한 조직에 매핑되면 다음과 유사한 결과가 표시됩니다.

**보고 및 분석 (이전 Sitecatalyst) 에는 두 개의 Demandbase 컨텍스트 데이터 변수가 포함되어 있습니다.**

![](assets/debugger1.png)

** Target mbox 에는 Demandbase 프로필 매개 변수가 포함되어 있습니다. **

페이지에서 Target 이 구현되고 Adobe Target에 대해 이 통합이 구성된 경우에만 이 문제를 보게 됩니다. Adobe 통합 마법사의 4 단계를 참조하십시오.

![](assets/debugger2.png)

## 보고 {#section-1792fe75dc3249d0ad063dfd87a89162}

Adobe 통합 마법사를 사용하여 자동으로 생성된 대시보드를 사용하여 Adobe Analytics 내에서 Demandbase 보고서를 검토합니다 (7 단계).

또는 Adobe Analytics 메뉴 구조 내에서 Demandbase 보고로 이동할 수 있습니다 (아래 스크린샷 참조).

>[!NOTE]
>
>이 데이터는 성공적으로 배포한 후 24-48 시간 내에 나타납니다.

![](assets/reporting1.png)

![](assets/reporting2.png)

## FAQ {#section-d926b160a2ef4f07b43ea1bc67ac2a0a}

**"[N/A]"는 무엇을 의미합니까?**

Demandbase 데이터 커넥터는 이 기본값을 설정하여 속성이 "사용할 수 없음" 인 경우를 나타냅니다. 기본값이 설정되는 일반적인 시나리오는 두 가지가 있습니다.

* Demandbase는 방문자가 회사에 속하지 않는 IP 주소에서 온다고 감지합니다.
* 계정 감시 속성 («watch_ list» 로 시작하는 것) 이 사용되지만, 회사가 계정 감시 목록에 없습니다.

** 특정 속성에 대해 "[N/A]" 가 더 자주 나타나는 이유는 무엇입니까? **

Demandbase는 모든 IP 주소를 분류하며 방문자가 회사 IP에서 오지 않을 때도 Audience 및 Audience_ Segment 속성을 제공합니다. 고객이 "주거용", "무선" 및 "접대" 와 같은 값을 반환하면 나머지 속성은 사용할 수 없습니다.

때때로 방문자의 대상은 "smb" 이지만 다른 속성은 "[n/a]" 가 표시됩니다. 즉, Demandbase는 방문자를 소규모 기업으로 분류할 수 있지만 전체 회사 프로필을 사용할 수 없습니다. 이는 일반적으로 두 개 이상의 소규모 기업에서 동일한 서비스 제공업체 또는 IP 주소 블록을 사용하고 있는 경우 가장 작은 회사에서 발생합니다.

## 개발자 고려 사항 {#section-d33fff55bc4b4db99f82dee418ef1bc2}

구현에서 기본값을 조정해야 하는 경우, 행을 업데이트하십시오.

```
_db._nonOrgMatchLabel = "[n/a]";
```

