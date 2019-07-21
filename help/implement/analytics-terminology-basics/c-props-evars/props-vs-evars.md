---
description: Experience Cloud에서 사용할 수 있는 변수에는 몇 가지 유형이 있습니다. 흔히 사용되는 Prop 및 eVar의 두 유형을 사용하면 조직에서 표준적인 기성 보고서로는 제공되지 않는 사용자 지정 차원에 대한 사이트 보고서를 만들 수 있습니다.
keywords: Analytics 구현; prop; Evar; prop와 evar; 명명 규칙; 트래픽 변수; 지속성; 성공 이벤트; 경로 지정
seo-description: Experience Cloud에서 사용할 수 있는 변수에는 몇 가지 유형이 있습니다. 흔히 사용되는 Prop 및 eVar의 두 유형을 사용하면 조직에서 표준적인 기성 보고서로는 제공되지 않는 사용자 지정 차원에 대한 사이트 보고서를 만들 수 있습니다.
seo-title: Prop과 eVar 비교
solution: Analytics
title: Prop과 eVar 비교
topic: 개발자 및 구현
uuid: 0 F 02760 F-FF 69-481 C-A 817-799 F 02 DAFE 8 E
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Prop과 eVar 비교

Experience Cloud에서 사용할 수 있는 변수에는 몇 가지 유형이 있습니다. 흔히 사용되는 Prop 및 eVar의 두 유형을 사용하면 조직에서 표준적인 기성 보고서로는 제공되지 않는 사용자 지정 차원에 대한 사이트 보고서를 만들 수 있습니다.

지정되는 변수와 그 위치를 결정하려면 Prop과 eVar 기능 사이의 차이점을 이해하는 것이 중요합니다. 이러한 차이점을 이해하면 조직에서 사용하기에 가장 좋은 유형을 결정할 수 있습니다. 

**Prop과 eVar 비교**

다음은 Prop과 eVar의 주된 차이점입니다.

* **이름 지정 규칙**: Prop은 트래픽 변수로 취급됩니다. 즉, 사이트에서 다양한 차원의 인기도를 보고하는 데 사용됩니다. eVar는 전환 변수로 취급됩니다. 사이트에서 성공 이벤트에 가장 크게 기여하는 차원을 결정하는 데 사용됩니다.
* **지속성**: Prop은 실행한 이미지 요청을 넘어서까지 지속되지 않습니다. 같은 이미지 요청에 있지 않은 다른 변수와는 연결할 수 없습니다. 그러나 eVar는 지속적입니다. 백엔드 변수를 사용하여 처음 실행된 값을 보존하므로 나중에 성동 이벤트에 연결할 수 있습니다.
* **성공 이벤트**: 전환 이벤트라고도 하는 성공 이벤트는 방문자가 목표에 도달한 횟수를 측정하는 지표입니다. 사이트의 제품 구입, 신문 구독 등 다양한 것이 이 이벤트에 속할 수 있습니다. eVar는 전환 이벤트에 대해 보고하고, 방문자에게 영향을 주어 목표 달성에 도움이 되는 값을 표시할 수 있게 디자인되었습니다. 트래픽 변수에는 이 기능이 없습니다. 그러나 보고서 세트를 올바르게 구성하면 기여도 지표를 볼 수 있습니다.
* **경로 지정**: Prop은 경로 지정을 사용할 수 있으므로 조직이 표시된 변수의 컨텍스트 내에서 사용자가 이용한 경로를 볼 수 있습니다. Adobe 담당자는 요청을 받아 경로 지정을 활성화할 수 있습니다. eVar는 경로 지정을 사용할 수 없습니다.
* **사용 가능한 지표**: Prop과 eVar가 사용할 수 있는 지표는 변수의 설정과 데이터 플랫폼/버전에 따라 매우 다를 수 있습니다. 다음 목록은 기본적으로 활성화되는 것이 아닌 활성화할 수 있는 것을 소개합니다. 보고서에 사용하고 싶은 특정 지표를 찾을 수 없는 경우는 조직의 지원되는 사용자를 통해 고객 지원 센터에 문의하십시오.

<table id="table_FB963F60857A4AD79562324FB6F4B6A9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>지표 </p> </th> 
   <th colname="col2" class="entry"> <p>Prop </p> <p>(트래픽 변수) </p> </th> 
   <th colname="col3" class="entry"> <p>eVar </p> <p>(전환 변수) </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>평균 페이지 깊이 </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_165C1BF1574247CEA9190ADCABF79D69" /> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>평균 체류 시간 </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_9F0F396E11B442959EC3E5D4D508496D" /> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>바운스 비율 </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_A268EAF747EA45F8A6A93A1B66667A06" /> </p> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_09D486144CEA4293A505DCA3F90B82EC" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>바운스 수 </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_471A02B78FD842BB97ED3FF4A5908B03" /> </p> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_D2F11B5687484D9EBF6D1DEB3F303A20" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>계산된 지표 </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_7FAB1CF2ACC44D9198C648D3FC9E52D9" /> </p> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_8BCC2EE92CC04778809D1BD48D2623D7" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용자 지정 변환 이벤트 </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_D75C764B83AE4491A7E68C459FED1300" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>시작 </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_E9A1FCDFCB924D75ABFAEBD5570D4EE0" /> </p> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_F5E57974B5A64F3FA3A145428420EB23" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>종료 </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_BE343F94EAD74D54B6ABC80E8A76A9BD" /> </p> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_3183B2BB62C24B048EDED3295F2BEC85" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>인스턴스 </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_8733F5AC189E43DAA8D1847416EA68C8" /> </p> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_B10AB2898F3D4EBA947FADB27B118143" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>페이지 보기 횟수 </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_8BD2B23FBDA64A648BED40A2993F7C1C" /> </p> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_CBDFD74340FA4973847033C1F956F0AC" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>기여도 지표 </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_E63F978830FB46809E62654F37C4C182" /> </p> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_6AB756A4598F4452887D29AD4971985A" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>구입 지표 </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_8F8AB7CD02764245BA73CA1E6B69BAE1" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>다시 로드 </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_FBE0C84E01004937B7B408198A33A9E7" /> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>장바구니 지표 </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_123993465D734EABB311730ED03263F6" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>단일 액세스 </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_038C6991E3F341B18E7A355D17C88895" /> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>총 체류 시간 </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_090587D29F1649319033D5A15B34B138" /> </p> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_841DF09FD32A44B1B1B876F4E0CE29AC" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>고유 방문자 수 </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_38556E6A43B04E2E8A01855452D30A83" /> </p> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_F5D4BDE1AA9C4C58A6402418390EEC52" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>방문 횟수 </p> </td> 
   <td colname="col2"> <p><img  src="assets/check-mark.png" id="image_017BB279C5824028870360A5D4D27556" /> </p> </td> 
   <td colname="col3"> <p><img  src="assets/check-mark.png" id="image_2832E346D220429DA643B908EC10260D" /> </p> </td> 
  </tr> 
 </tbody> 
</table>

* **상세 분류**: Prop은 상관 관계를 사용하여 같은 이미지 요청에서 실행된 다른 트래픽 변수의 페이지 보기를 표시합니다. eVar는 하위 관계를 사용하여 성공 이벤트와 관련된 다른 전환 변수의 분류를 제공합니다.

## Prop 또는 eVar에 대한 고급 이점 {#section_B384031AB8674065BA5187B0A3A3DAB9}

버전 15의 릴리스로 Prop과 eVar 간의 기능 차이가 분명하지 않게 되었습니다. eVar는 최소한의 처리 부하로 경로 지표는 물론, 방문 수/고유 방문자 수와 같은 기능들을 포함하도록 최근에 업데이트되었습니다.

Prop에는 eVar의 몇 가지 장점들이 있으며, 그 중 일부는 우회할 수 있습니다.

* Prop 데이터는 수집되어 거의 즉시 보고에서 사용할 수 있습니다. eVar는 보고서 세트 데이터에 표시되는 데 30분 이상 소요될 수 있습니다.
* 모든 Prop에는 방문자가 사용자의 사이트에 도달하는 경로를 볼 수 있도록 해주는 플로차트와 유사한 보고서가 활성화될 수 있습니다. These pathing flow reports are available for both Props and eVars in [!UICONTROL Ad Hoc Analysis].
* Prop은 여러 수준과 관련지을 수 있으며, 이때 eVar는 하위 관계를 한 번만 맺을 수 있습니다. 이 제한은 동일한 데이터를 상관 관계로 제공하는 세그멘테이션을 사용하여 완화할 수 있습니다.
* 기여도 지표를 사용하면 성공 이벤트 전에 prop 값이 기여한 내용을 볼 수 있습니다.

반면에 eVar에는 제한된 Prop 특성에 대한 몇 가지 유리한 점이 있습니다.

* eVar는 성공 이벤트를 지표로 사용할 수 있습니다. Prop은 그렇게 할 수 없습니다.
* 모든 히트 만료 지정을 비롯하여 eVar 만료는 사용자 지정할 수 있습니다(어쨌든 영구 값은 없음). Prop은 어떤 식으로든 영구적이지 않습니다.

총 체류 시간, 시작 수 및 종료 수와 같은 경로 지표는 원래 eVar에는 사용할 수 없었습니다. 하지만, 최근의 업데이트를 통해 이러한 지표들을 사용할 수 있게 되어 eVar의 값이 증가했습니다.

## 사용할 항목 {#section_022D016A4EEB45179A15BFF044A261A4}

**Props:** 지연이 가장 큰 관심 사항이고 이 차원으로 트래픽(성공 이벤트 없음)만 측정하려는 경우 사용합니다.

**eVars:** 데이터 분류 및 관계가 가장 큰 문제입니다.

>[!TIP]
>
>Evar가 지속되지 않도록 하려면 만료를'히트'로 변경하여 히트가 히트 이외의 데이터를 유지하도록 할 수 있습니다.

