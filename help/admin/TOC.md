---
product: analytics
audience: admin
user-guide-title: Analytics 관리 안내서
breadcrumb-title: 관리 안내서
user-guide-description: Experience Cloud Admin Console에서의 사용자 및 제품 관리, 보고서 세트 구성 등과 같은 Analytics 관리 작업에 대해 알아봅니다.
source-git-commit: 35675c2e65456a175d1516dd421b80d2af809286
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 99%

---


# Adobe Analytics 관리 안내서 {#admin}

+ [Analytics 관리 안내서](home.md)
+ [Analytics 릴리스 정보](https://experienceleague.adobe.com/ko/docs/analytics/release-notes/latest)
+ Adobe Admin Console {#admin-console}
   + [개요](admin-console/home.md)
   + [Adobe Analytics 첫 번째 관리 안내서](admin-console/first-admin-guide.md)
   + [Adobe Analytics의 관리자 역할](admin-console/admin-roles-in-analytics.md)
   + Analytics 도구 권한 요약 {#permissions}
      + [Adobe Analytics의 제품 프로필](admin-console/permissions/product-profile.md)
      + [보고서 세트 도구에 대한 제품 프로필 권한](admin-console/permissions/report-suite-tools.md)
      + [Analytics 도구에 대한 제품 프로필 권한](admin-console/permissions/analytics-tools.md)
+ Analytics 관리 도구 {#admin-tools}
   + [관리 도구 개요](tools/c-admin-tools.md)
   + [코드 관리자](tools/code-manager-admin.md)
   + [Analytics 인벤토리](tools/analytics-inventory.md)
   + [데이터 소스](tools/data-sources.md)
   + [IP 주소로 제외](tools/exclude-ip.md)
   + [로그](tools/logs.md)
   + 보고 활동 관리자 {#reporting-activity-manager}
      + [개요](tools/reporting-activity-manager/reporting-activity-overview.md)
      + [보고 활동 보기](tools//reporting-activity-manager/reporting-activity.md)
      + [보고 요청 취소](tools/reporting-activity-manager/reporting-activity-cancel-requests.md)
   + 구성 요소 마이그레이션 {#component-migration}
      + [마이그레이션 준비](tools/component-migration/prepare-component-migration.md)
      + [마이그레이션 워크플로](tools/component-migration/component-migration.md)
   + 보고서 세트 관리자 {#manage-report-suites}
      + 보고서 세트의 설정 편집 {#edit-report-suite}
         + 일반 {#report-suite-general}
            + [일반 계정 설정](tools/manage-rs/edit-settings/general/general-acct-settings-admin.md)
            + [내부 URL 필터](tools/manage-rs/edit-settings/general/internal-url-filter-admin.md)
            + [사용자 정의 캘린더](tools/manage-rs/edit-settings/general/custom-calendar.md)
            + 유료 검색 감지 {#paid-search-detection}
               + [유료 검색 감지 개요](tools/manage-rs/edit-settings/general/paid-search-detection/paid-search-detection.md)
               + [유료 검색 감지 구성](tools/manage-rs/edit-settings/general/paid-search-detection/t-paid-search-detection.md)
            + 처리 규칙 {#processing-rules}
               + [개요](tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md)
               + [인터페이스](tools/manage-rs/edit-settings/general/processing-rules/pr-interface.md)
               + [기록 보기](tools/manage-rs/edit-settings/general/processing-rules/pr-view-history.md)
               + [규칙 복사](tools/manage-rs/edit-settings/general/processing-rules/pr-copy.md)
               + [사용 가능한 차원 및 지표](tools/manage-rs/edit-settings/general/processing-rules/pr-variables.md)
               + [사용 사례](tools/manage-rs/edit-settings/general/processing-rules/pr-use-cases.md)
            + 보트 규칙 {#bot-removal}
               + [보트 제거](tools/manage-rs/edit-settings/general/bot-removal/bot-removal.md)
               + [보트 규칙 이해 및 구성](tools/manage-rs/edit-settings/general/bot-removal/bot-rules.md)
               + [일반 보트 서명](tools/manage-rs/edit-settings/general/bot-removal/bot-signatures.md)
               + [보트 제외 방법](tools/manage-rs/edit-settings/general/bot-removal/bot-exclusion-methods.md)
            + [개인정보 보호 설정](tools/manage-rs/edit-settings/general/privacy-settings.md)
            + [타임스탬프 구성](tools/manage-rs/edit-settings/general/timestamp-configuration.md)
            + 서버측 전달 {#server-side-forwarding}
               + [서버측 전달 개요](tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf.md)
               + [GDPR/ePrivacy 준수 및 서버측 전달](tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf-gdpr.md)
               + [서버측 전달 요구 사항](tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf-requirements.md)
               + [서버측 전달 데이터 및 코드 참조](tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf-reference.md)
               + [서버측 전달 구현 확인 방법](tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf-verify.md)
               + [서버측 전달 FAQ](tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf-faq.md)
         + 트래픽 {#traffic-variables}
            + [트래픽 변수](tools/manage-rs/edit-settings/c-traffic-variables/traffic-var.md)
            + [트래픽 분류](tools/manage-rs/edit-settings/c-traffic-variables/traffic-classifications.md)
            + [사용자 정의 보고서 설명](tools/manage-rs/edit-settings/c-traffic-variables/custom-desc-admin.md)
         + 전환 {#conversion-variables}
            + [전환 변수](tools/manage-rs/edit-settings/conversion-var-admin/conversion-var-admin.md)
            + [검색 방법](tools/manage-rs/edit-settings/conversion-var-admin/finding-methods.md)
            + [전환 분류](tools/manage-rs/edit-settings/conversion-var-admin/conversion-classifications.md)
            + 고유 방문자 변수 {#unique-visitor-variable}
               + [고유 방문자 변수 지정](tools/manage-rs/edit-settings/conversion-var-admin/unique-visitor-variable-admin/t-unique-visitor-variable.md)
               + [사용 사례 - 방문자 ID 추출](tools/manage-rs/edit-settings/conversion-var-admin/unique-visitor-variable-admin/extract-visitorids-usecase.md)
            + [성공 이벤트](tools/manage-rs/edit-settings/conversion-var-admin/c-success-events/success-event.md)
            + [분류 계층](tools/manage-rs/edit-settings/conversion-var-admin/classification-hierarchies.md)
            + [목록 변수](tools/manage-rs/edit-settings/conversion-var-admin/list-var-admin.md)
            + [머천다이징 eVar](tools/manage-rs/edit-settings/conversion-var-admin/merchandising-evars.md)
         + 마케팅 채널 {#marketing-channels}
            + [마케팅 채널 관리자](tools/manage-rs/edit-settings/marketing-channels/c-channels.md)
            + [마케팅 채널 처리 규칙](tools/manage-rs/edit-settings/marketing-channels/c-rules.md)
            + [마케팅 채널 분류](tools/manage-rs/edit-settings/marketing-channels/classifications-mchannel.md)
            + [마케팅 채널 만료](tools/manage-rs/edit-settings/marketing-channels/visitor-engagement.md)
         + 트래픽 관리 {#traffic-management}
            + [개요](tools/manage-rs/edit-settings/c-traffic-management/traffic-management.md)
            + [스파이크 예약](tools/manage-rs/edit-settings/c-traffic-management/t-traffic-schedule-spike.md)
            + [영구 트래픽](tools/manage-rs/edit-settings/c-traffic-management/t-traffic-permanent.md)
         + [기본 지표](tools/manage-rs/edit-settings/default-metrics.md)
         + 앱 관리 {#app-management}
            + [앱 보고](tools/manage-rs/edit-settings/app-reporting.md)
            + [앱 분류](tools/manage-rs/edit-settings/app-classifications.md)
         + [미디어 관리](tools/manage-rs/edit-settings/media-management.md)
         + [Activity Map](tools/manage-rs/edit-settings/activity-map.md)
         + [AEM](tools/manage-rs/edit-settings/adobe-experience-manager.md)
         + [Adobe Campaign](tools/manage-rs/edit-settings/adobe-campaign.md)
         + [개인 정보 보호 보고](tools/manage-rs/edit-settings/privacy-reporting.md)
         + Document Cloud 관리 {#doc-cloud-mgt}
            + [Adobe Analytics로 Document Cloud 구성](tools/manage-rs/edit-settings/document-cloud-mgt.md)
            + [Document Cloud 보고 구성](tools/manage-rs/edit-settings/document-cloud-config.md)
         + [Advertising Analytics 구성](tools/manage-rs/edit-settings/advertising-analytics-config.md)
         + 실시간 {#real-time-reports}
            + [실시간 보고서 개요](tools/manage-rs/edit-settings/realtime/realtime.md)
            + [실시간 보고서 구성](tools/manage-rs/edit-settings/realtime/t-realtime-admin.md)
            + [지원되는 실시간 지표 및 차원](tools/manage-rs/edit-settings/realtime/realtime-metrics.md)
      + [보고서 세트 관리](tools/manage-rs/report-suites-admin.md)
      + [글로벌 보고서 세트](tools/manage-rs/rollup-report-suite.md)
      + [보고서 세트 검색 저장](tools/manage-rs/t-report-suite-saved-search.md)
      + [보고서 세트 설정 다운로드](tools/manage-rs/t-download-rs-settings.md)
      + 새 보고서 세트 {#c-new-report-suite}
         + [보고서 세트 만들기](tools/manage-rs/new-rs/t-create-a-report-suite.md)
         + [보고서 세트 그룹 만들기](tools/manage-rs/new-rs/t-create-rs-group.md)
         + [새 보고서 세트 - 설정](tools/manage-rs/new-rs/new-report-suite.md)
         + [소스 보고서 세트에서 복사되지 않은 설정](tools/manage-rs/new-rs/settings-not-copied-from-rs.md)
      + 보고서 세트 템플릿 {#report-suite-templates}
         + [보고서 세트 템플릿 개요](tools/manage-rs/rs-templates/report-suite-templates.md)
         + [애그리게이터 포털](tools/manage-rs/rs-templates/aggregator-portal.md)
         + [상거래](tools/manage-rs/rs-templates/commerce-admin.md)
         + [콘텐츠 및 미디어](tools/manage-rs/rs-templates/content-media.md)
         + [기본 템플릿](tools/manage-rs/rs-templates/default-rs-template.md)
         + [금융 서비스](tools/manage-rs/rs-templates/financial-services.md)
         + [구직 포털](tools/manage-rs/rs-templates/job-portal.md)
         + [리드 생성](tools/manage-rs/rs-templates/lead-generation.md)
         + [지원 미디어](tools/manage-rs/rs-templates/support-media.md)
   + 회사 설정 {#company-settings}
      + [회사 설정 개요](tools/company/c-company-settings.md)
      + [보안 관리자](tools/company/security-manager.md)
      + [웹 서비스](tools/company/web-services-admin.md)
      + [Report Builder 보고서](tools/company/report-builder-reports-admin.md)
      + [SSO (Single Sign-On)](tools/company/single-signon-admin.md)
      + [보고서 세트 숨기기](tools/company/c-hide-report-suites.md)
      + [환경 설정 관리자](tools/company/preferences-manager.md)
      + [보류 중인 작업](tools/company/pending-actions-admin.md)
      + [기능 액세스 수준](tools/company/feature-access-levels.md)
   + 개인정보 보호 라벨링 {#privacy-labeling}
      + [개요](tools/privacy-labeling/labeling-overview.md)
      + [Analytics 구성 요소의 데이터 개인 정보 보호 레이블](tools/privacy-labeling/labels.md)
      + [보고서 세트의 개인 정보 보호 레이블 보기/관리](tools/privacy-labeling/view-settings.md)
      + [레이블 지정 모범 사례](tools/privacy-labeling/best-practices.md)
      + [레이블 지정 예](tools/privacy-labeling/examples.md)
      + [네임스페이스](tools/privacy-labeling/namespaces.md)
   + 서버 호출 사용량 {#server-call-usage}
      + [서버 호출 사용량 개요](tools/server-call-usage/overage-overview.md)
      + [현재 서버 호출 사용량 보기](tools/server-call-usage/server-call-usage-dashboard.md)
      + [보고서 세트 사용량 보기](tools/server-call-usage/report-suite-usage.md)
      + [서버 호출 사용량 경고](tools/server-call-usage/scu-alerts.md)
      + [서버 호출 사용량 FAQ](tools/server-call-usage/overage-faq.md)
   + 사용자 및 제품 관리 (기존) {#user-product-management}
      + [사용자 및 제품 관리 (기존)](tools/user-management/user-management.md)
      + [기존 사용자 계정, 자산 및 만료 관리](tools/user-management/users-assets.md)
      + Adobe Admin Console로 사용자 마이그레이션 {#migrate-users}
         + [Admin Console로 Analytics 사용자 마이그레이션](tools/user-management/user-migration/c-migration-tool.md)
         + [Adobe ID에 대한 Analytics 사용자 계정 마이그레이션](tools/user-management/user-migration/t-migrate-users.md)
         + [Enterprise 및 Federated ID에 대한 Analytics 사용자 계정 마이그레이션](tools/user-management/user-migration/migrate-enterprise.md)
         + [기존 로그인 비활성화](tools/user-management/user-migration/t-disable-legacy-login.md)
         + [마이그레이션의 영향을 받는 API](tools/user-management/user-migration/developer.md)
+ [관리 API](c-admin-api/c-admin-api.md)
+ [Adobe Analytics 1.4 API EOL FAQ](c-admin-api/c-admin-14-api-eol.md)

