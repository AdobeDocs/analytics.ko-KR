---
title: 모바일 조회 차원
description: 디바이스의 IP 주소 및 사용자 에이전트를 기반으로 하는 차원입니다.
feature: Dimensions
exl-id: fa460888-513d-4d14-93b1-33d308e0758a
TQID: https://experienceleague.adobe.com/X80x0MIx5gd16J20VU37fNSExDO2NSXPrHR8EKqsMqw
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: c77ba355-6681-41fe-b719-563d3f507fdb
  - id: d2311670-43bd-4c2e-bc98-1da2aaba9cef
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 961
ht-degree: 98%

---

# 모바일 조회 차원

*이 페이지는 웹 사이트에 액세스하는 모바일 디바이스의 속성을 참조합니다. 모바일 앱 내 추적은 [모바일 라이프사이클 차원](lifecycle-dimensions.md) 또는 [모바일 라이프사이클 지표](../metrics/lifecycle-metrics.md)를 참조하십시오.*

모바일 조회 [차원](overview.md)은 사이트를 방문하는 모바일 디바이스의 속성에 대한 인사이트를 제공합니다. 이러한 속성은 사용자 에이전트 및 히트의 IP 주소를 기반으로 합니다. 이 차원을 사용하여 모바일 디바이스가 지원하는 기능을 이해할 수 있습니다.

## 데이터로 이 차원 채우기

이 차원은 Adobe 내부 조회 규칙을 참조합니다.

* [!UICONTROL 이동통신사] 차원의 경우 Adobe는 NetAcuity를 사용하는 [Digital Element](https://www.digitalelement.com/)와 협력하여 IP 주소와 이동통신사 간의 조회를 유지 관리합니다.
* 다른 모든 모바일 차원의 경우 Adobe는 [DeviceAtlas](https://deviceatlas.com/)와 협력하여 사용자 에이전트와 각 모바일 차원 간의 조회를 유지 관리합니다.

이러한 차원의 가용성은 구현 유형에 따라 다릅니다.

* AppMeasurement 구현의 경우 이러한 차원은 즉시 작동합니다.
* Web SDK 구현의 경우 [&#x200B; 데이터스트림을 구성](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=ko)할 때 [!UICONTROL 지역 조회] (이동통신사) 또는 [!UICONTROL 디바이스 조회] (다른 모든 차원)를 활성화하십시오.

## 모바일 차원 설명

>[!NOTE]
>
>레이블이 `"None"`이라고 지정된 차원 항목은 모바일이 아닌 디바이스입니다. 모바일 디바이스만 포함하는 보고서가 필요하면 &#39;모바일 디바이스&#39; 차원을 Workspace 캔버스의 세그먼트 영역으로 드래그하십시오.

* **[!UICONTROL 모바일 오디오 지원]**: 디바이스가 재생할 수 있는 파일 형식을 결정합니다. 값의 예로는 `"MP3"`, `"AAC"` 및 `"MIDI Monophonic"`이 있습니다. 이 차원의 값은 함께 사용할 수 있습니다. 단일 히트가 여러 차원 항목에 기여할 수 있습니다.
* **[!UICONTROL 이동통신사]**: 디바이스의 전화 또는 데이터 제공업체입니다. 값의 예로는 `"Reliance Jio"`, `"Airtel"`, `"Vodafone"` 및 `"Verizon"`이 있습니다.
* **[!UICONTROL 모바일 색상 깊이]**: 모바일 디바이스의 비트 단위 색상 깊이입니다.
* **[!UICONTROL 모바일 쿠키 지원]**: 모바일 디바이스가 쿠키를 지원하는지 여부를 결정합니다. 이 차원은 브라우저가 쿠키를 수락하는지 여부는 기술하지 않습니다. 차원 항목은 `"Supported"`, `"Not supported"` 및 `"Unknown"`을 포함합니다.
* **[!UICONTROL 모바일 디바이스]**: 방문자가 사용하는 모바일 디바이스입니다.
* **[!UICONTROL 모바일 디바이스 번호]**: 모바일 디바이스가 해당 번호를 전송하는지 여부를 결정합니다. 이 차원은 휴대폰 번호 자체는 제공하지 않습니다. 차원 항목은 `"Supported"`, `"Not supported"` 및 `"Unknown"`을 포함합니다.
* **[!UICONTROL 모바일 디바이스 유형]**: 모바일 디바이스의 유형입니다. 값의 예로는 `"Mobile phone"`, `"Tablet"`, `"Media player"` 및 `"Gaming console"`이 있습니다.
* **[!UICONTROL 모바일 DRM]**: 모바일 디바이스가 지원하는 DRM 유형입니다. 값의 예로는 `"DRM OMA forward"`, `"DRM OMA combined delivery"` 및 `"DRM OMA separate delivery"`이 있습니다.
* **[!UICONTROL 모바일 이미지 지원]**: 모바일 디바이스에서 지원하는 이미지 유형입니다. 값의 예로는 `"PNG"`, `"JPEG"` 및 `"GIF 87"`이 있습니다. 이 차원의 값은 함께 사용할 수 있습니다. 단일 히트가 여러 차원 항목에 기여할 수 있습니다.
* **[!UICONTROL 모바일 정보 서비스]**: 디바이스에서 지원하는 뉴스 서비스 유형입니다. 최신 디바이스는 일반적으로 이 정보를 보고하지 않습니다.
* **[!UICONTROL 모바일 Java VM]**: 디바이스가 지원하는 Java 버전입니다.
* **[!UICONTROL 모바일 메일 장식]**: 디바이스가 한때 일본 디바이스에서 널리 사용되었던 기능인 [Decome](https://en.wikipedia.org/wiki/Decome)를 지원하는지 여부를 판단합니다.
* **[!UICONTROL 모바일 제조업체]**: 제조업체별로 모바일 디바이스를 분류합니다. 값의 예로는 `"Apple"`, `"Samsung"`, `"Huawei"` 및 `"Motorola"`가 있습니다.
* **[!UICONTROL 모바일 최대 책갈피 길이]**: 모바일 디바이스가 책갈피가 지정된 URL에서 지원하는 최대 바이트 수입니다. 최신 디바이스에는 일반적으로 제한이 없습니다.
* **[!UICONTROL 모바일 최대 브라우저 URL 길이]**: 모바일 디바이스가 URL에서 지원하는 최대 바이트 수입니다. 최신 디바이스에는 일반적으로 제한이 없습니다.
* **[!UICONTROL 모바일 최대 이메일 길이]**: 모바일 디바이스가 이메일에서 지원하는 최대 바이트 수입니다. 최신 디바이스에는 일반적으로 제한이 없습니다.
* **[!UICONTROL 모바일 네트 프로토콜]**: 인터넷에 액세스할 때 디바이스가 지원하는 프로토콜 유형입니다. 값의 예로는 `"EDGE"`, `"GPRS"`, `"UMTS"` 및 `"LTE"`가 있습니다.
* **[!UICONTROL 모바일 운영 체제(사용 중지)]**: 대신 [운영 체제](operating-systems.md) 차원을 사용하십시오.
* **[!UICONTROL 모바일 대화 푸시]**: 모바일 디바이스가 양방향 라디오와 유사하게 작동할 수 있도록 해 주는 PTT(Push to Talk)를 디바이스가 지원하는지 여부를 결정합니다. 최신 디바이스는 일반적으로 이 기능을 보고하지 않습니다.
* **[!UICONTROL 모바일 화면 높이]**: 화면의 픽셀 단위 높이입니다. iPhone은 iPhone 디바이스 버전을 확인할 수 없어서 항상 `"480"`을 보고합니다. iPhone 디바이스 버전 확인에 대해서는 아래 섹션을 참조하십시오.
* **[!UICONTROL 모바일 화면 크기]**: 모바일 디바이스의 픽셀 단위 전체 크기입니다. 보고된 화면 크기는 디바이스의 방향을 의미하지 않습니다. 화면 방향과 상관없이 각 디바이스는 보고서에서 화면 해상도를 고정했습니다. 이 크기는 어떤 방향성이 더 가능성이 높은지를 결정하는 연구를 기반으로 한다. 각각의 크기가 하나 이상의 각기 다른 디바이스를 나타내는 동일한 보고서에서 `"768x1024"` 및 `"1024x768"`과 같은 크기를 볼 수 있습니다.
* **[!UICONTROL 모바일 화면 너비]**: 화면의 픽셀 단위 너비입니다.
* **[!UICONTROL 모바일 비디오 지원]**: 모바일 디바이스가 지원하는 비디오 파일 형식 및 코덱입니다. MP4 및 3GPP 파일의 다양한 코덱에 대해 여러 차원 항목이 존재합니다. 이 차원의 값은 함께 사용할 수 있습니다. 단일 히트가 여러 차원 항목에 기여할 수 있습니다.

## 모델 또는 버전으로 iPhone 구분

모바일 디바이스는 디바이스 버전이 아니라 사용자 에이전트 문자열에 있는 펌웨어 버전을 보고합니다. 예를 들어 현재 세대 iPhone에는 동일한 펌웨어 버전을 사용하는 경우 지난 세대 iPhone과 동일한 사용자 에이전트가 포함됩니다. JavaScript를 사용하여 iPhone의 디바이스 버전을 확인할 방법이 없으므로 모든 iPhone은 동일한 버킷에 속합니다. 모바일 차원은 절대적으로 사용자 에이전트를 참조하는 조회에 기반하므로 모든 iPhone에서는 모바일 화면 크기를 `320 x 480`으로 표시합니다.

iPhone 디바이스 버전을 수집하려는 경우 이 제한을 피할 수 있는 두 가지 방법이 있습니다.

* **Mobile SDK 사용**: Mobile SDK에는 보고 시 사용할 디바이스 버전을 표시하는 차원이 포함되어 있습니다. 이 방법은 웹 사이트보다 모바일 앱에 더 적합합니다.
* **JavaScript를 통해 사용할 수 있는 다른 변수 사용**: `screen.height` 및 `screen.width`와 같은 일부 변수를 사용하여 디바이스 버전을 유추할 수 있습니다. 예를 들어 사이트에서 다음 코드 조각을 사용할 수 있습니다.

  ```js
  if (navigator.userAgent.indexOf('iPhone') > -1) {
    s.eVarXX = screen.width + "x" + screen.height;
    }
  ```

  이 코드 블록은 먼저 디바이스가 iPhone인지 감지합니다. iPhone인 경우 코드는 JavaScript를 사용하여 화면 해상도를 eVar에 가져옵니다. 이 방법을 사용하면 화면 해상도가 고유한 경우 디바이스 버전을 대략 감지할 수 있습니다.
