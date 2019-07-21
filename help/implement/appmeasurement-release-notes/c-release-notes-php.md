---
description: 'null'
seo-description: 'null'
seo-title: PHP
solution: Analytics
subtopic: 릴리스 노트
title: PHP
topic: 개발자 및 구현
uuid: 65 A 644 EF -8 E 50-406 B -8 B 12-0582495 D 130 A
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# PHP{#php}

>[!NOTE]
>
>현재 라이브러리 버전을 찾으려면 디버그 로깅을 켭니다.

## 버전 1.2.2 {#section_0D547871DC684417B6CE1370E5C6AAC2}

릴리스 날짜: **2014년 8월**

* 예정된 기능을 지원하기 위한 내부 변경입니다.

## 버전 1.2.1 {#section_5717907F67AB482F860F1DFBCB4198C7}

릴리스 날짜: **2012년 7월**

* Added a check for the "off" returned for the $_SERVER['HTTPS'] in IIS. Without this check, typecasting to boolean ((bool)$_SERVER['HTTPS']) returned true in IE whether the request was made through HTTP or HTTPS. 이로 인해 비보안 페이지에서 보안 이미지 요청을 시도하게 되었습니다.

## 버전 1.1 {#section_8F4479681ED642FCB9233459E04FF702}

PHP 1.1용 Measurement Library에 버전 1.0의 다음 업데이트가 포함됩니다.

* 더 나은 지리 특성 정확도(`sendFromServer`가 활성화된 경우)
* 사용자가 이제 `userAgent` 변수에 추가될 수 있도록 버그를 수정했습니다.
* 이제 이미지 비콘이 더 많은 모바일 브라우저와 호환됩니다.
* 모바일이 활성화된 경우 `imageDimensions` 변수는 이제 기본적으로 5x5입니다.
* 보트 탐지 목록이 재정의되었습니다.
* `debugTracking` 및 `sendFromServer`가 활성화될 때 디버그 정보(HTTP 헤더, 응답, 오류 등)가 추가되었습니다.

* `debugFilename` 변수가 추가되었습니다 (활성화된 경우 `sendFromServer` ).

* The pagename variable defaults to `$_SERVER['SCRIPT_NAME']` when neither `pagename` nor `pageURL` are set.

* PHP의 CGI 구현에 대한 모든 지원
* 성능 향상.

