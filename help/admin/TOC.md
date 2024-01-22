---
product: analytics
audience: admin
user-guide-title: Analytics 관리 안내서
breadcrumb-title: 관리 안내서
user-guide-description: Experience Cloud Admin Console에서의 사용자 및 제품 관리, 보고서 세트 구성 등과 같은 Analytics 관리 작업에 대해 알아봅니다.
source-git-commit: 4545c3839586231918ba5ebbf17fcac5a366abab
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 94%

---


# Adobe Analytics 관리 안내서 {#admin}

+ [Analytics 관리 안내서](home.md)
+ [Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html?lang=ko-KR)
+ Adobe Admin Console {#admin-console}
   + [개요](admin-console/home.md)
   + [Adobe Analytics 첫 번째 관리 안내서](admin-console/first-admin-guide.md)
   + [Adobe Analytics의 관리자 역할](admin-console/admin-roles-in-analytics.md)
   + Analytics 도구 권한 요약 {#permissions}
      + [Adobe Analytics의 제품 프로필](admin-console/permissions/product-profile.md)
      + [보고서 세트 도구에 대한 제품 프로필 권한](admin-console/permissions/report-suite-tools.md)
      + [Analytics 도구에 대한 제품 프로필 권한](admin-console/permissions/analytics-tools.md)
+ Analytics 관리 도구 {#admin-tools}
   + [관리 도구 개요](admin/c-admin-tools.md)
   + [코드 관리자](admin/code-manager-admin.md)
   + [데이터 소스](admin/data-sources.md)
   + [IP 주소로 제외](admin/exclude-ip.md)
   + [로그](admin/logs.md)
   + 활동 관리자 보고 {#reporting-activity-manager}
      + [개요](admin/reporting-activity-manager/reporting-activity-overview.md)
      + [보고 활동 보기](admin//reporting-activity-manager/reporting-activity.md)
      + [보고 요청 취소](admin/reporting-activity-manager/reporting-activity-cancel-requests.md)
   + 구성 요소 마이그레이션 {#component-migration}
      + [마이그레이션 준비](admin/component-migration/prepare-component-migration.md)
      + [마이그레이션 워크플로](admin/component-migration/component-migration.md)
   + 보고서 세트 관리자 {#manage-report-suites}
      + 보고서 세트의 설정 편집 {#edit-report-suite}
         + 일반 {#report-suite-general}
            + [일반 계정 설정](admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md)
            + [내부 URL 필터](admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md)
            + [사용자 정의 달력](admin/c-manage-report-suites/c-edit-report-suites/general/custom-calendar.md)
            + 유료 검색 감지 {#paid-search-detection}
               + [유료 검색 감지 개요](admin/c-manage-report-suites/c-edit-report-suites/general/paid-search-detection/paid-search-detection.md)
               + [유료 검색 감지 구성](admin/c-manage-report-suites/c-edit-report-suites/general/paid-search-detection/t-paid-search-detection.md)
            + 처리 규칙 {#c-processing-rules}
               + [처리 규칙 개요](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md)
               + 처리 규칙 {#c-processing-rules-configuration}
                  + [처리 규칙 작동 방식](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/c-processing-rules-configuration/processing-rules-about.md)
                  + [처리 규칙 만들기](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.md)
                  + [활성 처리 규칙 보기](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/c-processing-rules-configuration/t-processing-rules-view.md)
                  + [처리 규칙 내역 보기](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/c-processing-rules-configuration/t-processing-rule-view-history.md)
                  + [처리 규칙 복원](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/c-processing-rules-configuration/t-processing-rules-restore.md)
                  + [다른 보고서 세트에 처리 규칙 복사](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/c-processing-rules-configuration/t-processing-rules-copy-to-rs.md)
                  + [처리 규칙에 사용 가능한 차원](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rule-dimensions.md)
               + 처리 규칙 예 {#processing-rules-examples}
                  + [처리 규칙 예](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-examples.md)
                  + [쿼리 문자열 매개변수에서 캠페인 ID 채우기](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-populate-campaign-id.md)
                  + [제품 개요 페이지에서 제품 보기 이벤트 설정](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/setting-the-product-view-event.md)
                  + [범주와 페이지 이름을 연결하여 하위 범주 추가](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/subcategory-concatenating.md)
                  + [eVar 값을 prop에 복사하여 경로 결정](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-determining-path.md)
                  + [보고서에서 값 정리](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/clean-up-values-in-a-report.md)
                  + [쿼리 문자열 매개변수를 사용하여 내부 검색어 채우기](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-populating-internal-search.md)
                  + [eVar에 컨텍스트 데이터 변수 복사](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md)
                  + [컨텍스트 데이터 변수를 사용하여 이벤트 설정](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data-event.md)
                  + [히트에서 이벤트 제거](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-remove-event.md)
               + [처리 규칙 팁과 트릭](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-tips.md)
            + 보트 규칙 {#bot-removal}
               + [보트 제거](admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-removal.md)
               + [보트 규칙 이해 및 구성](admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md)
               + [일반 보트 서명](admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-signatures.md)
               + [보트 제외 방법](admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-exclusion-methods.md)
            + [개인정보 보호 설정](admin/c-manage-report-suites/c-edit-report-suites/general/privacy-settings.md)
            + [타임스탬프 구성](admin/c-manage-report-suites/c-edit-report-suites/general/timestamp-optional.md)
            + 서버측 전달 {#server-side-forwarding}
               + [서버측 전달 개요](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf.md)
               + [GDPR/ePrivacy 준수 및 서버측 전달](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-gdpr.md)
               + [서버측 전달 요구 사항](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-requirements.md)
               + [서버측 전달 데이터 및 코드 참조](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-reference.md)
               + [서버측 전달 구현 확인 방법](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-verify.md)
               + [서버측 전달 FAQ](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-faq.md)
         + 트래픽 {#traffic-variables}
            + [트래픽 변수](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/traffic-var.md)
            + [트래픽 분류](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/traffic-classifications.md)
            + [사용자 정의 보고서 설명](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/custom-desc-admin.md)
         + 전환 {#conversion-variables}
            + [전환 변수](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-var-admin.md)
            + [검색 방법](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/finding-methods.md)
            + [전환 분류](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-classifications.md)
            + 고유 방문자 변수 {#unique-visitor-variable}
               + [고유 방문자 변수 지정](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/unique-visitor-variable-admin/t-unique-visitor-variable.md)
               + [사용 사례 - 방문자 ID 추출](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/unique-visitor-variable-admin/extract-visitorids-usecase.md)
            + 성공 이벤트 {#success-events}
               + [성공 이벤트 개요](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/success-event.md)
               + [성공 이벤트 구성](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/t-success-events.md)
               + [이벤트 유형 변경 정보](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/event-type.md)
            + [분류 계층](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/classification-hierarchies.md)
            + [목록 변수](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/list-var-admin.md)
            + [머천다이징 eVar](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/merchandising-evars.md)
         + 마케팅 채널 {#marketing-channels}
            + [마케팅 채널 관리자](admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-channels.md)
            + [마케팅 채널 처리 규칙](admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-rules.md)
            + [마케팅 채널 분류](admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/classifications-mchannel.md)
            + [마케팅 채널 만료](admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/visitor-engagement.md)
         + 트래픽 관리 {#traffic-management}
            + [개요](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-management/traffic-management.md)
            + [스파이크 예약](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-management/t-traffic-schedule-spike.md)
            + [영구 트래픽](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-management/t-traffic-permanent.md)
         + [기본 지표](admin/c-manage-report-suites/c-edit-report-suites/default-metrics.md)
         + 앱 관리 {#app-management}
            + [앱 보고](admin/c-manage-report-suites/c-edit-report-suites/app-reporting.md)
            + [앱 분류](admin/c-manage-report-suites/c-edit-report-suites/app-classifications.md)
         + [미디어 관리](admin/c-manage-report-suites/c-edit-report-suites/media-management.md)
         + [Activity Map](admin/c-manage-report-suites/c-edit-report-suites/activity-map.md)
         + [AEM](admin/c-manage-report-suites/c-edit-report-suites/adobe-experience-manager.md)
         + [Adobe Campaign](admin/c-manage-report-suites/c-edit-report-suites/adobe-campaign.md)
         + [개인정보 보호 보고](admin/c-manage-report-suites/c-edit-report-suites/privacy-reporting.md)
         + Document Cloud 관리 {#doc-cloud-mgt}
            + [Adobe Analytics로 Document Cloud 구성](admin/c-manage-report-suites/c-edit-report-suites/document-cloud-mgt.md)
            + [Document Cloud 보고 구성](admin/c-manage-report-suites/c-edit-report-suites/document-cloud-config.md)
         + [Advertising Analytics 구성](admin/c-manage-report-suites/c-edit-report-suites/advertising-analytics-config.md)
         + 실시간 {#real-time-reports}
            + [실시간 보고서 개요](admin/c-manage-report-suites/c-edit-report-suites/realtime/realtime.md)
            + [실시간 보고서 구성](admin/c-manage-report-suites/c-edit-report-suites/realtime/t-realtime-admin.md)
            + [지원되는 실시간 지표 및 차원](admin/c-manage-report-suites/c-edit-report-suites/realtime/realtime-metrics.md)
      + [보고서 세트 관리](admin/c-manage-report-suites/report-suites-admin.md)
      + [롤업 및 글로벌 보고서 세트](admin/c-manage-report-suites/rollup-report-suite.md)
      + [보고서 세트 검색 저장](admin/c-manage-report-suites/t-report-suite-saved-search.md)
      + [보고서 세트 설정 다운로드](admin/c-manage-report-suites/t-download-rs-settings.md)
      + 새 보고서 세트 {#c-new-report-suite}
         + [보고서 세트 만들기](admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md)
         + [보고서 세트 그룹 만들기](admin/c-manage-report-suites/c-new-report-suite/t-create-rs-group.md)
         + [새 보고서 세트 - 설정](admin/c-manage-report-suites/c-new-report-suite/new-report-suite.md)
         + [소스 보고서 세트에서 복사되지 않은 설정](admin/c-manage-report-suites/c-new-report-suite/settings-not-copied-from-rs.md)
      + 보고서 세트 템플릿 {#report-suite-templates}
         + [보고서 세트 템플릿 개요](admin/c-manage-report-suites/c-report-suite-templates/report-suite-templates.md)
         + [애그리게이터 포털](admin/c-manage-report-suites/c-report-suite-templates/aggregator-portal.md)
         + [상거래](admin/c-manage-report-suites/c-report-suite-templates/commerce-admin.md)
         + [콘텐츠 및 미디어](admin/c-manage-report-suites/c-report-suite-templates/content-media.md)
         + [기본 템플릿](admin/c-manage-report-suites/c-report-suite-templates/default-rs-template.md)
         + [금융 서비스](admin/c-manage-report-suites/c-report-suite-templates/financial-services.md)
         + [구직 포털](admin/c-manage-report-suites/c-report-suite-templates/job-portal.md)
         + [리드 생성](admin/c-manage-report-suites/c-report-suite-templates/lead-generation.md)
         + [지원 미디어](admin/c-manage-report-suites/c-report-suite-templates/support-media.md)
   + 회사 설정 {#company-settings}
      + [회사 설정 개요](admin/company/c-company-settings.md)
      + [보안 관리자](admin/company/security-manager.md)
      + [웹 서비스](admin/company/web-services-admin.md)
      + [Report Builder 보고서](admin/company/report-builder-reports-admin.md)
      + [SSO(Single Sign-On)](admin/company/single-signon-admin.md)
      + [보고서 세트 숨기기](admin/company/c-hide-report-suites.md)
      + [환경 설정 관리자](admin/company/preferences-manager.md)
      + [보류 중인 작업](admin/company/pending-actions-admin.md)
      + [기능 액세스 수준](admin/company/feature-access-levels.md)
   + 데이터 거버넌스 개인 정보 보호 레이블 {#data-governance}
      + [Adobe Analytics 데이터 개인정보 보호 워크플로](admin/c-data-governance/an-gdpr-workflow.md)
      + [자주 묻는 질문](admin/c-data-governance/gdpr-faq.md)
      + 데이터 레이블 지정 {#data-labels}
         + [Analytics 구성 요소의 데이터 개인정보 보호 레이블](admin/c-data-governance/data-labeling/gdpr-labels.md)
         + [보고서 세트 데이터에 레이블 지정](admin/c-data-governance/data-labeling/gdpr-setup-reportsuite.md)
         + [보고서 세트의 개인정보 보호 레이블 보기/관리](admin/c-data-governance/data-labeling/gdpr-view-settings.md)
         + [레이블 지정 모범 사례](admin/c-data-governance/data-labeling/gdpr-analytics-ids.md)
         + [레이블 지정 예](admin/c-data-governance/data-labeling/gdpr-labeling-example.md)
         + [네임스페이스](admin/c-data-governance/data-labeling/gdpr-namespaces.md)
      + [ID 확장](admin/c-data-governance/gdpr-id-expansion.md)
      + [CNIL 동의 면제](admin/c-data-governance/cnil-consent-exemption.md)
   + 서버 호출 사용량 {#server-call-usage}
      + [서버 호출 사용량 개요](admin/c-server-call-usage/overage-overview.md)
      + [현재 서버 호출 사용량 보기](admin/c-server-call-usage/server-call-usage-dashboard.md)
      + [보고서 세트 사용량 보기](admin/c-server-call-usage/report-suite-usage.md)
      + [서버 호출 사용량 경고](admin/c-server-call-usage/scu-alerts.md)
      + [서버 호출 사용량 FAQ](admin/c-server-call-usage/overage-faq.md)
   + 사용자 및 제품 관리(기존) {#user-product-management}
      + [사용자 및 제품 관리(기존)](admin/user-management2/user-management.md)
      + [사용자 자산 전송 또는 계정 만료 설정](admin/user-management2/users-assets.md)
      + Adobe Admin Console로 사용자 마이그레이션 {#migrate-users}
         + [Admin Console로 Analytics 사용자 마이그레이션](admin/user-management2/user-migration/c-migration-tool.md)
         + [Adobe ID에 대한 Analytics 사용자 계정 마이그레이션](admin/user-management2/user-migration/t-migrate-users.md)
         + [Enterprise 및 Federated ID에 대한 Analytics 사용자 계정 마이그레이션](admin/user-management2/user-migration/migrate-enterprise.md)
         + [기존 로그인 비활성화](admin/user-management2/user-migration/t-disable-legacy-login.md)
         + [마이그레이션의 영향을 받는 API](admin/user-management2/user-migration/developer.md)
+ [관리 API](c-admin-api/c-admin-api.md)

