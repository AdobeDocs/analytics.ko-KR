---
description: Silverpop 용 데이터 커넥터 통합은 Analytics 변수를 사용하여 다양한 Silverpop 지표를 추적합니다.
seo-description: Silverpop 용 데이터 커넥터 통합은 Analytics 변수를 사용하여 다양한 Silverpop 지표를 추적합니다.
seo-title: Analytics 통합 변수
title: Analytics 통합 변수
uuid: 3 aef 3 caf-e 24 e -4 fe 7-b 4 d 7-50 ca 0 f 6703 b 5
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# Analytics Integration Variables{#analytics-integration-variables}

Silverpop 용 데이터 커넥터 통합은 Analytics 변수를 사용하여 다양한 Silverpop 지표를 추적합니다.

Silverpop 통합과 함께 사용할 이벤트와 evar를 확인한 후 Adobe Analytics 관리 콘솔을 사용하여 이를 활성화합니다 ( [보고서 세트](http://microsite.omniture.com/t2/help/en_US/reference/index.html?f=report_suites_admin)참조).

다음 표에서는 Silverpop 통합에 필요한 Analytics 변수에 대해 설명합니다.

## 필수 변수 {#section-3ca8dc46bab0436cba0c9ef827c8356a}

| 변수 유형 | 이름 | 채우기 방법 | 설명 |
|---|---|---|---|
| 이벤트 (숫자) | 바운스 수 | 실버팝에서 자동으로 가져옵니다. | 바운스 이벤트는 배달 문제로 인해 수신자에게 배달되지 않은 이메일 메시지 수를 볼 수 있도록 해줍니다. |
| 이벤트 (숫자) | 클릭 수 | 실버팝에서 자동으로 가져옵니다. | 클릭한 이벤트를 통해 이메일 메시지를 클릭한 방문자 수를 확인할 수 있습니다. |
| 이벤트 (숫자) | opens | 실버팝에서 자동으로 가져옵니다. | 열린 이벤트를 통해 이메일 메시지를 연 방문자 수를 볼 수 있습니다. |
| 이벤트 (숫자) | send | 실버팝에서 자동으로 가져옵니다. | 보내기 이벤트를 사용하면 전송된 이메일 메시지 수를 볼 수 있습니다. |
| 이벤트 (숫자) | 가입 해지 | 실버팝에서 자동으로 가져옵니다. | 가입 취소된 이벤트는 이메일 메시지를 연 다음, 조직의 향후 이메일 메시지를 옵트아웃하는 구독 취소 링크를 클릭한 방문자 수를 볼 수 있도록 해줍니다. |
| eVar | Silverpop ID/방문자 ID | 자동 수집 방법 또는 JavaScript 플러그인을 통해 이메일 링크의 쿼리 매개 변수에서 수집되었습니다. | 고유 방문자 ID |
| Evar 또는 s. campaign | 메일링 ID | 자동 수집 방법 또는 JavaScript 플러그인을 통해 이메일 링크의 쿼리 매개 변수에서 수집되었습니다. | 종종 캠페인 변수에 저장됩니다. |

## 옵션 변수 {#section-5f0a32b0a2084c87a64b5f90c0d0fb53}

| 변수 유형 | 이름 | 채우기 방법 | 설명 |
|---|---|---|---|
| 이벤트 (카운터) | 다운로드한 파일 | Analytics 태그를 통해 수동으로 수집됩니다. | 이 이벤트는 사이트에서 파일을 다운로드한 사용자를 식별하는 데 사용됩니다. |
| 이벤트 (카운터) | 양식 시작 | Analytics 태그를 통해 수동으로 수집됩니다. | 시작된 양식은 양식을 시작한 사용자를 식별하는 데 사용됩니다. |
| 이벤트 (카운터) | 양식 작성됨 | Analytics 태그를 통해 수동으로 수집됩니다. | 완료된 양식은 양식을 시작하고 완료하지 않은 방문자를 식별하는 데 사용됩니다. |
| eVar | Email Address | Analytics 태그를 통해 수동으로 수집됩니다. | 이메일 주소는 등록, 로그인 또는 이메일 주소가 수집되는 기타 페이지에서 이메일 주소를 수동으로 수집하는 데 사용됩니다. 이 변수는 이메일을 받도록 선택한 사용자에게 리마케팅하는 데 사용되며 이전에 이메일을 클릭했을 수 없습니다. |
| eVar | 다운로드한 파일 | Analytics 태그를 통해 수동으로 수집됩니다. | 다운로드한 파일은 방문자가 다운로드한 파일을 식별합니다. |
| eVar | 양식 이름 | Analytics 태그를 통해 수동으로 수집됩니다. | 양식 이름은 방문자가 포기한 양식을 식별합니다. |

