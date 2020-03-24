---
description: Silverpop용 Data Connectors 통합은 Analytics 변수를 사용하여 다양한 Silverpop 지표를 추적합니다.
title: Analytics 통합 변수
uuid: 3aef3caf-e24e-4fe7-b4d7-50ca0f6703b5
translation-type: ht
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Analytics 통합 변수{#analytics-integration-variables}

Silverpop용 Data Connectors 통합은 Analytics 변수를 사용하여 다양한 Silverpop 지표를 추적합니다.

Silverpop 통합에 사용할 이벤트 및 eVar를 식별한 후 Adobe Analytics 관리 콘솔을 사용하여 활성화하십시오([보고서 세트](https://docs.adobe.com/content/help/ko-KR/analytics/admin/manage-report-suites/report-suites-admin.html) 참조).

아래 표는 Silverpop 통합에 필요한 Analytics 변수를 설명합니다.

## 필수 변수 {#section-3ca8dc46bab0436cba0c9ef827c8356a}

| 변수 유형 |  이름  | 채우기 방법 | 설명 |
|---|---|---|---|
| event (numeric) | 바운스 수 | Silverpop에서 자동으로 가져옵니다. | 바운스 이벤트를 사용하면 배달 문제로 인해 수신자에게 배달되지 않은 이메일 메시지 수를 볼 수 있습니다. |
| event (numeric) | 클릭 수 | Silverpop에서 자동으로 가져옵니다. | 클릭됨 이벤트를 사용하면 이메일 메시지를 클릭한 방문자 수를 볼 수 있습니다. |
| event (numeric) | 열림 | Silverpop에서 자동으로 가져옵니다. | 열림 이벤트를 사용하면 이메일 메시지를 연 방문자 수를 볼 수 있습니다. |
| event (numeric) | 전송함 | Silverpop에서 자동으로 가져옵니다. | 전송함 이벤트를 사용하여 전송된 이메일 메시지 수를 볼 수 있습니다. |
| event (numeric) | 가입 해지됨 | Silverpop에서 자동으로 가져옵니다. | 가입 해지됨 이벤트를 사용하면 이메일 메시지를 열었지만 나중에 가입 해지 링크를 클릭하여 조직에서 발송하는 향후 이메일 메시지를 거부한 방문자 수를 볼 수 있습니다. |
| eVar | Silverpop ID/방문자 ID | 자동화된 수집 방법 또는 JavaScript 플러그인을 통해 이메일 링크의 쿼리 매개 변수에서 수집됩니다. | 고유 방문자 ID |
| eVar 또는 s.campaign | 메일링 ID | 자동화된 수집 방법 또는 JavaScript 플러그인을 통해 이메일 링크의 쿼리 매개 변수에서 수집됩니다. | 캠페인 변수에 저장되는 경우가 많습니다. |

## 옵션 변수 {#section-5f0a32b0a2084c87a64b5f90c0d0fb53}

| 변수 유형 |  이름  | 채우기 방법 | 설명 |
|---|---|---|---|
| event (counter) | 파일 다운로드됨 | Analytics 태그를 통해 수동으로 수집합니다. | 이 이벤트는 사이트에서 파일을 다운로드한 사용자를 식별하는 데 사용됩니다. |
| event (counter) | 양식 시작됨 | Analytics 태그를 통해 수동으로 수집합니다. | 양식 시작됨은 양식을 시작하지만 완료하지 않은 사용자를 식별하는 데 사용됩니다. |
| event (counter) | 양식 완료됨 | Analytics 태그를 통해 수동으로 수집합니다. | 양식 완료됨은 양식을 시작하고 완료하지 않은 방문자를 식별하는 데 사용됩니다. |
| eVar | 이메일 주소 | Analytics 태그를 통해 수동으로 수집합니다. | 이메일 주소는 가입, 로그인 또는 이메일 주소가 수집된 다른 페이지에서 이메일 주소를 수동으로 수집하기 위한 것입니다. 이 변수는 이메일 수신을 선택했지만 과거에 수신한 이메일을 아직 클릭하지 않은 사용자를 리마케팅하는 데 사용됩니다. |
| eVar | 다운로드한 파일 | Analytics 태그를 통해 수동으로 수집합니다. | 다운로드한 파일은 방문자가 다운로드한 파일을 식별합니다. |
| eVar | 양식 이름 | Analytics 태그를 통해 수동으로 수집합니다. | 양식 이름은 방문자가 포기한 양식을 식별합니다. |

