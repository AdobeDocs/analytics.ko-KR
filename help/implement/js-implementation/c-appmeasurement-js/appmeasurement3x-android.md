---
description: ios용 AppMeasurement 3.x
seo-description: ios용 AppMeasurement 3.x에 대한 기존 설명서
seo-title: ios용 AppMeasurement 3.x
solution: Analytics
subtopic: 책갈피
title: ios용 AppMeasurement 3.x
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 4907b2930d894525b93b02f743c095f824a61a3b

---


# iOS용 AppMeasurement 3.x

*참고:이 문서에는 이전 버전의 AppMeasurement, 특히 iOS용 버전 3.x에 대한 이전 정보가 포함되어 있습니다.
현재 AppMeasurement 구현에 대한 자세한 내용은 JavaScript[용 AppMeasurement 정보를 참조하십시오](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html).*

*iOS용 AppMeasurement 3.x 최종 업데이트*

Adobe AppMeasurement for iOS를 사용하면 Adobe Experience Cloud에서 기본 Apple iPhone 및 iPad 애플리케이션을 측정할 수 있습니다.

이 안내서는 두 섹션으로 나누어져 있습니다.한 섹션은 Adobe Analytics 경험이 있는 분석가를 위한 것이고 한 섹션은 모바일 앱 개발 경험이 있는 iOS 개발자를 위한 것입니다.

**지원되는 버전**:iOS 4.3 이상.

**모든 AppMeasurement**&#x200B;모바일 플랫폼에 대한 라이브러리 다운로드 지침 및 링크는 Developer Connection의 Measurement and OptimizingMobile Applications 페이지에서 다운로드할 수 있습니다. 무료 Developer Connection 계정 또는 보고 및 분석 로그인 계정이 있어야 라이브러리를 다운로드할 수 있습니다. 다운로드 링크는 로그인할 때까지 표시되지 않습니다.

## 분석 빠른 시작

이 섹션에서는 iOS 라이브러리를 구현하고 표준 구현에 필요한 코드를 추가하는 과정을 안내합니다. 사용자 지정 이벤트와 기타 데이터를 전송하는 방법을 보여주는 단계가 포함됩니다.

분석가로서 보고서 세트에 대해 모바일 애플리케이션 보고서를 활성화해야 합니다. 캡처할 추가 지표가 있는 경우 애플리케이션에서 전송해야 하는 컨텍스트 데이터 변수의 설명을 개발자에게 제공해야 합니다. 예를 들어, 로그인 후 사용자 이름을 수집하려면 개발자가 `myco.username`이라는 컨텍스트 데이터 변수에 사용자 이름을 설정하도록 할 수 있습니다.

### Analytics에서 모바일 애플리케이션 보고서 활성화

Analytics는 모바일 앱 라이프사이클 추적을 활성화할 수 있는 인터페이스를 제공합니다. 이 매핑을 통해 Analytics는 모바일 애플리케이션 보고서를 자동으로 생성합니다.

1. 관리 콘솔 &gt; 보고서 세트 &gt; 설정 편집 &gt; 모바일 관리 &gt; 모바일 애플리케이션 보고를 엽니다.
1. 모바일 앱 라이프사이클 추적 활성화를 클릭합니다.

이제 라이프사이클 지표가 캡처되고 SiteCatalyst의 보고서 메뉴에 모바일 애플리케이션 보고서가 표시됩니다.

### 처리 규칙을 사용하여 추가 지표 캡처

구현에서 컨텍스트 데이터를 사용하여 추가 이벤트와 치수를 전송하는 경우 해당 데이터를 캡처하도록 처리 규칙을 구성해야 합니다.

처리 규칙을 생성하려면 먼저 조직의 사용자가 인증을 받아야 합니다. 자세한 내용은 처리 규칙 도움말을 참조하십시오.

처리 규칙을 활성화한 후 컨텍스트 데이터 변수 복사 예제는 컨텍스트 데이터를 매핑하는 데 필요한 프로세스를 보여줍니다.

### (옵션) 오프라인 추적 활성화

장치가 오프라인일 때 히트를 저장하려면 보고서 세트에 타임스탬프를 사용해야 합니다.

오프라인 추적을 활성화한 후에는 모든 히트에 타임스탬프를 적용해야 하며 그렇지 않은 경우 히트가 수집되지 않습니다. 현재 JavaScript의 데이터도 수집하는 보고서 세트에 AppMeasurement 데이터를 보고하는 경우, 모바일 데이터에 별도의 보고서 세트를 설정하여 데이터 손실을 방지하거나 s.timestamp 변수를 사용하여 JavaScript 히트에 사용자 지정 타임스탬프를 포함해야 할 수도 있습니다.

보고서 세트에 타임스탬프를 사용할 수 있는지 여부를 잘 모를 경우 고객 지원 센터에 문의하십시오.

## 개발자 빠른 시작

이 섹션에서는 iOS 라이브러리를 구현하고 다음을 포함한 측정 데이터 전송을 시작하는 단계를 안내합니다.

* 라이브러리 가져오기
* 프로젝트에 라이브러리 추가
* TrackingHelper의 빠른 워드
* 구현


### 라이브러리 가져오기

Developer Connection의 모바일 애플리케이션 측정 및 최적화를 방문하여 Android 라이브러리를 다운로드합니다. 다운로드 파일의 압축을 풀면 다음 소프트웨어 구성 요소를 갖게 됩니다.

* admsAppLibrary.jar: Android 장치 및 시뮬레이터와 함께 사용하도록 고안된 라이브러리입니다. Android 2.0 이상이 필요합니다.
* Examples\TrackingHelper.java: 추적 코드를 애플리케이션 로직과 구분하도록 고안된 선택적 클래스입니다.

### 프로젝트에 라이브러리 추가

1. Eclipse IDE에서 프로젝트 이름을 마우스 오른쪽 버튼으로 클릭합니다.
1. 작성 경로 &gt; 외부 아카이브 추가를 선택합니다.
1. 선택 `admsAppLibrary.jar`.
1. 열기를 클릭합니다.
1. 다시 프로젝트를 마우스 오른쪽 버튼으로 클릭한 다음 작성 경로 &gt; 작성 경로 구성을 선택합니다.
1. 주문 및 내보내기 탭을 클릭합니다.
1. Ensure that `admsAppLibrary.jar` is selected.

애플리케이션에서 import com.adobe.ADMS를 사용하여 admsAppLibrary.jar 라이브러리에서 클래스/인터페이스를 가져올 수 있습니다.*;

### 앱 권한 추가

AppMeasurement 라이브러리를 사용하려면 데이터를 전송하고 오프라인 추적 호출을 기록할 다음 권한이 필요합니다.

* INTERNET
* ACCESS_NETWORK_STATE

To add these permissions, add the following lines to your AndroidManifest.xml file (in the application project directory):
`<uses-permission android:name="android.permission.INTERNET" />`
`<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />`

### TrackingHelper의 빠른 워드

SDK에는 TrackingHelper라는 추가, 옵션 클래스가 포함되어 있습니다. TrackingHelper는 애플리케이션 논리와 측정 코드를 구분하는 방법을 제공합니다.

다음 예제를 고려하십시오. 애플리케이션에서 각 로그인을 추적하는 이벤트를 전송하려고 합니다. 로그인 코드 바로 뒤에 다음 코드를 추가하여 이 이벤트를 전송할 수 있습니다. 코드 세부 정보에 대해 염려하지 마십시오. 나중에 설명할 것입니다.

```
Hashtable<String, Object> contextData = new Hashtable<String, Object>();
contextData.put("username", "username_value");
measure.trackEvents("event1", contextData);
```

이 직접 방식은 양호하지만 애플리케이션을 개발하는 동안 방해하지 않도록 어딘가에 이 코드를 삽입하지 않겠습니까? TrackingHelper가 바로 그 "어딘가"입니다. TrackingHelper 내에서 trackLogonEvent라고 하는 메서드에 이 코드를 배치할 수 있습니다.

```
public static void trackLogonEvent (String username_value) {
Hashtable<String, Object> contextData = new Hashtable<String, Object>();
contextData.put("username", username_value);
measure.trackEvents("event1", contextData);
}
```

이제, 애플리케이션 코드에서 trackLogonEvent에 대한 간단한 호출을 사용하여 로그온 이벤트를 추적할 수 있습니다.

TrackingHelper.trackLogonEvent("사용자 이름");

애플리케이션 코드에서 측정 호출은 한 줄입니다. 또한 기본 측정 논리를 변경해야 하는 경우 TrackingHelper만 업데이트해야 합니다. 다른 개발자가 코드를 추가하는 경우 AppMeasurement 라이브러리에서 충돌 과정 없이 정의한 간단한 메서드를 사용할 수 있습니다.

설정에 추가로 1~2분이 필요하더라도 새로운 구현에 대해 TrackingHelper를 사용하는 것이 좋을 것입니다. 이 안내서의 나머지 단계는 TrackingHelper를 설정하고 측정 데이터 전송을 시작하는 과정을 안내합니다.

앱용 클래스 파일이 들어 있는 디렉토리로 TrackingHelper.java를 복사하고 이 파일 위쪽의 패키지 이름을 패키지 구조(com.company.application)와 일치하도록 바꿉니다 TrackingHelper를 사용하지 않고 구현하려면 TrackingHelper에서 애플리케이션에 복사할 수 있는 몇 가지 샘플을 찾을 수 있습니다.

### 구현

1. TrackingHelper.java를 열고 보고서 세트 ID와 추적 서버로 TRACKING_RSID 및 TRACKING_SERVER를 업데이트합니다. 예:

   ```
   private static final String TRACKING_RSID = "rsid";
   private static final String TRACKING_SERVER = "server";
   ```

   이러한 값은 필수이며 수정해야 합니다. 그렇지 않으면 측정이 작동하지 않습니다. 이러한 값에 대해 잘 모르겠으면 SiteCatalyst 전문가에게 문의하십시오.

2. configureAppMeasurement 메서드를 찾습니다. 이곳에서 SSL을 활성화하고 오프라인 추적을 활성화하고 구성을 전역 변경합니다. 여기에서 예상대로 작동할 때까지 줄에서 주석을 해제하여 debugLogging을 활성화합니다.

3. 애플리케이션의 루트 활동에서 configureAppMeasurement에 호출을 추가합니다.

```
@Override
public void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.main);
TrackingHelper.configureAppMeasurement(this);
}
```

이것이 사용자 지정 지표 추적을 시작하는 데 필요한 모든 코드입니다. 그러나 몇 개의 코드 줄을 추가하면 시작, 업그레이드, 충돌 및 일별/월별 사용자 수를 포함하여 라이프사이클 지표를 자동으로 전송하도록 라이프사이클 추적을 활성화할 수 있습니다.

AppMeasurement 라이브러리가 무거운 리프트를 모두 수행하므로 사용자는 애플리케이션의 각 Activity 클래스에 두 가지 메서드 호출을 추가하기만 하면 됩니다.

### (권장) 라이프사이클 이벤트 추적

라이프사이클 추적이 활성화되면 앱을 시작할 때마다 설치, 업그레이드, 참여일 수 및 기타 라이프사이클 지표를 추적하기 위해 단일 히트가 전송됩니다.

라이프사이클 이벤트 추적을 시작하려면 앱에서 다음 예제와 나와 있는 것처럼 애플리케이션 내부의 각 활동에서 onResume() 및 onPause() 메서드에 대한 호출을 추가합니다. 또한 글로벌 애플리케이션 컨텍스트 대신 컨텍스트 개체로 활동 또는 서비스를 전달하는 것이 좋습니다.

```
@Override
protected void onResume() {
super.onResume();
TrackingHelper.startActivity(this);
}
@Override
protected void onPause() {
super.onPause();
TrackingHelper.stopActivity();
}
```

그러면 됩니다! 이제 Android 앱에서 기본 라이프사이클 추적을 구현했습니다. 보고하는 AppMeasurement 지표를 처리하도록 웹 분석가가 SiteCatalyst를 구성한 후에 SiteCatalyst 보고서 세트는 기본 라이프사이클 지표를 포함합니다.

이곳에서 이동할 위치:

* (옵션) 사용자 지정 이벤트 추적. 사용자 지정 메서드를 TrackingHelper에 추가하여 애플리케이션에서 측정하려는 모든 이벤트를 추적합니다. 로그온, 인앱 구매 등을 추적하는 메서드를 추가할 수 있습니다.
* (옵션) 앱 상태 추적. 애플리케이션 상태는 페이지 뷰와 유사합니다. 이 섹션은 사용자 지정 메서드를 TrackingHelper에 추가하여 앱 상태를 추적하는 방법을 보여줍니다.
* 비디오 측정 빠른 시작. 코드를 추가하여 비디오 뷰, 총 재생 시간 및 가장 인기 있는 비디오를 포함한 비디오 지표를 추적합니다.

### (옵션) 사용자 지정 이벤트 추적

사용자 지정 이벤트는 애플리케이션에 고유한 성공 지표입니다. 사용자가 로그인하거나 앱 구매를 시작하거나 Facebook 페이지에서 링크를 클릭하면 사용자 지정 이벤트를 전송할 수 있습니다. 추적 헬퍼 클래스에는 사용자 지정 이벤트를 추적하는 방법을 보여주는 예제가 포함되어 있습니다. 이 메서드를 템플릿으로 사용하여 추가 이벤트 추적 메서드를 추가할 수 있습니다.

TrackingHelper.java에서 사용자 지정 이벤트 추적 메서드를 정의합니다.

```
public static void trackCustomEvents () {
Hashtable<String, Object> contextData = new Hashtable<String, Object>();
contextData.put("contextKey", "value");
measure.trackEvents("event1, event2", contextData);
}
```

코드 전체에서 이 메서드를 호출하여 사용자 지정 이벤트를 추적할 수 있습니다.

`TrackingHelper.trackCustomEvents();`

이 프로세스를 사용하여 이벤트 추적 메서드를 필요한 만큼 추가합니다. A Quick Word on the TrackingHelper에는 예시 메서드가 포함되어 있으므로 로그인 이벤트를 추적할 수 있습니다.

### (옵션) 앱 상태 추적

추적 헬퍼 클래스에는 애플리케이션 상태를 추적하는 방법을 보여주는 예제도 포함되어 있습니다. 사용자 지정 상태를 추적하는 것은 이벤트 추적과 매우 유사하며 유일한 차이점은 trackEvents 대신 trackAppState 메서드를 사용하는 것입니다.

```
measure.trackAppState("name", contextData);
```

보고 관점에서 볼 때 trackAppState에서는 페이지 뷰가 증가되지만 trackEvents에서는 그렇지 않습니다.

## 비디오 측정 빠른 시작

비디오 측정은 SiteCatalyst에서 비디오 측정 안내서에서 설명합니다. 비디오를 측정하는 일반 프로세스는 모든 AppMeasurement 플랫폼에서 매우 유사합니다. 이 빠른 시작 섹션은 코드 샘플과 함께 개발자 작업의 기본 개요를 제공합니다.

애플리케이션 및 비디오 추적에는 같은 라이브러리인 admsAppLibrary.jar가 사용됩니다. 설명서는 플랫폼에서 일관성을 위해 미디어 모듈로 이러한 메서드를 참조합니다.

미디어 모듈을 사용하기 전에 측정 인스턴스를 구성해야 합니다.

Android에서 비디오 추적을 구현하려면 다음 작업을 완료하십시오.

* 플레이어 이벤트를 SiteCatalyst 변수에 매핑
* 마일스톤, 세그먼트 및 호출 주기 구성
* 플레이어 이벤트 추적

### 플레이어 이벤트를 SiteCatalyst 변수에 매핑

비디오 측정을 구성하려면 비디오 추적을 위해 선택한 SiteCatalyst 이벤트와 eVar을 컨텍스트 데이터 변수에 매핑해야 합니다. 자세한 내용은 SiteCatalyst 비디오 구성을 참조하십시오.

웹 분석가는 비디오 데이터를 수신하도록 구성된 SiteCatalyst 변수의 목록이 포함된 비디오 구현 워크시트를 제공해야 합니다.

* 비디오 이름(eVar): eVar2
* 비디오 이름(Prop): prop2
* 세그먼트(eVar): eVar3
* 컨텐트 유형(eVar): eVar1
* 비디오 시간(이벤트): event3
* 비디오 뷰(이벤트): event1
* 비디오 완료(이벤트): event7
* 비디오 세그먼트 뷰(이벤트): event2

1. 구현에 코드를 추가한 이후에 다음 코드를 추가하면 선택한 SiteCatalyst 변수를 다음 코드의 예시로 교체할 수 있습니다.

   ```
   ADMS_MediaMeasurement mediaMeasure = ADMS_MediaMeasurement.sharedInstance();
   Hashtable<String, Object> contextDataMapping = new Hashtable<String, Object>();
   contextDataMapping.put("a.media.name", "eVar2,prop2");
   contextDataMapping.put("a.media.segment", "eVar3");
   contextDataMapping.put("a.contentType", "eVar1"); //note that this is not in the .media
   namespace
   contextDataMapping.put("a.media.timePlayed", "event3");
   contextDataMapping.put("a.media.view", "event1");
   contextDataMapping.put("a.media.segmentView", "event2");
   contextDataMapping.put("a.media.complete", "event7");
   mediaMeasure.ContextDataMapping = contextDataMapping;
   ```

2. 마일스톤, 세그먼트 및 호출 주기 구성.

3. 플레이어 이벤트 추적.


### 마일스톤, 세그먼트 및 호출 주기 구성

마일스톤을 사용하면 비디오의 특정 포인트에 도달할 때 이벤트를 전송할 수 있습니다. 세그먼트를 사용하면 세부적인 추적을 위해 섹션으로 나눌 수 있습니다. 호출 추기를 사용하면 특정 간격으로 본 시간을 사용하여 측정 호출을 전송할 수 있습니다. 자세한 내용은 비디오 지표를 참조하십시오.

### 마일스톤 매핑

전체 길이의 백분율 또는 경과된 시간(초)을 기반으로 하여 마일스톤을 정의할 수 있습니다. 이 예제는 마일스톤을 전체 길이의 백분율로 정의합니다. 2분 비디오의 경우 다음 코드는 30초, 60초 및 90초에 마일스톤 이벤트를 전송합니다.

```
Hashtable<String, Object> milestoneMapping = new Hashtable<String, Object>();
milestoneMapping.put("25", "event4");
milestoneMapping.put("50", "event5");
milestoneMapping.put("75", "event6");
contextDataMapping.put("a.media.milestones", milestoneMapping);
```


### 오프셋 마일스톤 매핑

이 예는 비디오 첫 부분에서 경과된 시간(초)에 따라 마일스톤을 정의합니다. 2분 비디오의 경우 다음 코드는 전체 비디오 길이에 관계 없이 20초, 40초 및 60초에 마일스톤 이벤트를 전송합니다.

```
Hashtable<String, Object> offsetMilestoneMapping = new Hashtable<String, Object>();
offsetMilestoneMapping.put("20", "event8");
offsetMilestoneMapping.put("40", "event9");
offsetMilestoneMapping.put("60", "event10");

contextDataMapping.put("a.media.offsetMilestones", offsetMilestoneMapping);
```

### 예

```
//get sharedInstance
ADMS_MediaMeasurement mediaMeasure = ADMS_MediaMeasurement.sharedInstance();

//Track By Milestones:
mediaMeasure.trackMilestones = "25,50,75";

// track Milestones & segmentByMilestones:
mediaMeasure.trackMilestones = "25,50,75";
mediaMeasure.segmentByMilestones = true;

// track by seconds:
mediaMeasure.trackSeconds = 15;

// track Milestones & segmentByMilestones & seconds:
mediaMeasure.trackMilestones = "25,50,75";
mediaMeasure.segmentByMilestones = true;
mediaMeasure.trackSeconds = 15;

// track offsetMilestones & segmentByOffsetMilestones:
mediaMeasure.trackOffsetMilestones = "15,30,45,60,75,90";
mediaMeasure.segmentByOffsetMilestones = true;

// track offsetMilestones:
mediaMeasure.trackOffsetMilestones = "5,15,45";
```

### 플레이어 이벤트 추적

비디오를 측정하려면 플레이어에서 이벤트가 발생할 때 미디어 모듈을 알리는 코드를 추가해야 합니다(open, play, stop 및 close 메서드 사용). 사용자가 비디오를 재생하면 미디어 모듈은 본 시간(초) 계산을 시작하도록 play 메서드를 호출해야 합니다.

사용자가 비디오를 일시 중지하면 카운트가 일시 중지되도록 stop을 호출해야 합니다. 이는 일반적으로 플레이어에서 노출하는 이벤트 핸들러를 사용하여 수행됩니다.

예:

로드: open 및 play를 호출합니다.

일시 중지: stop을 호출합니다. 예를 들어 사용자가 15초 후에 비디오를 일시 중지하는 경우에는 stop("Video1",15)를 호출합니다.

버퍼: 비디오를 버퍼링하는 동안 stop을 호출합니다. 재생을 다시 시작할 때 play를 호출합니다.

재시작: play를 호출합니다. 예를 들어 사용자가 처음에 비디오를 15초 동안 재생한 후 비디오를 재시작하는 경우에는 s.play("Video1",15)를 호출합니다.

스크러빙(슬라이더): 사용자가 비디오 슬라이더를 끌면 stop을 호출합니다. 사용자가 비디오 슬라이더를 놓으면 play를 호출합니다.

종료: stop을 호출한 다음 close를 호출합니다. 예를 들어 100초 길이의 비디오가 끝나면 stop("Video1",100)과 close("Video1")을 차례로 호출합니다.

이러한 경우 미디어 플레이어의 이벤트 핸들러에서 호출할 수 있는 네 개 사용자 지정 함수를 정의할 수 있습니다. open, play, stop 및 close에 전달되는 다양한 매개 변수가 플레이어에서 옵니다. 다음 의사 코드 예제는 이 방법을 보여줍니다.

```
function startMovie(){
mediaMeasure.open(mediaName,mediaLength,mediaPlayerName);
playMovie();
}
/*Call on video resume from pause and slider release*/
function playMovie(){
mediaMeasure.play(mediaName,mediaOffset);
}
/*Call on video pause and slider grab*/
function stopMovie(){
mediaMeasure.stop(mediaName,mediaOffset);
}
/*Call on video end*/
function endMovie(){
stopMovie();
mediaMeasure.close(mediaName);
Video Measurement Quick Start 12
```

## 라이프사이클 지표

다음 워크시트는 자동 라이프사이클 추적을 활성화했을 때 측정되는 지표 및 차원을 나열합니다.

### 라이프사이클 지표 및 차원

구성된 경우 라이프사이클 지표가 컨텍스트 데이터 매개 변수로 Analytics에 전송되고, 매개 변수가 각 mbox 호출로 타겟에 전송되며, 대상 관리에 신호로 전송됩니다. 분석 및 타겟은 같은 형식을 사용하지만, 대상 관리는 각 지표에 다른 접두사를 사용합니다.

Analytics에서 각 라이프사이클 추적 호출과 함께 전송된 컨텍스트 데이터는 설명 열에 언급된 것을 제외하고, 첫 번째 열에 나열된 지표 또는 차원을 사용하여 자동으로 캡처되고 보고됩니다.

| 지표 | Analytics 컨텍스트 | Analytics Context Audience Manager 신호 설명 | 데이터/타겟 매개 변수 |
|--- |--- |--- |--- |
| 첫 번째 실행 | a.InstallEvent | c_a_InstallEvent | 설치(또는 재설치) 후 처음 실행할 때 트리거됩니다. |
| 업그레이드 | a.UpgradeEvent | c_a_UpgradeEvent | 업그레이드 후 처음 실행 시(버전 번호가 변경될 때마다) 트리거됩니다. |
| 일별 참여 사용자 | a.DailyEngUserEvent | c_a_DailyEngUserEvent | 특정 날짜에 애플리케이션을 사용할 때 트리거됩니다. |
| 월별 참여 사용자 | 월별 참여 사용자 | a.MonthlyEngUserEvent | 특정 월에 애플리케이션을 사용할 때 트리거됩니다. |
| 시작 | a.LaunchEvent | c_a_LaunchEvent | 충돌 및 설치를 포함하여 매 실행 시 트리거됩니다. | 론치 라이프사이클 세션 시간 초과가 초과된 경우 백그라운드에서 다시 시작할 때도 트리거됩니다. |
| 충돌 | a.CrashEvent | c_a_CrashEvent | 응용 프로그램이 정상적으로 종료되지 않을 때 트리거됩니다. 이벤트는 충돌 후 응용 프로그램을 시작할 때 전송됩니다. 종료가 호출되지 않은 경우 응용 프로그램에 충돌이 발생한 것으로 간주됩니다. |
| 이전 세션 길이 | a.PreviousSessionLength | Cc_a_PreviousSessionLength | 집계된 이전 세션 길이 합계(초)입니다. |

*참고:일별&#x200B;**참여 사용자**및&#x200B;**월별 참여 사용자는**Analytics 지표에 자동으로 저장되지 않습니다. 이러한 지표를 캡처하려면 사용자 지정 이벤트를 설정하는 처리 규칙을 만들어야 합니다.*

### 차원

| 지표 | Analytics 컨텍스트 데이터/타겟 매개 변수 | Analytics Context Audience Manager 신호 | 설명 |
|--- |--- |--- |--- |
| 설치 날짜 | a.InstallDate | c_a_InstallDate | 설치 후 처음 시작하는 날짜 YYYY/MM/DD |
| 업그레이드 | a.UpgradeEvent | c_a_UpgradeEvent | 업그레이드 후 처음 실행 시(버전 번호가 변경될 때마다) 트리거됩니다. |
| 앱 ID | a.AppID | c_a_AppID | 애플리케이션 이름과 버전을 다음 형식으로 저장:`[AppName] [BundleVersion]` 구문을 사용하는 키-값 쌍으로 전달됩니다. 예, myapp 1.1. |
| 처음 사용한 이후 일수 | a.DaysSinceFirstUse | c_a_DaysSinceFirstUse | 처음 실행한 이후 일수입니다. |
| 월별 참여 사용자 | 월별 참여 사용자 | a.MonthlyEngUserEvent | 특정 월에 애플리케이션을 사용할 때 트리거됩니다. |
| 시작 | a.LaunchEvent | c_a_LaunchEvent | 충돌 및 설치를 포함하여 매 실행 시 트리거됩니다. | 론치 라이프사이클 세션 시간 초과가 초과된 경우 백그라운드에서 다시 시작할 때도 트리거됩니다. |
| 충돌 | a.CrashEvent | c_a_CrashEvent | 응용 프로그램이 정상적으로 종료되지 않을 때 트리거됩니다. 이벤트는 충돌 후 응용 프로그램을 시작할 때 전송됩니다. 종료가 호출되지 않은 경우 응용 프로그램에 충돌이 발생한 것으로 간주됩니다. |
| 이전 세션 길이 | a.PreviousSessionLength | Cc_a_PreviousSessionLength | 집계된 이전 세션 길이 합계(초)입니다. |
| 마지막 사용한 이후 일수 | a.DaysSinceLastUse | c_a_DaysSinceLastUse | 마지막 사용한 이후 일수. |
| 요일 | a.DayOfWeek | c_a_DayOfWeek | 앱을 시작한 평일 횟수. |
| 시간 | a.HourOfDay | c_a_HourOfDay | 앱을 시작한 시간을 측정합니다. 24시간 숫자 형식을 사용합니다. 피크 사용 시간을 결정하기 위한 시간 분할에 사용됩니다. |
| 운영 체제 버전 | a.OSVersion | c_a_OSVersion | OS 버전. |
| 마지막 업그레이드한 이후 일수 | a.DaysSinceLastUpgrade | c_a_DaysSinceLastUpgrade | 애플리케이션 버전 번호가 변경된 이후의 일수입니다. |
| 마지막 업그레이드 이후 출시 | a.LaunchesSinceUpgrade | c_a_LaunchesSinceUpgrade | 애플리케이션 버전 번호가 변경된 이후의 시작 횟수. |
| 장치 이름 | a.DeviceName | c_a_DeviceName | 장치 이름을 저장합니다. | iOS: iOS 장치를 식별하는 쉼표로 구분된 2자리 문자열. 첫 번째 번호는 일반적으로 장치 생성을 나타내며 두 번째 번호는 일반적으로 장치 제품군의 다른 구성원을 나타냅니다. iOS 장치 버전을 참조하여 일반 장치 이름 목록을 확인합니다. |
| 통신사 이름 | a.CarrierName | c_a_CarrierName | 장치에서 제공한 대로 모바일 서비스 공급자의 이름을 저장합니다. |
| 해상도 | a.Resolution | c_a_Resolution | 너비 x 높이(실제 픽셀) |

*참고:마지막 업그레이드&#x200B;**이후**일수,**마지막 업그레이드**이후 시작 및&#x200B;**통신사**이름은Analytics 변수에 자동으로 저장되지 않습니다. You must create a processing rule to copy these values to an Analytics variable for reporting.*

## 컨텍스트 데이터

컨텍스트 데이터는 애플리케이션 데이터를 컬렉션 서버로 전송하는 기본 방법입니다.

값을 props 및 eVars에 명시적으로 할당하는 대신 컨텍스트 데이터 변수를 사용하여 SiteCatalyst에 매핑되는 이름 값 쌍을 전송할 수 있습니다. 이러한 키 값 쌍을 기반으로 하여 이벤트를 설정하고, 값을 eVar 및 prop에 복사하고, 추가 조건문을 실행할 수 있습니다. 이렇게 하면 다른 보고서 세트 구성을 지원하기 위해 코드를 업데이트하는 것이 방지됩니다.

추적 방법을 사용하여 컨텍스트 데이터를 전송하는 방법은 두 가지가 있습니다. PersistentContextData 개체에 직접 설정한 컨텍스트 데이터는 각 호출과 함께 전송됩니다. 또한 해당 호출만 사용하여 전송되는 단일 추적 호출에 컨텍스트 데이터를 매개 변수로 전달할 수도 있습니다.

### 영구 컨텍스트 데이터

영구 컨텍스트 데이터에 배치된 값은 각 서버 호출을 사용하여 전송됩니다. 다음 예제에서는 "key" 및 "value"가 모든 trackAppState 호출을 사용하여 전송됩니다.

```
Hashtable<String, Object> contextData = new HashTable<String,Object>();
contextData.put("key", "value");
measure.setPersistentContextData(contextData);
measure.trackAppState("state1");
measure.trackAppState("state2");
measure.trackAppState("state3");
```

### 단일 호출 컨텍스트 데이터

단일 호출을 위해 컨텍스트 데이터를 전송하려면 매개 변수로 컨텍스트 데이터를 추적 호출로 전송합니다(trackAppState, trackEvents 등).

다음 예제에서는 "key" 및 "value"가 모두 세 trackAppState 호출을 사용하여 전송됩니다. 그러나 "key2" 및 "value2"는 두 번째 trackAppState 호출만 사용하여 전송됩니다.

```
Hashtable<String, Object> contextData = new HashTable<String,Object>();
contextData.put("key", "value");
measure.setPersistentContextData = contextData;
Hashtable<String, Object> contextDataState = new HashTable<String,Object>();
contextDataState.put("key2", "value2");
measure.trackAppState("state1");
measure.trackAppState("state2", contextDataState);
measure.trackAppState("state3");
```

## 구성 변수

다음 변수는 애플리케이션을 시작할 때 설정됩니다.:

*참고:ReportSuiteID 및 trackingServer를 제외한 모든 구성 변수는 선택 사항입니다.*

**공유 인스턴스**

측정 호출을 하기 전에 측정 라이브러리에서 호출하는 각 메서드에 대해 라이브러리의 인스턴스를 검색해야 합니다.

```
ADMS_Measurement measure = ADMS_Measurement.sharedInstance(((Activity)
context).getApplication());
```

*참고: 구성 변수는 개인 변수입니다. get 및 set 메서드를 사용하여 이러한 값을 변경합니다.*

### 구성 변수

**reportSuiteID**:(필수) 추적하려는 보고서 세트(다중 세트 태깅). 여러 보고서 세트를 추적하려면 각 보고서 세트의 쉼표로 구분된 목록을 전달합니다.

단일 호출을 위해 이 변수를 무시할 수 없으며 영구 값을 변경해야 합니다.

구문:

```
String getReportSuiteIDs()
void setReportSuiteIDs(String reportSuiteIDs)
```

예:

`measure.setReportSuiteIDs("rsid");`

다중 세트 태깅:
`measure.setReportSuiteIDs("rsid1, rsid2");`

**trackingServer**:(필수) 수집 서버를 식별합니다.

이 변수는 "http://" 또는 https://" 프로토콜 접두사 없이 추적 서버 도메인으로 채워야 합니다. 프로토콜 접두사는 ssl 변수를 기반으로 하여 라이브러리에서 자동으로 처리합니다.

ssl이 true이면 이 서버에 보안 연결이 설정됩니다. ssl이 false이면 이 서버에 비보안 연결이 설정됩니다.

단일 호출을 위해 이 변수를 무시할 수 없으며 영구 값을 변경해야 합니다.

구문:

```
String getTrackingServer()
void setTrackingServer(String trackingServer)
```

예:

`measure.setTrackingServer("metrics.corp1.com");`

**visitorID**:기본값:uuid각 방문자에 대한 고유 식별자입니다. 사용자 지정 visitorID를 설정하지 않은 경우 고유한 visitorID가 생성됩니다.

특정 사용 사례가 없다면 기본값을 사용하여 visitorID를 설정하는 것이 좋습니다. 사용자 지정 visitorID를 설정하면 라이프사이클 추적을 사용할 때 중복된 방문이 발생할 수 있습니다. 이를 피하려면 앱 측정을 구성하기 전에 visitorID를 설정하십시오.

**characterSet**:기본값은 UTF-8입니다.

구문:

```
String getCharSet()
void setCharSet(String charSet)
```

예:
`[measure.setCharacterSet("UTF-8");`

**currencyCode**:Default는 none입니다(보고서 세트에 대해 정의된 값이 사용됨).

Android 애플리케이션에서 추적된 구매 또는 통화 이벤트에 사용된 통화 코드.

구문:

```
String getCurrencyCode()
void setCurrencyCode(String currencyCode)
```

예:
`measure.setCurrencyCode("USD");`

**lifecycleSessionTimeout**:기본값은 5분입니다

앱 시작이 새 세션으로 간주되기 전에 다음 앱이 시작되기까지 경과되어야 하는 시간(초)을 지정합니다. 이 시간 초과는 응용 프로그램이 백그라운드로 전송되고 다시 활성화될 때도 적용됩니다. 앱이 백그라운드에서 소요하는 시간은 세션 길이에 포함되지 않습니다.

구문:

```
int getLifecycleSessionTimeout()
void setLifecycleSessionTimeout(int sessionLength)
```

예:

`measure.setLifecycleSessionTimeout(600); //10 minute session`

**ssl**:기본값은 false입니다.

SSL(HTTPS)을 통해 측정 데이터 전송을 활성화(true)/비활성화(false)합니다. 단일 호출을 위해 이 변수를 무시할 수 없으며 영구 값을 변경해야 합니다.

구문:

`void setSSL(boolean ssl)`

예:

`measure.setSSL(true);`

**debugLogging** 기본값은 false입니다.

출력 콘솔에서 디버그 정보 보기 및 라이브러리 버전을 활성화(true)하거나 비활성화(false)합니다. 기본적으로 이 변수는 false입니다. 단일 호출을 위해 이 변수를 무시할 수 없으며 영구 값을 변경해야 합니다.

구문:

`void setDebugLogging(boolean debugLogging)`

예:

`measure.setDebugLogging(true);`

## 추적 변수

**공유 인스턴스**

측정 호출을 하기 전에 측정 라이브러리에서 호출하는 각 메서드에 대해 라이브러리의 인스턴스를 검색해야 합니다.

```
ADMS_Measurement measure = ADMS_Measurement.sharedInstance(((Activity)
context).getApplication());
```

*참고: 구성 변수는 개인 변수입니다. get 및 set 메서드를 사용하여 이러한 값을 변경합니다.*

### 영구 추적 변수

**Evar**:지정된 eVar를 제공된 값으로 설정합니다. eVar은 빈 문자열로 설정하거나 var 지우기를 호출하여 지워질 때까지 모든 추적 호출을 사용하여 전송됩니다.

구문:

`void setEvar(int evarNum, String evarValue)`

예:
`measure.setEvar(1, "value");`

**Prop**:지정된 prop을 제공된 값으로 설정합니다. prop은 빈 문자열로 설정하거나 clearVars를 호출하여 지워질 때까지 모든 추적 호출을 사용하여 전송됩니다.

구문:

`void setProp(int propNum, String propValue)`

예:

`measure.setProp(1, "value");`

**hier**:지정된 heir 변수를 제공된 값으로 설정합니다. heir 변수는 빈 문자열로 설정하거나 clearVars를 호출하여 지워질 때까지 모든 추적 호출을 사용하여 전송됩니다.

구문:

`void setHier(int hierNum, String hierValue)`

예:

`measure.setHier(1, "value");`


**ListVar**:지정된 listVar을 제공된 값으로 설정합니다. listVar는 빈 문자열로 설정하거나 clearVars를 호출하여 지워질 때까지 모든 추적 호출을 사용하여 전송됩니다.

구문:

`void setListVar(int listNum, String listValue)`

예:

`measure.setListVar(1, "value");`

**purchaseID**:purchaseID 파섹

사이트에서 구매 이벤트를 사용할 때마다 purchaseID 변수를 사용하여 이 구매에 고유한 ID를 할당해야 합니다.

`measure.setPurchaseID("unique_id");`

**transactionID**:Integration Data Sources는 거래 ID를 사용하여 오프라인 데이터를 온라인 트랜잭션(예: 온라인에서 생성된 리드 또는 구매)에 연결합니다.

Adobe에 전송된 각 고유 transactionID는 해당 트랜잭션에 대한 오프라인 정보의 데이터 소스 업로드 준비 시 기록됩니다.

`measure.setTransactionID("unique_id");`

**appState**:(페이지 이름)앱 상태에 제공된 값은 페이지 이름 변수에 저장됩니다.

`measure.setAppState("state");`

**채널**:measure.setChannel("mobile");

**appSection**:앱 섹션에 제공된 값은 서버 변수에 저장됩니다.

구문:

`void setAppSection(String Section)`

예:
`measure.setAppSection("news");`

**campaign**

구문:

`void setCampaign(String Campaign)`

예:

`measure.setCampaign("112233");`

**products**

구문:

```
void setProducts(String Products)
// example Products string: Category;Product[,Category;Product]
```

예:

`measure.setProducts("Running;Shoe");`

**events**

구문:

`void setEvents(String Event) //comma-delimited list`

예:

`measure.setEvents("event1, event2");`

**geoState**

구문:

`void setGeoState(String GeoState)`

예:

`measure.setGeoState("UT");`

**geoZip**

구문:

`void setGeoZip(String GeoZip)`

예:

`measure.setGeoZip("12345");`

**지속적인 컨텍스트 데이터**:영구 컨텍스트 데이터에 배치된 값은 각 서버 호출과 함께 전송됩니다. 단일 호출을 위해 컨텍스트 데이터를 전송하려면 contextData 해시 테이블을 매개 변수로 추적 호출로 전송합니다(trackAppState, trackEvents 등).

예:

```
Hashtable contextData = new Hashtable<String, Object>();
contextData.put("key", "value");
measure.setPersistentContextData(contextData);
```

컨텍스트 데이터를 참조하십시오.

**linkTrackVars**:링크 추적을 위해 현재 변수 세트를 제한하는 쉼표로 구분된 변수 이름 목록입니다. linkTrackVars가 정의되지 않은 경우 AppMeasurement for Android는 trackLink 호출을 사용하여 정의된 모든 변수를 전송합니다.

구문:

`void setLinkTrackVars(String Vars) //comma-delimited list`

예:

`measure.setLinkTrackVars("eVar1, prop1");`

**linkTrackEvents**:링크 추적을 위해 현재 이벤트 세트를 제한하는 쉼표로 구분된 이벤트 목록. linkTrackEvents가 정의되지 않은 경우 AppMeasurement for Android는 trackLink 호출을 사용하여 모든 이벤트를 전송합니다.

구문:

`void setLinkTrackEvents(String Events) //comma-delimited list`

예:

`measure.setLinkTrackEvents("event1, event2");`

## 메서드

이 섹션에는 Android 라이브러리에서 제공하는 메서드 목록이 포함되어 있습니다.

**공유 인스턴스**

측정 호출을 하기 전에 측정 라이브러리에서 호출하는 각 메서드에 대해 라이브러리의 인스턴스를 검색해야 합니다.

```
ADMS_Measurement measure = ADMS_Measurement.sharedInstance(((Activity)
context).getApplication());
```

### 초기 구성

이 메서드는 필요한 변수를 구성하며 다른 메서드 전에 호출해야 합니다.

**configureMeasurement**:이 메서드는 애플리케이션 측정을 시작하는 데 필요한 두 매개 변수를 구성하는 데 사용됩니다. 서버 호출을 전송하기 전에 이 메서드를 사용하여 측정 개체에서 reportSuiteIDs 및 trackingServer 값을 설정해야 합니다.

구문:

`void configureMeasurement(String reportSuiteIDs, String trackingServer)`

예:

`measure.configureMeasurement("my_rsid", "my_tracking_server");`

### 이벤트 및 상태 추적

사용자 지정 이벤트와 앱 상태를 추적하는 데 사용되는 기본 메서드입니다.

**trackAppState**:애플리케이션에서 애플리케이션 상태를 추적하는 데 권장되는 방법입니다. appState에서 제공하는 값은 서버 호출의 페이지 이름 변수로 나타납니다. appState 문자열은 다음 호출로 전달되지 않기 때문에 호출할 때마다 제공해야 합니다.

이 호출과 함께 전송된 컨텍스트 데이터는 persistentContextData에 있는 값에 추가되며 호출과 함께 전송됩니다. persistentContextData에 설정된 값만 다음 호출 동안 유지됩니다.

구문:

`void trackAppState(string AppStateName)`

예:

`measure.trackAppState("state");`

```
Hashtable contextData = new Hashtable<String, Object>();
contextData.put("key", "value");
measure.trackAppState("state", contextData);
```

**trackEvents**:애플리케이션에서 이벤트를 추적하는 데 권장되는 방법입니다. trackEvents는 trackAppState와 비슷하지만 페이지 이름 대신 이벤트를 전송합니다. 이벤트는 쉼표로 구분된 문자열로 제공됩니다. events 문자열은 다음 호출로 전달되지 않기 때문에 호출할 때마다 제공해야 합니다.

이 메서드는 trackLinkURL을 기본적으로 호출합니다. 여기서 linkURL은 nil로 설정되고, linkType은 "o"로 설정되며 linkName은 애플리케이션 ID로 채워집니다.

즉, linkTrackVars 및 linkTrackEvents는 trackEvents에 대한 호출에 적용됩니다.

이 호출과 함께 전송된 컨텍스트 데이터는 persistentContextData에 있는 값에 추가되며 호출과 함께 전송됩니다. persistentContextData에 설정된 값만 다음 호출 동안 유지됩니다.

구문:

`void trackEvents(string Events)`

예:

`measure.trackEvents("event1");`

```
Hashtable<String, Object> contextData = new HashTable<String,Object>();
contextData.put("key", "value");
measure.trackEvents("event1", contextData);
```

**trackLink 메서드를 사용 중인 경우 메모 가져오기**

trackEvents는 trackLink를 호출합니다. 여기서 linkURL은 null로 설정되고, linkType은 "o"으로 설정되며 linkName은 애플리케이션 ID로 채워집니다. 이는 이벤트를 전송할 때마다 페이지 뷰(상태 뷰) 카운트가 증가되는 것을 방지하기 위한 것입니다.

trackLink를 직접 호출하고 linkTrackVars 및 linkTrackEvents에 대한 값을 설정하는 경우 이러한 변수와 이벤트 제한은 TrackEvents에 적용됩니다. 즉, 이러한 목록에 정의된 변수와 이벤트만 TrackEvents를 사용하여 전송됩니다. 이러한 제한을 trackEvents에 적용하고 싶지 않은 경우 linkTrackVars 및 linkTrackEvents를 null로 설정해야 합니다.

### 고급 추적(Track 및 TrackLink)

이러한 메서드는 추가 추적 옵션을 제공하며 prop, eVar 및 다른 SiteCatalyst 변수를 직접 채울 수 있습니다. 이 방법은 기존 구현이 있는 고객 또는 다른 SiteCatalyst 구현에 아주 익숙한 고객이 사용해야 합니다.

`track` 및 `trackLink`는 여러 플랫폼에서 Adobe 측정 라이브러리의 모든 버전에 구현되는 핵심 측정 메서드입니다. 모바일 애플리케이션을 추적하는 대부분의 환경에서 track 및 trackLink를 직접 호출하는 대신 trackAppState, trackEvents 메서드를 사용하는 것이 쉽습니다.

페이지 뷰 추적(track) 및 링크 추적(trackLink)은 값(null 아님, 비어 있지 않음, 0이 아님)을 가진 모든 변수를 전송합니다. 필요에 따라 track 또는 trackLink를 호출하기 전에 모든 변수를 재설정하거나 지워야 합니다.

*참고:최신 애플리케이션에는 멀티스레드 특성이 있으므로 향후 추적 호출과 함께 전송할 영구 변수 값을 설정하는 것은 권장되지 않습니다(setEvar, setProp, setHier, SetListVar 및 setPersistentContextData 사용). 예를 들어, 변수 값이 여러 스레드에서 설정된 경우 추적 호출을 만들 때 값이 일관되지 않은 상태일 수 있습니다. 이를 피하려면 각 추적 호출 시 컨텍스트 데이터를 전달하고 처리 규칙에 변수 값을 설정하는 것이 좋습니다.

**메서드 설명**

**추적**:측정 개체에 설정된 추가 변수와 함께 표준 페이지 보기를 수집 서버로 전송합니다.

각 추적 호출은 측정 개체에 정의된 모든 영구 데이터(clearVars의 경우 설명에 나열됨)와 해당 호출에 대해서만 사용자가 제공하는 contextData 또는 변수를 전송합니다. 정의된 변수를 전송하는 경우 해당 영구 변수에 있는 모든 값을 덮어씁니다.

구문:

```
void track()
void track(Hashtable<String, Object> contextData)
void track(Hashtable<String, Object> contextData, Hashtable<String, Object>
variables)
```

예:

`measure.track();`

```
measure.setEvar(1, "evar1value");
Hashtable contextData = new Hashtable<String, Object>();
contextData.put("key", "value");
measure.track(contextData);
```

```
//set an eVar
measure.setEvar(1, "evar1value");
//contextData
Hashtable contextData = new Hashtable<String, Object>();
contextData.put("key", "value");
//variable overrides
Hashtable variableOverrides = new Hashtable<String, Object>();
variableOverrides.put("evar2", "evar2value");
//sends eVar1, eVar2 (set in overrides), and context data
measure.track(contextData, variableOverrides);
```

**trackLink**:값이 있는 모든 trackconfig 변수와 함께 사용자 지정, 다운로드 또는 종료 링크 데이터를 Adobe 데이터 수집 서버로 전송합니다.

trackLink를 사용하여 페이지 뷰를 수집해서는 안 되는 모든 활동을 추적합니다.

구문:

```
void trackLink(String linkURL, String linkType, String linkName,
Hashtable<String, Object> contextData, Hashtable<String, Object> variables)
```

**linkURL**: 클릭한 URL을 나타냅니다. URL을 지정하지 않을 경우 이름이 사용됩니다. Android 애플리케이션 내에서 웹 페이지로 연결하는 경우에만 이 매개 변수를 사용하십시오. 그렇지 않으면 이 매개 변수에 대해 null이 전달됩니다.

**linkType**: URL 또는 이름을 표시하는 링크 보고서를 나타냅니다. 지원되는 값은 다음과 같습니다.
* “o”(사용자 지정 링크)
* “d”(파일 다운로드)
* “e”(종료 링크)

**linkName**: 링크 보고서에 나타나는 이름입니다. 이름을 지정하지 않을 경우 보고서에 URL이 사용됩니다.

데이터를 수집하려면 linkURL 또는 linkName 매개 변수 중 하나를 지정해야 합니다. 이러한 매개 변수, 컨텍스트 데이터 또는 추가 변수 중 하나를 사용하지 않는 경우 null을 값으로 전달합니다.

예:

`measure.trackLink("url", "o", "name", contextData, null);`

**setEvar**:지정된 eVar를 제공된 값으로 설정합니다. eVar은 빈 문자열로 설정하거나 var 지우기를 호출하여 지워질 때까지 모든 추적 호출을 사용하여 전송됩니다.

구문:

`void setEvar(int evarNum, String evarValue)`

**setProp**:지정된 prop을 제공된 값으로 설정합니다. prop은 빈 문자열로 설정하거나 var 지우기를 호출하여 지워질 때까지 모든 추적 호출을 사용하여 전송됩니다.

구문:

`void setProp(int propNum, String propValue)`

**setHier**:지정된 heir 변수를 제공된 값으로 설정합니다. heir 변수는 빈 문자열로 설정하거나 var 지우기를 호출하여 지워질 때까지 모든 추적 호출을 사용하여 전송됩니다.

구문:

`void setHier(int hierNum, String hierValue)`

**setListVar**:지정된 listVar을 제공된 값으로 설정합니다. listVar은 빈 문자열로 설정하거나 var 지우기를 호출하여 지워질 때까지 모든 추적 호출을 사용하여 전송됩니다.

구문:

`void setListVar(int listNum, String listValue)`

**setPersistentContextData**:영구 컨텍스트 데이터에 배치된 값은 각 서버 호출과 함께 전송됩니다. 단일 호출을 위해 컨텍스트 데이터를 전송하려면 contextData 해시 테이블을 매개 변수로 추적 호출로 전송합니다(trackAppState, trackEvents 등).

```
Hashtable<String, Object> contextData = new HashTable<String,Object>();
contextData.put("key", "value");
measure.setPersistentContextData(contextData);
```

컨텍스트 데이터를 참조하십시오.

**clearVars**:객체의 다음 변수에서 값을 제거합니다.

```
props
eVars
heirs
listVars
events
PersistentContextData
purchaseID
transactionID
appState
channel
appSection
campaign
products
geoZip
geoState
linkTrackVars
linkTrackEvents
```

구문:

`void clearVars()`

예:
`measure.clearVars();`

**오프라인 추적**&#x200B;을 추가했습니다

*참고: 오프라인 AppMeasurement를 활성화하려면 보고서 세트에 타임스탬프가 활성화되어 있어야 합니다.*

다음 변수를 사용하면 애플리케이션이 오프라인 상태일 때 측정 호출을 저장할 수 있습니다. 오프라인 AppMeasurement를 활성화하려면 보고서 세트는 타임스탬프 활성화되어야 합니다. 이 변경 후에 모든 히트 수는 타임스탬프로 처리되어야 하며, 그렇지 않으면 삭제됩니다. JavaScript에서 데이터도 수집하는 보고서 세트에 AppMeasurement 데이터를 현재 보고하는 경우 데이터 손실을 방지하기 위해 오프라인 AppMeasurement를 위해 별도의 보고서 세트를 설정해야 할 수 있습니다.

활성화되면 Offline AppMeasurement는 다음 방식으로 동작합니다.
* 애플리케이션은 서버 호출을 전송하지만 데이터 전송은 실패합니다.
* AppMeasurement가 현재 히트에 대한 타임스탬프를 생성합니다.
* AppMeasurement가 히트 데이터를 버퍼링한 후, 데이터 손실을 방지하기 위해 영구 저장 장치에 버퍼링된 히트 데이터를 백업합니다.

후속 히트가 발생할 때마다 또는 offlineThrottleDelay에서 정의한 간격으로 AppMeasurement가 초기 히트 순서를 유지하면서 버퍼링된 히트 데이터를 전송합니다. 데이터 전송에 실패하면 히트 데이터 버퍼링을 계속합니다. 이는 장치가 오프라인인 동안 계속됩니다.

### 구성 메서드

**setOfflineTrackingEnabled**:기본값은 false입니다. 측정 라이브러리에 대한 오프라인 추적을 활성화하거나 비활성화합니다.

구문:

`void setOfflineTrackingEnabled(boolean Enabled);`

예:"measure.setOfflineTrackingEnabled(true);

**setOfflineHitLimit**:기본값은 1000입니다. 큐에 저장되는 최대 오프라인 히트 수입니다. 히트 제한이 5000 이상으로 설정된 경우 성능이 나빠질 수 있습니다.

구문:

`void setOfflineHitLimit(int offlineHitLimit)`

예:

`measure.setOfflineHitLimit(2000);`

**getTrackingQueueSize**:오프라인 큐에서 저장된 추적 호출 수를 반환합니다.

구문:

`int getTrackingQueueSize()`

예:

`int size = measure.getTrackingQueueSize();`

**clearTrackingQueue**:오프라인 큐에서 모든 저장된 추적 호출을 제거합니다.

구문:

`void clearTrackingQueue()`

예:

`measure.clearTrackingQueue();`

**경고: 되돌릴 수 없으므로 큐를 수동으로 지울 때는 주의하십시오.**


**setOnline 및 setOffline**:측정 개체의 온라인 또는 오프라인 상태를 수동으로 설정합니다. 라이브러리는 장치가 오프라인인지 또는 온라인인지 자동으로 감지하므로 이러한 메서드는 측정 오프라인을 강제로 수행하는 경우에만 필요합니다. SetOnline은 수동으로 오프라인 상태가 된 후에 온라인 상태로 되돌리는 데만 사용됩니다.

측정이 오프라인 상태일 때:

* offlineTrackingEnabled가 true인 경우: 측정이 오프라인 상태가 될 때까지 히트는 저장됩니다.
* offlineTrackingEnabled가 false인 경우 히트가 무시됩니다.

구문:

```
void setOnline()
void setOffline()
```

예:

```
measure.setOffline();
measure.setOnline();
```

## 오프라인 추적

AppMeasurement를 사용하면 Android 장치가 오프라인 상태일 때도 애플리케이션 사용량을 측정할 수 있습니다.

*참고: 오프라인 AppMeasurement를 활성화하려면 보고서 세트에 타임스탬프가 활성화되어 있어야 합니다.*

오프라인 추적을 참조하십시오.

## Target

Adobe는 Android 애플리케이션 내에서 타깃팅된 컨텐츠를 전달하는 기능을 제공합니다.

Test&amp;Target에서 반환되는 컨텐트는 HTML, XML 또는 일반 텍스트 같은 텍스트 기반 컨텐트가 될 수 있습니다. 컨텐트가 로드되면 Android 애플리케이션 개발자는 애플리케이션 내에서 컨텐트가 소비되는 방법을 결정합니다. 애플리케이션의 동작을 변경하기 위해 컨텐트를 HTML로 표시하거나 사용할 수 있습니다. 이 안내서는 Test&amp;Target 클래스의 간단한 사용 예를 제공합니다.

요구 사항

* JDK 5/6/7
* Platform 1.5 이상용 Android SDK.

이 섹션의 예는 Eclipse를 기반으로 합니다.

**라이브러리 가져오기**

Developer Connection의 모바일 애플리케이션 측정 및 최적화를 방문하여 Android 라이브러리를 다운로드합니다.

다운로드 파일의 압축을 풀면 다음 소프트웨어 구성 요소를 갖게 됩니다.

* admsAppLibrary.jar: Android 장치 및 시뮬레이터와 함께 사용하도록 고안된 라이브러리입니다. Android 2.0 이상이 필요합니다.
* Examples\TrackingHelper.java: 추적 코드를 애플리케이션 로직과 구분하도록 고안된 선택적 클래스입니다.

**프로젝트에 라이브러리 추가**

1. Eclipse IDE에서 프로젝트 이름을 마우스 오른쪽 버튼으로 클릭합니다.
1. 작성 경로 &gt; 외부 아카이브 추가를 선택합니다.
1. admsAppLibrary.jar를 선택합니다.
1. 열기를 클릭합니다.
1. 다시 프로젝트를 마우스 오른쪽 버튼으로 클릭한 다음 작성 경로 &gt; 작성 경로 구성을 선택합니다.
1. 주문 및 내보내기 탭을 클릭합니다.
1. admsAppLibrary.jar가 선택되었는지 확인합니다.

애플리케이션에서 .*;를 사용하여 `importcom.adobe.ADMS.*;`admsAppLibrary.jar 라이브러리로부터 클래스/인터페이스를 가져올 수 있습니다.

**앱 권한 추가**

AppMeasurement 라이브러리를 사용하려면 데이터를 전송하고 오프라인 추적 호출을 기록할 다음 권한이 필요합니다.

* INTERNET
* ACCESS_NETWORK_STATE

이러한 권한을 추가하려면 애플리케이션 프로젝트 디렉토리의 AndroidManifest.xml 파일에 다음 줄을 추가하십시오.

```
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

예

프로젝트에 라이브러리를 추가하고 앱 권한을 추가한 후에 Test&amp;Target 클래스 MboxFactory와 Mbox를 사용할 수 있습니다.

다음 예는 간단한 Android 애플리케이션 내에서 Test&amp;Target을 WebView로 HTML 컨텐트를 로드하는 방법을 보여줍니다. 이 예는 관련 HTML 오퍼와 캠페인이 Test&amp;Target 관리 도구에서 이미 만들어졌고 캠페인이 승인되었다고 가정합니다.

1. 구현의 단계를 완료한 다음 애플리케이션 또는 활동 하위 클래스 상단에서 testandtarget 패키지를 가져옵니다.

   `com.adobe.adms.testandtarget.*;`

2. mbox를 만들려면 아래의 번호 지정된 코드를 수행하십시오(각 코드 행에 대한 설명은 주석 참조). 이 단계를 완료하려면 Test&amp;Target 관리 도구에서 캠페인 설정에 사용되는 클라이언트 코드와 mbox의 이름을 알고 있어야 합니다.

   ```
   public class AndroidDemoApplication extends Activity {
   private WebView _webView;
   public void onCreate(Bundle savedInstanceState) {
   super.onCreate(savedInstanceState);
   _webView = new WebView(this);
   setContentView(_webView);
   // 1. Create an instance of the MboxFactory class with your client code.
   MboxFactory factory = new MboxFactory("androiddemo16");
   // 2. Use the MboxFactory instance to create an Mbox.
   Mbox mbox = factory.create("DemoApp");
   // 3. Set the default content for the Mbox.
   mbox.setDefaultContent("<h1>DEFAULT CONTENT</h1>");
   /**
   * 4. Create a custom MboxContentConsumer to consume the content returned. The
   * CustomMboxContentConsumer class defined below simply displays the content
   * returned in a BrowserField as HTML.
   */
   CustomConsumer consumer = new CustomConsumer(_webView);
   mbox.addOnLoadConsumer(consumer);
   // 5. Load the Mbox.
   mbox.load();
   ...
   ```

3. MboxContentConsumer 인터페이스를 구현하는 사용자 지정 클래스를 정의합니다. 이 추상 인터페이스는 컨텐트를 전달하는 “consume”이라는 메서드를 정의하기만 하면 됩니다. 아래 정의된 CustomConsumer 클래스는 WebView의 컨텐트를 표시합니다.

   ```
   class CustomConsumer implements MboxContentConsumer {
   private WebView _view;
   public CustomConsumer(WebView webview) {
   _view = webview;
   }
   public void consume(String content) {
   _view.loadData(content, "text/html", "utf-8");
   }
   }
   ```

4. 프로젝트를 마우스 오른쪽 버튼으로 클릭하고 다른 이름으로 실행 &gt; Android 애플리케이션을 선택하여 애플리케이션을 작성하고 테스트합니다. Test&amp;Target 캠페인을 올바르게 설정하고 승인한 경우 Android 장치 에뮬레이터에 표시된 오퍼를 볼 수 있을 것입니다.

**라이프사이클 지표**&#x200B;를 참조하십시오

라이프사이클 지표가 활성화된 경우 라이프사이클 지표가 각 mbox 로드에 매개 변수로 전송됩니다.

* (권장) 라이프사이클 이벤트 추적
* 라이프사이클 지표

## 대상 관리

Adobe는 신호를 보내고 대상 관리에서 방문자 세그먼트를 검색하는 기능을 제공합니다.

### 요구 사항

* JDK 5/6/7
* Platform 1.5 이상용 Android SDK.

이 섹션의 예는 Eclipse를 기반으로 합니다.

### 라이브러리 가져오기

Developer Connection의 모바일 애플리케이션 측정 및 최적화를 방문하여 Android 라이브러리를 다운로드합니다.

다운로드 파일의 압축을 풀면 다음 소프트웨어 구성 요소를 갖게 됩니다.

* admsAppLibrary.jar: Android 장치 및 시뮬레이터와 함께 사용하도록 고안된 라이브러리입니다. Android 2.0 이상이 필요합니다.
* Examples\TrackingHelper.java: 추적 코드를 애플리케이션 로직과 구분하도록 고안된 선택적 클래스입니다.

### 프로젝트에 라이브러리 추가

1. Eclipse IDE에서 프로젝트 이름을 마우스 오른쪽 버튼으로 클릭합니다.
1. 작성 경로 &gt; 외부 아카이브 추가를 선택합니다.
1. admsAppLibrary.jar를 선택합니다.
1. 열기를 클릭합니다.
1. 다시 프로젝트를 마우스 오른쪽 버튼으로 클릭한 다음 작성 경로 &gt; 작성 경로 구성을 선택합니다.
1. 주문 및 내보내기 탭을 클릭합니다.
1. admsAppLibrary.jar가 선택되었는지 확인합니다.

애플리케이션에서 .*;를 사용하여 `importcom.adobe.ADMS.*;`admsAppLibrary.jar 라이브러리로부터 클래스/인터페이스를 가져올 수 있습니다.

### 앱 권한 추가

AppMeasurement 라이브러리를 사용하려면 데이터를 전송하고 오프라인 추적 호출을 기록할 다음 권한이 필요합니다.
* INTERNET
* ACCESS_NETWORK_STATE

이러한 권한을 추가하려면 애플리케이션 프로젝트 디렉토리의 AndroidManifest.xml 파일에 다음 줄을 추가하십시오.

```
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

### 코드 샘플

프로젝트에 라이브러리를 추가하면 ADMS_AudienceManager 클래스를 사용할 수 있습니다. To import the audience manager package add: `import com.adobe.adms.audiencemanager;`

1. 대상 관리를 구성합니다.

   `ADMS_AudienceManager.ConfigureAudienceManager("mycompany.demdex.net", this);`

   mycompany.demdex.net을 종단점으로 바꿉니다. 애플리케이션에서 언제든지 대상 관리를 구성할 수 있습니다.


2. 선택적으로 dpid 및 dpuuid를 설정합니다.

   `ADMS_AudienceManager.SetDpidAndDpuuid("284", "abc123");`

3. 트레이트 사전을 만들고 그 사전을 신호로 전송합니다.

```
HashMap<String, Object> data = new HashMap<String, Object>();
data.put("trait", "b");
ADMS_AudienceManager.SubmitSignal(data, new
ADMS_AudienceManager.AudienceManagerCallback<HashMap>() {
@Override
public void call(HashMap visitorProfile) {
// do things with visitorProfile
}
});
```

방문자 프로필 사전이 콜백에 content 매개 변수로 반환됩니다.

### 라이프사이클 지표

라이프사이클 지표가 활성화되고 대상 관리가 application:didFinishLaunchingWithOptions:에 구성된 경우에는 구성이 완료된 후 라이프사이클 지표가 포함된 신호가 전송됩니다.

* (권장) 라이프사이클 이벤트 추적
* 라이프사이클 지표

### ADMS_AudienceManager 참조

**메서드**

**ConfigureAudienceManager**:대상 관리 끝점을 설정합니다.

구문:

`public static void ConfigureAudienceManager(String server, Context context);`

예:

`ADMS_AudienceManager.ConfigureAudienceManager("mycompany.demdex.net", this);`

**GetDebugLogging**:Audience Manager 메서드에서 콘솔에 디버그 로깅을 제공할지 여부를 나타내는 부울 값을 반환합니다.

구문:

`public static boolean GetDebugLogging();`

**GetDpid**:dpid를 반환합니다.

구문:

`public static String GetDpid();`

**GetDpuuid**:dpuuid를 반환합니다.

구문:

`public static String GetDpuuid();`

**GetVisitorProfile**:이 방법은 가장 최근 방문자 프로필을 검색하기 위한 신호를 제출한 후 언제든지 호출할 수 있습니다.

방문자 프로필에는 stuff 개체에서 반환된 모든 키 값 쌍이 포함되어 있습니다.

구문:

`public static HashMap GetVisitorProfile();`

**SetDebugLogging**:콘솔에서 디버그 로깅을 활성화하거나 비활성화합니다.

구문:

`public static void SetDebugLogging(boolean logging);`

**SetDpidAndDpuuid**:newDpid 및 newDpuuid가 설정되면 각 신호와 함께 전송됩니다.

구문:

`public static void SetDpidAndDpuuid(String newDpid, String newDpuuid);`

**전송 신호**:트레이트 사전으로 전송하고 콜백에서 업데이트된 방문자 프로필을 받습니다.

JSON 응답의 uuid는 내부적으로 저장되고 이후의 모든 신호에 사용됩니다. 또한 픽셀 요청은 dests 개체에 있는 각 URL로 전송됩니다.

구문:

```
public static void SubmitSignal(HashMap<String, Object> data,
AudienceManagerCallback<HashMap> callback);
```

### 인터페이스

**메서드**


**AudienceManagerCallback**

구문:

```
public interface AudienceManagerCallback<T> {
AudienceManagerCallback
public void call(T item);
}
```

SubmitSignal 호출에서 콜백에 사용된 개체의 인터페이스입니다.


## PhoneGap 플러그인

이 플러그인을 사용하여 PhoneGap 프로젝트에서 Android AppMeasurement 호출을 전송할 수 있습니다.

PhoneGap 프로젝트 생성에 대한 도움을 얻으려면 Android로 PhoneGap 시작하기를 참조하십시오.

이 플러그인을 다운로드하려면 SiteCatalyst용 PhoneGap iOS 및 Android 플러그인을 참조하십시오.

### 플러그인 포함

1. ADMS_plugin.java를 src 폴더의 패키지에 복사합니다.
2. ADMS_Helper.js를 PhoneGap 프로젝트의 assets/www/js 폴더에 복사합니다.
3. In the res/xml folder, open config.xml file and register an new plugin by creating a new child node under plugins: `<plugin name="ADMS_Plugin" value="[YOUR_PACKAGE_NAME].ADMS_plugin" />`

For example, if you package is named com.example.phonegaptest, then your plugin node would be the following: `<plugin name="ADMS_Plugin" value="com.example.phonegaptest.ADMS_plugin" />`

### AppMeasurement 라이브러리 포함

AppMeasurement 라이브러리를 다운로드하려면 라이브러리 가져오기를 참조하십시오.

1. admsAppLibrary.jar를 PhoneGap 프로젝트의 libs 폴더에 복사합니다.
2. libs &gt; 작성 경로 &gt; 작성 경로 구성을 마우스 오른쪽 단추로 클릭하여 작성 경로에 admsAppLibrary.jar가 있는지 확인합니다.
3. 라이브러리 탭에서 목록에 없는 경우 JAR 추가를 클릭하고 libs 폴더에서 admsAppLibrary.jar를 선택합니다.


### 라이프사이클 지표 자동 추적

추적 라이프 사이클 추적에는 PhoneGap 외부의 구성이 필요합니다. 라이프사이클 자동 추적을 활성화하려면 개발자 빠른 시작에서 구현 단계를 완료합니다.

### 플러그인 사용

추적을 사용할 html 파일에 다음을 포함합니다.

`<script type="text/javascript" src="js/ADMS_Helper.js"></script>`

이제 측정 호출을 수행할 준비가 되었습니다. PhoneGap 플러그인 메서드를 참조하십시오.

### 문제 해결

**구문이 올바른데 플러그인의 코드가 작동하지 않는 이유는 무엇입니까?**

Check your output console for the following error: `java.lang.ClassNotFoundException: ADMS_plugin`

이 오류가 발생하면 플러그인 포함 섹션에서 3단계를 수행했는지 확인하십시오.

## PhoneGap 플러그인 메서드

이러한 메서드를 사용할 html 파일에 다음을 포함합니다.

`<script type="text/javascript" src="js/ADMS_Helper.js"></script>`

**구성 메서드**


**configureMeasurementWithReportSuiteIDsTrackingServer**:이 메서드는 애플리케이션 측정을 시작하는 데 필요한 두 매개 변수를 구성하는 데 사용됩니다. 서버 호출을 전송하기 전에 이 메서드를 사용하여 측정 개체에서 reportSuiteIDs 및 trackingServer 값을 설정해야 합니다.

구문:

`void configureMeasurementWithReportSuiteIDsTrackingServer(stringreportSuiteIDs, string trackingServer);`

예:

`ADMS.configureMeasurementWithReportSuiteIDsTrackingServer("testRSID","10.20.40.199:5050");`

**setOnline 및 setOffline**:측정 개체의 온라인 또는 오프라인 상태를 수동으로 설정합니다. 라이브러리는 장치가 오프라인인지 또는 온라인인지 자동으로 감지하므로 이러한 메서드는 측정 오프라인을 강제로 수행하는 경우에만 필요합니다. SetOnline은 수동으로 오프라인 상태가 된 후에 온라인 상태로 되돌리는 데만 사용됩니다.

측정이 오프라인 상태일 때:

* offlineTrackingEnabled가 true인 경우: 측정이 오프라인 상태가 될 때까지 히트는 저장됩니다.
* offlineTrackingEnabled가 false인 경우 히트가 무시됩니다.

구문:

```
void setOnline();
void setOffline();
```

예:

```
ADMS.setOnline();
ADMS.setOffline();
```

**setDebugLogging**:디버그 정보 보기를 활성화(true)/비활성화(false)합니다. 기본적으로 이 변수는 false입니다.

변수 대체를 사용하여 이 변수를 대체할 수 없습니다.

구문:

`void setDebugLogging(bool debugLogging);`

예:

`ADMS.setDebugLogging(true);`

### 이벤트 및 상태 추적 메서드


**trackAppState**:애플리케이션에서 애플리케이션 상태(예: 페이지)를 추적하는 데 권장되는 방법입니다. appState에서 제공하는 값은 서버 호출의 페이지 이름 변수로 나타납니다. appState 문자열은 다음 호출로 전달되지 않기 때문에 호출할 때마다 제공해야 합니다.

구문:

`void trackAppState(string stateName);`

예:

`ADMS.trackAppState("login page");`

**track 파섹**:애플리케이션에서 애플리케이션 상태(예: 페이지)를 추적하는 데 권장되는 방법입니다. appState에서 제공하는 값은 서버 호출의 페이지 이름 변수로 나타납니다. appState 문자열은 다음 호출로 전달되지 않기 때문에 호출할 때마다 제공해야 합니다.

이 호출과 함께 전송된 컨텍스트 데이터는 persistentContextData에 있는 값에 추가되며 호출과 함께 전송됩니다. persistentContextData에 설정된 값만 다음 호출 동안 유지됩니다.

구문:

`void trackAppStateWithContextData(string stateName, JSON cData);`

cData: 컨텍스트 데이터로 전송할 키-값 쌍이 있는 JSON 개체

예:

```
trackAppStateWithContextData("login page",
{"user":"john","remember":"true"});
```

**trackEvents**:애플리케이션에서 이벤트를 추적하는 데 권장되는 방법입니다. trackEvents는 trackAppState와 비슷하지만 페이지 이름 대신 이벤트를 전송합니다. 이벤트는 쉼표 trackEvents로 구분된 문자열로 제공됩니다. events 문자열은 다음 호출로 전달되지 않기 때문에 호출할 때마다 제공해야 합니다.

이 메서드는 trackLinkURL을 기본적으로 호출합니다. 여기서 linkURL은 null로 설정되고, linkType은 "o"로 설정되며 linkName은 애플리케이션 ID로 채워집니다.

즉, linkTrackVars 및 linkTrackEvents는 `trackEvents`에 대한 호출에 적용됩니다.

구문:

`void trackEvents(string eventNames);`

예:

`ADMS.trackEvents("login,event2");`

**trackLink 메서드를 사용 중인 경우 메모 가져오기**

`trackEvents`는 trackLinkURL을 기본적으로 호출합니다. 여기서 linkURL은 null로 설정되고, linkType은 "o"로 설정되며 linkName은 애플리케이션 ID로 채워집니다. 이는 이벤트를 추적할 때마다 페이지 뷰(상태 뷰) 카운트가 증가되는 것을 방지하기 위한 것입니다.

trackLinkURL을 직접 호출하고 linkTrackVars 및 linkTrackEvents에 대한 값을 설정하는 경우 이러한 변수와 이벤트 제한이 TrackEvents에 적용됩니다. 즉, 이러한 목록에 정의된 변수와 이벤트만 TrackEvents를 사용하여 전송됩니다. 이러한 제한을 trackEvents에 적용하고 싶지 않은 경우 linkTrackVars 및 linkTrackEvents를 null로 설정해야 합니다.

**trackEventsWithContextData**:애플리케이션에서 이벤트를 추적하는 데 권장되는 방법입니다. trackEvents는 trackAppState와 비슷하지만 페이지 이름 대신 이벤트를 전송합니다. 이벤트는 쉼표로 구분된 문자열로 제공됩니다. events 문자열은 다음 호출로 전달되지 않기 때문에 호출할 때마다 제공해야 합니다.

이 메서드는 trackLinkURL을 기본적으로 호출합니다. 여기서 linkURL은 null로 설정되고, linkType은 "o"로 설정되며 linkName은 애플리케이션 ID로 채워집니다.

즉, linkTrackVars 및 linkTrackEvents는 trackEvents에 대한 호출에 적용됩니다.

이 호출과 함께 전송된 컨텍스트 데이터는 persistentContextData에 있는 값에 추가되며 호출과 함께 전송됩니다. persistentContextData에 설정된 값만 다음 호출 동안 유지됩니다.

구문:

`void trackEventsWithContextData(string eventNames, JSON cData);`

cData: 컨텍스트 데이터로 전송할 키-값 쌍이 있는 JSON 개체

예:

`ADMS.trackEventsWithContextData("login,event2",
{"user":"john","remember":"true"});`

**trackLink 메서드를 사용 중인 경우 메모 가져오기**

trackEvents는 trackLinkURL을 기본적으로 호출합니다. 여기서 linkURL은 null로 설정되고, linkType은 "o"로 설정되며 linkName은 애플리케이션 ID로 채워집니다. 이는 이벤트를 추적할 때마다 페이지 뷰(상태 뷰) 카운트가 증가되는 것을 방지하기 위한 것입니다.

trackLinkURL을 직접 호출하고 linkTrackVars 및 linkTrackEvents에 대한 값을 설정하는 경우 이러한 변수와 이벤트 제한이 TrackEvents에 적용됩니다. 즉, 이러한 목록에 정의된 변수와 이벤트만 TrackEvents를 사용하여 전송됩니다. 이러한 제한을 trackEvents에 적용하고 싶지 않은 경우 linkTrackVars 및 linkTrackEvents를 null로 설정해야 합니다.

**고급 추적 메서드(track 및 trackLink)**

이러한 메서드는 추가 추적 옵션을 제공하며 prop, eVar 및 다른 SiteCatalyst 변수를 직접 채울 수 있습니다. 이 방법은 기존 구현이 있는 고객 또는 다른 SiteCatalyst 구현에 아주 익숙한 고객이 사용해야 합니다.

`track` 및 `trackLink`는 여러 플랫폼에서 Adobe 측정 라이브러리의 모든 버전에 구현되는 핵심 측정 메서드입니다. 모바일 애플리케이션을 추적하는 대부분의 환경에서 track 및 trackLink를 직접 호출하는 대신 trackAppState, trackEvents 메서드를 사용하는 것이 쉽습니다.

페이지 뷰 추적(track) 및 링크 추적(trackLink)은 값(null 아님, 비어 있지 않음, 0이 아님)을 가진 모든 변수를 전송합니다. 필요에 따라 track 또는 trackLink를 호출하기 전에 모든 변수를 재설정하거나 지워야 합니다.

**메서드**

**추적**:측정 개체에 설정된 추가 변수와 함께 표준 페이지 보기를 수집 서버로 전송합니다.

구문:

`void track();`

예:

`ADMS.track();`

**trackWithContextData**:측정 개체에 설정된 추가 변수와 함께 표준 페이지 보기를 수집 서버로 전송합니다.

각 trackWithContextData 호출은 측정 개체에 정의된 모든 영구 데이터(clearVars의 경우 설명에 나열됨)와 해당 호출에 대해서만 사용자가 제공하는 contextData를 전송합니다.

구문:

`void trackWithContextData(JSON cData);`

cData: 컨텍스트 데이터로 전송할 키-값 쌍이 있는 JSON 개체

예:

`ADMS.trackWithContextData({"key1":"value1","key2":"value2"});`


**trackWith ContextDataAndVariables**:측정 개체에 설정된 추가 변수와 함께 표준 페이지 보기를 수집 서버로 전송합니다.

각 trackWithContextDataAndVariables 호출은 측정 개체에 정의된 모든 영구 데이터(clearVars의 경우 설명에 나열됨)와 해당 호출에 대해서만 사용자가 제공하는 contextData 및 변수를 전송합니다. 정의된 변수를 전송하는 경우 해당 영구 변수에 있는 모든 값을 덮어씁니다.

구문:

`void trackWithContextDataAndVariables(JSON cData, JSON vars);`

cData: 컨텍스트 데이터로 전송할 키-값 쌍이 있는 JSON 개체

예:

```
ADMS.trackWithContextDataAndVariables({"key1":"value1","key2":"value2"},
{"eVar1":"newValue","prop3":"newValue"});
```

**trackLinkURLWithLinkTypeName**:값이 있는 추적 구성 변수와 함께 사용자 지정, 다운로드 또는 종료 링크 데이터를 Adobe 데이터 수집 서버로 전송합니다.

trackLink를 사용하여 페이지 뷰를 수집해서는 안 되는 모든 활동을 추적합니다.

각 trackLinkURLWithLinkTypeNameContextDataVariables 호출은 측정 개체에 정의된 모든 영구 데이터(clearVars의 경우 설명에 나열됨)와 해당 호출에 대해서만 사용자가 제공하는 contextData를 전송합니다.

구문:

```
void trackLinkURLWithLinkTypeNameContextDataVariables(string`
linkUrl, string linkType, string linkName, JSON cData, JSON vars);
```

cData: 컨텍스트 데이터로 전송할 키-값 쌍이 있는 JSON 개체

예:

```
ADMS.trackLinkURLWithLinkTypeNameContextDataVariables("theLink",
"o", "logout", {"key1":"value1"}, {"eVar1":"newValue"});
```

### AppMeasurement 변수 설정 및 가져오기

**메서드**

**setEvarToValue**:지정된 eVar를 제공된 값으로 설정합니다. eVar은 다음 추적 호출을 사용하여 전송됩니다.

구문:

`void setEvarToValue(int evar, string value);`

예:

`ADMS.setEvarToValue(1, "newValue");`

**setPropToValue**:지정된 prop을 제공된 값으로 설정합니다. prop은 다음 추적 호출을 사용하여 전송됩니다.

구문:

void setPropToValue(int prop, string value);

예:

`ADMS.setPropToValue(1, "newValue");`

**setHierToValue**:지정된 hier 변수를 제공된 값으로 설정합니다. 이 변수는 다음 추적 호출 시 전송됩니다.

구문:

`void setHierToValue(int hier, string value);`

예:

`ADMS.setHierToValue(1, "newValue");`

**setListVarToValue**:지정된 listvar를 제공된 값으로 설정합니다. listvar는 다음 추적 호출 시 전송됩니다.

구문:

`void setListVarToValue(int list, string value);`

예:

`ADMS.setListVarToValue(1, "newValue");`

**getEvar**:지정된 변수를 가져옵니다.

구문:

`void getEvar(int evar, function success, function fail);`

예:

```
ADMS.getEvar(1, function (value) { myTempEvar1 = value; }, function ()
{ myTempEvar1 = null; });
```

**getProp**:지정된 변수를 가져옵니다.

구문:

`void getProp(int prop, function success, function fail);`

예:

```
ADMS.getProp(1, function (value) { myTempProp1 = value; }, function ()
{ myTempProp1 = null; });
```

**getHier**:지정된 변수를 가져옵니다.

구문:

`void getHier(int hier, function success, function fail);`

예:

```
ADMS.getHier(1, function (value) { myTempHier1 = value; }, function ()
{ myTempHier1 = null; });
```

**getListVar**:지정된 변수를 가져옵니다.

구문:

`void getListVar(int list, function success, function fail);`

예:

```
ADMS.getListVar(1, function (value) { myTempListVar1 = value; }, function
() { myTempListVar1 = null; });
```

**clearVars**:객체의 다음 변수에서 값을 제거합니다.

```
props
eVars
heirs
listVars
events
PersistentContextData
purchaseID
transactionID
appState
channel
appSection
campaign
products
geoZip
geoState
linkTrackVars
linkTrackEvents
```

구문:

`void clearVars();`

예:

`ADMS.clearVars();`

**trackingQueueSize**:오프라인 큐에서 저장된 추적 호출 수를 가져오거나 설정합니다.

구문:

`void trackingQueueSize(function success, function fail);`

예:

`ADMS.trackingQueueSize(function (value) { myQueueSize = value; }, function () { myQueueSize = 0; });`

**clearTrackingQueue**:오프라인 큐에서 모든 저장된 추적 호출을 제거합니다. 경고: 되돌릴 수 없으므로 큐를 수동으로 지울 때는 주의하십시오.

구문:

`void clearTrackingQueue();`

예:

`ADMS.clearTrackingQueue();`

### 구성 변수 설정 및 가져오기

**메서드**

**getVersion**:라이브러리 버전을 가져옵니다.

구문:

`void getVersion(function success, function fail);`

예:

```
ADMS.getVersion(function (value) { versionNum = value; }, function ()
{ versionNum = 1.0; });
```

**setReportSuiteIDs**:(필수) 추적하려는 보고서 세트(다중 세트 태깅). 여러 보고서 세트를 추적하려면 각 보고서 세트의 쉼표로 구분된 목록을 전달합니다.

단일 호출을 위해 이 변수를 무시할 수 없으며 영구 값을 변경해야 합니다.

구문:
`void setReportSuiteIDs(string reportSuiteIDs);`

예:

`ADMS.setReportSuiteIDs("rsid1, rsid2");`

**setTrackingServer**:(필수) 수집 서버를 식별합니다.

이 변수는 코드 관리자에서 사용자를 위해 생성한 값으로 채워야 합니다.

ssl을 활성화한 경우 보안 추적에 같은 값이 사용됩니다.

단일 호출을 위해 이 변수를 무시할 수 없으며 영구 값을 변경해야 합니다.

구문:

`void setTrackingServer(string trackingServer);`

예:

`ADMS.setTrackingServer("10.23.52.191:5923");`

**setDataCenter**:

구문:

`void setDataCenter(string dataCenter);`

예:

`ADMS.setDataCenter("myDataCenter");`

**setVisitorID**:기본값은 CFUUID입니다.

각 방문자의 고유 식별자. 사용자 지정 visitorID를 설정하지 않은 경우 초기 실행 시 visitorID가 생성되어(Apple의 CFUUID 사용) 사용자 기본 키에 저장됩니다. 이 키는 현 시점으로부터 AppMeasurement 및 PhoneGap에서 사용됩니다. 또한 이 키는 표준 애플리케이션 백업 프로세스 시 저장되고 복원됩니다.

구문:

`void setVisitorID(string visitorId);`

예:

`ADMS.setVisitorID("myVisitorId");`

**setCharSet**:기본값은 UTF-8입니다.

구문:

`void setCharSet(string charSet);`

예:

`ADMS.setCharSet("UTF-8");`

**setCurrencyCode**:기본값은 none(보고서 세트에 대해 정의된 값이 사용됨)입니다.

iOS 애플리케이션에서 추적된 구매 또는 통화 이벤트에 사용된 통화 코드.

구문:

`void setCurrencyCode(string currencyCode);`

예:

`ADMS.setCurrencyCode("USD");`


**setSLEunenabled**:기본값은 false입니다.

SSL(HTTPS)을 통해 측정 데이터 전송을 활성화(true)/비활성화(false)합니다. 단일 호출을 위해 이 변수를 무시할 수 없으며 영구 값을 변경해야 합니다.

구문:

`void setSSLEnabled(bool sslEnabled);`

예:

`ADMS.setSSLEnabled(false);`

### 영구 추적 변수 설정 및 가져오기

**메서드**

**setPurchaseID**:

구문:

`void setPurchaseID(string purchaseId);`

예:

`ADMS.setPurchaseID("purchase1");`

**setTransactionID**:

구문:

`void setTransactionID(string transactionId);`

예:

`ADMS.setTransactionID("transaction1");`

**setAppState**:

구문:

`void setAppState(string stateName);`

예:

`ADMS.setAppState("myAppState");`

**setChannel**:

구문:

`void setChannel(string channel);`

예:

`ADMS.setChannel("myChannel");`

**setAppSection**:

구문:

`void setAppSection(string appSection);`

예:

`DMS.setAppSection("myAppSection");`

**setCampaign**:

구문:

`void setCampaign(string campaign);`

예:

`ADMS.setCampaign("myCampaign");`

**setProducts**:

구문:

`void setProducts(string products);`

예:

`ADMS.setProducts("myProduct1,myProduct2");`

**setEvents**:

구문:

`void setEvents(string events);`

예:

`ADMS.setEvents("event1, event2");`

**setGeoState**

구문:

`void setGeoState(string state);`

예:

`ADMS.setGeoState("FL");`

**setGeoZip**:

구문:

`void setGeoZip(string zip);`

예:

`ADMS.setGeoZip("39984");`

**setPersistentContextData**:컨텍스트 데이터는 데이터를 수집하는 데 권장되는 방법입니다. 컨텍스트 데이터를 전송하려면 JSON 개체를 만들고 전송하려는 값에 대해 키 값 쌍을 할당합니다.

구문:

`void setPersistentContextData(JSON cData);`

예:

`ADMS.setPersistentContextData({"key1":"value1"});`

**persistentContextData**:

구문:

`void persistentContextData(function success, function fail);`

예:

```
ADMS.persistentContextData(function(value) { alert(value); },
function(error) { alert(error); });
```

**setLinkTrackVars**:링크 추적을 위해 현재 변수 세트를 제한하는 쉼표로 구분된 변수 이름 목록입니다.

linkTrackVars가 정의되지 않은 경우 PhoneGap 플러그인은 trackLink 호출을 사용하여 정의된 모든 변수를 전송합니다.

구문:

`void setLinkTrackVars(string linkTrackVars);`

예:

`ADMS.setLinkTrackVars("eVar1,eVar2");`


**setLinkTrackEvents**:링크 추적을 위해 현재 이벤트 세트를 제한하는 쉼표로 구분된 이벤트 목록. linkTrackEvents가 정의되지 않은 경우 PhoneGap 플러그인은 trackLink 호출을 사용하여 모든 이벤트를 전송합니다.

구문:

`void setLinkTrackEvents(string linkTrackEvents);`

예:

`ADMS.setLinkTrackEvents("event1,loginEvent");`


**setLightTrackVars**:라이트 추적 호출에 대한 현재 변수 집합을 제한하는 쉼표로 구분된 변수 목록. 라이트 서버로 전송하는 이 변수는 ClientCare에 의해 구성됩니다.

구문:

`void setLightTrackVars(string lightTrackVars);`

예:

`ADMS.setLightTrackVars("prop1,hier3");`

### 오프라인 추적

**메서드**

**setOfflineTrackingEnabled**:

구문:

`void setOfflineTrackingEnabled(bool offlineTrackingEnabled);`

예:

`ADMS.setOfflineTrackingEnabled(true);`

**setOfflineHitLimit**:

구문:

`void setOfflineHitLimit(int offlineHitLimit);`

예:

`ADMS.setOfflineHitLimit(3000);`

## Android 버전 2.x ~ 3.x 마이그레이션 안내서

* AppMeasurement는 이제 ADMS_Measurement입니다. 입니다. 이 클래스를 참조할 위치를 찾고 이름을 ADMS_Measurement로 업데이트합니다.
* getInstance는 이제 sharedInstance입니다. getInstance를 호출하는 위치를 찾고 sharedInstance로 바꿉니다.
* churn 측정에 대한 모든 호출을 제거합니다(getChurnInstance). 이러한 호출은 자동 추적에 의해 처리되고 이제 컨텍스트 데이터를 사용하여 삽입됩니다.
* Timestamp가 제거됩니다. 라이브러리는 타임스탬프를 자동으로 처리합니다.

다음 메서드의 구문이 변경되었습니다. 모든 속성과 메서드의 업데이트된 예를 구성 변수 및 메서드를 참조하십시오.


### 보고서 세트

**이전 버전(2.1.x)**

`account`

**새 버전(3.x)**

`reportSuiteIDs`

### 추적

**이전 버전(2.1.x)**


`String track()`

`String track(Hashtable variableOverrides)`

**새 버전(3.x)**

사용하지 않은 값에 대해 null을 전달합니다.

```
void track()
void track(Hashtable<String, Object>
contextData)
void track(Hashtable<String, Object>
contextData, Hashtable<String, Object>
variables)
```

### 링크 추적

**이전 버전(2.1.x)**

```
String trackLink(String linkURL, String
linkType, String linkName)
```

```
String trackLink(String linkURL, String
linkType, String linkName,
Hashtable variableOverrides)
```

**새 버전(3.x)**

이러한 두 호출은 단일 호출로 대체되었습니다. 사용하지 않은 값에 대해 null을 전달합니다.

```
void trackLink(String linkURL, String linkType,
String linkName,
Hashtable<String, Object> contextData,
Hashtable<String, Object> variables)
```

### 오프라인 추적 메서드

**이전 버전(2.1.x)**

`void forceOffline();`


`void forceOnline();`

**새 버전(3.x)**

`void setOnline();`

`void setOffline();`


### 변수 이름 변경

다음 목록은 2.x 버전 변수와 3.x 버전의 해당 값을 표시합니다. 라이브러리를 좀 더 모바일 집중형으로 만들고 구현을 간소화할 수 있도록 3.x 버전에서 몇 가지 변수가 제거되었습니다.


*참고: 3.x 버전은 공개 변수 대신 getter 및 setter를 사용합니다. get 및 set 메서드를 사용할 수 있도록 변수를 직접 설정하는 코드에서 위치를 업데이트해야 합니다.*

```
timestamp; //Removed
trackOffline; //void setOfflineTrackingEnabled(boolean Enabled)
offlineLimit; //void setOfflineHitLimit(int offlineHitLimit)
account; //reportSuiteIDs
linkURL; //Removed (sent with linkTrackURL)
linkName; //Removed (sent with linkTrackURL)
linkType; //Removed (sent with linkTrackURL)
linkTrackVars; //void setLinkTrackVars(String Vars) //comma-delimited list
linkTrackEvents; //void setLinkTrackEvents(String Events) //comma-delimited list
dc; //Removed
trackingServer; //void setTrackingServer(String trackingServer)
trackingServerSecure; //Removed, trackingServer value is used for secure server if ssl=YES
userAgent; //Removed
dynamicVariablePrefix; //Removed
visitorID; //void setVisitorID(String ID)
charSet; //void setCharSet(String charSet)
visitorNamespace; //Removed
pageName; //void setAppState(String State)
pageURL; //Removed
referrer; //Removed
currencyCode; //void setCurrencyCode(String currencyCode)
purchaseID; //void setPurchaseID(String ID)
channel; //void setChannel(String Channel)
server; //void setAppSection(String Section)
pageType; //Removed
transactionID; //void setTransactionID(String ID)
campaign; //void setCampaign(String Campaign)
state; //void setGeoState(String GeoState)
zip; //void setGeoZip(String GeoZip)
events; //void setEvents(String Event) //comma-delimited list
products; //void setProducts(String Products)
list1-list3; //setListVar(int listNum, String listValue);
hier1-heir5; //setHier(int hierNum, String hierValue);
prop1-prop75; //setProp(int propNum, String propValue);
eVar1-eVar75; //setEvar(int evarNum, String evarValue);
ssl; //void setSSL(boolean ssl)
linkLeaveQueryString; //Removed
debugTracking; //debugLogging
usePlugins; //Removed
useBestPractices; //Removed - handled by Lifecycle AutoTracking
contextData; //persistentContextData
```

## Bloodhound를 사용하여 모바일 애플리케이션 테스트

Bloodhound 도구를 사용하여 모바일 애플리케이션을 테스트하기 위해 로컬 컴퓨터에 서버 호출을 전송할 수 있습니다.

*중요: 2017년 4월 30일 현재 Adobe Bloodhound는 종료되었습니다. 2017년 5월 1일부터 추가적인 개선이나 추가 엔지니어링 또는 Adobe Expert Care 지원이 제공되지 않습니다.*

애플리케이션을 개발할 때 Bloodhound를 사용하면 로컬별 서버 호출을 볼 수 있으며 선택적으로 Adobe 컬렉션 서버에 데이터를 전송할 수 있습니다.

Bloodhound는 Mac과 Windows에서 사용할 수 있습니다.

### 요구 사항

* Snow Leopard(10.6) 이상을 실행하는 Intel 기반 Mac 컴퓨터 또는 Windows PC
* 모바일 장치 또는 시뮬레이터에 대한 네트워크 연결.

### 다운로드

Developer Connection에서 Bloodhound - 앱 측정 QA 도구를 참조하십시오.

### 설치

* Mac: 다운로드한 dmg를 열고 Bloodhound를 애플리케이션 폴더로 드래그하여 놓습니다.
* Windows: 다운로드한 설치 파일을 실행합니다.

### Bloodhound 사용

이 도구를 시작해도 [시작] 단추를 클릭해야만 서버가 활성화됩니다. 응용 프로그램에서 서버 호출을 캡처할 준비가 되면 [시작] 단추를 클릭합니다.

선택적으로 서버를 시작하기 전에 사용자 지정 포트 번호(1024보다 커야 함)를 지정할 수 있습니다. 포트 번호를 제공하지 않으면 서버는 열린 포트를 자동으로 선택합니다.

서버가 실행된 후 도구에 데이터를 전송하려면 애플리케이션이나 장치를 구성해야 하며, 이 내용은 다음 섹션에서 설명됩니다.

### Bloodhound로 히트를 전송하도록 장치 구성

장치의 프록시 설정을 변경하여 http 요청을 도구로 전송할 수 있습니다. 도구에 전송된 요청은 선택적으로 Adobe 데이터 컬렉션 서버에 전달될 수 있습니다.

장치가 프록시를 지원하지 않을 경우 히트를 테스트용으로 Bloodhound로 직접 전송할 수 있습니다.

*참고: Bloodhound는 SSL 추적을 지원하지 않습니다. Bloodhound를 사용하여 테스트할 때는 AppMeasurement 라이브러리에서 SSL을 비활성화해야 합니다.*

#### iOS 장치

iOS 장치는 Bloodhound를 호스팅하는 컴퓨터가 속한 동일한 네트워크에 연결되어 있어야 합니다.

1. 설정 &gt; Wi-Fi로 이동합니다.
1. 현재 Wi-Fi 네트워크 오른쪽에 있는 파란색 화살표를 클릭합니다.
1. HTTP 프록시 설정으로 스크롤합니다.
1. 자동을 선택합니다.
1. (Bloodhound UI의) 프록시 URL 및 포트를 URL 필드에 입력합니다.

#### 기타 장치

장치가 프록시 자동 구성을 지원하는 경우 간단하게 프록시 URL(Bloodhound UI)을 PAC(프록시 자동 구성) URL로 사용하면 됩니다. 프록시 지원은 Android 버전마다 다르며 구성을 단순화하기 위해 일부 Android용 프록시 구성 도구를 사용할 수 있습니다.

### 히트 직접 전송

프록시를 지원하지 않는 장치(iOS 시뮬레이터, 이전 Android 버전 등)의 경우 생성된 히트를 캡처하기 위해 Bloodhound를 추적 서버로 지정할 수 있습니다. 이렇게 하려면 추적 서버를 "<Bloodhound IP>:<BloodhoundPort>".

예:

```
//iOS
[measure configureMeasurementWithReportSuiteIDs:@"my_rsid" trackingServer:@"10.10.2.2:5000"];
measure.ssl = NO;
```

```
//Android
measure.configureMeasurement("my_rsid", "10.10.2.2:5000");
measure.ssl = false;
```

```
//WinRT for Windows 8, Windows Phone 8
measure.ConfigureMeasurement("my_rsid", "10.10.2.2:5000");
measure.ssl = false;
```

### 문제 해결/일반 문제

* Bloodhound는 SSL 이외의 추적에만 작동합니다. SSL을 통해 전송된 추적 히트는 위에서 사용된 메서드에 관계없이 어떤 경우에도 캡처되지 않습니다.

## Android 위젯

Android 위젯은 앱과 같은 메서드를 사용하여 추적할 수 있습니다. 위젯은 애플리케이션 컨텍스트를 앱과 공유하므로 히트 순서와 방문자 식별이 유지됩니다.

다음 지침은 Android 위젯을 추적하는 데 도움이 됩니다.

* 위젯 자체에서 라이프사이클 지표(startActivity/stopActivity) 호출을 구현하지 마십시오.
* 위젯이 홈 화면에 추가되는 시기를 추적하려면 trackState 또는 trackEvent 호출을 위젯의 onEnabled 메서드에 추가합니다.
* 위젯에서 앱이 시작되는 시기를 추적하려면 애플리케이션을 시작하려는 의도를 생성하기 전에 trackState 또는 trackEvent 호출을 추가합니다.
* 작업 컨텍스트를 추적하는 데 관심이 있다면 각각을 세그먼트화하는 옵션을 별도로 제공하는 ContextData 변수를 정의할 수 있습니다(예: AppExperienceType="widget" vs. "app").
