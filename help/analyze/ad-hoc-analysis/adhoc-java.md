---
description: Java 11에서 애드혹 분석을 실행하는 방법에 대한 지침입니다.
seo-description: Java 11에서 애드혹 분석을 실행하는 방법에 대한 지침입니다.
seo-title: 애드혹 분석 및 Java 11
title: Java 11를 사용하여 애드혹 분석 실행
translation-type: tm+mt
source-git-commit: 23bdb0c24416c376ec1df7b609a5794dbf8886f2

---


# Java 11를 사용하여 애드혹 분석 실행

Java 8에서 Ad Hoc Analysis를 실행할 때와 달리 Java 11에서 Ad Hoc Analysis를 실행할 때 추가 단계를 수행해야 합니다.

## 전제 조건

IT 팀과 함께 다음 항목이 제 위치에 있는지 확인하십시오.

* Java 11 must be installed, with *JAVA_HOME* environment variable set
* JavaFX를 설치하고, *PATH_TO_FX_SDK* 환경 변수가 JavaFX SDK 디렉토리를 가리켜야 합니다. 예를 들면 Mac의 경우 *PATH_TO_FX_SDK=/homedir/javafx-sdk-11.0.2*, PC의 경우 *PATH_TO_FX_SDK=C:\Users\username\javafx-sdk-11.0.2*&#x200B;를 가리켜야 합니다.

## Java 11용 Ad Hoc Analysis 설치

1. Go to **[!UICONTROL Analytics &gt; Tools &gt; Ad Hoc Analysis]**.
1. **[!UICONTROL 애드혹 분석 (Java 11)]**&#x200B;를 클릭합니다. zip 파일이 다운로드됩니다.
1. 다운로드한 파일의 압축을 풉니다.
1. **.bat(PC) 또는 .sh(Mac) 파일을 선택**&#x200B;합니다. Adobe Analytics URL에서 "sc" 다음에 오는 숫자를 확인하여 해당 데이터 센터 파일을 선택합니다. (3 = lon, 4 = sin, 5 = PNW) PC를 사용하는 경우'PC 정보'로 이동하여 32 비트 또는 64 비트 Windows 운영 체제를 실행 중인지 확인합니다. 그런 다음 적절한 .bat 파일을 선택합니다.
1. **선택한 파일을 실행**&#x200B;합니다. PC의 경우: .bat 파일을 두 번 클릭합니다. Mac의 경우: .sh 파일을 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL 열기 &gt; 기타...  &gt; 유틸리티 &gt; (모든 애플리케이션 사용) &gt; 터미널 &gt; 열기]**&#x200B;를 선택합니다.
1. Ad Hoc Analysis에 로그인합니다.

>[!NOte]
>
> Federated 및 Enterprise ID 인증 방법은 Java 11 버전의 애드혹 분석과 호환되지 않습니다.

## Ad Hoc Analysis에서 지원되지 않는 기능(Java 11)

애드혹 분석과 호환되는 Java 11 버전에서는 몇 가지 알려진 제한 사항이 있습니다.

* Federated ID 및 Enterprise ID 인증 방법은 지원되지 않습니다.
* Linux 운영 체제는 지원되지 않습니다.
* When using a Mac, do not use the Mac application menu (including *cmd + Q*). 이로 인해 경고 없이 Ad Hoc Analysis이 종료될 수 있습니다. 대신 Ad Hoc Analysis 내의 메뉴를 사용하십시오.
* 이 사이트 분석 시각화는 MacOS에서 Ad Hoc Analysis를 실행할 때 지원되지 않습니다.

## FAQ

**Q: " Unable find\ bin\ javaw "오류 (아래 예) - 어떻게 해야 합니까?**

![](/help/analyze/ad-hoc-analysis/assets/error-java.png)

A: 이 오류가 발생하면 IT 팀과 함께 Java 11에서 Ad Hoc Analysis를 실행하는 데 필요한 *JAVA_HOME* 환경 변수를 설정하십시오.