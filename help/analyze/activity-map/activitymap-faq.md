---
description: 'Activity Map 기능의 설정, 구성 및 사용과 관련하여 자주 묻는 질문입니다. '
title: Activity Map FAQ
uuid: e4f6d4e2-55d1-4e32-bf70-a334178af370
feature: Activity Map
role: 비즈니스 전문가, 관리자
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 45%

---


# Activity Map FAQ

Activity Map 기능의 설정, 구성 및 사용과 관련하여 자주 묻는 질문입니다. 

## 모든 Analytics 고객이 관리 도구 ActivityMap 지원 페이지에 액세스할 수 있습니까?

Adobe Analytics Standard, Premium 및 Ultimate에 대한 계약을 보유한 조직은 Activity Map을 이용할 수 있습니다.

## Activity Map은 &quot;보기&quot;에 대한 데이터를 제공합니까?

아니요. Adobe는 열람한 링크를 추적하지 않습니다.

## Activity Map에서 지원하는 브라우저 및 버전은 무엇입니까?

Activity Map은 최신 버전의 브라우저를 지원합니다.

## Activity Map은 서버 호출을 증가시키나요?

Activity Map은 자체 서버 호출을 전송하지 않습니다. 대신 Activity Map 컨텍스트 데이터 변수는 이후 페이지의 Analytics 페이지 보기 호출에 포함됩니다.

## 왜 일부 등급 항목 오버레이가 누락되어 있습니까?**

하위 메뉴 링크와 같은 일부 등급 링크는 페이지에서 숨겨집니다. 따라서 해당 링크 오버레이는 표시되지 않습니다. 등급은 숨겨진 링크를 포함하여 페이지의 모든 링크에 대해 계산됩니다.

## 모든 링크 보고서에서 링크 등급은 어떻게 결정됩니까?**

* **그라디언트 및 버블 모드에서**:등급은 지표 열에 의해 결정됩니다. 동일한 지표 값이 있는 링크의 경우, 등급은 추가적으로 링크 ID 알파벳순을 기반으로 합니다.
* **승자 및 패자 모드에서**:등급은 주로 % 게인 열에 의해 결정됩니다. 동일한 게인이 있는 링크의 경우 등급은 추가적으로 링크 ID 알파벳순을 기반으로 합니다.

## Activity Map은 여러 보고서 세트를 사용하는 페이지에서 어떻게 작동합니까?

기본적으로 Activity Map에서는 페이지가 보내는 첫 번째 태그와 연결된 보고서 세트를 사용합니다. **[!UICONTROL Activity Map 설정]** > **[!UICONTROL 기타]** 탭을 통해 서로 다른 태그가 지정된 보고서 세트를 선택할 수 있습니다.

## Activity Map은 페이지에서 Adobe Analytics을 검색하는 데 얼마나 걸립니까?

Activity Map은 페이지 완료 이벤트 후 최대 20초 동안 Adobe Analytics이 있는지 검색합니다.

## Activity Map은 어떻게 다이내믹 컨텐츠를 처리합니까?

Activity Map은 2초마다 다음과 같은 웹 페이지의 상태에 변경 사항이 있는지 확인합니다.

* 표시된 HTML 컨텐츠
* 숨겨진 HTML 컨텐츠
* 주입된 새 HTML 컨텐츠

컨텐츠가 숨거나 표시되는 경우, 애플리케이션이 영향을 받은 링크 상태를 자동으로 숨김에서 표시로, 또는 표시에서 숨김으로 변경합니다(따라서 오버레이합니다). 새 컨텐츠가 주입되면 애플리케이션은 연관된 링크를 검색하고, 해당 링크에 대한 분석 데이터를 가져오고, 이러한 링크에 대한 오버레이를 추가합니다.

## 페이지 흐름 보고서는 어떤 지표를 기반으로 합니까?

표시된 모든 데이터는 페이지 보기를 기반으로 합니다.

## 데이터 피드를 통해 Activity Map 컨텍스트 데이터 변수를 내보낼 수 있습니까?

Activity Map 컨텍스트 데이터 변수는 데이터 피드에서 사용할 수 없습니다.

## 세그먼트는 라이브 모드에서 작동합니까?

아니요. 세그먼트는 라이브 모드에서 작동하지 않습니다. 이 기능은 세그먼테이션을 지원하지 않는 보고 및 분석의 실시간 보고와 같습니다.

## Activity Map은 가상 보고서 세트와 호환합니까?

예. 하지만, 가상 보고서 세트 제한 사항으로 인해 Activity Map의 라이브 모드는 가상 보고서 세트와 호환하지 않습니다.
