---
description: 다음 변수와 함수를 사용하면 애플리케이션이 오프라인 상태일 때 측정 호출을 저장할 수 있습니다.
keywords: Analytics 구현
seo-description: 다음 변수와 함수를 사용하면 애플리케이션이 오프라인 상태일 때 측정 호출을 저장할 수 있습니다.
seo-title: 오프라인 추적
solution: Analytics
title: 오프라인 추적
topic: 개발자 및 구현
uuid: f 7 c 55 aef -28 a 4-4 f 2 f -8 f 47-792 a 05 f 9525 b
translation-type: tm+mt
source-git-commit: 01a6fc7e44dc71b868bd38a4f6a5a4089eae6349

---


# 오프라인 추적

다음 변수와 함수를 사용하면 애플리케이션이 오프라인 상태일 때 측정 호출을 저장할 수 있습니다.

>[!NOTE]
>
>오프라인 추적을 활성화하려면 보고서 세트에 타임스탬프가 활성화되어 있어야 합니다. 보고서 세트에서 타임스탬프가 활성화된 경우 `trackOffline` 구성 속성이 *true*&#x200B;이어야 합니다. 보고서 세트에서 타임스탬프가 사용되지 않는 경우에는 `trackOffline` 구성 속성이 *반드시* false여야 합니다. 이 속성이 제대로 구성되지 않으면 데이터가 손실됩니다. 보고서 세트 타임 스탬프 활성화 여부가 확실치 않으면 [고객 지원 센터에 문의하십시오](https://helpx.adobe.com/contact/enterprise-support.ec.html#analytics)

활성화되면 Offline AppMeasurement는 다음 방식으로 동작합니다.

* 애플리케이션은 서버 호출을 전송하지만 데이터 전송은 실패합니다.
* AppMeasurement가 현재 히트에 대한 타임스탬프를 생성합니다.
* AppMeasurement가 히트 데이터를 버퍼링한 후, 데이터 손실을 방지하기 위해 영구 저장 장치에 버퍼링된 히트 데이터를 백업합니다.

후속 히트가 발생할 때마다 또는 `offlineThrottleDelay`에서 정의한 간격으로 AppMeasurement가 초기 히트 순서를 유지하면서 버퍼링된 히트 데이터를 전송합니다. 데이터 전송에 실패하면 히트 데이터 버퍼링을 계속합니다. 이는 장치가 오프라인인 동안 계속됩니다.

<table id="table_E8FD8C89025C4E819FE2FEBC7A78984D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 속성 또는 메서드 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>trackOffline </p> </td> 
   <td colname="col2"> <p>기본값: false </p> <p>측정 라이브러리에 대한 오프라인 추적을 활성화하거나 비활성화합니다. </p> <p> <b>예:</b> </p> 
    <code class="syntax c">s. trackoffline = true; </code>
  </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>offlineLimit </p> </td> 
   <td colname="col2"> <p>기본값: 제한 없음 </p> <p>큐에 저장되는 최대 오프라인 히트 수입니다. </p> <p> <b>예:</b> </p> 
    <code class="syntax c">s. offlinehitlimit = 100; </code>
  </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>offlineThrottleDelay </p> </td> 
   <td colname="col2"> <p>기본값: 0 </p> <p>AppMeasurement가 활성 네트워크 연결을 감지할 때 버퍼링된 히트 데이터를 전송하기 위한 케이던스(지연)을 밀리초로 지정합니다. 그러면 애플리케이션에서 여러 개의 히트를 전송함에 따른 성능 영향이 최소화됩니다. </p> <p>예를 들어 offlineThrottleDelay=1000의 경우 히트 데이터 전송에 300ms가 걸리고 AppMeasurement가 다음 버퍼링된 히트를 보내기 전에 700ms를 기다립니다. </p> 
    <code class="syntax c">s. offlinethrottledelay = 1000; </code>
  </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>forceOnline </p> <p>forceOffline </p> </td> 
   <td colname="col2"> <p> 측정 개체의 온라인 또는 오프라인 상태를 수동으로 설정합니다. 라이브러리는 장치가 오프라인인지 또는 온라인인지 자동으로 감지하므로 이러한 메서드는 측정 오프라인을 강제로 수행하는 경우에만 필요합니다. <code> forceOnline은 수동으로 오프라인 상태가 된 후에 온라인 상태로 되돌리는 데만 사용됩니다.</code> </p> <p>측정이 오프라인 상태일 때: </p> 
    <ul id="ul_5A9CFD2968F64F938652C1D779EB7589"> 
     <li id="li_AF074C55DFED4DC8BD8CF3D25805040C"> <code>trackOffline</code>이 true인 경우: 측정이 오프라인 상태가 될 때까지 히트는 저장됩니다. </li> 
     <li id="li_6A623377462548DB97C31654EADCFAF3"> <code>trackOffline</code>이 false인 경우 히트가 무시됩니다. </li> 
    </ul> <p> <b>예:</b> </p> 
    <code class="syntax c">s. forceoffline ();

s.forceOnline();
</code> </td>
</tr> 
 </tbody> 
</table>
