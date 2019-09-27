---
description: 타임스탬프가 지정된 데이터와 지정되지 않은 데이터를 모두 하나의 보고서 세트에 결합하십시오.
seo-description: 타임스탬프가 지정된 데이터와 지정되지 않은 데이터를 모두 하나의 보고서 세트에 결합하십시오.
seo-title: 타임스탬프 선택 사항
solution: Analytics
title: 타임스탬프 선택 사항
topic: 관리 도구
uuid: 0fa63658-1cc2-4adc-8d51-a0662d0aa941
translation-type: tm+mt
source-git-commit: 0dbc8ac9b416ce50f197a884bb71c6cd389cd0bb

---


# 타임스탬프 선택 사항

타임스탬프가 지정된 데이터와 지정되지 않은 데이터를 모두 하나의 보고서 세트에 결합하십시오.

타임스탬프 옵션을 사용하면

* 타임스탬프가 지정된 데이터와 지정되지 않은 데이터를 동일한 전역 보고서 세트에서 혼합할 수 있습니다.
* 타임스탬프가 지정된 데이터를 모바일 앱에서 전역 보고서 세트로 보낼 수 있습니다.
* 새 보고서 세트를 만들지 않고도 오프라인 추적을 사용하도록 앱을 업그레이드할 수 있습니다.

보고서 세트에서 타임스탬프를 사용할 때 우수 사례가 필요하면 [타임스탬프 옵션 사용](/help/implement/js-implementation/timestamps-overview.md)을 참조하십시오.

>[!IMPORTANT]
>
>If you are using Timestamps Optional, then do not set [s.visitorID](https://marketing.adobe.com/resources/help/en_US/sc/implement/visid_custom.html) on data that is already timestamped. 설정하는 경우 데이터 순서가 잘못되고 시간 계산(체류 시간 값 등), 속성(eVar 지속성), 방문 번호/방문 카운트 및 경로 지정 보고서에 부정적인 영향을 줄 수 있습니다.

>[!NOTE]
>
>타임스탬프 사용 세션 데이터는 최대 92일 동안 유지됩니다. 즉, 방문/세션이 92일 동안 "열려 있음"으로 표시되고, 이전 히트(히트 시간) 이후 30분이 아닌 추가 히트는 여전히 동일한 방문/세션에 포함될 수 있습니다. Any "old" hits that are received out of order will produce "unknown" results, since a number of factors (segmentation, allocation, expiration, etc.) influence whether these hits will be included in reporting or not.

## 새 보고서 세트 {#section_095A7CFBD280494593B9BEC1592B73A6}

* 템플릿에서 만들 경우 새 보고서 세트의 기본값이 타임스탬프 옵션으로 지정됩니다.

   (**관리 &gt; 보고서 세트 &gt; 새로 만들기 &gt; 보고서 세트**&#x200B;에서 템플릿으로 새 보고서 세트를 만들 수 있습니다.)
* 기존 보고서 세트에서 복사하면, 새 보고서 세트가 다음 항목을 포함한 원래 보고서 세트의 타임스탬프 설정을 상속합니다.

   * **타임스탬프가 허용되지 않음**(s.visitorID 설정이 지원됨)
   * **타임스탬프 필수**(s.visitorID 설정이 지원되지 않음)
   * **타임스탬프 옵션**(s.visitorID 설정이 지원되지만 타임스탬프가 지정된 조회수는 지원되지 않음)

## 기존 보고서 세트를 타임스탬프 옵션으로 변경하려면 {#section_40BCD3B4639241DEA716F7640ED33E72}

1. **관리 &gt; 보고서 세트 &gt; 설정 편집 &gt; 일반 &gt; 타임스탬프 구성**&#x200B;으로 이동합니다.
1. **선택한 보고서 세트를 타임스탬프 옵션으로 변환** 상태를 선택합니다.

   이렇게 하면 보고서 세트가 타임스탬프 옵션으로 변경됩니다.

>[!NOTE]
>
>If a report suite was set to **Timestamps Optional**, to change this to any other setting, please contact Adobe Client Care.

