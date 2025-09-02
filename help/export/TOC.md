---
product: analytics
audience: end-user
user-guide-title: Analytics 내보내기 안내서
breadcrumb-title: 내보내기 안내서
user-guide-description: 데이터 피드 및 Data Warehouse을 사용하여 데이터 출력을 검색하는 방법에 대해 알아봅니다.
source-git-commit: 9131c9ffbcf409620a67b36637367af22733b909
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 95%

---


# Adobe Analytics 내보내기 안내서 {#export}

+ [Analytics 내보내기 안내서](home.md)
+ [Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html)
+ Analytics 데이터 피드 {#analytics-data-feed}
   + [데이터 피드 개요](analytics-data-feed/data-feed-overview.md)
   + [데이터 피드 만들기](analytics-data-feed/create-feed.md)
   + [데이터 피드 관리](analytics-data-feed/df-manage-feeds.md)
   + [데이터 피드 작업 관리](analytics-data-feed/df-manage-jobs.md)
   + 데이터 피드 콘텐츠 {#data-feed-contents}
      + [데이터 피드 콘텐츠 개요](analytics-data-feed/c-df-contents/datafeeds-contents.md)
      + [지표 계산](analytics-data-feed/c-df-contents/datafeeds-calculate.md)
      + [데이터 열 참조](analytics-data-feed/c-df-contents/datafeeds-reference.md)
      + [페이지 이벤트 조회](analytics-data-feed/c-df-contents/datafeeds-page-event.md)
      + [동적 조회](analytics-data-feed/c-df-contents/dynamic-lookups.md)
      + [머천다이징 eVar 조회](analytics-data-feed/c-df-contents/merchandising-evar-lookup.md)
      + [특수 문자](analytics-data-feed/c-df-contents/datafeeds-spec-chars.md)
      + [늦게 도착하는 히트](analytics-data-feed/c-df-contents/late-arriving-hits.md)
   + [데이터 피드 FAQ](analytics-data-feed/df-faq.md)
   + [데이터 피드 모범 사례](analytics-data-feed/data-feeds-best-practices.md)
   + [데이터 피드 문제 해결](analytics-data-feed/troubleshooting.md)
+ Data Warehouse {#data-warehouse}
   + [Data Warehouse 개요](data-warehouse/data-warehouse.md)
   + [Data Warehouse 사용자 그룹 추가](data-warehouse/t-dw-group.md)
   + Data Warehouse 요청 만들기 {#dw-create-request}
      + [Data Warehouse 요청 만들기](/help/export/data-warehouse/create-request/t-dw-create-request.md)
      + [일반 설정](/help/export/data-warehouse/create-request/dw-general-settings.md)
      + [보고서 작성](/help/export/data-warehouse/create-request/dw-request-build-report.md)
      + [보고서 대상](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)
      + [보고서 옵션](/help/export/data-warehouse/create-request/dw-request-report-options.md)
      + [예약 옵션](/help/export/data-warehouse/create-request/dw-request-scheduling.md)
      + [알림 이메일](/help/export/data-warehouse/create-request/dw-request-email.md)
   + [게재 시간 요청](data-warehouse/delivery-time.md)
   + [타블로 데이터 파일](data-warehouse/t-tableau.md)
   + [지표로 정렬](data-warehouse/sorting-by-metric.md)
   + [Data Warehouse 요청 관리](data-warehouse/data-warehouse-requests-manage.md)
   + [Data Warehouse에서 지원되는 구성 요소](data-warehouse/component-support.md)
   + [Data Warehouse 모범 사례](data-warehouse/data-warehouse-bp.md)
+ FTP 및 SFTP {#ftp-and-sftp}
   + [Adobe Experience Cloud와 FTP 및 SFTP 사용](ftp-and-sftp/ftp-overview.md)
   + Adobe에서 호스팅하는 FTP 계정 설정 {#set-up-ftp-accounts}
      + [FTP 계정 설정 - 개요](ftp-and-sftp/c-set-up-ftp-accounts/ftp-accounts.md)
      + [분류](ftp-and-sftp/c-set-up-ftp-accounts/ftp-saint.md)
      + [데이터 소스](ftp-and-sftp/c-set-up-ftp-accounts/ftp-datasources.md)
      + [데이터 피드](ftp-and-sftp/c-set-up-ftp-accounts/ftp-datafeeds.md)
      + [Data Warehouse 게재된 보고서](ftp-and-sftp/c-set-up-ftp-accounts/ftp-dw-reports.md)
      + [Report Builder 게재된 보고서](ftp-and-sftp/c-set-up-ftp-accounts/ftp-arb-reports.md)
      + [FTP로 엔지니어링 서비스 참여](ftp-and-sftp/c-set-up-ftp-accounts/ftp-eng-services.md)
   + [FTP 제한 및 데이터 보존](ftp-and-sftp/ftp-limits.md)
   + [FTP 데이터 및 FTP 계정 삭제](ftp-and-sftp/ftp-delete.md)
   + [삭제된 FTP 데이터 및 FTP 계정 복원](ftp-and-sftp/ftp-restore.md)
   + [Adobe FTP 서버 업그레이드](ftp-and-sftp/ftp-upgrade.md)
   + [수동 FTP 모드 사용](ftp-and-sftp/ftp-passive.md)
   + [FTP 처리 시간](ftp-and-sftp/ftp-processing.md)
   + SFTP (Secure File Transfer Protocol) {#secure-file-transfer-protocol}
      + [SFTP 서비스 업그레이드 - FAQ](ftp-and-sftp/c-sftp/sftp-upgrade.md)
      + [Secure File Transfer Protocol - 개요](ftp-and-sftp/c-sftp/ftp-sftp.md)
      + [SFTP를 통해 Adobe FTP 계정에 연결](ftp-and-sftp/c-sftp/ftp-sftp-connect.md)
      + [SFTP를 통해 외부 FTP 계정으로 Adobe 데이터 보내기](ftp-and-sftp/c-sftp/ftp-sftp-transfer.md)
      + [SFTP 서버로 Data Warehouse 요청 보내기](ftp-and-sftp/c-sftp/ftp-sftp-dw.md)
      + [SFTP를 통해 암호 없이 Adobe에 연결](ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md)
+ [Analysis Workspace 다운로드](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/download-send.html)
+ [Adobe Analytics API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html)
+ [Report Builder](https://experienceleague.adobe.com/ko/docs/analytics/analyze/report-builder/rb-overview)
