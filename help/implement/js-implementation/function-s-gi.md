---
description: s_gi() 함수는 보고서 세트 ID로 AppMeasurement 인스턴스를 만들거나 찾는 데 사용됩니다. 내부적으로 AppMeasurement는 생성된 모든 인스턴스를 추적하고 s_gi()는 보고서 세트에 대한 기존 인스턴스가 있으면 이를 반환합니다. 인스턴스가 존재하지 않는 경우 새로운 인스턴스가 생성되어 반환됩니다.
keywords: Analytics 구현
seo-description: s_gi() 함수는 보고서 세트 ID로 AppMeasurement 인스턴스를 만들거나 찾는 데 사용됩니다. 내부적으로 AppMeasurement는 생성된 모든 인스턴스를 추적하고 s_gi()는 보고서 세트에 대한 기존 인스턴스가 있으면 이를 반환합니다. 인스턴스가 존재하지 않는 경우 새로운 인스턴스가 생성되어 반환됩니다.
seo-title: s_gi() 함수
solution: Analytics
title: s_gi() 함수
topic: 개발자 및 구현
uuid: a 77 de 90 e-c 60 e -4946-90 cf-deaf 8 aa 3 d 755
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# s_gi() 함수

s_gi() 함수는 보고서 세트 ID로 AppMeasurement 인스턴스를 만들거나 찾는 데 사용됩니다. 내부적으로 AppMeasurement는 생성된 모든 인스턴스를 추적하고 s_gi()는 보고서 세트에 대한 기존 인스턴스가 있으면 이를 반환합니다. 인스턴스가 존재하지 않는 경우 새로운 인스턴스가 생성되어 반환됩니다.

We recommend calling `s_gi()` before setting variables and making tracking calls throughout your page code. 이는 실수로 s 변수를 덮어쓴 경우 추적 호출을 할 때 올바른 개체가 사용되도록 보장합니다.

## 여러 보고서 세트 사용 {#section_F2F3B76E7AFD4B4B91CDC8BBEB34BBC5}

반환되는 개체는 전달되는 보고서 세트 ID에 따라 달라집니다. 예를 들어 `s_gi()`()에 대해 다음과 같이 초기 호출을 하는 경우:

```
var s=s_gi('rsid1,rsid2')
```

다음 테이블은 후속 호출에서 무엇이 반환되는지 설명합니다.

| ** s_gi 후속 호출** | ** 반환되는 개체 설명** |
|---|---|
| `s=s_gi('rsid1,rsid2')` | 앞서 참조된 것과 같은 개체가 반환됩니다. |
| `s=s_gi('rsid1')` | 앞서 생성된 개체의 원본이 아닌 사본이 반환됩니다. |
| `s=s_gi('rsid1,rsid3')` | 앞서 생성된 개체의 원본이 아닌 사본이 반환됩니다. |
| `s=s_gi('rsid3')` | 구성 변수가 설정되지 않은 새로운 빈 개체(예: linkTrackVars와 linkDownloadFileTypes 모두 비어 있음)가 반환됩니다. |

