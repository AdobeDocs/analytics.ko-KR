---
description: 테이블을 조회하여 page_event 값을 기준으로 히트의 유형을 파악하십시오.
keywords: Data Feed;page;event;page_event;post_page_event
title: 페이지 이벤트 조회
topic: Reports and analytics
uuid: 73af597c-5560-466e-94b2-ddd1d64797c8
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# 페이지 이벤트 조회

테이블을 조회하여 page_event 값을 기준으로 히트의 유형을 파악하십시오.

| 히트 유형 | `page_event` 값 | `post_page_event` 값 |
| --- | --- | --- |
| 페이지 보기 횟수 | 0: 모바일 SDK의 모든 페이지 보기 호출 및 `trackState` 호출 | `post_page_event`와 동일한 값 |
| 링크 추적 | 10: 모바일 SDK의 사용자 지정 링크 및 `trackAction` 호출<br>11: 다운로드 링크<br>12: 종료 링크 | 100: 모바일 SDK의 사용자 지정 링크 및 `trackAction` 호출<br>101: 다운로드 링크<br>102: 종료 링크 |
| 이정표 비디오 | 31: 미디어 시작<br>32: 미디어 업데이트(다른 변수 처리 안 함)<br>33: 미디어 업데이트(다른 변수 포함) | 76: 미디어 시작<br>77: 미디어 업데이트(다른 변수 처리 안 함)<br>78: 미디어 업데이트(다른 변수 포함) |
| 하트비트 비디오 | 50: 미디어 스트림 시작(Primetime 제외)<br>51: 미디어 스트림 닫기(Primetime 제외)<br>52: 미디어 스트림 스크러빙(Primetime 제외)<br>53: 미디어 스트림 활성 상태 유지(Primetime 제외)<br>54: 미디어 스트림 광고 시작(Primetime 제외)<br>55: 미디어 스트림 광고 닫기(Primetime 제외)<br>56: 미디어 스트림 광고 스크러빙(Primetime 제외)<br>60: Primetime 미디어 스트림 시작<br>61: Primetime 미디어 스트림 닫기<br>62: Primetime 미디어 스트림 스크러빙<br>63: Primetime 미디어 스트림 활성 상태 유지<br>64: Primetime 미디어 스트림 광고 시작<br>65: Primetime 미디어 스트림 광고 닫기<br>66: Primetime 미디어 스트림 광고 스크러빙 | `post_page_event`와 동일한 값 |
| 설문 조사 | 40: 설문 조사에서 생성된 모든 호출 | 80: 설문 조사에서 생성된 모든 호출 |
| Target용 Analytics | 70: 히트에 Target 활동 데이터 포함 | `post_page_event`와 동일한 값 |
