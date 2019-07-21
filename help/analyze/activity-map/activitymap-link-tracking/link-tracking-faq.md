---
description: Activity Map에서의 링크 추적에 대한 FAQ.
seo-description: Activity Map에서의 링크 추적에 대한 FAQ.
seo-title: 링크 추적 FAQ
solution: Analytics
title: 링크 추적 FAQ
topic: Activity Map
uuid: 10172073-B 98 B -4950-8397-67 A 18 B 37 B 3 B 4
translation-type: tm+mt
source-git-commit: d877f86dd5a05d0aa452ecebce47468ebf94cbb2

---


# 링크 추적 FAQ

Activity Map에서의 링크 추적에 대한 FAQ.

>[!CAUTION]
>
>By turning on Activity Map tracking, **you may be** **collecting personally identifiable information (PII) data.** This data can be used on its own or with other information to identify, contact, or locate a single person, or to identify an individual in context.

다음은 Activity Map 추적을 사용하여 PII 데이터를 수집할 수 있는 알려진 몇 가지 경우입니다.

* `Mailto` 링크를 참조하십시오. mailto 링크는 이메일을 보내기 위해 컴퓨터에서 기본 메일 클라이언트를 활성화하는 HTML 링크의 유형입니다.
* `User ID` 사용자가 로그인하면 웹 사이트의 머리글과 바닥글에 나타날 수 있는 링크입니다.
* 금융 기관의 경우 계정 번호가 링크로 표시될 수 있습니다. 클릭하면 링크의 텍스트가 수집됩니다.
* Healthcare 웹 사이트에는 링크로 표시된 PII 데이터가 있을 수 있습니다. 이러한 링크를 클릭하면 링크의 텍스트를 수집하므로 PII 데이터가 수집됩니다.

<table id="table_0951EAC617344156BAE43000CCD838AF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <b>Q: 언제 링크 추적이 발생합니까?</b> <p> </p> </td> 
   <td colname="col2"> A: Activity Map 링크 및 영역 식별은 사용자가 페이지를 클릭하면 수행됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Q: 기본적으로 추적되는 항목은 무엇입니까?</b> <p> </p> </td> 
   <td colname="col2"> A: 요소에서 클릭 이벤트가 발생하면, 요소는 확인 사항을 전달하여 AppMeasurement에서 이것이 링크로 처리하는지 여부를 판단해야 합니다. 확인 사항은 다음과 같습니다. 
    <ul id="ul_81B9A5A7F8534E71AEF68F2199A154F0"> 
     <li id="li_49F6DDD9DC124AE5846EC5B7D7BEA20E">이것은 HREF 속성이 있는 &lt;A&gt; 또는 &lt;AREA&gt; 태그입니까? </li> 
     <li id="li_77828D24D54343E5B9A1FF7345221781">s_objectID 변수를 설정하는 클릭 속성이 있습니까? </li> 
     <li id="li_D4B0AEEEA58A4F82A1BCBD3971A60D02">이것은 값 또는 하위 텍스트가 있는 INPUT 태그 또는 SUBMIT 단추입니까? </li> 
     <li id="li_F7ABE88308E1413E9B9C2224DEC91BAB">이것은 유형 IMAGE 및 src 속성이 있는 INPUT 태그입니까? </li> 
     <li id="li_F34A0C986E8040109A1DDF88C26E56D5">이것은 &lt;Button&gt;입니까? </li> 
    </ul> <p>위의 질문 중 하나라도 답이 <b>예</b>이면, 요소가 링크로 처리되고 추적됩니다. </p> <p>중요: 속성 유형이 "button"인 단추 태그는 AppMeasurement에서 링크로 간주되지 않습니다. 단추 태그에서 "type='button'"을 제거하고 role="button" 또는 submit="button"을 대신 추가합니다. </p> <p>중요: " # "로 시작하는 HREF가 있는 앵커 태그는 페이지를 떠나지 않기 때문에 링크가 아닌 appmeasurement 별로 내부 대상 위치로 간주됩니다. 기본적으로 Activity Map는 이러한 내부 대상 위치를 추적하지 않습니다. 사용자를 새 페이지로 이동시키는 링크만 추적합니다.</p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Q: Activity Map은 어떻게 다른 시각적 HTML 요소를 추적합니까?</b> </td> 
   <td colname="col2"> 
    <ol id="ol_DA3AED165CFF44B08DFB386D4DEE26C5"> 
     <li id="li_E3E3F498F37B4FADAFDA39CCAE41511F"> <b><code>s.tl()</code> 함수 사용</b> <p>s.tl 호출을 통해 클릭이 발생하면, Activity Map에서는 이 클릭 이벤트를 받고 linkName 문자열 변수가 발견되었는지 판단하게 됩니다. s.tl을 실행하는 동안, 해당 linkName은 Activity Map 링크 ID로 설정됩니다. s.tl() 호출을 발생시킨 클릭 요소는 영역을 결정하는 데 사용됩니다. 예: </p> <p> 
       <code>&lt; img &amp; amp; nbsp; onclick = "s. tl (true,' o ',' abc ')" &amp; amp; nbsp; src = "someimageurl. png"/&gt; </code>
  </p> </li> 
     <li id="li_A93725B810FE408BA5E6B267CF8CEAE5"> <b><code>s_objectID</code> 변수 사용</b> <p>예: </p> <p> 
       <code>&lt; img onclick = "s_ objectid =' abc '; " src = "someimageurl. png"/&gt; &lt; a href = "some-url.html" onclick = "s_ objectid =' abc '; " &gt; Link text here &lt;/a &gt; </code>
  </p> <p>중요: Activity Map에서 s_objectID를 사용할 때에는 끝에 추가하는 세미콜론(;)이 있어야 합니다. </p> </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Q: 추적되는 링크의 예를 제공할 수 있습니까?</b> </td> 
   <td colname="col2"> 
    <ol id="ol_697E5CE0B84D4A309DD80670697A02BA"> 
     <li id="li_2C511EFD10F14F438B1F3A1BAB4B45E0"> 
      <code>&lt; a &amp; amp; nbsp; href = "/home" &gt; home &lt;/a &gt; </code>
  </li> 
     <li id="li_76F3DB36ED734132A2386871E6EB4929"> 
      <code>&lt; input &amp; amp; nbsp; type = "submit" &amp; amp; nbsp; value = "submit"/&gt; </code>
  </li> 
     <li id="li_10CF9EDA224645169E7CDF74956DB98B"> 
      <code>&lt; input &amp; amp; nbsp; type = "image" &amp; amp; nbsp; src = "submit-button. png"/&gt; </code>
  </li> 
     <li id="li_9FA171D7F49547E798DE21869F73A402"> 
      <code>&lt; p onclick = "var s_ objectid =' custom link id '; " &gt; &lt; span class = "title" &gt; 현재 시장 비율 &lt;/span &gt; &lt; span class = "subtitle" &gt; 1.45 USD &lt;/span &gt; &lt;/p &gt; </code>
  </li> 
     <li id="li_C5D77589006E4514AA6F3AEB509A0BAF"> 
      <code>&lt; div onclick = "s. tl (true,' o ',' custom link id ')" &gt; &lt; span class = "title" &gt; 현재 시장 비율 &lt;/span &gt; &lt; span class = "subtitle" &gt; 1.45 usd &lt;/span &gt; &lt;/div &gt; </code>
  </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Q: 추적되지 않는 링크의 예를 제공할 수 있습니까?</b> </td> 
   <td colname="col2"> 
    <ol id="ol_CDFDB572F76B4F68A64B66A6B0237547"> 
     <li id="li_99372060646B43EF94C13A9C682CE693">이유: 앵커 태그에 올바른 href가 없습니다. 
      <code>&lt; a &amp; amp; nbsp; name = "inneranchor" &gt; section &amp; amp; nbsp; header &lt;/a &gt; </code>
  </li> 
     <li id="li_736A5F7DC2D74B4DA1CECEE3AD10EB19">Reason: Neither <code> s_ObjectID </code> nor <code> s.tl() </code> present 
      <code>
        &lt;p onclick="showPanel('market rates')"&gt;     &lt;span class="title"&gt;Current Market Rates&lt;/span&gt;&lt;span  class="subtitle"&gt;1.45USD&lt;/span&gt; &lt;/p&gt;
      </code> </li> 
     <li id="li_45F9ED97140F47F99F8C167BC1DC546F">Reason: Neither <code> s_ObjectID </code> nor <code> s.tl() </code> present 
      <code>
        &lt;input type="radio" onclick="changeState(this)" name="group1" value="A"/&gt; &lt;input type="radio" onclick="changeState(this)" name="group1" value="B"/&gt; &lt;input type="radio" onclick="changeState(this)" name="group1" value="C"/&gt;
      </code> </li> 
     <li id="li_9EBFCC58F3A94F30BA62156F14B15D55">Reason: src property is missing a form input element 
      <code>
        &lt;input&amp;nbsp;type="image"/&gt; 
      </code> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

