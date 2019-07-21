---
description: 테이블을 조회하여 page_event 값을 기준으로 히트의 유형을 파악하십시오.
keywords: 데이터 피드; page; 이벤트; page_ event; post_ page_ event
seo-description: 테이블을 조회하여 page_event 값을 기준으로 히트의 유형을 파악하십시오.
seo-title: 페이지 이벤트 조회
solution: Analytics
title: 페이지 이벤트 조회
topic: Reports & Analytics
uuid: 73 AF 597 C -5560-466 E -94 B 2-DDD 1 D 64797 C 8
translation-type: tm+mt
source-git-commit: 01a6fc7e44dc71b868bd38a4f6a5a4089eae6349

---


# 페이지 이벤트 조회

테이블을 조회하여 page_event 값을 기준으로 히트의 유형을 파악하십시오.

<table id="table_33AF375E0B41474696D7A4A92C652A5F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 히트 유형 </th> 
   <th colname="col02" class="entry"> page_event 값 </th> 
   <th colname="col2" class="entry"> post_page_event 값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 페이지 보기 횟수 </td> 
   <td colname="col02"> 게시물과 동일 </td> 
   <td colname="col2"> <p>모든 페이지 보기의 경우 0(<code>s.t()</code>개의 호출) </p> <p>모바일 SDK의 <code>trackState</code> 호출의 경우 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 링크 추적 </td> 
   <td colname="col02"> <p>"기타 링크"의 경우 10 </p> <p>모바일 SDK의 <code>trackAction</code> 및 라이프사이클 호출의 경우 10 </p> <p>"다운로드 링크"의 경우 11 </p> <p>"외부 또는 종료 링크"의 경우 12 </p> </td> 
   <td colname="col2"> <p>"기타 링크"의 경우 100 </p> <p>모바일 SDK의 <code>trackAction</code> 및 라이프사이클 호출의 경우 100 </p> <p>"다운로드 링크"의 경우 101 </p> <p>"외부 또는 종료 링크"의 경우 102 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이정표 비디오 </td> 
   <td colname="col02"> 
    <!--<p>30 - Legacy full media tracking event at the end of the video playback (no longer supported)</p>--> <p>31 - 미디어 시작 이벤트 </p> <p>32 - 미디어 업데이트 전용 이벤트 (Evar 또는 다른 변수 처리를 수행하지 않음) </p> <p>33 – 미디어 + 기타 변수 업데이트 이벤트(eVar 및 기타 변수 처리 포함) </p> </td> 
   <td colname="col2"> 
    <!--<p> 75 - Legacy full media tracking event at theend of the video playback (no longer supported)</p>--> <p> 76 - 미디어 시작 이벤트 </p> <p>77 – 미디어 업데이트 전용 이벤트(eVar 또는 다른 변수 처리를 수행하지 않음) </p> <p>78 – 미디어 + 기타 변수 업데이트 이벤트(eVar 및 기타 변수 처리 포함) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>하트비트 비디오 </p> </td> 
   <td colname="col02"> 게시물과 동일 </td> 
   <td colname="col2"> <p> 50 = (non-Primetime) 미디어 스트림 시작 </p> <p> 51 = (non-Primetime) 미디어 스트림 닫기(완료/마침) </p> <p> 52 = (non-Primetime) 미디어 스트림 스크러빙 </p> <p> 53 = (non-Primetime) 미디어 스트림 활성화 유지 </p> <p> 54 = (non-Primetime) 미디어 스트림 광고 시작 </p> <p> 55 = (non-Primetime) 미디어 스트림 광고 닫기(완료/마침) </p> <p> 56 = (non-Primetime) 미디어 스트림 광고 스크러빙 </p> <p> 60 = Primetime 미디어 스트림 시작 </p> <p> 61 = Primetime 미디어 스트림 닫기(완료/마침) </p> <p> 62 = Primetime 미디어 스트림 스크러빙 </p> <p> 63 = Primetime 미디어 스트림 활성화 유지 </p> <p> 64 = Primetime 미디어 스트림 광고 시작 </p> <p> 65 = Primetime 미디어 스트림 광고 닫기(완료/마침) </p> <p> 66 = Primetime 미디어 스트림 광고 스크러빙 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 설문 조사 </td> 
   <td colname="col02"> 40 </td> 
   <td colname="col2"> 80 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 타겟 분석 </td> 
   <td colname="col02"> 70 - 타겟 활동 데이터를 포함하는 히트를 나타냅니다. Analytics 호출과 연결된 히트 및 연결되지 않은 히트의 경우 70입니다. </td> 
   <td colname="col2"> </td> 
  </tr> 
 </tbody> 
</table>

