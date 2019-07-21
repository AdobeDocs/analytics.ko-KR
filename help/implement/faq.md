---
description: 구현에 대한 자주 묻는 질문 및 추가 정보 링크.
keywords: Analytics 구현; FAQ; FAQEvar 만료; 사용자 지정 이벤트 가시성; timestamp; 방문자 ID 유예 기간; 방문자 ID; Experience Cloud 방문자 ID; Analytics 방문자 ID; DTM; 하트비트; 쿠키; 추적 서버; 성능; Javascript; 데이터 수집; s_ code 버전; s_ code debug; 링크 유형 추적; 비디오 추적; Track Mobile App; 퍼스트 파티 쿠키; SSL 인증서; 인증 만료; 인증서 만료; Plugins; 데이터 삽입 API; 500 오류; 500; 사용자 관리; 그룹 관리; 사용자; 그룹
seo-description: 구현에 대한 자주 묻는 질문 및 추가 정보 링크.
seo-title: Analytics 구현에 대한 FAQ
solution: Analytics
title: Analytics 구현에 대한 FAQ
topic: 개발자 및 구현
uuid: 983 D 759 A-C 4 F 2-4021-84 C 8-0486 DBB 951 B 8
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# Analytics 구현에 대한 FAQ

구현에 대한 자주 묻는 질문 및 추가 정보 링크.

<table id="table_91790388C2DE4C5E8AEF0B9981AFFE27"> 
 <tbody> 
  <tr> 
   <td> <b>질문</b> </td> 
   <td> <b>답변</b> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Analytics 사용자 및 그룹을 어떻게 관리합니까? </p> </td> 
   <td colname="col3"> <p>For information about managing users and groups, refer to <a href="https://marketing.adobe.com/resources/help/en_US/reference/user_management.html" format="html" scope="external"> User and Product Management </a> in the Adobe Experience Cloud help. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>eVar 만료 - 왜 보고서에서 eVar의 특성이 '없음'으로 지정되고 있습니까? </p> </td> 
   <td colname="col3"> <p> <span class="uicontrol"> 유효 기간</span>은 eVar 값이 만료된 후 기간 또는 이벤트를 지정합니다(더 이상 성공 이벤트에 대한 크레디트를 받지 않음). 성공 이벤트가 eVar 만료 후 발생하는 경우 값이 해당 이벤트에 대한 크레딧을 받지 않습니다(eVar가 활성화되지 않았음). 이벤트를 만료 값으로 선택하면 이 이벤트가 발생하는 경우에만 해당 변수가 만료됩니다. 해당 이벤트가 발생하지 않으면 해당 변수가 만료되지 않습니다. <a href="https://marketing.adobe.com/resources/help/en_US/reference/conversion_var_admin.html" format="https" scope="external"> 자세히... </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>사용자 지정 이벤트 가시성 - 왜 [사용자 지정 이벤트]가 보고서 메뉴에 나타나지 않습니까? </p> </td> 
   <td colname="col3"> <p>가시성 열에서 표준(내장) 지표, 사용자 지정 이벤트, 내장 이벤트를 메뉴, 지표 선택기, 계산된 지표 빌더, 세그먼트 빌더에서 숨길 수 있습니다. 이 설정은 해당 지표 또는 이벤트의 데이터 수집에는 영향을 주지 않습니다. 사용자 인터페이스에서의 가시성에만 영향을 줍니다. <a href="https://marketing.adobe.com/resources/help/en_US/reference/metric-visibility.html" format="https" scope="external"> 자세히... </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>타임스탬프 - 타임스탬프 설정을 변수하기 전에 고려해야 할 사항은 무엇입니까? </p> </td> 
   <td colname="col3"> <p>타임스탬프 옵션 기능을 사용하면 데이터 손실을 발생시키지 않고도 타임스탬프가 지정되지 않은 데이터를 지정된 데이터와 결합할 수 있습니다. 모바일 장치에서 생성된 타임스탬프가 있는 오프라인 데이터는 웹 페이지에서 라이브의, 타임스탬프가 지정되지 않은 데이터와 결합하거나, 클라이언트측 타임스탬프 호출을 사용하여 모든 플랫폼의 데이터와 통합할 수 있습니다. <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/timestamps-overview.html" format="https" scope="external"> 자세히... </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>방문자 ID - 방문자 ID 유예 기간은 어떻게 작동하고, 어떻게 활성화됩니까? </p> </td> 
   <td colname="col3"> <p>동일한 보고서 세트에 데이터를 전송 중인 JavaScript 파일이 여러 개 있거나 사이트에서 Flash 비디오 측정과 같은 기타 기술을 사용하는 경우에는 유예 기간을 구성하는 것이 좋습니다. <a href="https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid_grace_period.html" format="https" scope="external"> 자세히... </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>방문자 ID - Experience Cloud 방문자 ID와 Analytics 방문자 ID의 차이점은 무엇입니까? </p> </td> 
   <td colname="col3"> <p>ID 서비스는 모든 사이트 방문자에게 고유한 영구 식별자를 할당합니다. 이 ID를 사용하면 방문자 및 해당 데이터를 Experience Cloud의 여러 다른 솔루션 간에 공유할 수 있습니다. 또한, 이 ID는 Analytics 방문자 ID와 같은 솔루션에서 사용하는 ID로 대체되거나 이러한 ID와 사용할 수 있습니다. <a href="https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-overview.html" format="https" scope="external"> 자세히... </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>방문자 ID - 쿠키가 차단된 경우 방문자 ID는 어떻게 설정됩니까? </p> </td> 
   <td colname="col3"> <p>표준 s_vi 쿠키를 사용할 수 없을 경우, 무작위로 생성된 고유 ID를 사용하는 대체 쿠키가 웹 사이트의 도메인에 만들어집니다. s_fid라는 이 쿠키는 2년 동안 사용할 수 있으며 앞으로 식별 대비책으로 사용됩니다. <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/visid_fallback.html" format="https" scope="external"> 자세히... </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>다이내믹 태그 관리 - 내 DTM 규칙이 실행되지 않는 이유는 무엇입니까? </p> </td> 
   <td colname="col3"> <p>이벤트 기반 규칙이 실행되지 않는다면 선택기나 규칙의 조건에 문제가 있을 수 있습니다. 원하는 이벤트 작업이 발생하는 사이트에서 요소를 찾아 마우스 오른쪽 단추를 클릭하고 요소 검사를 선택하십시오. 열려 있는 상자에서 강조 표시된 스크립트를 검사하고 올바른 요소를 타깃팅하고 있는지 확인하십시오. <a href="https://marketing.adobe.com/resources/help/en_US/dtm/c_Troubleshooting.html" format="https" scope="external"> 자세히... </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>하트비트 비디오 추적은 어떻게 구현합니까? </p> </td> 
   <td colname="col3"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/hbvideo/" format="https" scope="external"> 이 섹션</a>에는 사용자의 플랫폼을 위한 비디오 하트비트 SDK 및 개발자 안내서를 다운로드하는 방법이 들어 있습니다. SDK를 다운로드할 때에는 docs 폴더에 있는 개발자 안내서도 다운로드하십시오. 비디오 하트비트에 대한 구체적인 구현 지침이 들어 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>쿠키를 올바른 하위 도메인에 추가하려면 어떻게 합니까? </p> </td> 
   <td colname="col3"> <span class="varname"> Cookiedomainperiods </span> 변수는 페이지 URL의 도메인에서 점의 수를 파악하여 Analytics 쿠키 s_ cc 및 s_ sq가 설정되는 도메인을 결정합니다. 이 변수는 일부 플러그인에서 플러그인의 쿠키를 설정할 올바른 도메인을 결정할 때 사용하기도 합니다. [구성 변수] (/help/implement/js-implementation/c-variables/configuration-variables. md 참조) </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>추적 서버 - 추적 서버는 어떻게 올바로 채웁니까? </p> </td> 
   <td colname="col3"> <p>데이터를 Adobe Analytics 서버에 보내도록 구현을 구성할 때에는 올바른 위치에 보내야 합니다. 그렇게 하지 않으면 방문자 계산이 인플레이션되거나 데이터가 손실이 발생합니다. <a href="https://helpx.adobe.com/analytics/kb/determining-data-center.html" format="https" scope="external"> 자세히... </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>성능 - 인터넷 연결, 프록시, 방화벽 또는 Adobe에서의 서비스 중단으로 인한 외부 Adobe JavaScript 로드 실패가 성능에 영향을 줄 수 있습니까? </p> </td> 
   <td colname="col3"> <p>아닙니다. JavaScript 파일은 Adobe 서버에서 호스트되지 않으므로 Adobe 중단은 JavaScript 실행에 영향을 주지 않습니다. 다이내믹 태그 관리가 적용되는 경우, JavaScript 파일은 Akamai에 의해 호스트되거나, 고객이 결정한 서버 위치에서 호스트됩니다. </p> <p><i>다이내믹 태그 관리를 사용하면 웹 사이트 성능이 저하됩니까?</i>(<a href="https://marketing.adobe.com/resources/help/en_US/dtm/faq.html" format="https" scope="external">다이내믹 태그 관리 FAQ</a>)를 참조하십시오. </p> <p>또한, Akamai의 CDN에 의존하는 것이 불안할 경우, 자신의 핵심 다이내믹 태그 관리 파일을 호스트할 수 있습니다. <a href="https://marketing.adobe.com/resources/help/en_US/dtm/?f=deployment" format="https" scope="external">포함 코드 및 호스트 옵션</a>을 참조하십시오 . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>성능 - 외부 Adobe JavaScript의 로드로 성능이 저하될 수 있습니까? </p> </td> 
   <td colname="col3"> <p> JavaScript 파일은 처음에 로드된 후 방문자의 브라우저에 캐싱되며 일반적으로 세션당 한 번 이상 다운로드되지 않습니다. 이 파일은 사이트의 모든 페이지에서 사용되더라도 각 페이지에서 다운로드되지 않습니다. 대부분의 웹 사이트에서 사용자는 평균적으로 세션당 여러 번 페이지를 보기 때문에 여러 번 사용되는 JavaScript를 이 파일로 전송하면 다운로드되는 전체 데이터가 줄어들 수 있습니다. </p> <p> JavaScript 용 JavaScript! DNL appmeasurement] 압축: Adobe의 JavaScript 클라이언트의 페이지 무게 (크기) 가 걱정되는 경우에는 GZIP를 사용하여 파일을 압축하는 것이 좋습니다. GZIP은 모든 주요 브라우저에서 지원되며, JavaScript 압축보다 나은 성능을 제공하여 코어 <span class="filepath">s_code.js</span> JavaScript 파일을 압축 및 압축 해제할 수 있도록 해줍니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>성능 - 데이터를 브라우저에서 Adobe 서비스로 보내면 성능이 저하될 수 있습니까? </p> </td> 
   <td colname="col3"> <p> Adobe JavaScript 파일은 HTML 페이지 내에 이미지 개체를 만들며, 그렇게 되면 브라우저가 Adobe 서버의 이미지 개체를 요청합니다. Adobe 서버가 느려지거나 응답을 하지 않으면, 이미지가 반환되거나, 시간 초과가 발생할 때까지 해당 요청을 처리하는 스레드가 지연됩니다. 브라우저는 여러 스레드로 이미지를 처리하고, Adobe 중단이 페이지 로드 시간에 미치는 영향은 매우 작으므로, 다른 스레드가 계속 작동하는 동안 한 스레드를 연결 중입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>성능 - Adobe의 JavaScript 이벤트가 시스템 동작이나 기능에 영향을 줄 수 있습니까? </p> </td> 
   <td colname="col3"> <p>아닙니다. 앞의 성능 답변을 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> 자체적으로 정의한 조건을 기반으로 수집한 데이터를 변경하는 방법은 무엇입니까? </td> 
   <td colname="col3"> 처리 규칙을 사용하여 보고에 전송한 대로 데이터 컬렉션을 간소화하고 컨텐츠를 관리합니다. <a href="https://marketing.adobe.com/resources/help/en_US/reference/processing_rules.html" format="https" scope="external"> 추가 정보 </a> </td> 
  </tr> 
  <tr> 
   <td> s_code 파일의 최신 버전은 무엇입니까? </td> 
   <td> This section contains a release history for [! DNL appmeasurement] 라이브러리를 참조하십시오. 각 라이브러리의 최신 버전은 [보고 및 분석] &gt; [관리 도구] &gt; [코드 관리자]에서 다운로드할 수 있습니다. <a href="https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/release/?f=c_release_notes_javascript" format="http" scope="external"> 추가 정보 </a> </td> 
  </tr> 
  <tr> 
   <td> s_code 파일은 어떻게 디버깅합니까? </td> 
   <td> Adobe Debugger(이전 DigitalPulse Debugger)는 특정 페이지에서 수집되는 데이터를 볼 수 있도록 Adobe에서 제공하는 무료 도구입니다. <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=debugger" format="http" scope="external"> 추가 정보 </a> </td> 
  </tr> 
  <tr> 
   <td> 다른 링크 유형을 어떻게 추적합니까? </td> 
   <td> JavaScript용 AppMeasurement 파일에 설정된 매개 변수를 기반으로 파일 다운로드 및 종료 링크를 자동으로 추적할 수 있습니다. <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=function_tl" format="http" scope="external"> 추가 정보 </a> </td> 
  </tr> 
  <tr> 
   <td> 비디오를 어떻게 추적합니까? </td> 
   <td> JavaScript를 사용하여 광범위한 플레이어를 추적할 수 있습니다. JavaScript를 사용하여 추적하려면, 플레이어가 들어 있는 웹 페이지에 코드를 추가하고 이벤트 핸들러를 사용하여 플레이어를 추적합니다. <a href="https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/video/?f=video_js" format="http" scope="external"> 추가 정보 </a> </td> 
  </tr> 
  <tr> 
   <td> 모바일 앱을 어떻게 추적합니까? </td> 
   <td> Adobe Mobile Services에서 고유한 추적 코드가 있는 획득 링크를 생성할 수 있습니다. 사용자가 생성된 링크를 클릭한 후 Apple App Store에서 앱을 다운로드하여 실행하면, SDK에서는 자동으로 획득 데이터를 수집하여 Adobe Mobile Services로 보냅니다. <a href="https://marketing.adobe.com/resources/help/en_US/mobile/ios/?f=acquisition" format="http" scope="external"> iOS</a> <a href="https://marketing.adobe.com/resources/help/en_US/mobile/android/?f=acquisition" format="http" scope="external">Android </a> </td> 
  </tr> 
  <tr> 
   <td> 비디오 추적은 어떻게 구현합니까? </td> 
   <td> 비디오 플레이어 이벤트 핸들러에 연결된 기능을 만들어 미디어 플레이어를 추적할 수 있습니다. 이 방법에서는 적절한 때에 Media.open, Media.play, Media.stop 및 Media.close를 호출할 수 있습니다. <a href="https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/video/?f=video_js_events" format="http" scope="external"> 추가 정보 </a> </td> 
  </tr> 
  <tr> 
   <td> 자사 쿠키를 설정하려면 어떻게 합니까? </td> 
   <td> Analytics는 쿠키를 사용하여 이미지 요청과 브라우저 세션 간에 지속되지 않는 변수 및 구성 요소에 대한 정보를 제공합니다. 이러한 무해 쿠키는 Adobe에서 호스트하는 도메인에서 생성되는 것으로, 타사 쿠키로 알려져 있습니다. <a href="https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/?f=fpcookies_cert" format="http" scope="external"> 추가 정보 </a> </td> 
  </tr> 
  <tr> 
   <td> SSL 인증서를 가져오려면 어떻게 합니까? </td> 
   <td> 사이트에서 https:// 프로토콜을 사용하는지 판별합니다. 그런 경우, CSR을 요청하고 SSL 인증서를 구입해야 합니다. 참고: 보안 페이지 또는 컨텐츠가 없는 경우 SSL 인증서가 필요하지 않습니다. 사이트에서 https:// 프로토콜만 사용하는 경우 이 전체 단계를 건너뛸 수 있습니다. <a href="https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/?f=fpcookies_cert" format="http" scope="external"> 추가 정보 </a> </td> 
  </tr> 
  <tr> 
   <td> 인증 만료 알림에 대한 정보는 어디에서 찾을 수 있습니까? </td> 
   <td> SSL 인증서는 매년 만료됩니다. 즉, 만료가 될 때마다 Adobe에 업데이트된 인증서를 요청해야 합니다. 이 경우 FPC 전문가가 충분히 경고를 하지만, 미리 만료를 모니터링하고 Adobe에 업데이트된 이 인증서를 제공하는 것이 좋습니다. <a href="https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/?f=fpcookies_renewals" format="http" scope="external"> 추가 정보 </a> </td> 
  </tr> 
  <tr> 
   <td> 플러그인이란 무엇입니까? </td> 
   <td> JavaScript용 AppMeasurement 플러그인은 몇 가지 고급 기능을 수행하는 프로그램 또는 기능입니다. 이러한 플러그인은 JavaScript의 기능을 확장함으로써, 기본 구현으로는 사용할 수 없는 기능들을 브라우저에서 사용할 수 있도록 해줍니다. Adobe에서는 고급 솔루션의 일부로서 다른 플러그인도 많이 제공하고 있습니다. JavaScript를 사용하여 데이터를 캡처하고 싶지만 진행하는 방법을 모르는 경우에는 담당 계정 관리자에게 문의하십시오. <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=impl_plugins" format="http" scope="external"> 추가 정보 </a> </td> 
  </tr> 
  <tr> 
   <td> 데이터 삽입 API에 대한 정보? </td> 
   <td> Adobe는 Analytics에 데이터를 보낼 수 있는 여러 가지 방법을 개발했습니다. <a href="https://marketing.adobe.com/resources/help/en_US/reference/?f=usecase_sending_data_to_sc" format="http" scope="external"> 추가 정보 </a> </td> 
  </tr> 
  <tr> 
   <td> 500 오류란? </td> 
   <td> "500 쿼리 오류" 상태를 초래한 내부 서버 오류에 대한 정보. <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=pageType" format="http" scope="external">Pagetype 변수 참조 </a> </td> 
  </tr> 
 </tbody> 
</table>

